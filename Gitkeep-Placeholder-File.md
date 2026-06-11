---
title: ".gitkeep Placeholder File"
created: 2026-06-11
processed: true
tags: [system, git, placeholder, auto-index]
---

# .gitkeep

`.gitkeep` is a conventional empty (or near-empty) file used to preserve empty directories in Git repositories (since Git does not track empty directories by default).

**Not a content file** — purely a Git hygiene / placeholder artifact. Should be excluded from content processing pipelines.

**Detected locations:** 
- `raw_input/docx/.gitkeep` (processed earlier)
- `raw_input/pdf/.gitkeep` (processed earlier)
- `raw_input/images/.gitkeep` (this task)

**Action taken:** 
- Created this companion note
- Moved originals to `processed/other/.gitkeep`, `processed/other/.gitkeep-pdf`, and `processed/other/.gitkeep-images` respectively

**Note:** All `.gitkeep` files are identical placeholder artifacts.

**Recommendation:** Update the Git post-commit hook and file detection logic to automatically ignore `.gitkeep` files (add to `.gitignore` patterns if needed, and skip Kanban task creation for them).

**processed: true**