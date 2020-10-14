---
title: "Uitgangspunten"
name: Uitgangspunten
date: 14-10-2020
---
Bij het opstellen van de API-standaard zijn een aantal uitgangspunten, of leidende principes, gehanteerd. Deze uitgangspunten zijn gehanteerd als de ankerpunten van de API-standaard. Bij iedere afweging die ten aanzien van het oplossen van vraagstukken is gemaakt zijn deze uitgangspunten meegewogen. De uitgangspunten zijn:

- [Het perspectief van de burger is leidend](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#het-perspectief-van-de-burger-is-leidend)
- [Het doel is duiden, niet reconstrueren](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#het-doel-is-duiden-niet-reconstrueren)
- [Privacy by design](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#privacy-by-design)
- [We faciliteren laagdrempelige inbouw](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#we-faciliteren-laagdrempelige-inbouw)
- [De implementatie laten we over aan de markt](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#de-implementatie-laten-we-over-aan-de-markt)

In onderstaande paragrafen worden deze uitgangspunten nader toegelicht en worden de ontwerpbesluiten en aanbevelingen die een directe relatie hebben met het uitgangspunt benoemd.

## Het perspectief van de burger is leidend
Onderstaande aanbevelingen en ontwerpbesluiten zijn direct gericht op de het perspectief van de burger of bevatten elementen die daaraan gerelateerd zijn.

### Cases


### Aanbevelingen
- [A5924: Mogelijkheden om duidelijke logentries te maken](./ontwerp/artefacten/5924.md)

### Ontwerpbesluite
-	[B6856: Hiërarchie: Verwerkingsactiviteit, Verwerking, Handeling en Actie](./ontwerp/artefacten/6856.md)
- [B1598: Opname van Betrokkenheid](./ontwerp/artefacten/1598.md)
- [B6247 - Opname van Verwerkt soort gegeven](./ontwerp/artefacten/6247.md)
- [B7952: Loggen vanuit applicatie - Welke momenten en hoe vaak](./ontwerp/artefacten/7952.md)

### Openstaande vraagstukken
- [V3934 - Loggen van afgeleide informatie](./ontwerp/artefacten/3934.md)
- [V7168 - Logging van selecties](./ontwerp/artefacten/7168.md)

## Het doel is duiden, niet reconstrueren
- [B5469: Doelstelling van logging - Duiden versus reconstrueren](./ontwerp/artefacten/5469.md)

## Privacy by design
Onderstaande cases, ontwerpbesluiten en functies zijn direct gericht op de bescherming van de privacy of bevatten elementen die daaraan gerelateerd zijn.

### Cases
In onderstaande cases is bijzondere aandacht besteed aan de bescherming van de privacy.
- [C4081: Registratie Verhuizing – Zoeken op geboortedatum en naam](./ontwerp/artefacten/4081.md)
- [C5889: Zoekvraag – Onbekende zoekcriteria, vooraf gedefinieerde resultaatvelden](./ontwerp/artefacten/5889.md)
- [C3677: Inzage door burger](./ontwerp/artefacten/3677.md)
- [C9713: Inzage door burger – Gegevens die niet langer vertrouwelijk zijn](./ontwerp/artefacten/9713.md)
- [C9713: Inzage door burger – Gegevens die niet langer vertrouwelijk zijn](./ontwerp/artefacten/9713.md)
- [C5953: Inzage door gemeentelijk medewerker](./ontwerp/artefacten/5953.md)
- [C9041: Notificaties – Informatiearm](./ontwerp/artefacten/9041.md)

### Ontwerpbesluiten
- [B3238: Alleen identificatoren en geen achterliggende waarden](./ontwerp/artefacten/3238.md)
- [B2042: Pseudonimisering BSN](./ontwerp/artefacten/2042.md)
- [B9207: Opname van Gebruiker](./ontwerp/artefacten/9207.md)
- [B3908: Opname van Vertrouwelijkheid](./ontwerp/artefacten/3908.md)
- [B8157: Opname van Verwerking ID en Verwerking afnemer](./ontwerp/artefacten/8157.md)
- [B7972: Identificatie van personen bij privaatrechtelijke taken](./ontwerp/artefacten/7972.md)
- [B7952: Loggen vanuit applicatie - Welke momenten en hoe vaak](./ontwerp/artefacten/7952.md)
- [B9177: Meegeven van informatie t.b.v. logging in API’s](./ontwerp/artefacten/9177.md)

### Functies
- [F4086: Opvragen Acties – Beperkte set velden, niet vertrouwelijk](./ontwerp/artefacten/4086.md)
- [F6624: Log Vertrouwelijke Actie](./ontwerp/artefacten/6624.md)
- [F2969: Wijzig vertrouwelijkheid van Verwerking](./ontwerp/artefacten/2969.md)
- [F2525: Opvragen Acties – Beperkte set velden, vertrouwelijkheid opgeheven](./ontwerp/artefacten/2525.md)

## We faciliteren laagdrempelige inbouw
- [B9177: Meegeven van informatie t.b.v. logging in API’s](./ontwerp/artefacten/9177.md)

Bij het opstellen van het [Uitwisselingsgegevensmodel (UGM)](../../gegevensmodel/uitwisselingsgegevensmodel/readme.md) hebben overwegingen ten aanzien van de implementeerbaarheid van de API-standaard door leveranciers een grote rol gespeeld. Getracht is om de balans te vinden voor snelle en succesvolle eerste implementaties van de API door eenvoud en het tegelijkertijd faciliteren van leveranciers die logging in de meest volledige vorm willen implementeren. 

functgioneel verplicht

## De implementatie laten we over aan de markt
Ten aanzien van het gebruik van functies uit de API-standaard zijn verschillende spelregels opgesteld. Zo is het bijvoorbeeld verplicht om om bepaalde header informatie mee te geven als die te herleiden is. Daarnaast is beschreven op welke momenten verwerkingen gelogd moeten worden. Ten aanzien van de wijze waarop een leverancier de API-standaard inbouwd worden geen dwingende adviezen gegeven. Wel worden best-practices beschreven bijvoorbeeld ten aanzien van hoe in het kader van privacy by design kan worden omgegaan met de opslag van logging van vertrouwelijke en niet vertrouwelijke verwerkingen. Ook ten aanzien van de wijze waarop logging technisch in een logregister wordt opgenomen (via een persistent queueing mechanisme of direct) worden wel handreikingen gedaan maar geen verplichtingen opgelegd.

Het is aan leveranciers om te bepalen hoe de aanbevelingen en ontwerpbesluiten worden vertaald naar technische oplossingen. Het kan uiteraard wel zo zijn dat gemeenten in hun rol van opdrachtgever eisen gaan stellen aan de technische inrichting.

