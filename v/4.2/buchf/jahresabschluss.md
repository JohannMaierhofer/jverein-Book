# Jahresabschlüsse

## Liste der Jahresabschlüsse

Zunächst wird eine Liste der bereits getätigten Jahresabschlüsse angezeigt:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_JahresAbschluesseView.png" alt="" /></picture>

Damit ein Jahresabschluss verbucht werden kann, müssen folgende Bedingungen erfüllt sein:

* Für jedes Konto muss ein Jahresanfangsbestand existieren
* Alle Buchungen müssen einer Buchungsart zugeordnet worden sein.
* Die Abschlüsse müssen in chronologischer Reihenfolge erfolgen.

Über das Kontextmenü kann jeweils nur der neuste Jahresabschluss gelöscht werden.

Über den Bearbeiten Button lassen sich die Jahresabschlüsse anzeigen bzw. editieren. Gleiches gilt für eine Doppelklick auf einen Eintrag in der Tabelle.

## Jahresabschluss

Durch eine Klick auf Neu kann ein neuer Jahresabschluss vorgenommen werden:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_JahresabschlussView.png" alt="" /></picture>

Der Jahresabschluss zeigt den Zeitraum des Jahresabschlusses an. Es ist das Geschäftsjahr nach dem letzten Abschluss.

Bei Name sollte der Name desjenigen eingetragen werden, der den Abschluss durchführt.

Das Kontextmenü bietet folgende Einträge:
* Bearbeiten: Bei Auswahl einer Konto Zeile lässt sich das entsprechende Konto editieren
* Buchungen anzeigen: Zeigt bei Auswahl einer Steuer Zeile die enthaltenen Buchungen an

Tipp: Die Checkbox "Anfangsbestände Folgejahr" sollte aktiviert werden. Damit werden die Endstände in der Liste der Anfangsbestände abgespeichert und als Basis für das nächste Geschäftsjahr verwendet. Auch das Anlagenverzeichnis verwendet die Anfangsbestände.

Ist in den [Einstellungen](../administration/einstellungen/anzeige.md) der Ort der Abschreibung auf "Checkbox in Jahresabschluss" konfiguriert, wird hier auch die Checkbox "Erzeuge Abschreibungen" sichtbar. Ist sie gewählt, werden automatisch die AfA Abschreibungen generiert.

**PS: Die AfA Buchungen sind in der angezeigten Tabelle noch nicht enthalten, da sie erst beim Speichern generiert werden.**

Die Felder:

* Rest Verwendungsrückstand aus dem Vorjahr
* Zwanghafte satzungsgemäße Weitergabe von Mitteln

werden nur angezeigt wenn [Mittelverwendung](mittelverwendung.md) aktiviert ist.

