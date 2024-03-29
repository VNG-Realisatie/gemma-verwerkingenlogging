---
layout: page-with-side-nav
title: Aanvullende specificaties voor GET /verwerkingsacties
date: 28-03-2022
---

# Aanvullende specificaties voor GET /verwerkingsacties

## Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `read:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties te lezen.
| `read:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties te lezen.     

## Controles

| Regel | Foutcode |
| :---- | :---- |
| Bij autorisatiescope `read:normal` moet de query parameter `vertrouwelijkheid` ingevuld zijn met de waarde `Normaal`. | 403 |


## Gedrag
* Er worden alleen verwerkingsacties geretourneerd waarvan het tijdstip valt binnen de opgegeven periode: groter of gelijk aan `beginDatum`, kleiner dan de `eindDatum`.
* Bij het gebruik van de query parameters `objecttype`, `soortObjectId` en `objectId` worden zowel de verwerkingsacties als de verwerkte objecten die in deze verwerkingsacties zijn opgenomen gefilterd. Alleen de verwerkingsacties  waarbij een verwerkt object matcht met de opgegeven waarden van deze query parameters worden geretourneerd. Voorbeeld: we zoeken naar de verwerkingsacties met betrekking tot de persoon met BSN 8273365. Dit is een GET operatie met de volgende query parameters:
  - `objecttype=Persoon`,
  - `soortObjectId=BSN`,
  - `objectId=8273365`. 

* Indien de zoekparameter `verwerkingsactiviteitId` is opgegeven, dan worden alleen de verwerkingsacties die voldoen aan die waarde geretourneerd. 
* Indien de zoekparameter `vertrouwelijkheid` is opgegeven, dan worden alleen de verwerkingsacties die voldoen aan die waarde geretourneerd.
* De zoekparameter `vertrouwelijkheid__in` kan meerdere waarden van vertrouwelijkheid bevatten gescheiden door komma's. De verwerkingsacties die worden geretourneerd moeten voldoen aan één van deze waarden.
* Als het log meerdere versies van een verwerkingsactie bevat dan worden alleen actuele niet vervallen versies geretourneerd. Zie [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) voor meer informatie over versies van verwerkingsacties.
