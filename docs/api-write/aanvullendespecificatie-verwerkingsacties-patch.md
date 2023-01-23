---
layout: page-with-side-nav
title: Aanvullende specificaties voor PATCH /verwerkingsacties
date: 28-03-2022
---

# Aanvullende specificaties voor PATCH /verwerkingsacties

## Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `update:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties bij te werken. 
| `update:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties bij te werken.

## Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `update:normal` moet de vertrouwelijkheid van de oorspronkelijke verwerkingsactie 'Normaal' zijn en mag alleen het element `bewaartermijn` gewijzigd worden. | 403 |
| Bij autorisatiescope `update:confidential` mogen zowel het element `bewaartermijn` als `vertrouwelijk` gewijzigd worden. | 403 |

## Gedrag

* Alle verwerkingsacties met de opgegeven query parameter `verwerkingId` worden met de opgegeven `bewaartermijn` of/en `vertrouwelijkheid` aangepast.
* Als de `verwerkingId` niet gematcht kan worden met een verwerkingsactie of de gevonden verwerkingsactie blijkt te zijn vervallen, dan wordt een `HTTP 400` foutmelding teruggestuurd.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* Alle verwerkingsacties die horen bij de verwerking worden opgehaald.
* Zijn er van een verwerkingsactie meerdere voorkomens dan worden alle niet actuele voorkomens genegeerd.
* Zijn er vervallen voorkomens dan worden deze genegeerd.
* Maak voor ieder van de overgebleven verwerkingsacties een nieuwe logentry:
    * Het attribuut `Actie ID` wordt gevuld met een nieuw UUID.
    * Het attribuut `Tijdstip Registratie` wordt gevuld met de actuele datum/tijd.
	* Het attribuut `Vertrouwelijkheid` wordt gevuld met de opgegeven waarde.
    * Alle overige attributen krijgen inhoudelijk de waarden van het meeste actuele voorkomen dat gevonden werd.
