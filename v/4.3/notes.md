# Release Notes

## Allgemeines

Die Version 4.3 ist eine Minor Version und rückwärts kompatibel mit einer 4.2, 4.1 und 4.0.

## The Big Ones

### Allgemeiner Export bei Tabellen erweitert

Beim Export der Tabellen über die Buttons im oberen Panel wurde ein weiterer Tab zur Konfiguration der Schriftarten hinzugefügt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogSchriftart.png" alt="" /></picture>

Für die Tabellen Header Zeile und den Tabelleninhalt lässt sich jeweils die Schriftart, Schriftgröße und Hintergrundfarbe (für spezielle Zellen) einstellen. Weiter kann festgelegt werden ob negative Zahlen in roter Farbe ausgegeben werden.

### Konfigurierbarkeit von PDF Reports

Für Saldenreports, PDF Reports die über die Export Buttons generiert werden, sowie für Kontoauszug und Personalbogen lässt sich der Report in ähnlicher Weise konfigurieren wie die Tabellenausgabe über die Panel Buttons. Es ist der gleiche Dialog verfügbar allerdings ohne die Spaltenauswahl.

### Lokale Dokumentspeicherung

Neben der Speicherung von Dokumenten über Jameica Messging lassen sich jetzt Dokumente auch lokal speichern. Siehe hierzu die Beschreibung unter [Dokumente](../../sonstiges/dokumente.md).

### Konfigurierbare Rechnungsnummer

Das Format der Rechnungsnummer lässt sich nun unter Administration->Einstellungen->Rechnungen festlegen. Für die Nummer werden Variablen unterstützt.

### Buchungsreport

Über das Kontextmenü der Buchungen lassen sich Buchungsreports generieren z.B. Ersatzbeleg. Der Report basiert auf Nutzer definierten Formularen. Hierfür wurde eine neue Formularart "Buchungsreport" eingeführt. In den Formularen sind neben den allgemeinen Variablen auch die Buchung Variablen verfügbar.

## Kleinere Korrekturen, Erweiterungen oder Modifikationen

### Auswertungen Menüeinträge gelöscht

Die Einträge im Navigationsmenü für Auswertungen wurden entfernt. Die Reports sind jetzt über den Export Button in der Liste der Mitglieder bzw. Nicht-Mitglieder verfügbar. Damit ist für sie auch die Möglichkeit der individuellen Konfigurierbarkeit vorhanden, wie oben beschrieben.

PS: Die Möglichkeit über externe CSV Files die zu exportierenden Spalten zu definieren wurde ebenfalls entfernt. Über die bestehende allgemeine Export Möglichkeit der Tabellen lässt sich ebenfalls festlegen welche Spalten exportiert werden sollen. Darum ist diese Möglichkeit hier nicht mehr nötig.

### Mail Dialog überarbeitet

* "Speichern und Senden" wurde in "Senden" umbenannt, macht aber das gleiche wie bisher und sendet an Empfänger an die die Mail noch nicht versendet wurde
* "Speichern und erneut senden" wurde entfernt. Diese Funktion macht keinen Sinn mehr, weil bereits versendete Mails nicht mehr editiert werden können. Als Alternative gibt es jetzt den Button "Duplizieren". Dieser erstellt eine Kopie der Mail welche sich wieder editieren lässt

Eine bereits versendete Mail lässt sich nicht mehr ändern. Es lassen sich aber neue Empfänger hinzufügen und die gleiche Mail nochmals an die neu hinzugefügten Empfänger versenden, selbst an Empfänger an die sie schon einmal versendet wurde, falls der Empfänger neu hinzugefügt wurde. Beim Empfänger ist nach dem Versenden jeweils gespeichert wann sie an ihn versendet wurde.

### Abrechnungslauf Abschließen überarbeitet

* Ein abgeschlossener Abrechnungslauf kann wieder aufgeschlossen werden
* Die Menüeinträge haben Icons
* Die Tabelle der Abrechnungsläufe hat eine Spalte für Abgeschlossen
* In Abrechnungslauf Tabellenspalten bei Buchung, Sollbuchung und Lastschrift wird im Text ein Icon eingeblendet wenn der Abrechnungslauf abgeschlossen ist und es in den Einstellungen aktiviert ist
* Abschließen und Aufschließen sind ausgegraut wenn das Fälligkeitsdatum in einem Jahresabschluß liegt
* Prenotification wird nicht mehr blockiert
* Löschen wird bei abgeschlossenen Abrechnungsläufen nicht ausgegraut, es gibt aber eine Fehlermeldung. Wenn man in den Einstellungen den Haken wieder weg macht, würde man sich sonst wundern, warum Löschen ausgegraut ist
* Buchungen, Sollbuchungen und Lastschriften von abgeschlossenen Abrechnungsläufen können nicht mehr gelöscht oder editiert werden
* Ein abgeschlossener Abrechnungslauf kann in DBBereinigen gelöscht werden

## Sonstiges

* Einige Fehlerkorrekturen
* Carlito Schriftart (Calibri kompatibel) hinzugefügt
* Falls Konten Buchungen abgeschlossener Geschäftsjahre zugeordnet haben, können nicht mehr alle Felder geändert werden
* Falls Buchungsarten von Buchungen abgeschlossener Geschäftsjahre verwendet werden, können nicht mehr alle Felder geändert werden
* Versanddatum von Rechnung, Spendenbescheinigung und Lastschrift lässt sich nicht mehr editieren
