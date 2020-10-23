## Specificatie van de API voor Logging en Werking
API specificatie (OAS3) in
  [ReDoc](http://redocly.github.io/redoc/?url=https://raw.githubusercontent.com/HenriKorver/gemma-verwerkingenlogging/master/docs/_content/api/oas-specification/logging-verwerkingen-api/openapi.yaml),
  [Swagger](https://petstore.swagger.io/?url=https://raw.githubusercontent.com/HenriKorver/gemma-verwerkingenlogging/master/docs/_content/api/oas-specification/logging-verwerkingen-api/openapi.yaml) of
  [YAML](https://raw.githubusercontent.com/HenriKorver/gemma-verwerkingenlogging/master/docs/_content/api/oas-specification/logging-verwerkingen-api/openapi.yaml)

## Mapping logging functies naar API-calls

![mapping functies naar api](https://github.com/HenriKorver/gemma-verwerkingenlogging/blob/master/docs/_content/api/oas-specification/mapping.png)

N.B. Vanwege het platslaan van het objecttype `Verwerking` in het objecttype `Actie` passen de logging-functies F2969 en F2969 niet in het CRUD-model van REST en zijn deze functies als RPC-calls gespecificeerd.
