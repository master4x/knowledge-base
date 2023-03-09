# Relationenmodell
Wir verwenden eine relationale Datenbank und überführen das ER-Modell daher in ein relationales Datenmodell. Für die spätere Datenbank muss das konzeptionelle Datenmodell stattdessen in ein hierzu passendes logisches Datenmodell übersetzt werden. In einer relationalen Datenbank werden die Daten in Form von Tabellen gespeichert. Das Relationenmodell beschreibt nun, welche Tabellen angelegt werden müssen, wie diese aufgebaut sind und wie sie miteinander verbunden sind.

| ER-Modell    | Relationenmodell |
|--------------|------------------|
| Entitätstyp  | Relation         |
| Entität      | Tupel            |
| Attribut     | Attribut         |
| Attributwert | Attributwert     |

Die Relationen lassen sich entweder in Tabellenschreibweise oder im Relationenschema notieren. Die Beziehungen im klassischen Sinne werden aufgelöst und über Primär- und Fremdschlüssel abgebildet. Der Primärschlüssel wird dabei unterstrichen und er Fremdschlüssel entweder unterstrichelt oder durch einen hochzeigenden Pfeil (↑) vor dem Attributnamen maskiert.

**Relationenschema**:
- Kunde(kundeID, name, vorname)

**Tabelle**: Kunde
| kundeID | name       | vorname |
|---------|------------|---------|
| 1       | Mustermann | Max     |
| …       | …          | …       |

## Zwischenrelationen
Besteht zwischen zwei Entitätstypen ein n:m-Beziehungstyp beziehungsweise eine Variante mit dem Buchstaben `c` (`m:nc`,  `mc:nc`), wird eine neue Relation angelegt. Diese besteht aus zwei Attributen – den Primärschlüsseln der aus den beiden verbundenen Entitätstypen hervorgegangenen Relationen. Gleichzeitig fungiert jedes der beiden Attribute als Fremdschlüssel. Im Namen der Relation sollten die Namen der Ursprungsentitätstypen vorkommen, wobei diese durch einen Zusatz, den Namen der Beziehung oder durch eine Zahl bzw. ein Sonderzeichen getrennt werden.

**Beispiele**:
- KundeZuBestellung(…)
- KundeTaetigtBestellung(…)
- Kunde2Bestellung(…)
- Kunde_Bestellung(…)