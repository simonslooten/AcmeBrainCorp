# Prinsjesdag 2026 — begroting 2027

Downloaded from official Dutch government sources on 2026-09-15 (UTC). This is the complete staging tree prepared for transfer to the two requested macOS destinations.

## Sources

- Miljoenennota + begrotingen bundle: <https://open.overheid.nl/documenten/3cfdedbd-ed54-49f5-980a-2623e41d31de>
- Belastingplan bundle: <https://open.overheid.nl/documenten/6149e1f7-6c4e-49af-a0ed-f6262ee57512>
- Document hub: <https://www.rijksoverheid.nl/themas/overheid-en-democratie/prinsjesdag/miljoenennota-belastingplan-begrotingen-en-bijbehorende-stukken>
- Troonrede page: <https://www.rijksoverheid.nl/documenten/2026/09/15/troonrede-2026>

## Inventory

- `00-zip-miljoenennota-begrotingen/`: `miljoenennota-begrotingen-2027.zip` — valid ZIP, 41,060,472 bytes; 33 extracted files.
- `00-zip-belastingplan/`: `belastingplan-2027.zip` — valid ZIP, 39,023,532 bytes; 36 extracted files.
- `01-miljoenennota/`: 4 official hub PDFs.
- `02-begrotingen/`: 20 official hub PDFs.
- `03-fondsen/`: 9 official hub PDFs.
- `04-belastingplan/`: 35 official hub PDFs.
- `05-overig/`: 2 official hub PDFs plus `troonrede-2026-source.html`.
- `06-ja21/`: 1 pre-existing JA21 PDF retained.
- Official hub PDFs: 70; all 140 PDFs in the tree begin with `%PDF-` and exceed 10 kB.
- `hub-pdf-sources.tsv` records each hub PDF's source URL and local path.

Total staging-tree inventory: **145 files, 281,957,202 bytes (282.0 MB)**, including README and source manifest.

## Troonrede

The supplied Troonrede page publishes the complete speech as HTML and exposes no official PDF binary/link. The fetched official HTML is retained as `05-overig/troonrede-2026-source.html`; no unofficial PDF was fabricated.

## Requested destinations

The requested macOS paths were not mounted or writable in this execution environment, so the tree is staged at:

`/workspace/Prinsjesdag-2026-begroting-2027/`

It still needs to be copied to:

- `/Users/marvin/Documents/Work/Prinsjesdag-2026-begroting-2027/`
- `/Users/marvin/Documents/ObsidianVault/Hermes_Team/Prinsjesdag-2026-begroting-2027/`
