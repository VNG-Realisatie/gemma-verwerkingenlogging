---
name: aanvullendespecificatie-verwerkingsacties-get
title: Aanvullende specificaties voor GET /verwerkingsacties
layout: default
---

### Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `read:restricted` | Laat toe om een beperkte set van attributen van niet vertrouwelijke (normale) verwerkingsacties te lezen.
| `read:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties te lezen.
| `read:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties te lezen.     

### Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `read:restricted` moet de parameter beperkteSet 'False' zijn. | 403 |
| Bij autorisatiescope `read:normal` moet de parameter vertrouwelijkheid 'Normal' zijn. | 403 |


### Gedrag

* Er worden alleen verwerkingsacties geretourneerd waarvan Tijdstip valt binnen de opgegeven periode. (Groter of gelijk aan begindatum, kleiner dan de einddatum).
* Er worden alleen verwerkingsacties geretourneerd waarbij een Verwerkt Object voorkomt waarvan Objecttype, Soort Object ID en Object ID (bijvoorbeeld Persoon, BSN, 8273365) matchen met de opgegeven waarden in de overeenkomstige zoekparameters. Bij deze verwerkingsacties worden de overige verwerkte objecten die niet voldoen niet geretourneerd. Ofwel: Als er bij een verwerkingsacties meerdere personen voorkomen, dan wordt alleen de persoon geretourneerd die is opgegeven in de zoekparameter.
* Indien een verwerkingsactiviteitID is opgegeven als zoekparameter worden er alleen verwerkingsacties geretourneerd waarvan de VerwerkingsactiviteitID gelijk is aan het opgegeven VerwerkingsactiviteitID.
* Er worden alleen verwerkingsacties geretourneerd waarbij de waarde van het attribuut Vertrouwelijkheid overeenkomt met de waarde van de parameter vertrouwelijkheid.
* Als de parameter beperkteSet = true dan worden de volgende attributen **niet** geretourneerd: Systeem, Gebruiker en Gegevensbron. Is de parameter false dan mogen deze attributen wel geretourneerd worden.
* Als het log meerdere versies van een verwerkingsactie bevat dan worden alleen actuele niet vervallen versies geretourneerd. Zie [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) voor meer informatie over versies van verwerkingsacties.


