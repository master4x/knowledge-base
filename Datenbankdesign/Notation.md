Eine **Notation** in der Informatik und Datenmodellierung beschreibt die Art und Weise, wie Informationen oder Modelle grafisch oder symbolisch dargestellt werden. Notationen werden verwendet, um Konzepte, Beziehungen und Strukturen klar und präzise abzubilden, sodass sie leicht verständlich und interpretierbar sind. Verschiedene Notationen werden in unterschiedlichen Kontexten eingesetzt, wie etwa in der Datenbankmodellierung, Softwareentwicklung oder Prozessmodellierung.

# Chen-Notation
Die **Chen-Notation** wurde von Peter Chen in den 1970er Jahren entwickelt und ist eine der ersten und am weitesten verbreiteten Notationen zur Modellierung von Datenbanken. In der Chen-Notation werden Entitäten, Attribute und Beziehungen zwischen Entitäten grafisch dargestellt.

### Hauptbestandteile der Chen-Notation
1. **Entitäten**:
   - Eine **Entität** repräsentiert ein Objekt in der Datenbank.
   - In der Chen-Notation werden Entitäten als **Rechtecke** dargestellt.
2. **Attribute**:
   - Ein **Attribut** beschreibt eine Eigenschaft oder ein Merkmal einer Entität.
   - Attribute werden als **Ellipsen** dargestellt und durch eine Linie mit der entsprechenden Entität verbunden.
	1. **Schlüsselattribute**:
	   - Ein **Schlüsselattribut** ist ein Attribut, das eine Entität eindeutig identifiziert
	   - In der Chen-Notation wird das Schlüsselattribut als **unterstrichenes Attribut** dargestellt.
3. **Beziehungen**:
   - Eine **Beziehung** stellt die Verbindung zwischen zwei oder mehr Entitäten dar.
   - Beziehungen werden als **Rauten** dargestellt und sind durch Linien mit den beteiligten Entitäten verbunden.
4. **Kardinalitäten**:
   - Kardinalitäten geben die Anzahl der Entitäten an, die an einer Beziehung beteiligt sind, z. B. 1:1, 1:n oder n:m. 
   - In der Chen-Notation werden Kardinalitäten neben den Linien dargestellt, die die Entitäten mit der Beziehung verbinden.

| Operator      | Beziehungsart                        | Kardinalitäten |
| ------------- | ------------------------------------ | -------------- |
| 1 *(0 bis ∞)* | einfache Beziehung *(muss)*          | 1 (eindeutig)  |
| c             | mögliche Beziehung *(kann)*          | 0 oder 1       |
| m, n          | mehrfache Beziehung *(muss)*         | min. 1         |
| mc, nc        | mehrfach mögliche Beziehung *(kann)* | min. 0         |

#### Abweichungen von der Chen-Notation

##### Einführung von binären Operatoren
Zur Abgrenzung von Zuständen, welche einen einfach-optionale Beziehung haben, kann der Operator `c` verwendet werden. Dieser kann ebenfalls in Kombination mit einer Mehrfachbeziehung vorkommen: `mc`.

##### Abgrenzung von Mehrfachbeziehungen
Da die Kardinalität `m:m` keine Aussage über die Komplexität trifft, kann angenommen werden, dass der Wert `m = m` ist. Aus diesem Grund kann als weiterer Parameter `n` verwendet werden.

## Beispiel

![](../_Medien/ERD_Beispiel.png)
Als standardisierte Leserichtung gilt von *links nach rechts* und von *oben nach unten*.
**Beispiel:** Ein Fahrzeug belegt eine oder keine Garage. 

# Weitere Notationen

## Crow’s Foot Notation
Diese kompakte Darstellung verwendet „Füße“ an den Linien, um die Kardinalitäten anzuzeigen. Sie wird häufig in modernen Datenmodellierungswerkzeugen verwendet.

## IE (Information Engineering) Notation
Diese Notation ähnelt der Crow’s Foot Notation, hat aber leicht abweichende Darstellungen für Beziehungen und Kardinalitäten.

| Notation          | Darstellung von Entitäten und Beziehungen                 |
| ----------------- | --------------------------------------------------------- |
| **Chen**          | Entitäten als Rechtecke, Attribute als separate Ellipsen  |
| **Modified Chen** | Attribute direkt in den Entitäten, Beziehungen als Linien |
| **Crow’s Foot**   | Entitäten als Rechtecke, Kardinalitäten als „Füße“        |
| **IE Notation**   | Ähnlich zu Crow’s Foot, aber mit leicht anderen Symbolen  |
