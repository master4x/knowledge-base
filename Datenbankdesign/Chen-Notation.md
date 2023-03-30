# Modifizierte Chen-Notation
Die Modifizierte Chen-Notation (engl. „Modified Chen Notation“, MC-Notation) ist eine *Erweiterung* der Chen-Notation, bei der die Aussage „*kein oder ein Element*“ mit dem Buchstaben c („choice“), und die Aussage „*ein oder mehr Element(e)*“ mit dem Buchstaben m („must“) angegeben wird.

| Abkürzung     | Beziehungsart                      | Anzahl Entitäten |
| ------------- | ---------------------------------- | ---------------- |
| 1 *(0 bis ∞)*   | einfache Beziehung *(muss)*          | 1 (eindeutig)    |
| c             | mögliche Beziehung *(kann)*          | 0 oder 1         |
| m, n          | mehrfache Beziehung *(muss)*         | min. 1           |
| mc, nc        | mehrfach mögliche Beziehung *(kann)* | min. 0           |

Die Kombination m:m (*mindestens 1* zu *mindestens 1*) unterscheidet sich je nach Dialekt von der
erweiterten Hilfskombination `m:n` (*mindestens 1* zu *mindestens 1*), da die Platzhalter als selbes
Element interpretiert werden können.

![](../_Medien/ERD_Beispiel.png)
Als standardisierte Leserichtung gilt von *links nach rechts* und von *oben nach unten*.
**Beipiel:** Ein Fahrzeug belegt eine oder keine Garage. 
