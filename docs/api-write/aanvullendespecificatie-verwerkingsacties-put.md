---
layout: page-with-side-nav
title: Aanvullende specificaties voor PUT /verwerkingsacties
date: 28-03-2022
---

# Aanvullende specificaties voor PUT /verwerkingsacties

## Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `update:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties bij te werken. 
| `update:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties bij te werken.


## Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `update:normal` moet de oorspronkelijke verwerkingsactie 'Normaal' zijn en mag deze waarde niet worden gewijzigd. | 403 |
| Bij autorisatiescope `update:confidential` mag de vertrouwelijkheid worden gewijzigd in 'Normaal' of 'Vertrouwelijk' maar niet in `Opgeheven`. | 403 |


## Gedrag

* Alle gegevens van de verwerkingsactie moeten opnieuw worden meegegeven, ook de gegevens die niet wijzigen. Dat betekent dat alle elementen van de verwerkingsactie verplicht in het request bericht moeten worden opgenomen.<sup>[1](#Voetnoot1)</sup> Als dit niet het geval is, dan wordt er een HTTP 400 (Bad Request) foutmelding teruggegeven. 
* De gegevens van de bestaande verwerkingsactie, geïdentificeerd met behulp van de path parameter `actieId`, worden overschreven met de gegevens in de body van de request.
* Als de `actieId` niet gematcht kan worden met een verwerkingsactie of de gevonden verwerkingsactie blijkt te zijn vervallen, dan wordt een HTTP 400 foutmelding teruggestuurd.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* De verwerkingsactie die hoort bij de opgegeven path parameter `actieId` wordt opgehaald.
* Zijn er van de verwerkingsactie meerdere voorkomens dan worden alle niet actuele voorkomens genegeerd.
* Is het meest actuele voorkomen vervallen, dan retourneert de functie een foutmelding (HTTP 400).
* Is het meest actuele voorkomen niet vervallen, dan wordt een nieuwe logentry aangemaakt.
    * Het attribuut `Actie ID` wordt gevuld met een nieuw UUID.
    * Het attribuut `Tijdstip Registratie` wordt gevuld met de actuele datum/tijd.
    * Het attribuut `Vervallen` krijgt de waarde `False`.
    * Alle overige attributen krijgen inhoudelijk de waarden die in het request bericht zijn meegegeven.

## Voetnoten
<a name="Voetnoot1"> 1</a>
Let op: in de OAS wordt dit niet afgedwongen, vandaar deze aanvullende specificatie. Het verplicht zijn van deze velden is namelijk situatie-specifiek en dan zou je per situatie een schema moeten specificeren. In OAS is dat niet praktisch omdat je daar niet hetzelfde schema kunt hergebruiken voor alle situatie.
