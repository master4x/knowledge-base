# IPv4-Adresse
Eine IPv4-Adresse ist eine 32 Bit lange Binärzahl, welche im sog. Dotted-Decimal-Format mit Punkten als Trennzeichen angegeben wird. Jedes Bytes wird als Dezimalzahl im Wertebereich von 0-255 angegeben und durch Punkt getrennt. Als *Selbstreferenz* bezeichnet man die IP `127.0.0.1` (auch als Hostname `localhost`). Man teilt ihre Gültigkeitsbereich in [[Netzwerklassen]] ein.

# IPv6-Adresse
Die IPv6-Adresse ist der Weiterentwicklung der IPv4-Adresse. Die wichtigsten Änderungen sind die Erweiterung der Adresslänge auf *128 Bit* und die feste Länge des Hostanteils. Eine IPv6-Adresse besteht aus *8 Blöcken* mit 4 kleingeschriebenen *Hexadezimalwerten*, welche durch Doppelpunkte getrennt sind.

## Kategorien

IPv6-Adressen sind in verschiedene Kategorien unterteilt, die jeweils spezifische Anwendungsbereiche und Eigenschaften haben. Hier sind die wichtigsten Unterarten von IPv6-Adressen:

### 1. Link-Local Adressen
Link-Local Adressen sind für die Kommunikation innerhalb eines einzelnen Netzwerksegments (Link) gedacht. Sie sind nicht über Router hinaus routbar.

- **Präfix:** fe80::/10
- **Verwendung:** Lokale Kommunikation zwischen Geräten im selben Netzwerksegment, z.B. für die automatische Adresskonfiguration (SLAAC) und die Kommunikation mit dem Standard-Gateway.

### 2. Global Unicast Adressen
Global Unicast Adressen sind eindeutige Adressen, die im gesamten IPv6-Internet routbar sind. Sie sind vergleichbar mit den öffentlichen IPv4-Adressen.

- **Präfix:** 2000::/3
- **Verwendung:** Eindeutige Adressierung von Geräten, die direkt über das Internet erreichbar sein sollen.

### 3. Unique Local Adressen
Unique Local Adressen sind für die lokale Kommunikation innerhalb eines privaten Netzwerks gedacht und nicht global routbar. Sie sind vergleichbar mit den privaten IPv4-Adressen.

- **Präfix:** fc00::/7
- **Verwendung:** Interne Netzwerkkommunikation, die nicht ins öffentliche Internet geleitet wird.

### 4. Multicast Adressen
Multicast Adressen werden verwendet, um Datenpakete an mehrere Empfänger gleichzeitig zu senden.

- **Präfix:** ff00::/8
- **Verwendung:** Übertragung von Daten an eine Gruppe von Geräten, z.B. für Streaming oder Kommunikationsdienste.

### 5. Anycast Adressen
Anycast Adressen sind einer Gruppe von Interfaces zugewiesen, wobei Pakete an das nächstgelegene Interface der Gruppe gesendet werden.

- **Verwendung:** Lastverteilung und effiziente Ressourcennutzung durch Weiterleitung von Anfragen an den geografisch nächsten oder am wenigsten ausgelasteten Server.

### 6. Loopback Adresse
Die Loopback Adresse dient der internen Kommunikation auf einem einzelnen Gerät und wird für Tests und Diagnosen verwendet.

- **Adresse:** ::1
- **Verwendung:** Kommunikation innerhalb des Geräts selbst, ähnlich der IPv4-Loopback-Adresse 127.0.0.1.

Diese Unterarten von IPv6-Adressen bieten Flexibilität und Funktionalität für verschiedene Netzwerkbedürfnisse, von der lokalen Kommunikation bis hin zur globalen Adressierung und speziellen Verteilungsmechanismen wie Multicast und Anycast.
## Subnetzmaske
Die Subnetzmaske *fällt bei IPv6 ersatzlos weg*. Um trotzdem eine Segmentierung durchführen zu können, wird die *Präfixlänge* definiert und mit einem Schrägstrich an die IPv6-Adresse angehängt.

## Verkürzung
Für die Darstellung von IPv6-Adressen gibt es mehrere Notationsregeln, um eine Adresse zu kürzen (RFC 5952).

1. Alle führenden Nullen eines Blocks werden grundsätzlich ausgelassen. 
2. Eine oder Mehrere aufeinanderfolgende Nullerblöcke werden durch zwei aufeinanderfolgende Doppelpunkte gekürzt:. 
   *Diese Regel darf nur einmal bei der längsten Folge an Nullerblöcken (oder bei gleicher Länge die erste von links) angewendet werden.*

```
2001:0db8:03fe:0000:0100:0000:0000:0007 
2001: db8: 3fe:   0: 100:    :        7 ⇨ 2001:db8:3fe:0:100::7
```

```
1b46:0000:0000:03ed:0000:0000:0000:0004 
1b46:   0:   0: 3ed:    :             4 ⇨ 1b46:0:0:3ed::4
```

## Abwärtskompatibilität
Gelegentlich müssen Hosts, die nur IPv4 unterstützen, mithilfe einer Übersetzung angesprochen werden. Für diese wurde ein eigener Adressbereich mit dem Präfix `0:0:0:0:0:ffff::` reserviert. Die verbleibenden 32 Bit der Adresse werden mit der IPv4-Adresse in dezimaler Schreibweise gefüllt.

```
192.168.2.1 
⇩ 
::ffff:192.168.2.1 
::ffff:c0a0:0201 ⇦ HEX-Darstellung
```
