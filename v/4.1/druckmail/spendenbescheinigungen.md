# Spendenbescheinigungen

## Aktivierung

Zur Nutzung der Spendenbescheinigungen ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

Anschließend sollte JVerein neu gestartet werden, damit der Menüpunkt "Spendenbescheinigungen" zur Verfügung steht.

## Spendenbescheinigungen selektiv drucken

Im View Spendenbescheinigungen werden bereits erstellte Spendenbescheinigungen angezeigt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_SpendenbescheinigungenListeView.png" alt="" /></picture>

JVerein wird also eine gedruckte Unterschrift nur bei reinen Geldspenden generieren falls gedruckte Unterschrift aktiviert ist.

Möchte man also Spendenbescheinigungen per Mail verschicken geht das nur für echte Geldspenden. Dafür ist der Filter für Spendenart auf "Geldspende ohne Erstattungsverzicht" zu setzen. In diesem Fall erhält man alle echten Geldspenden für die auch eine Unterschrift generiert wurde.

Mit der Option "Sachspende oder Geldspende mit Erstattungsverzicht" erhält man alle Spendenbescheinigungen für die keine Unterschrift gedruckt wird. Diese müssen ausgedruckt und per Hand unterschrieben werden.

In der Liste können ein oder mehrere Einträge markiert werden. Über ein Kontextmenu (rechter Mausklick) stehen verschiedene Aktionen zur Verfügung.

## Spendenbescheinigung selektiv drucken oder per Mail versenden

Über den Menüpunkt "Druck und Mail" öffnet sich der Dialog Spendenbescheinigungen der Sie beim Versenden der Spendenbescheinigungen unterstützt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_SpendenbescheinigungenDruckMailView1.png" alt="" /></picture>

Im Info Feld erfolgt eine Information über die Anzahl der ausgewählten Spendenbescheinigungen ausgegeben.

Danach wird angezeigt für welche Mitglieder keine Mail Adresse konfiguriert ist und ihre Spendenbescheinigungen damit nicht verschickt werden.

Es wird ebenfalls angezeigt für welche Spendenbescheinigung kein Mitglied zugeordnet ist. In diesem Fall wird der Inhalt von Zeile 1..3 ausgegeben und keine Mail verschickt.

Im Parameter Feld gibt es folgende Optionen:
* Ausgabe: Es lässt sich wählen ob die Rechnungen als PDF (eine Datei oder einzelne Dateien) gedruckt oder per Mail verschickt werden sollen
* Adressblatt: Es lässt sich einstellen ob eine extra Seite mit einer Anschrift und oder Anschreiben ausgedruckt werden soll. Bei gedrucktem Anschreiben wird der Text aus dem Text Feld verwendet.
* Versanddatum setzen: Diese Option ist für die Ausgabe als PDF verfügbar. Ist sie gewählt, wird beim Druck das Versanddatum gesetzt. Damit kann man z.B. Probeausdrucke machen ohne das Versanddatum zu setzen. Bei Mailversand wird das Versanddatum immer gesetzt

Im Bereich Mail lässt sich der Betreff und der Mailtext eingeben.

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Spendenbescheinigungen generiert oder verschickt werden
* Starten: Startet die Ausgabe

Durch Klick auf den Starten Button werden die Spendenbescheinigungen an die Mitglieder versendet bzw. gedruckt.

## Spendenbescheinigung automatisch drucken oder per Mail versenden

Neben der individuellen Auswahl für Drucken und Versenden über das Kontextmenü im Spendenbescheinigungen Dialog lässt sich dies auch über den Eintrag im Navigations Menü erreichen.

Der Dialog enthält hier die Filter Optionen wie im Spendenbescheinigungen Dialog.

JVerein wird also eine gedruckte Unterschrift nur bei reinen Geldspenden generieren falls gedruckte Unterschrift aktiviert ist.

Möchte man also Spendenbescheinigungen per Mail verschicken geht das nur für echte Geldspenden. Dafür ist der Filter für Spendenart auf "Geldspende ohne Erstattungsverzicht" zu setzen. In diesem Fall erhält man alle echten Geldspenden für die auch eine Unterschrift generiert wurde.

Mit der Option "Sachspende oder Geldspende mit Erstattungsverzicht" erhält man alle Spendenbescheinigungen für die keine Unterschrift gedruckt wird. Diese müssen ausgedruckt und per Hand unterschrieben werden.

Mit der Option Adressblatt lässt sich auswählen, ob eine zusätzliche Seite an die Spendenbescheinigung angefügt werden soll. Auf diese lässt sich eine Briefanschrift und/oder ein Anschreiben ausgeben. Das Anschreiben wird im Feld Text eingegeben.

Es werden hier alle Spendenbescheinigungen gedruckt bzw. versendet die die Filterkriterien erfüllen. Eine individuelle Auswahl aus den gefilterten Einträgen ist hier nicht möglich.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_SpendenbescheinigungenDruckMailView2.png" alt="" /></picture>

Im Parameter Feld gibt es folgende Optionen:
* Ausgabe: Es lässt sich wählen ob die Rechnungen als PDF (eine Datei oder einzelne Dateien) gedruckt oder per Mail verschickt werden sollen
* Adressblatt: Es lässt sich einstellen ob eine extra Seite mit einer Anschrift und oder Anschreiben ausgedruckt werden soll. Bei gedrucktem Anschreiben wird der Text aus dem Text Feld verwendet.
* Versanddatum setzen: Diese Option ist für die Ausgabe als PDF verfügbar. Ist sie gewählt, wird beim Druck das Versanddatum gesetzt. Damit kann man z.B. Probeausdrucke machen ohne das Versanddatum zu setzen. Bei Mailversand wird das Versanddatum immer gesetzt

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Spendenbescheinigungen generiert oder verschickt werden
* Starten: Startet die Ausgabe
