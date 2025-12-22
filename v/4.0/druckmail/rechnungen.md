# Rechnungen

## Aktivierung

Zur Nutzung der Rechnungen ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

Anschließend sollte JVerein neu gestartet werden, damit der Menüpunkt "Rechnungen" zur Verfügung steht.

## Allgemeines

Möchten Sie Rechnungen direkt aus JVerein druckfertig generieren, müssen zuvor Rechnungen erstellt werden, siehe [Rechnungen](../mitglieder/rechnung.md).

Die Rechnungen können für den Druck in ein PDF-Dokument ausgegeben werden oder per Mail an die Mitglieder versandt werden.

Beim versenden der Rechnung per Mail und wenn nur eine Rechnung als PDF erstellt wird, wird diese automatisch als E-Rechnung im ZUGFeRD Format erstellt.

## Rechnungen selektiv drucken oder mailen

Möchten Sie eine Rechnung selektiv ausgeben, so öffnen Sie den Dialog Rechnungen. Wählen Sie den Filter so, dass die gewünschten Daten angezeigt werden. Selektieren Sie einen oder mehrere Einträge und drücken die rechte Maustaste. Es öffnet sich ein Kontext-Menü. Wählen Sie hier den Menüpunkt "Druck und Mail". Es öffnet sich hier der Dialog Rechnung der Sie bei der Erstellung der Rechnung unterstützt.

Hier lässt sich bei der Ausgabe zwischen Drucken oder Versenden per Mail wählen.

Im Info Feld wird angezeigt wie viele Rechnungen selektiert wurden und ob zugehörige Mitglieder keine Mailadresse haben. Haben sie keine Mail Adresse werden sie beim Versand per Mail ignoriert.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_RechnungenDruckMailView1.png" alt="" /></picture>

Im Parameter Feld "Ausgabe" lässt sich wählen ob die Rechnungen als PDF gedruckt oder per Mail verschickt werden sollen.

Im Falle des Mail Versand sind die Felder Betreff und Text auszufüllen.

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Rechnungen generiert oder verschickt werden
* Starten: Startet die Ausgabe

Das drücken des Startknopf löst im Fall der Mail Ausgabe bei korrekt eingestellten Mail-Server-Daten den Versand der Mails aus. Es ist daher ratsam, diese Funktion im Vorfeld zu testen, ohne mit echten Mitgliederdaten/Mails zu hantieren.

## Rechnungen automatisch drucken oder mailen

Um automatisch Rechnungen zu erstellen wählen Sie im Navigations Baum dem Menü Eintrag "Rechnungen" aus. Es öffnet sich ebenfalls der Dialog Rechnungen.

Im Gegensatz zum selektiven Erstellen wird hier der gleiche Filter Bereich angezeigt wie im Rechnungen Dialog. Es werden dann Rechnungen die die Filter Kriterien erfüllen gedruckt bzw. per Mail versendet.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_RechnungenDruckMailView2.png" alt="" /></picture>

Der Filter Bereich bietet folgende Optionen:

* Name: Der Name eine Mitglieds.
* Differenz: Bei "Fehlbetrag" werden nur Kontoauszüge für Mitglieder erstellt wenn ein Fehlbetrag vorliegt und bei "Überzahlung" nur wenn überzahlt wurde. Bei "Egal" wird nicht auf den Betrag geprüft.
* Ohne Abbucher: Schließt Mitglieder die per Lastschrift bezahlen aus.
* Datum von/bis: Es werden nur Mitgliedskonten Einträge im gewählten Zeitraum berücksichtigt.
* Mail: Hier lässt sich auswählen ob nur Mitglieder mit Mailadresse, ohne Mailadresse oder unabhängig von einer Mailadresse ausgewählt werden.

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Rechnungen generiert oder verschickt werden
* Starten: Startet die Ausgabe

Tipp:

Falls Sie Rechnungen per Mail versenden wollen, wählen Sie erst bei Mail die Option "Nur mit Mailadresse" und als Ausgabe Mail. Damit versenden sie die Rechnung an alle Mitglieder die eine Mail Adresse haben.

Falls nicht alle Mitglieder eine Mail Adresse haben, wählen Sie anschließend bei Mail die Option "Nur ohne Mailadresse" und die Ausgabe Druck. Diese können Sie dann per Post verschicken.

## Rechnungen drucken

Es öffnet sich ein Dialog der den Speicherort und den Dateinamen der PDF Datei abfragt, in die alle Rechnungen erstellt werden. Mit Bestätigen dieser Eingaben werden die Rechnungen generiert und die fertige PDF geöffnet. Diese können Sie nun ausdrucken.

## Rechnungen per Mail versenden

Rechnungen können per Mail versandt werden. Dazu muss die Mailkonfiguration abgeschlossen sein. Bei der Ausgabe wird zu Kontrollzwecken eine ZIP-Datei mit allen erstellten und versandten Rechnungen erstellt.
