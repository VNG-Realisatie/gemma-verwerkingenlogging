---
title: "Productvisie Verwerkingenlogging API-standaard"
name: Productvisie
---

Gemeenten gebruiken binnen de uitvoering van de gemeentelijke taken grote hoeveelheden gegevens. Een deel van deze betreft gegevens over personen. Vanuit privacywetgeving zijn gemeenten verplicht het gebruik van persoonsgegevens vast te leggen en dit gebruik inzichtelijk te maken voor burgers. Deze transparantie over het gebruik van persoonsgegevens geeft de burger de mogelijkheid om na te gaan of de gemeente deze gegevens op de juiste wijze gebruikt.

Om burgers inzage te kunnen geven in de verwerking van zijn of haar persoonsgegevens is het van belang dat gemeentelijke informatiesystemen die verwerkingen gestructureerd vastleggen in logging. Om te voorkomen dat alle leveranciers van informatiesystemen zelf een werkwijze en structuur van logging moeten bedenken wordt door VNG Realisatie een API-standaard voor de logging van verwerkingen (hierna: Verwerkingenlogging API) ontwikkeld. Via deze API-standaard en daarbij behorende documentatie worden gemeenten en hun leveranciers ondersteund bij de implementatie van de verplichtingen die ten aanzien van het vastleggen van verwerking van voortvloeien uit de privacywetgeving persoonsgegevens en het bieden van transparantie over deze verwerkingen.

## Wat is de scope van de API-standaard?
Bij de vastlegging van een verwerking van een object worden niet de daadwerkelijke gegevens die verwerkt zijn vastgelegd maar categorieën van gegevens die verwerkt zijn. Daarnaast wordt een verwijzing naar het object dat verwerkt is opgenomen. Bij de verwerking van persoonsgegevens is deze verwijzing bijvoorbeeld het BSN van de persoon waarvan gegevens verwerkt zijn. Bij een verwerking wordt ook vastgelegd wat het doel en de grondslag (bijvoorbeeld wetgeving of toestemming van een burger) van de verwerking was. Dit noemen we ook wel de ‘doelbinding’. Door het vastleggen van de doelbinding kan als het over de verwerking van persoonsgegevens gaat aan de betreffende burger duidelijk worden gemaakt waarvoor de gegevens verwerkt zijn. 
Met de Verwerkingenlogging API die wordt ontwikkeld kunnen verwerkingen van objecten worden vastgelegd. Hoewel de focus ligt op het kunnen loggen van de verwerking van persoonsgegevens is er voor gekozen om de Verwerkingenlogging API flexibel op te zetten en ook geschikt te maken voor het loggen van verwerking van andere objecten (bijvoorbeeld kadastrale objecten of adresseerbare objecten). Met de Verwerkingenlogging API kunnen dus verwerkingen van verschillende soorten objecten worden vastgelegd. Hierdoor is de logging API breed inzetbaar. 

Bij de vastlegging van een verwerking van een object worden niet de daadwerkelijke gegevens die verwerkt zijn vastgelegd maar categorieën van gegevens die verwerkt zijn. Daarnaast wordt een verwijzing naar het object dat verwerkt is opgenomen. Bij de verwerking van persoonsgegevens is deze verwijzing bijvoorbeeld het BSN van de persoon waarvan gegevens verwerkt zijn. Bij een verwerking wordt ook vastgelegd wat het doel en de grondslag (bijvoorbeeld wetgeving of toestemming van een burger) van de verwerking was. Dit noemen we ook wel de ‘doelbinding’. Door het vastleggen van de doelbinding kan als het over de verwerking van persoonsgegevens gaat aan de betreffende burger duidelijk worden gemaakt waarvoor de gegevens verwerkt zijn. 

De Verwerkingenlogging API, en daarmee de vastlegging van logging in een registratie is bedoeld voor het navolgbaar maken van verwerkingen van gegevens van objecten. Het doel is niet om reconstructies te kunnen maken van situaties en gegevens in systemen op een bepaald tijdstip in het verleden.

## Voor wie wordt de API-standaard ontwikkeld?
De API-standaard wordt ontwikkeld voor partijen die informatiesystemen ontwikkelen die door gemeenten en gemeentelijke samenwerkingen worden gebruikt. Deze partijen kunnen de API-standaard implementeren in hun informatiesystemen om zodoende op een compliant manier logging te kunnen vastleggen en ontsluiten.

## Voor welke informatiesystemen is de standaard van toepassing?
Alle informatiesystemen die persoonsgegevens verwerken zijn vanuit de privacywetgeving verplicht om deze verwerkingen vast te leggen en te ontsluiten naar de burger. Dat houdt in dat implementatie van de API-standaard voor al deze informatiesystemen verplicht is. Deze verplichting geldt voor zowel bestaande als nieuwe informatiesystemen. 

Voor informatiesystemen die geen persoonsgegevens maar wel gegevens van andere soorten objecten verwerken is implementatie optioneel. 

## Wat wordt geleverd?
Door VNG Realisatie worden de onderstaande producten geboden op het gebied van de logging van de verwerking van (persoons)gegevens.

- Informatiemodel Verwerkingenlog
- API-standaard voor Logging van verwerkingen
- Referentieimplementatie van een verwerkingenlogregister
- Referentieimplementatie van een informatiesysteem wat verwerkingen logt
- Beschrijving best-practices en architectuurmodellen

## Uitwerking
Bij de uitwerking van de Verwerkingenlogging API zijn [requirements](../achtergronddocumentatie/ontwerp/requirements.md)  die voorkomen uit vigerende privacywet- en regelgeving en daaraan gerelateerde architectuuruitwerkingen geïnventariseerd. Daarnaast zijn [cases](../ontwerp/achtergronddocumentatie/cases.md) opgesteld ten aanzien van het gebruik van logging. Vanuit de uitwerking van de cases zijn [vraagstukken](../achtergronddocumentatie/ontwerp/vraagstukken.md) geïnventariseerd en zijn daar waar nodig [ontwerpbesluiten](../achtergronddocumentatie/ontwerp/ontwerpbesluiten.md) genomen en [aanbevelingen](../achtergronddocumentatie/ontwerp/aanbevelingen.md) gedaan ten aanzien van implementatie en/of scope van de Logging API. 
