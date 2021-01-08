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
| Bij autorisatiescope `read:restricted` moet de zoekparameter beperkteSet 'true' zijn. | 403 |
| Bij autorisatiescope `read:normal` moet de zoekparameter vertrouwelijkheid 'Normal' zijn. | 403 |


### Gedrag

* Er worden alleen verwerkingsacties geretourneerd waarvan het tijdstip valt binnen de opgegeven periode: groter of gelijk aan `beginDatum`, kleiner dan de `eindDatum`.
* Er worden alleen verwerkingsacties geretourneerd waarbij het verwerkte object (bijvoorbeeld Persoon, BSN, 8273365) matched met de opgegeven waarden van de zoekparameters. In dit geval:
  - `objecttype = "Persoon"`,
  - `soortObjectId = "BSN"`,
  - `objectId = "8273365"`.
Bij deze verwerkingsacties worden de overige verwerkte objecten die niet voldoen niet geretourneerd. Ofwel: Als er bij een verwerkingsactie meerdere personen voorkomen, dan wordt alleen de persoon geretourneerd die matched met de zoekparameters.
* Indien de zoekparameter `verwerkingsactiviteitId` is opgegeven, dan worden alleen de verwerkingsacties die voldoen aan die waarde geretourneerd. 
* Indien de zoekparameter `vertrouwelijkheid` is opgegeven, dan worden alleen de verwerkingsacties die voldoen aan die waarde geretourneerd.
* De zoekparameter `vertrouwelijkheid__in` kan meerdere waarden van vertrouwelijkheid bevatten gescheiden door komma's. Als een verwerkingsactie niet voldoet aan één van deze waarden, dan mag de verwerkingsactie niet worden geretourneerd.
* Als de zoekparameter `beperkteSet=true` dan worden de volgende attributen **niet** geretourneerd: Systeem, Gebruiker en Gegevensbron. Is de parameter false dan mogen deze attributen wel geretourneerd worden.
* Als het log meerdere versies van een verwerkingsactie bevat dan worden alleen actuele niet vervallen versies geretourneerd. Zie [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) voor meer informatie over versies van verwerkingsacties.


