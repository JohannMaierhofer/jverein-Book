# Release Notes

## Allgemeines

Die Version 4.0 ist eine neuer Major Version. Nach einer Migration der Datenbank auf die 4.0 kann diese nicht mehr mit einer älteren Version bearbeitet werden.

## Achtung Migration !!!!
*  Für das Redesign des abweichenden Zahler existiert keine vollständige Migration. Betroffene Anwender müssen evtl. etwas nacharbeiten
*  Hierzu gibt es drei Anwendungsfälle

#### Bei einem Familienmitglied war als Zahlungsweg Vollzahler ausgewählt
* Falls in einem Familienverband bei einem Familienmitglied der Zahlungsweg "Vollzahler" war, wir dies automatisch migriert
* Der Vollzahler wird als abweichender Zahler gesetzt
* Der Zahlungsweg des Mitglied auf Überweisung geändert
* Es ist keine Nacharbeit nötig

#### Das Konto des Mitglieds ist ein Gemeinschaftskonto 
* Wegen der Bezeichnung für das Gemeinschaftskonto wurden die Felder für den alternativen Kontoinhaber ausgefüllt
* In 4.0 gibt es bei den Kontodaten das neue optionale Feld "Kontoinhaber"
* Falls der Kontoinhaber nicht genau dem Namen+Vornamen des Mitglieds entspricht kann hier die genaue Bezeichnung eingegeben werden
* Während der Migration werden hier Name und Vorname aus den alten nicht mehr vorhandenen Feldern des alternativen Kontoinhabers kopiert
* Der Anwender sollte also bei Mitgliedern mit Gemeinschaftskonto prüfen ob der eingetragene Kontoinhaber korrekt ist

#### Eine andere Person zahlt die Beiträge 
* Bereits konfigurierte alternative Kontoinhaber werden nicht automatisch in Nicht-Mitglieder umgewandelt. Es könnte ja sein, dass es nur ein Gemeinschaftskonto ist oder dass der Zahler bereits als Mitglied oder Nicht-Mitglied existiert
* Der Anwender muss also selbst bei bereits bestehenden alternativen Kontoinhabern falls nötig ein Nicht-Mitglied erzeugen
* Existiert das Mitglied oder Nicht-Mitglied bereits welches zahlen soll, dann kann dieses direkt als alternativer Zahler gesetzt werden. Da noch die fremden Kontodaten eingetragen sind, sollten sie gelöscht werden oder durch die Daten des Mitglieds ersetzt werden
* Falls noch kein Mitglied oder Nicht-Mitglied existiert, kann es über den Button "Abweichenden Zahler anlegen (Nicht-Mitglied)" angelegt werden
* Bei einem bestehenden Namen im alternativen Kontoinhaber (alte Felder) werden dessen Daten und die Kontodaten in das neue Nicht-Mitglied übernommen. Er wird dann als Zahler gesetzt und die Kontodaten automatisch gelöscht. Auch wird dann der alte Name im alternativen Kontoinhaber gelöscht


## The Big Ones

### Erweiterte Formularfelder

* Bisher waren die Formularfelder einzelne Variablen die an eine bestimmte Stelle im Formular platziert werden konnten
* Wollte man diese in Texte integrieren musste man in den Vorlagen entsprechend Platz lassen, das war aber schwierig, weil nicht im Voraus die Länge der Variable bekannt ist
* In der neuen Version werden die Formularfelder durch Textfelder ersetzt die an definierten Stellen in der Vorlage platziert werden können
* In das Textfeld kann jetzt Text mit Variablen gemischt werden. Damit entfällt das Problem der Platzierung der Variablen
* Die Migration der Datenbank für die Formularfelder ist ein Grund warum man nicht mehr auf die alte Version zurückgehen kann

### Konfigurierbare Titel und Subtitel bei Reports

* Ähnlich wie bereits für Dateinamen verfügbar lassen sich jetzt über die Vorlagen die Titel und Subtitel der Reports frei konfigurieren

### Hintergrund und Vordergrund bei Reports

* Über Administration->Einstellungen->Reports lassen sich jetzt ein Vordergrund und ein Hintergrund für PDF Reports konfigurieren
* Entsprechende Hintergründe und Vordergründe können als Formulare mit der neuen Art "Hintergrund/Vordergrund" erzeugt werden
* Diese Vorlagen erlauben keine zusätzlichen Formularfelder
* Ein Hintergrund liegt unterhalb aller Ausgaben des Reports, der Vordergrund liegt über allem
* Bei ausgegeben Tabellen hat man die Möglichkeit zu wählen ob die Zellen transparent sind oder nicht. Sind sie nicht transparent, dann haben sie entweder einen weißen oder farbigen Hintergrund. Sind sie transparent, dann ist der Hintergrund unter den Zellen sichtbar

### Redesign für den abweichenden Zahler

* Bisher gab es mehrere Möglichkeiten einen alternativen Zahler für Beiträge und Zusatzbeträge zu definieren
* War ein Mitglied ein Familienangehöriger in einem Familienverband, dann konnte über den Zahlungsweg "Vollzahler" definiert werden, dass das voll zahlende Mitglied bezahlt
* Ansonsten gab es nur die Möglichkeit einen alternativen Kontoinhaber zu definieren. Da dieser aber kein Mitglied bzw. Nicht-Mitglied war, konnte in der Sollbuchung nur das Mitglied selbst als Zahler eingetragen werden. Die führte wieder zu anderen Problemen

Die Konfiguration für den abweichenden Zahler wurde jetzt in der 4.0 neu implementiert.
* Der abweichende Zahler ist unabhängig von einem Familienverband konfigurierbar
* In den Zahlungsweg Feldern gibt es ein neues Feld zu konfigurieren den alternativen Zahler
* Falls das Mitglied Beiträge und Zusatzbeträge nicht selbst bezahlt wird hier der alternative Zahler gesetzt. Es kann ein Mitglied oder auch Nicht-Mitglied sein
* Falls noch kein Mitglied oder Nicht-Mitglied existiert kann es über den Button "Abweichenden Zahler anlegen (Nicht-Mitglied)" gemacht werden.  Das neue Nicht-Mitglieder wird dabei direkt im Feld für den alternativen Zahler gesetzt
*  Beim Abrechnungslauf wird ein vorhandener Zahler als Zahler in der Sollbuchung eingetragen. Bei Zahlungsweg Lastschrift, werden Lastschriften werden auf den Zahler ausgestellt. Ist keiner gesetzt wird das Mitglied als Zahler eingetragen und dieses für Lastschriften verwendet
*  Daneben können auch der Zahlungsweg und Kontodaten des Mitglieds eingegeben werden
*  Ist ein Mitglied als Zahler in einer Sollbuchung eingetragen, dann werden immer seine Kontodaten verwendet, egal ob ein alternativer Zahler konfiguriert ist. Dieses ermöglicht es, dass das Mitglied auch selbst Zahlungen machen kann
*  Bei den Kontodaten gibt es das optionale Feld "Kontoinhaber". Weicht der Kontoinhaber vom Namen und Vornamen des Mitglied ab kann hier die genaue Bezeichnung eingegeben werden z.B. bei einem Gemeinschaftskonto. In diesem Fall muss kein Nicht-Mitglied erzeugt werden. Es wird aber davon ausgegangen, dass das Mitglied Mit-/Inhaber ist, weil dann das Mitglied als Zahler in der Sollbuchung steht und z.B. Spendenbescheinigungen in diesem Fall auf das Mitglied ausgestellt werden
*  Standard mäßig werden auch Zusatzbeiträge wie Beiträge über den alternativen Zahler verbucht. Will man Zusatzbeiträge jedoch abweichend davon vom Mitglied zahlen lassen, kann dies durch die neue Checkbox "Mitglied zahlt selbst" im Zusatzbetrag ausgewählt werden. In diesem Fall müssen natürlich auch die benötigten Kontodaten beim Mitglied eingetragen sein, z.B. IBAN bei Lastschriften

### Erweiterungen bei Wirtschaftsplan

* Die Planung der Rücklagen kann über einen eigenen Baum durchgeführt werden
* Die Rücklagen Daten sind in den Exports aufgelistet
* Neben dem nach Einnahmen und Ausgaben sortierten PDF Report wird auch ein nach Buchungsklassen sortierter Report unterstützt
* Der CSV Export unterstützt jetzt auch mehrere Wirtschaftspläne

### Versanddatum

* Bei Rechnungen, Spendenbescheinigungen und Lastschriften (Pre-Notification) wird ein Versanddatum unterstützt
* Das Versanddatum kann im jeweiligen Liste und Detail View editiert werden
* Das Versanddatum wird automatisch bei einem Mailversand gesetzt
* In den Liste Views und Druck & Mail Views lässt sich nach versendeten oder noch nicht versendeten Einträgen filtern


## Kleinere Korrekturen und Erweiterungen

### Drag and Drop Support für Mitglieds- und Buchungsdokumente

* Mitglieds- und Buchungsdokumente können per "Drag and Drop" in die Dokumentliste eingefügt werden

### Einstellungsänderungen ohne Neustart

* In Administration->Einstellungen->Anzeige gibt es Schalter die bisher einen Neustart erforderten.
* Wird mindestens die Jameica Version 2.12.0 verwendet, dann ist jetzt kein Neustart mehr nötig

### Erweiterter Buchungsart Zuordnen Dialog

* Der erweiterte Buchungsart Zuordnen Dialog erlaubt es jetzt auch neben der Buchungsklasse auch gleichzeitig die Steuer zu setzen
* Der Dialog erlaubt es auch nur einzelne Attribute zu setzen und andere unmodifiziert zu lassen
* Der extra Dialog zu setzen der Steuer wurde entfernt

### VOP Close-Match Namen in Kontoinhaber übernehmen

* Bei Hibiscus gibt es bei VOP-close-match einen Dialog um den geänderten Namen im Auftrag und Adressbuch zu übernehmen. Mit diesem PR wird der Name auch bei JVerein als Kontoinhaber eingetragen, sofern die Adressbuch Checkbox ausgewählt ist

### UnreadCounter

* Bei Sollbuchungen, Rechnungen, Zusatzbeträgen und Wiedervorlagen wird im Navigationsbaum die Anzahl der fälligen Einträge angezeigt

### Buchungsklasse und Buchungsart als String

* Buchungsklasse und Buchungsart sind jetzt Strings, damit können führende Nullen eingegeben werden


## Sonstiges

* Die Spalte Mandat-Id wurde in die Mitglieder Liste aufgenommen
* Für Pre-Notification Dateinamen für Kursteilnehmer gibt es eine eigene Vorlage
* Tooltip bei Buchungsliste Betrag Input
* Bank Name Variable bei Rechnungen unterstützen
* Bei Sachspenden wurde das Feld für Bezeichnung auf 100 Zeichen erweitert
* Bei Auswertung Nicht-Mitglieder ist auch die Option "Alle" bei Mitgliedstyp unterstützt
* Mitglied zahlt selbst Attribut bei Zusatzbetrag Import unterstützt
* Option zum Druck einzelner Dateien bei Rechnung, Mahnung, Kontoauszug und Freie Formulare
*  Einstellungen Eintrag für "Zeige Kontonummer in Buchungsliste" von Buchführung nach Reports verschoben
*  Die zukünftige Beitragsgruppe lässt sich jetzt in den Einstellungen -> Anzeige freischalten und ausblenden
*  Spalte mandatid in Mitglieder Liste aufgenommen
*  Mitglied Id beim Speichern eines neuen Mitglieds anzeigen


