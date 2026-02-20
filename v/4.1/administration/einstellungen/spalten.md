# Mitglieder Spalten

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Mitgliederspalten.png" alt="" /></picture>

Festlegung der Spalten, die in der Mitglieder Tabelle angezeigt werden sollen.

In diesem Dialog werden auch benutzerdefinierte [Zusatzfelder](../mitglieder/felddefinition.md) angezeigt. Diese können ebenfalls für die Anzeige in der Mitgliederliste selektiert werden.

In der Version 3.0.0 wurde eine optionale Spalten hinzu gefügt:

* Status\
  Ist diese Spalte platziert, dann zeigt sie an ob der gespeicherte Datensatz des Mitglied konsistent ist, also ob die Daten des Mitglieds aktuell fehlerfrei gespeichert werden könnten.\
  Es empfiehlt sich mit jeder neuen Version diese Spalte einmal zu aktivieren und zu schauen ob alle Einträge gut sind. Danach kann man die Spalte wieder entfernen.\
  Der Grund warum es zu inkonsistenten Einträgen kommen kann ist wenn in einer neuen Version verbesserte Checks implementiert wurden. Ein Beispiel ist die Eingabe der IBAN bei Lastschriften. Die IBAN wurde früher nicht geprüft und man konnte hier auch Unsinn eingeben. Dies wurde beim Speichern nicht festgestellt. In den aktuellen Versionen wird dies aber beim speichern geprüft.\
  Über die Spalte könnte man problematische Mitglieder leicht feststellen ohne jedes Mitglied zu öffnen und dort neu zu speichern

In der Version 3.1.0 sind zwei weiter optionale Spalten hinzu gefügt worden:

* Kontostand\
  Ist diese Spalte gesetzt, wird für jedes Mitglied durch ein Icon angezeigt ob das Mitglied einen ausgeglichenen Kontostand hat oder eine Fehlbetrag. Zusätzlich wird der aktuelle Kontostand angezeigt.\
  PS: Wegen einem Problem des Graphik Systems werden die Inhalte nicht rechtsbündig angezeigt wenn nicht eine der in der Liste vorangegangenen Spalten aktiviert wurde, also z.B. die Mitgliedsnummer oder Externe Mitgliedsnummer.\
  Da hierbei beim Aufbau der Mitgliederliste für jedes Mitglied auf die Datenbank zugegriffen werden muss um den aktuellen Kontostand zu berechnen könnte es abhängig von der verwendeten Datenbank Struktur zu Performance Problemen kommen. Sollte dies der Fall sein, sollte man diese Spalte nicht aktivieren
* D\
  Diese Spalte zeigt, wie bei Buchungen, an ob für das Mitglied ein Dokument hinterlegt ist und auch wie viele Dokumente
