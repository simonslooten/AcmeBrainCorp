# Review — JA21 Beleidsdashboard (abacusai.app)
Datum: 2026-09-16  
URL: https://ja21dashboards.abacusai.app  
Status: DRAFT voor Simon (landelijk bestuur) — Bonica CLEAR nog niet

## Kort oordeel
Sterk als **publiek/briefing-dashboard** (14 thema’s, JA21-branding, geen login). Bruikbaar voor agenda-setting en fractiecommunicatie. **Niet** decision-grade zonder bronvalidatie: methodologie ontbreekt globaal, jaren/denominators mixen, toon is deels advocacy (“Code Rood”, “Explosieve groei”) naast cijfers.

## Wat het is
“Beleidsdashboard Nederland — een initiatief van JA21” (ook WI JA21 genoemd). Host: `*.abacusai.app` (Abacus AI-infra), geen zichtbare Abacus-branding in UI.

Thema’s o.a.: Asiel & Migratie, Zorg, EU, Defensie, Luchtvaart, Digitaal, Onderwijs, Economie, Veiligheid, Energie, Wonen, Buitenland, Overheidsfinanciën (incl. begroting 2027), MKB.

## Inhoud (steekproef)
- **Overheidsfinanciën:** editie sept 2026; KPIs 2027 o.a. groei 1,2%, inflatie 2,8%, mediane koopkracht −0,3%, EMU −2,1%, schuld 48% BBP; defensie-intensivering genoemd. Bronnen: CPB/CBS/Rijksfinanciën/DNB (+ soms media/consultancy).
- **Asiel:** 33.500 aanvragen (2024), inwilligings% 48,3%, COA bezetting, EU-rang; bronnen IND/COA.
- **Defensie:** budget €34,9 mrd (2026), NAVO-aandeel ~2,02%.
- **Energie / Wonen / Onderwijs:** kern-KPI’s + charts; onderwijs deels “indicatief”.

## Sterktes
- Brede dekking thema’s die in het JA21-programma zitten.
- Sectie-bronnenpagina’s bestaan.
- Geen login; snel te delen.

## Zwaktes / risico’s (bestuur)
1. Prognoses/2027-cijfers kunnen als harde feiten herhaald worden.
2. JA21-duiding naast stats → risico “neutrale data” terwijl het gekleurd is.
3. Geen globale methodologie / data dictionary / export / versiegeschiedenis.
4. Gemengde peiljaren en denominators (asiel vs chartperiode; energie totaal vs elektriciteit).
5. `/about`, `/bronnen`, `/methodologie` → 404; alleen sectie-bronnen werken.
6. UX: smalle content naast vaste sidebar; labels knippen.

## Aanbevelingen (top 5)
1. Globale methodologie + update-log + definities.
2. Op elke KPI: bron, peildatum, status (definitief/raming), denominator.
3. Harde scheiding: officiële data | schatting | media | JA21-interpretatie.
4. Export CSV/PNG/PDF met timestamps.
5. Contact/privacy/toegankelijkheid + mobiel layout.

## Tape
- **Sources:** live browse https://ja21dashboards.abacusai.app (2026-09-16); WebFetch homepage; secties Overheidsfinanciën, Asiel, Defensie, Energie, Wonen, Onderwijs.
- **Guesses:** of dit officieel WI-JA21 product is vs campagnestuk — hostname Abacus, attribution JA21/WI, geen formeel about-document gevonden.
- **Skipped:** niet alle 14 thema’s end-to-end; geen mobiele viewport-test; geen cijfer-voor-cijfer audit vs CBS/CPB/MN2027.
- **Evidence:** screenshots in Work/vault map `JA21/dashboard-review-2026-09-16/`.
