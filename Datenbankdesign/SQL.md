In SQL gibt es verschiedene Befehlsarten, die in unterschiedliche Kategorien unterteilt sind. Diese Kategorien definieren den Zweck und die Funktion der jeweiligen Befehle innerhalb einer Datenbank. Die gängigsten Befehlsarten sind **DDL**, **DML**, **DCL** und **DQL**.

# DDL - Data Definition Language
**DDL-Befehle** werden verwendet, um die Struktur einer Datenbank zu definieren oder zu ändern. Mit diesen Befehlen können Tabellen, Datenbankobjekte und Datenbankschemata erstellt, verändert oder gelöscht werden.

Beispiele für DDL-Befehle:
- `CREATE`: Erzeugt eine neue Tabelle, Datenbank oder ein anderes Datenbankobjekt.
- `ALTER`: Ändert die Struktur einer bestehenden Tabelle.
- `DROP`: Löscht eine Tabelle oder ein anderes Datenbankobjekt.

```sql
CREATE TABLE Mitarbeiter (
    ID INT PRIMARY KEY,
    Name VARCHAR(100),
    Abteilung VARCHAR(50)
);
```

# DML - Data Manipulation Language
**DML-Befehle** dienen der Bearbeitung der in einer Datenbank gespeicherten Daten. Sie ermöglichen es, Daten einzufügen, zu aktualisieren oder zu löschen, ohne die Struktur der Datenbank zu verändern.

Beispiele für DML-Befehle:
- `INSERT`: Fügt neue Daten in eine Tabelle ein.
- `UPDATE`: Aktualisiert bestehende Daten in einer Tabelle.
- `DELETE`: Löscht Daten aus einer Tabelle.

```sql
INSERT INTO Mitarbeiter (ID, Name, Abteilung)
VALUES (1, 'Max Mustermann', 'Vertrieb');
```

# DCL - Data Control Language
**DCL-Befehle** werden verwendet, um die Zugriffsrechte auf die Datenbank zu verwalten. Sie regeln, welche Benutzer oder Rollen welche Operationen innerhalb der Datenbank ausführen dürfen.

Beispiele für DCL-Befehle:
- `GRANT`: Erteilt einem Benutzer oder einer Rolle bestimmte Rechte.
- `REVOKE`: Entzieht einem Benutzer oder einer Rolle bestimmte Rechte.

```sql
GRANT SELECT, INSERT ON Mitarbeiter TO Benutzername;
```

# DQL - Data Query Language
**DQL-Befehle** werden verwendet, um Daten aus der Datenbank abzurufen. Der wichtigste Befehl in dieser Kategorie ist `SELECT`. Mit `SELECT` können Abfragen durchgeführt werden, um Daten aus einer oder mehreren Tabellen zu lesen.

Beispiele für DQL-Befehle:
- `SELECT`: Ruft Daten aus einer oder mehreren Tabellen ab.

```sql
SELECT Name, Abteilung FROM Mitarbeiter;
```

Diese Befehlsarten sind die grundlegenden Kategorien von SQL-Befehlen und definieren, wie mit Daten und der Datenbankstruktur gearbeitet wird.
