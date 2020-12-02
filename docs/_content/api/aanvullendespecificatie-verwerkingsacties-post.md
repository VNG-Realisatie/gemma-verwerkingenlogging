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
| Bij autorisatiescope `create:normal` moet de parameter Vertrouwlijkheid 'Normaal' zijn. | 401 |
| Bij autorisatiescope `create:confidential` mag de parameter Vertrouwlijkheid 'Normaal' of 'Vertrouwelijk' zijn. | 401 |
| De parameter Vertrouwlijkheid mag nooit de waarde 'Opgeheven' hebben. | 401 |


### Gedrag

* Het attribuut ID wordt gevuld met een nieuw UUID.
* Het attribuut Tijdstip Registratie wordt gevuld met de actuele datum/tijd.
* Het attribuut Vervallen krijgt de waarde 'False'.
