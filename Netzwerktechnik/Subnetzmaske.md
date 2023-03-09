# Subnetzmaske
Eine Subnetzmaske gibt die Stelle des Umbruchs zwischen *Netzanteil* und *Hostanteil* einer IP-Adresse an. Der Netzanteil muss bei allen Clients im Netzwerk gleich groß sein. Der Hostanteil dient zur Identifizierung von Clients. *Sobald eine Subnetzmaske durch eine logische Null unterbrochen wird, darf der Rest der Subnetzmaske auch nur noch null sein*.

## CIDR
Die CIDR-Notation ist eine alternative Schreibweise der Subnetzmaske. Für die Umrechnung einer herkömmlichen Subnetzmaske nach CIDR werden die logischen Einsen der binären Subnetzmaske gezählt und mit einem Slash hinter die IP-Adresse geschrieben. CIDR ist die Grundlage für Subnetting.

**IP-Adresse:** `192.168.25.17`
**Subnetzmaske:** `255.255.255.0` ➔ `11111111.11111111.11111111.00000000`
**CIDR:** `192.168.25.17/24`
