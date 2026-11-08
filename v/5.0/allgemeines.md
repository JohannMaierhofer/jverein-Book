# Allgemeines

## JVerein Menü

Das Jverein Menü wird in der oberen Leiste angezeigt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_jverein_menu.png" alt="" /></picture>

Das Jverein Menü bietet folgende Menüeinträge:
* Über: Zeigt die JVerein Version und Datenbank Version an
* Lizenzinformationen: Listet die verwendeten Lizenzen auf
* Neues Mitglied: Öffnet die Ansicht für ein neues Mitglied
* Neue Buchung: Öffnet die Ansicht für eine neue Buchung
* Neuer Abrechnungslauf: Öffnet den Abrechnungslauf Dialog
* Erweitert-> Belege prüfen: Prüft die Belege auf Konsistenz

## Panel Buttons

In der Panelleiste oben sind verschiedene Buttons verfügbar. Sie werden bei Ansichten mit Tabellen angezeigt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_Panelbuttons.png" alt="" /></picture>

Die ersten drei Buttons werden von JVerein bereit gestellt:
* Spaltenauswahl: Es lässt sich auswählen, welche Spalten in der Tabelle angezeigt werden sollen
* CSV: Gibt die ausgewählten Spalten der angezeigten Tabelle als CSV Datei aus
* PDF: Gibt die ausgewählten Spalten der angezeigten Tabelle als PDF aus

### Spaltenauswahl

Beim Spaltenauswahl Dialog erfolgt eine Dialogabfrage in dem man die anzuzeigenden Spalten auswählen kann. 

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_SpaltenauswahlDialog.png" alt="" /></picture>

Buttons:
* Hilfe: Zeigt diese Hilfe an
* Reset: Setzt die selektierten Spalten auf Defaultwerte zurück
* Speichern: Übernimmt die Auswahl in die Tabelle
* Abbrechen: Beendet den Dialog

Außerdem kann die Auswahl der Spalten über einen Rechtsklick auf den Tabellenkopf der jeweiligen Tabelle erfolgen.

### Profile

Für die CSV/PDF Export Dialoge lassen sich Profile erstellen.

Buttons:
* Neu: Erzeugt ein neues Profil mit den aktuellen Einstellungen des Dialogs
* Speichern: Überschreibt das ausgewählte Profil mit den aktuellen Einstellungen des Dialogs
* Löschen: Löscht das ausgewählte Profil 
* Anwenden: Setzt die im Profil gespeicherten Daten im Dialog


### CSV Export Dialog

Die im Dialog ausgewählten Spalten lassen sich als CSV exportieren.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogCSV.png" alt="" /></picture>

Buttons:
* Hilfe: Zeigt diese Hilfe an
* Reset: Setzt die selektierten Spalten auf Defaultwerte zurück
* Starten: Startet den Export der Daten
* Abbrechen: Beendet den Dialog

PS: Die Spaltenreihenfolge lässt sich durch Umsortieren (Drag & Drop) mit der Maus ändern.

### PDF Export Dialog

Die im Dialog ausgewählten Spalten lassen sich als PDF exportieren.

Allgemeine Buttons:
* Hilfe: Zeigt diese Hilfe an
* Starten: Startet den Export der Daten
* Abbrechen: Beendet den Dialog

#### Spalten Lasche

In de Lasche Spalten werden die zu exportierenden Spalten ausgewählt und es lässt sich das relative Verhältnis der Spaltenbreiten im PDF Report einstellen.
 
Defaultmäßig werden die Breiten aus der angezeigten Tabelle übernommen. Die Breiten sind keine absoluten Werte sondern geben nur das Verhältnis der Breiten zueinander an. Bei der Ausgabe wird die verfügbare Breite im PDF im Verhältnis der Breitenwerte aufgeteilt. Eine Spalte mit doppeltem Wert von einer anderen Spalte wird also bei der Ausgabe doppelt so breit.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogPDF.png" alt="" /></picture>

Buttons:
* Breiten zurücksetzen: Setzt die Breiten im Verhältnis zur angezeigten Tabelle zurück
* Reset: Setzt die Spaltenauswahl und die Breiten auf Defaultwerte zurück

PS: Die Spaltenreihenfolge lässt sich durch Umsortieren (Drag & Drop) mit der Maus ändern.

Wird ein Report über die Export Buttons z.B. bei den Mitgliedern oder Buchungen generiert fehlt diese Lasche im Dialog weil die entsprechenden Werte im Ausgabecode implementiert sind.

#### Ränder Lasche

Im Ränder Tab kann der Randabstand der Tabelle im PDF Report eingestellt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogRaender.png" alt="" /></picture>

Buttons:
* Reset: Setzt die Werte auf Defaultwerte zurück

#### Formular Lasche

Im Formular Tab kann das Vordergrund und Hintergrund Formular ausgewählt werden, ob Header oder Zellen transparent sein sollen oder ob im Querformat gedruckt werden soll.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogFormular.png" alt="" /></picture>

Buttons:
* Reset: Setzt die Werte auf Defaultwerte zurück

#### Schriftart Lasche

Für die Tabellen Header Zeile und den Tabelleninhalt lässt sich jeweils die Schriftart, Schriftgröße und Hintergrundfarbe (für spezielle Zellen) einstellen. Weiter kann festgelegt werden ob negative Zahlen in roter Farbe ausgegeben werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogSchriftart.png" alt="" /></picture>

#### Optionen Lasche

Die Lasche "Optionen" wird nur angezeigt wenn auch eine Option für den Report vorhanden ist.

Dieser bietet folgende Schalter:
* Filterparameter ausgeben: Für Reports die gefilterte Tabellen ausgeben, kann ausgewählt werden ob am Ende des Reports eine Tabelle mit den aktiven Filtern ausgegeben wird. Die Tabelle wird nur gezeichnet wenn auch mindesten ein Filter aktiv ist
* Zeige Kontonummer in Buchungsliste: Diese Option wird bei, Buchungsexport "PDF Einzelbuchungen" angeboten
* Wirtschaftsplan Ist-Beträge von laufendem Zeitraum ausgeben: Diese Option wird beim PDF Export der Wirtschaftspläne angeboten

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_TabelleExportDialogOptionen.png" alt="" /></picture>

Buttons:
* Reset: Setzt die Werte auf Defaultwerte zurück

## Tastaturkürzel (Shortcuts)

Einige Buttons sind mit Tastaturkürzel hinterlegt. Dies sind:
* Löschen: Entf
* Speichern: Ctrl + S
* Speichern und Neu: Ctrl + Alt + S
* Vor: Ctrl + Pfeil-Rechts
* Zurück: Ctrl + Pfeil-Links
* Hilfe: F1
* Neu: Ctrl + N
* PDF: Ctrl + P
* View ohne Speichern verlassen Dialog: Ohne Speichern Verlassen: Ctrl + SHIFT + W
* Neues Mitglied: Alt + M
* Neue Buchung: Alt + B
* Neuer Abrechnungslauf: Alt + A

