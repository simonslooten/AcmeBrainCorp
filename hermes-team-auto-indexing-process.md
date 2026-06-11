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
├── evernote/
└── other/
```

- Drop new files into the appropriate subfolder under `raw_input/`
- **Evernote exports: Use .enex format** (not PDF). The entire automation pipeline (Git hook → tung_tung → companion .md notes) is built and optimized for .enex. PDF exports lose structure, tags, metadata, and make accurate conversion much harder.

## Key Principles
- **.enex is the required format** for Evernote notebook exports. PDF is only acceptable as a supplementary visual backup, never as the primary input for processing.
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
- **bonica**: Quality review + **blocked task fixer** (standard part of the workflow)

**Mandatory rules:**
- tung_tung must **not** mark a task complete without notifying grok-coo.
- After any real processing work (especially the first few files), a retro must be run with bonica.
- Review must be done by a different agent — no self-review.
- tung_tung should only work on **one file at a time** unless explicitly approved by grok-coo. If the load is too high, additional agents should be brought in.

When tung_tung processes a task for a non-markdown file, they:
1. Create a companion `.md` note
2. Add link/embed to the original file
3. Write summary + key information
4. Add tags and frontmatter (`processed: true`)
5. Notify bonica that the task is ready for review
6. Move the task to review

**bonica's responsibilities after review:**
- Perform quality check
- Commit and push all changes (`git add -A && git commit && git push`)
- Move the task to complete
5. Move the task to complete

## File Type Handling

| File Type     | Action by tung_tung                          | Result                              |
|---------------|----------------------------------------------|-------------------------------------|
| `.pdf`        | Extract text + create summary note           | `Report.pdf` → `Report.pdf.md`      |
| `.docx`       | Extract text + create summary note           | Companion `.md` note                |
| `.xlsx`       | Extract key data + create structured note    | Companion `.md` note                |
| Images        | Describe + tag                               | Companion `.md` note                |
| `.md`         | Normal indexing                              | Direct processing                   |
| `.enex`       | Parse Evernote XML (ENML), extract notes/metadata, create rich companion .md (frontmatter + summary + links + tags + processed: true) | `post 5-6-26.enex` → `Evernote/post-5-6-26.md` |

---

This version now includes the `raw_input/` ingestion area, makes the agents responsible for creating companion `.md` notes, and adds explicit `.enex` (Evernote) handling per Phase 1 conversion spec in t_72642295.