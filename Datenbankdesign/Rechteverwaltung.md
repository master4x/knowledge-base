# Rechteverwaltung
Es wird in SQL zwischen zwei Klassen von Rechten unterscheiden: Objektrechte und Systemrechte. Die Organisation der Zugangsrechte findet über Benutzer und Rollen statt.
  
| **Objektrechte**  	| **Systemrechte**  	|
|------------------	|------------------	|
| `SELECT`         	| `CREATE`         	|
| `INSERT`         	| `DROP`           	|
| `UPDATE`         	|                  	|
| `DELETE`         	|                  	|
| `ALTER`          	|                  	|

Objektrechte sind Rechte für bestimmte Datenaktionen an einem einzigen Objekt (z.B. einer Tabelle) in der [[Datenbank]]. *Systemrechte sind weiterreichende Rechte*, mit denen man Aktionen (z.B. das *Erstellen einer Datenbank*) auf der Datenbank auszuführen kann.
