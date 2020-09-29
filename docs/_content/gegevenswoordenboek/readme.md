---
title: "Gegevenswoordenboek logging van verwerkingen"
name: Gegevenswoordenboek
date: 28-09-2020
---
## Terminologie en volgorde
Dit gegevenswoordenboek beschrijft het [uitwisselingsgegevensmodel (UGM)](../gegevensmodel/uitwisselingsgegevensmodel/readme.md). Daarbij wordt de volgende terminologie gehanteerd:

|Term|Beschrijving|Voorbeeld|
|--|--|--|
|Objecttype|Soort object. Ook wel klasse of entiteit genoemd.|Verwerking, Verwerkingsactiviteit|
|Attribuut|Eigenschap van een objecttype.|Tijdstip registratie van de verwerking.|
|Attribuuttype|Soort eigenschap. Ook wel domein genoemd.|Datum/tijd, BSN, UUID|

## Bijzondere meta-attributen
Bij alle attributen is het meta-attribuut ‘Aanwezigheid’ opgenomen. Dit meta-attribuut geeft aan of het attribuut ingevuld ofwel ’aanwezig’ dient te zijn of niet. Bij diverse attributen kunnen er omstandigheden zijn waardoor het attribuut niet altijd bepaald kan worden. Technisch gezien leidt dit tot een ‘optioneel’ attribuut.

In het gevenswoordenboek spreken we in dergelijke gevallen over *‘Verplicht indien …’*. Bijvoorbeeld *‘Verplicht indien relevant’* of *‘Verplicht indien te bepalen’*. Ofwel:
-	Als het attribuut in de programmatuur bepaald kan worden, dient het weldegelijk altijd ingevuld te worden.
-	Kan het niet bepaald worden, maar bijvoorbeeld wel gevraagd worden aan de gebruiker, dan dient dat gedaan te worden.
-	Kan ook de gebruiker het niet altijd bepalen? Geef deze dan bijvoorbeeld wel een waarschuwing dat het attribuut/veld bij voorkeur ingevuld dient te worden.

## Objecttypen
- [Actie](./objecttypen/Actie.md)
- [Verwerkt object](./objecttypen/Verwerkt_object.md)
- [Verwerkt soort gegeven](./objecttypen/Verwerkt_soort_gegeven.md)

## Attributen
- [Actie](./attributen/Actie.md)
- [Afnemer](./attributen/Afnemer.md)
- [Betrokkenheid](./attributen/Betrokkenheid.md)
- [Bewaartermijn](./attributen/Bewaartermijn.md)
- [Gebruiker](./attributen/Gebruiker.md)
- [Gegevensbron](./attributen/Gegevensbron.md)
- [Handeling.Naam](./attributen/Handeling.Naam.md)
- [ID](./attributen/ID.md)
- [Naam](./attributen/Naam.md)
- [Object ID](./attributen/Object_ID.md)
- [Objecttype](./attributen/Objecttype.md)
- [Soort gegeven](./attributen/Soort_gegeven.md)
- [Soort object ID](./attributen/Soort_object_ID.md)
- [Systeem](./attributen/Systeem.md)
- [Tijdstip](./attributen/Tijdstip.md)
- [Tijdstip registratie](./oattributen/Tijdstip_registratie.md)
- [Uitvoerder](./attributen/Uitvoerder.md)
- [Vertrouwelijkheid](./attributen/Vertrouwelijkheid.md)
- [Vervallen](./attributen/Vervallen.md)
- [Verwerking.ID](./attributen/Verwerking.ID.md)
- [Verwerking.Naam](./attributen/Verwerking.Naam.md)
- [Verwerking afnemer](./attributen/Verwerking_afnemer.md)
- [Verwerkingsactiviteit.ID](./attributen/Verwerkingsactiviteit.ID.md)
- [Verwerkt object](./attributen/Verwerkt_object.md)

## Attribuuttypen
- [Aantal jaar](./attribuuttypen/Aantal_jaar.md)
- [Identificator](./attribuuttypen/Identificator.md)
- [Ja/Nee](./attribuuttypen/Ja_Nee.md)
- [Mate van vertrouwelijkheid](./attribuuttypen/Mate_van_vertrouwelijkheid.md)
- [Moment](./attribuuttypen/Moment.md)
- [Naam](./attribuuttypen/Naam.md)
- [Objecttype](./attribuuttypen/Objecttype.md)
- [Organisatie Identificatie Nummer (OIN)](./attribuuttypen/OIN.md)
- [Universal Unique IDentifier (UUID)](./attribuuttypen/UUID.md)

