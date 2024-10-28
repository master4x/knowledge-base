In der Datenbankmodellierung und speziell in [[ERD#Entity-Relationship-Diagrammen]] (ERDs) beschreibt der Begriff **Entität** ein Objekt oder Konzept, das in einer Datenbank repräsentiert wird. Entitäten werden auf Grundlage von Ähnlichkeiten in Gruppen zusammengefasst, die als **Entitätstypen** bezeichnet werden. Ein **Entitätstyp** beschreibt eine Menge von Entitäten mit gleichen Attributen, jedoch unterschiedlichen Attributwerten.

# Entität und Entitätstyp
Im Deutschen wird unterschieden zwischen einer **Entität** (eine konkrete Ausprägung oder Instanz) und einem **Entitätstyp** (die abstrakte Definition). Der Entitätstyp legt fest, welche Eigenschaften oder Attribute alle Entitäten dieser Gruppe teilen. Im Englischen wird für beides oft das Wort **Entity** verwendet.

## Beispiel

In einer Datenbank, die Kundendaten speichert, könnte der **Entitätstyp** „Kunde“ definiert sein. Ein bestimmter Kunde, z. B. „Max Mustermann“, ist dann eine **Entität** des Typs „Kunde“. Jede Entität besitzt Attribute (z. B. Name, Wohnort), die spezifische Werte haben.

| Entitätstyp | Entität    | Attribut | Attributwert |
|-------------|------------|----------|--------------|
| Kunde       | Mustermann | Wohnort  | Musterstadt  |

In diesem Beispiel beschreibt der Entitätstyp **Kunde** alle Kunden in der Datenbank, während die konkrete Entität **Mustermann** einen spezifischen Kunden mit dem Attributwert „Musterstadt“ für den Wohnort repräsentiert.

## Eigenschaften von Entitäten

- **Attribute**: Merkmale oder Eigenschaften, die eine Entität beschreiben, z. B. Name, Adresse, Geburtsdatum.
- **Primärschlüssel**: Ein eindeutiges Attribut oder eine Kombination von Attributen, das jede Entität eines Entitätstyps identifiziert, z. B. „Kunden-ID“.
- **Beziehungen**: Entitäten können in Beziehung zu anderen Entitäten stehen, etwa Kunden und Bestellungen, was in ER-Diagrammen durch Verbindungen dargestellt wird.

