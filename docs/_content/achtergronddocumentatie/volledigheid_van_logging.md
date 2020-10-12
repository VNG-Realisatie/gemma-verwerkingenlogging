---
title: "Volledigheid van logging"
name: Volledigheid van logging
date: 28-09-2020
---

## Introductie
De API-standaard kan doordat de meeste attributen in het uitwisselgegevensmodel optioneel zijn eenvoudig worden geimplementeerd. Hoe meer veldden worden ingevuld hoe zinvoller de informatie die wordt vastgelegd is en hoe duidelijker de informatie voor de burger is. Het streven moet dus zijn zoveel mogelijk attributen vast te leggen. 

## Minimale versus maximale logging
Onderstaande afbeelding toont logging in zijn meest basale vorm.

<img src="./_assets/minimaal.png" alt="Minimale variant van logging" width="700"/>

-	Het gemeentelijk VAR is nog geen informatiesysteem maar een document of spreadsheet. De verwerkingsactiviteiten in het VAR zijn al wel voorzien van een uniek ID ([UUID](../gegevenswoordenboek/attribuuttypen/UUID.md)) zodat er vanuit het log naar het VAR verwezen kan worden.
-	Vanuit de gedachte ‘beter iets dan niets loggen’ worden van het [uitwisselingsgegevensmodel](../gegevensmodel/uitwisselingsgegevensmodel/readme.md) alleen de meest basale attributen gebruikt. Dit zal niet leiden tot een voor de burger begrijpelijk log maar het is een begin en beter dan niets.

Ter vergelijking laat onderstaande afbeelding een voorbeeld zien van het maximale gebruik van logging.

<img src="./_assets/maximaal.png" alt="Maximale variant van logging" width="700"/>

-	Het VAR is een informatiesysteem.
-	Van het [uitwisselingsgegevensmodel](../gegevensmodel/uitwisselingsgegevensmodel/readme.md) worden alle attributen gebruikt. Dit zal leiden tot een veel begrijpelijker log voor de burger.
-	Bij volledige implementatie van de API is het nu mogelijk om:
    - Bewaartermijnen die later in een proces bekend worden te registreren.
    - De vertrouwelijkheid van verwerkingen op te heffen.
    - De logging over bepaalde verwerkingen logisch te verwijderen.
    - Et cetera.
    
    




