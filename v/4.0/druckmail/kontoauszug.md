# Kontoauszüge

## Allgemeines

Der Kontoauszug ist eine Liste (PDF-Ausgabe) sämtlicher Buchungen auf einem Mitgliedskonto.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Kontoauszug.jpg" alt="" /></picture>

Einen Kontoauszug kann in der Anzeige des Mitglieds (bzw. Nicht-Mitglied) abgerufen werden und auf einen Zeitraum eingegrenzt werden.

Die jüngsten Positionen des Kontoauszugs werden auch auf dem Personalbogen ausgegeben.

Die Kontoauszüge können für den Druck in ein PDF-Dokument ausgegeben werden oder per Mail an die Mitglieder versandt werden.

## Kontoauszüge selektiv erstellen

Möchten Sie einen Kontoauszug selektiv erstellen, so öffnen Sie den Dialog Mitglieder bzw. Nicht-Mitglieder. Wählen Sie den Filter so, dass die gewünschten Mitglieder angezeigt werden. Selektieren Sie einen oder mehrere Einträge und drücken die rechte Maustaste. Es öffnet sich ein Kontext-Menü. Wählen Sie hier den Menüpunkt "Kontoauszug". Es öffnet sich hier der Dialog Kontoauszug der Sie bei der Erstellung des Kontoauszug unterstützt.

Hier lässt sich bei der Ausgabe zwischen Drucken oder Versenden per Mail wählen.

Alternativ kann in der Detailansicht eines Mitglieds über den Button "Kontoauszug" der Dialog für dieses Mitglied geöffnet werden.

Im Info Feld wird angezeigt wieviele Mitglieder selektiert wurden und welche keine Mailadresse haben. Haben sie keine Mail Adresse werden sie beim Versand per Mail ignoriert.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_KontoauszuegeDruckMailView1.png" alt="" /></picture>

Der Filter Bereich bietet folgende Optionen:

* Differenz: Bei "Fehlbetrag" werden nur Kontoauszüge für Mitglieder erstellt wenn ein Fehlbetrag vorliegt und bei "Überzahlung" nur wenn überzahlt wurde. Bei "Egal" wird nicht auf den Betrag geprüft.
* "Differenz Limit": Zusätzlich kann angegeben werden, ob nur Sollbuchungen mit Differenzen zwischen Soll und Ist (Offene Posten oder Überzahlungen) über dem konfigurierten Limit gefiltert werden.
* Datum von/bis: Es werden nur Mitgliedskonten Einträge im gewählten Zeitraum berücksichtigt.

Im Parameter Feld "Ausgabe" lässt sich wählen ob die Kontoauszüge als PDF gedruckt oder per Mail verschickt werden sollen.

Im Falle des Mail Versand sind die Felder Betreff und Text auszufüllen.

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Kontoauszüge generiert oder verschickt werden
* Starten: Startet die Ausgabe

Das drücken des Startknopf löst im Fall der Mail Ausgabe bei korrekt eingestellten Mail-Server-Daten den Versand der Mails aus. Es ist daher ratsam, diese Funktion im Vorfeld zu testen, ohne mit echten Mitgliederdaten/Mails zu hantieren.

## Kontoauszüge automatisch erstellen

Um automatisch Kontoauszüge zu erstellen wählen Sie im Navigations Baum dem Menü Eintrag "Kontoauszüge" aus. Es öffnet sich ebenfalls der Dialog Kontoauszug.

Im Gegensatz zum selektiven Erstellen wird hier der ein Filter Bereich angezeigt. Es werden dann Kontoauszüge für alle Mitglieder/Nicht-Mitglieder die die Filter Kriterien erfüllen gedruckt bzw. per Mail versendet.

Ist kein Mitgliedstyp ausgewählt werden die Kontoauszüge sowohl für alle Mitglieder als alle Nicht-Mitglieder erzeugt.

Da der Filter hier eine Untermenge des Filters im Mitglied bzw. Nicht-Mitglied Dialog ist, hat man hier weniger Filter Möglichkeiten. Werden weitere Filter Optionen gebraucht muss über den selektiven Weg gegangen werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_KontoauszuegeDruckMailView2.png" alt="" /></picture>

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Kontoauszüge generiert oder verschickt werden
* Starten: Startet die Ausgabe

Tipp:

Falls Sie Kontoauszüge per Mail versenden wollen, wählen Sie erst bei Mail die Option "Nur mit Mailadresse" und als Ausgabe Mail. Damit versenden sie die Kontoauszüge an alle Mitglieder die eine Mail Adresse haben.

Falls nicht alle Mitglieder eine Mail Adresse haben, wählen Sie anschließend bei Mail die Option "Nur ohne Mailadresse" und die Ausgabe Druck. Diese können Sie dann per Post verschicken.
