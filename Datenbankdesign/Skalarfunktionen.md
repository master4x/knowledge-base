# Skalarfunktionen
Mithilfe von Skalarfunktionen (ähnlich zu [[Aggregatsfunktionen]]) können Sie einen Wert von einem *Datentyp* in einen anderen *konvertieren* und *[[Datentypen|Datums- und Zeitwerte]] verarbeiten*. Darüber hinaus können Sie Teile einer Zeichen- oder grafischen Zeichenfolge bearbeiten und Nullwerte vermeiden.
- `DAY()`
- `MONTH()`
- `DATEADD()`
- `DATEDIFF()`
- `DATENAME()`

``` sql
SELECT DATEDIFF(year, Einstellung, Entlassung) FROM Mitarbeiter;
```
