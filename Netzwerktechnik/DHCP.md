Das DHCP („Dynamic Host Configuration Protocol“) dient dazu, Clients eine *vollautomatische Konfiguration* der TCP/IP-Einstellungen (auch Netzwerkkonfiguration) über UDP zu ermöglichen und verhindert so gleichzeitig *IP-Adresskonflikte*. Dies ist besonders in größeren Netzwerken praktisch, weil man durch DHCP nicht jeden einzelnen Host manuell konfigurieren muss bzw. der Nutzer keine Kenntnis über die im aktuellen Netz gültigen Einstellungen benötigt. Der Systemadministrator *konfiguriert den DHCP-Server* mit den Optionen, die an den Client übergeben werden sollen.

**DHCP-Netzwerkkonfiguration**:
 - [[IP-Adressen|IP-Adresse]]
 - [[Subnetzmaske]]
 - Standard-[[Gateways|Gateway]]
 - [[DNS]]-Server (optional)

**Technischer Ablauf**:
1. Host:     `DHCP-Discover` *([[Übertragungsmethoden#Broadcast|Broadcast]]])*
2. Server:   `DHCP-Offer` *([[Übertragungsmethoden#Broadcast|Broadcast]]])*
3. Host:     `DHCP-Request` *([[Übertragungsmethoden#Broadcast|Broadcast]]]/[[Übertragungsmethoden#Unicast|Unicast]])*
4. Server:   `DHCP-(N)ACK` *([[Übertragungsmethoden#Broadcast|Broadcast]]]/[[Übertragungsmethoden#Unicast|Unicast]])*

Erhält der Client mehr als ein Angebot, darf er *unter den eingetroffenen Angeboten wählen*. Der Client benachrichtigt den DHCP-Server per `DHCP-Request`-Nachricht über seine Auswahl. Für die Antwort benutzt der Client als Quelladresse jedoch noch nicht die angebotene IP-Adresse, sondern immer noch die gleiche IP-Adresse wie für das `DHCP-Discover`. Zur Identifikation gegenüber dem DHCP-Server dient die in der `DHCP-REQUEST` ebenfalls enthaltene MAC-Adresse des Clients oder die Transaktions-ID der Anfrage (auf welche der Client referiert).

# Lease
Der *IP-Lease* ist einer der wichtigsten Begriffe bei DHCP. Jede durch DHCP vergebene Adresse hat eine *Lease-Dauer*, eine *Zeit in der sie dem Client zur Verfügung steht*. DHCP vergibt seine Adressen nicht auf Dauer, sondern nur für die konfigurierte Zeit. Nach Ablauf des Lease stellt der Client zur Verlängerung seiner IP-Adresse, indem er *nur den* `DHCP-Request` und `DHCP-(N)ACK` ausführt.

# Pool
Ein *DHCP-Pool* gibt an, *wie viele IP-Adressen in einem Bereich* vergeben werden können. Es können mehrere DHCP-Server pro Netzwerk eingesetzt werden, *sofern der IP-Pool sich nicht überschneidet*. Gibt es in einem Netzwerk mehrere DHCP-Server, so antworten in der Regel alle DHCP-Server auf einen DHCP-Discover.

# Rouge
Ein Rogue-DHCP ist ein *bösartiger DHCP-Server*, der einen gesicherten IP-Pool besitzt. Dabei gilt, dass dieser *Pool sich mit einem anderen überschneidet*. Daraus resultieren doppelt vergebene IP-Adressen im Netzwerk, was diese *nicht mehr eindeutig* macht. Die Funktion „DHCP-Snooping“ schützt vor Rogues.

# Relay
Der DHCP-Server muss sich *im selben (Sub-)Netzwerk befinden* wie der Client, da der Client für seine Anfrage einen Broadcast verwendet und [[Komponenten#Router|Router]] Broadcasts nicht weiterleiten. Wenn sich der DHCP-Server in einem anderen (Sub-)Netzwerk befindet als der Client, so muss *im Netz des Clients ein DHCP-Relay(-Agent) installiert werden*, der die DHCP-Anfragen an den zuständigen DHCP-Server weiterleitet. Ein [[Komponenten#Layer3-Switch|L3-Switch]] zum Routing zwischen Subnetzen ersetzt kein DHCP-Relay.

Im Fall von Windows-Clients kann die IP-Adresse `169.254.0.0` auf einen falsch konfigurierten DHCP-Server oder *ein fehlendes DHCP-Relay hinweisen*. Diese Adresse wird vom Betriebssystem immer vergeben, wenn keine gültige Netzwerkkonfiguration von einem DHCP-Server eingeholt werden kann. Auf Clients jeglicher Systeme ist DHCP *standardmäßig aktiv*.
