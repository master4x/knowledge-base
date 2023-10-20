Eine Subnetzmaske gibt die Stelle des Umbruchs zwischen *Netzanteil* und *Hostanteil* einer [[IP-Adressen|IP-Adresse]] an. Der Netzanteil muss bei allen Clients im Netzwerk gleich groß sein. Der Hostanteil dient zur Identifizierung von Clients. *Sobald eine Subnetzmaske durch eine logische Null unterbrochen wird, darf der Rest der Subnetzmaske nur noch logisch Null sein*.

**Beispiel:** `11111111.11111111.11111111.00000000`

# Dotted-Decimal-Notation
Dies ist die althergebrachte Schreibweise, die leider immer noch üblich ist. Sie wird besonders bei Microsoft-Betriebssystemen verwendet. Dabei wird die Subnetzmaskewie eine [[IP-Adressen|IP-Adresse]] geschrieben.

**Beispiel:** `255.255.255.0`

# CIDR-Schreibweise
Die neuere und einfachere Schreibweise gibt an, wie viele Bits der Adresse den Netzanteil darstellen. Dazu wird diese Zahl als Präfix hinter die [[IP-Adressen|IP-Adresse]] geschrieben, und gibt an wieviele Bits der Netzanteil sind.

**Beispiel:** `192.168.25.17/24`
