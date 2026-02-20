# Mitgliederstatistik

Für die Erstellung einer Statistik gibt es generell drei Möglichkeiten:

* Direkte Nutzung der Statistik-Funktion in JVerein. Diese erstellt direkt eine PDF-Datei mit Tabellen (keine Grafik)
* Export ausgewählter Daten mittels Mitglieder-Auswertung und Verarbeitung in einer Tabellenkalkulation
* Direkter Zugriff eines Analyse-Programms (z.B. OpenOffice) auf die JVerein-Datenbank

## Statistik-Funktion in JVerein

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_StatistikBeispiel.jpg" alt="" /></picture>

Für die Statistik ist ein Stichtag vorzugeben. Standardmäßig wird der 31.12. des aktuellen Jahres vorgegeben.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MitgliederStatistikView.png" alt="" /></picture>

### Altersgruppen

In der Statistik nach Altersgruppen wird der Mitgliederbestand nach den in den Einstellungen unter Statistik eingetragenen Altersgruppen summiert. Die Ausgabe erfolgt nach Geschlecht getrennt und insgesamt.

### Beitragsgruppen

Die Statistik nach Beitragsgruppen summiert den Mitgliederbestand nach den Beitragsgruppen nach Geschlecht und insgesamt.

### Anmeldungen/Abmeldungen\[Bearbeiten]

In diesem Bereich wird die Anzahl der An- und Abmeldungen zwischen dem 1.1. und dem eingegebenen Stichtag ermittelt.

## Statistik mittels Auswertung und Export

Unter Auswertungen->Mitglieder können die Mitgliederdaten zunächst nach diversen Kriterien gefiltert und das Ergebnis in eine CSV-Datei exportiert werden. In dieser Datei sind auch selbst definierte Eigenschaften und Zusatzfelder enthalten.

Mit einer Tabellenkalkulation wie Excel oder OpenOffice können die Daten dann eingelesen werden. Hier kann dann nochmals gefiltert werden. Natürlich können hier auch Grafiken erzeugt werden, wie Kuchendiagramme, Balkendiagramme usw.

Ein weitere wichtige Anwendung ist die Erstellung einer Bestandserhebung für einen Verband, wie z.B. einen Sportverband. Die Verbände verlangen oft eine spezifische Statistik die je nach Verband/Verein nur durch selbst definierte Eigenschaften und Zusatzfelder umgesetzt werden kann.

## Direkter Zugriff von OpenOffice/LibreOffice

Wenn häufig fest definierte Statistiken erstellt werden sollen kann dieser Weg der schnellste sein, denn aus OpenOffice/LibreOffice kann direkt auf die H2-Datenbank zugegriffen werden. Man benötigt dazu jedoch einige Kenntnisse der ooBase-Anwendung und auch SQL-Kenntnisse. Die Vorbereitung einer neuen Statistik ist hier also aufwändiger.
