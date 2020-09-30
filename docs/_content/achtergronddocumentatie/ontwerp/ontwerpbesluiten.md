---
title: "Ontwerpbesluiten"
name: ontwerpbesluiten
date: '16-09-2020'
---

Vanuit de uitwerking van de [cases](./cases.md) en de [requirements](./requirements.md) zijn een aantal ontwerpbesluiten genomen. Per besluit is herleidbaar gemaakt aan welk requirement of case het requirement gerelateerd is. Een overzicht van de relatie tussen besluiten, cases en requirements is [hier](../../archief/work_in_progress.md) te vinden.

Deze ontwerpbesluiten zijn gegroepeerd naar specifieke aspect van de API-standaard. Onderkende aspecten zijn:
- fundamentele besluiten, 
- besluiten ten aanzien van scope van de API-standaard, 
- besluiten ten aanzien van de relatie met het register van verwerkingen, 
- besluiten ten aanzien van het gegevensmodel, en
- besluiten ten aanzien van tijd- en historie.

Per aspect kunnen ook aanbevelingen gelden. De aanbevelingen zijn op de [aanbevelingen pagina](./aanbevelingen.md) na te lezen.

## Fundamenteel
- [B5469: Doelstelling van logging: Duiden versus reconstrueren](./artefacten/5469.md)
- [B7952: Loggen vanuit applicatie: Welke momenten en hoe vaak](./artefacten/7952.md)
- [B7259: Loggen aan beide kanten van een API](./artefacten/7259.md)
- [B9177: Meegeven van informatie t.b.v. logging in API’s](./artefacten/9177.md)
- [B3238: Logging-API: Alleen identificatoren of ook achterliggende waarden?](./artefacten/3238.md)
- [B8970: Benadering log bij gefedereerde inrichting](./artefacten/8970.md)

## Scope
- B0538: Logging beperkt tot verwerkingen
- B4421: Logging beperkt tot geautomatiseerde verwerkingen
- B5214: Inzage log beperkt tot gemeentelijk log
- B0403: Standaardisatie leesbaar logformaat
- B3001: Vastlegging toestemming van een persoon
- B0797: Standaardisatie rapportages

## Relatie tot het VAR
- B0869: Koppeling tussen applicaties en VAR
- B8278: Beëindigen van de geldigheid van verwerkingsactiviteiten

## Gegevensmodel logging
- B9428: Terminologie: Gebruiker of Medewerker
- B0601: Terminologie: Handeling of Gebeurtenis
- B4047: Terminologie: Actie of Operatie
- B6856: Hiërarchie: Verwerkingsactiviteit, Verwerking, Handeling en Actie
- B2357: Kunstmatige identificatoren
- B0516: Identificatie van organisaties
- B7972: Identificatie van personen bij privaatrechtelijke taken
- B2042: Pseudonimisering BSN
- A7838: Standaardwaarden voor Actie
- B7571: Meerdere personen/objecten per verwerking
- B8157: Modellering van Verwerkt soort gegeven
- B9330: Opname van Afnemer
- B1598: Opname van Betrokkenheid
- B9559: Opname van Bewaartermijn
- B9207: Opname van Gebruiker
- B8585: Opname van Gegevensbron
- [B6872: Opname van Handeling](./artefacten/6872.md)
- B7726: Opname van Resultaat verwerking
- B3133: Opname van Rol van de gebruiker
- B0378: Opname van Systeem
- B2017: Opname van Tijdstip verwerking
- B7191: Opname van Uitvoerder
- B3908: Opname van Vertrouwelijkheid
- B6247: Opname van Verwerkt soort gegeven
- B0233: Opname zoekcriteria op in het log

## Wijzigen, tijd en historie
- B3891: Wijzigbaarheid en historie
- B3707: Opname van Tijdstip Registratie
- B8641: Opname van Vervallen
- B8157: Opname van Referentie

