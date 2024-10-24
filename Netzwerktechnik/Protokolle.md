Ein Netzwerkprotokoll ist ein Kommunikationsprotokoll für den Austausch von Daten Computern bzw. Prozessen, die in einem Netzwerk miteinander verbunden sind. Ein Netzwerkprotokoll definiert einen Regelsatz zum Kommunikationsablauf (Syntax) und dem Kommunikationsverhalten (Semantik).

| Name    | Bezeichnung                       | Anwendung                   | Port(s)         |
| ------- | --------------------------------- | --------------------------- | --------------- |
| TCP     | Transmission Control Protocol     | Sicherer Paketversand       | 0-1023          |
| UDP     | User Datagram Protocol            | Schneller Paketversand      | 0-1023          |
| ICMP    | Internet Control Message Protocol | Ping-Anfragen               | 1               |
| DNS     | Domain Name System                | Namensauflösung             | 53              |
| ARP     | Address Resolution Protocol       | Zuordnung MAC zu IP         | -               |
| HTTP(S) | Hyper-Text Transfer Protocol      | Webseitenaufruf             | 80, 8080, (443) |
| FTP     | File Transfer Protocol            | Dateiübertragung            | 21              |
| POP3    | Post Office Protocol Version 3    | E-Mail: Empfang             | 110, 995        |
| SMTP    | Simple Mail Transfer Protocol     | E-Mail: Versand             | 25, 465         |
| IMAP    | Internet Message Access Protocol  | E-Mail: Empfang (erweitert) | 143, 993        |
| SMB     | WIP                               |                             |                 |
| NFS     | WIP                               |                             |                 |
| DCHP    | WIP                               |                             |                 |
| SSH     | WIP                               |                             |                 |

# ARP
Das ARP-Protokoll sucht innerhalb eines privaten Netzwerks die MAC-Adresse zu einer bekannten IP-Adresse. Das Protokoll arbeitet auf der 3. OSI-Schicht.

1. **Anfragesteller**: „Who has X?“ Abfrage *([[Übertragungsmethoden#Broadcast|Broadcast]])*
2. **Inhaber**: Response, mit der MAX-Adresse *([[Übertragungsmethoden#Unicast|Unicast]])*
