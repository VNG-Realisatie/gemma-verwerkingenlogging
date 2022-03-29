---
title: "Objecttype - Verwerkingsactie"
name: Objecttype - Verwerkingsactie
date: 28-09-2020
---

## Beschrijving
Een verwerkingsactie is een operatie die wordt uitgevoerd door een geautomatiseerd systeem waarbij er (persoons)gegevens verwerkt worden.
Een verwerkingsactie wordt uitgevoerd als onderdeel van (een handeling van) een verwerking.

## Toelichting
Binnen de verwerkingsactie is de onderstaande hiërarchie ‘platgeslagen’ (gedenormaliseerd):
Verwerkingsactiviteit -> Verwerking -> Handeling -> Actie

We zien informatie uit deze hiërarchie, in omgekeerde volgorde, terugkomen in de attributen:
- Actie ID: UUID van de Actie
- Actie Naam: Naam van de Actie
- Handeling Naam: Naam van de Handeling
- Verwerking Naam: Naam van de Verwerking
- Verwerking ID: UUID van de Verwerking
- Verwerkingsactiviteit ID: UUID van de Verwerkingsactiviteit

Zie voor extra informatie ook de toelichting op de basisterminologie van het gegevensmodel.

## Synoniemen
In spreektaal wordt vaak het woord ‘logentry’ gebruikt. In dit ontwerp proberen we deze term te voorkomen. ‘Logentry’ wordt door veel mensen namelijk geassocieerd met een logrecord en dat zit te dicht tegen de implementatie aan.

De term kan bijvoorbeeld verwarring geven als gesproken wordt over de verwerking van een huwelijk. Bij de verwerking zijn in dat geval meerdere personen betrokken. Dat zien we terug in het gegevensmodel: bij een Verwerking horen één of meer personen . Het kan echter best zijn dat er in de implementatie gekozen is voor een gedenormaliseerde structuur. Er wordt dan bijvoorbeeld per persoon een apart logrecord aangemaakt met daarin zowel de gegevens van de verwerking als van de persoon.

## Attributen
- [Actie ID](../attributen/Actie_ID.md)
- [Actie Naam](../attributen/Actie_Naam.md)
- [Handeling Naam](../attributen/Handeling_Naam.md)
- [Verwerking Naam](../attributen/Verwerking_Naam.md)
- [Verwerking ID](../attributen/Verwerking_ID.md)
- [Verwerkingsactiviteit ID](../attributen/Verwerkingsactiviteit_ID.md)
- [Verwerkingsactiviteit URL](../attributen/Verwerkingsactiviteit_URL.md)
- [Vertrouwelijkheid](../attributen/Vertrouwelijkheid.md)
- [Bewaartermijn](../attributen/Bewaartermijn.md)
- [Uitvoerder](../attributen/Uitvoerder.md)
- [Systeem](../attributen/Systeem.md)
- [Gebruiker](../attributen/Gebruiker.md)
- [Gegevensbron](../attributen/Gegevensbron.md)
- [Soort afnemer ID](../attributen/Soort_afnemer_ID.md)
- [Afnemer ID](../attributen/Afnemer_ID.md)
- [Verwerkingsactiviteit ID Afnemer](../attributen/Verwerkingsactiviteit_ID_Afnemer.md)
- [Verwerkingsactiviteit URL Afnemer](../attributen/Verwerkingsactiviteit_URL_Afnemer.md)
- [Verwerking ID Afnemer](../attributen/Verwerking_ID_Afnemer.md)
- [Tijdstip](../attributen/Tijdstip.md)
- [Tijdstip registratie](../attributen/Tijdstip_registratie.md)
- [Vervallen](../attributen/Vervallen.md)
