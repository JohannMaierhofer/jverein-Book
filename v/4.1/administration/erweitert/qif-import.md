# QIF Datei-Import

## Starten des Dialoges

Sie finden den Dialog in

* JVerein
  * Administration
    * Buchführung
      * QIF Datei-Importieren

## Wann verwende ich den Dialog

Möchten Sie auf JVerein wechseln und Ihre alten Buchungen aus dem früheren Programmen übernehmen, unterstützt Sie dieser Dialog bei der einmaligen Übernahme aller Buchungen.

Voraussetzungen damit dieser Dialog verwendet werden kann sind:

* Ihr altes Programm exportiert in QIF Dateien
* JVerein enthält noch keine Buchungen
* JVerein enthält noch keine Anfangsbestände von Konten

## Allgemeines

Viele Programme wie z.B. Quicken exportieren ihre Buchungen in Dateien, die das QIF Format verwenden.

Dieses Format ist leider nicht sehr exakt definiert und überlässt den Entwicklern viel Freiräume, was den Import nicht gerade vereinfacht.

Das hier vorliegende Import-Modul orientiert sich an folgender Dokumentation: Quicken Interchange Format und wurde mit Exports aus verschiedenen Quicken Versionen getestet.

## Überblick

Der Import von QIF Buchungen läuft in folgenden Schritten:

* Buchungen im alten Programm exportieren
* Konten in JVerein anlegen
* Buchungsgruppen und Buchungsarten in JVerein anlegen
* QIF Dateien in JVerein einlesen
* Buchungsarten den externen zuordnen
* eventuell Mitglieder zuordnen
* JVerein Datenbank sichern
* Buchungen übernehmen

## Vorbereitungen

### Vorbereitung in JVerein

Dieser Dialog unterstützt bei der ersten Übernahme von Buchungen beim Umstieg auf JVerein aus dem früher verwendeten Programm.

In JVerein müssen dazu die Konten angelegt werden, für die Buchungen importiert werden sollen.

Geben Sie weder ein Eröffnungsdatum, noch einen Anfangssalto an, weil diese Daten mit dem Import gesetzt werden. Legen Sie auch nur die Konten an die für den Import benötigt werden.

Möchten Sie weitere Konten in JVerein führen, können Sie diese später anlegen, nachdem der Import abgeschlossen wurde.

Nun müssen Sie noch die Buchungsklassen und Buchungsarten in JVerein anlegen. Prüfen Sie dabei gleich, ob Sie jeder Buchungsart des alten Programmes eine neuen Buchungsart aus JVerein zuordnen könnten.

Sollen Buchungen Mitgliederkonten zugeordnet werden, müssen alle Mitglieder in JVerein angelegt sein.

### Vorbereitung im alten Programm

Exportieren Sie die Buchungen eines jeden Kontos in eine eigene QIF Datei.

Auch wenn das Programm die Möglichkeit bietet, alle Konten in eine Datei zu exportieren, wird der Import dieser Dateien von JVerein nicht unterstützt.

Bei Tests mit Quicken hat sich herausgestellt, das Buchungen in der Datei fehlen, wenn mehrere Konten in eine Datei exportiert werden.

So lässt Quicken bei Umbuchungen zwischen Konten die Belastungsbuchung weg. Wurde das Konto mit der Entlastungsbuchung bereits geschlossen, exportiert Quicken diese Kontodaten gar nicht und lasst damit den Transfer komplett weg, was zu falschen Kontoständen führt.

## Import durchführen

### Schritt 1 - Dateien importieren

Die Übernahme der Buchungen beginnt mit dem Einlesen der QIF Dateien in JVerein. Dieser Vorgang ändert noch keine Buchung in JVerein, ist harmlos und kann jederzeit wiederholt werden.

Die Daten der QIF Dateien werden in JVerein in den Tabellen QIFImportHead und QIFImportPos eingetragen und können hier mit den nächsten Arbeitsschritten weiter für die Buchungsübernahme vorbereitet werden.

Das Einlesen einer Datei läuft innerhalb einer Datenbank Transaktion. Das bedeutet, wenn beim Einlesen ein Fehler auftritt, werden aus diese Datei keinerlei Daten übernommen. Sie bekommen immer alles oder gar nichts.

Lesen Sie nach und nach für alle gewünschten Konten die QIF Dateien an.

Nach dem Einlesen einer Datei wird der Name des Kontos in der Auswahlbox Externes Konto aufgenommen.

Wählen Sie hier das Konto aus und prüfen Sie die eingelesenen Daten, vor allem ob Eröffnungssalto und Gesamt Salto mit den Angaben im alten Programm überein stimmen.

Möchten Sie einen Import wiederholen, können Sie jederzeit den Import eines Kontos oder aller Konten löschen, in dem Sie die Schalter Import Löschen oder Imports Löschen verwenden.

### Schritt 2 - JVerein Konto zuordnen

Ordnen Sie den externen Konten jeweils ein Konto in JVerein zu.

Wählen Sie dazu im Bereich Konto Kopfdaten über die Auswahlbox Externes Konto ein importiertes Konto aus.

Wählen Sie nun im Bereich Zugeordnetes Konto in JVerein.. über die Auswahlbox JVerein Konto das dazugehörige Konto in JVerein. Diese Auswahl wird sofort gespeichert.

Prüfen Sie ob allen externen Konton ein JVereinskonto zugeordnet ist. Wenn Sie ein externes Konto auswählen, wird das zugeordnete JVereins Konto angezeigt.

### Schritt 3 - Buchungsart zuordnen

Wenn Sie den Schalter Buchungsarten zuordnen drücken, wechseln Sie in eine Ansicht, die alle externen Buchungsarten und deren Zuordnung zu JVereins Buchungsarten zeigen und ändern lassen. Buchungen, die keine externe Buchungsart haben, werden einzeln dargestellt und müssen hier auch einzeln bearbeitet werden.

Diese Ansicht bietet folgende Möglichkeiten

* externe Buchungsart einer JVereins Buchungsart zuordnen
* externe Buchungart zum Import sperren
* für eine Buchungsart festlegen, ob Mitgliedskonten referenziert werden können.

Wählen Sie eine Buchungsart in der Liste an, so können Sie auf der Seite Beispielbuchungen einzelne Buchungen zu dieser Buchungsart anschauen und damit leichter entscheiden, welche JVereins Buchungsart diesen Buchungen entspricht.

Wählen Sie die JVereinsbuchungsart aus der Auswahlbox JVerein Buchungsart aus und bestätigen Sie diese Auswahl mit dem Schalten Speichern.

In der Spalte Status zeigt Ihnen nun ein grüner Haken, dass Sie diese Zeile bearbeitet haben und in der Spalte JVerein Buchungsart sehen sie die zugeordnete Buchungsart.

Möchten Sie später Buchungen in Mitgliedskonten übernehmen, dann setzen Sie in den entsprechenden Buchungsarten einen Haken in der Box Für Mitgliedskonto. Speichern Sie diese Änderung mit dem Schalter Speichern.

Sie sehen nun für diese Buchungsarten in der Spalte Mitgliedskonto den Text Buchung im Mitgliedskonto möglich

Haben Sie Buchungsarten die sie nicht übernehmen möchten, z.B. mit Betrag 0 oder Buchung und Korrekturbuchung die sich gegenseitig aufheben, dann können Sie bei solchen in der Box Nicht importieren einen Haken setzen. Speichern Sie diese Änderung mit dem Schalter Speichern.

Sie sehen für diese Buchungsarten in der Spalte Status ein Schloss.

### Schritt 4 - Mitglied zuordnen

Sollen Buchungen in Mitgliedskonten importiert werden, müssen Sie die Namen der externen Buchungen den entsprechenden Mitgliedskonten in JVerein zuordnen.

Öffnen Sie die Ansicht zum Zuordnen der Mitglieder durch Drücken auf den Schalter Mitglieder zuordnen.

Es werden Ihnen alle Namen der externen Buchungen angezeigt, bei denen Sie in der Buchungsart einen Haken in Für Mitgliedskonto gesetzt hatten.

Wählen Sie einen Namen in der Liste an, wird die Auswahlbox JVerein Mitglied mit passenden Namen gefüllt.

Suchen Sie aus der Auswahlbox das Mitgliedskonto, das sie zuordnen möchten und speichern dies durch Drücken auf den Schalter Zuordnung Speichern.

Wird in der Auswahlbox der gewünschte Name nicht mit angezeigt, dann setzen Sie einen Haken in die Box alle Mitglieder anzeigen. Die Auswahlbox enthält nun alle Mitgliedsdaten.

Prüfen Sie die angezeigten Beispielbuchungen, ob diese in das Mitgliedskonto übernommen werden sollen.

### Schritt 5 - JVereins Datenbank sichern

Bis zu diesem Schritt werden die externen Buchungen nur in Tabellen für den Import gespeichert. Alle Einstellungen erfolgten in diesen Tabellen und haben keine Auswirkung auf Konten oder Buchungen in JVerein.

Mit dem nächsten Schritt ändert sich dies und deshalb ist das der richtige Zeitpunkt eine Datensicherung für JVerein durchzuführen.

Erkennen Sie dass der Import nicht das gewünschte Ergebnis brachte, wollen Sie immer zu den jetzt aktuell vorhandenen Datenbestand zurück kehren können.

### Schritt 6 - Buchungen importieren

Haben Sie alle Schritt 1 - 5 erfolgreich abgearbeitet und zeigen die angezeigten Buchungen die erwarteten Daten, dann können Sie nun die Buchungen in JVerein importieren.

Drücken Sie den Schalter Buchungen übernehmen.

Es werden die importieren Daten geprüft und die JVerein Konten geprüft.

Allen externen Buchungen muss eine Buchungsart in JVerein zugeordnet sein oder die Buchung muss für die Übernahme gesperrt sein.

Alle Dateien muss einem Konto in JVerein zugeordnet sein.

Das Konto in JVerein darf keine Buchungen enthalten, das Konto darf keinen Anfangsbestand enthalten.

Sie alle Bedingungen erfüllt werden Sie nochmals gefragt, ob die Buchungen übernommen werden sollen.

Bestätigen Sie diese Frage, startet der Import.

* Alle Buchungen werden in den zugewiesenen Konten getätigt.
* Wenn eingestellt, werden Referenzbuchungen im Mitgliedskonto durchgeführt
* Im zweiten Durchlauf wird für jedes Konto und jedes Jahr ein Anfangsbestand ermittelt und gespeichert
* Für jedes Konto und jedes "alte" Jahr werden Jahresabschlüsse gespeichert.

Diese Aktionen laufen in einer Datenbank Transaktion. Das bedeutet sie bekommen entweder alles oder nichts. Tritt beim Buchen ein Fehler auf, werden alle Änderungen zurück genommen.
