---
id: "e16a9d74-139f-41c4-b5f1-ed519679bff3"
title: "NS ePublisher"
notebook: "Default Notebook"
created: "2015-06-21T18:34:18+00:00"
updated: "2015-06-21T18:50:49+00:00"
deleted: false
body_source: "offline_search"
source: evernote-local-live
---

# NS ePublisher

Prisma IT heeft in opdracht van de NS de ePublisher ontwikkeld als online management-tool voor Digitale informatie de binnen de NSverwerkt moet worden. Op basis van voorkeuren en “business-rules” wordt digitale informatie verdeeld naar zogenaamde “channels’.

Channels kunnen publieke websites zijn, maar ook email-nieuwsbrieven, gedrukte nieuwsbrieven, twitter, CMS’s, de NS RailPocket, RSS feeds, Persberichten en andere kanelen. Momenteel wordt er door NS en Prisma IT hard gewerkt aan het toevoegen van kanalen voor NarrowCasting (NedTrain) aan “de wal” en op treinen (OBIS).

Het “beheerders-deel” van de applicatie wordt afgeschermd met behulp van username/password combinaties. Er is gesproken over, en gewerkt aan een koppeling met het zogenaamde ADFS systeem van NS, maar door verschillende oorzaken (administratief en/of organisatorisch binnen NS), heeft er nog geen productie-release plaatsgevonden. Het gevolg van deze wijziging zou zijn dat beheerders van de applicatie en de content, met hun NS username/password in het ePublisher systeem zouden kunen inloggen.

Aan de “voorkant” van de applicatie (dit is de “publieke” zijde waar informatie door het systeem beschikbaar gesteld wordt aan verschillende kanalen) is geen authenticatie en/of authorisatie ingebouwd. Het systeem is dus vooraslnog niet bedoeld om “gevoelige” of interne informatie mee beschikbaar te stellen voor intern gebruik.

Over de beveiliging valt een aantal dingen te zeggen:

1. Het aanleveren van informatie door ePublisher aan kanalen die deze informatie op een of andere wijze publiceren, gebeurt beveiligt. Als ePublisher dus informatie zou aanleveren aan bijvoorbeeld een intern NS Intranet CMS, dan is door ePublisher de link naar het CMS beveiligt. Het Intranet CMS heeft de verantwoordelijkheid voor de beveiliging van de gepubliceerde content

2. Informatie die door ePublisher direct, middels een ePublisher website beschikbaar gesteld wordt, is niet beveiligd. de webpagina’s die ePublisher beschibaar stelt, zijn algemeen toegankelijk. Gebruik van ePublisher op deze wijze is dus nooit bedoeld geweest voor het bschikbaar stellen van “gevoelige informatie.

3. Er is in het verleden wel gesproken over het definieren van een beveiligings model voor informatie die door ePublisher via ePublisher websites gepubliceerd wordt. Er is een aantal manieren waarop een dergelijke beveiliging gerealiseerd zou kunnen worden. Prisma IT gaat hierover graag in gesprek met NS.
