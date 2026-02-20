# Abrechnung

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Abrechnung.png" alt="" /></picture>

## Beitragsmodell

Beitragsmodell, siehe auch [Beitragsmodelle](../../../../allgemein/beitragsmodelle.md)

Die Standardwerte für den Zahlungsrhythmus und den Zahlungsweg bei der Speicherung neuer Mitglieder kann eingestellt werden.

## SEPA

Für die SEPA-Konvertierung ist das SEPA-Land auszuwählen.

SEPA XML-Version welche für die Generierung einer 1ct Überweisung (pain.001...) bzw. einer Lastschrift (pain.008...) XML Datei verwendet wird.

Unterstützte Versionen sind aus folgender Tabelle ersichtlich.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_SepaSupportedVersions.png" alt="" /></picture>

## Verrechnungskonto für Lastschriften

Hier wird das Konto ausgewählt auf dem die beim Abrechnungslauf erzeugten Buchungen für Lastschriften erzeugt werden.

## Arbeitsstundenmodell

Mit dem Arbeitsstundenmodel wird die Buchung von Arbeitsstunden eingestellt.

Mögliche Werte sind:

### Standardverfahren

Es können beim Erfassen der Arbeitsstunden nur positive Werte im Stundenfeld eingegeben werden.

### Negative Stunden erlaubt

Beim Erfassen der Arbeitsstunden vom Mitgliedern können im Stundenfeld positive und negative Werte eingetragen werden. Positive und negative Werte können sich gegenseitig aufheben. Negative Werte können die Gesamtschuld an Arbeitsstunden bei einem Mitglied erhöhen und zu einer höheren Buchung von Zusatzbeiträgen führen.

## Altersstufen für gestaffelte Beiträge

Hier können für die Verwendung in gestaffelten Beiträgen die Altersbereiche eingegeben werden für die jeweils ein anderer Beitrag eingegeben werden kann.

## Zusatzbeträge auch für Ausgetretene abrechnen

Ist dies aktiviert, werden Zusatzbeträge auch für ausgetretene Mitglieder abgerechnet.

## Keine Istbuchung bei Lastschriften erzeugen

Standard mäßig erzeugt die Abrechnung beim Zahlungsweg "Basislastschrift" neben der Sollbuchung auch direkt eine Buchung auf dem konfigurierten Konto. Diese wird auch direkt der Sollbuchung zugewiesen. Daneben wird eine Gegenbuchung mit dem Summen Betrag aller erzeugten Buchungen generiert. Diese hebt die Buchungen auf so dass der Kontostand ausgeglichen ist. Dieser Betrag wird dann von der Bank eingezogen und verbucht.

In Fällen, dass die Lastschriften mit externen Tools abgerechnet werden und die Lastschriften nicht als Summen Betrag eingehen, sondern als einzelne Buchungen per Mitglied kann über diese Option die Generierung der Istbuchungen und der Gegenbuchung verzichtet werden.

## Abrechnungslauf abschließen

Funktionalität zum Abschließen von Abrechnungsläufen einschalten.

## Quelle für SEPA-Mandatsreferenz

Hier lässt sich auswählen wie die Mandats-ID beim Mitglied gebildet wird.

* Mitgliedsnummer
* Externe Mitgliedsnummer
* Individuelle ID (neu in Version 3.1.0)
