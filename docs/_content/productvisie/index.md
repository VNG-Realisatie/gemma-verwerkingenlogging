---
title: "Productvisie Verwerkingenlogging API-standaard"
name: Productvisie
---

## Algemeen
Gemeenten gebruiken binnen de uitvoering van de gemeentelijke taken grote hoeveelheden gegevens. Een deel van deze gegevens betreft persoonsgegevens. Vanuit de privacywetgeving zijn gemeenten verplicht dit gebruik van persoonsgegevens vast te leggen, en inzichtelijk te maken voor burgers. Door deze transparantie over het gebruik van persoonsgegevens heeft de burger de mogelijkheid om na te gaan of de gemeente zijn of haar gegevens rechtmatig gebruikt. Naast de gegevens van personen worden door gemeenten ook gegevens van andere 'objecten', zoals kadastrale percelen, verwerkt. Hoewel er geen wettelijke verplichting bestaat om van deze objecten  verwerkingen vast te leggen kan het wel een toegevoegde waarde hebben. 

Door VNG Realisatie wordt de Verwerkingenlogging API-standaard ontwikkeld. Met deze API-standaard wordt de wijze waarop de verwerking van gegevens van een object worden vastgelegd en ontsloten gestandaardiseerd. Een object kan hierbij een persoon zijn maar ook bijvoorbeeld een kadastraal object. Het doel van de API-standaard, en daarmee de vastlegging van verwerkingen in een logregistratie is het kunnen duiden van verwerkingen van objectgegevens. De standaard is niet bedoeld, en ook niet geschikt voor het maken van reconstructies van situaties en gegevens in systemen op een bepaald tijdstip in het verleden. Via implementatie van de API-standaard in persoonsgegevens verwerkende systemen kan invulling worden gegeven aan (een deel) van de [AVG Verantwoordingsplicht](https://autoriteitpersoonsgegevens.nl/nl/onderwerpen/algemene-informatie-avg/verantwoordingsplicht). 

Ten aanzien van de Verwerkingenlogging API-standaard zijn een aantal belangrijke uitgangspunten benoemd.

- [Het perspectief van de burger is leidend](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#het-perspectief-van-de-burger-is-leidend)
- [Het doel is duiden, niet reconstrueren](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#het-doel-is-duiden-niet-reconstrueren)
- [Privacy by design](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#privacy-by-design)
- [We faciliteren laagdrempelige inbouw](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#we-faciliteren-laagdrempelige-inbouw)
- [De implementatie laten we over aan de markt](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/achtergronddocumentatie/uitgangspunten.md#de-implementatie-laten-we-over-aan-de-markt)

Door een API-standaard te ontwikkelen vanuit VNG Realisatie wordt voorkomen dat leveranciers van gemeentelijke informatiesystemen zelf een werkwijze en structuur van verwerkingenlogging moeten bedenken. Het voorkomt ook dat gemeenten met verschillende implementaties van logging van verwerkingen worden geconfronteerd met alle problemen ten aanzien van ontsluiting van deze gegevens naar de burger. De API-standaard is voorbereid op de mogelijkheid om de verwerking van gegevens van een breed scala van objecttypen te ondersteunen. In eerste instantie richt de API-standaard zich echter op de vastlegging van de verwerking van persoonsgegevens. Zowel de publiek- als privaatrechtelijke verwerking van persoonsgegevens door de gemeente zijn hierbij in scope van de API-standaard. Uitgangspunt bij de ontwikkeling van de API-standaard is 'privacy by design'.   

## Voor wie wordt de API-standaard ontwikkeld?
De API-standaard wordt ontwikkeld voor partijen die informatiesystemen ontwikkelen die door gemeenten en gemeentelijke samenwerkingen worden gebruikt. Deze partijen kunnen de API-standaard implementeren in hun informatiesystemen om zodoende op een compliant manier verwerkingenlogging te kunnen vastleggen en ontsluiten. De API-standaard is zowel op bestaande als nieuwe informatiesystemen gericht. Initieel ligt de focus van de API-standaard op het faciliteren van de vastlegging en ontsluiting van verwerkingen van persoonsgegevens. Op een later moment wordt de standaard uitgebreidt naar voor vastlegging en ontsluiting van gegevens van andere objecten. 

Hoewel deze API-standaard primair ontwikkeld is voor gebruik door gemeenten en hun softwareleveranciers is de standaard ook toepasbaar binnen andere delen van de overheid. De standaard bevat namelijk geen gemeente-specifieke elementen. 

## Wordt de API-standaard verplicht?
De API-standaard is toepasbaar voor alle informatiesystemen die gegevens van objecten verwerken. Voor informatiesystemen die geen persoonsgegevens maar wel gegevens van andere soorten objecten verwerken is implementatie optioneel. Voor systemen die wel persoonsgegevens verwerken is de API-standaard aanbevolen.

Gezien het belang van de API-standaard voor de regie van burgers op hun eigen gegevens is het het streven om de verwerkingenlogging API-standaard op termijn verplicht te maken voor alle gemeentelijke systemen die persoonsgegevens verwerken. Hiertoe zal na oplevering van de eerste productie-versie van de API-standaard een traject worden opgestart richting het College van Dienstverleningszaken van de VNG.

## Toegevoegde waarde voor gemeenten
- Gemeenten kunnen op een eenvoudige, en gestandaardiseerde wijze de verwerkingenlogging ontsluiten van informatiesystemen die de API-standaard hebben geïmplementeerd;
- Gemeenten kunnen informatiesystemen die de API-standaard hebben geïmplementeerd eenvoudig koppelen aan een gemeentelijk verwerkingenloggingregister;
- Gemeenten kunnen op een gestandaardiseerde wijze burger faciliteren in hun recht op inzage van verwerkingen van hun gegevens;

## Toegevoegde waarde voor leveranciers
- Geen eigen ontwerp van een koppelvlak nodig en daardoor lagere kosten;
- Naadloze integratie met verwerkingenloggingregisters van andere partijen.





