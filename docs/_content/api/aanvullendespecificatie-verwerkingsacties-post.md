---
name: aanvullendespecificatie-verwerkingsacties-post
title: Aanvullende specificaties voor POST /verwerkingsacties
layout: default
---

### Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `create:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties aan te maken. |
| `create:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties aan te maken. |

### Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `create:normal` moet in de request het element `vertrouwelijkheid` gevuld zijn met de waarde `Normaal`. | 403 |
| Bij autorisatiescope `create:confidential` moet in de request het element `vertrouwelijkheid` gevuld zijn met de waarde `Normaal` of `Vertrouwelijk`. | 403 |
| Het element `vertrouwelijkheid` mag nooit de waarde `Opgeheven` hebben. | 403 | <!-- we kunnen dit ook afdwingen in de OAS, maar dat wordt het schema niet mooier van -->

### Gedrag
Voor het responsbericht gelden de volgende regels:
* Het element `url` is gevuld met een URL-referentie naar de aangemaakte verwerkingsactie.
* Het element `actieId` is gevuld met een nieuwe UUID.
* Het element `tijdstipRegistratie` is gevuld met de actuele datum/tijd.
* Alle overige elementen zijn gevuld met dezelfde waarden die in de request zijn meegegeven. Optionele elementen die niet zijn meegegeven in de request worden wel teruggegeven in de respons, maar dan met lege waarden.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden op de achterliggende database:
* Er wordt een nieuw `Verwerkingsactie` record aangemaakt met attributen zoals beschreven in het SIM/UGM.
* Het attribuut `Actie ID` krijgt een nieuwe UUID.
* Het attribuut `Tijdstip Registratie` krijgt de actuele datum/tijd.
* Het attribuut `Vervallen` krijgt de waarde `Ja`.
* Alle overige attributen van het record krijgen de waarden van de corresponderende elementen die in het request bericht zijn meegegeven.
