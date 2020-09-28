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
- [ID](./objecttypen/ID.md)
- [Naam](./objecttypen/Naam.md)
- [Handeling.Naam](./objecttypen/Handeling.Naam.md)
- [Verwerking.Naam](../objecttypen/Verwerking.Naam.md)
- [Verwerking.ID](./objecttypen/Verwerking.ID.md)
- [Verwerkingsactiviteit.ID](./objecttypen/Verwerkingsactiviteit.ID.md)
- [Vertrouwelijkheid](./objecttypen/Vertrouwelijkheid.md)
- [Bewaartermijn](./objecttypen/Bewaartermijn.md)
- [Uitvoerder](./objecttypen/Uitvoerder.md)
- [Systeem](./objecttypen/Systeem.md)
- [Gebruiker](./objecttypen/Gebruiker.md)
- [Gegevensbron](./objecttypen/Gegevensbron.md)
- [Afnemer](./objecttypen/Afnemer.md)
- [Verwerking afnemer](./objecttypen/Verwerking_afnemer.md)
- [Tijdstip](./objecttypen/Tijdstip.md)
- [Tijdstip registratie](./objecttypen/Tijdstip_registratie.md)
- [Vervallen](./objecttypen/Vervallen.md)
