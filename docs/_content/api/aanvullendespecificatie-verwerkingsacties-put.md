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
| Bij autorisatiescope `update:normal` moet de parameter Vertrouwlijkheid 'Normaal' zijn en moet ook de vertrouwelijkheid van de oorspronkelijke verwerkingsactie 'Normaal' zijn. | 403 |
| Bij autorisatiescope `update:confidential` mag de parameter Vertrouwlijkheid 'Normaal' of 'Vertrouwelijk' zijn. | 403 |
| De parameter Vertrouwlijkheid mag nooit de waarde 'Opgeheven' hebben. | 403 |


### Gedrag

* Alle gegevens van de verwerkingsactie moeten opnieuw worden meegegeven, ook de gegevens die niet wijzigen. Dat betekent dat alle elementen van de verwerkingsactie verplicht in het requestbericht moeten worden opgenomen.<sup>[1](#Voetnoot1)</sup> Als dit niet het geval is, dan wordt er een HTTP 400 (Bad Request) foutmelding teruggegeven. 

* De gegevens van de bestaande verwerkingsactie, geïdentificeerd met behulp van de path parameter `uuid`, worden overschreven met de gegevens in de body van de request.

* Als de `uuid` niet gematched kan worden met een verwerkingsactie of de gevonden verwerkingsactie blijkt te zijn vervallen, dan wordt een HTTP 400 foutmelding teruggestuurd.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden:
* De verwerkingsactie die hoort bij de opgegeven path parameter `uuid` wordt opgehaald.
* Zijn er van de verwerkingsactie meerdere voorkomens dan worden alle niet actuele voorkomens genegeerd.
* Is het meest actuele voorkomen vervallen, dan retourneert de functie een foutmelding (HTTP 400).
* Is het meest actuele voorkomen niet vervallen, dan wordt een nieuwe logentry aangemaakt.
    * Het attribuut `Actie ID` wordt gevuld met een nieuw UUID.
    * Het attribuut `Tijdstip Registratie` wordt gevuld met de actuele datum/tijd.
    * Het attribuut `Vervallen` krijgt de waarde `False`.
    * Alle overige attributen krijgen inhoudelijk de waarden die in het request bericht zijn meegegeven.

### Voetnoten
<a name="Voetnoot1"> 1</a>
**Let op:** in de OAS wordt dit niet afgedwongen, vandaar deze aanvullende specificatie. Het verplicht zijn van deze velden is situatie-specifiek en dan zou je per situatie een schema moeten specificeren. In OAS is dat niet practisch omdat je dan niet hetzelfde schema kunt hergebruiken voor alle situaties.
