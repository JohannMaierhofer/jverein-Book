# Pre-Notification

## Allgemeines

Mit der Pre-Notification Funktion ist es einfach möglich, den Ansprüchen der SEPA Regelung bzgl. der Ankündigung einer SEPA-Lastschrift gerecht zu werden. Die Pre-Notification Benachrichtigung kann erst erstellt werden, wenn der Buchungsvorgang abgeschlossen ist. Die Buchungen (d.h. die Abrechnung) müssen dafür nur erstellt sein. Eine Onlinebuchung/ -übertragung zur Bank ist für diese Funktion nicht erforderlich.

In JVerein stehen folgende Alternativen für die Pre-Notifications zur Verfügung:

* Schriftlich an alle Mitglieder
* Per E-Mail an alle Mitglieder mit E-Mail-Adresse und schriftlich an die Übrigen
* Als 1ct-Überweisung an alle Mitglieder

## Aufruf der Pre-Notification Funktion über Abrechnungsläufe

Die Pre-Notification Funktion ist etwas versteckt und kann über die Liste der Abrechnungsläufe erreicht werden.

Mit einem Rechtsklick auf den entsprechenden Abrechnungsverlauf öffnet sich ein Kontextmenü, mit dem man die Pre-Notifications erstellen kann.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_AbrechnungslaufListeView.png" alt="" /></picture>

## Dialog bei Aufruf über Abrechnungsläufe

In diesem Fenster kann die Pre-Notification erstellt werden, und zwar auf der Karte Mail + PDF .

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_PrenotificationDruckMailView3.png" alt="" /></picture>

Im Parameter Feld gibt es folgende Optionen:
* Formular: Bei der Option PDF ist ein Formular auszuwählen. Dieses muss gegebenenfalls erstellt werden. Siehe [Formulare](../administration/mitglieder/formulare.md).
* Ausgabe: Es lässt sich wählen ob die Rechnungen als PDF (eine Datei oder einzelne Dateien) gedruckt oder per Mail verschickt werden sollen
* Versanddatum setzen: Diese Option ist für die Ausgabe als PDF verfügbar. Ist sie gewählt, wird beim Druck das Versanddatum gesetzt. Damit kann man z.B. Probeausdrucke machen ohne das Versanddatum zu setzen. Bei Mailversand wird das Versanddatum immer gesetzt

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Pre-Notifikationen generiert oder verschickt werden
* Starten: Startet die Ausgabe


## Aufruf der Pre-Notification Funktion über Lastschriften

Die Pre-Notification Funktion kann auch über die Liste der Lastschriften erreicht werden.

Mit einem Rechtsklick auf eine oder mehrere Lastschriften öffnet sich ein Kontextmenü, mit dem man die Pre-Notifications erstellen kann.

Diese Option hat den Vorteil, dass man einzelne Lastschriften auswählen kann. Da bei wiederkehrenden Lastschriften eine Pre-Notification nur beim ersten Mal notwendig ist, kann man hier nur die Mitglieder auswählen die neu hinzugekommen sind oder bei denen sich etwas geändert hat.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_LastschriftenListeView.png" alt="" /></picture>


## Dialog bei Aufruf über Lastschriften

In diesem Fenster kann die Pre-Notification erstellt werden, und zwar auf der Karte Mail + PDF .

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_PrenotificationDruckMailView1.png" alt="" /></picture>

Im Parameter Feld gibt es folgende Optionen:
* Formular: Bei der Option PDF Ausgabe ist ein Formular auszuwählen. Dieses muss gegebenenfalls erstellt werden. Siehe [Formulare](../administration/mitglieder/formulare.md).
* Ausgabe: Es lässt sich wählen ob die Rechnungen als PDF (eine Datei oder einzelne Dateien) gedruckt oder per Mail verschickt werden sollen
* Versanddatum setzen: Diese Option ist für die Ausgabe als PDF verfügbar. Ist sie gewählt, wird beim Druck das Versanddatum gesetzt. Damit kann man z.B. Probeausdrucke machen ohne das Versanddatum zu setzen. Bei Mailversand wird das Versanddatum immer gesetzt

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Pre-Notifikationen generiert oder verschickt werden
* Starten: Startet die Ausgabe

## Aufruf der Pre-Notification Funktion über Druck & Mail

Die Pre-Notification Funktion kann auch über den Navigationsbaum erreicht werden.

Mit einem Rechtsklick auf den entsprechenden Eintrag öffnet sich der Dialog, mit dem man die Pre-Notifications erstellen kann.

In diesem Fall wählt man den Abrechnungslauf für den die Pre-Notifications erzeugt werden sollen im Dialog aus.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_PrenotificationDruckMailView2.png" alt="" /></picture>

Im Parameter Feld gibt es folgende Optionen:
* Formular: Bei der Option PDF Ausgabe ist ein Formular auszuwählen. Dieses muss gegebenenfalls erstellt werden. Siehe [Formulare](../administration/mitglieder/formulare.md).
* Ausgabe: Es lässt sich wählen ob die Rechnungen als PDF (eine Datei oder einzelne Dateien) gedruckt oder per Mail verschickt werden sollen
* Versanddatum setzen: Diese Option ist für die Ausgabe als PDF verfügbar. Ist sie gewählt, wird beim Druck das Versanddatum gesetzt. Damit kann man z.B. Probeausdrucke machen ohne das Versanddatum zu setzen. Bei Mailversand wird das Versanddatum immer gesetzt

Der View besitzt folgende Buttons:

* Mail Vorlage: Öffnet den Auswahldialog zur Übernahme von Vorlagen
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt, die für den aktuellen Report geeignet sind. Diese lassen sich zum Kopieren in die Zwischenablage auswählen, um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben z.B. wenn sie geändert wurde
* Empfänger Liste: Zeigt einen Dialog mit der Liste aller Empfänger für die Pre-Notifikationen generiert oder verschickt werden
* Starten: Startet die Ausgabe


### Schriftliche Pre-Notification an alle Mitglieder

Bevor Pre-Notifications gedruckt werden können muss zunächst ein [Formular](../administration/mitglieder/formulare.md) dafür angelegt werden.


### Mail-Pre-Notification an Mitglieder mit Mail-Adresse

Im Block Parameter bei Ausgabe muss Mail eingestellt werden.

Im Block Mail wird der Mail-Text eingegeben und schließlich der Startknopf gedrückt.

Über die Buttons lässt sich eine gespeicherte Mailvorlage auswählen.

Das drücken des Startknopf löst bei korrekt eingestellten Mail-Server-Daten den Versand der Mails aus. Es ist daher ratsam, diese Funktion im Vorfeld zu testen, ohne mit echten Mitgliederdaten/Mails zu hantieren.

Die versendeten Pre-Notification Mails werden nach dem Versand beim jeweiligen Mitglied in der Mail-Historie gespeichert.

#### Beispiel für eine Pre-Notification Mail

```
NAME_DES_VEREINS___  - SEPA  Ankündigung

$lastschrift_empfaenger

ORT____, den  $lastschrift_abrechnungslauf_datum

aufgrund des von Dir erteilten Mandats zieht DER_VEREIN___ mittels SEPA-Lastschrift
von Deinem unten angegebenen Konto folgende Forderung am $lastschrift_abrechnungslauf_faelligkeit ein.

unsere Gläubiger-ID: DE___
Deine Mandats-ID: $lastschrift_mandatid
Das Mandats-Datum: $lastschrift_mandatdatum
Deine BIC: $lastschrift_bic
Deine IBAN: $lastschrift_iban
Das Fälligkeitsdatum: $lastschrift_abrechnungslauf_faelligkeit
Der Verwendungszweck: $lastschrift_verwendungszweck
Der Betrag: $lastschrift_betrag Euro

Fragen und Korrekturen bitte an: EMAILADRESSE___

Mit freundlichen Grüßen
die Verwaltung
```

### Schriftliche Pre-Notification an Mitglieder ohne E-Mail-Adresse

Nachdem die Pre-Notifications per E-Mail versendet wurden müssen die übrigen Mitglieder diese Nachricht noch schriftlich erhalten.

Im Block Parameter bei Ausgabe muss nun PDF (Lastschriften ohne Mailadresse) eingestellt werden und das Formular passend ausgewählt werden, dann den Startknopf drücken.

Die weitere Bedienung entspricht dem Vorgehen beim Senden der schriftlichen Pre-Notification an alle Mitglieder.

## 1ct-Überweisung Pre-Notification

Durch eine Überweisung von einem Cent kann über den Verwendungszweck die Pre-Notification durchgeführt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_Prenotification1ctErstellung.png" alt="" /></picture>

Auf der Karte 1ct-Überweisung müssen die Ausgabeart (Datei oder Hibiscus) und das Ausführungsdatum eingestellt werden.

Für den Verwendungszweck stehen alle unten aufgeführten $lastschrift\_\*-Variablen zur Verfügung.

### Beispiel für einen Verwendungszweck

```
Lastschriftankündigung/Betrag:$lastschrift_betrag/Datum:$lastschrift_abrechnungslauf_faelligkeit/Mandat-ID:$lastschrift_mandatid/Gläubiger-ID:DE....
```

In der Mail können im Betreff und im Text, bei der 1ct-Überweisung im Verwendungszweck die Lastschriftvariable verwendet werden. Diese Daten werden aus dem Abrechnungslauf genommen. Änderungen in den Mitgliederdaten nach dem Abrechnungslauf werden NICHT berücksichtigt.

## Besonderheiten - zusammengefasst

new Buchungsuebernahme();

* Änderungen der Mitgliederdaten nach einem Buchungslauf werden für diesen Buchungslauf NICHT mehr berücksichtigt. Der Buchungslauf stellt eine eigenen Datensatz dar.
  * So werden z.B. E-Mailadresseänderungen für die Pre-Notification außer acht gelassen.
  * Teilt ein Mitglied z.B. aufgrund der Pre-Notification eine neue Bankverbindung mit, so ändert man sie in den Mitgliederdaten nur für künftige Abrechnungen.
    * Wurde die entsprechende Lastschrift der aktuellen Abrechnung jedoch noch nicht zur Bank übertragen, so kann man zusätzlich in Hibiscus (oder in der XML-Datei) für diese Abrechnung noch die Bankverbindung ändern (Achtung: evtl. neue Mandatsreferenz und geänderte Erst-/Folgelastschrift beachten).
    * Wurde die Lastschrift aber bereits zur Bank übertragen, dann sind für diese Abrechnung keine Änderungen mehr möglich. Die Lastschrift wird wahrscheinlich zurückkommen, zum Handling siehe Rücklastschrift.
* Das Mailformular wird mit ausgeführtem Mailversand gespeichert.
* Die Variablen in der Pre-Notification Mail sind NICHT identisch mit den Variablen eines "normalen" E-Mailversandes.
