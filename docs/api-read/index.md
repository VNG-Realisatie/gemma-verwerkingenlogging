---
layout: page-with-side-nav
title: Verwerkingenlogging inzage API-standaard
date: 28-03-2022
---

# Verwerkingenlogging inzage API-standaard

## Functionele view Inzage API

Onderstaande tabel beschrijft de door de inzage API geboden functies. Klik op de naam van de functie voor de beschrijving.

| Categorie \ Functie  |
| :----------- |
| Opvragen | 
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F4086: Opvragen verwerkte objecten – Beperkte set velden, niet vertrouwelijk](../achtergronddocumentatie/ontwerp/artefacten/4086.md) |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F2008: Opvragen verwerkte objecten – Beperkte set velden, niet vertrouwelijk of vertrouwelijkheid opgeheven](../achtergronddocumentatie/ontwerp/artefacten/2008.md) |

## Technische view Inzage API

### OAS

- **Published** versie van de API specificatie (OAS3) in
  [ReDoc](http://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/master/docs/api-read/oas-specification/logging-verwerkingen-api/openapi.yaml),
  [Swagger](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/master/docs/api-read/oas-specification/logging-verwerkingen-api/openapi.yaml) of
  [YAML](https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/master/docs/api-read/oas-specification/logging-verwerkingen-api/openapi.yaml).

- **Development** versie van de API specificatie (OAS3) in
  [ReDoc](http://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/develop/docs/api-read/oas-specification/logging-verwerkingen-api/openapi.yaml),
  [Swagger](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/develop/docs/api-read/oas-specification/logging-verwerkingen-api/openapi.yaml) of
  [YAML](https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/develop/docs/api-read/oas-specification/logging-verwerkingen-api/openapi.yaml).

### Aanvullende specificaties Inzage API

Klik op de API-call in de onderstaande tabel om de aanvullende specificaties te zien.

| Type | API-call |
| :---- | :------- |
| REST | [GET /verwerkte-objecten](./aanvullendespecificatie-verwerkteobjecten-get.md) |

### Opmerkingen
- De autorisatie-scopes zijn [hier](./oas-specification/logging-verwerkingen-api/scopes.md) beschreven. Als de API call niet voldoet aan de scope dan zal een `HTTP 403 (Forbidden)` foutmelding worden teruggegeven.

## Gehanteerde standaarden
Op de verwerkingenlogging API-standaard zijn de volgende standaarden van toepassing:
- [De REST-API Design Rules (ADR)](https://forumstandaardisatie.nl/open-standaarden/rest-api-design-rules)
- [MIM - Metamodel Informatie Modellering v1.1](https://docs.geostandaarden.nl/mim/mim/)
