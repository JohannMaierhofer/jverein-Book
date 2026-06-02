# Anlagenverzeichnis

### Aktivierung

Zur Nutzung der Anlagenkonten ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

### Verzeichnis

Das Anlagenverzeichnis basiert auf steuerlichen Vorgaben.

Es listet alle Anlagenkonten auf die noch nicht geschlossen sind.

Über die Buchungsklasse in den [Anlagenkonten](konten.md) lässt sich eine Gruppierung erreichen.

Die Liste zeigt unter anderem:

* Anschaffungsdatum und Anschaffungskosten
* Buchwerte zu Anfang und Ende des Geschäftsjahres
* Zugänge und Abgänge im Geschäftsjahr
* Getätigte Abschreibungen im Geschäftsjahr

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_AnlagenverzeichnisView.png" alt="" /></picture>

Der Inhalt der Tabelle lässt sich über die entsprechenden Buttons als festes PDF exportieren. Da die Breite der Seite beschränkt ist werden zur besseren Lesbarkeit die Spalten Zugang und Abgang weggelassen wenn sie keine Einträge haben.

Das Kontextmenü bietet folgende Einträge:
* Bearbeiten: Bei Auswahl der Anlagenart Zeile lässt sich die entsprechende Buchungsart editieren. Bei Auswahl einer Bezeichnung Zeile lässt sich das entsprechende Konto editieren
* Buchungen anzeigen: Zeigt bei Auswahl von Bezeichnung die enthaltenen Buchungen an

Hinweis:

Die Buchwerte zu Anfang und Ende des Geschäftsjahres werden aus den Anfangsbeständen der Anlagenkonten genommen. Es ist also wichtig, dass beim [Jahresabschluss](jahresabschluss.md) die Checkbox für Anfangsbestände Folgejahr ausgewählt ist. Damit werden die Anfangsbestände generiert.

Das bedeutet auch, dass in der Tabelle der Buchwert für das Ende des Geschäftsjahres erst nach dem Jahresabschluss angezeigt wird.
