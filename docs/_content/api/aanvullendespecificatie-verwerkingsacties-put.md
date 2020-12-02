---
name: aanvullendespecificatie-verwerkingsacties-put
title: Aanvullende specificaties voor PUT /verwerkingsacties
layout: default
---

### Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `update:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties bij te werken. 
| `update:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties bij te werken.


### Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `update:normal` moet de parameter Vertrouwlijkheid 'Normaal' zijn en moet ook de vertrouwelijkheid van de oorspronkelijke verwerkingsactie 'Normaal' zijn. | 401 |
| Bij autorisatiescope `update:confidential` mag de parameter Vertrouwlijkheid 'Normaal' of 'Vertrouwelijk' zijn. | 401 |
| De parameter Vertrouwlijkheid mag nooit de waarde 'Opgeheven' hebben. | 401 |


### Gedrag

De gegevens van de bestaande verwerkingsactie, geïdentificeerd met behulp van het Actie ID, worden overschreven met de opgegeven gegevens.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* De verwerkingsactie die hoort bij het opgegeven Actie ID wordt opgehaald.
* Zijn er van de verwerkingsactie meerdere voorkomens dan worden alle niet actuele voorkomens genegeerd.
* Is het meest actuele voorkomen vervallen dan retourneert de functie een foutmelding.
* Is het meest actuele voorkomen niet vervallen dan wordt een nieuwe logentry aangemaakt.
    * Het attribuut ID wordt gevuld met een nieuw UUID.
    * Het attribuut Tijdstip Registratie wordt gevuld met de actuele datum/tijd.
    * Het attribuut Vervallen krijgt de waarde 'False'.
    * Alle overige attributen krijgen in houdelijk de waarden die aan de functie zijn meegegeven.

