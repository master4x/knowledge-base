# IP-Adressen

## IPv4-Adresse
Eine IPv4-Adresse ist eine 32 Bit lange Binärzahl, welche im sog. Dotted-Decimal-Format mit Punkten als Trennzeichen angegeben wird. Jedes Bytes wird als Dezimalzahl im Wertebereich von 0-255 angegeben und durch Punkt getrennt. Als *Selbstreferenz* bezeichnet man die IP `127.0.0.1` (auch `localhost`). Man teilt ihre Gültigkeitsbereich in [[Netzwerklassen]] ein.

## IPv6-Adresse
Die IPv6-Adresse ist der Weiterentwicklung der IPv4-Adresse. Die wichtigsten Änderungen sind die Erweiterung der Adresslänge auf *128 Bit* und die feste Länge des Hostanteils. Eine IPv6-Adresse besteht aus *8 Blöcken* mit 4 kleingeschriebenen *Hexadezimalwerten*, welche durch Doppelpunkte getrennt sind.

Die Subnetzmaske *fällt bei IPv6 ersatzlos weg*. Um trotzdem eine Segmentierung durchführen zu können, wird die *Präfixlänge* definiert und mit einem Schrägstrich an die IPv6-Adresse angehängt.

### Verkürzung (RFC 5952)
Für die Darstellung von IPv6-Adressen gibt es mehrere Notationsregeln, um eine Adresse zu kürzen.

1. Alle führenden Nullen eines Blocks werden grundsätzlich ausgelassen. 
2. Eine oder Mehrere aufeinanderfolgende Nullerblöcke werden wie folgt gekürzt: „::“. 
   *Diese Regel darf nur einmal bei der längsten Folge an Nullerblöcken (oder bei gleicher Länge die erste von links) angewendet werden.*

```
2001:0db8:03fe:0000:0100:0000:0000:0007 
2001: db8: 3fe:   0: 100:    :        7 ⇨ 2001:db8:3fe:0:100::7
```

```
1b46:0000:0000:03ed:0000:0000:0000:0004 
1b46:   0:   0: 3ed:    :             4 ⇨ 1b46:0:0:3ed::4
```

### Unterstützung für IPv4
Gelegentlich müssen Hosts, die nur IPv4 unterstützen, mithilfe einer Übersetzung angesprochen werden. Für diese wurde ein eigener Adressbereich mit dem Präfix `0:0:0:0:0:ffff::` reserviert. Die verbleibenden 32 Bit der Adresse werden mit der IPv4-Adresse in dezimaler Schreibweise gefüllt.

```
192.168.2.1 
⇩ 
::ffff:192.168.2.1 
::ffff:c0a0:0201 ⇦ HEX-Darstellung
```