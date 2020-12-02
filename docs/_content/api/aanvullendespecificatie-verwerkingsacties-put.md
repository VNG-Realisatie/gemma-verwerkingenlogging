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
| Bij autorisatiescope `update:normal` moet de verwerkingsactie voor het wijzigen de vertrouwlijkheid 'Normaal' hebben. Verwerkingsacties met vertrouwelijkheid 'Vertrouwelijk' of 'Opgeheven' mogen niet via autorisatiescope `update:normal' aangepast worden. | 401 |


### Gedrag

De gegevens van de bestaande verwerkingsactie, geïdentificeerd met behulp van het Actie ID, worden overschreven met de opgegeven gegevens.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* De verwerkingsactie die hoort bij het opgegeven Actie ID wordt opgehaald.
* Zijn er van de verwerkingsactie meerdere voorkomens dan worden alle niet actuele voorkomens genegeerd.
* Is het meest actuele voorkomen vervallen dan retourneert de functie een foutmelding.
* Is het meest actuele voorkomen niet vervallen dan wordt een nieuwe logentry aangemaakt.
 * Deze logentry krijgt inhoudelijk de waarden die aan de functie zijn meegegeven.
 * Het attribuut Vertrouwelijkheid wordt gevuld met de waarde ‘Normaal’.
 * Het attribuut Tijdstip Registratie wordt gevuld met de actuele datum/tijd.
 * Het attribuut Vervallen krijgt de waarde ‘Ja’.
