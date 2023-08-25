# Vererbung
Siehe [[Spezielle Beziehungen#Generalisierung (is-a)|Generalisierung (is-a)]] unter [[Spezielle Beziehungen]]
## Partitionierungsmodell
Beim Partitionierungsmodell werden *nur die (auf der Vererbungsstufe) neu hinzukommenden Attribute mit in die Relationen aufgenommen sowie der Primärschlüssel*. Soll eine Person in die Datenbank eingetragen werden, so werden die Attribute auf die Relationen aufgeteilt. Dadurch entsteht ein *erhöhter Aufwand*, wenn alle Eigenschaften einer Person abgefragt werden sollen, da hierzu in verschiedenen Relationen nachgeschaut werden muss – es kommt *ohne Redundanz* aus.

**Beispiel**:
- Person(<u>id</u>, name, straße, ort)
- Student(<u>id</u>, dat)
- Dozent(<u>id</u>, fach)

*Wird ein Student angelegt, so werden die Eigenschaften zur Person in die Personentabelle eingetragen, die zusätzlichen Informationen werden in die Studententabelle eingetragen.*

## Überrelation/Supertyp
Alle Datensätze werden hier, mit ihren Attributen, *in einer Relation* abgelegt, was die *Nachteile der bisherigen Lösungen beseitigt*. Zusätzlich wird jedoch noch ein Attribut "Typ" mit in die Relation aufgenommen, was eine Zuordnung des Entitätstyps ermöglicht. Nachteilig wirkt sich hier aus, *dass alle Attribute in einer Relation* landen, was bei vielen Attributen zu *Unübersichtlichkeit* führen kann. Attribute die nicht zum jeweiligen Typ gehören werden mit null belegt. Der Benutzer muss immer wissen, welche Attribute zu welchem Typ gehören.

**Beispiel**:
- Person(<u>id</u>, typ, name, straße, ort, dat, fach)

*Beim Anlegen eines Studenten wird das Feld „Fach“ mit __null__ belegt und im Feld „Typ“ der Typ „Student“ hinterlegt.*

## Hausklassenmodell
Beim Hausklassenmodell wird *für jeden Entitätstyp eine Relation erzeugt, welche alle Attribute der Oberklassen beinhaltet*. Jede Instanz ist daher komplett und von anderen unabhängig, dies *erspart Redundanzen erschwert aber die Suche*, da mehrere Tabellen durchsucht werden müssen, z.B. bei der Suche nach der Person mit der ID 5. Die Basisklasse kann hierbei entfallen.

**Beispiel**:
- Person(<u>id</u>, name, straße, ort) - optional
- Student(<u>id</u>, name, straße, ort, dat)
- Dozent(<u>id</u>, name, straße, ort, fach)

*Wird ein Student angelegt, so werden die Eigenschaften nur in die Studententabelle eingetragen.*

## Volle Redundanz
Bei der vollen [[Anomalien#Redundanz|Redundanz]] werden die Relationen *wie beim Hausklassenmodell* angelegt, beim Abspeichern von Daten werden diese *jedoch in alle Relationen* eingetragen. Dies hat Vorteile bei der Abfrage der Daten, allerdings müssen bei Änderungen diese u.U. an mehreren Stellen durchgeführt werden, was *Inkonsistenzen* zur Folge haben kann.

**Beispiel**:
- Person(<u>id</u>, name, straße, ort, dat, fach)
- Student(<u>id</u>, name, straße, ort, dat)
- Dozent(<u>id</u>, name, straße, ort, fach)

*Wird ein Student angelegt, so werden die Eigenschaften komplett in die Person und Studententabelle eingetragen.*
