---
title: "Gegevensmodel logging van verwerkingen"
name: Gegevensmodel logging van verwerkingen
date: 28-09-2020
---
## Basisterminologie: Verwerkingsactiviteit, verwerking, handeling en actie

### Context
-	Gemeenten moeten volgens de AVG een Register van verwerkingsactiviteiten hebben (het VAR).
-	Het begrip verwerkingsactiviteit wordt niet in de AVG gedefinieerd.
-	In de VAR’s van gemeenten komen zowel hele generieke als hele specifieke verwerkingsactiviteiten voor. De granulariteit in het VAR wisselt dus sterk. Zo treffen we bijvoorbeeld ‘BRP Registratie’ aan, maar ook ‘Geslachtswijziging’.
-	Het begrip verwerking wordt wel in de AVG gedefinieerd.

### Terminologie
**Verwerkingsactiviteit**

Op basis van de inhoud van de gemeentelijke VAR’s is het nog niet zo eenvoudig om een eenduidige definitie te geven van het begrip verwerkingsactiviteit.
Nemen we ‘BRP Registratie’, ‘Gegevenslevering aan derden’ of ‘Fraudeonderzoek’ als uitgangspunt dan beschrijven deze begrippen eigenlijk een hele groep of categorie van verwerkingen. Nemen we ‘Geslachtswijziging’ als voorbeeld dan beschrijft dat een heel concrete taak van de gemeente.
Het wenselijk lijkt om het VAR op een zo concreet mogelijk niveau in te richten. Daar zijn twee kanttekeningen bij te plaatsen. Ten eerste zal dit naar alle waarschijnlijkheid een geleidelijk verbeteringsproces zijn. Ten tweede valt te verwachten dat er altijd verwerkingsactiviteiten in het register zullen voorkomen die niet specifieker omschreven kunnen worden. 

Dit alles in overweging nemend komen tot de volgende definitie:

`Verwerkingsactiviteit: Een verwerkingsactiviteit is of een categorie van verwerkingen of een concreet soort verwerking.`

We voegen in de definitie dus eigenlijk twee begrippen samen. Dat is wat ongebruikelijk maar noodzakelijk om recht te doen aan de daadwerkelijke invulling van het VAR. 

**Verwerking**

In de AVG staat in artikel 4 de volgende definitie:

`„verwerking”: een bewerking of een geheel van bewerkingen met betrekking tot persoonsgegevens of een geheel van persoonsgegevens, al dan niet uitgevoerd via geautomatiseerde procedés, zoals het verzamelen, vastleggen, ordenen, structureren, opslaan, bijwerken of wijzigen, opvragen, raadplegen, gebruiken, verstrekken door middel van doorzending, verspreiden of op andere wijze ter beschikking stellen, aligneren of combineren, afschermen, wissen of vernietigen van gegevens;`

Dit geeft een kader maar vult het begrip onvoldoende in vanuit het perspectief van een gegevensmodel. We definiëren een verwerking als:

`Verwerking: Een verwerking is een concrete taak die een gemeente uitvoert. De taak vormt vanuit het perspectief van de burger of medewerker een logisch geheel.`

Als de verwerking is afgerond is er dus ook vanuit het perspectief van de burger of medewerker echt iets afgerond: het adres is aangepast, het huwelijk is voltrokken en geregistreerd, de vergunning verleend, het fraudeonderzoek afgesloten etc.
Binnen de bedrijfsvoering van de gemeente zal een verwerking dus vaak corresponderen met een zaak of een verzoek.

Een bijzondere categorie van verwerkingen zijn de z.g.n. geautomatiseerde verwerkingen. Hierbij is de aanleiding niet een verzoek van een burger of het initiatief van een medewerker maar de planning van een geautomatiseerde taak. Voorbeelden zijn levering van gegevens aan de BRP of het uitvoeren van een selectie t.b.v. een rapportage.

**Handeling**

Eenvoudige verwerkingen zoals de registratie van een verhuizing of het leveren van gegevens aan een derde kunnen vaak in één keer uitgevoerd worden. Bij complexere verwerkingen is er vaak sprake van een proces met meerdere stappen.
Bij inzage in het log kan het voor de burger en de gemeentelijke medewerkers zeer verhelderend zijn om bij complexere verwerkingen niet alleen de naam van de verwerking te lezen (bijvoorbeeld ‘huwelijk’) maar ook de naam van de stap in het proces (‘ondertrouw’). Dit soort processtappen noemen we handelingen.

`Handeling: Een handeling is één stap in de uitvoering van een verwerking. Deze stap kan bij een zogenaamde ‘happy flow’ zonder onderbrekingen uitgevoerd worden.`

Toelichting:
-	Bij eenvoudige verwerkingen is het de enige stap in de uitvoering van de verwerking.
-	Bij een ‘happy flow’ zijn er geen uitzonderingen en gaat er niets fout.
-	In spreektaal zouden we zeggen dat een handeling op ‘één moment’ in de tijd uitgevoerd wordt.

**Actie**

Een handeling kan bestaan uit meerdere interacties met een systeem. Het kan bijvoorbeeld zijn dat we eerst gegevens ophalen, wellicht nog extra details opvragen, een aanpassing maken en daarna de wijzigingen opslaan. In dat geval zijn er in het kader van een handeling vier acties uitgevoerd.

`Actie: Een actie is een operatie die wordt uitgevoerd door een geautomatiseerd systeem waarbij er (persoons)gegevens verwerkt worden. Een actie wordt uitgevoerd als onderdeel van (een handeling van) een verwerking.`

Aangezien we het loggen beperken tot geautomatiseerde gegevensverwerking is er bij een acties dus altijd sprake van interactie met een geautomatiseerd systeem zoals een app, service, applicatie, gegevensmagazijn et cetera.

Zouden we ook handmatige gegevensverwerkingen loggen dan zou ook het bekijken van de gegevens op bijvoorbeeld het identiteitsbewijs van een burger een actie zijn.

## Voorbeelden
Onderstaande tabel toont voor vijf verschillende cases voorbeelden bij de begrippen:


Opmerkingen bij de cases:
-	Bij cases 1 en 5 is de verwerkingsactiviteit duidelijk een categorie van bij elkaar horende verwerkingen. Anders gezegd: Een burger kan deze verwerkingen niet één op één terugvinden op de website van de gemeente.
-	Bij cases 2, 3 en 4 lijkt de verwerkingsactiviteit een concreet soort verwerking. Deze begrippen zou je als burger wel terug kunnen vinden op de website van de gemeente. Of dit ook daadwerkelijk zo is hangt af van de verdere inrichting van het VAR. Stel dat er iets fout gegaan is bij de registratie en deze moet gecorrigeerd worden. Valt die correctie dan onder dezelfde verwerkingsactiviteit of is dat een aparte activiteit? Bevat het VAR geen aparte verwerkingsactiviteit voor de correctie dan zijn ook deze verwerkingsactiviteiten dus eigen categorieën van bij elkaar horende verwerkingen.



