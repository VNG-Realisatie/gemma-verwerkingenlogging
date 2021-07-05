---
title: "Verwerkingenlogging ontsluiting API-standaard"
name: Verwerkingenlogging ontsluiting API-standaard
date: 05-07-2021
---

# Deze pagina beschrijft de API-standaard voor het ontsluiten van verwerkingsacties op verwerkte objecten. De pagina is in ontwikkeling. De inhoud van deze pagina  en is nog niet geschikt voor systeemontwikkeling. 

## Functionele view

Onderstaande tabel beschrijft de door de API geboden functies. Klik op de naam van de functie voor de beschrijving.

| Categorie \ Functie  |
| :----------- |
| Opvragen | 
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F4086: Opvragen Verwerkingsacties – Beperkte set velden, niet vertrouwelijk](../achtergronddocumentatie/ontwerp/artefacten/4086.md) |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F2525: Opvragen Verwerkingsacties – Beperkte set velden, vertrouwelijkheid opgeheven](../achtergronddocumentatie/ontwerp/artefacten/2525.md) |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F9787: Opvragen Verwerkingsacties – Alle velden, niet vertrouwelijk](../achtergronddocumentatie/ontwerp/artefacten/9787.md)	| 
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; [F0143: Opvragen Verwerkingsacties – Alle velden, vertrouwelijk](../achtergronddocumentatie/ontwerp/artefacten/0143.md) | 

## Technische view

### OAS



### Aanvullende specificaties

Klik op de API-call in de onderstaande tabel om de aanvullende specificaties te zien.

| Type | API-call |
| :---- | :------- |
| REST | [GET /verwerkteObjecten](./aanvullendespecificatie-verwerkteobjecten-get.md) |

### Opmerkingen
- De autorisatie-scopes zijn [hier](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/api/oas-specification/logging-verwerkingen-api/scopes.md) beschreven. Als de API call niet voldoet aan de scope dan zal een `HTTP 403 (Forbidden)` foutmelding worden teruggegeven.

## Gehanteerde standaarden
Op de verwerkingenlogging API-standaard zijn de volgende standaarden van toepassing:
- [De REST-API Design Rules (ADR)](https://forumstandaardisatie.nl/open-standaarden/rest-api-design-rules)
- [MIM - Metamodel Informatie Modellering v1.1](https://docs.geostandaarden.nl/mim/mim/)
