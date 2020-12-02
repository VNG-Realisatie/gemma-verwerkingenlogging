---
name: aanvullendespecificatie-wijzigvertrouwelijkheidverwerking-post
title: Aanvullende specificaties voor POST /wijzigVertrouwelijkheidVerwerking
layout: default
---


### Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `update:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties bij te werken.


### Controles

| Regel | Foutcode |
| :---- | :---- |
| De functie mag alleen aangeroepen worden met autorisatiescope `update:confidential`. | 401 |


### Gedrag

De vertrouwelijkheid wordt bij alle acties die zijn gelogd in het kader van de meegegeven verwerking aangepast.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* Alle verwerkingsacties die horen bij de verwerking worden opgehaald.
* Zijn er van een verwerkingsactie meerdere voorkomens dan worden alle niet actuele voorkomens genegeerd.
* Zijn er vervallen voorkomens dan worden deze genegeerd.
* Maak voor ieder van de overgebleven verwerkingsacties een nieuwe logentry:
    * Het attribuut ID wordt gevuld met een nieuw UUID.
    * Het attribuut Tijdstip Registratie wordt gevuld met de actuele datum/tijd.
	* Het attribuut Vertrouwelijkheid wordt gevuld met de opgegeven waarde.
    * Alle overige attributen krijgen in houdelijk de waarden van de meeste actuele voorkomen dat gevonden werd.
