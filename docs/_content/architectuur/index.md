---
title: "Architectuur"
name: architectuur
---
De Verwerkingenlogging API-standaard standaardiseerd de wijze waarop processystemen de verwerking van (persoons)gegevens kunnen vastleggen in verwerkingenlogs en deze verwerkingenlogs kunnen ontsluiten naar geautoriseerde afnemers. Deze standaard vult hiermee een deel van de functies in die in de gemeentelijke informatievoorziening nodig zijn om invulling te kunnen geven aan de [Verantwoordingsplicht uit de AVG](https://autoriteitpersoonsgegevens.nl/nl/onderwerpen/algemene-informatie-avg/verantwoordingsplicht).

De Verwerkingenlogging API-standaard biedt ondersteuning voor:

* vastlegging in een verwerkingenlog van verwerkingen van (persoons)gegevens die door processystemen worden uitgevoerd;
* bevraging door geautoriseerde afnemers van een verwerkinglog .

Vanuit de AVG worden op het gebied van transparantie over de verwerking van persoonsgegevens nog aanvullende eisen gesteld. Het gaat hierbij om:

* het vastleggen van de verwerkingsactiviteiten van de gemeente in een Gemeentelijk register van verwerkingsactiviteiten en het bieden van transparantie over deze verwerkingsactiviteiten naar burgers, en
* het vastleggen van toestemmingen van burgers voor de (bovenwettelijke) verwerking van persoonsgegevens. 

In onderstaande schets is weergegeven welke informatiesystemen een rol spelen bij de implementatie van de verschillende aspecten van de Verantwoordingsplicht. De onderdelen die door de Verwerkingenlogging API-standaard worden afgedekt zijn hierbij rood omkaderd aangegeven. 

<img src="./_assets/API_standaard_werkingsgebied.png" alt="API-standaard" width="700"/>

Ten aanzien van de ontsluiting van het Gemeentelijk register van verwerkingsactiviteiten is een API-standaard in ontwikkeling. Deze standaard wordt naar verwachting in het eerste kwartaal van 2021 opgeleverd. Nadere informatie over deze standaard is [hier](https://github.com/VNG-Realisatie/gemma-verwerkingsactiviteiten) beschikbaar.

Gemeenten hebben ten aanzien van de inrichting van de verschillende informatiesystemen die in bovenstaande schets zijn opgenomen een aantal keuzes te maken. Zo kan gekozen worden voor één centraal verwerkingenlog voor de gemeente of kan de keuze worden gemaakt binnengemeentelijk meerdere verwerkingslogs te hanteren. Op GEMMAonline zijn de verschillende architectuurscenario's uitgewerkt. Deze uitwerking is [hier](https://www.gemmaonline.nl) te vinden. 

