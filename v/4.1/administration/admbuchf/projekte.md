# Projekte

## Aktivierung

Zur Nutzung der Projekte ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

Anschließend sollte JVerein neu gestartet werden, damit der Menüpunkt "Projekte" zur Verfügung steht.

## Allgemeines

Innerhalb der Buchführung können Buchungen zu Projekten zusammengefasst werden. Siehe auch [https://jverein-forum.de/viewtopic.php?f=4\&t=646](https://jverein-forum.de/viewtopic.php?f=4\&t=646)

Die Verwendung von Projekten ist dann sinnvoll, wenn die Informationen, die die normalen Auswertungen liefern, für bestimmte Fragestellungen nicht genügen. Üblicherweise werden die Buchungsklassen und die Buchungsarten darin so angelegt wie es z.B. für steuerliche Gründe sinnvoll oder gar vorgegeben ist. Buchungen, die sachinhaltlich zusammengehören, müssen dann meist aber auf verschiedene Buchungsarten verteilt werden so dass sich der Sachzusammenhang alleine aus den Salden der Buchungsklasse u.U. nicht mehr ergibt.

Indem bei einer Buchung ein Projekt hinterlegt wird, können zusammengehörige Buchungen über das Projekt ausgewertet werden.

Unter Administration->Buchführung->Projekte werden die Projekte angelegt bzw. bearbeitet.

## Liste der Projekte

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_ProjekteListeView.png" alt="" /></picture>

Mit neu kann ein neues Projekt eingerichtet werden.

Durch einen Doppelklick wird die Bearbeitung eines Projekt eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Löschen: Damit kann ein Projekt, dem keine Buchungen zugeordnet sind, gelöscht werden.

## Projekt

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_ProjektView.png" alt="" /></picture>

## Auswertung

Informationen zu Projekten liefert die Funktion Projekt-Saldo (zu finden unter Buchführung->Projekte), Detailinformation filtert man unter Buchführung->Buchungen.

### Projektsaldo

In Anlehnung an die Funktion Buchungsklassen liefert die Funktion Projekt-Saldo, die über Buchführung->Projekte aufgerufen wird, die Einnahmen und Ausgaben aller Projekte gruppiert nach Buchungsarten. Siehe [Projektsaldo](../../buchf/projekte.md)

### Buchungen

Die Liste aller Buchungen (Buchführung|Buchungen) kann auf ein Projekt, ggf. auch mit Datumseingrenzung, gefiltert werden. So erhält man die Liste aller Buchungen zu einen Projekt, die auch als PDF- oder CSV-Datei ausgegeben werden kann.
