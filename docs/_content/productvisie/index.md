---
title: "Productvisie Verwerkingenlogging API-standaard"
name: Productvisie
---

Gemeenten gebruiken binnen de uitvoering van de gemeentelijke taken grote hoeveelheden gegevens. Een deel van deze gegevens betreft persoonsgegevens. Vanuit de privacywetgeving zijn gemeenten verplicht dit gebruik van persoonsgegevens vast te leggen, en inzichtelijk te maken voor burgers. Door deze transparantie over het gebruik van persoonsgegevens heeft de burger de mogelijkheid om na te gaan of de gemeente zijn of haar gegevens rechtmatig gebruikt. Naast de gegevens van personen worden door gemeenten ook gegevens van andere 'objecten', zoals kadastrale percelen, verwerkt. Hoewel er geen wettelijke verplichting bestaat om deze verwerkingen vast te leggen in logging kan het wel een toegevoegde waarde hebben. 

Door VNG Realisatie wordt een API-standaard ontwikkeld waarmee de verwerkingen van de gegevens van objecten kunnen worden vastgelegd en ontsloten. Vanuit deze logging is navolgbaar voor welk doel de gemeente gegevens heeft gebruikt binnen de gemeentelijke processen. Het doel van de API-standaard, en daarmee de vastlegging van logging in een registratie is bedoeld voor het navolgbaar maken van verwerkingen van gegevens van objecten. Het doel is niet om reconstructies te kunnen maken van situaties en gegevens in systemen op een bepaald tijdstip in het verleden.

Door een API-standaard te ontwikkelen vanuit VNG Realisatie wordt voorkomen dat leveranciers van gemeentelijke informatiesystemen zelf een werkwijze en structuur van logging moeten bedenken. Het voorkomt ook dat gemeenten met verschillende implementaties van logging van verwerkingen worden geconfronteerd met alle problemen ten aanzien van ontsluiting van deze gegevens naar de burger. De API-standaard is voorbereid op de mogelijkheid om de verwerking van gegevens van een breed scala van objecttypen te ondersteunen. In eerste instantie richt de API-standaard zich echter op de vastlegging van de verwerking van persoonsgegevens. Zowel de publiek- als privaatrechtelijke verwerking van persoonsgegevens door de gemeente zijn hierbij in scope van de API-standaard.


## Voor wie wordt de API-standaard ontwikkeld?
De API-standaard wordt ontwikkeld voor partijen die informatiesystemen ontwikkelen die door gemeenten en gemeentelijke samenwerkingen worden gebruikt. Deze partijen kunnen de API-standaard implementeren in hun informatiesystemen om zodoende op een compliant manier logging te kunnen vastleggen en ontsluiten.


## Wat is de scope van de API-standaard?
Bij de vastlegging van een verwerking van een object worden niet de daadwerkelijke gegevens die verwerkt zijn vastgelegd maar de metagegevens van de verwwerking. Daarnaast wordt een verwijzing naar het object dat verwerkt is opgenomen. Bij de verwerking van persoonsgegevens is deze verwijzing bijvoorbeeld het BSN van de persoon waarvan gegevens verwerkt zijn. Bij een verwerking wordt als onderdeel van de metagegevens vastgelegd wat het doel en de grondslag (bijvoorbeeld wetgeving of toestemming van een burger) van de verwerking was. Dit wordt de ‘doelbinding’ genoemd. Door het vastleggen van de doelbinding kan als het over de verwerking van persoonsgegevens gaat aan de betreffende burger duidelijk worden gemaakt waarvoor de gegevens verwerkt zijn.  





## Voor welke informatiesystemen is de standaard van toepassing?
Alle informatiesystemen die persoonsgegevens verwerken zijn vanuit de privacywetgeving verplicht om deze verwerkingen vast te leggen en te ontsluiten naar de burger. Dat houdt in dat implementatie van de API-standaard voor al deze informatiesystemen verplicht is. Deze verplichting geldt voor zowel bestaande als nieuwe informatiesystemen. 

Voor informatiesystemen die geen persoonsgegevens maar wel gegevens van andere soorten objecten verwerken is implementatie optioneel. 


