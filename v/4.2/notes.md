# Release Notes

## Allgemeines

Die Version 4.2 ist eine Minor Version und rückwärts kompatibel mit einer 4.1 und 4.0.

## The Big Ones

### Spaltenauswahl bei View Tabellen und Reports

Es gibt eine allgemeine Erweiterung für alle Tabellen, außer den Saldo Tabellen. Es lässt sich einstellen, welche Spalten in den Tabellen am GUI angezeigt werden. Auch können die Tabellen als CSV und PDF ausgegeben werden.

Bei der Ausgabe als CSV oder PDF erfolgt eine Dialogabfrage in dem man die auszugebenden Spalten auswählen kann. Die Breite der Spalten im PDF Report orientiert sich am Breitenverhältnis der Spalten in der GUI Anzeige.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_SpaltenauswahlDialog.png" alt="" /></picture>

Die Buttons sind in der Panelleiste oben verfügbar.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_Panelbuttons.png" alt="" /></picture>

Drei Buttons sind verfügbar:
* CSV: Gib die ausgewählten Spalten der angezeigten Tabelle als CSV Datei aus
* PDF: Gibt die ausgewählten Spalten der angezeigten Tabelle als PDF aus
* Spalten auswählen: Es lässt sich auswählen, welche Spalten in der Tabelle angezeigt werden sollen

PS: Da die anzuzeigenden Spalten nun damit ausgewählt werden können wurde diese Option für Mitglieder in den Einstellungen entfernt. Leider konnten die Konfiguration aus den Einstellungen nicht mit übernommen werden. Es erfolgt eine feste Auswahl als Default. 

### Arbeitseinsatz Auswertung

* Die Auswertung der Arbeitseinsätze wird jetzt in einem Dialog angezeigt und kann nur noch aus der Liste der Arbeitseinsätze aufgerufen werden
* Der Menüeintrag im Navigationsbaum unter Auswertung ist entfernt worden
* Über einen eigenen Button in der Liste der Arbeitseinsätze können die Zusatzbeträge für nicht geleistete Arbeitseinsätze erstellt werden. Der zugehörige Dialog erlaubt es jetzt auch Daten des Zusatzbetrags einzugeben wie Zahlungsgrund, Fälligkeit, Zahlungsweg und ob das Mitglied selbst bezahlt
* Über einen weiteren Button kann direkt eine Abrechnung durchgeführt werden. Es ist dann nicht der Umweg über die Generierung von Zusatzbeträgen und anschließendem Abrechnungslauf nötig
* Ähnlich wie beim Abrechnungslauf Dialog werden in den beiden Dialogen auch die Lastschrift Tests durchgeführt

### Projektauswahl bei Projektsaldo

* Im Projektsaldo View lässt sich jetzt auch ein individuelles Projekt auswählen

### Wirtschaftsplan für Projekte

* Falls Projekte aktiviert sind, lassen sich im Wirtschaftsplan jetzt auch Projekte auswählen. Damit können Wirtschaftspläne für einzelne Projekte erstellt werden

### Mail Empfänger Dialog Redesign

Im Mailempfänger Auswahldialog wurden einige Änderungen durchgeführt:
* Es wird jetzt angezeigt welche Mitglieder, Eigenschaften und Eigenschaften Verknüpfung ausgewählt sind
* Eigenschaften werden jetzt mit den selektierten Mitgliedern über eine UND Operation verknüpft
* Bei den Eigenschaften lässt sich jetzt auch die Nicht-Eigenschaft auswählen
* Bei den Eigenschaften lässt sich jetzt auch die Verknüpfung und/oder auswählen

### Reports bei Abrechnungslauf

In den vier Laschen im Abrechnungslauf View ist jetzt bei allen die Ausgabe der Liste als PDF oder CSV unterstützt.

Diese Reports benutzen eine generische Implementierung zu Generierung der Reports aus den angezeigten Tabellen.
* Es wird ein Dialog geöffnet mit dem sich die Spalten auswählen lassen die ausgegeben werden sollen
* Die Breite der Spalten im PDF Report orientieren sich an der Breite der Spalten in der Anzeige

### Menü in Saldo Views

* In den Saldo View wie Buchungsklassensaldo etc. sind jetzt Menüs implementiert
* Über "Bearbeiten" oder Doppel Klick lässt sich die selektierte Buchungsklasse etc. editieren
* Über "Buchungen anzeigen" werden die Buchungen hinter der selektierten Zeile in einem Dialog angezeigt
* Über "Steuerbuchungen anzeigen" werden die Buchungen angezeigt die Steuer zur Steuerzeile beitragen

### Automatische Sollbuchung Zuordnung Redesign

Beim Zuordnung nach Name wird die Buchung jetzt auch gefunden wenn:
* Auch weiterer Text (Namen) im Namen der Buchung stehen, oder in andere Reihenfolge
* Der Name wird auch im Zweck der Buchung gesucht
* Es wird auch nach dem Kontoinhaber im Namen der Buchung gesucht
* Auch nach dem Namen und Kontoinhaber des abweichenden Zahlers wird gesucht

Bei Zuordnung nach Zweck kann der Zweck der Buchung auch weiteren Text enthalten.

Bei Zuordnung nach ID darf nur die ID im Zweck stehen so wie bisher. Sonst gibt es zu viele falsche Treffer, es sei denn, man hat externe IDs die komplexer sind.

Es muss nun nicht mehr eine für alle Mitglieder eindeutige IBAN, Name + Vorname oder Zweck sein. Es reicht, wenn die Buchung im gewählten Zeitraum nur für eine Sollbuchung passt. Sonst würde z.B. eine Zuordnung nach Name nie funktionieren, wenn man zwei Mitglieder mit gleichem Namen hat, diese aber unterschiedliche Beträge bezahlen.

In der Zuordnungsvorschau wurden Checkboxen hinzugefügt, so kann man individuell einzelne Buchungen abwählen, wenn diese nicht zugeordnet werden sollen.

In der Vorschau wurden einige zusätzliche Spalten hinzugefügt, so dass man besser prüfen kann, ob die Zuordnung richtig ist.


## Kleinere Korrekturen und Erweiterungen

### Stichtag Implementierung geändert 

* Der Stichtag Input wurde im Filterbereich der Mitglieder Liste direkt unterhalb der Mitgliedschaft platziert. Es wurde oft übersehen, dass der Stichtag bei der Filterung nach Mitgliedschaft entscheidend ist
* Wenn kein Stichtag eingegeben ist, wird jetzt das aktuelle Datum verwendet
* Abgemeldet ist jetzt auch wenn der Eintritt nach dem Stichtag liegt
* Angemeldet ist jetzt wenn entweder kein Eintritt konfiguriert ist oder dieser vor oder zum Stichtag liegt und entweder kein Austritt konfiguriert ist oder dieser nach dem Stichtag liegt
* Es wird beim Speichern eines Mitglied geprüft, dass Austritt nach Eintritt liegt

### Zweck bei Lastschriften einstellbar

Bei der Generierung des Zweck bei Lastschriften wird die Zahler ID und Zahler Name dem in Dialogen konfiguriertem Zweck vorangestellt.

Ab Version 4.2.0 lässt sich dieses Verhalten unter Administration->Einstellungen->Abrechnung abwählen.

### Spendenbescheinigung anzeigen im Buchung Menü

Im Menü der Buchung gibt es nun den Menüpunkt "Spendenbescheinigung anzeigen". Falls für eine Buchung eine Spendenbescheinigung existiert, kann sie damit angezeigt werden.



## Sonstiges

* Einige Fehlerkorrekturen
* Der Menüeintrag "In Zwischenablage kopieren" beim Mitglied wurde gelöscht. Wie bei den anderen Tabellen ist das über CTRL-C weiter möglich
* Manuelle Buchungen auf einer Steuerbuchungsart werden nicht unterstützt
