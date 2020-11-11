---
title: "Voortgang ontwikkeling API-standaard voor logging van verwerkingen"
name: Voortgang ontwikkeling API-standaard voor logging van verwerkingen
---

## 11 november 2020
Aanpassingen informatiemodel:
- [Verwerkingsactie](./gegevenswoordenboek/objecttypen/Verwerkingsactie.md).Afnemer was een OIN. Dit hebben we moeten omzetten naar een Soort ID/ID constructie omdat de afnemer ook een natuurlijk persoon kan zijn (zie [case 2521](./ontwerp/artefacten/2521.md)). Dit raakt alle afbeeldingen van het gegevensmodel en de API waarin het attribuut afnemer voorkomt.
- [Attribuuttype Naam](../gegevenswoordenboek/attribuuttypen/Naam.md): Lengte van 80 naar 242.
- [Attribuuttype OIN](../gegevenswoordenboek/attribuuttypen/OIN.md): Formeel patroon in de vorm van een regular expression toegevoegd.
- [Attribuuttype UUID](../gegevenswoordenboek/attribuuttypen/UUID.md): Formeel patroon in de vorm van een regular expression toegevoegd.
N.B. Bovenstaande aanpassingen moeten nog doorgevoerd worden in de API.

Tekstuele aanpassingen:
- [Case 2521](./ontwerp/artefacten/2521.md): 'Inzage van gegevens aan de balie' aangepast. Gaat niet langer alleen over derden, kan ook de burger zelf zijn. Gevolg is dat we het BSN van de burger als afnemer moeten kunnen vastleggen.
- [Case 9041](./ontwerp/artefacten/9041.md): 'Notificaties – Informatiearm'. Kleine tekstuele verduidelijkingen.
- [Case 9299](./ontwerp/artefacten/9299.md): 'Synchronisatie naar BGL'. BGL = Binnengemeentelijke Levering.
- [Case 9713](./ontwerp/artefacten/9713.md): 'Inzage door burger - Gegevens die niet langer vertrouwelijk zijn'. Kleine tekstuele correctie.
- [Logging Maturity Level](./logging_maturity_level.md): Kleine verbetering aan leesbaarheid schema met de verschillende niveau's.

## 8 november 2020
- Casing van html header attributen gecorrigeerd.

## 6 november 2020
- In de alle beschrijvingen 'het log' gewijzigd in 'het verwerkingenlog' om duidelijk te maken dat het enkel over de logging van verwerkingen gaat.

## 1 november 2020
- De resource `Actie` hernoemd naar `Verwerkingsactie`.
- De attributen 'Actie.Id' en 'Actie.Naam' hernoemd naar 'Verwerkingsactie.ActieI'd en 'Verwerkingsactie.ActieNaam'.
- Het attribuut 'Verwerkingsactie.VerwerkingsactiviteitUrl' toegevoegd.
- Het attribuut 'Verwerkingsactie.VerwerkingsactiviteitIdAfnemer' en 'Verwerkingsactie.VerwerkingsactiviteitUrlAfnemer' toegevoegd.
- De html header attributen uitgebreid met 'Verwerkingsactiviteit ID' en 'Verwerkingsactiviteit URL'.

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
- Beschrijvingen van de tot de standaard behorende [API functies](../api/index.md) toegevoegd.
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
