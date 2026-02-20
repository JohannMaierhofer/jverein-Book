# Mitgliederliste

### Allgemein

Das Fenster der Mitglieder-Suche besteht aus zwei Teilen: Filter (oben) und Mitgliedertabelle (unten). Die angezeigten Mitglieder können nach verschiedenen Kriterien gefiltert werden:

Im Allgemein Tab:

* Mitgliedschaft Status "Angemeldet", "Abgemeldet" und "Beide"
* Externe Mitgliedsnummer (optional)
* Name
* Beitragsgruppe
* Eigenschaften
* Zusatzfelder (optional)
* Geschlecht
* Mail
* Stichtag

Im Erweitert Tab Datum:

* Geburtsdatum von/bis
* Eintrittsdatum von/bis
* Austrittsdatum von/bis

Im Erweitert Tab Mitgliedskonto:

* Differenz
* Differenz Limit (Filter nach Fehlbetrag oder Überzahlung größer als das Limit)
* Datum von/bis (Datumsbereich für die Sollbuchungen die betrachtet werden)


Jeweils beim Verlassen eines Feldes mit pull down Menüs wird die Suche ausgelöst. Änderungen in Eingabefeldern für Text oder Datum lösen erst eine Suche aus wenn der Suchen Button gedrückt wird oder alternativ durch drücken des Enter auf der Tastatur.

Nach einem Doppelklick auf das Mitglied werden die kompletten Daten angezeigt. Mit einem Rechtsklick auf ein Mitglied öffnet sich ein Kontextmenü. Damit kann das Mitglied bearbeitet oder gelöscht werden. Außerdem ist die Ausstellung einer [Spendenbescheinigung](../spendenbescheinigung.md) möglich.

Die Filterkriterien können für eine spätere Verwendung in einem [Suchprofil](suchprofil.md) gespeichert werden.

Mit dem Reset Button können die Filter Felder auf Defaultwerte zurückgesetzt werden.

## Liste der Mitglieder

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MitgliedListeView.png" alt="" /></picture>

Erweiterte Filter:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MitgliedListeView2.png" alt="" /></picture>

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MitgliedListeView3.png" alt="" /></picture>

Mit dem Button "Neu" lässt sich ein neues Mitglied anlegen. Siehe [Stammdaten](grunddaten.md)

Mit dem Button "Import" lassen sich ein neue Mitglieder aus CSV Dateien importieren. Siehe [Mitglieder Import](../import.md)

Unter Administration->Einstellungen->Mitglieder Spalten lassen sich die die angezeigten Spalten konfigurieren.

In 3.1.0 wurde eine weitere Spalte "Status" eingeführt. Sie liefert das Ergebnis der Checks die auch beim Speichern eines Mitglieds ausgeführt werden. Es kann nützlich sein diese Spalte für einen Check zu aktivieren, weil z.B. weitere Checks implementiert wurden. Z.B. wurde in 3.0.0 ein genauerer Check der Kontodaten eingeführt. Wenn alles OK ist kann man sie wieder entfernen.

### Filterung nach Eigenschaften

Es können eine oder mehrere Eigenschaften ausgewählt werden.

Folgende Eigenschaften-Verknüpfungen sind möglich:

* "und": D.h. es werden nur die Mitglieder angezeigt, die alle ausgewählten Eigenschaften erfüllen.
* "oder": D.h. es werden die Mitglieder angezeigt, die mindestens eine der ausgewählten Eigenschaften erfüllen.

Auswahl einer Eigenschaft:

* "+": Hier ist die Eigenschaft ausgewählt.
* "-": Es ist die inverse Eigenschaft ausgewählt. Z.B. Gymnastik in Bild unten. Dies bedeutet diese Eigenschaft darf nicht enthalten sein.

Durch klicken auf die Eigenschaft kann zwischen den Werten umgeschaltet werden.

Bedeutung des Symbols bei der Eigenschaften Gruppe:

* "P": Bei der Eigenschaften Gruppe ist die Pflicht Checkbox ausgewählt.
* "I": Bei der Eigenschaften Gruppe ist die Maximal 1 Eigenschaft Checkbox ausgewählt.
* "PI": Bei der Eigenschaften Gruppe ist die Pflicht und die Maximal 1 Eigenschaft Checkbox ausgewählt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_EigenschaftenFilterDialog.png" alt="" /></picture>

### Filterung nach Zusatzfeldern

Soll nach Zusatzfelder gefiltert werden, kommt es auf den Datentyp des jeweiligen Zusatzfeldes an. Bei einem Ja/Nein Feld kann nur nach Ja-Einträgen gefiltert werden. Bei einem Textfeld gelten zur Filterung die SQL-Regeln für einen Textvergleich: Hier können die Wildcards % (0...n beliebige Zeichen) und \_ (genau 1 beliebiges Zeichen) eingesetzt werden. Durch die Verwendung der Kombination \_% kann man nach allen nicht leeren Textfeldern filtern.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_ZusatzfelderFilterDialog.png" alt="" /></picture>

## Kontextmenu

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_MitgliedMenu.png" alt="" /></picture>

### Bearbeiten

Mitglied bearbeiten. Identisch mit Doppelklick auf das Mitglied.

Siehe [Mitglied](grunddaten.md).

### Duplizieren

Es wird ein neuer Datensatz mit den Daten des Mitgliedes angelegt. Dieser kann dann vor der Speicherung verändert werden.

### In Zwischenablage kopieren

Es wird ein Datensatz mit den Daten des Mitgliedes in die Zwischenablage kopiert.

### Eigenschaften

Für alle markierten Mitglieder können die Eigenschaften gleichzeitig gesetzt oder gelöscht werden.

Die Icons haben fünf Zustände:

* Quadrat: Kein Mitglied hat die Eigenschaft gesetzt und sie wird bei niemanden geändert.
* Haken: Alle selektierten Mitglieder haben die Eigenschaft gesetzt und sie wird bei niemanden geändert.
* Gestrichelter Haken: Mindestens ein selektiertes Mitglieder hat die Eigenschaft gesetzt und sie wird bei niemanden geändert.
* Plus Zeichen: Die Eigenschaft wird nach OK bei allen selektierten Mitgliedern gesetzt.
* Minus Zeichen: Die Eigenschaft wird nach OK bei allen selektierten Mitgliedern gelöscht.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_EigenschaftenAuswahlDialog.png" alt="" /></picture>

### Arbeitseinsatz zuordnen

Für alle markierten Mitglieder werden Arbeitseinsätze erzeugt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_ArbeitseinsatzDialog.png" alt="" /></picture>

### Zusatzbetrag zuordnen

Für alle markierten Mitglieder werden Zusatzbeiträge erzeugt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_ZusatzbetragDialog.png" alt="" /></picture>

### Zu Nicht-Mitglied umwandeln

Ein Mitglied in ein Nicht-Mitglied umwandeln.

### Löschen

Löscht das Mitglied.

### Mail senden

Es wird eine Mail an das Mitglied versandt. Dabei wird eine Auswahl von Mailvorlagen zur Verfügung gestellt.

### vCard-Datei

Die Daten des Mitgliedes lassen sich als vCard exportieren.

### vCard-QR-Code

Zeigt eine QR-Code mit den Daten des Mitgliedes an.

### Kontoauszug

Für einen vorgegebenen Zeitraum werden alle Buchungen des Mitgliedskontos ausgegeben.

### Spendenbescheinigung

Automatische Erstellung von Spendenbescheinigungen, die direkt dem Mitglied zugeordnet sind. Werden mehrere Buchungen gefunden, wird eine Sammelbestätigung erzeugt. Bei Sachspenden wird für jede Buchung eine eigene Sachspendenbescheinigung erzeugt.

### Personalbogen

Ausgabe aller zu einem Mitglied gespeicherten Daten (Ausnahme: Ggfls. gespeicherte Dokumente)

### Manuelle Lastschrift

Generierung einer manuellen Lastschrift in Hibiscus.

## Freie Formulare

Wenn unter Administration->Mitglieder->Formulare mindestens ein Forular vom Typ "Freies Formular" angelegt wurde, so wir ein Untermenü mit allen Freien Formularen angezeigt. Beim Auswählen eine Eintrags kann dieses Formular an die Ausgwählten Mitglieder Verschickt/Gedruckt werden siehe [Freie Formulare](../../druckmail/freiesformular.md)
