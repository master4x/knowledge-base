# Firewall
Eine Firewall ist ein Sicherungssystem, das ein Rechnernetz oder einen einzelnen Computer *vor
unerwünschten Netzwerkzugriffen schützt*. Mit einer Firewall lässt sich der kommende und gehende Datenverkehr *kontrollieren, protokollieren, sperren und freigeben*.

Die Regeln für die Firewall werden in der „Access Control List“ (kurz ACL) definiert. *Die Reihenfolge der Regelsätze ist relevant* für die Ausführung. Die erste Regel, die für ein Datenpaket greift, wird angewendet – weitere Regeln werden in solchen Szenarien nicht beachtet.

| Erlaubnis | Quelladresse  | Protokoll | Zieladresse  | Port |
|-----------|---------------|-----------|--------------|------|
| ALLOW     | 161.72.160.27 | TCP       | 192.168.0.17 | 80   |
| ALLOW     | 161.72.160.20 | UDP       | ANY          | 2102 |
| DENY      | ANY           | ANY       | ANY          | ANY  |

Beispiel für eine portbasierte Regel (auch Portfreigabe) je nach Protokoll:

| Erlaubnis | Quelladresse | Protokoll | Zieladresse | Port |
|-----------|--------------|-----------|-------------|------|
| ALLOW     | ANY          | TCP       | ANY         | 22   |
| ALLOW     | ANY          | UDP       | ANY         | 22   |

## Hostbasierte Firewall
Die hostbasierte (engl. „host basted“) Firewall ist ein Softwareprodukt, welches nur den Client mit der entsprechenden Installation schützt.

![](../_Medien/Hostbasierte_Firewall.png)

## Netzwerkbasierte Firewall
Die netzwerkbasierte (engl. „network based“) Firewall kann eine Software- oder Hardwarelösung sein, welche das gesamte Netzwerk vor externen Zugriffen schützt.

![](../_Medien/Netzwerkbasierte_Firewall.png)

## DMZ
Die Abkürzung DMZ steht für „demilitarisierte Zone“ und bezeichnet einen *speziell kontrollierten Netzwerkteil*, der sich *zwischen dem externen* und dem internen Netz befindet. Es stellt eine Art Pufferzone dar, die die Netze durch strenge Kommunikationsregeln und Firewalls voneinander trennt.

In der demilitarisierten Zone befinden sich Server wie *Webserver, Mailserver, Authentication-Server oder Anwendungs-Gateways*. *Nur diese sind für User aus dem Internet erreichbar*. Durch die Trennung der DMZ vom internen Netz ist kein Zugriff für externe Anwender auf interne Ressourcen möglich. Das private Netzwerk bleibt vor *Angriffen aus dem Internet* oder vor Überlastung durch Internetanfragen geschützt. Die demilitarisierte Zone kann durch eine oder mehrere Firewalls von den angrenzenden Netzwerken separiert sein.

![](../_Medien/DMZ_Übersicht.png)

### 1-Firewall DMZ
Vorteile einer 1-Firewall-DMZ sind der geringere Konfigurations- und Administrationsaufwand durch die günstige Anschaffung nur eines Geräts (Router). Nachteile ist der Wegfall der Sicherungseinheit durch die fehlende zweite Firewall.

![](../_Medien/1_Firewall_DMZ.png)

### 2-Firewall-DMZ
Die 2-Firewall-DMZ ist der DMZ-Standard für größere Netzwerke. Die Besonderheit liegt in der zweifachen Filterung des Netzwerkverkehrs furch Firewalls, vor und nach der DMZ. Nachteil der Konfiguration im Vergleich zur 1-Firewall-DMZ liegt im erhöhten Preis und Administrationsaufwand.

![](../_Medien/2_Firewall_DMZ.png)

In beiden Firewall-Routern müssen *statische Routen* konfiguriert werden, damit die eingehenden Datenpakete der Verbindungen an die richtigen Hosts im LAN zugestellt werden können.
