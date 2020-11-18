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
Misschien wel het belangrijkste gehanteerde uitgangspunt is dat de burger bij de inzage in het verwerkingenlog voor hem of haar begrijpelijke informatie ziet. Als we niet alleen naar de letter maar ook naar de geest van de AVG willen handelen, dan is het bijzonder belangrijk om burgers bij inzage een duidelijk verwerkingenlog te kunnen presenteren. De burger moet de informatie uit het verwerkingenlog kunnen herleiden naar processen of acties die voor hem of haar herkenbaar zijn. Hoe herkenbaarder de informatie in het verwerkingenlog is hoe minder vragen de burger er over zal hebben en hoe minder vragen de gemeente dus krijgt. Het moet vanuit de vastlegging van de verwerkingen voor de burger dus duidelijk zijn:
- wat er met zijn of haar gegevens is gedaan, en 
- waarom de gegevens verwerkt zijn. 

Duidelijkheid over de verwerkingenlogentries begint bij een goede inrichting van het gemeentelijk register van verwerkingsactiviteiten (het VAR). De verwerkingen die worden vastgelegd in het verwerkingenlog worden immers gerelateerd aan een verwerkingsactiviteit uit het VAR. Het VAR moet dus zo min mogelijk generieke en dus zoveel mogelijk specifieke verwerkingsactiviteiten bevatten. De verwerkingsactiviteiten moeten vervolgens voorzien zijn van een duidelijk doel, grondslag en een toelichting op die grondslag. Daarnaast moeten de verwerkingenlogentries zelf zo informatief mogelijk zijn. De standaard biedt mogelijkheden om [uitgebreide informatie over een verwerking](./volledigheid_van_logging.md) vast te leggen. Het is wel zo dat hoe meer informatie vastgelegd wordt hoe ingewikkelder de implementatie van de standaard wordt.

Onderstaande aanbevelingen, ontwerpbesluiten en openstaande vraagstukken zijn gerelateerd aan het perspectief van de burger.

### Aanbevelingen
- [A5924: Mogelijkheden om duidelijke verwerkingenlogentries te maken](./ontwerp/artefacten/5924.md)

### Ontwerpbesluiten
-	[B6856: Hiërarchie: Verwerkingsactiviteit, Verwerking, Handeling en Actie](./ontwerp/artefacten/6856.md)
- [B1598: Opname van Betrokkenheid](./ontwerp/artefacten/1598.md)
- [B6247 - Opname van Verwerkt soort gegeven](./ontwerp/artefacten/6247.md)
- [B7952: Loggen vanuit applicatie - Welke momenten en hoe vaak](./ontwerp/artefacten/7952.md)

### Openstaande vraagstukken
- [V3934 - Loggen van afgeleide informatie](./ontwerp/artefacten/3934.md)
- [V7168 - Logging van selecties](./ontwerp/artefacten/7168.md)

## Het doel is duiden, niet reconstrueren
Het verwerkingenlog is primair bedoeld als ondersteunend middel voor het kunnen voldoen aan de verantwoordingsplicht uit de AVG. Het verwerkingenlog is dus bedoeld voor het kunnen aantonen dat een verwerking aan de belangrijkste beginselen van verwerking heeft voldaan, zoals rechtmatigheid, transparantie, doelbinding en juistheid. Het verwerkingenlog is niet bedoeld om reconstructies te maken van situaties en gegevens in systemen op een bepaald tijdstip in het verleden (audit-trail). Mocht de burger, of bijvoorbeeld gemeentelijke privacy officer, naar aanleiding van de gepresenteerde duiding van verwerkingen nadere vragen hebben dan kunnen eventuele 'forensische' onderzoeken worden uitgevoerd bij de applicaties die de gegevens daadwerkelijk hebben verwerkt.

- [B5469: Doelstelling van logging - Duiden versus reconstrueren](./ontwerp/artefacten/5469.md)

## Privacy by design
Bij de ontwikkeling van de standaard is vanaf het begin rekening gehouden met de bescherming van de privacy van personen (burgers en medewerkers van de gemeente). Het gaat daarbij om vraagstukken over noodzakelijkheid van het opslaan van gegevens; welke gegevens zijn echt nodig en welke niet? Ook is rekening  gehouden met de levenscyclus van gegevens in een verwerkingenlogregister. Hoe worden deze aangemaakt, gewijzigd en verwijderd en hoe is het mogelijk om daar regie op te voeren. Ook ten aanzien van de de toegang tot gegevens zijn maatregelen genomen die de bescherming van de privacy verhogen. Voorbeelden daarvan zijn de aanbevelimng om BSNs in het verwerkingenlog te pseudonimiseren en de aanbeveling om verwerkingenlogging van vertrouwelijke en niet-vertrouwelijke verwerkingen apart van elkaar op te slaan. Implementatie hiervan wordt ondersteund door API-functies van de standaard.

Onderstaande cases, ontwerpbesluiten en functies zijn direct gericht op de bescherming van de privacy of bevatten elementen die daaraan gerelateerd zijn.

### Cases
In onderstaande cases is bijzondere aandacht besteed aan de bescherming van de privacy.
- [C4081: Registratie Verhuizing – Zoeken op geboortedatum en naam](./ontwerp/artefacten/4081.md)
- [C5889: Zoekvraag – Onbekende zoekcriteria, vooraf gedefinieerde resultaatvelden](./ontwerp/artefacten/5889.md)
- [C3677: Inzage door burger](./ontwerp/artefacten/3677.md)
- [C9713: Inzage door burger – Gegevens die niet langer vertrouwelijk zijn](./ontwerp/artefacten/9713.md)
- [C5953: Inzage door gemeentelijk medewerker](./ontwerp/artefacten/5953.md)
- [C9041: Notificaties – Informatiearm](./ontwerp/artefacten/9041.md)

### Ontwerpbesluiten
- [B3238: Alleen identificatoren en geen achterliggende waarden](./ontwerp/artefacten/3238.md)
- [B2042: Pseudonimisering BSN](./ontwerp/artefacten/2042.md)
- [B9207: Opname van Gebruiker](./ontwerp/artefacten/9207.md)
- [B3908: Opname van Vertrouwelijkheid](./ontwerp/artefacten/3908.md)
- [B7972: Identificatie van personen bij privaatrechtelijke taken](./ontwerp/artefacten/7972.md)
- [B7952: Verwerkingen loggen vanuit applicatie - Welke momenten en hoe vaak](./ontwerp/artefacten/7952.md)
- [B9177: Meegeven van informatie t.b.v. verwerkingenlogging in API’s](./ontwerp/artefacten/9177.md)

### Functies
- [F4086: Opvragen Acties – Beperkte set velden, niet vertrouwelijk](./ontwerp/artefacten/4086.md)
- [F6624: Log Vertrouwelijke Actie](./ontwerp/artefacten/6624.md)
- [F2969: Wijzig vertrouwelijkheid van Verwerking](./ontwerp/artefacten/2969.md)
- [F2525: Opvragen Acties – Beperkte set velden, vertrouwelijkheid opgeheven](./ontwerp/artefacten/2525.md)

## We faciliteren laagdrempelige inbouw
Een belangrijk uitgangspunt bij de totstandkoming van de API-standaard is dat deze voor leveranciers op relatief eenvoudige wijze, en tegen acceptabele inspanning ingebouwd kan worden. Met de wetenschap dat de bestaande informatiesystemen niet zijn ontworpen op het kunnen loggen conform de eisen van de AVG is vanuit de gedachte ‘beter iets dan niets loggen’ besloten dat de informatie die vastgelegd wordt in verwerkingenlogging moet kunnen varieeren van [basisinformatie tot zeer uitgebreide informatie](./volledigheid_van_logging.md). Een gevolg van deze keuze is dat zo min mogelijk attributen 'verplicht' moeten worden ingevuld. Er is in plaats daarvan gekozen voor een systeem waarbij gegevens technisch niet verplicht zijn in te vullen, maar functioneel verplicht kunnen zijn. Dit houdt in dat als een gegeven bekend is, of tegen beperkte inspanning bekend kan worden, het moet worden opgenomen in de verwerkingenlogging. Zie [deze](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/tree/master/docs/_content/gegevenswoordenboek#bijzondere-meta-attributen) pagina voor een nadere uitleg.

Bij het opstellen van het [Uitwisselingsgegevensmodel (UGM)](../gegevensmodel/uitwisselingsgegevensmodel/readme.md) hebben overwegingen ten aanzien van de implementeerbaarheid van de API-standaard door leveranciers een grote rol gespeeld. Getracht is om de balans te vinden voor snelle en succesvolle eerste implementaties van de API door eenvoud en het tegelijkertijd faciliteren van leveranciers die verwerkingenlogging in de meest volledige vorm willen implementeren. 

Er is verder gekozen om een systeem te hanteren waarbij bestaande APIs niet 'opengebroken' hoeven te worden om de voor verwerkingenlogging benodigde attributen mee te geven. Besloten is om de payload van bestaande APIs niet te wijzigen en verwerkingenlogging attributen via http header attributen mee te geven. Zie [B9177: Meegeven van informatie t.b.v. verwerkingenlogging in API’s](./ontwerp/artefacten/9177.md) voor een nadere uitleg.

## De implementatie laten we over aan de markt
Ten aanzien van het gebruik van functies uit de API-standaard zijn verschillende spelregels opgesteld. Zo is het bijvoorbeeld verplicht om om bepaalde header informatie mee te geven als die te herleiden is. Daarnaast is beschreven op welke momenten verwerkingen gelogd moeten worden. Ten aanzien van de wijze waarop een leverancier de API-standaard inbouwd worden geen dwingende adviezen gegeven. Wel worden best-practices beschreven bijvoorbeeld ten aanzien van hoe in het kader van privacy by design kan worden omgegaan met de opslag van verwerkingenlogging van vertrouwelijke en niet vertrouwelijke verwerkingen. Ook ten aanzien van de wijze waarop verwerkingenlogging technisch in een verwerkingenlogregister wordt opgenomen (via een persistent queueing mechanisme of direct) worden wel handreikingen gedaan maar geen verplichtingen opgelegd.

Het is aan leveranciers om te bepalen hoe de aanbevelingen en ontwerpbesluiten worden vertaald naar technische oplossingen. Het kan uiteraard wel zo zijn dat gemeenten in hun rol van opdrachtgever eisen gaan stellen aan de technische inrichting.

Onderstaande ontwerpbesluiten geven richting aan de implementatie van de API-standaard maar zijn geen verplichtingen.
- [B8970: Benadering verwerkingenlog bij gefedereerde inrichting](./ontwerp/artefacten/8970.md)
- [B2042: Pseudonimisering BSN](./ontwerp/artefacten/2042.md)



