# Netzwerklassen
Die Einteilung von IP-Adressen in Netzwerkklassen wurde mit der Einführung von [[Subnetzmaske#CIDR-Schreibweise|CIDR]] abgelöst. Sie hat heute fast keine praxisrelevante Bedeutung mehr, da die Größe eines Subnetzes nicht mehr nur aus der IP-Adresse abzuleiten ist, sondern zwingend die Angabe einer [[Subnetzmaske]] erforderlich ist.

| Klasse | Adressbereich               | Subnetzmaske  |
| ------ | --------------------------- | ------------- |
| A      | 0.0.0.0 – 126.255.255.255   | 255.0.0.0     |
| B      | 128.0.0.0 – 191.255.0.0     | 255.255.0.0   |
| C      | 192.0.0.0 – 223.255.255.0   | 255.255.255.0 |
| D      | 224.0.0.0 – 239.255.255.255 | (Multicast)   |
| E      | 240.0.0.0 – 255.255.255.255 | (Reserviert)  |

## Logische Einteilung
![[Netzwerkklassen.png]]

## Private Netzwerke

| Klasse | Adressbereich                 | Subnetzmaske  | 
|--------|-------------------------------|---------------| 
| A      | 10.0.0.0 – 10.255.255.255     | 255.0.0.0     | 
| B      | 172.16.0.0. – 172.31.255.255  | 255.255.0.0   | 
| C      | 192.168.0.0 – 192.168.255.255 | 255.255.255.0 |
