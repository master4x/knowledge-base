Wir rechnen im Alltag mit dem Dezimalsystem (lat. _decimus_, der Zehnte) und verwenden dabei die zehn Ziffern 0, 1, ... 9. Der Wert einer Ziffer in einer Zahl hängt von ihrer Stelle ab, die erste 3 in 373 hat z.B. einen anderen Wert als die zweite 3, nämlich drei**hundert** und nicht drei. Im Dezimalsystem entspricht jeder Stelle eine Potenz der Basis 10: 100=1, 101=10, 102=100 usw.

# Dezimales Zahlensystem
**Nennwerte:** 0, 1, 2, 3, 4, 5, 6, 7, 8, 9
**Basis/Suffix:** 10
**Größter Nennwert:** 9

# Duales Zahlensystem (Binärsystem)
**Nennwerte:** 0, 1
**Basis/Suffix:** 2
**Größter Nennwert:** 1

# Hexadezimales Zahlensystem
**Nennwerte:** 0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F
**Basis/Suffix:** 16
**Größter Nennwert:** F

# Oktales Zahlensystem
**Nennwerte:** 0, 1, 2, 3, 4, 5, 6, 7
**Basis/Suffix:** 8
**Größter Nennwert:** 7

# Umrechnung
## Duales nach Dezimales System
Jede Stelle der Zahl hat den Wert der entsprechenden 2er-Potenz. Die der ersten Ziffer von rechts entsprechende Potenz ist 2º = 1. Nimm jede Ziffer mal mit der entsprechenden Potenz und summiere. Gehe am besten von rechts nach links vor:

```
0 · 1 = 0
1 · 2 = 2
0 · 4 = 0
1 · 8 = 8
        ——
        10 => 1010
```

## Dezimales nach Duales System
1. Teile die Zahl mit Rest durch 2.
2. Der Divisionsrest ist die nächste Ziffer von rechts nach links.
3. Falls der Quotient = 0 ist, bist du fertig, andernfalls nimm den Quotienten als neue Zahl.

```
10 : 2 =  5  Rest: 0
5 : 2 =  2   Rest: 1
2 : 2 =  1   Rest: 0
1 : 2 =  0   Rest: 1

Resultat: 1010 => 10
```
