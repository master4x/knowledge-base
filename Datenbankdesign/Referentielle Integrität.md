In relationalen Datenbanken wird die Integritätsprüfung dazu verwendet die *Konsistenz* der Datensätze sicherzustellen. 

Durch die Bedingung der referentiellen Integrität können nur Datensätze, die einen Fremdschlüssel aufweisen nur dann gespeichert werden, wenn der Wert des Fremdschlüssels einmalig in der referenzierten Tabelle existiert. Für den Fall, dass der referenzierte Schlüssel nicht vorhanden ist, wird das SQL-Statement mit einem Fehler abgebrochen.
# Kaskadierende Löschoperationen
Kaskadierende Löschoperationen sind erforderlich, wenn eine abhängige Entität nicht mehr dem Primärschlüssel bzw. der referenzierten Entität zugeordnet werden kann. Dieser Fall kann auftreten, wenn die übergeordnete Entität gelöscht wird oder die untergeordnete Entität nicht mehr zugeordnet ist.
