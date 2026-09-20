# Memory vault protocol — sustainable 40+ yr notes

**Status:** draft for Simon via CoS · 2026-09-20  
**Owner:** Archivaris (vault) · CoS routes · specialists domain-slice only  
**Goal:** one durable brain bots can use without dead weight — bodies when real, stubs never invented.

---

## 1. Three layers

| Layer | What | Path / store | Rule |
|-------|------|--------------|------|
| **Cold** | Immutable exports & originals | `Hermes_Team/processed/evernote/*.enex` (+ future docs/mail exports) | Never edit. Source of truth for rehydrate. |
| **Working vault** | Searchable markdown bots actually read | `Hermes_Team/Evernote/live/` (+ project folders under Hermes) | Only notes that pass the **body-gate**. June ENEX converts stay as archive companions under `Hermes_Team/Evernote/<notebook>/`. |
| **Agent memory** | Short, durable facts per bot | Agent profile / memory (GB) · GX bridge when CoS says | Facts & pointers only — not full note dumps. Prefer vault path + one-line why. |

Working vault is the live Evernote convert. Cold is ENEX/exports. Agent memory must not duplicate whole notebooks.

---

## 2. Import body-gate (no invent)

A note may enter / stay **Working** with a usable body only if at least one of:

1. **Offline search extract** (`Offline_Search_Note_Content`) has real text, or  
2. **`.dat` / ENML / ENEX body** yields extractable prose (not empty-shell chrome), or  
3. **Fresh ENEX / UI export** supplies the body.

Otherwise write a **stub**: YAML + title + honest flags (`deleted`, `body_source`, `body_detail`). **Never invent body text.**

Body-gate failure is not a bug when local store is empty (example: trash shell with `content_size` ~100 and offline length 0). Mark it; leave it.

**Do not** full re-convert the live tree unless CoS/Simon asks.

---

## 3. MOC (map of content)

- Prefer Obsidian search on `Hermes_Team/Evernote` over a giant top-level dump.  
- Keep / refresh a thin `_MOC` only where it earns place (e.g. project packs, Grok dumps INDEX).  
- CoS standing: no mandatory top-level `Evernote/_MOC.md` — search is enough for the big tree.  
- Every import batch: one short INDEX line (date, source, note count, gaps).

---

## 4. Retrieval-on-demand

Default: **do not** load notebooks into agent context.

1. Named project or CoS names a topic → Archivaris finds **one note or one notebook slice**.  
2. Return path + short excerpt / summary sourced from the file.  
3. Optional copy into that project’s Work folder; **vault remains the keep place**.  
4. Private bodies stay **held** unless CoS opens them. JA21 stays with Archivaris unless CoS opens.

---

## 5. Who may query

| Actor | Access |
|-------|--------|
| **Archivaris** | Vault owner: find, verify, file, rehydrate from cold when gate allows. |
| **CoS** | Routes asks; delivers to Simon; opens Private/JA21 when needed. |
| **Specialists** | Domain-slice only (path CoS/Archivaris already filed for that project). No full-library crawl. |
| **Simon** | Always; CoS is the ping channel for vault status. |

---

## 6. Evernote stub hygiene

Facts from 2026-09-20 GB-Mac diagnose (see CoS thread):

- `live/` **2098** `.md` files, **105** notebooks, **369** with `deleted: true` (2026-09-20 re-check, GB-Mac); many stubs are **trash/empty shells** (`deleted: true`, tiny `.dat`, offline 0) — not silently wiped active bodies.  
- Most notes already use `body_source: offline_search` with text.  
- Example: `live/Special Guitars/Dance Planet.md` — **title-only stub / no Offline_Search prose** (`body_source: dat`, `deleted: true`; deleted 2026-06-17; offline length 0; empty-shell `.dat`).

**Parked pending Simon A/B (CoS widget):**  
- **A** — document/segregate empty `deleted`+`dat` stubs (e.g. `live/_trash/` or keep flags only).  
- **B** — UI/ENEX export for notebooks where Simon insists bodies still exist in Evernote cloud.  

Archivaris does **not** start A or B until CoS confirms Simon’s pick.

---

## 7. Phased intake (Evernote → docs → mail)

| Phase | Source | Working target | Cold |
|-------|--------|----------------|------|
| **0 done** | June ENEX set (10 notebooks) | `Hermes_Team/Evernote/<notebook>/` | `processed/evernote/*.enex` |
| **1 done (partial)** | Local Evernote sync → markdown | `Hermes_Team/Evernote/live/` | keep ENEX; optional future Trash/UI export |
| **2 next** | Docs (Drive / Work packs) | Hermes project folders + thin INDEX | export snapshots as needed |
| **3 later** | Mail (labeled / project) | Hermes project or `mail/` archive | .eml / Takeout — only on ask |

Each phase: body-gate → INDEX line → no full dump into agent memory.

---

## 8. Park — ENEX notebook list (Simon)

Companion file: `enex-notebook-park-list-2026-09-20.md` (same folders). Cold set under `Hermes_Team/processed/evernote/`. June convert note counts are companions under `Hermes_Team/Evernote/` (not `live/`).

---

## Tape

**Sources**

- CoS architecture ask 2026-09-20 (Cold / Working / Agent memory; body-gate; MOC; retrieval; who may query; stub hygiene; phased intake).  
- Paths: `Hermes_Team/Evernote/live/`, `Hermes_Team/processed/evernote/`, `Work/GB-org/`, `Hermes_Team/GB-org/`.  
- Diagnose 2026-09-20 GB-Mac (re-check): Dance Planet id `404adcd1-2f0e-9413-5455-1931cd93167d`; RemoteGraph + Offline_Search + `.dat`; live **2098** `.md` / 105 notebooks / 369 `deleted: true`; ENEX listing via `ls` + note counts via `<note>` tags / convert folders.  
- Prior vault standing orders (Archivaris owner; no invent; report to CoS only).

**Guesses**

- If UI still shows body for some stubs, body may be cloud-only / not in local Offline or `.dat` — not verified via Evernote UI this draft.  
- Phase 2–3 shapes are directional until Simon names first doc/mail packs.

**Skipped**

- No A/B stub hygiene execution (waiting CoS confirm).  
- No full re-convert. No invented bodies. No Auth/token. No Simon ping from Archivaris.  
- No Evernote UI walk for cloud-only bodies this pass.

**Evidence:** N/A (filesystem + SQLite only).

---

## 8-punten (short)

1 Truth — stubs reflect title-only / no Offline_Search prose where flagged, not invented loss.  
2 Real problem — bots drowning in dead weight vs missing bodies where cold still has them.  
3 Clarity — three layers + body-gate.  
4 Minimal force — retrieval-on-demand; no full re-convert.  
5 Bias — “broken vault” ≠ every stub; many are trash/empty.  
6 Human overhead — A/B parked for Simon; Archivaris waits.  
7 Competitive — ENEX cold + searchable working beats proprietary-only.  
8 Compound — body-gate + INDEX each batch so year-40 vault stays lean.

**Best-possible-version action:** After Simon’s A/B pick, run only that bounded hygiene; then Phase 2 first doc pack when CoS names it.
