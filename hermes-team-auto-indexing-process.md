# Hermes_Team Vault Auto-Indexing Process (All-File)

**Goal**: Automatically detect **any new file** added by Simon to the Hermes_Team vault (`.md`, `.pdf`, `.docx`, `.xlsx`, `.txt`, images, etc.), create a task on the Hermes Kanban board, and route it to the right agent(s) for processing with minimal manual work.

The vault is Git-synced between computers.

## Key Principles
- Git-driven triggers (post-commit hook) for reliability
- Every new file → Kanban task first (no silent processing)
- Use existing agents where possible
- File-type aware processing (notes vs documents vs media)
- Idempotent and observable
- COO owns the overall system; quality-auditor owns final review

## Triggers

### 1. Primary: Git Post-Commit Hook (recommended)
Location: `.git/hooks/post-commit`

```bash
#!/bin/bash
# Detect all new or modified files in the last commit
NEW_FILES=$(git diff --name-only HEAD~1 HEAD || true)

for file in $NEW_FILES; do
    # Skip already processed files
    if git show HEAD:"$file" | grep -q "^processed: true"; then
        continue
    fi

    EXT="${file##*.}"
    TITLE="Index new file: $(basename "$file")"

    hermes kanban create \
        --title "$TITLE" \
        --body "New file added: $file\n\nExtension: .$EXT\n\nPlease process according to file type. See [[hermes-team-auto-indexing-process]].\n\nFile path: /Users/marvin/documents/ObsidianVault/Hermes_Team/$file" \
        --assignee tung_tung \
        --board default \
        --metadata "{\"source\":\"git-hook\",\"vault\":\"Hermes_Team\",\"file\":\"$file\",\"ext\":\"$EXT\"}"
done
```

Make it executable:
```bash
chmod +x .git/hooks/post-commit
```

### 2. Fallback
Cron/launchd job every 15–30 min that scans for files without `processed: true` in frontmatter (or a `.processed` sidecar file for non-markdown files).

### 3. Manual
`hermes kanban create` with the same template.

## File-Type Routing & Processing

| File Type       | Primary Agent     | Processing Steps                                                                 | Output                          |
|-----------------|-------------------|----------------------------------------------------------------------------------|---------------------------------|
| `.md`           | tung_tung        | Tag, summarize, wikilink, update MOCs                                            | Updated note + Kanban complete  |
| `.pdf`, `.docx` | tung_tung        | Extract text (OCR if needed), create summary note, tag                           | New `.md` companion note        |
| `.xlsx`, `.csv` | tung_tung        | Extract key data/tables, create structured summary note                          | New `.md` + optional data note  |
| Images          | tung_tung        | Describe content, extract text if present, tag                                   | New `.md` description note      |
| `.txt`, other   | tung_tung        | Basic ingestion + tagging                                                        | New or updated `.md`            |

**General rules**:
- Every file gets a Kanban task assigned to `tung_tung` initially.
- `tung_tung` can decompose or reassign sub-tasks.
- Non-markdown files usually result in a companion `.md` note (e.g. `Report.pdf` → `Report.pdf.summary.md` or embedded in a note).
- All processed files get `processed: true` (frontmatter for `.md`, sidecar file for others).

## Agent Ownership
- **grok-coo**: Overall process owner, hook setup, monitoring
- **tung_tung**: Primary indexer (all file types)
- **bonica**: Quality review of completed indexing tasks
- **Other agents**: Used by tung_tung when needed (e.g. copy-writer for summaries)

## Kanban Task Lifecycle
1. Task created automatically on file addition
2. tung_tung claims → processes according to file type
3. Marks complete with summary of what was done
4. bonica reviews (optional but recommended for important files)

---

**Next setup steps**:
1. Install the post-commit hook
2. Test with one `.md` and one non-markdown file
3. Add fallback watcher if needed

This version replaces the previous markdown-only design.