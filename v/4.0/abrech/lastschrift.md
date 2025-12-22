# Lastschriften

Lastschriften werden bei einem Abrechnungslauf für Mitglieder oder Nicht-Mitglieder generiert bei denen als Zahlungsweg "Basislastschrift" ausgewählt ist und auch für Kursteilnehmer.

Entsprechend der Abbuchungsausgabe wurden diese entweder an Hibiscus übergeben oder in einer XML Datei exportiert. Siehe [Abrechnung](abrechnung.md).

## Liste der Lastschriften

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_LastschriftenListeView.png" alt="" /></picture>

Die Lastschriften lassen sich in dem View nach verschiedenen Kriterien filtern. Mit dem Filter Mitgliedschaft lässt sich nach Mitglieder, Nicht-Mitglieder oder Kursteilnehmer filtern.

Die Lastschrifteinträge werden für die Generierung der Pre-Notificationen verwendet. Siehe [Pre-Notification](../druckmail/pre-notification.md).

Mit einem Rechtsklick auf einen oder mehrere selektierte Tabelleneinträge öffnet sich ein Menü mit folgenden Einträgen:

* Bearbeiten: Zeigt die Lastschrift an
* Versanddatum setzen: Setzen bzw. Löschen des Versanddatum
* Pre-Notification: Zeigt den Dialog zur Generierung von Pre-Notifications an
* Löschen: Damit können alte Einträge wenn sie aus Dokumentationszwecken nicht mehr gebraucht werden gelöscht werden
* Mitglied anzeigen: Zeigt die Mitglieder Daten an

Lastschrift Einträge werden automatisch gelöscht wenn man den zugehörigen Abrechnungslauf löscht.

**Achtung:**

Solange für Einträge die Pre-Notificationen noch nicht versendet wurden dürfen diese Einträge nicht gelöscht werden. Für gelöschte Einträge können keine Pre-Notificationen verschickt werden.

Auch sollten Lastschriften der letzten 3 Jahre nicht gelöscht werden, da für die Berechnung ob ein gültiges Mandat vorliegt geprüft wird ob in den letzten 3 Jahren eine Lastschrift erfolgt ist. Gibt es keine Lastschrift und das Mandat ist älter, ist ein neues Mandat nötig.

## Lastschrift

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_LastschriftView.png" alt="" /></picture>
