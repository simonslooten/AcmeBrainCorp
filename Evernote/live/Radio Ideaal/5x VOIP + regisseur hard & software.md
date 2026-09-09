---
id: "c377ed2a-0df6-1711-3cfd-86c4106aa8fc"
title: "5x VOIP + regisseur hard & software"
notebook: "Radio Ideaal"
created: "2026-06-12T11:40:52+00:00"
updated: "2026-06-12T11:56:31+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# 5x VOIP + regisseur hard & software

Aanbevolen architectuur
VoIP Phone System
 (sterk aanbevolen: geen analoge hybrids meer)
Telos VX (Prime of Enterprise)
 → beste keuze voor broadcast.
Native Dante/Livewire/AoIP-integratie.
Per-lijn mix-minus (automatisch of programmeerbaar).
Conferencing: callers kunnen elkaar + studio horen (minus eigen signaal).
GPIO/logica voor Axite-bediening.
Uitstekende echo-cancellation en processing.
Alternatief: Andere broadcast-VoIP zoals Broadcast Partners oplossingen of een goede SIP-server (Asterisk/FreePBX) met hybrid-software, maar Telos is professioneler en betrouwbaarder voor 24/7.
Axite-configuratie
Centrale I/O-rack
: VoIP-outputs (5 kanalen) komen via Dante binnen als individuele bronnen in de matrix.
Eén “Phone Fader”
 in de hoofd-Studio Axite (bijv. Studio 1):
Deze fader krijgt een 
sum
 van de 5 callers (via een sub-buss of VCA/DCA-groep).
De presentator heeft dus één fader voor alle telefoons.
Aparte regisseur-surface
 (extra Axite surface of extender in dezelfde of aangrenzende ruimte):
Volledige toegang tot de 5 individuele caller-kanalen.
De regisseur kan individuele lijnen cue’en, muten, op air zetten, levels aanpassen en talkback sturen.
Mix-Minus per lijn (kritiek punt)
Elke VoIP-lijn krijgt een 
dedicated mix-minus return
 (Clean Feed):
Program + alle andere callers + eventuele jingles/muziek.
Minus
 het eigen callersignaal (om echo/feedback te voorkomen).
Met Telos VX + Axite matrix is dit standaard te configureren:
Maak 5 aparte Aux/Mix-Minus bussen (Axite heeft er 16).
Of gebruik de ingebouwde per-line mix-minus van Telos en routeer die terug via Dante.
Resultaat: Lijn 1 hoort studio + lijnen 2-5 perfect, zonder zichzelf. Idem voor de anderen.
Talkback 
&
 onderlinge communicatie
Studio → Callers
: Via de mix-minus returns (regisseur of presentator kan talkback activeren via dedicated talkback-bussen – Axite heeft er 16).
Callers onderling
: Telos VX ondersteunt conferencing, zodat callers elkaar kunnen horen (via de matrix).
Regisseur → Callers / Presentator
: Dedicated talkback-knoppen op de regisseur-surface (MambaNet/GPIO).
Regisseur → Studio
: Via CRM-bussen of aparte talkback.
Praktische lay-out 
&
 gebruiksgemak
Regisseur-surface
: Extra 6-fader (of meer) Axite surface/extender. Deze beheert de 5 lijnen individueel + de sum-fader naar de studio.
Custom buttons
: Op beide surfaces programmeer je buttons zoals “Line 1 On Air”, “All Callers Dump”, “Talkback Regisseur”, “Conference All”.
Redundantie
: Dubbele VoIP-lijnen, backup hybrids, en failover in de Axite-matrix.
Compliance
: Logging van alle calls via de automation of master control.
Update aan het schema
 (ik pas het vorige diagram aan met deze phone-setup).
Volgende stappen als je technische adviseur
Inventariseer huidige telefoonoplossing (aantal lijnen, SIP-provider).
Vraag een demo aan van Telos VX bij een D
&
R/Broadcast Partners dealer.
We configureren in de Axite web-interface: Source Pool → 5 callers + 5 mix-minus outputs.
Testen in Studio 1 met regisseur-setup.
Dit maakt jullie talk/sports-programma’s echt top-professioneel, zonder echo-problemen en met soepele regie. Stuur meer details over jullie huidige telefoonlijnen of budget, dan maken we een exacte kosten/benefits-vergelijking en configuratie-stappen.
Wat is het eerste dat je wilt uitdiepen (Telos details, Axite button-programming, of kostenplaatje)? We bouwen dit robuust en gebruiksvriendelijk uit!
