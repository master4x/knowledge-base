# Übertragungsmedien

## Technologien

## Medien

### Kupferkabel
**Faustregel**: Netzwerkkabel nicht länger als 100m am Stück verlegen.

#### Kategorien
| Kategorie | Geschwindigkeit | Frequenz | Stecker | Norm         |
|-----------|-----------------|----------|---------|--------------|
| Cat.5e    | 1 Gbit/s        | 100 MHz  | RJ45    | TIA          |
| Cat.6     | 1 Gbit/s        | 250 MHz  | RJ45    | ISO, EN, TIA |
| Cat.7     | 10 Gbit/s       | 600 MHz  | GG45    | ISO, EN      |

#### Schirmung
| Twisted-Pair-Kabel (TP) | U/UTP | S/UTP | U/FTP | S/FTP | S/STP | F/FTP | SF/FTP |
| ----------------------- | ----- | ----- | ----- | ----- | ----- | ----- | ------ |
| Drahtgeflecht (S)       |       | X     |       | X     | X     |       | X      |
| Folie (F)               |       |       |       |       |       | X     | X      |
| Drahtgeflecht (S)       |       |       |       |       | X     |       |        |
| Folie (F)               |       |       | X     | X     |       | X     | X      |

### Glasfaser (LWL)
Lichtwellenleiter (kurz LWL) sind *um ein Vielfaches schneller als Kupferkabel*. Außerdem sind diese *weniger störanfällig* gegenüber elektromagnetischen Einflüssen, da per Laser nur Lichtimpulse übertragen werden. Glasfaserkabel sind damit einhergehend deutlich *filigrane und teurere Ware*.

Im *primären und sekundären Bereich wird Glasfaser* eingesetzt, zu den Endgeräten im tertiären Bereich werden Kupferkabel (min. Cat.5e, besser 6(a) oder 7) verlegt. Die angepeilte Struktur ist eine Stern-Stern-Topologie von den Gebäudeverteilern (kurz GVs, L3-Switches) über die Etagenverteilern (kurz EVs, L2-Switches) zu den Clients. Die Primärverkabelung endet/*beginnt am Router zum WAN*.

### Koaxialkabel
