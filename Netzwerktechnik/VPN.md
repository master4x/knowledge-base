# VPN
VPN (engl. „Virtual Private Network“) bezeichnet eine *getunnelte Netzwerkverbindung* mit *optionaler Verschlüsslung* (je nach [[Protokoll]]) in ein anderes Netzwerk, welche von außen nicht einsehbar ist.

![](../_Medien/VPN.png)

Das *konventionelle VPN* bezeichnet ein *virtuelles privates Netzwerk*. Virtuell in dem Sinne, dass es sich nicht um eine eigene physische Verbindung handelt, sondern um ein *bestehendes Kommunikationsnetz*, das als Transportmedium verwendet wird. Das VPN dient dazu, Teilnehmer des bestehenden Kommunikationsnetzes *an ein anderes Netz zu binden*, wobei es mehrere Typen gibt.

Die eingesetzte *VPN-Software stellt den Eingang zum VPN-Tunnel* üblicherweise als zusätzlichen *virtuellen Netzwerkadapter* (nicht als Hardware vorhandenen) bereit. Dabei sind VPN-Teilnehmer bei bestehender Verbindung *nie in mehreren Netzwerken gleichzeitig aktiv*. Angesprochene *VPN-Sever sind reine NAT-Router*, welche Inhalte (im Gegensatz zu Proxy-Servern) nur „weiterleiten“ und *nicht einsehen, speichern oder verändern* können.

## Anwendung
Vorteile vom Einsatz einer VPN für Privatpersonen ist zumeist die Möglichkeit *seine IP-Adresse und seinen Browserverlauf zu verschleiern*. Durch die Anonymisierung der eigenen IP-Adresse können per DNS-Sperren oder *Geoblocking-Sperren umgangen* werden. Außerdem wird *Tracking* des Nutzers durch Werbedienste oder Strafverfolgungsbehörden erschwert (ist aber z.B. durch Browser-Fingerprinting weiterhin möglich). In der Geschäftswelt wird hingegen der Aspekt der *sicheren Verbindung in geschützte Netzwerke* mit dessen Inhalten wie Fileservern geschätzt.

Es gibt jedoch bei der Anwendung von VPN einige Probleme und Einschränkungen. So unterstützen nicht alle Geräte und Systeme Verbindungen mit VPNs. Auch wenn verschlüsselte VPN-Tunnel als sicher erachtet werden, *schützten VPN-Verbindungen nicht vor allen Gefahren im Internet*. Es ist hervorzuheben, dass *kostenlose VPN-Anbieter nicht vertrauenswürdig sind*. Wie bereits erwähnt gibt es viele Wege einen Nutzer trotzdem zu tracken, was den Anonymitätsaspekt beschränkt. Ein Nebeneffekt der Verbindung können die *Reduzierung der Internetgeschwindigkeit oder eine erhöhte Latenz sein*. Die betriebene VPN-Software und der VPN-Sever bilden *attraktive Ziele für Angriffe* auf kritische Infrastruktur und können selbst über Sicherheitslücken verfügen.

## Typen
### End-to-Site VPN
End-to-Site-VPN beschreibt ein VPN-Szenario, bei dem Heimarbeitsplätze oder mobile Benutzer (Außendienst) in ein Unternehmensnetzwerk eingebunden werden. Der externe Mitarbeiter soll so arbeiten, wie wenn er sich im Netzwerk des Unternehmens befindet. Man bezeichnet dieses VPN-Szenario auch als Remote-Access-VPN oder spricht vom Road-Warrior-Szenario

![](../_Medien/End-to-Site_VPN.png)

### Site-to-Site VPN
Site-to-Site-VPN und LAN-to-LAN-VPN, oder auch Branch-Office-VPN genannt, sind VPN-Szenarien, um mehrere lokale Netzwerke von Außenstellen oder Niederlassungen zu einem virtuellen Netzwerk über ein öffentliches Netz zusammenzuschalten.

![](../_Medien/Site-to-Site_VPN.png)

### End-to-End VPN
End-to-End-VPN beschreibt ein VPN-Szenario, bei dem ein Client auf einen anderen Client in einem entfernten Netzwerk zugreift. Hierbei deckt der VPN-Tunnel die gesamte Verbindung zwischen zwei Hosts ab. 

![](../_Medien/End-to-End_VPN.png)

Auf beiden Seiten muss eine entsprechende VPN-Software installiert und konfiguriert sein. In der der Regel ist der Verbindungsaufbau nur durch die Unterstützung einer zwischengeschalteten Station möglich. Das bedeutet, eine direkter Verbindungsaufbau von Host zu Host ist nicht möglich. Stattdessen bauen beide Seiten eine Verbindung zu einem Gateway auf, dass die beiden Verbindungen dann zusammenschalten.
