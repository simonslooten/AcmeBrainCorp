---
title: ".DS_Store System File"
created: 2026-06-11
processed: true
tags: [system, macos, ignore, auto-index]
---

# .DS_Store

macOS system file (`Desktop Services Store`) that stores folder-specific view settings and metadata. 

**Not a content file** — should be excluded from Git, backups, and note processing pipelines.

**Detected location:** `raw_input/.DS_Store`

**Action taken:** 
- Created this companion note
- Moved original to `processed/other/.DS_Store`

**Recommendation:** Update the Git post-commit hook and file detection logic to automatically ignore `.DS_Store` files (add to `.gitignore` if not already present, and skip in Kanban task creation).

**processed: true**