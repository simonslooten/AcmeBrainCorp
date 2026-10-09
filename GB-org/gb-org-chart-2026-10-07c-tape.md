# Tape — gb-org-chart-2026-10-07c

### Mission Contract
- **Result:** rev c FLAG fix — full ORG name strings, Stalk→La Vaca handoff path, sunset chip nit
- **Inputs:** ORG.md (7 Oct ~09:35) + Bonica FLAG notes via Bombardino on rev b
- **Output:** pdf/png/tape + Hermes staging copies
- **Schedule:** one-shot FLAG fix 7 Oct ~09:41–09:45 CEST
- **Definition of done:** A4 landscape; pdftotext hits `La Vaca Saturno Saturnita` + `Cappuccino Assassino` + `CareerHandling`; handoff from Stalk→La Vaca (not Tung/Balerina); sunset chip not double-rendered; Hermes copies present
- **Constraints:** no Simon ping; no agent messages; files only
- **Approval gates:** Bonica CLEAR via Bombardino before DONE

### Tape
- **Sources:**
  - `/workspace/GB-org/ORG.md` (updated 2026-10-07 ~09:35 — GX sunset HAL/Marvin/Jarvis; Stalk CH-intel = stippellijn handoff → La Vaca, geen rapportagelijn)
  - `/workspace/GB-org/gb-org-chart-2026-10-07b.pdf` + `.png` + `gen_org_chart_b.py` (rev b FAIL baseline)
  - Bonica FLAG via Bombardino: truncated names; handoff path toward Tung/Balerina forbidden; sunset double-render nit
- **Guesses:**
  - Layout geometry only (box widths, La Vaca–Brr corridor gap, peer bus span, Balerina x). No seat/role guesses.
  - One-line full name for La Vaca (fits at 6.4pt in W=96) chosen over two-line wrap so pdftotext verify regex hits the contiguous literal string.
- **Skipped:**
  - **Avatar/group strip** — same as rev b: no curated groepsfoto; unlabeled hashed assets would clutter A4. Do not invent portraits.
  - Messaging other agents / Simon (explicit: files only).
- **Evidence:**
  - PDF: `/workspace/GB-org/gb-org-chart-2026-10-07c.pdf`
    - `pdfinfo` Page size: **841.89 x 595.276 pts (A4)** landscape
  - PNG: `/workspace/GB-org/gb-org-chart-2026-10-07c.png` — 2047×1447 px @ 175 DPI via pdftocairo
  - Tape: `/workspace/GB-org/gb-org-chart-2026-10-07c-tape.md`
  - Generator: `/workspace/GB-org/gen_org_chart_c.py` (fork of `_b.py`)
  - Hermes staging:
    - `/workspace/vault-staging/Hermes_Team/GB-org/gb-org-chart-2026-10-07c.pdf`
    - `/workspace/vault-staging/Hermes_Team/GB-org/gb-org-chart-2026-10-07c.png`
    - `/workspace/vault-staging/Hermes_Team/GB-org/gb-org-chart-2026-10-07c-tape.md`
  - **pdftotext proof (FLAG names):**
    ```
    $ pdftotext …07c.pdf - | grep -E 'La Vaca Saturno Saturnita|Cappuccino Assassino|CareerHandling'
    La Vaca Saturno Saturnita
    CareerHandling
    Cappuccino Assassino
    ```
    No ellipsis (`…`) chars in PDF text. Rev b had `Saturno Saturni…` / `areerHandling` / `ccino Assassino` (box off left edge + draw_box truncate).
  - **Handoff from-node / to-node (PDF pts, origin bottom-left):**
    - from-node **Stalk Bot** top-center: `(516.0, 88.0)`
    - to-node **La Vaca Saturno Saturnita** right-mid: `(108.0, 385.3)`
    - waypoints: `(516.0, 88.0) → (516.0, 120.0) → (119.5, 120.0) → (119.5, 385.3) → (108.0, 385.3)`
    - path_y=120 (low gap, well below Tung/Balerina at y≈385); vertical rise at x≈119.5 in La Vaca–Brr corridor (clears Cappuccino under La Vaca); label on Stalk–La Vaca horizontal segment
    - Stalk cx=516 vs Tung/Balerina x=562 (Δx=−46; Stalk not under Tung)
  - **Sunset chip check:** HAL/Marvin/Jarvis = role `sunset` inside dashed muted box only; external chip removed. `pdftotext | grep -c '^sunset$'` → **3** (was 6 in rev b = role+chip duplicate).
  - Keep (Pass): BPV Chimpanzini left (right=393 < x_drop=407); Bonica on CoS-bus (cx=446, Δx vs Chim=+95); GX sunset dimmed+dashed; bridge not under CoS; 7 peers; Frigo footer; Hermes staging; avatar skip.
- **Handoff:** Artifact paths above → CoS. Exact next = Bonica CLEAR via Bombardino, then CoS shows Simon. No Simon ping from this run.
- **Self-critique:**
  1. **Name truncation killed:** Root cause was BD row clamped off the left page edge (La Vaca cx≈13.5 → left=−29) *plus* `draw_box` ellipsis. Fix: keep bd_left≥12; widen La Vaca (W=96) + Cappuccino (W=94); `allow_truncate=False` shrinks font instead of cutting. pdftotext now shows full literals.
  2. **Handoff path corrected:** Rev b horizontal hugged BD row and visually read toward Tung/Balerina; vertical under Stalk aligned with Tung. Rev c: short rise from Stalk → left across low gap → up in La Vaca–Brr corridor → into La Vaca right-mid. Not a reporting line; label “CH site intel (handoff, not reporting)” on that segment.
  3. **Sunset nit:** Removed duplicate external `chip="sunset"`; role text inside box retained (3 standalone `sunset` lines).
