---
id: "c177f3be-ad93-4dd1-bfae-394b54f7bf8a"
title: "NS OBIS 2017"
notebook: "Prisma IT - Projecten"
created: "2017-02-10T07:48:23+00:00"
updated: "2017-02-20T07:47:59+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# NS OBIS 2017

Bespreking Offerte Q393 OBIS 2017Q1
Inbelnummer: (010) 299 10 01 Deelnemerscode: 69518916
Input Mark over noodzakelijke verbeteringen
requirements niet duidelijk en uitgewerkt (vb buitenboord aanduiding, vb grafischare kaart, TSI/PRM vaak aangepast)
we zijn afhankelijk van anderen (bijv Nomad, CGI) voor omgevingen. (bijv ons Testrig in R’dam is wederom niet up-to-date)
Inrichten testsystem Intel trein loopt uit uren door vele opleveren
Werking Presentatiebus is nog niet duidelijk (ligt bij Nomad)
Ondersteuning bij releases is niet of moeilijk in te schatten
Hardware op testomgevingen is niet gelijk
Wij kunnen geen pre-release tests doen op testwalls NS
Er zijn veel materieel afhankelijkheden die pas in productie beshcikbaar zijn (32 schermen)
Op veel omgevingen geen toegang (test/acc/prod) dus kunnen we onze eigen logfiles niet zien, die moeten bij Nomad opgevraagd worden. Zijn regelmatig dan al weggegooid
Er zijn onbekende materieel afhankelijkheden (vb CFA trein). Testmuur wordt nu gebouwd, we hebben nauwelijks specs. We kunnen dus niet inschatten of het gaat werken.
Dus bij inschatting EPICS gaat minstend 80% van de werkzaamheden buiten de inschatting vallen.
- tekst opnemen dat sp3 en 4 worden ingeschat.
- JDI architect / consultant opnemen
- 
Run vs change
Vanwege het feit dat er nu ook tenminste één productie versie van de OBIS software zal zijn, gaat er een interactie komen tussen Run en change requests. De wijze waarop wij dit proces ingericht hebben is als volgt:
- Alle change werkzaamheden, inclusief de “project”-werkzaamheden zijn in deze offerte opgenomen. Onze visie is dat als er vanuit de beheer-organisatie een change request komt, die request in de vorm van een of meerdere tickets in een sprint opgenomen wordt. Als het gevolg daarvan is dat beschikbare resources ontoereikend zijn, dan zullen we daar contact over opnemen via de project teams van beide organisaties.
 - Alle andere SLA requests worden in een normale 1e, 2e, 3e lijns aanpak behandeld. Het is de bedoeling dat alleen in uitzonderings-situaties benodigde resources “uit het project” gehaald moeten worden om een SLA-ticket af te kunnen handelen. De daarmee gemoeid zijnde werkzaamheden rusten dan bij ons niet op het project. Simpel gezegd: men schrijft die uren bij ons op het SLA-project, waarover wij apart rapporteren.
