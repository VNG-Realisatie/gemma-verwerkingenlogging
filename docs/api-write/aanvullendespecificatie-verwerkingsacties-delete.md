---
layout: page-with-side-nav
title: Aanvullende specificaties voor DELETE /verwerkingsacties
date: 28-03-2022
---

# Aanvullende specificaties voor DELETE /verwerkingsacties

## Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `delete:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties te verwijderen. 
| `delete:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties te verwijderen.


## Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `delete:normal` moet de vertrouwelijkheid van de te verwijderen verwerkingsactie `Normaal` zijn. | 403 |


## Gedrag

De opgegeven verwerkingsactie, geïdentificeerd met behulp van de path parameter `actieId`, wordt **niet fysiek** maar **logisch** verwijderd.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast. 

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* De verwerkingsactie die hoort bij de opgegeven path parameter `actieId` wordt opgehaald door deze te matchen op het attribuut `Actie ID` van de verwerkingsacties. Indien de verwerkingsactie niet wordt gevonden, dan wordt er een status 400 foutmelding teruggegeven (bad request).
* Zijn er van de verwerkingsactie meerdere voorkomens, dan worden alle niet actuele voorkomens genegeerd.
* Is het meest actuele voorkomen vervallen, dan retourneert de delete operatie een status 400 foutmelding.
* Is het meest actuele voorkomen niet vervallen, dan wordt er een nieuwe logentry aangemaakt.
    * Het attribuut `Actie ID` wordt gevuld met een nieuwe UUID.
    * Het attribuut `Tijdstip Registratie` wordt gevuld met de actuele datum/tijd.
    * Het attribuut `Vervallen` krijgt de waarde `True`.
    * Alle overige attributen krijgen inhoudelijk de waarden van het meeste actuele voorkomen dat gevonden werd.
