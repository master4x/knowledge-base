Subnetting ist die Bildung von Teilnetzen (bzw. Subnetzen) innerhalb eines privaten Adressbereichs. Ein Subnetz fasst *mehrere gleich große IP-Adressbereiche mit je einer Subnetzmaske zusammen*. Subnetting trennt die Teilnetzte *logisch* (auf der 3. OSI-Schicht) voneinander, was Routing zwischen den Subnetzen nötig macht (mit min. L3-Switch). Bei betreib eines DHCP-Servers im Netzwerk, muss ein *DHCP-Relay* eingesetzt werden. Die Aufteilung der Netze ist *von außerhalb weder erkennbar*, noch einem Subnetz zuordbar. Als Vorteil von Subnetting gehen die Trennung von Zugriffsrechten, die *geringere Netzlast und kleinere Broadcasts* innerhalb des Netzwerks. Das erste Subnetz hat immer die Gesamtnetz-ID als Subnetz-ID

# Berechnung über Anzahl der Subnetze
**Beispiel**: 3 Subnetzte in einem privaten Klasse-C-Netzwerk mit der Netz-ID `192.168.0.0/24`

1. **Leihbits berechnen**
   Die Anzahl der Leihbits lässt sich über die Formel $2^n \geq S$ bestimmen.
   `S` steht dabei für die Anzahl der Subnetze und $n$ für die Anzahl der Leihbits.
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
   Die Größe der Subnetze lässt sich über die Formel $2^m = G$ bestimmen.
   `G` steht dabei für die Anzahl Subnetzgröße und $m$ für die Anzahl der verbleibenden Bits.
   Um die Hostanzahl $H$ zu bestimmen wird folgende Formel verwendet: $2^m - 2 = H$.
```
2ᵐ = G     ⇨     2⁶ – 2 = 64     ⇨     64 – 2 = 62 (Hosts)
```
4. **Subnetzübersicht aufstellen**
 | Name        | Subnetz-ID    | Hostbereich                   | Broadcast     |
 | ----------- | ------------- | ----------------------------- | ------------- |
 | Buchhaltung | 192.168.0.0   | 192.168.0.1 - 192.168.0.62    | 192.168.0.63  |
 | Vertrieb    | 192.168.0.64  | 192.168.0.65 – 192.168.0.126  | 192.168.0.127 |
 | Support     | 192.168.0.128 | 192.168.0.129 – 192.168.0.190 | 292.168.0.191 |

# Berechnung über Größe der Subnetze
**Bespiel**: 100 Clients im größten Subnetz eines B-Netzwerks mit der Netz-ID `172.16.0.0/16`

1. Hostbits berechnen
   Mit der Formel $2^m - 2 = H$ lassen sich die übrigen Bits berechnen, z.B. durch ausprobieren.
```
2ᵐ – 2 = H     ⇨     2⁷ – 2 = 126     ⇨     7 Hostbits
```
2. Leihbits berechnen
   Die Summe von Leihbits und übrigen Bits muss restlos (Modulo) durch 8 teilbar sein. Es muss beachtet werden, dass die Summe ggf. über der Länge eines Segments (1 Byte) liegen kann. Es können maximal so viele Segmente eingenommen werden, wie in der Subnetzmaske des Starts logisch null sind.
```
Annahme 1 Byte:   8 – 7 = 1 (Leihbit)      ⇨     falsch 
Annahme 2 Bytes:  16 – 7 = 9 (Leihbits)    ⇨     wahr 
                  ⇩ 
                  2ⁿ = S     ⇨     2⁹ = 512 (Subnetze)
```
3. Subnetzmaske berechnen
```
Klasse B:   1111 1111.1111 1111.0000 0000.0000 0000 /16     ⇨     255.255.0.0 
            ⇩ 
Subnetz 1:  1111 1111.1111 1111.0000 0000.0000 0000 /25     ⇨     255.255.255.128 
Subnetz 2:  1111 1111.1111 1111.0000 0000.1000 0000 /25     ⇨     255.255.255.128
```
4. Subnetzübersicht aufstellen
| Name              | Subnetz-ID   | Hostbereich                 | Broadcast    |
| ----------------- | ------------ | --------------------------- | ------------ |
| Anmeldung         | 172.16.0.0   | 172.16.0.1 – 172.16.0.124   | 172.16.0.125 |
| Personalabteilung | 172.16.0.126 | 172.16.0.127 – 172.16.0.150 | 172.16.0.251 |

