Ein Subselect ist eine Abfrage, die in einer `SELECT`-, `INSERT`-, `UPDATE`- oder `DELETE`-Anweisung bzw. in einer anderen *Unterabfrage* verschachtelt ist. Ein Subselect kann überall dort verwendet werden, *wo ein Ausdruck zulässig ist*.

``` sql
SELECT Name FROM Mitarbeiter WHERE Mitarbeiter.AbteilungsID =
         (SELECT Mitarbeiter.AbteilungsID FROM Mitarbeiter 
                 WHERE Mitarbeiter.Jahresbonus = 
                          (SELECT MAX(Mitarbeiter.Jahresbonus) FROM Mitarbeiter));
```
