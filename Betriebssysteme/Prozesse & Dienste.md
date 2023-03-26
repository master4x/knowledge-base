# Unterschied Prozesse & Dienste
Jede ausgeführte Anwendung ist ein Prozess, der Arbeitsspeicher belegt und bei Bedarf den Prozessor beansprucht. Viele Anwendungen, wie z.B. Google Chrome, starten mehrere Prozesse. In der Regel gibt es für jede Anwendung maximal einen Dienst, auf den diese zurückgreifen. Auch jeder Dienst ist ein Prozess, jedoch mit dem Unterscheid, dass ein Dienst in Gegensatz zu einem klassischen Prozess nur im Hintergrund aktiv ist und auf eingehende Anfragen wartet. Ein Dienst besitzt keine direkte Schnittstelle zum Benutzer, die Interaktion ist nur über eine bestimmte Software möglich. Es existieren auch Systemdienste wie z.B. der DHCP-Client. Beide Typen haben eine PID.