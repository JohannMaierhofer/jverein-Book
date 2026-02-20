# Forderung

## Allgemein

Neben Mitgliedsbeiträgen können auch Zusatzbeträge (siehe  [Zusatzbeträge](zusatzbetrage.md)) abgerechnet werden (siehe [Abrechnungslauf](../abrech/abrechnung.md)). Dieses ist sinnvoll bei periodischen Zahlungen wie z.B. Mieteinnahmen.

Daneben gibt es auch einmalige Forderungen ohne Intervall wie z.B. Kursgebühren. Diese können ebenfalls durch Erstellen eines Zusatzbetrages ohne Intervall und anschließendem Abrechnungslauf abgerechnet werden.

Das Forderung Feature erlaubt das Erstellen einer einmaligen Forderung. In diesem Fall werden keine Zusatzbeträge benötigt bzw. erstellt.

Über einen Dialog werden die Daten der Forderung ähnlich zu denen für einen Zusatzbetrag eingegeben. Als weiteres die Daten wie sie bei einem Abrechnungslauf eingegeben werden. Über den "Erstellen" Button wird die Generierung gestartet. Ähnlich dem Abrechnungslauf werden Sollbuchung und bei Basislastschrift auch Lastschriften und Buchungen erzeugt.

Es wird auch ein Eintrag in der Tabelle der Abrechnungsläufe erzeugt mit dem Modus "Forderung". Bei Fehlern bei der Generierung kann dieser Eintrag gelöscht werden. Es werden dann auch alle generierten Daten gelöscht.

## Aufruf

Der Dialog kann über folgende Kontextmenüs aufgerufen werden:
* In der Liste der Mitglieder oder Nicht-Mitglieder
* In der Liste der Lehrgänge

## Dialog

Nach Auswahl der Menüeintrags "Forderung erstellen" öffnet sich folgender Dialog:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/401_ForderungDialog.png" alt="" /></picture>

Die Daten unter dem Punkt Forderung entsprechen den Eingaben in einem Zusatzbetrag (siehe  [Zusatzbeträge](zusatzbetrage.md)) aber ohne die Intervall Möglichkeit, da es sich um eine einmalige Aktion handelt.

Die anderen Daten entsprechen den Punkten aus dem Abrechnungslauf (siehe [Abrechnungslauf](../abrech/abrechnung.md)).

Die Felder für Rechnungen werden nur angezeigt wenn Rechnungen unter Administration->Einstellungen-> Anzeige aktiviert wurden.

In den Feldern für Zahlungsgrund und Rechnungstext können Variablen verwendet werden. Ist ein Text in Rechnungstext eingegeben, erscheint dieser als Zweck in der Sollbuchung. Werden keine Rechnungen erstellt oder es ist nichts eingegeben wird der Zahlungsgrund verwendet.

Es existieren folgende Buttons:
* Hilfe: Aufruf dieser Hilfe Seite
* Zahlungsgrund Variablen: Öffnet den Dialog der möglich Variablen für den Zahlungsgrund anzeigt
* Rechnungstext Variablen: Öffnet den Dialog der möglich Variablen für den Rechnungstext anzeigt
* Vorlagen: Öffnet den Vorlagen Dialog um bestehende Vorlagen auswählen zu können
* Auf Probleme prüfen: Prüft auf bestehende Probleme und zeigt diese in der Tabelle "Fehler/Warnungen/Hinweise" an
* Erstellen: Startet das Erstellen
* Abbrechen: Schließt den Dialog ohne Aktion

## Probleme

Mit dem Button "Auf Probleme prüfen" wird auf mögliche Probleme getestet. Beim Öffnen des Dialog passiert ein automatischer Test. Falls Fehler oder Warnungen gefunden werden kann die Erstellung nicht durchgeführt werden.

Die folgenden Prüfungen sind nur relevant wenn bei einem selektierten Mitglied bzw. Zahler der Zahlungsweg "Basislastschrift" eingetragen ist oder im Dialog der Zahlungsweg "Basislastschrift" ausgewählt ist.

Es werden folgende allgemeine Prüfungen durchgeführt:
* Es muss unter Administration->Einstellungen->Abrechnung ein Verrechnungskonto gesetzt sein
* Es muss unter Administration->Einstellungen->Allgemein ein Vereinsname gesetzt sein
* Es muss unter Administration->Einstellungen->Allgemein eine gültige IBAN gesetzt sein
* Unter Administration->Einstellungen->Allgemein ist eine BIC optional, aber wenn sie gesetzt ist muss sie gültig sein
* Es muss unter Administration->Einstellungen->Allgemein eine Gläubiger-ID gesetzt sein
* Die Fälligkeit muss in der Zukunft liegen

Falls bei einem Mitglied bzw. Zahler per Basislastschrift eingezogen wird muss bei diesem folgendes erfüllt sein:
* Es muss ein Mandat Datum gesetzt sein
* Das Mandat Datum darf nicht in der Zukunft liegen
* Es muss eine gültige  IBAN konfiguriert sein
* Eine BIC kann optional gesetzt sein, aber wenn sie gesetzt ist muss sie gültig sein
* Wenn noch keine Lastschrift in JVerein existiert darf das Mandat Datum nicht älter als 36 Monate sein. Falls man neu mit JVerein startet kann man im Dialog den SEPA-Check temporär deaktivieren
* Falls die letzte Lastschrift und das Mandat sind älter als 36 Monate muss ein neues Mandat angefordert werden