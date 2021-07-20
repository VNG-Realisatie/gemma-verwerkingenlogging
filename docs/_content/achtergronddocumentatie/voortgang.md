---
title: "Voortgang ontwikkeling API-standaard voor logging van verwerkingen"
name: Voortgang ontwikkeling API-standaard voor logging van verwerkingen
---

## 21 juli 2021
* De Verwerkingenlogging API-standaard is opgedeeld in twee verschillende APIs. Een API voor de bewerking van verwerkingen en een API voor de opvraging van verwerkte objecten. De API voor bewerkingen wordt gebruikt door procesapplicaties die verwerkingen van (persoons)gegevens vastleggen. De inzage API wordt gebruikt voor het opvraghen van verwerkingsacties voor specifieke verwerkte objecten. De inzage API is met name bedoeld voor informatiesystemen die inzage aan betrokkenen geven over verwerkingen van hun gegevens die plaats hebben gevonden. Een voorbeeld van een dergelijk systeem is een MijnGemeente systeem die na inlog van de burger met DigiD de verwerkingen weergeeft.
* De API voor het bewerken van verwerkingen is [hier](../api-write/index.md) te vinden.
* De API voor het inzien van verwerkingen is [hier](../api-read/index.md) te vinden.

## 11 mei 2021
* De referentieimplementatie van het providerdeel van de API-standaard is gerealiseerd. De referentieimplementatie is te downloaden van [Gitlab](https://gitlab.com/commonground/referentie-apis/verwerkingenlogging) en kan via een Docker installatie lokaal worden geinstalleerd. Instructies voor de installatie van de referentieimplementatie zijn te vinden op de [documentatie website.](https://commonground.gitlab.io/referentie-apis/verwerkingenlogging/index.html)  

## 14 april 2021
* Naar aanleiding van terugkoppeling die het project heeft ontvangen van fouten in het yaml-bestand zijn aanpassingen aan deze definitie gemaakt. Deze wijzigingen leiden tot breaking changes ten aanzien van de versie in de 1.0.0 RC1 release. Om deze reden is besloten een nieuwe release candidate aan te maken (1.0.0 RC2). Wijzigingen die aangebracht zijn hebben onder andere te maken met foutieve lengtes van een aantal velden, wijziging van de manier van doorgeven van het `vertrouwelijkheid` attribuut, het ontbreken van de foutcode 400 (Bad Request) in de GET van `verwerkingacties` en incorrect gebruik van `minLength` bij het attribuut `verwerkingsactiviteitUrl`. Daarnaast is overbodig commentaar uit het yaml-bestand verwijderd.

## 25 maart 2021
* De FAQ is aangevuld naar aanleiding van de Bijeenkomst API-standaard voor logging van verwerkingen. 

## 6 maart 2021
* De RPC calls voor het wijzigen van de Bewaartermijn en Vertrouwelijkheid van verwerkingsacties zijn omgezet naar een PATCH operatie conform REST.

## 27 januari 2021
* In [C3677: Inzage door burger](./ontwerp/artefacten/3677.md) is een passage toegevoegd over de noodzaak om ook de inzage van het verwerkingenlog te loggen. Ook in de quickstart guide is toegevoegd dat dit moet en wordt naar deze casus verwezen.
* In de quickstart guide en op de pagina van de opvragingscases wordt nu verwezen naar [C2866 - Detailvraag op basis van BSN – Door een derde partij](./ontwerp/artefacten/2866.md) en naar [C0031 - Opvragen van gegevens bij een derde partij](./ontwerp/artefacten/0031.md) omdat deze cases voorzien zijn van een aanvullende toelichting die laat zien hoe de gegevens van de afnemer via de http-header in het log van de aanbieder terechtkomen:

## 14 januari 2021
* Op diverse pagina's de tekst 'html header' gewijzigd naar 'http header'.

## 8 januari 2021
* Architectuurschets bij case [C2866 - Detailvraag op basis van BSN – Door een derde partij](./ontwerp/artefacten/2866.md) toegevoegd.

## 7 januari 2021
* Aanbeveling toegevoegd inzake [gebruik van de autorisatie API uit het ZGW project](./ontwerp/artefacten/9726.md).

## 6 januari 2021
* Kleine verbeteringen aan navigatie binnen de site. Sitemap is weggehaald en voor zover relevant geintegreerd in de pagina over de achtergrond documentatie.
* Casus toegevoegd ivm [handmatige verwerking van gegevens](./ontwerp/artefacten/5672.md).

## 18 december 2020
* Architectuurschets bij case [C0031 - Opvragen van gegevens bij een derde partij](./ontwerp/artefacten/0031.md) toegevoegd.

## 17 december 2020
* [Architectuurschetsen](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/architectuur/index.md) van inrichtingsscenario's toegevoegd. Deze schetsen geven inzicht in de verschillende mogelijkheden die gemeenten hebben bij de inrichting van de informatiesystemen die een rol spelen bij logging van verwerkingsactiviteiten en het ontsluiten van die gegevens naar burgers.
* Naar aanleiding van ingediend [issue](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/issues/4) in de tekst van de aanvullende specificatie van de GET /verwerkingsacties duidelijker omschreven dat het filteren op Objecttype, Soort Object ID en Identificator feitelijk zorgt dat er op personen gefilterd wordt.
* Naar aanleiding van ingediend [issue](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/issues/3) in de specificatie van het attribuuttype Moment aangegeven dat de tijdzone verplicht is en dat de provider deze opslaat zoals aangereikt en dus niet omrekent.

## 16 december 2020
* Datatype van Bewaartermijn is gewijzigd van `Aantal Jaar` in `Periode`. In de API moet dit nog vertaald worden naar `xs:duration`.
* Gegevenswoordenboek aangevuld met `Verwerkingsactiviteit URL` en `Verwerkingactiviteit URL Afnemer`. Deze attributen waren al verwerking in de afbeeldingen en in de API maar ontbraken nog in gegevenswoordenboek.
* Besluit [B7259](./ontwerp/artefacten/7259.md) stelde nog dat de consumer aan de provider geen doelbinding mee geeft. Inmiddels is dat wel mogelijk via de http header. Essentie van het besluit is echter dat de provider de doelbinding van de consumer niet kan gebruiken om zelf te loggen. Het besluit is aangepast om aan te geven dat de doelbinding (in de vorm van een verwerkingsactiviteit) wel meegegeven kan worden via de http header maar dat de provider moet loggen op basis van een eigen doelbinding.

## 2 december 2020
De API pagina is aangepast op de volgende punten:
* Verwijzing naar Quick Start Guide opgenomen.
* Eerst worden functies opgesomd. Per functie is een beschrijving beschikbaar en een uitleg hoe de mapping is met de API en welke autorisatiescope gebruikt moet worden.
* De API-calls worden daarna opgesomd. Per call is een aparte aanvullende specificatie opgenomen.

## 1 december 2020
Quick Start Guide toegevoegd.

## 23 november 2020
Autorisaties (scopes) toegevoegd aan de Verwerkingsacties API zodat alle logging-functies gemapped kunnen worden op de API calls.
- Beschrijvingen van de [scopes](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/api-write/oas-specification/logging-verwerkingen-api/scopes.md) toegevoegd.
- Resources in de [OAS-specificatie](http://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/VNG-Realisatie/gemma-verwerkingenlogging/master/docs/_content/api-write/oas-specification/logging-verwerkingen-api/openapi.yaml#operation/verwerkingsactie_list) uitgebreid met de juiste scopes.
- [Mapping-tabel](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/api-write/index.md#oas-specificaties) uitgebreid met een extra kolom voor de scopes zodat alle logging-functies gemapped kunnen worden.


## 18 november 2020
- Verwerkingsactie.Vervallen verwijderd uit specificaties van opvragingsfuncties. Alle getourneerde verwerkignsacties zijn niet vervallen dus attribuut heeft geen meerwaarde. (OAS was al correct).

## 16 november 2020
OAS in overeenstemming gebracht met het informatiemodel en UGM. Onder andere:
- Lengte van namen opgerekt van 80 naar 242.
- Voor OIN een reguliere expressie toegevoegd conform gegevenswoordenboek
- Her en der velden toegevoegd, aangepast of verwijderd om de API in overeenstemming te brengen met het informatiemodel
- Her en der velden in andere volgorde gezet om API in overeenstemming te brengen met het informatiemodel
- Her en der foutjes met camelCase opgelost.

## 11 november 2020
Inhoudelijke aanpassingen:
- [Verwerkingsactie](../gegevenswoordenboek/objecttypen/Verwerkingsactie.md).Afnemer was een OIN. Dit hebben we moeten omzetten naar een [Soort ID](../gegevenswoordenboek/attributen/Soort_afnemer_ID.md)/[ID](../gegevenswoordenboek/attributen/Afnemer_ID.md) constructie omdat de afnemer ook een natuurlijk persoon kan zijn (zie [case 2521](./ontwerp/artefacten/2521.md)). Dit raakt alle afbeeldingen van het gegevensmodel en de API waarin het attribuut afnemer voorkomt. Ook de tekst van besluit [B9330](./ontwerp/artefacten/9330.md) 'Opname van afnemer' is aangepast zodat deze weer aansluit bij de wijziging.
- [Attribuuttype Naam](../gegevenswoordenboek/attribuuttypen/Naam.md): Lengte van 80 naar 242.
- [Attribuuttype OIN](../gegevenswoordenboek/attribuuttypen/OIN.md): Formeel patroon in de vorm van een regular expression toegevoegd.
- [Attribuuttype UUID](../gegevenswoordenboek/attribuuttypen/UUID.md): Formeel patroon in de vorm van een regular expression toegevoegd.
- Aanwezigheid van [http header attributen](../api-write/index.md) toegelicht.
N.B. Bovenstaande aanpassingen moeten nog doorgevoerd worden in de API.

Correcties:
- De nieuwe http header attributen (verwerkingsactiviteit id en url) zijn toegevoegd aan [besluit 9177](./ontwerp/artefacten/9177.md).
- De resourcenaam wijziging was nog niet doorgevoerd op de [toelichtingspagina over de API](../api-write/index.md).

Tekstuele aanpassingen:
- [Case 2521](./ontwerp/artefacten/2521.md): 'Inzage van gegevens aan de balie' aangepast. Gaat niet langer alleen over derden, kan ook de burger zelf zijn. Gevolg is dat we het BSN van de burger als afnemer moeten kunnen vastleggen.
- [Case 9041](../../../gegevenswoordenboek/attributen/Afnemer_ID.md)9041.md): 'Notificaties – Informatiearm'. Kleine tekstuele verduidelijkingen.
- [Case 9299](./ontwerp/artefacten/9299.md): 'Synchronisatie naar BGL'. BGL = Binnengemeentelijke Levering.
- [Case 9713](./ontwerp/artefacten/9713.md): 'Inzage door burger - Gegevens die niet langer vertrouwelijk zijn'. Kleine tekstuele correctie.
- [Logging Maturity Level](./logging_maturity_level.md): Kleine verbetering aan leesbaarheid schema met de verschillende niveau's.

## 8 november 2020
- Casing van http header attributen gecorrigeerd.

## 6 november 2020
- In de alle beschrijvingen 'het log' gewijzigd in 'het verwerkingenlog' om duidelijk te maken dat het enkel over de logging van verwerkingen gaat.

## 1 november 2020
- De resource `Actie` hernoemd naar `Verwerkingsactie`.
- De attributen `Actie.Id` en `Actie.Naam` hernoemd naar `Verwerkingsactie.ActieId` en `Verwerkingsactie.ActieNaam`.
- Het attribuut `Verwerkingsactie.VerwerkingsactiviteitUrl` toegevoegd.
- Het attribuut `Verwerkingsactie.VerwerkingsactiviteitIdAfnemer` en `Verwerkingsactie.VerwerkingsactiviteitUrlAfnemer` toegevoegd.
- De http header attributen uitgebreid met `Verwerkingsactiviteit ID` en `Verwerkingsactiviteit URL`.

## 28 oktober 2020
- Update van afbeeldingen van informatie- en gegevensmodel.
- Update van API beschrijvingen.
- Site index toegevoegd.

## 26 oktober 2020
- Enkele foutieve links in pagina's opgelost.

## 15 oktober 2020
- [Uitgangspunten](./uitgangspunten.md) die gehanteerd zijn bij de totstandkoming van de API-standaard beschreven en gerelateerd aan ontwerp artefacten.
-  Excel overzicht van de verschillende [ontwerpartefacten per case](./ontwerp/artefacten/20201011_Artefacten_en_cases.xlsx) toegevoegd.

## 12 oktober 2020
- Beschrijvingen van de tot de standaard behorende [API functies](../api-write/index.md) toegevoegd.
- Case beschrijvingen toegevoegd voor:
    - [Leveren van gegevens](./ontwerp/cases/leveren_van_gegevens.md)
    - [Delegatie en mandatering](../ontwerp/cases/delegatie_en_mandatering.md)
    - [Vertrouwelijke verwerkingen](../ontwerp/cases/vertrouwelijke_verwerkingen.md)
    - [Privaatrechtelijke verwerking](./ontwerp/cases/privaatrechtelijke_verwerkingen.md)
    - [Bewaartermijnen](./ontwerp/cases/bewaartermijnen.md)
    - [Inzage in het log](./ontwerp/cases/inzage_in_log.md)
    - [Bijzondere rechten in de AVG](./ontwerp/cases/bijzondere_rechten.md)
- Diverse tekstuele aanpassingen in ontwerpbesluiten.

## 8 oktober 2020
- Case beschrijvingen voor [het opvragen van gegevens](./ontwerp/cases/Opvragen_van_gegevens.md) toegevoegd.

## 7 oktober 2020
- Case beschrijvingen voor [het bijhouden van gegevens](./ontwerp/cases/Bijhouden_van_gegevens.md) toegevoegd.

## oktober 2020
- Concept [Gegevensmodel](../gegevensmodel/index.md) gepubliceerd.
- Concept [Gegevenswoordenboek](../gegevenswoordenboek/readme.md) gepubliceerd.
- [Ontwerpbesluiten](./ontwerp/ontwerpbesluiten.md) toegevoegd.
- [Aanbevelingen](./ontwerp/aanbevelingen.md) toegevoegd.
- Lijst van [brondocumenten](./ontwerp/brondocumenten.md) toegevoegd.
- Lijst van [openstaande vraagstukken](./ontwerp/vraagstukken.md) toegevoegd.
