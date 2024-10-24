**Skalarfunktionen** ermöglichen es, einzelne Werte zu verarbeiten und zu transformieren. Sie dienen dazu, einen Wert von einem *Datentyp* in einen anderen zu konvertieren, *[[Datentypen|Datums- und Zeitwerte]]* zu verarbeiten und Teile von Zeichenfolgen zu bearbeiten. Außerdem können sie dabei helfen, Nullwerte zu vermeiden.

# Beispiele für gängige Skalarfunktionen:
- `DAY()`: Gibt den Tag eines Datums zurück.
- `MONTH()`: Gibt den Monat eines Datums zurück.
- `DATEADD()`: Fügt einem Datum eine bestimmte Zeitspanne hinzu.
- `DATEDIFF()`: Berechnet die Differenz zwischen zwei Datumswerten basierend auf einer bestimmten Zeiteinheit.
- `DATENAME()`: Gibt den Namen eines Datumsbestandteils zurück, z. B. den Monat oder Wochentag.

**Beispiel**: Berechnung der Dauer zwischen zwei Daten
```sql
SELECT DATEDIFF(YEAR, Einstellung, Entlassung) FROM Mitarbeiter;
```

Skalarfunktionen sind nützlich, um einzelne Datenwerte zu manipulieren und spezifische Informationen aus Datums-, Zeit- und Zeichenfolgen zu extrahieren.
