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


## Liste der Sollbuchungen <a id="mitgliedskontouebersicht"></a>

Es gibt eine zentrale Übersicht über alle Sollbuchungen. Die Sollbuchungen können über einen Zeitraum oder über einen Namen der Mitglieds oder des Zahlers, bzw. Namensfragment gefiltert werden. Zusätzlich kann angegeben werden, ob nur Sollbuchungen mit Differenzen zwischen Soll und Ist \(Offene Posten oder Überzahlungen\) angezeigt werden.

Zudem lässt sich filtern ob das Mitglied per Lastschrift zahlt oder eine Mail Adresse hat.

![](img/SollbuchungenListeView.png)

Durch einen Doppelklick auf die Sollbuchung wird die Sollbuchung angezeigt.

Folgende Buttons stehen zu Verfügung:
* Exportieren: Damit können die Sollbuchungen als CSV Datei exportiert werden
* Neu: Damit kann eine neue Sollbuchung erzeugt werden

Durch einen Rechtsklick auf einen Abrechnungslauf öffnet sich ein Kontextmenü mit mehreren Optionen:
* Bearbeiten: Bearbeiten der Sollbuchung
* Löschen: Löschen der Sollbuchungen
* Mitglied anzeigen: Öffnet das Mitglied zur Sollbuchung
* Rechnung anzeigen: Zeigt die zur Sollbuchung gehörige Rechnung an
* Rechnung(en) erstellen: Erstellt Rechnungen für die selektierten Sollbuchungen


## Sollbuchung

Mit einem Klick auf Neu oder Bearbeiten öffnet sich folgender Dialog:

![](img/SollbuchungView.png)

Durch einen Doppelklick auf eine Sollbuchungsposition wird die Sollbuchungsposition angezeigt.

Folgende Buttons stehen zu Verfügung:
* Neu: Damit kann eine neue Sollbuchungsposition erzeugt werden. Bei einer neuen Sollbuchung können Sollbuchungsposition erst erzeugt werden wenn die Sollbuchung selbst einmal gespeichert wurde
* Speichern: Speichert die Sollbuchung

Durch einen Rechtsklick auf eine Sollbuchungsposition öffnet sich ein Kontextmenü mit mehreren Optionen:
* Bearbeiten: Bearbeiten der Sollbuchungsposition
* Löschen: Löschen der Sollbuchungsposition

Durch einen Rechtsklick auf eine zugeordnete Buchung öffnet sich ein Kontextmenü mit mehreren Optionen:
* Bearbeiten: Bearbeiten der Buchung
* Mitglied anzeigen: Öffnet das Mitglied zur Buchung

Mit Version 3.0.0 wurde auch das Feld Zahler eingeführt. Hier kann ein vom Mitglied abweichender Zahler eingetragen werden. Eine Spendenbescheinigung wird dann auf den Zahler ausgestellt.

## Sollbuchungsposition

In diesem Dialog lassen sich die Felder der Sollbuchungsposition editieren.:

![](img/SollbuchungpositionView.png)