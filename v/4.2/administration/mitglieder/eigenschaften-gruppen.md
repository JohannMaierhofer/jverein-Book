# Eigenschaftengruppen

Zur Gruppierung der Eigenschaften können Eigenschaften-Gruppen eingerichtet werden.

## Allgemeines

Für Mitglieder lassen sich Eigenschaften definieren. Diese lassen sich mit Eigenschaftengruppen gruppieren. Eingerichtet werden Eigenschaftengruppen unter Administration->Mitglieder->Eigenschaftengruppen.

Eingerichtete Eigenschaftengruppen erscheinen beim Mitglied unter dem Reiter "Eigenschaften".

Zusätzlich lassen sie sich in der Tabelle der Mitgliederliste als eigene Spalte anzeigen. Über die Spaltenauswahl des Panel Buttons kann die Anzeige ausgewählt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_MitgliederListeEigenschaftView.png" alt="" /></picture>

In dem Bild wurde die Eigenschaftengruppe "Abteilung" in der Tabelle eingeblendet.

Eigenschaftengruppen lassen sich auch als Variablen in Mails und Reports einfügen. Es wird dabei über den Namen adressiert. Intern wird `mitglied_eigenschaften_` vorne angefügt. Um z.B. beim Schreiben einer Mail auf die Eigenschaftengruppe Abteilung zuzugreifen, muss `$mitglied_eigenschaften_abteilung` eingegeben werden.

## Liste der Eigenschaftengruppen

Eine Liste der Eigenschaftengruppen kann über den Eintrag Administration->Mitglieder->Eigenschaftengruppen im Navigationsbaum angezeigt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_EigenschaftengruppenListeView.png" alt="" /></picture>

Mit Neu kann eine neue Eigenschaftengruppe eingerichtet werden.

Durch einen Doppelklick wird die Bearbeitung einer Eigenschaftengruppe eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Löschen: Damit kann eine Eigenschaftengruppe, deren keine Eigenschaft zugeordnet ist, gelöscht werden. Bei zugeordneten Eigenschaften erscheint eine Fehlermeldung

## Eigenschaftengruppe

Bei der Erstellung einer neuen Eigenschaftengruppe erscheint folgende Anzeige.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_Eigenschaftengruppe.png" alt="" /></picture>

Folgende Attribute sind vorhanden:

* Name: Name der Eigenschaftengruppe wie sie in den Mails, Formularen und Import/Export verwendet werden. Diese dürfen nur die Zeichen a-z, 0-9 und _ (Unterstrich) enthalten. Er darf keine Leerzeichen enthalten und sich nicht mit existierenden Namen überschneiden
* Bezeichnung: Name der am GUI von JVerein angezeigt wird. Hier gibt es keine Zeichen Beschränkung
* Pflicht: Den Eigenschaften-Gruppen gibt man mit, ob sie Pflichtfelder sind (es muss eine Eigenschaft dazu beim Mitglied angewählt werden) oder Kann-Felder (es kann eine Eigenschaft beim Mitglied angewählt werden)
* Maximal 1 Eigenschaft: Weiterhin kann man anwählen, ob man max. eine Eigenschaft (in Verbindung mit dem Flag "Pflicht" dann genau eine) anwählen kann.

Beispiel für eine Pflichtgruppe: Ein Mitglied gehört mindestens einer Abteilung des Vereins an.

Beispiel einer nicht-Pflichtgruppe: Ein Mitglied gehört dem Vorstand an.

Beispiel einer Eigenschaft Max. 1: Zahlungsart Abbuchung, Überweisung, Dauerauftrag, ggf. dann in Verbindung mit dem Pflicht-Flag.
