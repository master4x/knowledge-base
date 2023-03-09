# Ports
Ports (TCP/UDP) sind primär die *Schnittstelle zwischen Anwendungen* in Netzwerken,  
wobei diese die Unterscheidung mehrere Verbindungen zwischen demselben Paar an Endpunkten ermöglichen. Eine IP-Adresse wird für die Kommunikation um einen spezifizierten Port ergänzt.

Ports sind ein direktes Einfallstor in Netzwerke, weshalb der Zustand von nicht essentiellen Ports geschlossen (`CLOSED`)ist. Andere mögliche Zustände sind offen (`OPEN`) oder mit Firewall: gefiltert (`FILTERED`). Um weitere Risiken zu vermeiden werden wichtige Wartungsports wie SSH (22) oft umgelegt.

| Bezeichnung           | Bereich       | Anwendung                                                         | Beispiel       |
| --------------------- | ------------- | ----------------------------------------------------------------- | -------------- |
| Standardisierte Ports | 1 – 1023      | Standardports für essentielle Dienste von Systemen und Netzwerken | 21: FTP        |
| Registrierte Ports    | 1024 – 49151  | Anwendungsports für bei der IANA registrierte Verwendungszwecke   | 1194: OpenVPN  |
| Dynamische Ports      | 49152 – 65535 | Freie Ports für die lokale Nutzung oder ausgehende Kommunikation  | 56721: Spotify |
