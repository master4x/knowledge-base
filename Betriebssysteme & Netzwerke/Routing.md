Ein Router hat immer nur Informationen über unmittelbar verbundene Netzwerke. Um ein Datenpacket in ein unbekanntes Netzwerk zu transportieren, muss der Router entscheiden, über welche Schnittstelle das Packet geleiten werden muss, damit es zum Ziel gelangt.

# Statisches Routing
Beim statischen Routing werden die Routen manuell in Weiterleitungstabellen eingetragen. Dem Router liegen nur diese *Routen* als Datengrundlage vor.

# Dynamisches Routing
Beim dynamischen Routing verwaltet der Router die Weiterleitungstabelle und trägt im laufenden Betrieb neu ermittelte Routen automatisch ein.

# Weiterleitungstabelle
| Ziel        | Netzmaske       | Nächstes Gateway | Über Schnittstelle |
|-------------|-----------------|------------------|--------------------|
| 192.168.3.1 | 255.255.255.255 | 127.0.0.1        | 127.0.0.1          |
| 192.168.2.1 | 255.255.255.255 | 127.0.0.1        | 127.0.0.1          |
| 192.168.3.0 | 255.255.255.0   | 192.168.3.1      | 192.168.3.1        |
| 192.168.2.0 | 255.255.255.0   | 192.168.2.1      | 192.168.2.1        |
| 127.0.0.1   | 255.0.0.0       | 127.0.0.1        | 127.0.0.1          |
| 172.16.3.0  | 255.255.0.0     | 192.168.3.2      | 192.168.3.1        |

**Zieladresse**: Die IP-Adresse des Zielnetzwerks. 
**Netzmaske**: Die Subnetzmaske des Zielnetzwerks. 
**Nächstes Gateway**: Die IP-Adresse des *Gateways des nächsten Routers*. 
**Über Schnittstelle**: Die IP-Adresse der *ausgehenden Netzwerkkarte* des Routers.
