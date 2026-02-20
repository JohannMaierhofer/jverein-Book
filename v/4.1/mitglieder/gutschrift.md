# Gutschrift

## Allgemein

Das Feature Gutschrift bietet unterschiedlich Funktionalität.

#### Stornierung von bestehenden Rechnungen oder Sollbuchungen

Bei der Auswahl von Rechnungen oder Sollbuchungen (bei selektierten Abrechnungsläufen alle zugewiesenen Sollbuchungen) können diese storniert werden. Hierbei ist die Option "Fixen Betrag erstatten" nicht selektiert.

Beim Erstellen wird folgendes erzeugt:
* Eine Sollbuchung mit dem negativen Betrag der selektierten Rechnung bzw. Sollbuchung
* Eine Buchung mit dem negativen Betrag der selektierten Rechnung bzw. Sollbuchung. Diese wird der erzeugten Sollbuchung zugewiesen wodurch sie ausgeglichen ist
* Eine Überweisung des Betrags an den Zahler der Sollbuchung. Falls die Rechnung bzw. Sollbuchung nicht vollständig bezahlt wurde, wird nur der bereits bezahlte Betrag überwiesen. Wurde noch nichts bezahlt, dann erfolgt auch keine Überweisung
* Eine Gegenbuchung über die Summe aller Überweisungen ähnlich wie bei Abrechnungsläufen mit Lastschriften
* Falls die Rechnung bzw. Sollbuchung nicht vollständig bezahlt wurde, wird eine Ausgleichsbuchung erzeugt welche der selektierten Sollbuchung zugewiesen wird, bei Rechnung, der der Rechnung zugewiesenen Sollbuchung. Die Ausgleichsbuchung führt dazu, dass die selektierte Rechnung bzw. Sollbuchung ausgeglichen ist und nicht mehr als offen erscheint

Alle erzeugten Buchungen heben sich auf dem Verrechnungskonto gegenseitig auf.

#### Teilweise Erstattung von fixen Beträgen bei bestehenden Rechnungen oder Sollbuchungen

Bei der Auswahl von Rechnungen oder Sollbuchungen (bei selektierten Abrechnungsläufen alle zugewiesenen Sollbuchungen) können feste Beträge erstattet werden z.B. bei einem teilweisen Erlass von Gebühren. Hierbei ist die Option "Fixen Betrag erstatten" selektiert. Es wird die Forderung der ursprünglichen Rechnung bzw. Sollbuchung um einen festen Betrag reduziert.

Beim Erstellen wird folgendes erzeugt:
* Eine Sollbuchung mit dem negativen Wert des zu erstattenden Betrags
* Eine Buchung mit dem negativen Betrag des zu erstattenden Betrags. Diese wird der erzeugten Sollbuchung zugewiesen wodurch sie ausgeglichen ist
* Eine Überweisung des zu erstattenden Betrags an das Zahler der Sollbuchung. Falls die Rechnung bzw. Sollbuchung nicht vollständig bezahlt wurde, wird der zu erstattenden Betrag mit dem noch offenen Betrag verrechnet und dann eventuell nichts oder nur ein Teil überwiesen 
* Eine Gegenbuchung über die Summe aller Überweisungen ähnlich wie bei Abrechnungsläufen mit Lastschriften
* Falls eine Verrechnung mit offenen Beträgen stattgefunden hat, wird eine Ausgleichsbuchung erzeugt welche der selektierten Sollbuchung zugewiesen wird, bei Rechnung, der der Rechnung zugewiesenen Sollbuchung. Die Ausgleichsbuchung gleicht den zu verrechneten Betrag aus damit dieser nicht mehr als offen vorhanden ist

Alle erzeugten Buchungen heben sich auf dem Verrechnungskonto gegenseitig auf.

#### Storno oder teilweise Erstattung von fixen Beträgen bei selektierten Lastschriften

Lastschriften sind immer vollständig bezahlt. Es erfolgt also ein Storno mit Überweisung des vollen Betrags oder eine Überweisung eines fixen Betrags.

Beim Erstellen wird folgendes erzeugt:
* Eine Sollbuchung mit dem negativen Wert des zu erstattenden Betrags falls in der Lastschrift ein Mitglied eingetragen ist, also nicht bei Kursteilnehmern
* Eine Buchung mit dem negativen Betrag des zu erstattenden Betrags. Diese wird der erzeugten Sollbuchung zugewiesen falls sie existiert, wodurch sie ausgeglichen ist
* Eine Überweisung des zu erstattenden Betrags an die in der Lastschrift hinterlegten IBAN und Name
* Eine Gegenbuchung über die Summe aller Überweisungen ähnlich wie bei Abrechnungsläufen mit Lastschriften

Alle erzeugten Buchungen heben sich auf dem Verrechnungskonto gegenseitig auf.

#### Erstattung von fixen Beträgen bei selektierten Mitgliedern

Selektierten Mitgliedern können fixe Beträge erstattet werden.

Beim Erstellen wird folgendes erzeugt:
* Eine Sollbuchung mit dem negativen Wert des zu erstattenden Betrags
* Eine Buchung mit dem negativen Betrag des zu erstattenden Betrags. Diese wird der erzeugten Sollbuchung zugewiesen, wodurch sie ausgeglichen ist
* Eine Überweisung des zu erstattenden Betrags an das Mitglied (PS: es muss eine IBAN beim Mitglied gesetzt sein)
* Eine Gegenbuchung über die Summe aller Überweisungen ähnlich wie bei Abrechnungsläufen mit Lastschriften

Alle erzeugten Buchungen heben sich auf dem Verrechnungskonto gegenseitig auf.

#### Rechnung erstellen

Falls in den Einstellungen Rechnungen aktiviert sind und die Checkbox "Rechnung zur Gutschrift erzeugen" selektiert ist, wird zur erzeugten Sollbuchungen eine Rechnung generiert.

Die Rechnung hat ab 4.1 drei neue Attribute. Diese werden bei Gutschriften mit Daten gefüllt.
* Rechnungstext: Dies ist der evaluierte Rechnungstext aus dem Dialog. Er wird in der Liste der Rechnungen und im Rechnung View angezeigt
* Referenz Rechnung: Es ist eine Referenz auf die ursprüngliche Rechnung die mit dieser Rechnung storniert oder reduziert wurde
* Erstattungsbetrag: Dies ist der Betrag der bei dieser Rechnung an das Mitglied überwiesen wurde

Diese drei werte sind auch in den Variablen enthalten damit sie in Rechnungsformularen verwendet werden können. Bei der Referenz Rechnung ist die Rechnungsnummer der Referenz in den Variablen enthalten.

#### Abrechnungslauf Eintrag

Es wird auch ein Eintrag in der Tabelle der Abrechnungsläufe erzeugt mit dem Modus "Gutschrift". Bei Fehlern bei der Generierung kann dieser Eintrag gelöscht werden. Es werden dann auch alle generierten Daten gelöscht.

## Aufruf

Der Dialog kann über folgende Kontextmenüs aufgerufen werden:
* In der Liste der Mitglieder oder Nicht-Mitglieder
* In der Liste der Sollbuchungen
* in Der Liste der Sollbuchungen im Tab "Mitgliedskonto" beim Mitglied
* In der Liste der Rechnungen
* In der Liste der Abrechnungsläufe (für die vom Abrechnungslauf generierten Sollbuchungen)
* In der Liste der Lastschriften

## Dialog

Nach Auswahl der Menüeintrags "Forderung erstellen" öffnet sich folgender Dialog:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_GutschriftDialog.png" alt="" /></picture>

Es existieren folgende Eingabefelder:
* Ausgabe: Ausgabeart für die Überweisungen, entweder Hibiscus oder Datei
* Ausführungsdatum: Ausführungsdatum für die Überweisung
* Verwendungszweck: Verwendungszweck in der Überweisung. Als Verwendungszweck in der Sollbuchung falls kein Rechnungstext konfiguriert ist
* Fixen Betrag erstatten: Es wird nicht der ganze Betrag der Sollbuchung bzw. Rechnung erstattet sondern ein fixer Betrag. PS: Sind Mitglieder selektiert, dann ist nur ein fixer Betrag möglich und die Checkbox wird nicht angezeigt
* Erstattungsbetrag: Erstattungsbetrag bei fixem Betrag
* Buchungsart: Buchungsart für die Erstattung-Buchung
* Buchungsklasse: Buchungsklasse für die Erstattung-Buchung (Nur vorhanden wenn in den Einstellungen keine feste Zuordnung von Buchungsklasse zu Buchungsart konfiguriert ist)
* Steuer: Steuer für die Erstattung-Buchung (Nur vorhanden wenn in den Einstellungen Steuer individuell pro Buchung konfiguriert ist)

Die folgenden Eingabefelder werden nur angezeigt wenn in den Einstellung die Rechnung Option aktiviert ist.
* Rechnung zur Gutschrift erzeugen: Erzeugt eine Rechnung falls für die Gutschrift eine Sollbuchung erzeugt wird. PS: Bei Lastschriften für Kursteilnehmer werden keine Sollbuchungen erzeugt weil diese keine Mitglieder bzw. Nicht-Mitglieder sind
* Erstattungsformular: Formular für die Rechnung
* Rechnungsdatum: Datum der Rechnung
* Rechnungstext: Der Rechnungstext wird im Feld Zweck in der Sollbuchung eingetragen. Werden keine Rechnungen erstellt oder es ist nichts eingegeben wird der Zahlungsgrund verwendet
* Kommentar: Text der in den Kommentar der Rechnung eingetragen wird

Es existieren folgende Buttons:
* Hilfe: Aufruf dieser Hilfe Seite
* Verwendungszweck Variablen: Öffnet den Dialog der möglich Variablen für den Zahlungsgrund anzeigt
* Rechnungstext Variablen: Öffnet den Dialog der möglich Variablen für den Rechnungstext anzeigt
* Auf Probleme prüfen: Prüft auf bestehende Probleme und zeigt diese in der Tabelle "Fehler/Warnungen/Hinweise" an
* Erstellen: Startet das Erstellen
* Abbrechen: Schließt den Dialog ohne Aktion

## Probleme

Mit dem Button "Auf Probleme prüfen" wird auf mögliche Probleme getestet. Beim Öffnen des Dialog passiert ein automatischer Test. Falls Fehler  gefunden werden kann die Erstellung nicht durchgeführt werden.

Da mit diesem Feature Überweisungen erstellt werden sind alle Prüfungen relevant.

Es werden folgende allgemeine Prüfungen auf Fehler durchgeführt:
* Es muss unter Administration->Einstellungen->Abrechnung ein Verrechnungskonto gesetzt sein
* Es muss unter Administration->Einstellungen->Allgemein ein Vereinsname gesetzt sein
* Es muss unter Administration->Einstellungen->Allgemein eine gültige IBAN gesetzt sein
* Unter Administration->Einstellungen->Allgemein ist eine BIC optional, aber wenn sie gesetzt ist muss sie gültig sein

Falls Fehler gefunden werden, kann die Erstellung nicht gestartet werden.

Es werden folgende allgemeine Prüfungen auf Warnung durchgeführt:
* Außer in Lastschriften muss ein Mitglied/Zahler gesetzt sein muss
* Beim Mitglied/Zahler muss eine gültige  IBAN konfiguriert sein
* Beim Mitglied/Zahler kann eine BIC optional gesetzt sein, aber wenn sie gesetzt ist muss sie gültig sein
* Der Betrag bei einer selektierten Rechnung oder Sollbuchung darf nicht negativ sein
* Der Zahlungseingang bei einer selektierten Rechnung oder Sollbuchung darf nicht negativ sein
* Bei Rechnungen muss diesen eine Sollbuchung zugeordnet sein
* Betroffenen Sollbuchungen müssen Sollbuchungspositionen zugeordnet sein
* Bei allen Sollbuchungspositionen muss eine Buchungsart gesetzt sein
* Die Option "Fixer Betrag" wird nicht für Gesamtrechnungen unterstützt
* Bei der Option "Fixer Betrag" muss der fixe Betrag kleiner oder gleich dem Betrag der Sollbuchungspositionen mit der gleichen Buchungsart, Buchungsklasse und Steuer sein 

Falls Warnungen gefunden werden erscheint beim Erstellen ein Dialog, der den Anwender informiert und fragt ob fortgefahren werden soll. Wird fortgefahren, dann werden Einträge mit Warnungen bei der Erstellung übersprungen.


## Problembehandlung

Existiert in der Tabelle "Fehler/Warnungen/Hinweise" ein Eintrag, kann durch einen Doppel-Klick auf den Eintrag dieser angezeigt werden. Der Dialog bleibt dabei geöffnet.

Jetzt kann beim Eintrag der Fehler behoben werden z.B. durch Eingabe der IBAN. Nach Speichern des Eintrags kann erneut auf Probleme getestet werden.
