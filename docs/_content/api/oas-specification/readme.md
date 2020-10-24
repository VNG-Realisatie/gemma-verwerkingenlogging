## Specificatie van de API voor Logging en Werking
API specificatie (OAS3) in
  [ReDoc](http://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/HenriKorver/gemma-verwerkingenlogging/master/docs/_content/api/oas-specification/logging-verwerkingen-api/openapi.yaml),
  [Swagger](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/HenriKorver/gemma-verwerkingenlogging/master/docs/_content/api/oas-specification/logging-verwerkingen-api/openapi.yaml) of
  [YAML](https://raw.githubusercontent.com/HenriKorver/gemma-verwerkingenlogging/master/docs/_content/api/oas-specification/logging-verwerkingen-api/openapi.yaml)

## Mapping logging functies naar API-calls

<!-- ![mapping functies naar api](https://github.com/HenriKorver/gemma-verwerkingenlogging/blob/master/docs/_content/api/oas-specification/mapping.png) -->

| Code         | Logging functie      | API Call      | Stijl          |
| -----------  | :-----------         | :----------   | :-----------   |
| F7446        |  Log Actie           | POST /acties  | REST           |
| F6624 | Log Vertrouwelijke Actie *	|||
| F2969 | Wijzig vertrouwelijkheid van Verwerking | POST /wijzigVertrouwelijkheidVerwerking | RPC |
| F2969 | Wijzig bewaartermijn van Verwerking | POST /wijzigBewaartermijnVerwerking | RPC |
| F8316 | Wijzig Actie | PUT /acties/{uuid} | REST |
| F3835 | Wijzig Vertrouwelijke Actie*	|||
| F9906 | Verwijder Actie | DELETE /acties/{uuid} | REST |
| F2265 | Verwijder Vertrouwelijke Actie* |||
| F4086 | Opvragen Acties – Beperkte set velden, niet vertrouwelijk | GET /acties?beperkteSet=true | REST |
| F2525 | Opvragen Acties – Beperkte set velden, vertrouwelijkheid opgeheven* |||
| F9787 | Opvragen Acties – Alle velden, niet vertrouwelijk	| GET /acties?beperkteSet=true | REST |
| F0143 | Opvragen Acties – Alle velden, vertrouwelijk* |||		

Opmerkingen:

- Vanwege het platslaan van het objecttype `Verwerking` in het objecttype `Actie` passen de logging-functies F2969 en F2969 niet in het CRUD-model van REST en zijn deze functies als RPC-calls gespecificeerd.
- Logging functies met een sterretje zijn nog niet vertaald naar API-calls.
