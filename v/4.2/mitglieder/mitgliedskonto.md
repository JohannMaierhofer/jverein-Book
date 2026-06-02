# Sollbuchungen

### Aktivierung

Zur Nutzung der Sollbuchungen ist keine extra Aktivierung notwendig.

### Allgemeines

Sollbuchungen sind keine Buchungen in einem Konto und sie tauchen auch nicht im Buchungsklassensaldo auf. Sollbuchungen sind primär Forderungen an ein Mitglied oder Nicht-Mitglied. Bei Forderungen kann es sich um Beiträge, Zusatzbeiträge oder jede andere Art von Geldforderung handeln.

Sollbuchungen werden einem Mitglied oder Nicht-Mitglied zugeordnet und dokumentieren so seine an ihn gestellten Forderungen. Die Sollbuchungen werden in der Liste der Sollbuchungen aufgeführt, aber auch in der Lasche "Mitgliedskonto" beim Mitglied oder Nicht-Mitglied.

Wird die Forderung vom Mitglied durch eine Buchung auf einem Konto beglichen, muss diese der Sollbuchung zugewiesen werden. Diese Zuweisung erfolgt bei Abrechnungsläufen mit Lastschrift automatisch, weil hier automatisch sowohl eine Sollbuchung als auch eine zugehörige Buchung erzeugt wird. In den anderen Fällen muss die Zuordnung manuell erfolgen (siehe [Buchungen](../buchf/buchungen.md)).

Durch die Zuordnung der Buchung wird die Forderung an das Mitglied bzw. Nicht-Mitglied ausgeglichen. Setzt man in der Liste der Sollbuchungen den Filter "Differenz" auf "Fehlbetrag" erhält man alle Sollbuchungen die noch nicht beglichen wurden. So kann man z.B. feststellen welche Mitglieder bei Überweisung ihren Beitrag noch nicht bezahlt haben. Auch in der Lasche "Mitgliedskonto" beim Mitglied oder Nicht-Mitglied kann man den aktuellen Stand seine Zahlungen sehen.

Der aktuelle Kontostand eine Mitglieds lässt sich auch in der Liste der Mitglieder als eigene Spalte einblenden. Da dieser beim Aufbau der Tabelle jeweils berechnet werden muss kann es zu Performance Problemen bei der Anzeige der Liste kommen. Diese Spalte sollte also nur bei Bedarf eingeschaltet werden.

PS: Um Spendenbescheinigungen automatisch zu generieren müssen die Spendenbuchungen auch einer Sollbuchung zugeordnet werden. Nur dadurch kann die Software erkennen welchem Mitglied die Spende zuzuordnen ist. In diesem Fall ist die Sollbuchung keine Forderung, weil die Spende ja freiwillig ist. 

Sollbuchungen sind auch die Voraussetzung für Rechnungen. Falls Rechnungen ausgestellt werden, wird üblicherweise für jede Sollbuchung eine Rechnung erzeugt. Diese kann direkt bei einem Abrechnungslauf mit generiert werden. Manuell lassen sich aber auch mehrere Sollbuchungen zu einer Gesamtrechnung zusammen fassen. Da aber auch mehrere Sollbuchungspositionen in einer Sollbuchung stehen können ist das normalerweise nicht nötig.

### Erstellung

Die Sollbuchungen können erstellt werden

* automatisch bei einen Abrechnungslauf (siehe [Abrechnung](../abrech/abrechnung.md) )
* automatisch bei eine Forderung Abrechnung (siehe [Forderung](forderung.md))
* automatisch bei einer Gutschrift Abrechnung (siehe [Gutschrift](gutschrift.md))
* automatisch bei einer Abrechnung von Arbeitseinsätzen (siehe [Arbeitseinsätze](arbeitseinsatz.md))
* automatisch über die Zuordnung einer Sollbuchung zu einer Buchung bei der im Dialog ein Mitglied ausgewählt wird (siehe [Buchungen](../buchf/buchungen.md))
* manuell in den Mitglied Details (siehe [Mitgliedskonto](content/mitgliedskonto.md))
* manuell in der Liste der Sollbuchungen

Im Normalfall sollte die Erstellung der Sollbuchungen nur automatisch erfolgen. Nur in Ausnahmesituationen ist ein manuelles erstellen sinnvoll.

## Liste der Sollbuchungen <a href="#mitgliedskontouebersicht" id="mitgliedskontouebersicht"></a>

Es gibt eine zentrale Übersicht über alle Sollbuchungen. Die Sollbuchungen können über einen Zeitraum oder über einen Namen der Mitglieds oder des Zahlers, bzw. Namensfragment gefiltert werden.

Zusätzlich kann angegeben werden, ob nur Sollbuchungen mit Differenzen zwischen Soll und Ist (Offene Posten oder Überzahlungen) über dem konfigurierten Limit angezeigt werden.

Zudem lässt sich filtern ob das Mitglied per Lastschrift zahlt oder eine Mail Adresse hat.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_SollbuchungenListeView.png" alt="" /></picture>

Durch einen Doppelklick auf die Sollbuchung wird die Sollbuchung angezeigt.

Folgende Buttons stehen zu Verfügung:

* Exportieren: Damit können die Sollbuchungen als CSV Datei exportiert werden
* Neu: Damit kann eine neue Sollbuchung erzeugt werden

Durch einen Rechtsklick auf einen Abrechnungslauf öffnet sich ein Kontextmenü mit mehreren Optionen:

* Bearbeiten: Bearbeiten der Sollbuchung
* Löschen: Löschen der Sollbuchungen
* Mitglied anzeigen: Öffnet das Mitglied zur Sollbuchung
* Rechnung anzeigen: Zeigt die zur Sollbuchung gehörige Rechnung an
* Rechnung erstellen: Erstellt Rechnungen für die selektierten Sollbuchungen (jeweils eine Rechnung pro Sollbuchung)
* Gesamtrechnung erstellen: Erstellt bei mehreren selektierten Sollbuchungen eine einzige Rechnung welche alle Sollbuchungspositionen der selektierten Sollbuchungen enthält
* Gutschrift erstellen: Öffnet den Dialog zum Erstellen von Gutschriften, siehe [Gutschrift](gutschrift.md)

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

Die Sollbuchung enthält folgende Daten:

* Mitglied: Das Mitglied/Nicht-Mitglied dem die Sollbuchung zugewiesen ist, also an welches Mitglied die Forderung gerichtet ist
* Zahler: Das Mitglied/Nicht-Mitglied welches die Forderung bezahlt z.B. Eltern eine Kindes. Eine Spendenbescheinigung wird auf den Zahler ausgestellt
* Datum: Datum der Sollbuchung
* Verwendungszweck: Zweck
* Zahlungsweg: Zahlungsweg
* Betrag: Betrag der Sollbuchung
* Liste der Sollbuchungspositionen: Es können mehrere unterschiedliche Forderungen zu eine Sollbuchung beitragen
* Liste der Buchungen: Buchungen, die der Sollbuchung zugewiesen wurden

Durch einen Doppelklick auf eine Sollbuchungsposition wird die Sollbuchungsposition angezeigt.

Folgende Buttons stehen zu Verfügung:

* Neu: Damit kann eine neue Sollbuchungsposition erzeugt werden. Bei einer neuen Sollbuchung können Sollbuchungsposition erst erzeugt werden wenn die Sollbuchung selbst einmal gespeichert wurde
* Speichern: Speichert die Sollbuchung

Durch einen Rechtsklick auf eine Sollbuchungsposition öffnet sich ein Kontextmenü mit mehreren Optionen:

* Bearbeiten: Bearbeiten der Sollbuchungsposition
* Löschen: Löschen der Sollbuchungsposition

Durch einen Rechtsklick auf eine zugeordnete Buchung öffnet sich ein Kontextmenü mit mehreren Optionen:

* Bearbeiten: Bearbeiten der Buchung
* Istbuchung von Sollbuchung lösen: Löst die Buchung von der Sollbuchung
* Mitglied anzeigen: Öffnet das Mitglied zur Buchung

## Sollbuchungsposition

In diesem Dialog lassen sich die Felder der Sollbuchungsposition erzeugen.:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_SollbuchungpositionView.png" alt="" /></picture>
