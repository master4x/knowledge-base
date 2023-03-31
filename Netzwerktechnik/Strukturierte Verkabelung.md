# Strukturierte Verkabelung
Die strukturierte Gebäudeverkabelung ist in der `DIN EN 50173` geregelt. Die Norm unterteilt Gebäudekomplexe in drei Bereiche, in welchen verschiedene Netzwerkkomponenten und Übertragungsmedien eingesetzt werden.

![](../_Medien/EN_50173.png)

Im *primären und sekundären Bereich wird [[Übertragungsmedien#Glasfaser (LWL)|Glasfaser]] eingesetzt*, zu den Endgeräten im tertiären 
Bereich werden [[Übertragungsmedien#Kupferkabel|Kupferkabel]] (min. Cat.5e, besser 6(a) oder 7) verlegt. Die angepeilte Struktur ist eine Stern-Stern-Topologie von den Gebäudeverteilern (kurz GV, [[Komponenten#Layer3-Switch|L3-Switch]]) über die Etagenverteilern (kurz EV, [[Komponenten#Switch|L2-Switch]]) zu den Clients. Die Primärverkabelung endet/*beginnt am [[Komponenten#Router|Router]] zum WAN.*

![](../_Medien/EN_50173_Netzwerk.png)
