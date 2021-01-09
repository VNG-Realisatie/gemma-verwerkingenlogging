---
name: aanvullendespecificatie-verwerkingsacties-delete
title: Aanvullende specificaties voor DELETE /verwerkingsacties
layout: default
---


### Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `delete:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties te verwijderen. 
| `delete:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties te verwijderen.


### Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `delete:normal` moet de vertrouwelijkheid van de oorspronkelijke verwerkingsactie 'Normaal' zijn. | 403 |


### Gedrag

De opgegeven verwerkingsactie, geïdentificeerd met behulp van het Actie ID, wordt logisch verwijderd.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* De verwerkingsactie die hoort bij het opgegeven Actie ID wordt opgehaald.
* Zijn er van de actie meerdere voorkomens dan worden alle niet actuele voorkomens genegeerd.
* Is het meest actuele voorkomen vervallen dan retourneert de functie een foutmelding.
* Is het meest actuele voorkomen niet vervallen dan wordt een nieuwe logentry aangemaakt.
    * Het attribuut `ID` wordt gevuld met een nieuw UUID.
    * Het attribuut 'Tijdstip Registratie' wordt gevuld met de actuele datum/tijd.
    * Het attribuut 'Vervallen' krijgt de waarde True.
    * Alle overige attributen krijgen in houdelijk de waarden van de meeste actuele voorkomen dat gevonden werd.

