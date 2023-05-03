# Dateiformate
Es gibt eine Reihe von Möglichkeiten wie man *Datensätze aus einer Datenbank exportieren* kann. Welche Methode am besten ist, hängt von Kriterien ab wie: Datentyp, Datenmenge, Zugriffsgeschwindigkeit, Erweiterbarkeit, Implementierungsaufwand.

Um gespeicherte Datensätze zu exportieren, kann man sich einerseits ein *SQL-Skript generieren*, welches die gesamte Datenbank abbildet. Um die Daten in anderer Software bearbeiten zu können, bietet sich diese Form jedoch nicht an. Es wird in der Regel auf das *Tabellenformat CSV* oder Modelle der Markup-Sprache *XML* gesetzt.

## CSV
Ein sehr verbreitetes Import- und Exportformat für Datenbanken und Tabellenkalkulationen ist das CSV-Format (engl. „Comma Separated Values“). *CSV-Dateien sind Textdateien, die zeilenweise Datensätze enthalten* welche mit Trennzeichen (Semikolon oder Komma) versehen sind. Dabei ist die erste Zeile meistens der *Tabellenkopf mit Datenbezeichnungen*. Die Stärke der CSV ist ihre *Einfachheit* und *Kompatibilität*, jedoch wird diese bei größeren Datenmengen *inperformant*.

```
Marke;Modell;Leistung
Porsche;911;350
Skoda;Octavia;140
Audi;Q3;110
```

## XML
Das XML-Format (engl. „Extensible Markup Language“) ist ein alternatives Dateiformat zu CSV. Dieses Format bildet eine *hierarchisch aufgebaute Datenstruktur* (erweiterbar), welche in einem lesbaren Textformat verfasst ist. Das XML-Format ist besonders in der Informatik verbreitet. Es bildet Datenstrukturen korrekt ab und lässt sich *performant einlesen*. Nachteil ist der erhöhte Aufwand beim Einlesen der Daten in fremder Software. Mit „XPath“ können Knoten adressiert werden.

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<autohaus>
   <auto>
      <marke>Porsche</marke>
      <modell>911</modell>
      <leistung>350</leistung>
   </auto>
   <auto>
      <marke>Skoda</marke>
      <modell>Octavia</modell>
      <leistung>140</leistung>
   </auto>
   <auto>
      <marke>Audi</marke>
      <modell>Q3</modell>
      <leistung>110</leistung>
   </auto>
</autohaus>
```

### Wohlgeformtheit
Der Begriff Wohlgeformtheit, der Ihnen im Zusammenhang mit XML immer wieder begegnen wird, bedeutet, dass eine Datei die Regeln von XML korrekt einhält. Es handelt sich in folgenden Fällen um eine wohlgeformte XML-Datei:
- am Beginn steht der Seite *XML-Deklaration*,
- es gibt *mindestens ein Datenelement*,
- alle Datenelementen haben ein äußerstes Element,
- Tags werden nicht über Kreuz geschlossen.

### Gültigkeit
Was noch fehlt, ist der *Bezug zu einer DTD* (engl. „Document Type Definition“), in der die verwendeten *Elemente definiert* sind. Deshalb kann man über das Beispiel sagen, *es ist wohlgeformt, aber nicht gültig*. Gültigkeit erreicht das Dokument, wenn das Objektmodell der XML-Datei erfolgreich gegen ein DTD validiert worden ist. Ein DTD *legt Elemente, Attribute und Entitäten fest*, welche dem Dokument seine Struktur vorgeben und die Verarbeitung erleichtern. Die Dokumenttyp-*Deklaration muss am Anfang des Dokuments* (nur durch den XML-Header vorangestellt) angezeigt. Es ist nicht erlaubt irgendwo anders innerhalb im Dokument.

``` xml
<!DOCTYPE address [
   <!ELEMENT address (name,company,phone)>
   <!ELEMENT name (#PCDATA)>
   <!ELEMENT company (#PCDATA)>
   <!ELEMENT phone (#PCDATA)>
]>
```

## JSON
