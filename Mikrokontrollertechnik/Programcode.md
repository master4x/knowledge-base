Die Programmiersprache von Arduino kann in drei Hauptteile unterteilt werden: *Struktur*, *Werte* (Variablen und Konstanten) und *Funktionsbasis*. Die Struktur bilden Elemente der [[Arduino]] (C++) Programmiersprache mit den *Sketchfunktionen* `setup()` und `loop()` sowie (bitweise) *Operatoren* und *Syntax*. Für Variablen können bekannte Datentypen der C-Ableger verwendet werden. Im Bereich Funktionenbasis können vordefinierte Funktionen, ähnlich zu komplexeren Sprachen wie Java, eingesetzt werden um *Berechnungen effizienter durchzuführen*.

# Beispiele

## Digital I/O
- `digitalRead(pin)`
- `digitalWrite(pin, value)`
- `pinMode(pin, mode)`

## Analog I/O
- `analogRead(pin)`
- `analogWrite(pin, value)`

## Timer/Counter
- `delay(ms)`
- `micros()`
- `millis()`

## Mathe
- `map(value, fromLow, fromHigh, toLow, toHigh)`
- `min(x, y)`
- `max(x, y)`

## Zufall
- `random(min, max)`
- `randomSeed(seed)`
