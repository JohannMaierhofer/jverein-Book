# Zusatzfelder

### Aktivierung

Zur Nutzung der Zusatzfelder ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

### Allgemeines

Zusatzfelder sind Attribute für Mitglieder die zusätzlich zu den in JVerein vordefinierten Attributen vom Anwender frei definiert werden können. Eingerichtet werden solche Zusatzfelder unter Administration->Mitglieder->Zusatzfelder.

Damit lassen sich individuelle Daten zu einem Mitglied speichern. Eingerichtete Zusatzfelder erscheinen beim Mitglied unter dem Reiter "Zusatzfelder" und können dort individuell gesetzt werden.

Im Gegensatz zu Eigenschaften (siehe [Eigenschaften ](eigenschaften.md))  können je nach Datentyp individuelle Daten beim Mitglied eingegeben werden.

Im Filterbereich der Mitglieder kann auch nach Werten in Zusatzfeldern gefiltert werden.

Zusätzlich lassen sie sich in der Tabelle der Mitgliederliste als eigene Spalte anzeigen. Über die Spaltenauswahl des Panel Buttons kann die Anzeige ausgewählt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_MitgliederListeZusatzfeldView.png" alt="" /></picture>

In dem Bild wurde das Zusatzfeld "Übungsleiter" in der Tabelle eingeblendet.

Zusatzfelder lassen sich auch als Variablen in Mails und Reports einfügen. Es wird dabei über den Namen adressiert. Intern wird `mitglied_zusatzfeld_` vorne angefügt. Um z.B. beim Schreiben einer Mail auf das Zusatzfeld Übungsleiter zuzugreifen, muss `$mitglied_zusatzfeld_uebungsleiter` eingegeben werden.

### Liste der Zusatzfelder

Eine Liste der Zusatzfelder kann über den Eintrag Administration->Mitglieder->Zusatzfelder im Navigationsbaum angezeigt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_ZusatzfelderListeView.png" alt="" /></picture>

Mit Neu kann ein neues Zusatzfeld eingerichtet werden.

Durch einen Doppelklick wird die Bearbeitung eines Zusatzfeldes eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Löschen: Damit kann ein Zusatzfeld, die keinem Mitglied zugeordnet ist, gelöscht werden. Bei zugeordneten Zusatzfeldern erscheint eine Fehlermeldung

### Zusatzfeld

Durch einen Klick auf neu öffnet sich folgendes Fenster:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_ZusatzfeldView.png" alt="" /></picture>

Der Name des Feldes kann aus den Zeichen a-z und 0-9 und \_ (Unterstrich) bestehen. Er darf keine Leerzeichen enthalten und sich nicht mit existierenden Feldnamen überschneiden. Er wird bei der Bildung des Variablennamen verwendet.

Als Label kann ein beliebiger Begriff verwendet werden. Es wird am GUI verwendet, z.B. als Name der Spalte in der Mitglieder Tabelle.

Folgende Datentypen stehen zur Verfügung:

* Zeichenkette (bis zu 1.000 Zeichen lang)
* Datum (Format TT.MM.JJJJ)
* Ganzzahl
* Ja/Nein-Wert
* Währung

Feldnamen und Label können jederzeit geändert werden. Daten gehen hierdurch nicht verloren. Bis zur Version 1.2 (einschl.) kann ein Feld nur gelöscht werden, wenn bei keinem Mitglied Daten in diesem Feld gespeichert sind. Ab Version 1.3 werden die Daten nach Rückfrage gelöscht.

Bei der Änderung des Datentypen ist zu beachten, dass eine Konvertierung möglich sein muss. Beispielsweise kann ein Zusatzfeld vom Typ Zeichenfolge nur dann in den Typ Datum umgewandelt werden, wenn ausschließlich Daten in der Form TT.MM.JJJJ gespeichert sind. Alle Datentypen können in Zeichenfolge umgewandelt werden.
