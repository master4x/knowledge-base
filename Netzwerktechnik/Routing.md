# Routing
Ein [[Komponenten#Router|Router]] hat immer nur Informationen über unmittelbar verbundene Netzwerke. Um ein Datenpacket in ein unbekanntes Netzwerk zu transportieren, muss der Router entscheiden, über welche Schnittstelle das Packet geleiten werden muss, damit es zum Ziel gelangt.

## Statisches Routing
Beim statischen Routing werden die Routen manuell in Weiterleitungstabellen eingetragen. Dem Router liegen nur diese *Routen* als Datengrundlage vor.

## Dynamisches Routing
Beim dynamischen Routing verwaltet der Router die Weiterleitungstabelle und trägt im laufenden Betrieb neu ermittelte Routen automatisch ein.

## Weiterleitungstabelle
In der Weiterleitungstabelle, auch Routingtabelle, sind die logischen Verknüpfungen für die Adresszuordnung gespeichert. Hier werden den Adaptern die passenden Adressen, Netzwerke, Broadcasts und Routen zugeordnet.

| Ziel        | Subnetzmaske    | Gateway     | Schnittstelle | Metrik |
|-------------|-----------------|-------------|---------------| -------|
| 192.168.3.1 | 255.255.255.255 | 127.0.0.1   | 127.0.0.1     | 25     |
| 192.168.2.1 | 255.255.255.255 | 127.0.0.1   | 127.0.0.1     | 25     |
| 192.168.3.0 | 255.255.255.0   | 192.168.3.1 | 192.168.3.1   | 45     |
| 192.168.2.0 | 255.255.255.0   | 192.168.2.1 | 192.168.2.1   | 45     |
| 127.0.0.1   | 255.0.0.0       | 127.0.0.1   | 127.0.0.1     | 2      |
| 172.16.3.0  | 255.255.0.0     | 192.168.3.2 | 192.168.3.1   | 3      |

**Zieladresse**: Die IP-Adresse des Zielnetzwerks. 
**Subnetzmaske**: Die Subnetzmaske des Zielnetzwerks. 
**Gateway**: Die IP-Adresse des *Gateways des (nächsten) [[Komponenten#Router|Routers]]*. 
**Schnittstelle**: Die IP-Adresse der *ausgehenden Netzwerkkarte* des [[Komponenten#Router|Routers]].
**Metrik**: Die Anzahl der Hops für die Verbindung dieser Route. (siehe [[Routing#Metrik|Metrik]])

### Metrik
Unter Metrik versteht man einen numerischen Wert, der einer Route zugeordnet ist. Ein niedriger Wert führt dazu, dass die Route vom System bevorzugt wird, falls zwei Routen zu demselben Ziel existieren. Metriken können etwa Kosten darstellen oder sie weisen auf Faktoren wie Bandbreite, Geschwindigkeit, Zuverlässigkeit, Pfadlänge oder Verzögerung von Routen hin.
