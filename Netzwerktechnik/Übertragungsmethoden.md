![[Übertragungsmethoden_Veranschaulichung.png]]

## Unicast
Unicast bezeichnet die direkte Verbindung zwischen zwei Stationen, entweder direkt oder über ein Netzwerk. Die Kommunikation kann unidirektional oder bidirektional sein. Die benötigte Bandbreite steigt mit jeder zusätzlichen Host im Netzwerk, was zu erhöhter Netzlast führen kann. Dies kann bei Audio- und Video-Streaming zu Wiedergabeaussetzern führen.

## Multicast
Multicast beinhaltet einen Sender, der Signale, Daten und Informationen an eine definierte Gruppe von Empfängern überträgt. Die Bandbreite wird nur für einen Teilnehmer verbraucht, und die Verteilung an die einzelnen Empfänger erfolgt durch den letzten Router, der die Daten dupliziert.

## Broadcast
Broadcast bezeichnet ein Datenpaket, das in das Netzwerk eingespeist und von dort an alle Hosts übertragen wird. Jeder Host empfängt die Daten, unabhängig davon, ob er sie möchte oder nicht. Dies folgt dem Gießkannenprinzip, wie es beim Rundfunk oder Fernsehen verwendet wird.

## Anycast
Anycast sendet eine Nachricht an einen Empfänger aus einer Gruppe von Empfängern, ohne festzulegen, an welchen. Dahinter steht die Idee einer mehrfach vorhandenen Adresse (IPv6-Anycast-Adresse). Dies bedeutet jedoch, dass kein wechselseitiger Dialog möglich ist, da nicht sicher ist, ob immer dieselbe Maschine verbunden ist.
