# Wirtschaftsplanung

## Allgemeines
In vielen Vereinen ist es laut Satzung oder gelebter Praxis üblich, dass die Mitgliederversammlung den Wirtschaftsplan vorgelegt bekommt und bestätigt. Die Mitgliederversammlung überwacht außerdem, ob der beschlossene Wirtschaftsplan eingehalten wird. Dies bildet die Grundlage für die Entlastung des Vorstands. Mit diesem Modul kann der Vorstand seiner Rechenschaftspflicht einfach nachkommen.

Weiterführende Informationen zur Erstellung eines Wirtschaftsplans sind hier zu finden: https://www.iww.de/vb/vereinsmanagement/vereinsfinanzen-der-haushaltsplan-ein-wichtiges-planungs-und-steuerungsinstrument-fuer-den-verein-f76581

## Aktivierung
Um die Wirtschaftsplanung zu verwenden, aktivieren Sie die entsprechende Option unter Administration → Einstellungen → Anzeige.
Damit die Änderung wirksam wird, starten Sie die Software anschließend neu.

## Liste der Wirtschaftspläne

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_planung_list.png" alt="" /></picture>

In dieser Übersicht werden alle bestehenden Wirtschaftspläne sowie die folgenden Kenndaten angezeigt:
- Bezeichnung
- Zeitraum Von/Bis
- Einnahmen Soll und Ist
- Ausgaben Soll und Ist
- Saldo Soll und Ist
- Differenz zwischen Saldo Soll und Ist

Die Ist-Daten werden automatisch aus der Buchhaltung übernommen. So lässt sich überprüfen, ob der Wirtschaftsplan im aktuellen und in früheren Zeiträumen eingehalten wurde.

Über das Kontextmenü kann der Wirtschaftsplan als PDF exportiert werden. Über Administration -> Einstellungen -> Buchführung lässt sich konfigurieren, ob die Ist-Beträge für den laufenden Zeitraum mit ausgegeben werden sollen.

## Wirtschaftsplan Detailansicht
In der Wirtschaftsplan Detailansicht kann die Zusammensetzung der einzelnen Planungspositionen eingesehen werden.
Übersicht
In der Übersicht sehen Sie die folgenden Kenndaten, die Sie bei Bedarf anpassen können:
- Bezeichnung: Der Name des Wirtschaftsplans. Sie können damit alternative Pläne für denselben Zeitraum unterscheiden.
- Von/Bis: Gibt den Zeitraum an, den der Wirtschaftsplan abdeckt. Sie können beliebige Start- und Enddaten festlegen. Beide Daten sind einschließlich.
- Einnahmen Soll und Ist: Summierung der Plan- bzw. Buchungsdaten
- Ausgaben Soll und Ist: Summierung der Plan- bzw. Buchungsdaten
- Rücklagen gebildet und Rücklagen aufgelöst Ist: Wird nur angezeigt, falls Rücklagenkonten in den Einstellungen aktiviert sind. Zeigt die Ist-Daten der gebildeten und aufgelösten Rücklagen.
- Forderungen und Verbindlichkeiten Ist: Wird nur angezeigt, falls Verbindlichkeitskonten in den Einstellungen aktiviert sind. Zeigt die noch ausstehenden Forderungen und Verbindlichkeiten aus den entsprechenden Konten an.
- Ausgaben inkl. Verbindlichkeiten und Einnahmen inkl. Forderungen Ist: Wird nur angezeigt, falls Verbindlichkeitskonten in den Einstellungen aktiviert sind. Zeit eine Summe Ausgaben und Verbindlichkeiten bzw. Einnahmen und Forderungen. Dient dazu um noch eingehende bzw. ausgehende Zahlungen zu beachten.

## Baumansicht der Planungsdaten

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_planung_tree.png" alt="" /></picture>

Die Planungsdaten werden in einer Baumansicht angezeigt. Zur besseren Übersicht sind sie in Einnahmen und Ausgaben unterteilt. Die Zuordnung erfolgt gemäß der Definition der Buchungsarten. Da sich Umbuchungen gegenseitig aufheben, können sie nicht in die Planung aufgenommen werden.

Falls in den Einstellungen die Rücklagen Option aktiviert ist wird ein dritter Baum angezeigt.

Die Baumansicht besteht aus drei Ebenen, die der Buchführungsstruktur von OpenJVerein entsprechen.

### Buchungsklasse
In der ersten Ebene befinden sich die Buchungsklassen. Sie zeigen eine Zusammenfassung der Plan- und Ist-Daten dieses Bereichs. Eine Bearbeitung der Daten ist hier nicht möglich.

### Buchungsart
In der zweiten Ebenen befinden sich die Buchungsarten. 
Wenn Buchungsarten bereits einer Buchungsklasse zugewiesen sind, erscheinen sie automatisch in der entsprechenden Kategorie der Baumansicht. Buchungsarten ohne eine Zuordnung zu einer Buchungsklasse können über das Kontextmenü zu einer Buchungsklasse hinzugefügt werden.
Zur detaillierten Planung können Planungspositionen angelegt werden (s. unten). Sie können Planungspositionen über das Kontextmenü hinzufügen. Wenn Sie keine Unterteilung wünschen, tragen Sie den gewünschten Betrag direkt in der Spalte „Soll“ ein. Sobald einer Buchungsart zwei oder mehr Planungspositionen zugeordnet sind, wird die Bearbeitung der Spalte „Soll“ automatisch gesperrt.

### Planungsposition
Die dritte Spalte enthält Planungspositionen zur detaillierten Planung der erwarteten Einnahmen bzw. Ausgaben einer Buchungsart. Diese Unterteilung ist besonders dann sinnvoll, wenn eine Buchungsart verschiedene Anteile umfasst, für die eigene Buchungsarten nicht notwendig wären. Planungsdaten für die Positionen können in der Spalte "Soll" festgelegt werden, in der Spalte "Posten" kann eine Bezeichnung für die Position gewählt werden.
Da Planungspositionen nicht direkt in den Buchungen gespeichert werden, ist ein Vergleich mit den Ist-Daten auf Positionsebene nicht möglich.
### Bedienelemente
In der Detailansicht stehen am unteren Rand diese Bedienelemente zur Verfügung:
Hilfe: Öffnet diese Seite
Pfeile vor/zurück: Wechselt durch die verfügbaren Wirtschaftspläne
Export: Es lassen sich zwei Arten von PDF-Exports des Wirtschaftsplans und ein CSV Export auswählen. Über Administration -> Einstellungen -> Reports lässt sich konfigurieren, ob die Ist-Beträge für den laufenden Zeitraum mit ausgegeben werden sollen.
Speichern: Speichert Änderungen am Wirtschaftsplan in der Datenbank.