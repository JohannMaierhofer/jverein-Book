# Anlagenbuchungen

### Aktivierung

Zur Nutzung der Anlagenkonten ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

### Buchungsliste

Im View Anlagenbuchungen werden Buchungen von Anlagenkonten angezeigt. Auch bei der Auswahl des Kontos werden nur Anlagenkonten angeboten.

Im Prinzip gibt es hier die gleichen Funktionen wie auch im Buchungen View, allerdings reduziert um nicht benötigte Optionen. Der View wurde eingeführt um den [Buchungen](buchungen.md) View nicht unnötig mit Anlagenkonten zu überfüllen.

Ist unter Administration->Einstellungen->Anzeige eingestellt, dass die AfA Buchungen über den Button in diesem View erzeugt werden sollen, dann ist hier der entsprechende Button verfügbar.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_AnlagenbuchungenListeView.png" alt="" /></picture>

Folgende Buttons sind vorhanden:
* Import: (siehe unten)
* Export: (siehe unten)
* Neu: Neue Buchung erzeugen

Import bietet die Auswahl einer Quelle:
* CSV-Buchungsimport: Import von Buchungen aus einer CSV Datei. Siehe [Buchungsimport](buchungsimport.md). Hier ist die Auswahl des in der Datei verwendeten Encodings notwendig

Export bietet die Auswahl verschiedener Ausgaben an:
* CSV Buchungen: Die über die Suchkriterien ausgewählten Buchungen können als CSV-Datei ausgegeben werden. Dabei werden bei Nutzung des Mitgliedskontos ggfls. auch die Daten des Mitgliedes ausgegeben.
* PDF Buchungsjournal: Auflistung aller Buchungen nach verschiedenen Sortierungen
* PDF Einzelbuchungen: Auflistung aller Buchungen nach Buchungsarten
* PDF Summenbuchungen: Ausgabe der Summen pro Buchungsart

Die PDF-Auswertungen sind hier abrufbar. Ausführlich beschrieben werden sie im Artikel [Buchführung Zusammenhänge](../../../sonstiges/buchfuhrung-zusammenhange.md).

Buchungen Menü:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_AnlagenbuchungenMenue.png" alt="" /></picture>

Für eine Beschreibung der Behandlung von Anlagenkonten siehe [Konten](konten.md).
