---
title: "Attribuuttype - Periode"
name: Attribuuttype - Periode
date: 16-12-2020
---

## Logisch datatype
Duurformaat volgens ISO 8601 [(xs:duration)](https://www.w3schools.com/xml/schema_dtypes_date.asp)

ISO 8601-duur wordt uitgedrukt in het volgende formaat, waarbij (n) wordt vervangen door de waarde voor elk van de datum- en tijdelementen die volgen op (n):

`P` (n) `Y` (n) `M` (n) `DT` (n) H (n) M (n) S

Waar:

- `P` P geeft de periode aan (verplicht) en wordt altijd aan het begin van de duur geplaatst.
- `Y` is de jaaraanduiding die volgt op de waarde voor het aantal jaren.
- `M` is de maandaanduiding die volgt op de waarde voor het aantal maanden.
- `W` is de weekaanduiding die volgt op de waarde voor het aantal weken.
- `D` is de dagaanduiding die volgt op de waarde voor het aantal dagen.
- `T` geeft het begin van een tijdgedeelte aan (vereist als u uren, minuten of seconden gaat specificeren)
- `H` is de uuraanduiding die volgt op de waarde voor het aantal uren.
- `M` is de minutenaanduiding die volgt op de waarde voor het aantal minuten.
- `S` is de tweede aanduiding die de waarde volgt voor het aantal seconden.

Bijvoorbeeld:

- `P3Y6M4DT12H30M5S` Vertegenwoordigt een duur van drie jaar, zes maanden, vier dagen, twaalf uur, dertig minuten en vijf seconden.
