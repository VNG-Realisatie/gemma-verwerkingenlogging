---
layout: page-with-side-nav
title: Ontwerp
date: 28-03-2022
---

# Ontwerp
Het ontwerp van de API-standaard is gericht op het kunnen opstellen van een gegevensmodel en de benodigde API’s. Onderdeel van het ontwerp zijn: 
- de gehanteerde [afkortingen en terminologie](../ontwerp/terminologie.md)
- [cases](./ontwerp/ontwerpcases.md) die rond verwerkingenlogging en verwerking zijn uitgeschreven, en
- [ontwerpbesluiten](./ontwerp/ontwerpbesluiten.md) en [aanbevelingen](./ontwerp/aanbevelingen.md) ten aanzien van implementatie van de API-standaard.

Daarnaast zijn er een aantal nog [openstaande vraagstukken](./ontwerp/vraagstukken.md) waar nog een standpunt op moet worden ingenomen.

Een Excel overzicht van de verschillende ontwerpartefacten per case is [hier](./ontwerp/artefacten/Artefacten_en_Cases.xlsx) te downloaden.

## Scope en diepgang van het ontwerp
De diepgang van het ontwerp is gericht op het kunnen opstellen van een gegevensmodel en de benodigde API’s. Het ontwerp kan daarmee wel als startpunt dienen voor de realisatie van een verwerkingenlog maar zal daarvoor niet voldoende zijn. Het grootste gedeelte van het ontwerp gaat over het conceptueel en logisch niveau van verwerkingenlogging. Waar nodig worden korte uitstapjes naar de techniek gemaakt. Bijvoorbeeld om van een bepaald onderdeel te toetsen of het ook implementeerbaar is.

## Codering van ontwerpartefacten
De verschillende onderdelen van het ontwerp noemen we artefacten. Alle artefacten in het ontwerp zijn voorzien van een uniek willekeurig nummer en een prefix. De prefix geeft hierbij aan wat voor soort artefact het betreft. Zo verwijst A5042 naar Aanbeveling 5042 en B4362 naar het Besluit met nummer 4362.

| Prefix | Soort artefact |
|--|--|
| A	| Aanbeveling |
| B	| Besluit |
| C	| Case |
| F	| Functie in API |
| V	| Vraagstuk |

De nummer van artefacten is uniek over de artefacten heen. Als er dus een A5042 bestaat kan er geen B5042 bestaan. 

Vanuit de verschillende artefacten wordt verwezen naar andere artefacten. Zo kan in een casebeschrijving een verwijzing worden gemaakt naar een vraagstuk. Deze verwijzingen zijn in de documentatie via links naar de artefacten opgenomen.

## Voorbeelden binnen de artefacten
Alle gegevens in de voorbeelden zijn fictief en niet gebaseerd op personen of persoonsgegevens uit de werkelijkheid. Om te voorkomen dat de BSN’s in voorbeelden overeenkomen met BSN’s uit de praktijk zijn alle BSN’s in de voorbeelden 7 cijfers i.p.v. 9 cijfers lang.

## Relatie met het gemeentelijk verwerkingsactiviteitenregister (VAR)
In het ontwerp worden enkele aannamen gedaan over de vorm en de werking van het VAR. De koppeling tussen VAR en verwerkingenlog is zo beperkt mogelijk gehouden. De minimale API die een gemeentelijk VAR dient te ondersteunen is beschreven in de [API-standaard ten behoeve van verwerkingsactiviteiten](https://github.com/VNG-Realisatie/gemma-verwerkingsactiviteiten).

Regelmatig wordt gesproken over het Landelijk VAR. Hierbij gaan we ervanuit dat er naast de gemeentelijke VAR’s ook een gemeenschappelijk landelijk register bestaat: het Landelijk VAR. Mocht dit register (nog) niet bestaan dan kunnen de passages over dit register genegeerd worden. Het Landelijk VAR is vooral van belang vanuit het perspectief van standaardisatie van de inhoud van het gemeentelijk VAR. Vanuit het perspectief van het verwerkingenlog bevat het gemeentelijk VAR gewoon verwerkingsactiviteiten. Of deze afkomstig zijn uit het Landelijk VAR maakt voor het verwerkingenlog niet uit. 

