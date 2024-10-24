Datenbank-Constraints (Einschränkungen) stellen sicher, dass Daten in einer Datenbank konsistent und valide bleiben. Sie definieren Regeln für die zulässigen Werte in Tabellen und schützen die Datenintegrität. Es gibt verschiedene Arten von Constraints, die in relationalen Datenbanken verwendet werden. 

# NOT NULL 
Das **NOT NULL**-Constraint stellt sicher, dass eine Spalte niemals einen NULL-Wert enthält. Es wird verwendet, um sicherzustellen, dass bestimmte Felder immer einen Wert haben. 

**Beispiel**: 
```sql 
CREATE TABLE users (
	id INT PRIMARY KEY,
	username VARCHAR(50) NOT NULL
);
```

# UNIQUE
Das **UNIQUE**-Constraint stellt sicher, dass alle Werte in einer Spalte oder einer Kombination von Spalten einzigartig sind. Es verhindert, dass Duplikate in die Tabelle eingefügt werden.

**Beispiel**:
``` sql
CREATE TABLE users (
	id INT PRIMARY KEY,
	email VARCHAR(100) UNIQUE
);
```

# PRIMARY KEY
Der **PRIMARY KEY**-Constraint kombiniert die Eigenschaften von **NOT NULL** und **UNIQUE**. Er stellt sicher, dass jede Zeile in einer Tabelle eindeutig identifiziert werden kann. Eine Tabelle kann nur einen Primärschlüssel haben.

**Beispiel**:
``` sql
CREATE TABLE users (
  id INT PRIMARY KEY,
  username VARCHAR(50)
);
```

# FOREIGN KEY
Das **FOREIGN KEY**-Constraint stellt eine Beziehung zwischen zwei Tabellen her. Es erzwingt, dass Werte in einer Spalte mit Werten in der Primärschlüssel-Spalte einer anderen Tabelle übereinstimmen.

**Beispiel**:
``` sql
CREATE TABLE orders (
	id INT PRIMARY KEY, 
	user_id INT, 
	FOREIGN KEY (user_id) REFERENCES users(id) 
);
```

# CHECK
Das **CHECK**-Constraint stellt sicher, dass alle Werte in einer Spalte eine bestimmte Bedingung erfüllen. Es erlaubt die Definition von Bedingungen, die für jeden Datensatz überprüft werden.

**Beispiel**:
``` sql
CREATE TABLE employees (
  id INT PRIMARY KEY,
  salary DECIMAL(10, 2),
  CHECK (salary > 0)
);
```

# DEFAULT
Das **DEFAULT**-Constraint gibt einen Standardwert für eine Spalte an, wenn kein anderer Wert angegeben wird. Dies stellt sicher, dass die Spalte immer einen Wert enthält, auch wenn keine explizite Eingabe erfolgt.

**Beispiel**:
``` sql
CREATE TABLE products (
  id INT PRIMARY KEY,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```
