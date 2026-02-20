# Buchungsimport

Buchungen können im CSV-Format importiert werden. Der Dateiname muss eine Endung haben. Z. B. .csv oder .txt. Es kann jede beliebige Endung verwendet werden. Die Datenfelder werden durch Semikolon getrennt. Das Encoding kann ausgewählt werden.

Als Spaltennamen stehen die [Variablen](../../../sonstiges/variable.md) aus dem Bereich "Buchungen" zur Verfügung.

```
buchung_betrag;buchung_buchungsart_nummer;buchung_datum;buchung_kontonummer;buchung_name;buchung_zweck1;buchung_iban
80;2004;08.04.2012;1;Shop;"Mitgliedsbeitrag
1. Halbjahr
Hansi Müller";DE02100100100006820101
35;2004;08.04.2012;1;Shop;zweck1;DE02100100100006820101
```

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_tabellen_ansicht.png" alt="" /></picture>

Die oberste Zeile dient der Zuordnung. Der Inhalt dieser Zeile muss exakt so geschrieben werden. Hinweis: Das Hinzufügen der Felder "buchung\_buchungsart\_nummer" oder "buchung\_buchungsklasse\_nummer" hat dazu geführt, dass der Import nicht klappt. In die Spalte "buchung\_kontonummer" kommt die (JVerein) Kontonummer zu der die Buchung zugeordnet werden soll. Bei einem Hibiskuskonto ist das die Bankkontonummer. Bei einem reinen JVereinkonto die entsprechende Nummer des Kontos. Man kann sie hier nachschauen bzw. vorab ein Konto anlegen. In diesem Beispiel hat das JVerein interne Konto die Bezeichnung "manuell" und die Nummer 2.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_konto_navi.png" alt="" /></picture>

In LibreOffice "Datei" -> "Speichern unter" wählen und als Dateityp "CSV" auswählen. Zusätzlich den Haken bei "Edit filter settings" setzen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_tabellen_save.png" alt="" /></picture>

Die Einstellungen für den Export sind wie folgt:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_export_text_file.png" alt="" /></picture>

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_buchungen_ansicht.png" alt="" /></picture>

Der Import Button ist in JVerein unter "Buchführung" -> "Buchungen" -> "Import"

Zumindest beim Mac muss man nach dem Import die Ansicht wechseln, erst dann erscheinen die importierten Buchungen in der Liste.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_import_ergebnis.png" alt="" /></picture>
