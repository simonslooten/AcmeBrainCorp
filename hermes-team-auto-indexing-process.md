# Hermes_Team Vault Auto-Indexing Process

**Goal**: Automatically detect new `.md` files added by Simon to `/Users/marvin/documents/ObsidianVault/Hermes_Team`, create corresponding tasks on the Hermes Kanban board (default board), and route them to the appropriate agent for processing with minimal manual intervention. The vault is Git-synced.

**Key Principles**
- Git-driven triggers for reliability (post-commit hook).
- Tasks always appear on Kanban board first.
- Existing team agents used where possible; new lightweight role only if needed.
- Processing is idempotent and observable.
- COO (grok-coo) owns setup and oversight; quality-auditor (bonica) owns final review.

## Triggers

1. **Primary: Git Post-Commit Hook** (recommended, reliable, low-overhead)
   - Location: `.git/hooks/post-commit` in the Hermes_Team repo.
   - Script detects newly added `.md` files:
     ```bash
     #!/bin/bash
     NEW_FILES=$(git diff --name-only HEAD~1 HEAD | grep '\.md$' || true)
     for file in $NEW_FILES; do
       if [[ "$file" == *.md && ! $(git show HEAD:"$file" | grep -q "^processed: true") ]]; then
         hermes kanban create \
           --title "Index new note: $(basename "$file" .md)" \
           --body "New file added: $file\n\nPlease process: tag, summarize, link, extract actionables. See [[hermes-team-auto-indexing-process]].\n\nFile path: /Users/marvin/documents/ObsidianVault/Hermes_Team/$file" \
           --assignee tung_tung \
           --board default \
           --metadata '{"source":"git-hook","vault":"Hermes_Team","file":"'$file'"}'
       fi
     done
     ```
   - Make executable: `chmod +x .git/hooks/post-commit`
   - Runs automatically on every commit by Simon (or Obsidian Git plugin auto-commit).

2. **Fallback / Periodic**: Cron or launchd job (every 15-30 min)
   - Scans for unprocessed `.md` files (no `processed: true` in frontmatter or missing `#indexed` tag).
   - Creates Kanban tasks for any missed by hook.
   - Script: `~/scripts/hermes-vault-index-watcher.sh`

3. **Manual trigger**: `hermes kanban create` with the same template (used by COO or Simon via Telegram `/kanban`).

## Agent Ownership & Routing

- **grok-coo (COO)**: Owns the overall process, sets up hooks/cron, monitors Kanban for stuck tasks, runs retros via 8-points.
- **tung_tung (research-generalist)**: Primary owner of indexing tasks. Handles deep processing of new notes.
  - If volume high, decompose into sub-tasks or add lightweight "note-indexer" profile later.
- **bonica (quality-auditor)**: Reviews completed indexing tasks, runs 8-point retro, ensures links/tags are high quality.
- **Other agents** (as needed): Route sub-tasks (e.g. copy-writer for polishing summaries).

**Kanban Task Lifecycle**:
- Created in `todo` (or `triage` if using `specify`/`decompose`).
- tung_tung claims → processes → `complete` with handoff (summary of changes, links added, tags).
- If blocked → `block` with reason.
- COO can `reassign`, `unblock`, or `archive`.

## New Note Processing Steps (by tung_tung)

When a task is claimed:

1. **Read the note** (use obsidian skill / `read_file` on absolute path).
2. **Add frontmatter** (if missing):
   ```yaml
   ---
   created: <iso-date>
   processed: true
   processed_at: <iso-datetime>
   tags: [hermes-team, <domain-tag>, ...]
   aliases: []
   ---
   ```
3. **Generate & apply tags**:
   - Use #hashtags and/or frontmatter `tags:`.
   - Domain tags: #meeting, #idea, #decision, #research, #action, #project-hermes, etc.
   - Always include #hermes-team and #indexed.
4. **Create summary**:
   - Add or update `## Summary` section (2-4 sentences).
   - Extract key entities, decisions, action items.
5. **Add wikilinks & connections**:
   - Search existing vault for related notes (`search_files`).
   - Insert `[[Existing Note]]` and `[[New Note|alias]]` where semantically relevant.
   - Update any MOC (Map of Content) or Index notes (e.g. add to `memories/` or root index).
6. **Extract & create follow-up tasks** (optional but encouraged):
   - If action items found, create child Kanban tasks or new notes with `[[...]]`.
7. **Commit changes** (via Git or let Obsidian Git handle; prefer small commits).
8. **Handoff on Kanban**:
   - `kanban_complete` with metadata: `{"tags_added": [...], "links_added": [...], "summary": "...", "issues": null}`.

## Sustainability & Minimal Manual Work

- Hook ensures near-real-time creation of tasks.
- Idempotency via `processed: true` frontmatter check prevents duplicates.
- All processing produces observable Kanban artifacts (comments, metadata).
- Periodic watcher catches any edge cases (manual file adds outside Git, etc.).
- No new heavy infrastructure; reuses existing `hermes kanban` CLI, obsidian skill, Git, and team profiles.
- Future enhancement: Integrate Obsidian Git plugin "post backup" command to also trigger the hook.

## Setup Checklist (COO owns)

- [x] Create this note.
- [ ] Install Git hook (post-commit script above).
- [ ] Test with a sample new note.
- [ ] Add cron/launchd for watcher if needed.
- [ ] Brief tung_tung and bonica on the process (via Kanban task or chat).
- [ ] Monitor first 10 notes; refine tags/linking rules.

**Related Notes**: [[8-points-self-improvement]], [[grok-coo_SOUL]], vault Git config in .obsidian.

*Process designed for reliability, agent collaboration, and zero ongoing manual indexing by Simon.*
