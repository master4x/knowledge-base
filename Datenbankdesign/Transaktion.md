**Transaktionen** sind eine Abfolge von Datenbankoperationen, die als eine einzige, unteilbare Einheit ausgeführt werden. Ziel ist es, sicherzustellen, dass die Datenbank in einem konsistenten Zustand bleibt, selbst bei Fehlern oder Unterbrechungen. Transaktionen sind besonders wichtig für Anwendungen, die mehrere Änderungen in einer Datenbank als zusammenhängende Einheit ausführen müssen (z. B. bei Überweisungen, Bestellungen oder Lagerbestandsaktualisierungen).

# Das ACID-Prinzip

Um die Integrität und Konsistenz der Datenbank sicherzustellen, folgen Transaktionen dem **ACID-Prinzip**. Die ACID-Eigenschaften beschreiben die wesentlichen Merkmale einer Transaktion und gewährleisten, dass Daten zuverlässig verarbeitet werden.

## 1. Atomicity (Atomarität)
Die **Atomarität** stellt sicher, dass alle Operationen einer Transaktion entweder vollständig ausgeführt oder vollständig zurückgerollt werden. Es gibt keine teilweise Durchführung einer Transaktion – sie ist entweder „alles oder nichts“.
- **Beispiel**: Bei einer Banküberweisung wird der Betrag von einem Konto abgebucht und auf ein anderes gutgeschrieben. Die Atomarität sorgt dafür, dass entweder beide Operationen erfolgreich abgeschlossen oder beide rückgängig gemacht werden.

## 2. Consistency (Konsistenz)
Die **Konsistenz** gewährleistet, dass die Datenbank vor und nach einer Transaktion in einem gültigen Zustand bleibt und alle definierten Regeln und Einschränkungen erfüllt sind.
- **Beispiel**: Wenn eine Bestellung abgeschlossen wird, darf der Lagerbestand des bestellten Produkts nicht negativ sein. Die Konsistenz stellt sicher, dass solche Regeln immer eingehalten werden.

## 3. Isolation (Isolation)
Die **Isolation** sorgt dafür, dass parallele Transaktionen sich nicht gegenseitig beeinflussen. Jede Transaktion wird so ausgeführt, als wäre sie die einzige, die auf die Datenbank zugreift, um Konflikte zu vermeiden.

- **Beispiel**: Wenn zwei Transaktionen gleichzeitig versuchen, den Lagerbestand eines Produkts zu ändern, verhindert die Isolation, dass sie sich gegenseitig überschreiben oder auf unvollständige Daten zugreifen.

## 4. Durability (Dauerhaftigkeit)
Die **Dauerhaftigkeit** garantiert, dass nach erfolgreichem Abschluss einer Transaktion deren Ergebnisse dauerhaft in der Datenbank gespeichert sind, selbst bei einem Systemausfall.
- **Beispiel**: Wenn ein Kauf abgeschlossen ist und der Lagerbestand aktualisiert wurde, bleibt diese Änderung auch bei einem Serverabsturz bestehen.

# Ablauf einer Transaktion
In SQL werden Transaktionen häufig mit den folgenden Befehlen gesteuert:
- `BEGIN TRANSACTION`: Startet eine neue Transaktion.
- `COMMIT`: Bestätigt die Transaktion und speichert die Änderungen dauerhaft.
- `ROLLBACK`: Bricht die Transaktion ab und macht alle seit dem Beginn der Transaktion vorgenommenen Änderungen rückgängig.

## Beispiel

```sql
BEGIN TRANSACTION;

UPDATE Konten SET Betrag = Betrag - 100 WHERE KontoID = 1;

UPDATE Konten SET Betrag = Betrag + 100 WHERE KontoID = 2;

COMMIT;
```

