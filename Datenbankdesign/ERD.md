# ERD
Ein „Entity-Relationship-Diagram“ (kurz ERD) bzw. „Entity-Relationship-Modell“ (kurz ERM) ist eine visuelle Darstellung verschiedener Entitäten innerhalb eines Systems mit ihrer Beziehung zueinander.

![](../_Medien/ERD.png)
## Konventionen
- **Entitätstypen** werden groß und im Singular geschrieben. 
- **Attribute** werden klein und eindeutig geschrieben. (Primärschlüssel unterstreichen) 
- **Beziehungen** werden klein und in Leserichtung geschrieben. 
- Keine Verwendung von Umlauten und Sonderzeichen.

## Modifizierte Chen-Notation
Die Modifizierte Chen-Notation (engl. „Modified Chen Notation“, MC-Notation) ist eine *Erweiterung der Chen-Notation*, bei der die Aussage „*kein oder ein Element*“ mit dem Buchstaben c („choice“), und die Aussage „*ein oder mehr Element(e)*“ mit dem Buchstaben m („must“) angegeben wird.

| Abkürzung     | Beziehungsart                        | Anzahl Entitäten |
| ------------- | ------------------------------------ | ---------------- |
| 1 *(0 bis ∞)* | einfache Beziehung *(muss)*          | 1 (eindeutig)    |
| c             | mögliche Beziehung *(kann)*          | 0 oder 1         |
| m, n          | mehrfache Beziehung *(muss)*         | größer/gleich 1  |
| mc            | mehrfach mögliche Beziehung *(kann)* | größer/gleich 0  |

Die Kombination m:m (*mindestens 1* zu *mindestens 1*) unterscheidet sich je nach Dialekt von der
erweiterten Hilfskombination `m:n` (*mindestens 1* zu *mindestens 1*), da die Platzhalter als selbes
Element interpretiert werden können.

![](../_Medien/ERD_Beispiel.png)
**Leserichtung (links-rechts)**:     Ein Fahrzeug belegt eine oder keine Garage. 
**Leserichtung (rechts-links)**:     Eine Garage wird von genau einem Fahrzeug belegt.
