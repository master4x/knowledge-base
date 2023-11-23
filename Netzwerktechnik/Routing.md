Ein [[Komponenten#Router|Router]] hat immer nur Informationen über unmittelbar verbundene Netzwerke. Um ein Datenpaket in ein unbekanntes Netzwerk zu transportieren, muss der Router entscheiden, über welche Schnittstelle das Packet geleiten werden muss, damit es zum Ziel gelangt.

# Statisches Routing
Bei statischem Routing werden Routing-Einträge manuell von einem Netzwerkadministrator konfiguriert. Dies bedeutet, dass die Weiterleitungstabelle fest ist und sich nicht automatisch an Änderungen im Netzwerk anpasst. Es eignet sich gut für kleinere Netzwerke mit stabilen Topologien, erfordert jedoch regelmäßige manuelle Aktualisierungen bei Netzwerkänderungen.

## Weiterleitungstabelle
In der Weiterleitungstabelle, auch Routingtabelle, sind die logischen Verknüpfungen für die Adresszuordnung gespeichert. Hier werden den Adaptern die passenden Adressen, Netzwerke, Broadcasts und Routen zugeordnet.

| Ziel        | Subnetzmaske    | Gateway     | Schnittstelle | Metrik¹ |
|-------------|-----------------|-------------|---------------| --------|
| 192.168.3.1 | 255.255.255.255 | 127.0.0.1   | 127.0.0.1     | 25      |
| 192.168.2.1 | 255.255.255.255 | 127.0.0.1   | 127.0.0.1     | 25      |
| 192.168.3.0 | 255.255.255.0   | 192.168.3.1 | 192.168.3.1   | 45      |
| 192.168.2.0 | 255.255.255.0   | 192.168.2.1 | 192.168.2.1   | 45      |
| 127.0.0.1   | 255.0.0.0       | 127.0.0.1   | 127.0.0.1     | 2       |
| 172.16.3.0  | 255.255.0.0     | 192.168.3.2 | 192.168.3.1   | 3       |

¹Die Metrik ist eine Routeninformation, welche durch direkte Eingaben nicht veränderlich ist.

**Zieladresse**: Die IP-Adresse des Zielnetzwerks. 
**Subnetzmaske**: Die Subnetzmaske des Zielnetzwerks. 
**Gateway**: Die IP-Adresse des *Gateways des (nächsten) [[Komponenten#Router|Routers]]*. 
**Schnittstelle**: Die IP-Adresse der *ausgehenden Netzwerkkarte* des [[Komponenten#Router|Routers]].
**Metrik**: Die Anzahl der [[Routing#Hop|Hops]] für die Verbindung dieser Route. (siehe [[Routing#Metrik|Metrik]])

### Metrik
Unter Metrik versteht man einen numerischen Wert, der einer Route zugeordnet ist. Ein niedriger Wert führt dazu, dass die Route vom System bevorzugt wird, falls zwei Routen zu demselben Ziel existieren. Metriken können etwa Kosten darstellen oder sie weisen auf Faktoren wie Bandbreite, Geschwindigkeit, Zuverlässigkeit, Pfadlänge oder Verzögerung von Routen hin. 

### Hop
Als Hop bezeichnet man jegliche aktive Routing-Komponenten (z.B. [[Komponenten#Router|Router]] oder [[Komponenten#Layer3-Switch|L3-Switch]]) auf einer Paketroute. Man kann den ersten oder nächsten Knotenpunkt auch als *Next Hop* bezeichnen. 

# Dynamisches Routing
Im Gegensatz dazu verwendet dynamisches Routing Routing-Protokolle, um Routing-Informationen automatisch zwischen Routern auszutauschen. Die Weiterleitungstabelle wird kontinuierlich aktualisiert, um sich Änderungen in der Netzwerktopologie anzupassen. Dies ist ideal für größere und sich ändernde Netzwerke, da es die Skalierbarkeit erhöht und weniger manuelle Konfiguration erfordert.

## Autonomes System
Ein autonomes System (kurz AS) ist eine Netzwerkstruktur, in der Router nur die Netzwerke ihrer direkten Nachbarn kennen. Dies verbessert die Effizienz der Routing-Entscheidungen innerhalb des AS. Zur Verbindung und zum Datenaustausch zwischen verschiedenen autonomen Systemen werden Border-Router eingesetzt, insbesondere von Internet Service Providern (ISP) für das Interdomain Routing. AS ermöglichen die Organisation und das effiziente Routing von Datenverkehr in komplexen Netzwerken.

## Interne Routingprotokolle
### RIP
RIP (Routing Information Protocol) ist ein dynamisches Routingprotokoll, das den Distanz-Vektor-Algorithmus verwendet. Es wählt Wege basierend auf der Anzahl der Hops zwischen Quell- und Zielnetz aus und aktualisiert seine Routinginformationen alle 30 Sekunden. RIP ist einfach, unterstützt jedoch nur bis zu 15 Hops. Es gibt aktuelle Versionen wie RIPv2 und RIPnG für IPv6.

### OSPF
OSPF (Open Shortest Path First) ist ebenfalls ein dynamisches Routingprotokoll, das auf der Link State Database basiert. OSPF berechnet den besten Weg basierend auf Leitungskosten und verwendet Hello-Pakete, um Änderungen der Weiterleitungstabellen zu signalisieren. OSPF wird in einem Autonomen System (AS) eingesetzt und verwendet Border-Router, um zwischen verschiedenen AS zu vermitteln. Version 2 ist im RFC 2328 beschrieben, während Version 3 für IPv6 in RFC 2740 definiert ist.

## Load Balancing 
Die meisten Routingprotokolle ermöglichen ein sogenanntes Load Balancing, was bedeutet, dass alternative Wege zur Zieladresse verwendet werden können. Load Balancing heißt, dass bei zwei gleichwertigen Wegen (gleiche [[Routing#Metrik|Metrik]]) die Datenströme wechselseitig auf beide Wege verteilt werden.
