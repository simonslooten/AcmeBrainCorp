---
title: NS ePublisher GVB Referentie
created: 2017-09-20T13:22:52Z
updated: 2022-12-25T13:33:13Z
tags: []
source_enex: /Users/marvin/Documents/ObsidianVault/Hermes_Team/processed/evernote/Algemeen archive.enex
notebook: Algemeen archive
author: "simon@simonslooten.com"
evernote_source: desktop.mac
---

# NS ePublisher GVB Referentie

Prisma IT heeft het ePublisher platform gebouwd. Binnen ePublisher is een aantal Output kanalen actief. Twee van die kanalen willen we hier gebruiken als refentie, samen met het overkoepelende ePublisher platform. Alle componenten zijn onderdeel van een groete oplossing die Prisma IT in samenwerking met NS gebouwd heeft. Het ePublisher platform wordt door ons inmiddels onder de naam Alliant Multi Channel Publisher als Repeatable Solution gevoerd.

De vanuit refentie oogpunt belangrijke onderdelen van ePublisher zijn:

  

ePublisher-Core \- Dit is de centrale applicatie waarbinnen een CMS is opgenomen. Redacteuren kunnen digital content (tekst, images, videos etc), afkomstig uit vele verschillende bronnen, samenvoegen tot publicaties. Een Publicatie wordt vervolgens (na doorlopen van daarvoor gedefinieerde workflows) naar een of meerdere Output Channel(s) gestuurd. Output Channels kunnen zijn: Outlets kunnen zijn: nieuwsbrieven, mobile apps, externe CMS systemen, Intranet systemen, Narrowcasting (Digital Signage) etc.

  

ePublisher Edge (OBIS) \- een van de Output Channels zijn de ePublisher Edge servers die op alle treinen geimplementeerd zijn. De Edge servers ontvangen een voor hen gepubliceerde playlist en spelen deze (een groot aantal regels volgend) af op een trein. Dit gebeurt door gegevens uitwisseling met door ons gebouwde clients die draaien op de (intelligente) schermen die in treinen zijn gemonteerd. De Edge servers verrijken de geleverde informatie met zaken als actuele rit-informatie, overstap informatie.

OBIS is een volwaardig CMS dat in alle treinen draait. Het toont niet alleen actuele (op GPS gebaseerde) reis-informatie, maar ook vertragingen, verstoringen, overstap informatie en kan informatie van een aantal andere externe bronnen tonen (zoals Amber Alerts). Omdat OBIS (mede) op GPS gebaseerd is, kan te allen tijde informatie getoond worden over de huidige locatie (wat is er in de buurt te doen, wat zie ik als ik naar buiten kijk etc).

OBIS heeft een uitgebreid koppelvlak met de zogenaamde “Intelligente Trein”, een software systeem (geleverd door een andere partij) die op basis van de sensoren die in treinen zitten, events genereert. De events worden binnen OBIS omgezet in acties voor het CMS.

Het systeem heeft een aantal externe koppelingen (zoals een koppeling naar het Buitenboord aanduiding-systeem en het omroep-systeem).

  

ePublisher Digital Signage \- Dit is een Output Channel waarbij een aantal Intelligente schermen op verschillende lokaties, waarop een door Prisma IT ontwikkelde client-applicatie draait, door ePublisher gepubliceerde playlists afspelen.

  

Als laatste zouden we willen vermelden dat Prisma IT tevens leverancier is van de software die draait op alle schermen op Nederlandse trein-perrons waarop reis-informatie getoond wordt. Daartoe behoort ook het grote Video-scherm op Schiphol. Omdat wij deze software (vanaf 2017) in een onderaannemer-rol bouwen, onderhouden en leveren voor ProRail, hebben we dit project hier niet verder als referentie uitgewerkt.

De uitwisseling van gegevens met andere externe systemen, gebeurt volgens algemene standaard formaten (in een Webservices en JSON over REST architectuur). Wij hebben de door u genoemde standaard formaten uitgebreid bestudeerd (omdat in de keten van systemen meerdere standaards gebruikt worden), we gebruiken echter ook standaards als RNet, OV9292 en Google OV Informatie.

  

ePublisher Core wordt door ons ontwikkeld in een Fixed-Price / Fix-Date structuur, waarbinnen we meerdere projecten (nieuwe functionaliteiten, nieuwe output channels en/of nieuwe input channels (zoals recent een koppeling met Amber Alerts) opleveren in nieuwe releases. Voor deze projecten dragen wij volledige project verantwoordelijkheid. De Core applicatie is door ons in een Micro-Services architectuur opgezet, zodat de impact van nieuwe releases zo klein mogelijk (waar mogelijk binnen 1 afdeling) gehouden wordt. Releases van de Core gebeuren via een geautomatiseerd systeem, waarbij we gebruik maken maken van systemen als Puppet, Maven, Jenkins, Nexus en SVN voor Automated Builds, Selenium, Maven en Jenkins voor Automated Tests en Jira en Confluence voor de adminstratieve processen.

Het uitvoeren van projecten waarbij we project verantwoordelijkheid dragen (Fixed-price/fixed-date) is overigens iets dat Prisma IT al 25 jaar doet, voor een groot aantal klanten. Die klanten bestaan voornamelijk uit grote (inter-)nationale organisaties, (landelijke) Overheid (Ministeries, Tweede Kamer en Overheidsdiensten als DUO en UWV) en non-profit instellingen.

  

Voor ePublisher Edge hebben we een doorlopend SCRUM project waar, in sprints van 3 weken, na iedere sprint een nieuwe versie van de software wordt opgeleverd.

Voor de Core applicatie geldt dat tenminste 1 versie in productie is, terwijl parallel 2 verschillende branches ontwikkeld worden (vanwege de geplande overgang van een van de aanleverende systemen naar een nieuw systeem). Er zijn dus te allen tijde tenminste 3 versies van de software (1 in RUN, 2 in CHANGE) actueel.

Via vaste intervallen worden voortgang, Sprint-planningen, voortgangsmeeting, backlog meetings en andere overleg vormen georganiseerd, zowel intern als met de klant.

  

Voor releases van de client die op de Digital Signage Systemen draait, wordt Puppet gebruikt. Remote beheer voor deze systemen wordt door ons ook - waar mogelijk - met Puppet uitgevoerd. Voor remote “hands-on” werkzaamheden wordt SSH gebruikt. 

  

Beheer op deze systemen wordt door ons geleverd op TAB niveau in een 24/7 SLA voor de verschillende ePublisher onderdelen (Core, Edge). Voor onderdelen die niet een 24/7 dekking nodig hebben (zoals Digital Signage) zijn andere SLA’s afgesloten. Voor ePublisher Core (de Centrale Applicatie) wordt door ons ook de hosting verzorgd. Hiervoor is een TB SLA afgesloten, met een 24/7 dekking. Omdat we bij deze applicatie gekozen hebben voor een Virtual Private Cloud oplossing bij een van de grote Cloud Providers, kunnen we de applicatie zeer snel up/down schalen. (meer of minder capaciteit toekennen). Tevens is disaster recovery daardoor zeer goed geregeld.

  

Als laatste willen we vermelden dat we binnen deze projecten veelvuldig ingeschakeld worden (zowel planmatig en probleem-oplossend) op het gebied van keten-integratie tussen de vele systemen die binnen dit domein gebruikt worden en die door verschillende leveranciers onderhouden en/of gebouwd worden/zijn. 

  

ePublisher Core is in een eerste versie opgeleverd in 2011. Vanaf 2014 maken verschillende bedrijfsonderdelen gebruik van ePublisher core. Dit is inmiddels een mature, stabiel product. Nieuwe releases worden een aantal malen per jaar uitgerold, met daarin nieuwe features en bug fixes.

ePublisher Digital Signage (Narrowcasting) is in productie gegaan in 2015, de voor de intelligente schermen ontwikkelde client (fixed price, fixed date met project verantwoordelijkheid) draait inmiddels 3 jaren naar volle tevredenheid. Zo nodig worden hiervoor bug-fix releases uitgerold.

ePublisher Edge (OBIS) is gedurende 2016 uitgebreid getest en is operationeel vanaf begin 2017 op een groot aantal treinen. Aan dit product wordt (in een doorlopend Scrum project) doorontwikkeld, vanwege toe te voegen features en vanwege het feit dat nieuwe (qua configuratie afwijkende) treinen aan de vloot worden toegevoegd.
