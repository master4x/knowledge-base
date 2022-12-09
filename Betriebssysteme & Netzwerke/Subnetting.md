Subnetting ist die Bildung von Teilnetzen (bzw. Subnetzen) innerhalb eines privaten Adressbereichs. Ein Subnetz fasst *mehrere gleich große IP-Adressbereiche mit je einer Subnetzmaske zusammen*. Subnetting trennt die Teilnetzte *logisch* (auf der 3. OSI-Schicht) voneinander, was Routing zwischen den Subnetzen nötig macht (mit min. L3-Switch). Bei betreib eines DHCP-Servers im Netzwerk, muss ein *DHCP-Relay* eingesetzt werden. Die Aufteilung der Netze ist *von außerhalb weder erkennbar*, noch einem Subnetz zuordbar. Als Vorteil von Subnetting gehen die Trennung von Zugriffsrechten, die *geringere Netzlast und kleinere Broadcasts* innerhalb des Netzwerks. Das erste Subnetz hat immer die Gesamtnetz-ID als Subnetz-ID

# Berechnung über Anzahl der Subnetze
**Beispiel**: 3 Subnetzte in einem privaten Klasse-C-Netzwerk mit der Netz-ID `192.168.0.0/24`

1. **Leihbits berechnen**
   Die Anzahl der Leihbits lässt sich über die Formel `2ⁿ ≥ S` bestimmen.
   `S` steht dabei für die Anzahl der Subnetze und `n` für die Anzahl der Leihbits.
```
2ⁿ ≥ S     ⇨     2² = 4 > 3     ⇨     2 Leihbits
```
2. **Subnetzmaske berechnen**
```
Klasse C:  1111 1111.1111 1111.1111 1111.0000 0000 /24 ⇨ 255.255.255.0
⇩
Subnetz 1: 1111 1111.1111 1111.1111 1111.0000 0000 /26 ⇨ 255.255.255.224
Subnetz 2: 1111 1111.1111 1111.1111 1111.0100 0000 /26 ⇨ 255.255.255.224
Subnetz 3: ...
```
3. **Hostanzahl berechnen**
   Die Größe der Subnetze lässt sich über die Formel `2ᵐ = G` bestimmen.
   `G` steht dabei für die Anzahl Subnetzgröße und `m` für die Anzahl der verbleibenden Bits.
   Um die Hostanzahl `H` zu bestimmen wird folgende Formel verwendet: `2ᵐ - 2 = H`.
```
2ᵐ = G     ⇨     2⁶ – 2 = 64     ⇨     64 – 2 = 62 (Hosts)
```
4. **Subnetzübersicht aufstellen**
 | Name        | Subnetz-ID    | Hostbereich                   | Broadcast     |
 | ----------- | ------------- | ----------------------------- | ------------- |
 | Buchhaltung | 192.168.0.0   | 192.168.0.1 - 192.168.0.62    | 192.168.0.63  |
 | Vertrieb    | 192.168.0.64  | 192.168.0.65 – 192.168.0.126  | 192.168.0.127 |
 | Support     | 192.168.0.128 | 192.168.0.129 – 192.168.0.190 | 292.168.0.191 |
 