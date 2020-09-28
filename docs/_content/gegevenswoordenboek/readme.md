---
title: "Gegevenswoordenboek logging van verwerkingen"
name: Gegevenswoordenboek
date: 28-09-2020
---
## Terminologie en volgorde
Dit gegevenswoordenboek beschrijft het Uitwisselingsgegevensmodel. Daarbij wordt de volgende terminologie gehanteerd:

|Term|Beschrijving|Voorbeeld|
|--|--|--|
|Objecttype|Soort object. Ook wel klasse of entiteit genoemd.|Verwerking, Verwerkingsactiviteit|
|Attribuut|Eigenschap van een objecttype.|Tijdstip registratie van de verwerking.|
|Attribuuttype|Soort eigenschap. Ook wel domein genoemd.|Datum/tijd, BSN, UUID|

Eerst worden de objecttypen beschreven met per objecttype de attributen. Daarna volgt de beschrijving van de attribuuttypen.

### Toelichting bijzondere meta-attributen
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
- [Actie](./objecttypen/attributen/Actie.md)
- [Afnemer](./objecttypen/attributen/Afnemer.md)
- [Betrokkenheid](./objecttypen/attributen/Betrokkenheid.md)
- [Bewaartermijn](./objecttypen/attributen/Bewaartermijn.md)
- [Gebruiker](./objecttypen/attributen/Gebruiker.md)
- [Gegevensbron](./objecttypen/attributen/Gegevensbron.md)
- [Handeling.Naam](./objecttypen/attributen/Handeling.Naam.md)
- [ID](./objecttypen/attributen/ID.md)
- [Naam](./objecttypen/attributen/Naam.md)
- [Object ID](./objecttypen/attributen/Object_ID.md)
- [Objecttype](./objecttypen/attributen/Objecttype.md)
- [Soort gegeven](./objecttypen/attributen/Soort_gegeven.md)
- [Soort object ID](./objecttypen/attributen/Soort_object_ID.md)
- [Systeem](./objecttypen/attributen/Systeem.md)
- [Tijdstip](./objecttypen/attributen/Tijdstip.md)
- [Tijdstip registratie](./objecttypen/attributen/Tijdstip_registratie.md)
- [Uitvoerder](./objecttypen/attributen/Uitvoerder.md)
- [Vertrouwelijkheid](./objecttypen/attributen/Vertrouwelijkheid.md)
- [Vervallen](./objecttypen/attributen/Vervallen.md)
- [Verwerking.ID](./objecttypen/attributen/Verwerking.ID.md)
- [Verwerking.Naam](./objecttypen/attributen/Verwerking.Naam.md)
- [Verwerking afnemer](./objecttypen/attributen/Verwerking_afnemer.md)
- [Verwerkingsactiviteit.ID](./objecttypen/attributen/Verwerkingsactiviteit.ID.md)
- [Verwerkt object](./objecttypen/attributen/Verwerkt_object.md)

## Attribuuttypen

