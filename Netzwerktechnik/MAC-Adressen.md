Jedes Netzwerk-Interface hat eine eigene MAC-Adresse. MAC-Adressen bestehen aus 6 Oktetten (48 Bits). Die Adressen sind zweigeteilt in
Herstellerkennung (Vendor-ID oder Organisationally Unique Identifier, kurz: OUI) und fortlaufende Nummer des Herstellers. Große Interface-Hersteller besitzen mehrere Vendor-IDs, welche bei der [[IEEE]] verwaltet werden.

Die Schreibweise für MAC-Adressen ist byteweise hexadezimal, meist mit Bindestrichen oder Doppelpunkten als Trennzeichen.

# Besondere Bits
Das erste Oktett der MAC-Adresse hat zwei Bits mit besonderer Funktion: Bit 0 gibt an, ob [[Übertragungsmethoden#Unicast|Unicast]]- oder [[Übertragungsmethoden#Multicast|Multicast]]-Adressierung vorliegt und Bit 1 gibt an, ob die Adresse global oder nur im LAN einzigartig ist.

Multicast-Adressen adressieren beispielsweise alle Router im LAN oder alle Switches usw. Die Broadcast-Adresse lautet `ff-ff-ff-ff-ff-ff`.

![[MAC_Adresse.png]]

