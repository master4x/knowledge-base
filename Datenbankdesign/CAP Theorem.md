Das CAP Theorem ist ein Konzept aus dem Bereich der Datenwissenschaft (verteilte Systeme). Es besagt, dass in einem verteilten System nur zwei der drei Eigenschaften gleichzeitig garantiert werden können:

# Bestandteile
## Consistency
Alle Knoten im System sehen die gleichen Daten zur gleichen Zeit. Dies bedeutet, dass wenn Daten in einem Teil des Systems geändert werden, diese Änderungen sofort und einheitlich in allen anderen Teilen des Systems reflektiert werden müssen.
## Availability
Das System reagiert stets auf Anfragen, auch wenn Teile des Systems fehlerhaft sein sollten. Mit anderen Worten, das System bleibt weiterhin ansprechbar und liefert Antworten, auch wenn einzelne Knoten oder Netzwerksegmente ausfallen.
## Partition Tolerance
Das System bleibt betriebsbereit, selbst wenn das Netzwerk zwischen den Knoten des Systems in mehrere Partitionen aufgeteilt wird, wodurch diese Partitionen nicht miteinander kommunizieren können.

# Beispiel an Datenbanken
Entwickler stehen oft vor der Entscheidung zwischen [[Datenbankmodelle#Relationale Datenbanken (SQL)|SQL]]- und [[Datenbankmodelle#Dokumentenorientierte Datenbanken (NoSQL)|NoSQL-Datenbanken]], insbesondere wenn es um die Gewährleistung von Konsistenz, Verfügbarkeit und Partitionstoleranz geht, wie im CAP-Theorem beschrieben. SQL-Datenbanken sind traditionelle relationale Datenbanken, während NoSQL-Datenbanken eine breite Palette von nicht-relationalen Datenbanken umfasst.

| Eigenschaft        | SQL-Datenbanken                                                       | NoSQL-Datenbanken                                                 |
| ------------------ | --------------------------------------------------------------------- | ----------------------------------------------------------------- |
| Konsistenz         | Hohe Konsistenz, da Transaktionen sofort aktualisiert werden.         | Möglicherweise geringere Konsistenz, da Kompromisse möglich sind. |
| Verfügbarkeit      | Hohe Verfügbarkeit, um stets auf Anfragen reagieren zu können.        | Hohe Verfügbarkeit auch bei Ausfällen oder Partitionen.           |
| Partitionstoleranz | Möglicherweise eingeschränkte Partitionstoleranz bei Netzwerkfehlern. | Hohe Partitionstoleranz, um weiterhin betriebsbereit zu bleiben.  |
