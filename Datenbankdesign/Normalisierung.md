# Normalisierung
## Erste Normalform
Eine Relation liegt in der ersten Normalform (kurz 1.NF) vor, wenn alle Attributwerte atomar vorliegen.

**Hinweis**: Atomar ist ein Attribut(-wert), wenn nicht weiter zerteilt werden kann.

## Zweite Normalform
Eine Relation liegt in der zweiten Normalform (kurz 2.NF) vor, wenn sie in der ersten Normalform vorliegt und jedes Nicht-Schlüsselattribut vollfunktional vom gesamten Primärschlüssel abhängig ist.

**Hinweis**: Funktionale Abhängigkeiten basieren auf n:m-Verknüpfungen.
**Zusammenfassung**: Die zweite Normalform erfordert eine Trennung der Sachverhalte mit eindeutigen Schlüsseln.

## Dritte Normalform
Eine Relation liegt in der dritten Normalform (kurz 3.NF) vor, wenn die in der zweiten Normalform vorliegt und keine transitiven Abhängigkeiten bestehen.

**Hinweis**: Transitive Abhängigkeiten basieren auf der Trennung aller übrigen Relationen.
**Zusammenfassung**: Die dritte Normalform prüft die Abhängigkeiten der Nicht-Schlüsselattribute untereinander.
