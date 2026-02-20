# Buchungsarten

## Allgemeines

Über Buchungsarten kann festgelegt werden, für welche Zwecke Geld eingenommen oder ausgegeben wurde.

## Liste der Buchungsarten

Eine Liste der Buchungsarten kann über den Eintrag Buchungsarten im Navigationsbaum angezeigt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_BuchungsartenListeView.png" alt="" /></picture>

Über den Neu Button können neue Buchungsarten erzeugt werden.

Über das Kontextmenü können bestehende Buchungsarten bearbeitet und gelöscht werden.

Mit einem Klick auf PDF-Ausgabe wird eine Buchungsarten-Liste erstellt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Buchungsartenpdf.png" alt="" /></picture>

## Buchungsart

Mit Neu kann eine neue Buchungsart eingerichtet werden. Jeder Buchungsart wird eine Nummer zugeordnet. Diese Nummer dient der Sortierung in der Buchungsliste. Z. B. werden den Einnahmen die 1.000er Nummern, den Ausgaben die 2.000er und den Umbuchungen die 3.000er gegeben.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_buchungsarten.png" alt="" /></picture>

Eine Buchungsart hat folgende Parameter:

* Nummer
* Bezeichnung
* Art: Für jede Buchungsart wird die Art "Einnahme", "Ausgabe" oder "Umbuchung" ausgewählt
* Buchungsklasse: Buchungsklassen dienen zu Gruppierung von Buchungsarten. Es hängt vom gewählten Kontenrahmen ab wie dieser Wert benutzt wird (siehe unten)
* Spende: Bei einer Ausgabe für die Spendenbescheinigungen erstellt werden sollen ist dieser Schalter zu aktivieren
* Abschreibung: Falls Abschreibungen gebucht werden sollen und diese Buchungsart für eine Abschreibung benutzt werden soll ist dieser Schalter zu aktivieren
* Steuer: Für Umsatzsteuer pflichtige Vereine kann hier die Steuer ausgewählt werden
* Status: Aktiv bedeutet, dass der Eintrag in Auswahlmenüs zur Eingabe der Buchungsart angezeigt wird. Deaktiviert bedeutet, das die Buchungsart nicht mehr angeboten wird. Das kann Sinn machen wenn man die Buchungsart nicht mehr braucht aber noch alte Buchungen existieren denen sie zugeordnet sind. Bei Auto wird eine Buchungsklasse automatisch ausgeblendet wenn sie mehrere Monate nicht mehr verwendet wurde. Die Anzahl der Monate lässt sich unter Administration->Einstellungen->[Buchführung](../einstellungen/buchfuehrung.md) konfigurieren.
* Suchbegriff: Hier kann ein Suchbegriff (oder Komma getrennte Liste von Suchbegriffen) angegeben werden anhand der die aus Hibiscus importierten Buchungen automatisch dieser Buchungsart zugeordnet werden.
* Suchbegriff ist regulärer Ausdruck: wenn aktiviert, wird der Suchbegriff als regulärer Ausdruck ausgewertet.

## Kontenrahmen

Anstelle des Begriffs "Buchungsarten" wird im Kontext der Buchhaltung oft von "Konto" gesprochen, ein Kontenrahmen listet dann alle möglichen Buchungsarten/Konten auf.

Ein Verein ist aber nicht verpflichtet eine Standard Kontenrahmen zu verwenden.

Insbesondere für gemeinnützige Vereine war hier der Standard Kontenrahmen SKR 49 interessant, der im Forum als Vorlage zur Verfügung steht.

Ab 2025 gilt für Vereine der neue Standard Kontenrahmen SKR 42. Ein Verein ist aber nicht verpflichtet auf diesen umzusteigen. Dies ist evtl. nötig wenn man mit einem Steuerberater zusammen arbeitet der den neuen Kontenrahmen verwenden muss.

Startet man neu mit JVerein empfiehlt es sich dann gleich den neuen SKR 42 zu verwenden falls man einen Standard Kontenrahmen verwenden will.

## Unterstützung des SKR 42

Beim SKR 49 waren den Buchungsarten die Buchungsklassen fest zugeordnet. Dies war auch so in JVerein implementiert. Über die Auswahl der Buchungsklasse in der Buchungsart erfolgt die Zuordnung. Buchungen im Buchungsklassensaldo werden entsprechend gruppiert.

Beim SKR 42 ist die feste Zuordnung zwischen Buchungsart und Buchungsklasse nicht gegeben. Das soll doppelte Buchungsarten vermeiden, weil eine Buchungsart dann bei mehreren Buchungsklassen verwendet werden kann. Das führt allerdings dazu, dass bei einer Buchung neben der Buchungsart auch die Buchungsklasse gesetzt werden muss, was zu einem etwas höheren Aufwand führen kann.

In JVerein gibt es ab 2.8.23 die Möglichkeit die feste Zuordnung zwischen Buchungsart und Buchungsklasse aufzuheben. Hierzu gibt es einen neuen Schalter in Administration->Einstellungen->[Buchführung](../einstellungen/buchfuehrung.md).

Ist dieser Schalter nicht selektiert ist das Verhalten von JVerein so wie bisher. Wird der Schalter aktiviert ist die feste Zuordnung aufgehoben. Jetzt erscheint in den Buchungen neben der Buchungsart auch die Buchungsklasse. Das gleiche gilt für alle Dialoge bei denen bisher nur die Buchungsart eingegeben wurde. Hier muss auch immer die Buchungsklasse zusätzlich eingegeben werden.

Um den Konfigurationsaufwand zu minimieren kann man weiterhin eine Buchungsklasse bei der Buchungsart setzen. Dieses ist aber keine feste Zuordnung. Die Buchungsklasse wird nur als Defaultwert verwendet.

Gibt es einen Dialog in dem man Buchungsklasse und Buchungsart eingeben muss, dann sollte man als erstes die Buchungsart auswählen. Die Buchungsklasse wird dann automatisch mit dem konfigurierten Defaultwert der Buchungsart gefüllt. Das passiert aber nur solange in der Buchungsklasse noch kein Wert steht. Ein späteres Ändern der Buchungsart führt nicht zu einem Überschreiben der gesetzten Buchungsklasse.

Durch dieses Vorgehen gibt es keinen erhöhten Aufwand bei der Konfiguration solange der Defaultwert der richtige ist. Ist ein anderer Wert nötig muss die Buchungsklasse natürlich angepasst werde. Dies passiert aber nur bei Buchungsarten die in mehreren Buchungsklassen verwendet wird.

## Hinweis Aufhebung der festen Zuordnung

Wird die feste Zuordnung von Buchungsart zu Buchungsklasse aufgehoben ändert sich die Art wie die Einträge im Buchungsklassensaldo angezeigt werden.

Nun wird die Zuordnung aus der Buchung ausgelesen und diese entsprechend zugeordnet.

Lässt man sich nach dem Umschalten das Buchungsklassensaldo für frühere Jahre anzeigen so werden alle Buchungsarten unter nicht zugeordnet angezeigt, weil in den Buchungen keine Buchungsklassen gesetzt sind.

Dieses ist aber nur ein Problem der Anzeige. Möchte man ein altes Buchungsklassensaldo erneut mit der alten Sortierung anschauen und z.B. drucken, muss man dafür kurzzeitig die feste Zuordnung wieder einschalten. Solange man dann nicht neu konfiguriert ist das kein Problem. Nach Erstellen des Saldo Reports kann dann wieder zurück schalten.

Wegen dem unterschiedlichen Handling muss ein Wechsel der Kontenrahmen Art bzw. das Auflösen der festen Zuordnung an einem Wechsel des Geschäftsjahres passieren. Damit kann man das alte Geschäftsjahr abschließen und dann das neue mit dem neuen Kontenrahmen starten.

Alte Buchungsarten die dann nicht mehr benutzt werden kann man deaktivieren.
