# Domänen
Domänen sind definierte Administrationsbereiche in gewerblichen Netzwerken, welche redundant betrieben werden.

![](../_Medien/Domäne.png)

## Tree
Ein Tree (auch *Kerberos Two Way Transitive Trust*) besteht aus mehreren verbundenen Domänen. Die Domänen bleiben eigenständige „Verwaltungszonen“ und überschreiben sich nicht gegenseitig. Es gibt *keine* Vererbung von Gruppenrichtlinien. Ein Tree hat einen einheitlichen Namensraum.

![](../_Medien/Domäne_Tree.png)

## Forrest
Je Tree im Forrest gibt es *nur einen* Namensraum (bezieht sich auf die Adresse der Domäne). Ein Forrest besteht aus mehreren Trees.

![](../_Medien/Domäne_Forrest.png)
