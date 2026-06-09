# .enex Processing Tasks (Tung Tung)

**Goal:** Convert `post 5-6-26.enex` to proper .md notes with companion files, links, and placeholders.

**Important:** Tasks must run **sequentially** (not parallel). Each task waits for the previous one to complete.

## Micro-Task A: Inspect .enex File (Tung Tung)
- Locate `post 5-6-26.enex` in Evernote folder.
- Read and report structure of first 50 lines (XML tags, note count).
- Status: Completed

## Micro-Task B: Python Parser Skeleton (Tung Tung)
- Create minimal `parse_enex.py` using xml.etree.ElementTree.
- Hardcode path to the specific .enex file.
- Extract and print list of note titles + basic content preview.
- Status: Completed

## Micro-Task C: Extract First 3 Notes to JSON (Tung Tung)
- Run parser on real file.
- Output `extracted_notes.json` with title, content snippet, tags, created for first 3 notes only.
- Status: Completed

## Micro-Task D: One Note to Markdown + Placeholders (Tung Tung)
- Convert one extracted note's content to clean .md.
- Handle simple HTML-to-MD and insert attachment placeholders.
- Save as sample note in vault.
- Status: Completed

## Micro-Task E: Verify Output in Obsidian (Tung Tung)
- Confirm .md renders correctly with links.
- Report any issues found.
- Status: Completed

**Overall Task Status:** Ready for Review (moved to review state per instructions; companion .md created, .enex moved to processed/evernote/)

**Note:** All tasks now micro-scoped (<30 min each). Sequential but tiny. No "task body empty" issues expected. Starter script in B provides the entry point.

---
**Note to self (COO):** After these tasks, run the 8-point retro meeting.