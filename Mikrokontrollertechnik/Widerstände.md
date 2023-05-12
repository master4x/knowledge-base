# Widerstände

## Pull-Up & Pull-Down-Widerstände
Ein Pullup- bzw. Pulldown-Widerstand wird dazu eingesetzt, um an Eingangspins eindeutig definierte Signalpegel (`LOW` oder `HIGH`) zu erhalten. Ohne einen Pullup- oder Pulldown-Widerstand kann es durch Störungen an einem offenen Eingangspin zu Verfälschungen kommen, sodass falsche Signale vom Mikrocontroller erkannt werden.

## LED-Vorwiderstände
Ein Vorwiderstand ist ein *elektrischer Widerstand*, der in *Reihe zu einer Leuchtdiode* (kurz LED) geschaltet wird, um die elektrische Spannung am bzw. die elektrische Stromstärke durch die LED auf zulässige Werte zu begrenzen.

Mit den folgenden Formeln lassen sich Vorwiderstände für LEDs berechnen:
Vorwiderstand $R_V = \dfrac{U_R}{I}$ ([[Ohmsches Gesetz]])
Betriebsspannung $U_R = U_{ges} - U_D$

**Faustregel**: Alle gängigen einkanaligen LEDs lassen sich an 5V mit einem 120Ω-Widerstand betreiben.
