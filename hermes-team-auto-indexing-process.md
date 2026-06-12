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
5. Send a message to bonica with the file name and ask her to create a review + commit task for herself
6. Move the task to review

**bonica's responsibilities after review:**
- Perform quality check
- Commit and push all changes (`git add -A && git commit && git push`)
- Move the task to complete

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

## Recurring Scanner Task (Bonica-owned)

**Primary intelligence lives in a recurring Kanban task assigned to bonica:**

- Task title: "Scan raw_input/ and create processing tasks"
- Assignee: bonica
- Status: ready (re-created after each run)

**When bonica runs the scanner task she:**
1. Scans the entire `raw_input/` tree recursively
2. Skips `.gitkeep` and `.DS_Store`
3. For every unprocessed file (no companion `.md` + no `processed: true` marker):
   - Creates a **tung_tung** task (status: ready) for that specific file
   - Creates a **bonica** review task in status `Todo (waiting on dependencies)` that depends on tung_tung's task
4. After tung_tung finishes, bonica's review task becomes unblocked
5. Bonica performs the 8-point retro, commits, pushes, and completes both tasks
6. Re-creates the scanner task so the cycle continues

This approach keeps all logic with the agents (no intelligence in cron jobs) and works reliably across machines because the scanner task itself is the source of truth.

Current scanner task: t_cb2580be (created 2026-06-11)
## Handling Failed Processing Tasks

When a tung_tung processing task crashes repeatedly (protocol violations, agent crashes, etc.):

- Archive the blocked task and its dependent review task
- Create a new task with smaller scope / explicit micro-task guidance
- Document the failure reason in the new task body

Example: t_c6859d8e (Prisma IT - Strategy 2015.enex) was archived after 4 crashes. Replaced by t_bcb55149 with explicit instruction to break the work into smaller steps if needed.

## Long-Term Memory from Vault (Added 2026-06-12)

**Policy**: The Hermes_Team Obsidian vault is the primary long-term memory and single source of truth for all agents in the coo profile.

### Option 1 – Always-available vault access
- The `obsidian` skill is considered pre-approved and always loadable for any agent that needs vault context.
- Absolute vault path (coo profile): `/Users/marvin/Documents/ObsidianVault/Hermes_Team`
- Agents may use `search_files`, `read_file`, and `patch` directly on this path without additional approval when the task involves process docs, SOUL files, memories, or indexing work.
- `OBSIDIAN_VAULT_PATH` should be set in the profile `.env` (when writable) as documentation.

### Option 2 – Automatic vault → memory ingestion
- Key vault documents (hermes-team-auto-indexing-process.md, SOUL.md files, Hermes Indexing Dashboard.md, memories/*) are the source of truth.
- When these files change, bonica is responsible for syncing relevant excerpts into the profile's `memories/` directory so they are automatically injected on every turn.
- No intelligent cron jobs — the trigger is either the existing post-commit hook or an explicit bonica "memory sync" task created after substantial vault changes.
- tung_tung creates companion notes; bonica performs the memory sync + review + commit/push.

This ensures agents have up-to-date vault knowledge without manual `skill_view` calls on every turn.

**SSOT Rule**: Any change to this memory policy or the ingestion workflow must be reflected in this document first.

## Memory Sync Task (bonica-owned)

When the post-commit hook detects changes to key long-term memory documents (hermes-team-auto-indexing-process.md, Hermes Indexing Dashboard.md, vault memories/*.md, or any *SOUL.md), it automatically creates a task for bonica:

- Title: "Memory sync: vault → profile memories/"
- Status: Todo (waiting on dependencies) — created in the waiting lane
- Assignee: bonica

**bonica's responsibilities on this task:**
1. Read the changed vault documents
2. Extract the relevant, stable, high-value excerpts (process rules, ownership, key facts)
3. Update or append to the corresponding files in `~/.hermes/profiles/coo/memories/`
4. Perform quality review
5. Commit + push the profile memory changes
6. Move the task to complete

This task is created in addition to (not instead of) the normal review task for raw_input files.

**Rule**: tung_tung never self-reviews memory sync work. bonica always owns the final memory injection.

## Memory Excerpt Template (for bonica memory-sync tasks)

When syncing from vault to `~/.hermes/profiles/coo/memories/`, use this format. Keep excerpts short, stable, and high-signal only.

**Template structure** (one section per memory file):

```
### [Topic / File]

- Key fact / rule: [one sentence]
- Owner: [agent or role]
- Last updated: [date from vault doc]
- Source: [[hermes-team-auto-indexing-process.md]] (or other vault link)
```

**Rules for excerpts:**
- Only include items that will actually change agent behaviour on future turns.
- Never copy entire sections — extract the minimal stable truth.
- If the excerpt would be longer than 4–5 bullets, split it into a new memory file instead.
- After syncing, always run the 8-point retro if the change was substantial.

Example (for this document):

```
### Long-term Memory Policy

- Key fact / rule: The Hermes_Team vault is the primary long-term memory source for the coo profile.
- Owner: grok-coo (policy) + bonica (execution)
- Last updated: 2026-06-12
- Source: [[hermes-team-auto-indexing-process.md]]
```
