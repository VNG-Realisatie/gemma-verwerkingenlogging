---
title: "Veelgestelde vragen"
date: '10-10-2020'
weight: 40
---


### Algemeen

#### Wie is de opdrachtgever?

Formeel opdrachtgever is de Unit Manager Veiligheid, Architectuur en Standaarden van VNG Realisatie. Beheer van de standaard wordt uitgevoerd door de afdeling Veiligheid, Architectuur en Standaarden van VNG Realisatie.

#### Wat is de opdracht?

Het ontwikkelen van een API-standaard inclusief referentie implementatie voor de vastlegging en ontsluiting van de verwerking van (persoons)gegevens. De API-standaard moet aan een aantal eisen voldoen:

- implementeerbaar binnen de huidige gemeentelijke informatiesystemen en nieuwe op Common Ground gebaseerde informatiesystemen.
- conformeren aan de [landelijke API-strategie](https://docs.geostandaarden.nl/api/API-Strategie/)
- conformeren aan GEMMA Gegevenslandschap architectuur

#### Wat gaat er concreet gemaakt worden?

Als onderdeel van de API-standaard worden de volgende zaken opgeleverd:

* Verwerkingenlogging API's volgens Open API Specificatie v3 (AOS 3)
* open source referentie-implementatie van een loggingregister
* open source referentie-implementatie van applicatie die verwerkingen logt.
* Functionele en architectuurdocumentatie voor het gebruik van de API.

#### Wat betekent dit voor leveranciers?

Er komt een nieuwe API-standaard. Deze standaard dient door alle leveranciers die informatiesystemen aan gemeenten leveren waarin persoonsgegevens worden verwerkt moeten worden ingebouwd. De referentie implementaties bieden leveranciers een voorbeeld hoe deze standaard ingebouwd kan worden.

#### Wat is de rol van VNG?

* Ontwikkelaar en beheerder van de API-standaard
* Communicatie naar, en afstemming met gemeenten en leveranciers
* Toetsen aan en aanpassen van de GEMMA architectuur
* Afstemming met Common Ground
* Kwaliteitsbewaking

#### Is de referentie-implementatie bruikbaar in productie?

De referentieimplementatie is bedoeld voor het aantonen van de werking van de API-standaard en geschikt voor gebruik in een testomgeving. De referentieimplementatie is **niet** geschikt voor gebruik in een productie omgeving. De referentieimplementatie is hiervoor niet geschikt aangezien geen invulling is gegeven aan niet-functionele requirements zoals beschikbaarheid, performance, robuustheid etc. Ook is de ondersteuning vanuit VNG Realisatie tenaanzien van de referentieimplementatie niet ingericht op prodcutioneel gebruik.

#### Wanneer wordt een Release Candidate vastgesteld als Release?

Wanneer in de release candidate geen gebreken gevonden zijn en deze daarmee voldoende stabiel is wordt deze release candidate een release. De periode voor deze stabiliteit is vastgesteld op 2 maanden, ingaande vanaf de dag waarop de release candidate uitgebracht is. Onder gebreken wordt verstaan fouten in de standaard. Eventuele verbeteringen of verduidelijkingen in documentatie waarbij geen aanpassingen in de API's noodzakelijk zijn worden niet beschouwd als reden om een nieuwe release candidate uit te brengen.
