---
layout: page-with-side-nav
title: GEMMA Verwerkingenlogging
date: 28-05-2024
---
# Verwerkingenlogging
Organisaties die persoonsgegevens verwerken zijn conform de [Algemene Verordening Gegevensbescherming (AVG)](https://autoriteitpersoonsgegevens.nl/nl/over-privacy/wetten/algemene-verordening-gegevensbescherming-avg) en de [Uitvoeringswet AVG](https://wetten.overheid.nl/BWBR0040940/2019-02-19) verplicht om aan te kunnen tonen dat een verwerking van persoonsgegevens aan de belangrijkste beginselen van verwerking voldoet, zoals rechtmatigheid, transparantie, doelbinding en juistheid. Om aan deze verantwoordingsplicht te kunnen voldoen is het van belang dat per verwerking de belangrijkste metagegevens van de verwerkingen worden vastgelegd. Standaardisatie van de vastlegging van verwerkingen is van belang om de eenduidigheid en toegankelijkheid van deze gegevens te borgen. Door VNG-Realisatie is de Verwerkingenlogging API-standaard als onderdeel van de uitwerking van de informatiekundige visie Common Ground ontwikkeld en opgenomen in de GEMMA referentiearchitectuur. Deze API-standaard biedt leveranciers van informatiesystemen gestandaardiseerde API-specificaties voor het vastleggen en ontsluiten van metagegevens behorend bij vastgelegde (gelogde) verwerkingen.

## Status van de API-standaard (1 juli 2025)
Deze API-standaard is in 2023 opgeleverd als 1.0 versie. Gedurende het daaropvolgende standaardisatieproces heeft VNG een juridische toets laten uitvoeren op de uitwerking van de standaard. In deze toetsing is zowel gekeken naar de metagegevens die via de API-standaard kunnen worden vastgelegd als naar de wijze waarop de API-standaard in de informatievoorziening ingepast wordt.  Kern van het juridisch oordeel was dat voor de logging van individuele verwerkingen in een centraal register geen grondslag aanwezig is met betrekking tot het inzagerecht (art. 15 AVG), de beveiligingsplicht (art. 32 AVG) en de verantwoordingsplicht (art. 5(2) AVG).
Het inrichten van een centraal register waarin identificerende persoonsgegevens en acties die in verschillende informatiesystemen binnen gemeenten hebben plaatsgevonden worden vastgelegd gaat volgens het juridisch oordeel verder dan de logging die voor gemeenten noodzakelijk is om aan eerdergenoemde verplichtingen te voldoen. Een dergelijke inrichting voldoet in die zin niet aan de vereisten van proportionaliteit en subsidiariteit bij het treffen van passende beveiligingsmaatregelen.
 
Dit juridisch oordeel heeft ertoe geleid dat de VNG de standaard niet verder kan brengen in het standaardisatieproces. Naar aanleiding van dit juridisch oordeel heeft de VNG contact opgenomen met BZK om te bespreken op welke manier we tot een juridisch geborgde standaard kunnen komen. BZK heeft vervolgens de VNG standaard als basis gebruikt voor een nieuwe standaard die geborgd is in een juridisch beleidskader: het [Logboek Dataverwerkingen](https://logius-standaarden.github.io/logboek-dataverwerkingen-juridisch-beleidskader/). Deze standaard vervangt daarmee de VNG standaard. De VNG standaard wordt niet verder beheerd of doorontwikkeld. Indien u gebruik maakt van deze standaard beveelt de VNG u aan om te migreren naar de Logboek Dataverwerkingen standaard.

## Werkingsgebied 
Het primaire werkingsgebied voor deze API-standaard is: gemeenten en gemeentelijke samenwerkingsverbanden. Ook andere organisaties kunnen deze API-standaard hanteren aangezien er geen gemeente-specifieke zaken in de API-standaard zijn opgenomen.

## Inhoud van de API-standaard
- [Informatie- en gegevensmodel](./gegevensmodel/index.md)
- [API-specificaties (bewerking)](./api-write/index.md)
- [API-specificaties (inzage)](./api-read/index.md)
- [Referentieimplementatie van een verwerkingenlogregister](./referentieimplementatie.md)

## Documentatie
- [Productvisie](./productvisie.md)
- [Quickstart Guide](./quickstart.md)
- [Architectuur](./architectuur.md)
- [Informatie- en gegevensmodel](./gegevensmodel/index.md)
- [API-specificaties (bewerking)](./api-write/index.md)
- [API-specificaties (inzage)](.//api-read/index.md)
- [Achtergronddocumentatie](./achtergronddocumentatie/index.md)

## Beheer en ondersteuning
Deze standaard wordt niet meer beheerd of doorontwikkeld

## Licentie
Copyright &copy; VNG Realisatie 2022
Licensed under the [EUPL](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/LICENCE.md)
