---
title: "Definition of Done Verwerkingenlogging API-standaard"
date: '10-10-2020'
---

In dit document wordt beschreven welke eisen aan de verschillende onderdelen van een opgeleverde versie van de Verwerkingenlogging API-standaard worden gesteld. De onderdelen die hierbij een rol spelen zijn: 

- Stakeholder documentatie 
- Informatiemodel behorend bij de API-standaard 
- API-standaard gepositioneerd in de architectuur  
- Functionele specificatie van de API-standaard 
- API-specificaties  
- Referentieimplementatie 
- Testbaarheid via compliancy- en testvoorziening 
- Overdracht- en beheerdocumentatie 
 
In onderstaande paragrafen worden de eisen die aan de verschillende onderdelen worden gesteld beschreven. 

**Stakeholder documentatie**
- De voor de stakeholders relevante onderdelen van de standaard (informatiemodel, API-specificaties, functionele specificatie, architectuurmodellen, referentieimplementatie(s) en testgevallen) zijn gepubliceerd op de VNG Realisatie Github of GEMMAonline omgeving. 
- er is een beschrijving die ontwikkelaars op weg helpt om te starten met implementatie van de API-standaard 
- er is uitleg en installatie-instructies van de referentieimplementaties 
- er is uitleg over hoe mee ontwikkeld kan worden aan de referentieimplementatie(s), inclusief gebruik van relevante tooling 
- er zijn Postman-scripts met voorbeelden zodat consumers snel kunnen leren hoe ze de API moeten aanroepen. 
 
**Informatiemodel**

- Oplevering informatiemodel Verwerkingenlogging
- Modellering van het informatiemodel conform Metamodel Informatiemodellen (MIM) versie 1.1
- Informatiemodel gemodelleerd in Enterprise Architect conform de daarvoor binnen VNR-R geldende best practices 
- Informatiemodel is opgeslagen in SVN-omgeving VNG-R
 
**Architectuur**
- Modellen zijn gemodelleerd in Archi (Archimate 3.x) conform conventies GEMMA 
- Modellen zijn opgeslagen op Github omgeving VNG-R en ingericht voor samenwerking (main/develop branches)
- De stakeholders van de API-standaard zijn beschreven 
- Interactiepatronen zijn gemodelleerd 
- Positie van de API-standaard in de GEMMA informatiearchitectuur is gemodelleerd 
- Verwacht gedrag van een API is gemodelleerd als applicatieprocessen 
- De referentiecomponenten die het koppelvlak moeten realiseren zijn beschreven 
- Per referentiecomponent is beschreven welke verplicht dan wel optioneel te leveren (provider) of te gebruiken (consumer) services en operaties geïmplementeerd moeten zijn om compliant aan de standaard te zijn. 
 
**API-specificaties**
- Opgesteld conform Open API Specification 3.x 
- Gepubliceerd op VNG-Realisatie Github omgeving en beschikbaar via Redoc en Swagger 
- Ontwerpbeslissing zijn vertaald naar (aanvullende) specificaties 
- Voldoet aan landelijke API strategie, in het bijzonder de core design rules 
- Informatiebeveiliging en privacy best practices (IBD) worden gevolgd 
- In constructen wordt rekening wordt gehouden met code generatie 
- API-specificaties volgen de VNG-R best practices.  

**Compliancy en testen**
- API-standaard is geïmplementeerd in een referentieimplementatie  
- Testgevallen zijn beschreven voor elke service/operatie en aanvullende specificaties, zowel voor de happy als de unhappy flows 
- Elk testgeval beschrijft het logische testgeval, de teststap(pen) (wat wordt gedaan) en het verwachte resultaat 
- Er zijn compliancy tests beschikbaar voor elke referentie-component (consumers en providers) en alle betreffende services en operaties, zodat leveranciers kunnen testen en aantonen dat hun applicatie voldoet aan de standaard 
- Testgevallen zijn geïmplementeerd als Postman-scripts zodat de API geautomatiseerd getest kan worden. 
- Postman-scripts zijn gepubliceerd op api-test.nl zodat iedereen kan testen of de API voldoet aan zijn specificatie. 

**Referentie-implementatie** 
- Zowel consumer als provider implementatie. 
- Implementeert de OAS-specificatie inclusief de eventueel gedefinieerde aanvullende specificatie 
- Is voldoende functioneel om implementatie en gebruik van de API-standaard te demonstreren en compliancy aan te tonen 

**Overdrachtsdocument (beheer)** 
- De genomen ontwerpbeslissingen zijn beschreven en gemotiveerd 
- Er is een lijst met bekende fouten, gewenste verbeteringen, gewenste uitbreidingen (backlog) 
- Er wordt voldaan aan de acceptatie criteria van de beheer organisatie die de standaard in beheer neemt 
- Beheerafspraken zijn beschreven 
