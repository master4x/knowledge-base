# Schlüssel
## Primärschlüssel
Der Primärschlüssel (engl. „Primary Key“) kommt in relationalen Datenbanken zum Einsatz und wird *zur eindeutigen Identifizierung eines Datensatzes* verwendet. Der Wert eines Primärschlüssels muss in einer Tabelle einmalig (engl. „unique“) sein, da er jeden Datensatz eindeutig kennzeichnet.

### Einfacher Primärschlüssel
Als Spalte kann *ein Attribut des Datensatzes* verwendet werden, das für jeden Eintrag in der Tabelle *einen einmaligen Wert annimmt*. Als eindeutiges Primärschlüsselattribut könnte beispielsweise *die Sozialversicherungsnummer oder die Fahrgestellnummer* verwendet werden.

### Zusammengesetzte Primärschlüssel
Ist ein Datensatz anhand *eines Attributes nicht eindeutig identifizierbar*, so kann der Primärschlüssel auch aus einer *Kombination mehrerer Attribute* bestehen. Dabei muss sichergestellt werden, dass jede dieser *Kombinationen nur einmalig auftritt*. Ein zusammengesetzter Primärschlüssel kann z.B. der *Vor- und Nachname, sowie das Geburtsdatum* sein.

### Künstliche Primärschlüssel 
Gibt es in einer Tabelle *keine eindeutigen Spalten* bzw. Kombinationen aus Spalten, so kann auch auf einen künstlichen Schlüssel zurückgegriffen werden. In der Praxis wird häufig eine *Guid* verwendet, um einen Datensatz eindeutig identifizieren zu können.

## Fremdschlüssel
Bei dem Fremdschlüssel (engl. „Foreign Key“) handelt es sich um eine Schlüsselspalte, die *auf einen [[Schlüssel#Primärschlüssel|Primärschlüssel]]* einer anderen (oder aber derselben) *Tabelle verweist*. Der Fremdschlüssel kann nur Werte annehmen, *die in der Referenztabelle vorhanden sind*. Zudem kann eine beliebige Anzahl von Datensätzen den gleichen Fremdschlüsselwert aufweisen.
