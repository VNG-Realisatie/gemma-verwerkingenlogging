---
title: "Documentatie"
name: Documentatie
---
De documentatie bij de verwerkingenlogging API-standaard bestaat uit API-standaard documentatie en achtergrondinformatie. De achtergrondinformatie maakt geen onderdeel uit van de API-standaard maar vergroot het begrip en biedt achtergronden bij de genomen besluiten en gedane aanbevelingen.

## API-standaard documentatie
De onderstaande documentatie maakt deel uit van de verwerkingenlogging API-standaard.

- [Gegevens- en informatiemodel](../gegevensmodel/index.md)
- [API-specificatie](../api/index.md)
- [Quick Start Gids](../quickstart/index.md)

## Definition of Done
Bij de uitvoering van het project wordt een [Definition of Done (DoD)](../achtergronddocumentatie/definition_of_done.md) gehanteerd. Deze DoD is de checklist met criteria waar de API-standaard bij oplevering aan moet voldoen. 

## Achtergrondinformatie bij de API-standaard


### Informatieanalyse uitwerking
Bij het informatieanalyse is gebruik gemaakt van een aantal [brondocumenten](../achtergronddocumentatie/ontwerp/brondocumenten.md). De informatieanalyse is onderdeel van het [ontwerp](./ontwerp.md) van de API-standaard en is gericht op het helder krijgen van de functionele vereisten. De uitkomsten van de informatieanalyse zijn input voor het opstellen van een gegevens- en informatiemodel en de vertaling daarvan naar APIs. De volgende zaken zijn in de informatieanalyse uitgewerkt:

- de gehanteerde [afkortingen en terminologie](../achtergronddocumentatie/ontwerp/terminologie.md)
- [cases](../achtergronddocumentatie/ontwerp/ontwerpcases.md) die rond verwerkingenlogging zijn uitgeschreven 
- [ontwerpbesluiten](../achtergronddocumentatie/ontwerp/ontwerpbesluiten.md) en [aanbevelingen](../achtergronddocumentatie/ontwerp/aanbevelingen.md) ten aanzien van implementatie
- [openstaande vraagstukken](../achtergronddocumentatie/ontwerp/vraagstukken.md) waarover nog geen ontwerpbesluit is genomen 

Een overzicht van de relatie tussen besluiten en cases is [hier](./ontwerp/artefacten/20201011_Artefacten_en_cases.xlsx) te vinden.

### Verwerkingenlogging Maturity Levels
Gemeenten, systemen, leveranciers en derden zullen de komende jaren allemaal in een verschillend stadium verkeren t.a.v. het implementeren van de vastlegging van verwerkingen in verwerkingenlogging. Het lijkt goed om in een dashboard bij te gaan houden hoe gemeenten en de gemeentelijke software ervoor staan. Hierbij zou gebruik gemaakt kunnen worden van volwassenheidniveaus ten aanzien van verwerkingenlogging. Hiertoe zijn een aantal [Verwerkingenlogging Maturity Levels](./logging_maturity_level.md) ontwikkeld die gebruikt kunnen worden door gemeenten.

### Volledigheid van verwerkingenlogging 
De API-standaard kan doordat de meeste attributen in het uitwisselgegevensmodel optioneel zijn eenvoudig worden geimplementeerd. Hoe meer veldden worden ingevuld hoe zinvoller de informatie die wordt vastgelegd is en hoe duidelijker de informatie voor de burger is. Het streven moet dus zijn zoveel mogelijk attributen vast te leggen. Op de pagina [volledigheid van verwerkingenlogging](./volledigheid_van_logging.md) worden de verschillen van volledigheid van invulling geillustreerd.
