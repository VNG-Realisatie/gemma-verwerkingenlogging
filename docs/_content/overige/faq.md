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

#### Er wordt van de standaard een referentie implementatie beschikbaar gesteld. Wat houdt dat in?

De referentie implementatie is bedoeld als voorbeeld om te laten zien dat de API specificatie implementeerbaar is. Eventuele gedragsregels die niet in de OAS 3 specificatie staan kunnen dan ook gedemonstreerd worden. De referentie implementatie is geen productie waardige software. Het is een proof of concept, geen robuust geprogrammeerde component die direct uitgerold kan worden. Maar om een API implementatie te testen werkt het prima. Bovendien kunnen we door middel van de referentie-implementatie testscripts schrijven (Postman) zodat leveranciers kunnen testen of hun implementaties voldoen aan de standaard.

#### Is de referentie-implementatie bruikbaar in productie?

De referentieimplementatie is bedoeld voor het aantonen van de werking van de API-standaard en geschikt voor gebruik in een testomgeving. De referentieimplementatie is **niet** geschikt voor gebruik in een productie omgeving. De referentieimplementatie is hiervoor niet geschikt aangezien geen invulling is gegeven aan niet-functionele requirements zoals beschikbaarheid, performance, robuustheid etc. Ook is de ondersteuning vanuit VNG Realisatie tenaanzien van de referentieimplementatie niet ingericht op prodcutioneel gebruik.

#### Wanneer wordt een Release Candidate vastgesteld als Release?

Wanneer in de release candidate geen gebreken gevonden zijn en deze daarmee voldoende stabiel is wordt deze release candidate een release. De periode voor deze stabiliteit is vastgesteld op 2 maanden, ingaande vanaf de dag waarop de release candidate uitgebracht is. Onder gebreken wordt verstaan fouten in de standaard. Eventuele verbeteringen of verduidelijkingen in documentatie waarbij geen aanpassingen in de API's noodzakelijk zijn worden niet beschouwd als reden om een nieuwe release candidate uit te brengen.

#### Als een zoekopdracht wordt utgevoerd, wordt dit dan gezien als 'opvragen' en moet dit gelogd worden?

Hiervoor is een aantal cases beschreven. Deze zijn terug te vinden op Github:
[C3209 - Zoekvraag – Vooraf gedefinieerde zoekcriteria, vooraf gedefinieerde resultaatvelden](../achtergronddocumentatie/ontwerp/artefacten/3209)
[C5889 - Zoekvraag – Onbekende zoekcriteria, vooraf gedefinieerde resultaatvelden](../achtergronddocumentatie/ontwerp/artefacten/5889)
[C7293 - Zoekvraag – Onbekende zoekcriteria, onbekende resultaatvelden](../achtergronddocumentatie/ontwerp/artefacten/7293)

#### Hoe moet worden omgegaan met het attribuut 'gebruiker' als een consumer applicatie vanuit een geautomatiseerd proces een verwerking in de verwerkingenlogging gaat vastleggen?

Het attribuut moet de gebruiker identificeren binnen de context van het systeem. Het mag leeg gelaten worden indien de verwerking door het systeem wordt uitgevoerd. Mocht het systeem ook in dergelijke gevallen werken met ‘gebruikers’ dan mag de systeemgebruiker opgenomen worden.

Ziek ook https://vng-realisatie.github.io/gemma-verwerkingenlogging/gegevenswoordenboek/attributen/Gebruiker

#### Is er ook een mogelijk om niet via HTTP de standaard toe te passen en een ander communicatieprotocol te gebruiken?

De standaard is opgezet om te voorzien in communicatie tussen informatiesystemen via een RESTful API over HTTP. Andere protocollen voor communicatie tussen de systemen wordt nogg niet voorzien. 

#### Wordt voor het bepalen van de bewaartermijn de informatie uit de selectielijsten gebruikt?

Er is nog geen duidelijkheid over het bewaartermijn van de logging. Dit onderwerp wordt besproken met de Adviescommissie Archieven van de VNG. Zodra hierover duidelijk is, wordt dit opgenomen in de FAQ.

#### Elke organisatie kan een eigen selectielijst hanteren en daardoor andere bewaartermijnen hebben. Is dat een probleem als gegevens tussen organisaties worden uitgewisseld?

Nee, dat hoeft geen probleem te zijn. Zolang de vragende partij aangeeft wat het bewaartermijn is, kan de leverende partij dit ongewijzigd overnemen of een eigen bewaartermijn opnemen.

#### Moet je als leverende partij bijhouden aan welke consumers de gegevens zijn geleverd?

Het informatiesysteem moet zelf bijhouden uit welke informatiesystemen gegevens zijn opgehaald en aan welke informatiesystemen gegevens zijn geleverd. Dit is geen functionaliteit van de verwerkingenloggingcomponent.

#### Moeten integratie oplossingen (zoals bijvoorbeeld een ESB) ook logging vastleggen?

De standaard gaat er vanuit dat zowel een provider als een consumer zelf een logging registreren. Een integratieoplossing zoals een ESB wordt gezien als een transparant doorgeefluik. De ESB registeert dus geen logging in het kader van de AVG. Mogelijk dat er wel technische logging wordt vastgelegd, maar dat valt buiten de standaard.

#### Is er een strategie voor de migratie van systemen die aangeeft in welke volgorde en in welk termp zowel consumer applicaties als provider applicaties aangepast moeten of kunnen worden?

Nee, dat is nu nog niet voorhanden. Samen met gemeenten en leveranciers wordt gekeken wat het beste hierin kan worden gevolgd.

#### Kan het beschreven informatiemodel ook toegepast worden, zonder gebruik te maken van de RESTful API?

De gegevens moeten ontsloten worden via de RESTful API die gebaseerd is op het informatiemodel. De actie GET moet hierbij verplicht worden geïmplementeerd. Als de verwerkingenlogging niet als federatieve loggingcomponent aan andere consumers wordt aangeboden, hoeven de andere acties niet naar buiten toe worden opengesteld of geïmplementeerd.

#### Kan het gemeentelijke register van verwerkingsactiviteiten ook via bijvoorbeeld MijnOverheid ontsloten worden?

Ja, als het gemeentelijk register van verwerkingsactiviteiten via een URL te benaderen is, is deze in elke externe pagina op te nemen.

#### Kan het gemeentelijke verwerkingenloggingcomponent ook via bijvoorbeeld MijnOverheid ontsloten worden?

Het verwerkingenloggingregister kan alleen met de juiste authenticatie en autorisatie benaderd worden. Communicatie tussen MijnOverheid en een gemeentelijk register vraagt extra inspanningen van beide partijen. Voorlopig is daarin nog niet voorzien, maar mogelijk dat dit in de toekomst wel gerealiseerd kan worden.

#### Is bij het ontwikkelen van de standaard ook gekeken naar initiatieven die al in Nederland of Europa zijn gestart.

Er is gekeken naar kaders en richtlijnen zoals deze in de zorg worden toegepast. In Europa zijn wel initiatieven gestart, maar leveren nog geen concreet product op.

#### Is er een overzicht waar de wijzigingen ten opzichte van de vorige versie staan vermeld?

Op Github is opgenomen wanneer welke veranderingen zijn doorgevoerd. Zie hiervoor https://vng-realisatie.github.io/gemma-verwerkingenlogging/achtergronddocumentatie/voortgang
