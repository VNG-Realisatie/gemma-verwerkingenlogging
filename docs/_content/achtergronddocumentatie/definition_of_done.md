---
title: "Definition of Done"
date: '10-10-2020'
---

Op deze pagina wordt beschreven welke eisen aan de verschillende onderdelen van een opgeleverde versie van de Verwerkingenlogging API-standaard worden gesteld. De onderdelen die hierbij een rol spelen zijn: 

- [API-standaard gepositioneerd in de architectuur](./definition_of_done.md#api-standaard-gepositioneerd-in-de-architectuur)  
- [Informatiemodel behorend bij de API-standaard](./definition_of_done.md#informatiemodel-behorend-bij-de-api-standaard)
- [Functionele en technische API-specificaties](./definition_of_done.md#functionele-en-technische-api-specificaties) 
- [Referentie-implementatie](./definition_of_done.md#referentie-implementatie)
- [Testbaarheid via compliancy- en testvoorziening](./definition_of_done.md#testbaarheid-via-api-testplatform) 
- [Stakeholder documentatie](./definition_of_done.md#stakeholder-documentatie) 
- [Overdracht- en beheerdocumentatie](./definition_of_done.md#overdracht--en-beheerdocumentatie) 
- [Aanvullende specificaties voor beheer door VNG-R](./definition_of_done.md#aanvullende-specificaties-voor-beheer-door-vng-r) 
 
In onderstaande paragrafen worden de criteria die binnen de verschillende onderdelen worden gehanteerd beschreven. Deze criteria zijn overgenomen uit de generieke Definition of Done voor API-standaarden van VNG Realisatie. Bij het opleveren van de Verwerkingenlogging API-standaard wordt aan de verschillende eisen invulling gegeven, of wordt uitgelegd waarom van de gestelde eis is afgeweken. 
 
## API-standaard gepositioneerd in de Architectuur

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| De stakeholders van de API-standaard zijn beschreven  | <img src="./_assets/greensmiley.png" alt="" width="30"/>  | [<img src="./_assets/document.png" alt="" width="20"/>](../productvisie/index.md)  |
| Interactiepatronen zijn gemodelleerd | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |  [<img src="./_assets/document.png" alt="" width="20"/>](../achtergronddocumentatie/ontwerp/ontwerpcases.md) |
| Positie van de API-standaard in de GEMMA informatiearchitectuur is gemodelleerd | <img src="./_assets/greensmiley.png" alt="" width="30"/> | [<img src="./_assets/document.png" alt="" width="20"/>](../architectuur/index.md)   |
| Verwacht gedrag van een API is gemodelleerd als applicatieproces |   |   |
| De referentiecomponenten die het koppelvlak moeten realiseren zijn beschreven | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| Per referentiecomponent is beschreven welke verplicht dan wel optioneel te leveren (provider) of te gebruiken (consumer) services en operaties geïmplementeerd moeten zijn om compliant aan de standaard te zijn. |   |   |
| Modellen zijn gemodelleerd in Archi (Archimate 3.x) conform conventies GEMMA | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| Modellen zijn opgeslagen op GitLab / Github en ingericht voor samenwerking (main/develop branches) | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |

## Informatiemodel behorend bij de API-standaard

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| Er is een semantisch informatiemodel of een verwijzing naar het gebruikte semantisch informatiemodel  | <img src="./_assets/greensmiley.png" alt="" width="30"/>  | [<img src="./_assets/document.png" alt="" width="20"/>](../gegevensmodel/semantisch_informatiemodel/readme.md) |
| Dit conceptueel informatiemodel (CIM) is gemodelleerd conform de laatst vastgestelde versie Metamodel Informatiemodellen (MIM)  | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| Het informatiemodel is gebaseerd op de beschikbare standaard voor het domein  | n.v.t. |   |
| Er is een vertaling van het informatiemodel naar de API (vice versa), bij voorkeur is deze vastgelegd in de vorm van een uitwisselingsgegevensmodel (UGM). Tenminste bevat deze een technische beschrijving van resources, attributen en eigenschappen  |  <img src="./_assets/greensmiley.png" alt="" width="30"/> | [<img src="./_assets/document.png" alt="" width="20"/>](../gegevensmodel/uitwisselingsgegevensmodel/readme.md) |
| Informatiemodellen (CIM en UGM) zijn gemodelleerd conform de daarvoor geldende best practices  | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |  |
| Ontwerpbesluiten voor vertaling van CIM naar UGM zijn vastgelegd  | <img src="./_assets/greensmiley.png" alt="" width="30"/> | [<img src="./_assets/document.png" alt="" width="20"/>](../gegevensmodel/uitwisselingsgegevensmodel/readme.md)   |

## Functionele en Technische API-specificaties

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| Er is een globale functionele beschrijving | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |  [<img src="./_assets/document.png" alt="" width="20"/>](https://github.com/VNG-Realisatie/gemma-verwerkingenlogging/blob/master/docs/_content/quickstart/index.md) |
| Er zijn specificaties die het gedrag van de API beschrijven. Voor de consumer zijn deze opgenomen in de OAS, voor de provider zijn dit aanvullende specificaties |<img src="./_assets/greensmiley.png" alt="" width="30"/>  |  [<img src="./_assets/document.png" alt="" width="20"/>](../api-write/index.md) [<img src="./_assets/document.png" alt="" width="20"/>](../api-read/index.md)|
| Voldoet aan landelijke API strategie, in het bijzonder de core design rules, en de VNG-R best practices (op basis van verzamelde Design Decisions). Afwijkingen zijn gedocumenteerd | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| Informatiebeveiliging en privacy best practices (IBD) zijn geborgd | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| De OAS3-specificatie is door een peer uit het standaardisatie team gereviewed |   |   |
| De OAS3-specificatie is getest voor toepasbaarheid in de mainstream code-generatoren (Spring, SDK’s (met pumblingcode)) |   |   |
| Technische specificaties opgesteld in Open API Specification 3.x | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |  [<img src="./_assets/document.png" alt="" width="20"/>](../api-write/index.md) [<img src="./_assets/document.png" alt="" width="20"/>](../api-read/index.md) |

## Referentie-implementatie

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| API-standaard is geïmplementeerd in een referentieimplementatie van de provider in een gangbare programmeertaal |   | Q1 2021  |
| Implementeert de gehele OAS-specificatie inclusief de eventueel gedefinieerde aanvullende specificatie |   | Q1 2021  |

## Testbaarheid via API testplatform

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| Testgevallen zijn beschreven voor elke service/operatie en aanvullende specificaties, zowel voor de happy als de unhappy flows |   |  Q1 2021 |
| Elk testgeval beschrijft het logische testgeval, de teststap(pen) (wat wordt gedaan) en het verwachte resultaat |   | Q1 2021  |
| Er zijn compliancy tests beschikbaar voor elke referentie-component (consumers en providers) en alle betreffende services en operaties, zodat leveranciers kunnen testen en aantonen dat hun applicatie voldoet aan de standaard |   | Q1 2021 |
| Is er sprake van een API die zich beperkt tot het lezen van gegevens dan dient er een testset beschreven te zijn voor de provider |   | Q1 2021  |
| Testgevallen zijn geïmplementeerd als Postman-scripts zodat de API geautomatiseerd getest kan worden |   | Q1 2021  |

## Stakeholder documentatie

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| T.b.v. informatiemanagers (e.a.): globale functionele beschrijving staat op GEMMAonline | <img src="./_assets/greensmiley.png" alt="" width="30"/>  | [<img src="./_assets/document.png" alt="" width="20"/>](https://www.gemmaonline.nl/index.php/Thema_Logging_en_verwerkingsactiviteiten)  |
| T.b.v. architecten: het architectuurmodel is gepubliceerd op GEMMAonline | <img src="./_assets/greensmiley.png" alt="" width="30"/>  | [<img src="./_assets/document.png" alt="" width="20"/>](https://www.gemmaonline.nl/index.php/Thema_Logging_en_verwerkingsactiviteiten)  |
| T.b.v. ontwikkelaars: het informatiemodel is gepubliceerd op VNG-Realisatie Github | <img src="./_assets/greensmiley.png" alt="" width="30"/>  | [<img src="./_assets/document.png" alt="" width="20"/>](../gegevensmodel/semantisch_informatiemodel/readme.md)  |
| T.b.v. ontwikkelaars: de technische beschrijving is gepubliceerd op VNG-Realisatie Github | <img src="./_assets/greensmiley.png" alt="" width="30"/>  | [<img src="./_assets/document.png" alt="" width="20"/>](../api-write/index.md) [<img src="./_assets/document.png" alt="" width="20"/>](../api-read/index.md)  |
| T.b.v. ontwikkelaars: OAS specificatie (beschikbaar via Redoc en SwaggerUI) is gepubliceerd op VNG-Realisatie Github | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |  [<img src="./_assets/document.png" alt="" width="20"/>](../api-write/index.md) [<img src="./_assets/document.png" alt="" width="20"/>](../api-read/index.md) |
| T.b.v. ontwikkelaars: de uitleg en installatie-instructies van de referentieimplementaties inclusief testgevallen is gepubliceerd op VNG-Realisatie Github |   | Q1 2021  |
| T.b.v. ontwikkelaars: Postman-scripts zijn gepubliceerd op api-test.nl zodat iedereen kan testen of de implementatie voldoet aan zijn specificatie |   | Q1 2021  |
| De API-ontwikkelagenda is up-to-date | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| De Componenten/software catalogus is up-to-date |   |   |
| T.b.v. bestuurders: de API-standaard is vermeld op de VNG-site |   |   |

## Overdracht- en beheerdocumentatie

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| Belangrijke ontwerp-overwegingen zijn beschreven en gemotiveerd | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |  [<img src="./_assets/document.png" alt="" width="20"/>](../achtergronddocumentatie/ontwerp.md) |
| Er wordt voldaan aan de acceptatiecriteria van de beheerorganisatie die de standaard in beheer neemt |   |   |
| Er is een backlog (lijst met fouten, gewenste verbeteringen, gewenste uitbreidingen etc) | <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| De verantwoordelijke voor beheer is bekend |  <img src="./_assets/greensmiley.png" alt="" width="30"/>  |   |
| Beheerafspraken zijn beschreven |   |   |

## Aanvullende specificaties voor beheer door VNG-R

| Criterium | Status | Toelichting/Link |
|:--|:-:|---|
| Voor zaken die in VNG-R beheer worden genomen is het beheerkader getoetst |   |   |
| Informatiemodellen (CIM en UGM) zijn vastgelegd in Enterprise Architect |  <img src="./_assets/greensmiley.png" alt="" width="30"/> |   |
| Informatiemodel is opgeslagen in SVN |  <img src="./_assets/greensmiley.png" alt="" width="30"/> |   |
| Er is voldaan aan de overige beheerkaders |   |   |
| Releasebeleid is beschreven |   |   |
| De referentie-implementatie blijft beschikbaar als sandbox |   |   |
