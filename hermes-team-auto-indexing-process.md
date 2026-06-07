# Hermes_Team Vault Auto-Indexing Process (All-File)

**Goal**: Automatically detect files added to the `raw_input/` folder, create Kanban tasks, and have the agents generate companion `.md` notes for non-markdown files. Original files stay in `raw_input/`, while processed `.md` notes live in the main vault area.

The vault is Git-synced between computers.

## Folder Structure

```
raw_input/
├── pdf/
├── docx/
├── xlsx/
├── images/
└── other/
```

- Drop new files into the appropriate subfolder under `raw_input/`
- Agents will create companion `.md` notes (usually at root or in `notes/`)
- Original files remain untouched in `raw_input/`

## Key Principles
- Git-driven triggers (post-commit hook) for reliability
- Every new file → Kanban task first
- Agents create companion `.md` notes for non-markdown files
- Use existing agents where possible
- Idempotent and observable
- COO owns the overall system; quality-auditor owns final review

## Triggers

### 1. Primary: Git Post-Commit Hook (recommended)
Location: `.git/hooks/post-commit`

The hook detects new files in `raw_input/` and creates a Kanban task assigned to tung_tung.

### 2. Fallback
Periodic scan for unprocessed files in `raw_input/`.

## Agent Ownership & Companion Note Creation

- **grok-coo**: Overall process owner
- **tung_tung**: Primary owner — creates companion `.md` notes for files in `raw_input/`
- **bonica**: Quality review

When tung_tung processes a task for a non-markdown file, they:
1. Create a companion `.md` note
2. Add link/embed to the original file
3. Write summary + key information
4. Add tags and frontmatter (`processed: true`)
5. Move the task to complete

## File Type Handling

| File Type     | Action by tung_tung                          | Result                              |
|---------------|----------------------------------------------|-------------------------------------|
| `.pdf`        | Extract text + create summary note           | `Report.pdf` → `Report.pdf.md`      |
| `.docx`       | Extract text + create summary note           | Companion `.md` note                |
| `.xlsx`       | Extract key data + create structured note    | Companion `.md` note                |
| Images        | Describe + tag                               | Companion `.md` note                |
| `.md`         | Normal indexing                              | Direct processing                   |

---

This version now includes the `raw_input/` ingestion area and makes the agents responsible for creating companion `.md` notes.