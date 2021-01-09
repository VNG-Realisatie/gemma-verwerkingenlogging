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
| Bij autorisatiescope `create:normal` moet het element `vertrouwelijkheid` gevuld zijn met de waarde "Normaal". | 403 |
| Bij autorisatiescope `create:confidential` moet het element `vertrouwelijkheid` gevuld zijn met de waarde "Normaal" of de waarde "Vertrouwelijk". | 403 |
| Het element `vertrouwelijkheid` mag nooit de waarde "Opgeheven" hebben. | 403 |


### Gedrag

* In de respons is het element `url` gevuld met een URL-referentie naar de aangemaakte verwerkingsactie.
* In de respons is het element `actieId` gevuld met een nieuwe UUID.
* In de respons is het element `tijdstipRegistratie` gevuld met de actuele datum/tijd.
* In de respons zijn alle overige elementen gevuld met dezelfde waarden die in de request zijn meegegeven.
