Transaktionen sind eine Abfolge von Datenbankoperationen, die als eine einzige, atomare Einheit behandelt werden. Sie folgen dem ACID-Prinzip:
- **Atomicity (Atomarität)**: Alle Operationen innerhalb einer Transaktion werden entweder vollständig ausgeführt oder vollständig zurückgerollt.
- **Consistency (Konsistenz)**: Die Datenbank befindet sich immer in einem konsistenten Zustand, bevor und nachdem eine Transaktion ausgeführt wurde.
- **Isolation (Isolation)**: Die Operationen innerhalb einer Transaktion sind voneinander isoliert und können nicht von anderen Transaktionen beeinflusst werden.
- **Durability (Dauerhaftigkeit)**: Nachdem eine Transaktion abgeschlossen wurde, bleiben ihre Ergebnisse dauerhaft in der Datenbank gespeichert, selbst bei Systemfehlern.
