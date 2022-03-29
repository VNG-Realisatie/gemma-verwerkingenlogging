---
layout: page-with-side-nav
title: Aanvullende specificaties voor POST /verwerkingsacties
date: 28-03-2022
---

# Aanvullende specificaties voor POST /verwerkingsacties

## Autorisatie

| Scope | Autorisatie | 
| :---- | :---- |
| `create:normal` | Laat toe om niet vertrouwelijke (normale) verwerkingsacties aan te maken. |
| `create:confidential` | Laat toe om zowel vertrouwelijke als niet vertrouwelijke (normale) verwerkingsacties aan te maken. |

## Controles

| Regel | Foutcode |
| :---- | :---- |
| Als het element `vertrouwelijkheid` gevuld is met de waarde `Vertrouwelijk` dan moet de autorisatiescope `create:confidential` zijn. | 403 |
| Het element `vertrouwelijkheid` mag nooit de waarde `Opgeheven` hebben. | 403 |

Als het element `vertrouwelijkheid` gevuld is met de waarde `Normaal` dan wordt er niet gecontroleerd op de autorisatiescope. Anders moet er bij het wegschrijven van elke logregel een round trip gemaakt worden naar de Autorisatie Component (AC) en dat is niet wenselijk om performance redenen. Elke client die geregistreerd is bij de AC heeft per default `create:normal` rechten. De Verwerkingen Logging API checkt wel bij elke inkomende call of de client geregistreerd is. Hiervoor hoeven geen (herhalende) round trips gemaakt te worden naar de AC omdat ervan uit wordt gegaan dat de Verwerkingen Logging API reeds een lijstje met client_id/secret attributen heeft opgebouwd voor alle clients die via de AC geregistreerd zijn. Voor elke nieuwe client hoeft slechts één round trip naar de AC gemaakt te worden om het client_id/secret op te halen en toe te voegen aan het lijstje.

## Gedrag
Voor het responsbericht gelden de volgende regels:
* Het element `url` is gevuld met een URL-referentie naar de aangemaakte verwerkingsactie.
* Het element `actieId` is gevuld met een nieuwe UUID.
* Het element `tijdstipRegistratie` is gevuld met de actuele datum/tijd.
* Alle overige elementen zijn gevuld met dezelfde waarden die in de request zijn meegegeven. Elementen die niet zijn meegegeven in de request worden wel teruggegeven in de respons, maar dan met lege waarden.

In [B3891](../achtergronddocumentatie/ontwerp/artefacten/3891.md) is beschreven hoe een log dat in technische zin immutable is toch in logische zin kan worden aangepast.

Bij een dergelijk log zou het volgende conceptuele algoritme toegepast moeten worden op de achterliggende database:
* Er wordt een nieuw `Verwerkingsactie` record aangemaakt met attributen zoals beschreven in het SIM/UGM.
* Het attribuut `Actie ID` krijgt een nieuwe UUID.
* Het attribuut `Tijdstip Registratie` krijgt de actuele datum/tijd.
* Het attribuut `Vervallen` krijgt de waarde `Nee`.
* Alle overige attributen van het record krijgen de waarden van de corresponderende elementen die in het request bericht zijn meegegeven.
