In SQL werden **Datentypen** verwendet, um festzulegen, welche Art von Daten in den Spalten einer Tabelle gespeichert werden kann. Die Wahl des richtigen Datentyps ist wichtig, da sie Auswirkungen auf die Speichergröße, Leistung und Integrität der Daten hat. SQL-Datentypen lassen sich grob in folgende Kategorien einteilen: Zeichenfolgen, numerische Typen, Datum und Zeit sowie spezielle Typen.

# 1. Zeichenfolgen (String) Datentypen
Zeichenfolgen-Datentypen werden verwendet, um Textdaten zu speichern. SQL bietet verschiedene Typen für Textfelder, je nach Länge und Flexibilität der gespeicherten Daten.
- **CHAR(n)**: Fester Speicherplatz für eine Zeichenkette mit der festen Länge `n`. Ideal für Felder, die immer eine bestimmte Länge haben, wie z. B. Postleitzahlen.
- **VARCHAR(n)**: Variabler Speicherplatz für Zeichenketten mit einer maximalen Länge `n`. Gut geeignet für Felder mit unterschiedlich langen Texten, z. B. Namen oder Adressen.
- **TEXT**: Für sehr lange Texte ohne maximale Länge, wie Beschreibungen oder Kommentare. Die genaue Länge kann von der Datenbank abhängig sein.

# 2. Numerische Datentypen
Numerische Datentypen werden für die Speicherung von Ganzzahlen, Dezimalzahlen und anderen Zahlformaten verwendet.
- **INTEGER** / **INT**: Ganze Zahlen, häufig für IDs oder Zählungen verwendet.
- **FLOAT**: Gleitkommazahlen mit einfacher Genauigkeit, um Bruchzahlen darzustellen.
- **DECIMAL(p, s)** / **NUMERIC(p, s)**: Dezimalzahlen mit festgelegter Präzision `p` (Gesamtzahl der Stellen) und Skala `s` (Anzahl der Nachkommastellen), z. B. für Währungswerte.

# 3. Datum und Zeit Datentypen
Datum- und Zeit-Datentypen speichern Informationen über Zeitpunkte oder Zeitspannen.
- **DATE**: Speichert nur das Datum (Jahr, Monat, Tag), z. B. `2024-10-30`.
- **TIME**: Speichert nur die Uhrzeit (Stunde, Minute, Sekunde).
- **DATETIME** / **TIMESTAMP**: Kombiniert Datum und Uhrzeit, häufig für Zeitstempel verwendet, z. B. bei der Erstellung oder Aktualisierung von Datensätzen.

# 4. Boolean Datentypen
Der **BOOLEAN**-Datentyp speichert Wahrheitswerte (`TRUE` oder `FALSE`). Einige Datenbanken speichern `BOOLEAN`-Werte als `0` (falsch) oder `1` (wahr), obwohl der SQL-Standard `TRUE` und `FALSE` vorsieht.

# 5. Spezielle Datentypen
SQL bietet auch spezielle Datentypen für spezifische Anforderungen:
- **BLOB (Binary Large Object)**: Speichert große Binärdaten, z. B. Bilder oder Dateien, die nicht als Text dargestellt werden.
- **UUID (Universally Unique Identifier)**: Ein 128-Bit-Wert, der für globale Eindeutigkeit sorgt und oft für IDs verwendet wird.
- **ARRAY**: Ein Datentyp zur Speicherung von Arrays (Listen) von Werten. Wird nur in einigen SQL-Dialekten unterstützt.

# Übersicht der wichtigsten SQL-Datentypen

| Kategorie     | Datentyp      | Beschreibung                              |
| ------------- | ------------- | ----------------------------------------- |
| Zeichenfolgen | CHAR(n)       | Feste Länge `n`, für kurze Texte geeignet |
|               | VARCHAR(n)    | Variable Länge `n`, für längere Texte     |
|               | TEXT          | Sehr lange Texte                          |
| Numerisch     | INTEGER       | Ganze Zahlen                              |
|               | FLOAT         | Gleitkommazahlen                          |
|               | DECIMAL(p, s) | Dezimalzahlen mit festgelegter Präzision  |
| Datum & Zeit  | DATE          | Datum (Jahr, Monat, Tag)                  |
|               | TIME          | Uhrzeit                                   |
|               | DATETIME      | Datum und Uhrzeit                         |
| Boolean       | BOOLEAN       | Wahrheitswert (`TRUE` / `FALSE`)          |
| Speziell      | BLOB          | Binäre Daten, z. B. Bilder                |
|               | UUID          | Universell eindeutige Identifikation      |
