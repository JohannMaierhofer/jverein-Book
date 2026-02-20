# Sollbuchungen

### Aktivierung

Zur Nutzung der Sollbuchungen ist keine extra Aktivierung notwendig.

### Allgemeines

Die [Abrechnung](../abrech/abrechnung.md) schreibt Sollbuchungen zu Mitgliedsbeiträgen und Zusatzbeträgen in die Tabelle [Mitgliedskonto](content/mitgliedskonto.md) des Mitglieds. Durch die Zuweisung von Istbuchungen kann der Kontostand ausgeglichen werden.

### Erstellung

Die Sollbuchungen können erstellt werden

* über einen Abrechnungslauf (siehe [Abrechnung](../abrech/abrechnung.md) )
* in den Mitglied Details (siehe [Mitgliedskonto](content/mitgliedskonto.md))
* implizit über die Zuordnung einer Sollbuchung zu eine Buchung (siehe [Buchungen](../buchf/buchungen.md))
* aber auch in der Liste der Sollbuchungen

Im Normalfall sollte die Erstellung der Sollbuchungen nur über die Abrechnung erfolgen. Nur in Ausnahmesituationen ist ein manuelles erstellen sinnvoll.

## Liste der Sollbuchungen <a href="#mitgliedskontouebersicht" id="mitgliedskontouebersicht"></a>

Es gibt eine zentrale Übersicht über alle Sollbuchungen. Die Sollbuchungen können über einen Zeitraum oder über einen Namen der Mitglieds oder des Zahlers, bzw. Namensfragment gefiltert werden.

Zusätzlich kann angegeben werden, ob nur Sollbuchungen mit Differenzen zwischen Soll und Ist (Offene Posten oder Überzahlungen) über dem konfigurierten Limit angezeigt werden.

Zudem lässt sich filtern ob das Mitglied per Lastschrift zahlt oder eine Mail Adresse hat.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_SollbuchungenListeView.png" alt="" /></picture>

Durch einen Doppelklick auf die Sollbuchung wird die Sollbuchung angezeigt.

Folgende Buttons stehen zu Verfügung:

* Exportieren: Damit können die Sollbuchungen als CSV Datei exportiert werden
* Neu: Damit kann eine neue Sollbuchung erzeugt werden

Durch einen Rechtsklick auf einen Abrechnungslauf öffnet sich ein Kontextmenü mit mehreren Optionen:

* Bearbeiten: Bearbeiten der Sollbuchung
* Löschen: Löschen der Sollbuchungen
* Mitglied anzeigen: Öffnet das Mitglied zur Sollbuchung
* Rechnung anzeigen: Zeigt die zur Sollbuchung gehörige Rechnung an
* Rechnung(en) erstellen: Erstellt Rechnungen für die selektierten Sollbuchungen (jeweils eine Rechnung pro Sollbuchung)
* Gesamtrechnung erstellen: Erstellt bei mehreren selektierten Sollbuchungen eine einzige Rechnung welche alle Sollbuchungspositionen der selektierten Sollbuchungen enthält

## Sollbuchung Neu Dialog

Mit einem Klick auf Neu öffnet sich folgender Dialog:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_SollbuchungNeuDialog.png" alt="" /></picture>

Über diesen Dialog wird eine Sollbuchung und eine zugeordnete Sollbuchungsposition erzeugt.

Folgende Buttons stehen zu Verfügung:

* Speichern: Speichert die Sollbuchung und schließt den Dialog
* Speichern und Anzeigen: Speichert die Sollbuchung, schließt den Dialog und zeigt die Sollbuchung zum bearbeiten an z.B. um eine weiter Sollbuchungsposition zu erzeugen
* Speichern und Neu: Speichert die Sollbuchung und erlaubt es eine weitere Sollbuchung zu erzeugen. Außer Mitglied und Zahler bleiben die Eingaben erhalten
* Abbrechen: Bricht das erstellen einer neuen Sollbuchung ab

PS: Datum und Zweck der Sollbuchungsposition werden automatisch von der Sollbuchung übernommen wenn sie noch nicht gesetzt sind.

## Sollbuchung

Mit einem Klick auf Bearbeiten öffnet sich folgender Dialog:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_SollbuchungView.png" alt="" /></picture>

Durch einen Doppelklick auf eine Sollbuchungsposition wird die Sollbuchungsposition angezeigt.

Folgende Buttons stehen zu Verfügung:

* Neu: Damit kann eine neue Sollbuchungsposition erzeugt werden. Bei einer neuen Sollbuchung können Sollbuchungsposition erst erzeugt werden wenn die Sollbuchung selbst einmal gespeichert wurde
* Speichern: Speichert die Sollbuchung

Durch einen Rechtsklick auf eine Sollbuchungsposition öffnet sich ein Kontextmenü mit mehreren Optionen:

* Bearbeiten: Bearbeiten der Sollbuchungsposition
* Istbuchung von Sollbuchung lösen: Löst die Buchung von der Sollbuchung
* Löschen: Löschen der Sollbuchungsposition

Durch einen Rechtsklick auf eine zugeordnete Buchung öffnet sich ein Kontextmenü mit mehreren Optionen:

* Bearbeiten: Bearbeiten der Buchung
* Mitglied anzeigen: Öffnet das Mitglied zur Buchung

Mit Version 3.0.0 wurde auch das Feld Zahler eingeführt. Hier kann ein vom Mitglied abweichender Zahler eingetragen werden. Eine Spendenbescheinigung wird dann auf den Zahler ausgestellt.

## Sollbuchungsposition

In diesem Dialog lassen sich die Felder der Sollbuchungsposition erzeugen.:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_SollbuchungpositionView.png" alt="" /></picture>
