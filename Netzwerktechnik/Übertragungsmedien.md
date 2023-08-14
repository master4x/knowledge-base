# Übertragungsmedien

## Technologien
XXX

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
- **Verdrillung** verringert die Störempfindlichkeit der einzelnen Aderpaare.
- **Folienschirm**: Kunststofffolie mit äußerer Aluminiumbeschichtung
	- bedeckt den Innenleiter zu 100%
	- stabilisiert das Kabel
	- bestmögliche Schirmung
	- geringe Flexiblität
- **Geflechtsschirm**: Kupferdrahtgeflecht
	- bedeckt den Inneleiter zu 85-90%
	- gute Schirmung
	- hohe Flexiblität


##### Identifizierung
*nach ISO 11801*:  `XX/YZZ`

Gesamtschirmung `XX`:
- `U` = ungeschirmt
- `F` = Folienschirm
- `S` = Geschlechtsschirm
- `SF` = Geflechts- und Folienschirm

Aderpaarschirmung `Y`:
- `U` = ungeschirmt
- `F` = Folienschirm
- `S` = Geschlechtsschirm

Verdrillungvariante `ZZ`:
- `TP` = Twisted Pair
- `QP` = Quad Pair

| Twisted-Pair-Kabel (TP)   | U/UTP | S/UTP | U/FTP | S/FTP | S/STP | F/FTP | SF/FTP |
| ------------------------- | ----- | ----- | ----- | ----- | ----- | ----- | ------ |
| Gesamt: Drahtgeflecht (S) |       | X     |       | X     | X     |       | X      |
| Gesamt: Folie (F)         |       |       |       |       |       | X     | X      |
| Adern: Drahtgeflecht (S)  |       |       |       |       | X     |       |        |
| Adern: Folie (F)          |       |       | X     | X     |       | X     | X      |

### Glasfaser
Lichtwellenleiter (kurz LWL) sind *um ein Vielfaches schneller als Kupferkabel*. Außerdem sind diese *weniger störanfällig* gegenüber elektromagnetischen Einflüssen, da per Laser nur Lichtimpulse übertragen werden. Glasfaserkabel sind damit einhergehend deutlich *filigrane und teurere Ware*.

#### Single-Mode
XXX

#### Multi-Mode
XXX

### Koaxialkabel
XXX
