# Normalisierung
## Erste Normalform
Eine Relation liegt in der ersten Normalform (kurz 1.NF) vor, wenn alle Attributwerte atomar vorliegen.

**Hinweis**: Atomar ist ein Attribut(-wert), wenn es nicht weiter zerteilt werden kann.

## Zweite Normalform
Eine Relation liegt in der zweiten Normalform (kurz 2.NF) vor, wenn sie in der ersten Normalform vorliegt und jedes Nicht-Schlüsselattribut vollfunktional vom gesamten Primärschlüssel abhängig ist.

**Zusammenfassung**: Die zweite Normalform erfordert eine Trennung der Sachverhalte.
**Hinweis**: Funktionale Abhängigkeiten basieren in der Regel auf n:m-Verknüpfungen.

## Dritte Normalform
Eine Relation liegt in der dritten Normalform (kurz 3.NF) vor, wenn die in der zweiten Normalform vorliegt und keine transitiven Abhängigkeiten bestehen.

**Zusammenfassung**: Die dritte Normalformprüft die Abhängigkeiten der Nicht-Schlüsselattribute untereinander.
