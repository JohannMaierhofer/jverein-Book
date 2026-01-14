# Eigenschaftengruppen

Zur Gruppierung der Eigenschaften können Eigenschaften-Gruppen eingerichtet werden.

## Liste der Eigenschaftengruppen

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_Eigenschaftengruppen.png" alt="" /></picture>

Mit Neu kann eine neue Eigenschaftengruppe eingerichtet werden.

Durch einen Doppelklick wird die Bearbeitung einer Eigenschaftengruppe eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Löschen: Damit kann eine Eigenschaftengruppe, deren keine Eigenschaft zugeordnet ist, gelöscht werden. Bei zugeordneten Eigenschaften erscheint eine Fehlermeldung

## Eigenschaftengruppe

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_Eigenschaftengruppe.png" alt="" /></picture>

Folgende Attribute sind vorhanden:

* Name: Name der Eigenschaft wie sie in den Mails, Formularen und Import/Export verwendet werden. Diese dürfen nur die Zeichen a-z, 0-9 und _ (Unterstrich) enthalten. Er darf keine Leerzeichen enthalten und sich nicht mit existierenden Namen überschneiden
* Bezeichnung: Name der am GUI von JVerein angezeigt wird. Hier gibt es keine Zeichen Beschränkung
* Pflicht: Den Eigenschaften-Gruppen gibt man mit, ob sie Pflichtfelder sind (es muss eine Eigenschaft dazu beim Mitglied angewählt werden) oder Kann-Felder (es kann eine Eigenschaft beim Mitglied angewählt werden)
* Maximal 1 Eigenschaft: Weiterhin kann man anwählen, ob man max. eine Eigenschaft (in Verbindung mit dem Flag "Pflicht" dann genau eine) anwählen kann.

Beispiel für eine Pflichtgruppe: Ein Mitglied gehört mindestens einer Abteilung des Vereins an.

Beispiel einer nicht-Pflichtgruppe: Ein Mitglied gehört dem Vorstand an.

Beispiel einer Eigenschaft Max. 1: Zahlungsart Abbuchung, Überweisung, Dauerauftrag, ggf. dann in Verbindung mit dem Pflicht-Flag.
