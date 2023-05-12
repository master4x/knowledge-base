# Anomalien
Es existieren drei Arten von Datenbank-Anomalien, die Einfügeanomalie, die Änderungsanomalie und die Löschanomalie. Hierzugezählt werden darf das Auftreten von Redundanz.

In der Datenbankentwicklung ist die [[Normalisierung#Dritte Normalform|dritte Normalform]] oft ausreichend, um die perfekte *Balance aus [[Anomalien#Sonstige#Redundanz|Redundanz]], Performance und Flexibilität* für eine Datenbank zu gewährleisten. *Sie eliminiert auch die meisten Anomalien* in einer Datenbank, aber nicht alle.

## Einfügeanomalie
Die Einfügeanomalie (engl. „**Insert**“) beschreibt das *Einfügen unvollständiger Datensätze*. In vielen Fällen führt sie zu einer inkonsistenten Darstellung des Realitätsausschnittes.

## Änderungsanomalie
Die Änderungsanomalie (engl. „**Update**“) ist das manuelle, *unvollständige Ändern* von einzelnen Daten oder Datensätzen.

## Löschanomalie
Die Löschanomalie (engl. „**Delete**“) beschreibt das *unbeabsichtigte Löschen* von noch brauchbaren (oder noch zu gebrauchenden) Datensätzen.

## Sonstige

### Redundanz
Eine Redundanz beschreibt das *mehrfache Vorhandensein identischer Daten*(-sätze). Redundanzen in Datenbanken sind ein Zeichen für ein *schlechtes Datenbankdesign*, kann aber der performant Suchergebnisse liefern.
