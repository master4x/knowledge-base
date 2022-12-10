Views sind Abfragen, die in der Datenbank *als Objekt fest gespeichert* sind. Sie können als *virtuelle Tabellen* verstanden werden, deren Inhalt und Struktur auf anderen Tabellen oder Views basieren, und können in (fast) jedem SELECT-Befehl anstelle einer „echten“ Tabelle verwendet werden.

Bei einer View wird die *Abfrage in der Datenbank gespeichert*, aber nicht das Ergebnis. Bei jedem neuen Aufruf der View wird die dahinterliegende Abfrage neu ausgeführt, denn sie soll die aktuellen Daten verwenden. Die Abfragen, auf denen Views basieren, können grundsätzlich alle Klauseln wie eine normale Abfrage enthalten. Somit ist es möglich, bestimmte Daten in einer View zu selektieren und zu gruppieren.

Eine View kann z. B. für folgende Zwecke verwendet werden:
- Um die Darstellung einer Datenbank für jeden einzelnen Benutzer *einzuschränken*, zu *vereinfachen* (z.B. Relationen aus mehreren Joins) und anzupassen.
- Als *Sicherheitsmechanismus*, indem Benutzern der Zugriff auf Daten über die Sicht ermöglicht wird, ohne diesen Benutzern jedoch die Berechtigungen für den direkten Zugriff auf die zugrunde liegenden Basistabellen zu gewähren.
- Um eine abwärtskompatible Schnittstelle zum Emulieren einer Tabelle bereitzustellen, deren Schema geändert wurde.

``` sql
CREATE OR REPLACE VIEW Mitarbeiter_Webdesign AS
         SELECT * FROM Mitarbeiter WHERE Abteilungs_ID = 100 WITH CHECK OPTION;
```

Da sich Datensätze über eine View in die Ursprungstabelle einfügen lassen, kann man mit dem Zusatzstatement `WITH CHECK OPTION` erzwingen, dass alle für die View ausgeführten Datenänderungsanweisungen *den Kriterien entsprechen* müssen, die innerhalb vom `SELECT`-*Statement* festgelegt wurden. So lassen sich Inkonsistenzen vermeiden.
