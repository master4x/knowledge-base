Ein **Trigger** in einer Datenbank ist eine automatische Aktion, die ausgeführt wird, wenn bestimmte Ereignisse wie das Einfügen, Aktualisieren oder Löschen von Daten auf einer Tabelle stattfinden. Trigger können verwendet werden, um sicherzustellen, dass bestimmte Regeln oder Prozesse in der Datenbank eingehalten werden, ohne dass der Benutzer direkt eingreifen muss.

# Arten von Triggern

## BEFORE Trigger
Ein **BEFORE Trigger** wird vor dem Ausführen einer Operation wie `INSERT`, `UPDATE` oder `DELETE` ausgelöst. Er kann z. B. verwendet werden, um Daten vor der Speicherung zu überprüfen oder zu ändern.

## AFTER Trigger
Ein **AFTER Trigger** wird nach dem erfolgreichen Abschluss einer Operation wie `INSERT`, `UPDATE` oder `DELETE` ausgeführt. Er kann verwendet werden, um zusätzliche Aufgaben wie Protokollierung oder das Aktualisieren anderer Tabellen durchzuführen.

## Nutzen von Triggern
- **Automatisierung**: Trigger ermöglichen es, Aufgaben zu automatisieren, die sonst manuell durchgeführt werden müssten.
- **Datenintegrität**: Sie helfen, die Konsistenz und Integrität der Daten sicherzustellen, indem sie z. B. Regeln durchsetzen, die sicherstellen, dass bestimmte Bedingungen immer erfüllt sind.
- **Protokollierung**: Trigger können verwendet werden, um Änderungen an Daten nachzuverfolgen und in speziellen Log-Tabellen zu speichern.

Trigger sind besonders nützlich, wenn bestimmte Aktionen in der Datenbank automatisch und zuverlässig ausgeführt werden müssen, ohne dass der Benutzer direkt eingreift.
