# Steal/skip brief — @0xMovez Jev 10-steps

Tags: `#onepager #steal-skip #park #movez #typesafe #process`
**Date:** 2026-09-21 ~18:26 CEST  
**To:** CoS (mirror to Simon NL/EN as needed)  
**Post:** https://x.com/0xMovez/status/2101007482919227841  
**Author:** @0xMovez (Movez) · X Article  
**Metrics (fetch):** ~413k impress · 581 likes · 1,181 bookmarks · 78 RTs · 30 replies · 18 quotes  
**Created:** 2026-09-18 19:56 CEST  
**X credits after:** free_balance ~$49.79 (pre-fetch check)

---

## 1) What the post actually argues (concrete, not vibes)

X Article: **"Jev Engineering: how to build the fastest AI Agent Brain in 10 Steps (Full-Setup)"**.

Thesis: agents burn frontier LLM tokens on forks that never needed generation (yes/no, pick next worker, score relevance). Split the stack:

- **LLM** → research / plan / write text  
- **Jev (TypeSafe System One)** → typed decisions only: Choice / Score / Noul (+ confidence)  
- **Code** → exact rules, execution, stop conditions  

10 concrete steps:

| # | Tip | Concrete move |
|---|-----|----------------|
| 01 | Split | Mark each agent step as text / decision / rule; only decisions → Jev |
| 02 | Playground | Test one Choice on real state in TypeSafe Playground before any code |
| 03 | SDK | Install `typesafe-sdk`, API key, optional skill pack |
| 04 | Handoff | `chief.py` writes local JSON jobs into `queue/{research\|write\|review}` with choice + confidence |
| 05 | Primitives | Choice (pick), Score (scale), Noul (P(yes)); put real criteria in instructions; batch Qs on same state |
| 06 | Dynamic menu | Rebuild option list every turn from *currently available* workers/controls (Browser Use pattern) |
| 07 | Parallel | Many questions in one call; don't chain independent Qs; search first if Q needs fresh evidence |
| 08 | Guardrails | Action + spend ceilings; save progress; escalate on low confidence; **completion check ≠ decision confidence** (verify DONE separately) |
| 09 | Cost | Vendor: ~$0.042 / M input, $0 output; track **$/completed task**, not $/decision |
| 10 | Deploy | Five demos: browser control, paper classify, inbox triage, model router, context compaction |

Vendor claims (unverified by us): ~200× faster / ~400× cheaper vs LLM on System One tasks.

---

## 2) Map vs GB/GX stack

| Tip | Our analogue | Label | Note |
|-----|--------------|-------|------|
| 01 Split text / decide / rule | GB ops vs GX long-form; interrupt = money/product; material do/park; Bonica gate | **already have** | Same philosophy. Formal typed layer is the delta. |
| 02 Playground before code | Rung-6; Shoopy earn-scope; prove before cron | **already have** | Don't schedule unproven Jev paths. |
| 03 Install TypeSafe SDK | Hire bar; cash-first; existing Jev one-pager (2026-09-20) = **park** | **skip** | Tip-swarm product signup. Simon yes required. |
| 04 JSON local queues (`chief.py`) | Bridge INBOX/STATE/PROTOCOL; Shoopy **one CoS approval queue** | **already have** / **conflict** if duplicated | Do **not** stand up a parallel JSON queue beside bridge. |
| 05 Choice / Score / Noul + confidence thresholds | Interrupt money/product; do-alone vs park; Bonica CLEAR | **steal** (process only) | Encode thresholds in charters ("if unsure → park") without buying Jev. |
| 06 Dynamic menu from live availability | CoS routing + Movez **attention list** (live opens, not Monday intentions) | **steal** (light) | Refresh worker/option set from live roster/attention, not stale org chart. |
| 07 Parallel batch questions | Soft fan-out gate; Lirili cost; token lean | **conflict** if copied onto GB | On Jev API, batch is cheap; on Grok Bot, parallel = waste. Keep fan-out soft. |
| 08 Ceilings + kill + completion ≠ confidence | Shoopy ceilings / kill / Friday / one-queue; Lirili spend; material tape | **already have** + **steal** nuance | Steal: "confident Choice ≠ file saved / mail sent" → separate verify step. |
| 09 $/completed task | Lirili Cost hygiene weekly | **already have** | Keep; ignore vendor multiples until we measure. |
| 10a Browser Use / flight demo | computerUse idle waste is our *problem*, not a Jev install | **skip** | |
| 10b Paper classify / knipsel-style | knipselkrant (Bombardino→CoS ≤5); research classify | **skip** for Jev | Knipsel already capped; no new classifier bot. |
| 10c Inbox triage | LN open-card triage (outplacement vs 2e-spoor etc.) — named cash candidate in Jev one-pager | **steal** (parked spike only) | Reopen only with labeled cards + success criteria. |
| 10d Model router cheap→strong | GB short ops / GX long draft (ORG load-split) | **already have** | Don't wrap in LangChain AutoModeMiddleware. |
| 10e Context compaction via Jev scores | GX long threads; memory dumps | **skip / watch** | Interesting; no cash until measured. |

Cross-ref locked stack: Shoopy six rules · Movez ops (attention / stale-data / rung-6) · material output bar · hire bar · Lirili Friday · bridge GX · knipselkrant · `typesafe-ai-jev-onepager-2026-09-20.md`.

---

## 3) Verdict (cash impact rank) — implement **nothing** without Simon yes

**Do not tip-swarm.** This post is a fuller how-to of a product we already parked 2026-09-20.

### If anything later (ranked by cash)

1. **Highest cash (still PARK):** Bounded **LN open-card triage** spike — Choice/Score-style gates *in our code or a trial Jev call* on labeled cards **before** expensive computerUse. Success = accuracy + $/card vs current path. Owner: CoS + La Vaca; Lirili measures cost.  
2. **Process steal, $0 product:** Add charter line **"decision confidence ≠ side-effect proof"** (save/send/DONE verify separate). Fits Shoopy + material bar.  
3. **Process steal, $0:** Dynamic menu — CoS routes from **live available** specialists + attention list, not static roster.  
4. **Optional narrative (ABC, not ops):** "puber chat vs calibrated decide" for agency-before-lock-in content — Bombardino/Tralalero only if Simon wants.

### Explicitly NOT to do

- Install TypeSafe SDK / API key / skills pack  
- Clone `chief.py` JSON queues next to bridge  
- LangChain AutoModeMiddleware / ModelRouterMiddleware on GB  
- Browser Use flight-demo play / tip-10 five-way deploy binge  
- New decision-layer bot (hire bar)  
- Treat 200×/400× or $0.042/M as our facts  
- Reopen full Jev integration on tip energy ahead of Tuesday Optimus / BD / CH cash

**Standing verdict unchanged:** complement-idea, not install. Park. Reopen only for LN/CoS spike with criteria, or paying ABC client ask.

---

## 4) Tape

- **Sources:** X MCP `user-X--simon-s-private-account` `get_usage_credits` + `get_posts_by_id` 2101007482919227841 (article.plain_text); `/workspace/GB-org/typesafe-ai-jev-onepager-2026-09-20.md`; `movez-ops-rules-2026-09-17.md`; `shoopy-hygiene-gb-gx-2026-09-20.md`; `material-output-bar-2026-09-16.md`; `kloss-20tips-cost-hygiene-2026-09-16.md`; `gb-bot-hire-bar-2026-09-20.md`; knipselkrant brief; `bridge/ORG.md`; Lirili `cost-hygiene/weekly-latest.md`.  
- **Guesses:** Vendor speed/cost multiples and demo $ figures — marketing, not our benchmark. Namespace catalog said `user-X` but invoke needs `user-X--simon-s-private-account`.  
- **Skipped:** `search_posts_all`; replies/quotes fetch (not needed — full article in post payload); live TypeSafe API trial; messaging Simon; posting on X; any implementation.  
- **Evidence:** this file; raw article text via MCP article.plain_text field.
