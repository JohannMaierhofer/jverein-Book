# Projektsaldo

## Aktivierung

Zur Nutzung der Projekte ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.


## Einstellungen

Unter Administration->Buchführung->Projekte werden die Projekte angelegt bzw. bearbeitet.

## Projekt-Saldo

In Anlehnung an die Funktion Buchungsklassensaldo liefert die Funktion Projekt-Saldo, die über Buchführung->Projekte aufgerufen wird, die Einnahmen und Ausgaben aller Projekte gruppiert nach Buchungsarten. Auch die Salden aller Einnahmen und Ausgaben je Projekt sowie der jeweilige Projektgewinn werden ermittelt.

Neben der Anzeige aller Projekte lassen sich über die Projekteingabe auch nur einzelne Projekte anzeigen. In der Auswahlliste für die Projekte wird nach Projekten gefiltert die im ausgewählten Zeitraum aktiv sind. Projekte die vor dem Von Datum beendet wurden oder nach dem Bis Datum beginnen werden ausgefiltert.

Bei der Anzeige eines einzelnen Projektes wird das Saldo über alle Projekte nicht ausgegeben, es gibt ja nur eines.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_ProjektSaldoView.png" alt="" /></picture>

Das jeweilige Geschäftsjahr lässt sich über die Schnellzugriff Buttons auswählen. Mit den Navigations Pfeilen lässt sich die Zeitachse um jeweils 5 Jahre verschieben. Mit dem Zurück Button kommt man zum aktuellen Geschäftsjahr zurück.

Der aktuell ausgewählte Zeitraum wird angezeigt.

Über die Suchen Funktion lassen sich beliebige Zeiträume auswählen.

Mit den den Navigations Pfeilen lässt sich der ausgewählte Bereich nach vorne oder hinten verschieben.

Beginnt das Von Datum an einem Monatsanfang und endet das Bis Datum an einem letzten Tag eines Monats, wird Monatsweise geblättert. Andernfalls mit der Anzahl der Tage des Zeitbereichs.

Um sich wiederholende Projekte z.B. Jahresweise vergleichen zu können, kann entweder für jedes Jahr ein neues Projekt mit Jahreszahl (z.B. "St. Martin 2013", "St. Martin 2014" usw.) verwendet werden. Dann erhält man bei einem mehrjährigen Datumsbereich die einzelnen Projekte in einer Liste (wie im Beispiel des obigen Screenshots).

Alternativ kann man aber auch stets dasselbe Projekt verwenden (z.B. "St. Martin") und dann für einen Mehrjahresvergleich die Auswertung mit unterschiedlichen Datumsbereichen (je Jahr) mehrmals abrufen.

Die Tabelle kann als fester PDF Report ausgegeben werden.

Das Kontextmenü bietet folgende Einträge:
* Bearbeiten: Bei Auswahl der Projekt Zeile lässt sich das entsprechende Projekt editieren. Bei Auswahl einer Buchungsart Zeile lässt sich die Buchungsart editieren
* Buchungen anzeigen: Zeigt bei Auswahl einer Buchungsart Zeile die enthaltenen Buchungen an
* Steuerbuchungen anzeigen: Zeigt bei Steuerbuchungsarten die Buchungen an die zur Steuer beitragen

### Buchungen

Die Liste aller Buchungen (Buchführung->Buchungen) kann auf ein Projekt, ggf. auch mit Datumseingrenzung, gefiltert werden. So erhält man die Liste aller Buchungen zu einen Projekt, die auch als PDF- oder CSV-Datei ausgegeben werden kann.
