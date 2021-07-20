---
title: "Verwerkingenlogging inzage API-standaard"
name: Verwerkingenlogging inzage API-standaard
date: 05-07-2021
---

## Functionele view

Onderstaande tabel beschrijft de door de API geboden functies. Klik op de naam van de functie voor de beschrijving.

| Categorie \ Functie  |
| :----------- |
| Opvragen | 
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F2008: Opvragen Verwerkingsacties – Beperkte set velden, niet vertrouwelijk of vertrouwelijkheid opgeheven](../achtergronddocumentatie/ontwerp/artefacten/2008.md) |


## Technische view
| Categorie \ Functie  |
| :----------- |
| Opvragen | 
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F2008: Opvragen Verwerkingsacties – Beperkte set velden, niet vertrouwelijk of  vertrouwelijkheid opgeheven](../achtergronddocumentatie/ontwerp/artefacten/2008.md) |

### OAS
API specificatie (OAS3) in
  [ReDoc](http://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/master/docs/_content/api-read/openapi.yaml),
  [Swagger](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/master/docs/_content/api-read/openapi.yaml) of
  [YAML](https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/master/docs/_content/api-read/openapi.yaml).

### Aanvullende specificaties

Klik op de API-call in de onderstaande tabel om de aanvullende specificaties te zien.

| Type | API-call |
| :---- | :------- |
| REST | [GET /verwerkte-objecten](./aanvullendespecificatie-verwerkteobjecten-get.md) |

### Opmerkingen
- De autorisatie-scopes zijn [hier](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/api-read/oas-specification/logging-verwerkingen-api/scopes.md) beschreven. Als de API call niet voldoet aan de scope dan zal een `HTTP 403 (Forbidden)` foutmelding worden teruggegeven.

## Gehanteerde standaarden
Op de verwerkingenlogging API-standaard zijn de volgende standaarden van toepassing:
- [De REST-API Design Rules (ADR)](https://forumstandaardisatie.nl/open-standaarden/rest-api-design-rules)
- [MIM - Metamodel Informatie Modellering v1.1](https://docs.geostandaarden.nl/mim/mim/)
