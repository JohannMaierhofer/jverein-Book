# Auswertung Mitglieder

## Allgemein

Der Mitgliederbestand kann nach verschiedenen Kriterien ausgewertet und das Ergebnis zur direkten Nutzung oder zur Weiterverarbeitung exportiert werden. Hierzu gibt es folgende Möglichkeiten:

1. Filterung des Datenbestands
2. Sortierung der Ausgabe
3. Wahl des Ausgabeformats
4. Definition der Spalten bei CSV-Ausgabe

Die Ausgabe erfolgt entweder im PDF- oder im CSV-Format. Nach der Erzeugung der Datei wird ein entsprechendes Anzeigeprogramm aufgerufen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MitgliederView.png" alt="" /></picture>

## Sortierung

Die Sortierung erfolgt wahlweise nach

* Name, Vorname
* Eintrittsdatum
* Geburtsdatum
* Geburtsmonat und -jahr (Geburtstagliste).

Hinweis: Runde Geburtstage können in der [Jubiläumsliste](jubilaen.md) ausgegeben werden.

## Ausgabe im PDF-Format

### Mitgliederliste PDF

Die Mitgliederliste listet alle Mitglieder und enthält 5 Spalten:

* Name
* Anschrift / Kommunikation
* Geburtsdatum
* Eintritt / Austritt / Kündigung
* Beitragsgruppe / Eigenschaften / Mitgliedsnummer

### Adressliste PDF

Die Adressliste listet alle Mitglieder und enthält 5 Spalten:

* Name
* Adresse
* Telefon
* Email
* Geburtsdatum

## Ausgabe im CSV-Format

Eine [CSV-Datei](http://de.wikipedia.org/wiki/CSV_\(Dateiformat\)) ist eine Textdatei, bei der jeder Datensatz (jedes Mitglied) als einzelne Textzeile gespeichert ist. Die Textzeilen bestehen aus Feldern die mit Semikolon-Zeichen getrennt sind (im deutschen Sprachraum). Dieses einfache Dateiformat lässt sich sowohl mit einem Texteditor (bei Windows z.B. Notepad, bei Linux z.B. vim,Emacs,Nano) als auch mit einer Tabellenkalkulation wie Excel oder OpenOffice-Calc editieren.

Eine CSV-Datei kann in OpenOffice oder WinWord als Serienbriefdatenquelle zugewiesen werden.

Für die Ausgabe als CSV-Format gibt es 3 verschiedene Möglichkeiten:

* Mitgliederliste CSV
* Addressbuchexport CSV
* eigene Vorlagen für CSV (ab Version 2.5)

Bei der Mitgliederliste CSV werden sämtliche vorhandenen Mitglieder-Eigenschaften inklusive selbst definierte [Zusatzfelder](../administration/mitglieder/felddefinition.md) in die CSV-Datei exportiert.

DerAddressbuchexport CSV eignet sich u.a. für die Weiterverarbeitung in Mailprogrammen (z. B. Thunderbird, Outlook Express).

### Vorlagen für eigene CSV-Formate

Ab Version 2.5 kann man eigene Vorlagen für den CSV-Export erstellen.

Dazu ist zunächst unter [Einstellungen->Dateinamen](../administration/einstellungen/dateinamen.md) ein Verzeichnis zu wählen, in dem alle selbst erstellten Vorlagen gespeichert werden.

Jede der selbst erstellten Vorlagen ist ebenfalls eine CSV-Datei. Diese Dateien müssen mit einem externen Programm erstellt werden, also mit einem Texteditor oder mit einem Tabellenkalkulationsprogramm. Damit JVerein diese Vorlagendateien erkennt, müssen diese im gewählten Vorlagenverzeichnis gespeichert werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Ausgabe.png" alt="" /></picture>

Die Vorlagen kann man direkt in der Liste Ausgabe auswählen

Alle in diesem Verzeichnis vorhandenen CSV-Dateien werden im Dialog Auswertung Mitgliedsdaten im Auswahlfeld Ausgabe aufgelistet.

**Hinweis:** Wird das Vorlagen-Verzeichnis geändert oder neue Dateien in diesem Verzeichnis erstellt, so ist JVerein neu zu starten. Bei einer Änderung einer bestehenden Vorlage ist dies jedoch nicht notwendig.

**Wie ist nun eine solche Vorlagendatei aufgebaut?**

Jede CSV Vorlagendatei besteht aus 2 Zeilen:

1. Zeile: frei wählbare Spaltenüberschriften
2. Zeile: Zuordnung der JVerein-Felder zu den in Zeile 1 definierten Spalten

**Beispiel**

Datei Eintrittsdatum.csv, wird angezeigt unter Ausgabe als Vorlage CSV: Eintrittsdatum(ohne Endung .csv)

```
Name;Vorname;Eintrittsdatum
mitglied_name;mitglied_vorname;mitglied_eintritt
```

**Wie kann ich einfach Vorlagendateien erstellen?**

1.  Zunächst erzeugt man mittels der Auswahl

    Mitgliederliste CSV

    eine CSV-Datei die alle möglichen Datenfelder beinhaltet.
2. Dann öffnet man diese mit einem Tabellenkalkulationsprogramm, z.B. Excel oder OpenOffic-Calc. Hier sieht man nun die exportierten Datensätze, wobei die JVerein-Feldnamen in der ersten Zeile stehen.
3. Durch Löschen und Umsortieren von Spalten wird jetzt die gewünschte Spaltenreihenfolge definiert. Es sollten nur noch die Spalten übrig bleiben die man wirklich in der Ausgabe haben möchte.
4. Nun dupliziert man die erste Zeile und benennt in der ersten Zeile die Spalten so um wie man sie haben möchte
5. Zum Schluss löscht man noch alle Datensätze ab Zeile 3, da die Daten in der Vorlage ja nicht benötigt werden

Das war's. Die Vorlagen braucht man ja nur einmalig zu erstellen und kann Sie bei jedem Export nutzen.
