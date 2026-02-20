# Release Notes

## Allgemeines

Die Version 4.1 ist eine Minor Version und rückwärts kompatibel mit eine 4.0.


## The Big Ones

### Druck & Mail Vereinheitlichung

* Die Views für Druck & Mail wurden vereinheitlicht
* Die Parameter "Ausgabe" und "PDF als" wurden zusammen gelegt unter Ausgabe. Hier kann zwischen den drei Optionen "Mail", "Eine PDF Datei" und "Einzelne PDF Dateien" gewählt werden"
* Bei PDF Druck lässt sich auswählen ob das Versanddatum beim Druck gesetzt werden soll z.B. nicht bei Probeausdrucken
* Bei Spendenbescheinigungen wird bei Mailversand auch eine Zip Datei erzeugt wie bei den anderen Einträgen. Der Dateipfad für die Ausgabe wird nicht mehr in den Einstellungen konfiguriert sondern es wird sich der letzte benutze Pfad gemerkt und jeweils abgefragt

### Empfänger Liste Update in Druck & Mail

* In der Empfängerliste konnte man bisher in der Mitgliederliste alle Mitglieder auswählen. Es wurden in der Vorschau nur allgemeine und Mitglied Variablen ersetzt. Variablen aus den Anhängen wie z.B. Rechnungen wurden nicht ersetzt und mit dummy Daten angezeigt
* In der neuen Version wird für jede zu versendende Mail ein Eintrag in der Mitgliederliste erzeugt. Die Variablen Ersetzung basiert dann auf dem Mail Empfänger und dem jeweiligen Anhang. Es sind damit auch nur so viele Einträge in der Mitgliederliste wie auch Mails versendet werden. PS: wenn mehrere Mails an das gleiche Mitglied gesendet werden, ist das Mitglied mehrmals zur Auswahl, jeweils für eine spezifische Mail

### Forderungen

* Mit diesem Feature lassen sich einmalige Forderungen wie z.B. Kursgebühren direkt abrechnen. Es ist damit nicht mehr nötig einen Zusatzbetrag mit einmaliger Ausführung zu erzeugen und dann eine Abrechnungslauf durchzuführen
* Bei der Erstellung werden auch keine Zusatzbeträge generiert, lediglich Sollbuchungen und gegebenenfalls Lastschriften und Buchungen
* Es wird aber ein Eintrag in der Liste der Abrechnungsläufe erzeugt. Bei Fehlern kann dieser gelöscht werden, was dann wie bei regulären Abrechnungsläufen alle generierten Daten löscht
* Siehe [Forderung](mitglieder/forderung.md)

### Gutschriften

* Mit diesem Feature lassen sich bestehende Rechnungen, Sollbuchungen oder Lastschriften zurückerstatten z.B. wenn ein Kurs gestrichen wurde
* Es wird bei Rechnungen und Sollbuchungen eine Storno Rechnung/Sollbuchung mit dem negativen Betrag der ursprünglichen Forderung erzeugt. Ein bereits gezahlter Betrag wird zurück überwiesen, bei teilweiser Bezahlung eben auch nur der bereits bezahlte Teilbetrag
* Alternativ kann auch ein fester Betrag erstattet werden
* Ein fester Betrag kann auch bei der Auswahl von Mitgliedern an diese überwiesen werden
* Siehe [Gutschrift](mitglieder/gutschrift.md)


## Kleinere Korrekturen und Erweiterungen

### Variable Auswahl Dialog 

* Falls in einem Dialog oder View bei Eingabefeldern wie z.B. Verwendungszweck, Variablen verwendet werden können, dann existiert jeweils ein Button der eine Vorschau der unterstützten Variablen anzeigt

### Import von Vollzahler und Zahler

* Beim Mitglieder Import gibt es die Option auch Vollzahler und Zahler zu importieren
* Die betroffenen Mitglieder müssen schon in JVerein existieren evtl. müssen diese erst separat importiert werden

### Bezeichnung bei Lehrgängen

* Bei den Lehrgängen konnte man bisher nur eine Lehrgangsart eingeben
* Mit einem neuen Feld lässt sich auch eine Bezeichnung für den Lehrgang eingeben und danach filtern


## Sonstiges

* Buchungskorrektur wurde aus dem Navigationsbau entfernt und als Button in die Buchungsliste aufgenommen
* Beim Abrechnungslauf gibt es die neue Option die Rechnung als Buchungsdokument in der erzeugten Buchung zu speichern
* Das Kontoinhaber Attribut wurde zu Kursteilnehmer hinzugefügt
* In allen Liste Views mit Beträgen wird bei der Selektion mehrerer Einträge die in der Zeile unterhalb der Tabelle die Summen angezeigt
* Im Mail View wurden einige Buttons verschoben
* Bei Sollbuchungen mit negativem Betrag (Erstattung) lässt sich beim manuellen Erstellen einer Rechnung ein Erstattungsformular auswählen
* Das Mitglied wird in der Lastschrift angezeigt


