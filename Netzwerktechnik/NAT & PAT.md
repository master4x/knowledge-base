Um mit einer privaten IP-Adresse auf das Internet zugreifen zu können, müssen die Anfragen übersetzt und weitergeleitet werden. Dabei kommt das PAT („Port Address Translation”) zum Einsatz, welches seinen Vorgänger, das NAT („Network Address Translation”), abgelöst hat.

Stellt ein Teilnehmer aus dem privaten Netzwerk eine Anfrage ins Internet, so vergibt das PAT einen Port für die Anfrage. Der Router leitet die Anfrage mit seiner öffentlichen IP-Adresse und dem Port (Netzwerksocket) an den Empfänger weiter. Sollte der Empfänger eine Antwort an den Socket senden, empfängt der Router das Packet und gibt es an das PAT weiter. In der *Tabelle des PAT* kann die Anfrage anhand der Portnummer der Quelle im internen Netzwerk zugeordnet werden. Für die Portvergabe werden in der Regel *sehr hohe Ports* angesetzt. Zu lokalen Clients hinter einem PAT-Router kann von außerhalb keine Verbindung aufgebaut werden (Portfreigabe notwendig).

![](../_Medien/NAT_PAT.png)
