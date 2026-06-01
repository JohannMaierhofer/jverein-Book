# Eigenschaften

## Allgemeines

Für Mitglieder lassen sich Eigenschaften definieren. Eingerichtet werden Eigenschaften unter Administration->Mitglieder->Eigenschaften.

Im Gegensatz zu Zusatzfeldern (siehe [Zusatzfelder ](felddefinition.md)) ist die Bezeichnung vorgegeben und sie können sie nur selektiert werden. Bei Zusatzfeldern können je nach Datentyp Mitglied individuelle Daten eingegeben werden.

Jeder Eigenschaft ist eine [Eigenschaftengruppe ](eigenschaften-gruppen.md) zuzuordnen.

Eingerichtete Eigenschaften erscheinen beim Mitglied unter dem Reiter "Eigenschaften" und können dort ausgewählt werden. Über das Mitglied Menü in der Liste der Mitglieder können Eigenschaften für alle selektierten Mitglieder gleichzeitig gesetzt bzw. gelöscht werden.

Zusätzlich werden sie in der Tabelle der Mitgliederliste in der Spalte der zugehörigen Eigenschaftengruppe anzeigen. Über die Spaltenauswahl des Panel Buttons kann die Anzeige der zugehörigen Eigenschaftengruppe ausgewählt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_MitgliederListeEigenschaftView.png" alt="" /></picture>

In dem Bild wurde die Eigenschaftengruppe "Abteilung" in der Tabelle eingeblendet. Bei dem Mitglied Koch Otto wird die gesetzte Eigenschaft "Gymnastik" angezeigt.

Eigenschaften lassen sich auch als Variablen in Mails und Reports einfügen. Es wird dabei über den Namen adressiert. Intern wird `mitglied_eigenschaft_` vorne angefügt. Um z.B. beim Schreiben einer Mail auf das Zusatzfeld Übungsleiter zuzugreifen, muss `$mitglied_eigenschaf_gymnastik` eingegeben werden.

## Liste der Eigenschaften

Eine Liste der Eigenschaften kann über den Eintrag Administration->Mitglieder->Eigenschaften im Navigationsbaum angezeigt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_EigenschaftenListeView.png" alt="" /></picture>

Mit Neu kann eine neue Eigenschaft eingerichtet werden.

Durch einen Doppelklick wird die Bearbeitung einer Eigenschaft eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Löschen: Damit kann eine Eigenschaft gelöscht werden

## Eigenschaft

Bei der Erstellung einer neuen Eigenschaft erscheint folgende Anzeige.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_Eigenschaft.png" alt="" /></picture>


Folgende Attribute sind vorhanden:

* Name: Name der Eigenschaft wie sie in den Mails, Formularen und Import/Export verwendet werden. Diese dürfen nur die Zeichen a-z, 0-9 und _ (Unterstrich) enthalten. Er darf keine Leerzeichen enthalten und sich nicht mit existierenden Namen überschneiden
* Bezeichnung: Name der am GUI von JVerein angezeigt wird. Hier gibt es keine Zeichen Beschränkung
* Gruppe: Zugeordnete Eigenschaften Gruppe
