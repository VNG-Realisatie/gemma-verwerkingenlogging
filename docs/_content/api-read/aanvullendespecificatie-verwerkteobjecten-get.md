---
name: aanvullendespecificatie-verwerkteobjecten-get
title: Aanvullende specificaties voor GET /verwerkte-objecten
layout: default
---

### Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `read:normal` | Laat toe om een beperkte set van attributen van verwerkingsacties die betrekking hebben op een specifiek verwerkt object te lezen die niet vertrouwelijk zijn. 
| `read:confidential` | Laat toe om een beperkte set van attributen van verwerkingsacties die betrekking hebben op een specifiek verwerkt object te lezen die niet vertrouwelijk zijn of waarvan de vertrouwelijkheid van is opgeheven. 

### Gedrag

* Er worden alleen verwerkte objecten geretourneerd waarvan het tijdstip van de verwerkingsactie valt binnen de opgegeven periode: groter of gelijk aan `beginDatum`, kleiner dan de `eindDatum`.
* Verwerkte objecten worden gefilterd op basis van query parameters `objecttype`, `soortObjectId` en `objectId`. Voorbeeld: we zoeken naar de verwerkte objecten met betrekking tot de persoon met (fictief) BSN 8273365. Dit is een GET operatie met de volgende query parameters:
  - `objecttype=Persoon`,
  - `soortObjectId=BSN`,
  - `objectId=8273365`. 

Alleen verwerkingsacties waarbij een gekoppeld verwerkt object matched met de opgegeven waarden van deze query parameters worden gerourneerd. 
* Indien de zoekparameter `verwerkingsactiviteitId` is opgegeven, dan worden alleen de verwerkte objecten geretourneerd waarvan de gekoppelde verwerkingsactie voldoet aan die waarde . 
* De volgende elementen worden **niet** geretourneerd: `systeem`, `gebruiker` en `gegevensbron`. 
* Verwerkte objecten worden alleen geretourneerd als de gekoppelde verwerkingsactie actueel en niet vervallen versies is. Zie [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) voor meer informatie over versies van verwerkingsacties.

## Verplichting opname header 
Als een consumer de GET /verwerkte-objecten aanroept moet deze bij deze aanroep in de header de volgende informatie meegegeven worden ([B9177](../achtergronddocumentatie/ontwerp/artefacten/9177.md)).

<img src="./_assets/api_1.png" alt="" width="700"/>

De provider van de GET /verwerkte-objecten dient de bevraging van het log te loggen. De provider neemt de informatie uit de header als volgt over:

<img src="./_assets/api_2.png" alt="" width="700"/>
