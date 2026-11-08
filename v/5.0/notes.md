# Release Notes

## Allgemeines

Die Version 5.0 ist eine Major Version und nicht rückwärts kompatibel mit einer 4.x.

Man kann also mit einer migrierten Datenbank nicht mehr auf eine ältere Version von JVerein zurück. Es empfiehlt sich ein Backup der Datenbank vor dem Update anzulegen. Mit diesem kann auch wieder eine ältere Version benutzt werden.

Gründe für die Inkompatibilität:
* Für die Belegverwaltung musste die Datenbank Struktur geändert werden
* Löschung des Supports für Kursteilnehmer
* Umwandlung der Datenbank Attribute für Beträge von Double nach Decimal. Dies erlaubt eine exakte Speicherung von Beträgen ohne die Rundungsprobleme die mit der Format bedingten Umwandlung von Beträgen in das Fließkomma Format entstehen
* Unterstützung der neueren H2DB Version


## The Big Ones

### Support für Kursteilnehmer entfernt !!!

* Das Feature Kursteilnehmer ist veraltet und wurde aus dem Code entfernt
* Auch die entsprechenden Daten in der Datenbank wurden gelöscht
* Werden Kursteilnehmer als Nicht-Mitglieder weiter benötigt, müssen sie in der 4.3 in Nicht-Mitglieder umgewandelt werden
* Sollten Listen der Daten benötigt werden, so müssen sie noch mit der 4.3 generiert werden

### Unterstützung einer aktuellen H2DB version

Da die alte Version der H2 Datenbank fehlerhaft war und immer wieder zu Problemen führte wird jetzt die Migration zu einer aktuellen Version der Datenbank unterstützt.

Die Datenbank Version wird von Jameica bereitgestellt. Sie ist dort in einer Version höher als 2.12 enthalten, also ab der 2.13.0-nightly.

Die Option einer Migration wird beim Start von JVerein als Message Box angezeigt falls eine entsprechende Jameica Version installiert ist. Über einen Button lässt sich die Migration starten. Es wird dabei eine neue Datenbank mit neuem Namen erzeugt. Die alte Datenbank bleibt unverändert.

### Lokale Dokumentspeicherung

Neben der Speicherung von Dokumenten über Jameica Messaging (bisherige Methode) kann in den Einstellungen diese Option abgewählt werden. Dann erfolgt die Speicherung der Dokumente lokal.

Unter Administration->Einstellungen->Belege können die Wurzelverzeichnisse für die Dokumentspeicherung gesetzt werden. Diese können geändert werden wenn die Dokumente verschoben werden bzw. auf einen anderen Benutzer übertragen werden. Die Verzeichnisse stehen nicht in der Datenbank sondern sind lokal gespeichert.

Unter Administration->Einstellungen->Vorlagen lassen sich die relativen Pfade für die Belege mit Variablen definieren. Ein Beleg wird unter dem  Wurzelverzeichnis und dem relativen Pfad zusammengesetzt.


### Belegverwaltung

 Alle hinterlegten Belege werden in einem neuen View (Buchführung->Belege) angezeigt. Hier gibt es auch eine Filter Möglichkeit.
 
Belege (Dokumente) lassen sich bei den Buchungen und Mitgliedern erstellen aber auch direkt aus der Anzeige der Liste. Erstellte Belege lassen sich auch nachträglich einer Buchung bzw. einem Mitglied zuordnen. Es ist z.B. auch möglich, einen Beleg mehreren Buchungen zuzuordnen. Ein Beleg kann auch von einer Buchung entfernt werden ohne ihn zu löschen.

Über einen Menüpunkt Eintrag lassen sich die Belege auf Konsistenz prüfen.

Datenbank bereinigen löscht auch Belege.

## Kleinere Korrekturen, Erweiterungen oder Modifikationen

### Weitere PDF Export Optionen

Im Export Dialog für PDF Reports gibt es einen neuen Reiter "Optionen". Er wird nur angezeigt wenn auch eine Option für den Report vorhanden ist.

Dieser bietet folgende Schalter:
* Filterparameter ausgeben: Für Reports die gefilterte Tabellen ausgeben, kann ausgewählt werden ob am Ende des Reports eine Tabelle mit den aktiven Filtern ausgegeben wird. Die Tabelle wird nur gezeichnet wenn auch mindesten ein Filter aktiv ist
* Zeige Kontonummer in Buchungsliste: Diese Option wird bei, Buchungsexport "PDF Einzelbuchungen" angeboten
* Wirtschaftsplan Ist-Beträge von laufendem Zeitraum ausgeben: Diese Option wird beim PDF Export der Wirtschaftspläne angeboten

### Gesperrt Spalte

Bei Tabellen gibt es eine neue Spalte "Gesperrt" bzw. "Abgeschlossen". Sie ist standardmäßig ausgeblendet. Sie zeigt ein Schlosssymbol wenn der Eintrag nicht gelöscht werden kann. 

### Weitere Variablen bei Zusatzbeträgen

Bei den Buchungstext Variablen von Zusatzbeträgen werden weitere Variablen unterstützt.
* Abrechnungslauf Variablen
* Variablen aus Feldern des Zusatzbetrags wie z.B. die Fälligkeit des Zusatzbetrags


## Sonstiges

* Bei Rechnungsformularen sind in den Variablen jetzt auch die Attribute des Zahlers verfügbar
* Im Filterbereich der Zusatzbeträge sind weite Filter Optionen bereitgestellt
* Mitgliedskonto Tab bei den Mitgliedern und Nicht-Mitgliedern in Sollbuchung umbenannt
* Zahlung Tab bei den Mitgliedern umstrukturiert
* Eigener Defaultwert für den Zahlungsweg von Nicht-Mitgliedern unter Einstellungen->Abrechnung
* Im Rechnung View gibt es einen neuen Button um die Rechnung anzuzeigen

