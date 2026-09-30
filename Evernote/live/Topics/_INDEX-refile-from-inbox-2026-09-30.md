---
title: INDEX refile from _INBOX 2026-09-30
source: archivaris-vault-hygiene
date: 2026-09-30
tags: [archivaris, vault-hygiene, evernote-refile]
---

# Refile from Evernote `_INBOX` → `Topics/` — 2026-09-30

Owner: Archivaris (Simon Slooten vault). Pass: subject/topic grouping of Evernote dump notebook `_INBOX`.

## Constraints honored
- Stayed inside `Evernote/live/` — no moves into/out of GB-org, Acme Social Media Posts (top-level project), JA21/ (top-level), CareerHandling/, family/, job-search/, Prinsjesdag-*, Grok-GrokBot-memory/.
- Prefer thin folders under `Evernote/live/Topics/<slug>/` over deep trees / inventing giant taxonomy.
- Prefer Topics/ over merging into historical Evernote notebook folders (e.g. `AI - Grok`, `JA21 - *`).
- Conservative: ambiguous notes left in `_INBOX`.
- No note-body invention / tip-swarm.

## Inventory (pre-move)
- `_INBOX` markdown notes: **436** (excl. nothing; includes `_index.md` if present)
- Size buckets (approx from earlier scan): tiny&lt;350B ~98; mid 350–800 ~116; large&gt;800 ~222
- Many notes use `body_source: dat` / `offline_search` stubs; bodies often truncated/held.

### Sibling dump-like notebooks (inventory only — not mass-moved this pass)
| Notebook | .md count | Notes |
|---|---:|---|
| Checken | 3 | tiny urgency pile — leave |
| Default Notebook | 93 | large dump-like — leave for later pass |
| Keep watching | 2 | tiny — leave |
| Read Later | 10 | leave |
| Home Tasks | 1 | leave |
| _No_Notebook | 2 | leave |
| Simon's notebook | 120 | personal notebook, not treated as dump this pass |
| Algemeen archive | 227 | archive, not dump |

## Taxonomy (10 thin folders under `Evernote/live/Topics/`)

| Folder | Intent | Suggested YAML tags |
|---|---|---|
| `Topics/x-open-loops/` | X/Twitter & urgency open-loops (Kijken!!!, Superbelangrijk!, later-watch link dumps). Not agent memory. | `topic: x-open-loops`, `source: evernote-inbox` |
| `Topics/ai-grok/` | AI tools, Grok prompts, agents, AI training notes from inbox dump. | `topic: ai-grok`, `source: evernote-inbox` |
| `Topics/cash-bd-career/` | CareerHandling / SSL self-sell / job search / BD / lead-gen / LinkedIn. | `topic: cash-bd-career`, `source: evernote-inbox` |
| `Topics/ja21/` | JA21-related notes found in _INBOX (kept under Evernote Topics — NOT top-level Hermes_Team/JA21/). | `topic: ja21`, `source: evernote-inbox` |
| `Topics/geopolitics-curiosity/` | News clips / geopolitics / general curiosity reading (Telegraaf, NRC, AD, etc.). | `topic: geopolitics-curiosity`, `source: evernote-inbox` |
| `Topics/guitars-gear/` | Special Guitars, instruments, synths, music gear. | `topic: guitars-gear`, `source: evernote-inbox` |
| `Topics/home-life/` | House (Bermweg), travel, cars, photo gear, home logistics. | `topic: home-life`, `source: evernote-inbox` |
| `Topics/kids-school/` | Kids (Siem), school (Emmaus), family logistics. | `topic: kids-school`, `source: evernote-inbox` |
| `Topics/gifts-kadoos/` | Gift ideas, Kerstcadeaus, bestellingen. | `topic: gifts-kadoos`, `source: evernote-inbox` |
| `Topics/health/` | Health-named notes (Gezondheid, Ozempic, CORONA). | `topic: health`, `source: evernote-inbox` |

Optional frontmatter tags were **not bulk-written** this pass (move-only to avoid tip-swarm). Tags can be added in a later pass.

## Pre-move classification counts (high-confidence)
- `x-open-loops`: 24 notes
- `ai-grok`: 8 notes
- `cash-bd-career`: 26 notes
- `ja21`: 50 notes
- `geopolitics-curiosity`: 18 notes
- `guitars-gear`: 25 notes
- `home-life`: 16 notes
- `kids-school`: 9 notes
- `gifts-kadoos`: 6 notes
- `health`: 3 notes
- **Total planned moves:** 185
- **Leave in `_INBOX` (ambiguous / FVD-legacy / Untitled non-X / stubs):** 251

## Move map

*Appended as groups are moved.*


## Moves executed 2026-09-30 10:16 

### `x-open-loops` — 24 moved

- `_INBOX/Belangrijk te onthouden.md` → `Topics/x-open-loops/Belangrijk te onthouden.md`
- `_INBOX/Deze doen.md` → `Topics/x-open-loops/Deze doen.md`
- `_INBOX/Deze.md` → `Topics/x-open-loops/Deze.md`
- `_INBOX/Doen!!.md` → `Topics/x-open-loops/Doen!!.md`
- `_INBOX/In de gaten houden.md` → `Topics/x-open-loops/In de gaten houden.md`
- `_INBOX/Kijken echt serieus zeket doen.md` → `Topics/x-open-loops/Kijken echt serieus zeket doen.md`
- `_INBOX/Kijken!! (2).md` → `Topics/x-open-loops/Kijken!! (2).md`
- `_INBOX/Kijken!!!.md` → `Topics/x-open-loops/Kijken!!!.md`
- `_INBOX/Kijken!!.md` → `Topics/x-open-loops/Kijken!!.md`
- `_INBOX/Kijken.md` → `Topics/x-open-loops/Kijken.md`
- `_INBOX/Laten afdrukken.md` → `Topics/x-open-loops/Laten afdrukken.md`
- `_INBOX/Lezen.md` → `Topics/x-open-loops/Lezen.md`
- `_INBOX/links.md` → `Topics/x-open-loops/links.md`
- `_INBOX/Nuttige links.md` → `Topics/x-open-loops/Nuttige links.md`
- `_INBOX/Ook weer links.md` → `Topics/x-open-loops/Ook weer links.md`
- `_INBOX/Superbelangrijk!.md` → `Topics/x-open-loops/Superbelangrijk!.md`
- `_INBOX/Untitled (31).md` → `Topics/x-open-loops/Untitled (31).md`
- `_INBOX/Untitled note (12).md` → `Topics/x-open-loops/Untitled note (12).md`
- `_INBOX/Untitled note (13).md` → `Topics/x-open-loops/Untitled note (13).md`
- `_INBOX/Untitled note (22).md` → `Topics/x-open-loops/Untitled note (22).md`
- `_INBOX/Untitled note (27).md` → `Topics/x-open-loops/Untitled note (27).md`
- `_INBOX/Untitled note (29).md` → `Topics/x-open-loops/Untitled note (29).md`
- `_INBOX/Untitled note (30).md` → `Topics/x-open-loops/Untitled note (30).md`
- `_INBOX/Vrijdag doen.md` → `Topics/x-open-loops/Vrijdag doen.md`

### `ai-grok` — 8 moved

- `_INBOX/AI 2027.md` → `Topics/ai-grok/AI 2027.md`
- `_INBOX/Ai sites proberen.md` → `Topics/ai-grok/Ai sites proberen.md`
- `_INBOX/AI training HRacademy.md` → `Topics/ai-grok/AI training HRacademy.md`
- `_INBOX/AI training in HR.md` → `Topics/ai-grok/AI training in HR.md`
- `_INBOX/AI training voor niet techneuten.md` → `Topics/ai-grok/AI training voor niet techneuten.md`
- `_INBOX/Grok prompts.md` → `Topics/ai-grok/Grok prompts.md`
- `_INBOX/Jobhinting prompts.md` → `Topics/ai-grok/Jobhinting prompts.md`
- `_INBOX/Marlon- sterke fit met beknoptheidsrisico - Grok.md` → `Topics/ai-grok/Marlon- sterke fit met beknoptheidsrisico - Grok.md`

### `cash-bd-career` — 26 moved

- `_INBOX/(34) Stafmanager Informatiemanagement & IT Rijn IJssel LinkedIn.md` → `Topics/cash-bd-career/(34) Stafmanager Informatiemanagement & IT Rijn IJssel LinkedIn.md`
- `_INBOX/2e kamer soll.md` → `Topics/cash-bd-career/2e kamer soll.md`
- `_INBOX/Boardio.md` → `Topics/cash-bd-career/Boardio.md`
- `_INBOX/Careerhandling 230629.md` → `Topics/cash-bd-career/Careerhandling 230629.md`
- `_INBOX/Careerhandling.md` → `Topics/cash-bd-career/Careerhandling.md`
- `_INBOX/Directeur bedrijfsvoering.md` → `Topics/cash-bd-career/Directeur bedrijfsvoering.md`
- `_INBOX/HR rotterdam - 240404.md` → `Topics/cash-bd-career/HR rotterdam - 240404.md`
- `_INBOX/ITer gezocht.md` → `Topics/cash-bd-career/ITer gezocht.md`
- `_INBOX/Jobs.md` → `Topics/cash-bd-career/Jobs.md`
- `_INBOX/LinkedIN S Slooten.md` → `Topics/cash-bd-career/LinkedIN S Slooten.md`
- `_INBOX/LOS Case.md` → `Topics/cash-bd-career/LOS Case.md`
- `_INBOX/Motivaties div.md` → `Topics/cash-bd-career/Motivaties div.md`
- `_INBOX/Omschrijving LinkedIn ().md` → `Topics/cash-bd-career/Omschrijving LinkedIn ().md`
- `_INBOX/Omschrijving SSL.md` → `Topics/cash-bd-career/Omschrijving SSL.md`
- `_INBOX/Payment Structure.md` → `Topics/cash-bd-career/Payment Structure.md`
- `_INBOX/Payment Updates - REGELEN!.md` → `Topics/cash-bd-career/Payment Updates - REGELEN!.md`
- `_INBOX/Prive - vacatures.md` → `Topics/cash-bd-career/Prive - vacatures.md`
- `_INBOX/sollicitatie HB.md` → `Topics/cash-bd-career/sollicitatie HB.md`
- `_INBOX/Speaking.md` → `Topics/cash-bd-career/Speaking.md`
- `_INBOX/SSL - algemene introductie.md` → `Topics/cash-bd-career/SSL - algemene introductie.md`
- `_INBOX/SSL - Ideeen voor tekst.md` → `Topics/cash-bd-career/SSL - Ideeen voor tekst.md`
- `_INBOX/SSL Motivatie.md` → `Topics/cash-bd-career/SSL Motivatie.md`
- `_INBOX/Vacatures.md` → `Topics/cash-bd-career/Vacatures.md`
- `_INBOX/van Houdt en partners.md` → `Topics/cash-bd-career/van Houdt en partners.md`
- `_INBOX/Welcome mail march 2016.md` → `Topics/cash-bd-career/Welcome mail march 2016.md`
- `_INBOX/werk zoeken.md` → `Topics/cash-bd-career/werk zoeken.md`

### `ja21` — 50 moved

- `_INBOX/Diederik Boomsma vertrekt naar JA21- ’Wil rechtsere koers op migratie’ De Teleg… (2).md` → `Topics/ja21/Diederik Boomsma vertrekt naar JA21- ’Wil rechtsere koers op migratie’ De Teleg… (2).md`
- `_INBOX/Diederik Boomsma vertrekt naar JA21- ’Wil rechtsere koers op migratie’ De Teleg….md` → `Topics/ja21/Diederik Boomsma vertrekt naar JA21- ’Wil rechtsere koers op migratie’ De Teleg….md`
- `_INBOX/JA21 - ALV 2022.md` → `Topics/ja21/JA21 - ALV 2022.md`
- `_INBOX/JA21 - ALV 22.1.md` → `Topics/ja21/JA21 - ALV 22.1.md`
- `_INBOX/JA21 - ALV amendementen-moties.md` → `Topics/ja21/JA21 - ALV amendementen-moties.md`
- `_INBOX/JA21 - Amsterdam.md` → `Topics/ja21/JA21 - Amsterdam.md`
- `_INBOX/JA21 - Apparatuur partijkantoor.md` → `Topics/ja21/JA21 - Apparatuur partijkantoor.md`
- `_INBOX/JA21 - BambooHR.md` → `Topics/ja21/JA21 - BambooHR.md`
- `_INBOX/JA21 - Bestuur.md` → `Topics/ja21/JA21 - Bestuur.md`
- `_INBOX/JA21 - Bestuursvergadering items.md` → `Topics/ja21/JA21 - Bestuursvergadering items.md`
- `_INBOX/JA21 - disclaimer.md` → `Topics/ja21/JA21 - disclaimer.md`
- `_INBOX/JA21 - Google settings.md` → `Topics/ja21/JA21 - Google settings.md`
- `_INBOX/JA21 - H de Jonge.md` → `Topics/ja21/JA21 - H de Jonge.md`
- `_INBOX/JA21 - Heidag bestuur 221119.md` → `Topics/ja21/JA21 - Heidag bestuur 221119.md`
- `_INBOX/JA21 - Input Ted Dinklo.md` → `Topics/ja21/JA21 - Input Ted Dinklo.md`
- `_INBOX/JA21 - Interne nieuwsbrief bestuur.md` → `Topics/ja21/JA21 - Interne nieuwsbrief bestuur.md`
- `_INBOX/JA21 - IT en applicatie instellingen.md` → `Topics/ja21/JA21 - IT en applicatie instellingen.md`
- `_INBOX/JA21 - Kerstgroet '22.md` → `Topics/ja21/JA21 - Kerstgroet '22.md`
- `_INBOX/JA21 - Kwitantie maken als particulier.md` → `Topics/ja21/JA21 - Kwitantie maken als particulier.md`
- `_INBOX/JA21 - Ledenadministratie.md` → `Topics/ja21/JA21 - Ledenadministratie.md`
- `_INBOX/JA21 - lijst.md` → `Topics/ja21/JA21 - lijst.md`
- `_INBOX/JA21 - Longlist Eerste Kamer '23.md` → `Topics/ja21/JA21 - Longlist Eerste Kamer '23.md`
- `_INBOX/JA21 - Mensen gesproken in '22.md` → `Topics/ja21/JA21 - Mensen gesproken in '22.md`
- `_INBOX/JA21 - muziek background.md` → `Topics/ja21/JA21 - muziek background.md`
- `_INBOX/JA21 - Nifty handige links.md` → `Topics/ja21/JA21 - Nifty handige links.md`
- `_INBOX/JA21 - Oude privacy & voorwaarden tekst.md` → `Topics/ja21/JA21 - Oude privacy & voorwaarden tekst.md`
- `_INBOX/JA21 - Politiek Overleg.md` → `Topics/ja21/JA21 - Politiek Overleg.md`
- `_INBOX/JA21 - Potentiele commissieleden.md` → `Topics/ja21/JA21 - Potentiele commissieleden.md`
- `_INBOX/JA21 - PS23 - peilingen.md` → `Topics/ja21/JA21 - PS23 - peilingen.md`
- `_INBOX/JA21 - PS23-NH lijst DEF.md` → `Topics/ja21/JA21 - PS23-NH lijst DEF.md`
- `_INBOX/JA21 - Standpunten.md` → `Topics/ja21/JA21 - Standpunten.md`
- `_INBOX/JA21 - Things Done.md` → `Topics/ja21/JA21 - Things Done.md`
- `_INBOX/JA21 - Tools en systemen.md` → `Topics/ja21/JA21 - Tools en systemen.md`
- `_INBOX/JA21 - Verkiezingsavond.md` → `Topics/ja21/JA21 - Verkiezingsavond.md`
- `_INBOX/JA21 - Voorstel voorbereiding TK23 & EP24.md` → `Topics/ja21/JA21 - Voorstel voorbereiding TK23 & EP24.md`
- `_INBOX/JA21 - vragen kandidaten.md` → `Topics/ja21/JA21 - vragen kandidaten.md`
- `_INBOX/JA21 - Waarom politiek overleg.md` → `Topics/ja21/JA21 - Waarom politiek overleg.md`
- `_INBOX/JA21 - WS23 - golfsport.md` → `Topics/ja21/JA21 - WS23 - golfsport.md`
- `_INBOX/JA21 bestuur - 240909.md` → `Topics/ja21/JA21 bestuur - 240909.md`
- `_INBOX/JA21 Heidag '22 (2).md` → `Topics/ja21/JA21 Heidag '22 (2).md`
- `_INBOX/JA21 Heidag '22.md` → `Topics/ja21/JA21 Heidag '22.md`
- `_INBOX/JA21 Helpdesk IT.md` → `Topics/ja21/JA21 Helpdesk IT.md`
- `_INBOX/JA21 meeting Baker-Tilly.md` → `Topics/ja21/JA21 meeting Baker-Tilly.md`
- `_INBOX/JONG21 reglement.md` → `Topics/ja21/JONG21 reglement.md`
- `_INBOX/Kansen voor JA21 als ze het slim spelen Columns Telegraaf.nl.md` → `Topics/ja21/Kansen voor JA21 als ze het slim spelen Columns Telegraaf.nl.md`
- `_INBOX/Leden JA21 2022.md` → `Topics/ja21/Leden JA21 2022.md`
- `_INBOX/Michiel Hoogeveen (JA21)- ‘Rücksichtslos uit de EU stappen is bijzonder onverst….md` → `Topics/ja21/Michiel Hoogeveen (JA21)- ‘Rücksichtslos uit de EU stappen is bijzonder onverst….md`
- `_INBOX/Privacy statement JA 21.md` → `Topics/ja21/Privacy statement JA 21.md`
- `_INBOX/Ruzie binnen JA21- ‘De partij is een baantjesmachine voor Joost en Annabel’ - N….md` → `Topics/ja21/Ruzie binnen JA21- ‘De partij is een baantjesmachine voor Joost en Annabel’ - N….md`
- `_INBOX/Waarom JA21 de VVD in de komende vijf jaar moeiteloos leegeet en de dominante p….md` → `Topics/ja21/Waarom JA21 de VVD in de komende vijf jaar moeiteloos leegeet en de dominante p….md`

### `geopolitics-curiosity` — 18 moved

- `_INBOX/Alarm om dalend aantal mbo’ers- volop banen en hoog salaris, ’maar scholen zien….md` → `Topics/geopolitics-curiosity/Alarm om dalend aantal mbo’ers- volop banen en hoog salaris, ’maar scholen zien….md`
- `_INBOX/Ambtenaar onder extreemrechts kabinet.md` → `Topics/geopolitics-curiosity/Ambtenaar onder extreemrechts kabinet.md`
- `_INBOX/Annabel Nanninga over ’linkse wolk’ Rutte- ’Nu gaan bij mensen schellen van de….md` → `Topics/geopolitics-curiosity/Annabel Nanninga over ’linkse wolk’ Rutte- ’Nu gaan bij mensen schellen van de….md`
- `_INBOX/Annabel Nanninga- ‘Ik ben opgevoed met harde humor’.md` → `Topics/geopolitics-curiosity/Annabel Nanninga- ‘Ik ben opgevoed met harde humor’.md`
- `_INBOX/De naderende implosie van ons politieke systeem - Maurice de Hond.md` → `Topics/geopolitics-curiosity/De naderende implosie van ons politieke systeem - Maurice de Hond.md`
- `_INBOX/De tiende man - tenth man principle.md` → `Topics/geopolitics-curiosity/De tiende man - tenth man principle.md`
- `_INBOX/Deel jeugd Oostvoorne ontspoort- ’Kinderen met messen, jongens die meisjes aanr….md` → `Topics/geopolitics-curiosity/Deel jeugd Oostvoorne ontspoort- ’Kinderen met messen, jongens die meisjes aanr….md`
- `_INBOX/Geheime afspraak coalitie- mond dicht over migratie deze campagne Onder Politic….md` → `Topics/geopolitics-curiosity/Geheime afspraak coalitie- mond dicht over migratie deze campagne Onder Politic….md`
- `_INBOX/Griekse Oudheid.md` → `Topics/geopolitics-curiosity/Griekse Oudheid.md`
- `_INBOX/Grote zorgen om jongeren die cobra’s bewaren onder hun bed- ’Mensen denken dat….md` → `Topics/geopolitics-curiosity/Grote zorgen om jongeren die cobra’s bewaren onder hun bed- ’Mensen denken dat….md`
- `_INBOX/Hoe deze asielmotie laat zien dat mild-rechts een Kamermeerderheid heeft - Wyni….md` → `Topics/geopolitics-curiosity/Hoe deze asielmotie laat zien dat mild-rechts een Kamermeerderheid heeft - Wyni….md`
- `_INBOX/Huishoudboekje van scholen rammelt- ’Geld verdwijnt naar bullshitbanen’ Binnenl….md` → `Topics/geopolitics-curiosity/Huishoudboekje van scholen rammelt- ’Geld verdwijnt naar bullshitbanen’ Binnenl….md`
- `_INBOX/KLM-crew terug na dagen vast in Midden-Oosten door oorlog De Telegraaf.md` → `Topics/geopolitics-curiosity/KLM-crew terug na dagen vast in Midden-Oosten door oorlog De Telegraaf.md`
- `_INBOX/Sigrid Kaag over migratie- ‘Hekken horen niet bij een beschaafd land’ Politiek….md` → `Topics/geopolitics-curiosity/Sigrid Kaag over migratie- ‘Hekken horen niet bij een beschaafd land’ Politiek….md`
- `_INBOX/Verontwaardiging in China door moeder van acht kinderen die buiten vastgeketend….md` → `Topics/geopolitics-curiosity/Verontwaardiging in China door moeder van acht kinderen die buiten vastgeketend….md`
- `_INBOX/Wat vertellen de provinciehuizen over de provincies - NRC.md` → `Topics/geopolitics-curiosity/Wat vertellen de provinciehuizen over de provincies - NRC.md`
- `_INBOX/What really went on inside the Wuhan lab weeks before Covid erupted.md` → `Topics/geopolitics-curiosity/What really went on inside the Wuhan lab weeks before Covid erupted.md`
- `_INBOX/’Conservatieve partij die rechts is maar wel met iedereen praat’ Binnenland Tel….md` → `Topics/geopolitics-curiosity/’Conservatieve partij die rechts is maar wel met iedereen praat’ Binnenland Tel….md`

### `guitars-gear` — 25 moved

- `_INBOX/Allen & Heath.md` → `Topics/guitars-gear/Allen & Heath.md`
- `_INBOX/D'Angelico Excel EXS-1DH.md` → `Topics/guitars-gear/D'Angelico Excel EXS-1DH.md`
- `_INBOX/Fender Stratocaster Candy Apple Red.md` → `Topics/guitars-gear/Fender Stratocaster Candy Apple Red.md`
- `_INBOX/Fender Stratocaster deluxe hss 60th Anniversary.md` → `Topics/guitars-gear/Fender Stratocaster deluxe hss 60th Anniversary.md`
- `_INBOX/Fender Stratocaster Mark Knopfler.md` → `Topics/guitars-gear/Fender Stratocaster Mark Knopfler.md`
- `_INBOX/Gibson Les Paul Custom.md` → `Topics/guitars-gear/Gibson Les Paul Custom.md`
- `_INBOX/Ibanez ST50 serial number.md` → `Topics/guitars-gear/Ibanez ST50 serial number.md`
- `_INBOX/Music background tracks.md` → `Topics/guitars-gear/Music background tracks.md`
- `_INBOX/Music.md` → `Topics/guitars-gear/Music.md`
- `_INBOX/Pensa MK-90.md` → `Topics/guitars-gear/Pensa MK-90.md`
- `_INBOX/Pensa MK90 Blue Ice Metallic Mark Knopfler Signature P90 Ex Collector.md` → `Topics/guitars-gear/Pensa MK90 Blue Ice Metallic Mark Knopfler Signature P90 Ex Collector.md`
- `_INBOX/PRS West Street Limited - US$ 2980 (nov '18).md` → `Topics/guitars-gear/PRS West Street Limited - US$ 2980 (nov '18).md`
- `_INBOX/Schecter Stratocaster.md` → `Topics/guitars-gear/Schecter Stratocaster.md`
- `_INBOX/SG - Pensa-Suhr.md` → `Topics/guitars-gear/SG - Pensa-Suhr.md`
- `_INBOX/SG - Suhr Standard Custom.md` → `Topics/guitars-gear/SG - Suhr Standard Custom.md`
- `_INBOX/Special Guitars - Gibson Chet Atkins CE.md` → `Topics/guitars-gear/Special Guitars - Gibson Chet Atkins CE.md`
- `_INBOX/Special Guitars - Policies.md` → `Topics/guitars-gear/Special Guitars - Policies.md`
- `_INBOX/Special Guitars - Suhr Pro Series S3.md` → `Topics/guitars-gear/Special Guitars - Suhr Pro Series S3.md`
- `_INBOX/Special Guitars standard text.md` → `Topics/guitars-gear/Special Guitars standard text.md`
- `_INBOX/Special Guitars- Bezorgen Koerier.md` → `Topics/guitars-gear/Special Guitars- Bezorgen Koerier.md`
- `_INBOX/Synth repair offer.md` → `Topics/guitars-gear/Synth repair offer.md`
- `_INBOX/Tom Anderson Drop Top.md` → `Topics/guitars-gear/Tom Anderson Drop Top.md`
- `_INBOX/Verkoop CE.md` → `Topics/guitars-gear/Verkoop CE.md`
- `_INBOX/Verkoop Synthesizers.md` → `Topics/guitars-gear/Verkoop Synthesizers.md`
- `_INBOX/≥ E-MU Orbit 9090 - The Dance Planet V2 - Marktplaats.md` → `Topics/guitars-gear/≥ E-MU Orbit 9090 - The Dance Planet V2 - Marktplaats.md`

### `home-life` — 16 moved

- `_INBOX/Bermweg 213 - 230504.md` → `Topics/home-life/Bermweg 213 - 230504.md`
- `_INBOX/Bermweg 213 verf kleuren & leveranciers.md` → `Topics/home-life/Bermweg 213 verf kleuren & leveranciers.md`
- `_INBOX/Binnenverlichting.md` → `Topics/home-life/Binnenverlichting.md`
- `_INBOX/BMW definitive.md` → `Topics/home-life/BMW definitive.md`
- `_INBOX/BoxBrownie.com – TAKING THE BEST PHOTOS WITH A NIKON D7100-D7200 CAMERA.md` → `Topics/home-life/BoxBrownie.com – TAKING THE BEST PHOTOS WITH A NIKON D7100-D7200 CAMERA.md`
- `_INBOX/Computers.md` → `Topics/home-life/Computers.md`
- `_INBOX/Curacao Huis.md` → `Topics/home-life/Curacao Huis.md`
- `_INBOX/Dekbed.md` → `Topics/home-life/Dekbed.md`
- `_INBOX/Domotica IJsselstijn.md` → `Topics/home-life/Domotica IJsselstijn.md`
- `_INBOX/Fotospullen Brante.md` → `Topics/home-life/Fotospullen Brante.md`
- `_INBOX/iPhone hoesjes.md` → `Topics/home-life/iPhone hoesjes.md`
- `_INBOX/Overzetten Mac.md` → `Topics/home-life/Overzetten Mac.md`
- `_INBOX/Recommended Nikon D7100 Settings.md` → `Topics/home-life/Recommended Nikon D7100 Settings.md`
- `_INBOX/Spullen Bermweg.md` → `Topics/home-life/Spullen Bermweg.md`
- `_INBOX/Vakantiebestemmingen.md` → `Topics/home-life/Vakantiebestemmingen.md`
- `_INBOX/VD Ham toilet drukplaat.md` → `Topics/home-life/VD Ham toilet drukplaat.md`

### `kids-school` — 9 moved

- `_INBOX/Bed Siem en Puk.md` → `Topics/kids-school/Bed Siem en Puk.md`
- `_INBOX/Emmaus - Vragen na 22S1.md` → `Topics/kids-school/Emmaus - Vragen na 22S1.md`
- `_INBOX/Kids safe DNS settings.md` → `Topics/kids-school/Kids safe DNS settings.md`
- `_INBOX/Kim Zwangerschapsverlof.md` → `Topics/kids-school/Kim Zwangerschapsverlof.md`
- `_INBOX/Klacht Emmaus.md` → `Topics/kids-school/Klacht Emmaus.md`
- `_INBOX/Siem Schoolkeuze.md` → `Topics/kids-school/Siem Schoolkeuze.md`
- `_INBOX/Siem.md` → `Topics/kids-school/Siem.md`
- `_INBOX/Step Siem bol.com.md` → `Topics/kids-school/Step Siem bol.com.md`
- `_INBOX/Verjaardag Siem.md` → `Topics/kids-school/Verjaardag Siem.md`

### `gifts-kadoos` — 6 moved

- `_INBOX/Bestellen.md` → `Topics/gifts-kadoos/Bestellen.md`
- `_INBOX/Bestellingen.md` → `Topics/gifts-kadoos/Bestellingen.md`
- `_INBOX/Cadeau ideeen.md` → `Topics/gifts-kadoos/Cadeau ideeen.md`
- `_INBOX/Cadeaus.md` → `Topics/gifts-kadoos/Cadeaus.md`
- `_INBOX/Kerstcadeaus.md` → `Topics/gifts-kadoos/Kerstcadeaus.md`
- `_INBOX/Sinterklaas gedichten.md` → `Topics/gifts-kadoos/Sinterklaas gedichten.md`

### `health` — 3 moved

- `_INBOX/CORONA.md` → `Topics/health/CORONA.md`
- `_INBOX/Gezondheid.md` → `Topics/health/Gezondheid.md`
- `_INBOX/How Ozempic Is Transforming a Small Danish Town - The New York Times.md` → `Topics/health/How Ozempic Is Transforming a Small Danish Town - The New York Times.md`

## Post-move status
- Moved this pass: **185**
- Remaining in `_INBOX`: **251**
- Errors/skips: 0

## Remaining `_INBOX` — needs Simon decision / later pass
- Large **Untitled / Untitled note / Untitled Note** pile (~120+) — mostly ambiguous stubs; only X-link untitled were moved.
- **FVD-*** party-ops notes (~12) — related to politics history but not clearly JA21; left conservative.
- Campaign / politics ops without JA21 in title (PS23, TK21, Billboards, Coordinatoren, flyers, etc.).
- Private / legal / CSV / IKE correspondence — leave for Simon.
- Prisma / Railo / NS / HVC / career-meeting crumbs mixed with personal — ambiguous.
- Tiny stubs (`body_source: dat`, deleted, empty).
- `_index.md` inventory helper left in place.

## Ambiguous pile (examples left in `_INBOX`)
- `15 maart.md` (ambiguous)
- `2013-10-29.md` (ambiguous)
- `2013-12-11.md` (ambiguous)
- `2025-05-25 12.pdf (2).md` (ambiguous)
- `2025-05-25 12.pdf.md` (ambiguous)
- `6FUSH.md` (ambiguous)
- `A. bespreken.md` (ambiguous)
- `Aanmelden vrijwilliger verkiezingen.md` (ambiguous)
- `Accounts Social Media Provincies.md` (ambiguous)
- `Afscheid Michael Ruperti.md` (ambiguous)
- `Agenda 20211004.md` (ambiguous)
- `Algemeen kladblok.md` (ambiguous)
- `All I ever need to know.md` (ambiguous)
- `Baas & Baas 221006.md` (ambiguous)
- `Bank.md` (ambiguous)
- `Belasting 2020.md` (ambiguous)
- `Bericht Lijsttrekkers.md` (ambiguous)
- `Beschrijving.md` (ambiguous)
- `Bespreken met Jory.md` (ambiguous)
- `Bestuursvergadering 240826.md` (ambiguous)
- `Billboards.md` (ambiguous)
- `boardable.md` (ambiguous)
- `Brief IKE 210916.md` (ambiguous)
- `Briefje Ted Dinklo.md` (ambiguous)
- `Briefje van Jan - aan Joost Eerdmans - Buttkicken.nl.md` (ambiguous)
- `Campagne dirt.md` (ambiguous)
- `CH nooda.md` (ambiguous)
- `Change Education - Onderwijs.md` (ambiguous)
- `Coordinatoren per kieskring.md` (ambiguous)
- `CSV 2e brief.md` (ambiguous)
- `CSV brief.md` (ambiguous)
- `CSV problematiek.md` (ambiguous)
- `Damecon.md` (ambiguous)
- `Directeuren overleg politieke partijen.md` (ambiguous)
- `Evaluatie PS23.md` (ambiguous)
- `event.md` (ambiguous)
- `Ferenc János Toth.md` (ambiguous)
- `Flyers per KiesKring TK21.md` (ambiguous)
- `Frank v dalen.md` (ambiguous)
- `Funeral poem.md` (ambiguous)
- `Fvd (2).md` (ambiguous)
- `FvD (3).md` (ambiguous)
- `FVD - teamcaptain update.md` (ambiguous)
- `FVD aanmwelding.md` (ambiguous)
- `FVD afdeling meeting 2-9-20.md` (ambiguous)
- `FVD afdelingsvergadering 20200907 (2).md` (ambiguous)
- `FVD afdelingsvergadering 20200907.md` (ambiguous)
- `FVD begroting 2022.md` (ambiguous)
- `FVD gesprek 26-11.md` (ambiguous)
- `FVD mail naar belteam.md` (ambiguous)
- `FVD online team meetings.md` (ambiguous)
- `FVD.md` (ambiguous)
- `Ge.md` (ambiguous)
- `Gesprek Adrien.md` (ambiguous)
- `Gesprek Ronald & teksten.md` (ambiguous)
- `Google Ads Politieke partijen.md` (ambiguous)
- `Google check.md` (ambiguous)
- `Gunshop.md` (ambiguous)
- `Hicolas - 8-8-2024.md` (ambiguous)
- `HVC - Vincent - 20230904.md` (ambiguous)
- … plus more untitled/stubs; total left 251

---

# Pass 2 — 2026-09-30 (~10:25 Europe/Amsterdam)

Owner: Archivaris. Green light via CoS: FVD → `politics-nl-fvd`, Untitled → `_stubs`, then Default Notebook high-confidence refile.

## New folders created
| Folder | Intent |
|---|---|
| `Topics/politics-nl-fvd/` | FVD party-ops + TK21-era campaign without JA21 in title/body |
| `Topics/_stubs/` | Clear Untitled / Untitled note / Untitled Note stubs parked from `_INBOX` and Default Notebook |

## A. From `_INBOX`

### `politics-nl-fvd` — 17 moved
- FVD\* (12): `FVD.md`, `Fvd (2).md`, `FvD (3).md`, `FVD - teamcaptain update.md`, `FVD aanmwelding.md`, `FVD afdeling meeting 2-9-20.md`, `FVD afdelingsvergadering 20200907.md`, `FVD afdelingsvergadering 20200907 (2).md`, `FVD begroting 2022.md`, `FVD gesprek 26-11.md`, `FVD mail naar belteam.md`, `FVD online team meetings.md`
- Forum: `Standpunten - Forum voor Democratie.md`
- TK21-era campaign (no JA21): `TK21 campagne.md`, `Flyers per KiesKring TK21.md`, `Billboards.md`, `Coordinatoren per kieskring.md`

### `ja21` — 4 moved (clearly JA21 despite no JA21 in title)
- `PS23 - Opbouw teams.md` (ja21.nl emails)
- `Evaluatie PS23.md` (JA21 PS23 list / Nanninga)
- `Bericht Lijsttrekkers.md` (explicit JA21)
- `Directeuren overleg politieke partijen.md` (JA21 director notes)

### `_stubs` — 123 moved from `_INBOX`
- All filenames starting with `Untitled` / `Untitled note` / `Untitled Note` remaining in `_INBOX` after pass 1.

### `_INBOX` remaining after 2A
- **107** (was 251; −17 FVD −4 ja21 −123 stubs)

## B. Default Notebook (~93 → 50 remaining)

### Inventory themes (pre-move)
- Heavy: Job Description\* hiring pack; Untitled stubs; 4F/Prisma/Railo/vTiger/NS historical work crumbs; meeting notes (Aurelien, Vincent, Eric); device/home how-tos (Alexa/Hue, Android→iCloud photos); management articles; invoices; `Kadoos.md`.

### Moves (high-confidence only) — 43 total
| Destination | Count | Notes |
|---|---:|---|
| `Topics/_stubs/` | 19 | Untitled\* from Default Notebook; stored as `dn-Untitled*.md` after collision fix |
| `Topics/cash-bd-career/` | 18 | Job Description\* (15), Hiring Senior Web Analyst, Job Opportunity Systeembeheerder, Sales Executive, Technical Web Analytics Consultant |
| `Topics/home-life/` | 5 | Amazon Alexa Commands, Amazon Echo Alexa - Hue, Sync photos\* (3) |
| `Topics/gifts-kadoos/` | 1 | `Kadoos.md` |

### Default Notebook remaining — **50**
Left conservative: 4F/Prisma/NS/Railo/vTiger project crumbs, dated meeting notes, invoices, management articles, ambiguous personal (`silvella`, `mooie dingen`, `Praten met`, `Agenda`, `test`, `_index.md`, etc.). No new Topics slug created beyond the 2 green-lit this pass.

## Collision incident + recovery (Untitled filename clash)
When Default Notebook Untitled\* were moved into `_stubs/`, **19** filenames collided with already-parked `_INBOX` stubs and overwrote them (`mv` replace). Mitigations applied same pass:
1. Renamed Default stubs to `dn-<original>` (19 files).
2. Restored missing `_INBOX` Untitled notes from local Evernote RemoteGraph + `.dat` / snippet (**24** files rewritten into `_stubs/`, including 5 that existed in Evernote `_INBOX` but were absent from the live markdown dump). Restored notes carry frontmatter `restored: pass2-collision-recovery-2026-09-30`.

### `_stubs` final composition
- Surviving original `_INBOX` stubs: 104
- Default Notebook stubs (`dn-*`): 19
- Restored `_INBOX` stubs: 24
- **Total `_stubs/`: 147**

## Pass 2 counts summary
| Metric | Count |
|---|---:|
| Moved → politics-nl-fvd | 17 |
| Moved → ja21 (extra clear) | 4 |
| Moved → _stubs from `_INBOX` | 123 |
| Moved from Default Notebook | 43 |
| `_INBOX` remaining | **107** |
| Default Notebook remaining | **50** |
| New Topics folders | 2 (`politics-nl-fvd`, `_stubs`) |

## Ambiguous pile still needing Simon (short)
**Still in `_INBOX` (~107):** private/legal (CSV\*, Brief IKE, Briefje\*), `Campagne dirt.md`, `Aanmelden vrijwilliger verkiezingen.md` (stembureau, not party), `Google Ads Politieke partijen.md`, `Accounts Social Media Provincies.md` (creds — handle carefully), Bestuursvergadering / Baas / HVC crumbs, dated ambiguous (`15 maart`, `2013-*`), funeral poem, Gunshop, Change Education, etc.

**Still in Default Notebook (~50):** 4F\* / Prisma / NS / Railo / vTiger / Bynder historical company notes; person meeting notes (Vincent/Eric/Aurelien/Jorrit); management articles (Merit Matrix, Leadership, Partner Program, McKinsey); invoices; thin personal (`silvella`, `mooie dingen`, `Praten met`, `Uitzoeken`, `Agenda`, `test`).

Left conservative — do not auto-merge into Topics without Simon call.

---
*End of Archivaris refile pass 2 — 2026-09-30.*

---

# Pass 3 — private park — 2026-09-30

Conservative private/legal and invoice park from the remaining `_INBOX` and `Default Notebook` only. Ambiguous political, person, Prisma/NS, and company/legal-history notes were left in place.

## Moved from `_INBOX` — 8

- `_INBOX/Brief IKE 210916.md` → `Topics/_private/Brief IKE 210916.md`
- `_INBOX/CSV 2e brief.md` → `Topics/_private/CSV 2e brief.md`
- `_INBOX/CSV brief.md` → `Topics/_private/CSV brief.md`
- `_INBOX/CSV problematiek.md` → `Topics/_private/CSV problematiek.md`
- `_INBOX/IDA.md` → `Topics/_private/IDA.md`
- `_INBOX/Verrekenen met Ida.md` → `Topics/_private/Verrekenen met Ida.md`
- `_INBOX/Nieuwe gezeik.md` → `Topics/_private/Nieuwe gezeik.md`
- `_INBOX/Kopie rijbewijs 20 M.jpg.md` → `Topics/_private/Kopie rijbewijs 20 M.jpg.md`

## Moved from `Default Notebook` — 2

- `Default Notebook/FW- Invoice - FV 2-2013 - Prisma IT France.md` → `Topics/_private/FW- Invoice - FV 2-2013 - Prisma IT France.md`
- `Default Notebook/TRC invoice.md` → `Topics/_private/TRC invoice.md`

## Post-move status

- `Topics/_private/`: **10** notes added
- Remaining `_INBOX`: **99** markdown notes (including `_index.md`)
- Remaining `Default Notebook`: **48** markdown notes (including `_index.md`)
- Errors/skips: 0
