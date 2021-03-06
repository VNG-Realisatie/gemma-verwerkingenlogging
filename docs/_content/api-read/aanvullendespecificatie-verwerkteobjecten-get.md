---
name: aanvullendespecificatie-verwerkteobjecten-get
title: Aanvullende specificaties voor GET /verwerkteObjecten
layout: default
---

### Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `read:normal` | Laat toe om een beperkte set van attributen van niet vertrouwelijke (normale) verwerkingsacties te lezen. 

### Controles

| Regel | Foutcode |
| :---- | :---- |
|  |  |


### Gedrag

* Er worden alleen verwerkingsacties geretourneerd waarvan het tijdstip valt binnen de opgegeven periode: groter of gelijk aan `beginDatum`, kleiner dan de `eindDatum`.
* Bij het gebruik van de query parameters `objecttype`, `soortObjectId` en `objectId` worden zowel de verwerkingsacties als de verwerkte objecten die in deze verwerkingsacties zijn opgenomen gefilterd. Voorbeeld: we zoeken naar de verwerkingsacties met betrekking tot de persoon met BSN 8273365. Dit is een GET operatie met de volgende query parameters:
  - `objecttype=Persoon`,
  - `soortObjectId=BSN`,
  - `objectId=8273365`. 

Ten eerste worden alleen de verwerkingsacties geretourneerd waarbij het verwerkte object matched met de opgegeven waarden van deze query parameters. Ten tweede worden binnen deze verwerkingsacties de overige verwerkte objecten die niet voldoen aan de de  zoekopdracht niet geretourneerd. Oftewel: Als er bij een verwerkingsactie meerdere personen voorkomen, dan wordt in het kader van de privacy alleen de verwerkte objecten geretourneerd waarbij de gezochte persoon betrokken is.
* Indien de zoekparameter `verwerkingsactiviteitId` is opgegeven, dan worden alleen de verwerkingsacties die voldoen aan die waarde geretourneerd. 
* Indien de zoekparameter `vertrouwelijkheid` is opgegeven, dan worden alleen de verwerkingsacties die voldoen aan die waarde geretourneerd.
* De zoekparameter `vertrouwelijkheid__in` kan meerdere waarden van vertrouwelijkheid bevatten gescheiden door komma's. De verwerkingsacties die worden geretourneerd moeten voldoen aan één van deze waarden.
* De volgende elementen worden **niet** geretourneerd: `systeem`, `gebruiker` en `gegevensbron`. 
* Als het log meerdere versies van een verwerkingsactie bevat dan worden alleen actuele niet vervallen versies geretourneerd. Zie [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) voor meer informatie over versies van verwerkingsacties.
