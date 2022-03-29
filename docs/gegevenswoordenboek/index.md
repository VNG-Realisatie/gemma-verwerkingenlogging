---
layout: page-with-side-nav
title: Gegevenswoordenboek logging van verwerkingen
date: 28-03-2022
---

# Gegevenswoordenboek logging van verwerkingen

## Terminologie en volgorde
Dit gegevenswoordenboek beschrijft het [uitwisselingsgegevensmodel (UGM)](../gegevensmodel/uitwisselingsgegevensmodel/readme.md). Daarbij wordt de volgende terminologie gehanteerd:

|Term|Beschrijving|Voorbeeld|
|--|--|--|
|Objecttype|Soort object. Ook wel klasse of entiteit genoemd.|Verwerking, Verwerkingsactiviteit|
|Attribuut|Eigenschap van een objecttype.|Tijdstip registratie van de verwerking.|
|Attribuuttype|Soort eigenschap. Ook wel domein genoemd.|Datum/tijd, BSN, UUID|

## Bijzondere meta-attributen
Bij alle attributen is het meta-attribuut ‘Aanwezigheid’ opgenomen. Dit meta-attribuut geeft aan of het attribuut ingevuld ofwel ’aanwezig’ moet zijn of niet. Bij diverse attributen kunnen er omstandigheden zijn waardoor het attribuut niet altijd bepaald kan worden. Technisch gezien leidt dit tot een ‘optioneel’ attribuut.

In het gegevenswoordenboek spreken we in dergelijke gevallen over *‘Verplicht indien …’*. Bijvoorbeeld *‘Verplicht indien relevant’* of *‘Verplicht indien te bepalen’*. Ofwel:
-	Als het attribuut in de programmatuur bepaald kan worden, moet het wel degelijk altijd ingevuld te worden.
-	Kan het niet bepaald worden, maar bijvoorbeeld wel gevraagd worden aan de gebruiker, dan moet dat gedaan worden.
-	Kan ook de gebruiker het niet altijd bepalen? Geef deze dan bijvoorbeeld wel een waarschuwing dat het attribuut/veld bij voorkeur ingevuld moet worden.

## Objecttypen
- [Verwerkingsactie](./objecttypen/Verwerkingsactie.md)
- [Verwerkt object](./objecttypen/Verwerkt_object.md)
- [Verwerkt soort gegeven](./objecttypen/Verwerkt_soort_gegeven.md)

## Attribuuttypen
- [Identificator](./attribuuttypen/Identificator.md)
- [Ja/Nee](./attribuuttypen/Ja_Nee.md)
- [Moment](./attribuuttypen/Moment.md)
- [Naam](./attribuuttypen/Naam.md)
- [Objecttype](./attribuuttypen/Objecttype.md)
- [Organisatie Identificatie Nummer (OIN)](./attribuuttypen/OIN.md)
- [Periode](./attribuuttypen/Periode.md)
- [Uniform Resource Identifier (URI)](./attribuuttypen/URI.md)
- [Universal Unique IDentifier (UUID)](./attribuuttypen/UUID.md)
- [Vertrouwelijkheid](./attribuuttypen/Vertrouwelijkheid.md)

