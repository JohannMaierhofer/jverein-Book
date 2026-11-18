# Belege

## Aktivierung

Zur Nutzung der Belege ist unter Administration->Einstellungen->Anzeige die Option Dokumentenspeicherung zu aktivieren.


## Einstellungen für lokale Dokumentenspeicherung

Unter Administration->Einstellungen->Belege können die Wurzelverzeichnisse für die Dokumentspeicherung gesetzt werden. Diese können geändert werden wenn die Dokumente verschoben werden bzw. auf einen anderen Benutzer übertragen werden. Die Verzeichnisse stehen nicht in der Datenbank sondern sind lokal gespeichert.

Unter Administration->Einstellungen->Vorlagen lassen sich die relativen Pfade für die Belege mit Variablen definieren. Ein Beleg wird unter dem  Wurzelverzeichnis und dem relativen Pfad zusammengesetzt.

## Allgemeines

Belege können über Jameica Messaging oder lokal gespeichert werden. es gibt mehrere Arten von Belegen:
* Allgemeine Belege
* Buchung Belege
* Mitglied Belege
* Konto Belege

Je nach Typ eine Belegs wird dieser bei lokaler Dokumentspeicherung unter einem anderen Verzeichnis gespeichert. 

Unabhängig vom Typ des Belegs kann er trotzdem jeder Buchung, jedem Mitglied oder Konto zugeordnet werden. Ein Beleg kann auch mehreren Objekten gleichzeitig zugeordnet werden.

## Liste der Belege

In der Liste werden alle Belege aufgelistet und können nach verschiedenen Kriterien gefiltert werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegeListeView.png" alt="" /></picture>

Folgende Buttons sind vorhanden:
* Hilfe: Zeigt diese Hilfe an
* Export: Die Belege lassen sich ein ein externes Verzeichnis exportieren. Dateien lassen sich beim Export nach einem vorgegebenen Muster umbenennen.  Der "Beleg Export Dateiname" lässt sich unter Administration->Einstellungen->Vorlagen unter dem Filter Pfad einstellen
* Neu: Neuen Beleg erzeugen

Folgende Menü Einträge sind vorhanden:
* Bearbeiten: Öffnet den Beleg zum Bearbeiten
* Anzeigen: Öffnet das Dokument in einer externen Applikation und zeigt es an
* Löschen: Löscht den Beleg

## Neuer Beleg

Mit dem Neu Button wird ein neuer Beleg angelegt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegNeuView.png" alt="" /></picture>

Folgende Eingabefelder sind vorhanden:
* Belegart: Sie bestimmt welcher Pfad zum Speichern verwendet wird und wie die Belegnummer generiert wird
* Beleggruppe: Sie ist optional. Auch sind erst entsprechende Beleggruppen in den Einstellungen zu erstellen. Siehe [Beleggruppen](../administration/admbuchf/beleggruppe.md).
* Datum: Hinterlegtes Datum
* Bemerkung: Text zum Beleg
* Datei: Hier wird die Datei ausgewählt, die als Beleg gespeichert wird

Belege die hier erzeugt werden sind keiner Buchung oder keinem Mitglied zugeordnet. Das kann später in der Ansicht der Buchung oder des Mitglieds erfolgen.

## Neuer Beleg über Konto, Buchung und Mitglied erzeugen

Im Dialog eines Kontos, einer Buchung oder eines Mitglied werden bei aktivierter Dokumentspeicherung die zugeordneten Belege in einer Tabelle angezeigt. Dort lassen sich Belege neu erstellen bzw. bestehende Belege zuordnen.

Siehe hierzu [Dokumente](../../../sonstiges/dokumente.md)

Bei zugeordneten Belegen werden die Belegnummern in der Liste der Buchungen bzw. der Mitglieder in einer Spalte angezeigt.

## Beleg

Über den Bearbeiten Button kann die Beleginformation angezeigt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegView.png" alt="" /></picture>

Folgende Felder sind vorhanden:
* Belegnummer: Nummer des Belegs
* Belegart: Sie bestimmt welcher Pfad zum Speichern verwendet wird und wie die Belegnummer generiert wird
* Datum: Hinterlegtes Datum
* Bemerkung: Text zum Beleg
* Pfad: Pfad unter dem der Beleg gespeichert ist. Diese Information ist nur bei lokaler Speicherung verfügbar

In den Laschen:
* Buchungen werden diejenigen Buchungen aufgelistet, denen der Beleg zugeordnet ist
* Mitglieder werden diejenigen Mitglieder aufgelistet, denen der Beleg zugeordnet ist
* Konten werden diejenigen Konten aufgelistet, denen der Beleg zugeordnet ist