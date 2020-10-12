---
title: "API's"
name: API's
---
## Algemeen
De onderstaande APIs maken deel uit van de API-standaard voor de logging van verwerkingen. Ten aanzien van een aantal APIs geldt dat nog overwogen wordt of ze op deze wijze deel uit gaan maken van de API-standaard. Bij de APIs waar dit het geval is is dit aangegeven met een `*`.

## Over de implementatie van de API-standaard
Applicaties of services die de logging API-standaadr implementeren moeten op diverse punten worden aangepast. Uiteindelijk  moet voldaan worden aan alle onderstaande punten:

- Bij alle acties die persoonsgegevens verwerken wordt er gelogd ([B7952](../achtergronddocumentatie/ontwerp/artefacten/7952.md)). Hierbij gelden de volgende regels:
    - Alle verwerkingen hebben een eigen ID ([B8157](../achtergronddocumentatie/ontwerp/artefacten/8157.md)).
        - Als de verwerking overeenkomt met een proces uit de bedrijfsvoering (zoals een verzoek of zaak) en dit proces heeft een eigen UUID dan kan dit UUID gebruikt worden.
        - In alle andere gevallen moet een nieuw UUID toegewezen worden.
    - Het ID van de verwerking wordt gelogd en kan later gebruikt worden om acties die over deze verwerking gelogd zijn terug te vinden in het log en deze aan te passen of logisch te verwijderen.
    - Acties worden zodanig omschreven dat deze duidelijk zijn voor de burger. Hiertoe worden waar mogelijk en zinvol alle attributen van de actie ingezet ([A5924](../achtergronddocumentatie/ontwerp/artefacten/5924.md).

- Roept de applicatie/service een API aan waarbij die API persoonsgegevens verwerkt? Dan moet bij deze aanroep in de header de volgende informatie meegegeven worden ([B7259](../achtergronddocumentatie/ontwerp/artefacten/7259.md), [B9177](../achtergronddocumentatie/ontwerp/artefacten/9177.md)): OIN, Verwerking ID, Vertrouwelijkheid en Bewaartermijn.
Zie ‘Toevoeging aan de header van alle persoonsgegevens-verwerkende API’s’ voor meer informatie.

-  Wordt een service geboden waarbij persoonsgegevens verwerkt worden? Dan moet bij de uitvoering daarvan gekeken worden of in de header van de aanroep de volgende gegevens aanwezig zijn: OIN, Verwerking ID, Vertrouwelijkheid en Bewaartermijn. Deze gegevens dienen overgenomen te worden bij het loggen van de verwerking. Zie ‘*Toevoeging aan de header van alle persoonsgegevens-verwerkende API’s*’ voor meer informatie.
- De applicatie of service ondersteunt alle functies van de API.



## Logging APIs
- [F7446: Log Actie](../achtergronddocumentatie/ontwerp/artefacten/7446.md)
- [F6624: Log Vertrouwelijke Actie](../achtergronddocumentatie/ontwerp//artefacten/6624.md) `*` 
- [F2969: Wijzig vertrouwelijkheid van Verwerking](../achtergronddocumentatie/ontwerp//artefacten/2969.md)
- [F2969: Wijzig bewaartermijn van Verwerking](../achtergronddocumentatie/ontwerp//artefacten/2969.md)
- [F8316: Wijzig Actie](../achtergronddocumentatie/ontwerp//artefacten/8316.md)
- [F3835: Wijzig Vertrouwelijke Actie](../achtergronddocumentatie/ontwerp//artefacten/3835.md)
- [F9906: Verwijder Actie](../achtergronddocumentatie/ontwerp//artefacten/9906.md)
- [F2265: Verwijder Vertrouwelijke Actie](../achtergronddocumentatie/ontwerp//artefacten/2265.md) `*` 
- [F4086: Opvragen Acties – Beperkte set velden, niet vertrouwelijk](../achtergronddocumentatie/ontwerp//artefacten/4086.md)
- [F2525: Opvragen Acties – Beperkte set velden, vertrouwelijkheid opgeheven](../achtergronddocumentatie/ontwerp//artefacten/2525.md)
- [F9787: Opvragen Acties – Alle velden, niet vertrouwelijk](../achtergronddocumentatie/ontwerp//artefacten/9787.md)
- [F0143: Opvragen Acties – Alle velden, vertrouwelijk](../achtergronddocumentatie/ontwerp//artefacten/0143.md)


## Gehanteerde standaarden
Op de API-standaard voor logging zijn de volgende standaarden van toepassing:
-	[De REST-API Design Rules (ADR)](https://forumstandaardisatie.nl/open-standaarden/rest-api-design-rules)

Verder is gebruik gemaakt van onderdelen van de volgende standaarden:
-	[API Designrule extensions (Nederlandse API Strategie IIb)](https://docs.geostandaarden.nl/api/API-Strategie-ext/)
