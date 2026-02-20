# Mitgliedschaft

Beitragsgruppe ist ein Pflichtfeld. Die Beitragsgruppen können unter [Beitragsgruppen](../../administration/mitglieder/beitragsgruppen.md) für jeden Verein individuell konfiguriert werden. Siehe auch [Beitragsmodelle](../../../../allgemein/beitragsmodelle.md). Beim Austrittsdatum wird das Datum des satzungsgemäßen Austritts (z. B. der 31.12. des jeweiligen Jahres) eingetragen. Unter Kündigung wird das Datum des Eingangs der Kündigung vermerkt.

Standardaussehen des Formulars:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MitgliedschaftTab.png" alt="" /></picture>

In Administration->Einstellungen->Anzeige lässt sich einstellen, ob Eintrittsdatum ein Pflichfeld ist.

## Sekundäre Beitragsgruppen

Für ein Mitglied können auch Beiträge aus mehreren Beitragsgruppen abgerechnet werden. Dazu muss unter Administration->Einstellungen->Anzeige das Häkchen bei "Sekundäre Beitragsgruppen anzeigen" gesetzt werden und unter Administration->Beitragsgruppen muss für mindestens eine Beitragsgruppe das Häkchen "Sekundäre Beitragsgruppe" gesetzt werden. Dann kann beim Mitglied eine entsprechende Auswahl vorgenommen werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_SekundaereBeitragsGruppen.png" alt="" /></picture>

## Familienverband

Ein Mitglied kann einem Familienverband zugeordnet werden. Dazu muss unter Administration->Einstellungen->Anzeige das Häkchen bei "Familienbeitrag" gesetzt werden

Sofern eine Beitragsgruppe ausgewählt wurde, die mit "Familienangehöriger" gekennzeichnet ist, wird folgendes Formular angezeigt.

Die Person (ebenfalls ein Mitglied), die im Familienverband den vollen Beitrag zahlt, kann im Tab "Vollzahlendes Familienmitglied" aus einer Liste ausgewählt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_VollZahler.png" alt="" /></picture>

Im Tab "Familienmitglieder" werden die Personen angezeigt, die am Familienverband beteiligt sind.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_FamilienVerband.png" alt="" /></picture>

Sinn und Zweck dieser Familienverknüpfung ist es, die Voraussetzungen für die Familienmitgliedschaft prüfen zu können. Tritt ein Mitglied aus, dass für andere Mitglieder als Vollzahlendes Familienmitglied eingetragen ist, kommt eine entsprechende Fehlermeldung.

Dann sind die Beitragsgruppen der Familienmitglieder zu verändern oder es ist ein anderes Vollzahlendes Familienmitglied einzutragen.

Siehe auch: [Familientarife](../../../../allgemein/familientarife.md)

## Zukünftige Beitragsgruppen

Für ein Mitglied können zukünftige Beitragsgruppen eingerichtet werden. Dazu muss unter Administration->Einstellungen->Anzeige das Häkchen bei "Zukünftige Beitragsgruppen anzeigen" gesetzt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_ZukuenftigeBeitragsGruppen.png" alt="" /></picture>

Hier kann man Beitragsgruppen eintragen, die für dieses Mitglied ab einem definierten Datum gültig sein soll. Hat man z.B. im ersten Jahr einen vergünstigten Probebeitrag, trägt man diesen oben unter Beitragsgruppe ein. Die Beitragsgruppe für den normalen Beitrag, der gültig werden soll, sobald die Probezeit beendet ist, kann man sofort in dieser Tabelle zukünftige Beitragsgruppen eintragen.

Über den Button "Beitragsgruppe hinzufügen" lässt sich ein neuer Eintag erzeugen.

Über das Kontextmenü lässt sich ein bestehender Eintrag löschen.

Bei Programmstart wird geprüft, ob das Datum für eine Änderung der Beitragsgruppe erreicht wurde. Alle zu ändernden Mitglieder werden in einer Liste angezeigt und es können die neuen Beitragsgruppen für ausgewählte Mitglieder oder alle angezeigten übernommen werden. Damit die Daten angezeigt werden, ist einmal die Box "künftige Beitragsgruppen" zu aktivieren:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Boxactivate.png" alt="" /></picture>

Hinweis: Die Box ist nur sichtbar, wenn im Menü "Start" ausgewählt wurde.

Zum Erfassen einer zukünftigen Beitragsgruppe klicken Sie mit der rechten Maustaste in die Tabelle. Im Kontextmenü wählen Sie den Punkt Beitragsgruppe hinzufügen. Es öffnet sich eine Ansicht, in der Sie die neue Beitragsgruppe auswählen und das Datum erfassen, ab dem diese Gruppe gültig werden soll. Sie können in einem Bemerkungsfeld noch hinterlegen, warum diese Änderung durchgeführt werden sollte.

Bei Mitgliedern von Beitragsgruppen der Beitragsart Normal können Sie nur andere Beitragsgruppen mit der Beitragsart Normal als zukünftige Beitragsgruppe eintragen.

Bei Mitgliedern von Beitragsgruppen der Beitragsart Familienangehöriger können Sie keine zukünftigen Beitragsgruppen hinterlegen, weil hier u.U. Zahlungsdaten fehlen.
