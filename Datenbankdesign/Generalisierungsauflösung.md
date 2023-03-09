# Generalisierungsauflösung
## Hausklassenmodell
Beim Hausklassenmodell wird *für jeden Entitätstyp eine Relation erzeugt, welche alle Attribute der Oberklassen beinhaltet*. Jede Instanz ist daher komplett und von anderen unabhängig, dies *erspart Redundanzen erschwert aber die Suche*, da mehrere Tabellen durchsucht werden müssen, z.B. bei der Suche nach der Person mit der ID 5. Die Basisklasse kann hierbei entfallen.

**Beispiel**:
- Person(id, name, straße, ort)
- Student(id, name, straße, ort, dat)
- Dozent(id, name, straße, ort, fach)

*Wird ein Student angelegt, so werden die Eigenschaften nur in die Studententabelle eingetragen.*

## Volle Redundanz
Bei der vollen Redundanz werden die Relationen *wie beim Hausklassenmodell* angelegt, beim Abspeichern von Daten werden diese *jedoch in alle Relationen* eingetragen. Dies hat Vorteile bei der Abfrage der Daten, allerdings müssen bei Änderungen diese u.U. an mehreren Stellen durchgeführt werden, was *Inkonsistenzen* zur Folge haben kann.

**Beispiel**:
- Person(id, name, straße, ort)
- Student(id, name, straße, ort, dat)
- Dozent(id, name, straße, ort, fach)

*Wird ein Student angelegt, so werden die Eigenschaften komplett in die Person und Studententabelle eingetragen.*

## Partitionierungsmodell
Beim Partitionierungsmodell werden *nur die (auf der Vererbungsstufe) neu hinzukommenden Attribute mit in die Relationen aufgenommen sowie der Primärschlüssel*. Soll eine Person in die Datenbank eingetragen werden, so werden die Attribute auf die Relationen aufgeteilt. Dadurch entsteht ein *erhöhter Aufwand*, wenn alle Eigenschaften einer Person abgefragt werden sollen, da hierzu in verschiedenen Relationen nachgeschaut werden muss – es kommt *ohne Redundanz* aus.

**Beispiel**:
- Person(id, name, straße, ort)
- Student(id, dat)
- Dozent(id, fach)

*Wird ein Student angelegt, so werden die Eigenschaften zur Person in die Personentabelle eingetragen, die zusätzlichen Informationen werden in die Studententabelle eingetragen.*

## Überrelation

Alle Datensätze werden hier, mit ihren Attributen, *in einer Relation* abgelegt, was die *Nachteile der bisherigen Lösungen beseitigt*. Zusätzlich wird jedoch noch ein Attribut "Typ" mit in die Relation aufgenommen, was eine Zuordnung des Entitätstyps ermöglicht. Nachteilig wirkt sich hier aus, *dass alle Attribute in einer Relation* landen, was bei vielen Attributen zu *Unübersichtlichkeit* führen kann. Attribute die nicht zum jeweiligen Typ gehören werden mit null belegt. Der Benutzer muss immer wissen, welche Attribute zu welchem Typ gehören.

**Beispiel**:
- Person(id, typ, name, straße, ort, dat, fach)

*Beim Anlegen eines Studenten wird das Feld „Fach“ mit* null *belegt und im Feld „Typ“ der Typ „Student“ hinterlegt.*
