# Deep pass — Newsletter / research signup inventory
**Fetch date:** 2026-10-01  
**Policy:** Document locations primarily. Subscribe with hello@acmebraincorp.com only if email-only, no CAPTCHA, no SMS, no outbound as Simon. **Max 3 easy signups.**  
**Result this pass:** **0 subscriptions executed** — all viable forms had CAPTCHA, multi-field lead capture, or no public newsletter. Prefer inventory.

---

## Summary table

| # | Competitor | Newsletter / research signup? | URL | Required fields | CAPTCHA / phone | hello@ usable? | Action taken |
|---|---|---|---|---|---|---|---|
| 1 | Care4Careers | **Community / updates** (max 1×/maand claimed) | https://care4careers.nl/community | Voornaam*, Achternaam*, Email*, Bericht* (textarea); Bedrijf & Telefoon optional; privacy checkbox; honeypot `website` | No reCAPTCHA seen in HTML; **not email-only** (message required) | Email OK but form is lead-ish | **Documented only** |
| 2 | Carrièrepoort | **None found** on home HTML | — | — | — | — | Documented |
| 3 | Xynthesis | **Gratis seminar/webinar** signup (not classic NL) | https://www.xynthesis.nl/inschrijven-gratis-seminar/ | WPForms fields (multi) | **reCAPTCHA present** | Blocked by CAPTCHA | Documented |
| 4 | Focus Nederland | **None found** on home (contact/FAQ only) | — | — | — | — | Documented |
| 5 | Leeuwendaal | **Alumni Strengthscoach community** periodieke nieuwsbrief (not open email-only footer form located) | Article: https://www.leeuwendaal.nl/actualiteiten/de-kracht-van-de-strengthscoach-community/ ; Actualiteiten hub https://www.leeuwendaal.nl/actualiteiten/ | Gravity Forms loaded (ids 30/59/61/72) + **reCAPTCHA + Cloudflare Turnstile** on site | CAPTCHA/Turnstile | Not safe/easy | Documented; monitor webinars via public agenda |
| 6 | CareerAdvisor | **No nieuwsbrief/hs-form** on home or /blog (2026-10-01) | HubSpot CMS site | — | HubSpot tracking only | — | Documented; RSS/blog scrape alternative |
| 7 | Power4People | **None found** on home/shop | — | Contact / Vraagbaak phone | — | — | Documented |
| 8 | Nieuwe Koers | **Contact form only** (not newsletter) | https://nieuwekoers.nl/ footer `Contactformulier_footer` | Naam, Telefoon, E-mail, Bericht | **reCAPTCHA v3** | Would contact staff — **do not use** | Documented (avoid) |

---

## Detail notes

### Care4Careers Community
- Positioning: gratis community for HR — webinars, Spoor 2 tips, tools; FAQ says max one update/month; unsubscribe anytime.
- Fields confirmed 2026-10-01: `voornaam*`, `achternaam*`, `email*`, `bericht*` (+ optional bedrijf, telefoon).
- Also email field appears on other pages (same `cf-email` pattern) — treat as shared contact component.
- **Why not subscribed:** not a pure email newsletter (required message); would create a tracked lead with competitor CRM.

### Xynthesis seminar
- Event/webinar capture with WPForms + reCAPTCHA — research-useful if events listed, but signup blocked without CAPTCHA solve; prefer calendar monitoring.

### Leeuwendaal
- Best “research feed” without signup: public Actualiteiten + agenda webinars (e.g. wendbare organisatie / AI 29.09.26).
- Strengthscoach nieuwsbrief is community/alumni scoped per article language.

### Nieuwe Koers
- Footer form is **sales contact** with phone + message + recaptcha — **out of policy** (would contact competitor staff).

### Carrièrepoort / Focus / Power4People / CareerAdvisor
- No classic “inschrijven nieuwsbrief” located in static HTML this pass. CareerAdvisor blog exists but no embed subscribe form found.

---

## Recommended intel cadence (no signup)
1. Monthly WebFetch: C4C kenniscentrum newest + Focus OP star pages + CA pakketten + P4P shop prices.  
2. Leeuwendaal Actualiteiten RSS/manual.  
3. Revisit C4C community later **only if** productized to email-only without message/CAPTCHA and CoS approves hello@ use.

---

*End newsletter map 2026-10-01. Subscriptions performed: **0**.*
