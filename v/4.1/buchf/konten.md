# Konten

## Auflistung der Konten

Bei Auswahl des Konten Eintrags im Navigationsbaum werden alle Konten angezeigt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_KontenListeView.png" alt="" /></picture>

Durch Doppel Klick auf ein Konto werden die Daten der Kontos angezeigt.

Über die Buttons lassen

* Sich neue Offline Konten erstellen oder
* Online Konten aus Hibiscus importieren

Über das Konto Menü lassen sich

* Konten zum Bearbeiten anzeigen
* Ein Anfangsbestand erzeugen
* Das Konto löschen

## Kontenarten

In JVerein werden verschiedene Kontoarten unterstützt:

* Geldkonto

Ab JVerein 2.8.23 wird die Unterstützung von Anlagenkonten erweitert. Anlagenkonten sind unter Administration->Einstellungen->Anzeige zu aktivieren.

* Kontoart Anlagenkonto 
* Anzeige der Anlagenkonten und AfA Buchungen in einem eigenen [Anlagenbuchungen View](anlagenbuchungen.md)
* Erstellung eines [Anlagenverzeichnisses](anlagenverzeichnis.md)
* Unterstützung bei der Generierung von AfA Buchungen

Ab JVerein 3.0.0 gibt es zusätzlich folgende Kontoarten (Rücklagenkonten sind unter Administration->Einstellungen->Anzeige zu aktivieren):

* Fremdkapital (Darlehen, Kredite etc.)
* Zweckgebundene Rücklage nach § 62 Abs. 1 Nr. 1 AO
* Betriebsmittelrücklage nach § 62 Abs. 1 Nr. 1 AO
* Investitionsrücklage nach § 62 Abs. 1 Nr. 1 AO
* Instandhaltungsrücklage nach § 62 Abs. 1 Nr. 1 AO
* Wiederbeschaffungsrücklage nach § 62 Abs. 1 Nr. 2 AO
* Freie Rücklage nach § 62 Abs. 1 Nr. 3 AO
* Rücklage für Gesellschaftsrechte nach § 62 Abs. 1 Nr. 4 AO
* Vermögen nach § 62 Abs. 3 und 4 AO
* Konto für sonstige Rücklagen und Vermögen

Ab JVerein 3.1.0 gibt es zusätzlich folgende Kontoarten (Die Option ist unter Administration->Einstellungen->Anzeige zu aktivieren.:

* Verbindlichkeiten
* Forderungen

Diese Konten dienen nur zur Dokumentation, sie gehen nicht in das Buchungsklassensaldo ein weil in der einfachen Buchführung das Zuflussprinzip gilt, also immer so gebucht wird wie das Geld auf dem Bankkonto bewegt wird.

## Geldkonto und Fremdkapital

Geldkonten können echte Bankkonten, Sparkonten oder offline Konten wie z.B. Barkasse sein.

Fremdkapital sind Darlehen, Kredite etc.

Eine Unterscheidung von Geldkonten und Fremdkapital ist nur nötig wenn das Feature [Mittelverwendung](mittelverwendung.md) benutzt werden soll.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_GeldkontoView.png" alt="" /></picture>

Im Konto View können die Daten der Kontos editiert werden.

Folgende Daten können eingegeben werden:

* Kontoart: Geldkonto oder Fremdkapital
* Nummer
* Bezeichnung
* Eröffnungsdatum
* Auflösungsdatum
* Hibiscus-Konto: Zugeordnetes Konto in Hibiscus bei Online Konten
* Gegenbuchung(GB)-Buchungsart: Hier lässt sich eine Buchungsart einstellen. Falls beim Erzeugen einer Gegenbuchung, die selektierte Buchung, die hier konfigurierte Buchungsart besitzt, wird das Konto automatisch in der Gegenbuchung eingetragen
* Buchungsklasse: Dieses Feld ist für diese Konten nicht relevant
* Kommentar: Optionale Angaben zum Konto

Die weiteren Felder unter Anlagenkonto Daten sind hier nicht relevant.

## Rücklagenkonten

Gemeinnützige Vereine müssen ihre Einnahmen im aktuellen und den zwei folgenden Jahren ausgegeben haben (zeitnahe Verwendung). Dieses müssen sie dem Finanzamt nachweisen, siehe [Mittelverwendung](mittelverwendung.md). Sie dürfen aber Rücklagen bilden. Diese sind der zeitnahen Verwendung entzogen.

Zur Dokumentation der eingestellten Rücklagen wurden die Kontoarten für Rücklagen eingeführt:

* Zweckgebundene Rücklage nach § 62 Abs. 1 Nr. 1 AO
* Betriebsmittelrücklage nach § 62 Abs. 1 Nr. 1 AO
* Investitionsrücklage nach § 62 Abs. 1 Nr. 1 AO
* Instandhaltungsrücklage nach § 62 Abs. 1 Nr. 1AO
* Wiederbeschaffungsrücklage nach § 62 Abs. 1 Nr. 2 AO
* Freie Rücklage nach § 62 Abs. 1 Nr. 3 AO
* Rücklage nach § 62 Abs. 1 Nr. 4 AO
* Vermögen nach § 62 Abs. 3 und 4 AO
* Sonstige Rücklagen

Ein Verein kann für Rücklagen ein separates Bankkonto anlegen um sie dem Finanzamt nachzuweisen. Dafür fallen aber evtl. Kontoführungsgebühren an.

Mit den Kontoarten für Rücklagen ist das nicht notwendig. Auch können hier Rücklagenkonten für verschiedene Zwecke wie zB. freie Rücklage, Rücklage für einen festen Zweck etc. angelegt werden.

Rücklagen Zuführungen werden als normale Einnahme auf ein Rücklagenkonto gebucht. Entnahmen werden als Ausgabe verbucht. Es ist keine Gegenbuchung auf einem Bankkonto nötig.

Buchungen auf Rücklagenkonten werden nicht im Buchungsklassensaldo berücksichtigt. Die Gelder sind ja bereits in Geldkonten vorhanden. Sie werden auch nicht im Kontensaldo berücksichtigt. Sie werden im Kontensaldo View separat aufgelistet.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_KontenSaldoView.png" alt="" /></picture>

Diese Konten dienen nur zur Dokumentation der vorhanden Rücklagen. Sie werden aber bei der [Mittelverwendung](mittelverwendung.md) berücksichtigt.

## Anlagenkonten

Anlagenkonten sind dazu gedacht Abschreibungen durchzuführen und ein Anlagenverzeichnis nach steuerlichen Gesichtspunkten zu erstellen siehe [Anlagenverzeichnis](anlagenverzeichnis.md).

Hierbei wird nach folgenden Anlagen unterschieden:

* Wirtschaftsgüter mit einem Anschaffungswert von unter 250€ (Netto). Diese werden als Ausgabe gebucht und **nicht** als Anlagenkonto geführt
* Geringwertige Wirtschaftsgüter (GWG) mit einem Anschaffungswert von maximal 800€ (Netto). Diese können als Anlagenkonto geführt werden und tauchen dann im Anlagenverzeichnis auf. Sie werden aber sofort ganz abgeschrieben. Alternativ können sie in eine Pool Abschreibung aufgenommen werden
* Pool Abschreibung: Bewegliche Wirtschaftsgüter mit einem Anschaffungswert von maximal 1000€ (Netto) können in einem Anlagenkonto zusammen gefasst werden. Nur der Pool taucht im Anlagenverzeichnis auf. Ein Pool wird über 5 Jahre abgeschrieben und jedes Jahr wird ein neuer Pool erzeugt. Dies hat den Vorteil des geringeren Dokumentation Aufwandes. Es kann jedes Jahr neu entschieden werden ob die Pool Abschreibung oder eine Einzel Abschreibung verwendet wird
* Reguläre Abschreibung: Wirtschaftsgüter mit einem Anschaffungswert über 800/1000€ (Netto) werden regulär abgeschrieben

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_AnlagenkontoView.png" alt="" /></picture>

Im Konto View können die Daten der Anlagenkontos editiert werden.

Folgende allgemeine Daten können eingegeben werden:

* Kontoart: Anlagenkonto PS: Nach Speichern des ersten Anlagenkontos muss JVerein neu gestartet werden. Erst dann sind die Einträge für Anlagenbuchungen und Anlagenverzeichnis im Navigationsbaum sichtbar
* Nummer
* Bezeichnung
* Eröffnungsdatum
* Auflösungsdatum: Die Anlage bleibt solange im Anlagenverzeichnis bis es aufgelöst wird, auch wenn die Abschreibungsdauer bereits abgelaufen ist
* Hibiscus-Konto: Bei Anlagenkonten nicht relevant
* Gegenbuchung(GB)-Buchungsart: Hier lässt sich eine Buchungsart einstellen. Falls beim Erzeugen einer Gegenbuchung, die selektierte Buchung, die hier konfigurierte Buchungsart besitzt, wird das Konto automatisch in der Gegenbuchung eingetragen
* Buchungsklasse: Anlagen müssen im Anlagenverzeichnis nach steuerlichen Sphären gruppiert sein um die Zuordnung zu erkennen. Dies ist auch für die korrekte Erstellung der Mittelverwendungsrechnung notwendig. Wird eine Anlage gemischt in verschiedenen Sphären verwendet muss sie entsprechend der Nutzung aufgeteilt werden
* Kommentar: Optionale Angaben zum Konto z.B. Rechnungsnummer, Verkäufer etc.

Folgende Anlagen spezifische Daten können eingegeben werden:

* Anlagen Buchungsart: Buchungsart der Anlage. Diese ergibt sich aus dem Kontenplan. Auch die Anlagenbuchungen sollten diese Buchungsart haben. Sie muss als Umbuchung gekennzeichnet sein
* AfA Buchungsart: Die Buchungsart die für die zugehörigen Abschreibungen verwendet werden soll z.B. "AfA linear" oder "Keine AfA" für Grundstücke. In der Buchungsart muss der Schalter AfA gesetzt sein
* Anlagenwert: Wert der Anlage
* Anschaffungsdatum: Tag der Anschaffung oder bei Pool Abschreibung der Tag der letzten Anschaffung im Pool
* Nutzungsdauer: Dauer der AfA. Wert Wert ist 0 bei sofortiger Abschreibung und sonst die Dauer der Abschreibung
* Anlagen Restwert: Restwert der Anlage der nach der Abschreibungsdauer übrig bleiben soll z.B. wenn die Anlage auch nach der Abschreibung weiter benutzt werden soll. Der Default Wert kann in den Einstellungen gesetzt werden. In JVerein kann auch eine Anlage mit Restwert 0 im Anlagenverzeichnis geführt werden. Ein Anlagenkonto bleibt solange im Anlagenverzeichnis bis es aufgelöst wird
* AfA Mode: Modus für die Behandlung der Abschreibung (siehe weiter unten)
* Anlagenzweck: Dieses Attribut wird nur angezeigt wenn [Mittelverwendung](mittelverwendung.md) aktiviert wurde. Hier wird konfiguriert, ob die Anlage nutzungsgebunden ist oder zweckfremd verwendet wird

## Einstellungen

Unter Administration->Einstellungen->Buchführung lässt sich

* Der Default Wert für den Anlagen Restwert konfigurieren

Unter Administration->Einstellungen->Anzeige lässt sich folgendes konfigurieren:

* Summen Anlagenkonto im Konten Saldo: Ist dieses ausgewählt wird im Kontensaldo nicht jedes Anlagenkonto einzeln aufgelistet sondern nur ein Eintrag für die Summe über alle Anlagenkonten
* Ort der Abschreibung: Hier lässt sich entscheiden ob die automatische Generierung der Abschreibung über einen Button im Anlagenbuchungen View erfolgen soll oder über eine Checkbox beim Jahresabschluss ausgewählt werden kann. Werden die Abschreibungen über den Button generiert, wird als Buchungsdatum trotzdem der letzte Tag des Geschäftsjahres verwendet da es sich um eine Jahresabschreibung handelt

## Voraussetzungen für Anlagenkonten

Für das korrekte Handling von Anlagenkonten sind folgende Vorarbeiten nötig:

* Optionales Anlegen von Buchungsklassen zur Gruppierung der Anlagenkonten im Anlagenverzeichnis
* Anlegen von Buchungsarten für die Anlagen und Anlagenkonten. Diese müssen als Umbuchung gekennzeichnet sein
* Anlegen von Buchungsarten für die AfA. Diese müssen mit Ausgabe und Abschreibung gekennzeichnet sein

## Workflow für das Anlegen von Anlagenkonten

JVerein unterstützt bei der automatischen AfA Generierung nur lineare Abschreibung. Bei degressiver Abschreibung müssen die Abschreibungen manuell gebucht werden oder die Einstellungen im Anlagenkonto werden jedes Jahr manuell angepasst.

### Geringwertige Wirtschaftsgüter (GWG)

Geringwertige Wirtschaftsgüter können sofort abgeschrieben werden, werden aber in das Anlagenverzeichnis aufgenommen.

Folgende Schritte sollten ausgeführt werden:

* In der Buchungsliste wird der Buchung der Anschaffung eine passende Buchungsart wie oben erzeugt zugewiesen
* Über das Menü der Buchung wird "Neues Anlagenkonto" ausgewählt. Dieses erzeugt ein neues Anlagenkonto, einen Anfangsbestand Eintrag für das Konto (0€) und die entsprechende Gegenbuchung im Anlagenkonto. (Bei Umsatzsteuerpflicht wird nur der Nettobetrag als Gegenguchung erstellt, die Steuer ist direkt als Ausgabe abziehbar und wird im Buchungsklassensaldo ausgeweiesen).
* Es wird der Neues Anlagenkonto Dialog angezeigt. Buchungsklasse und Buchungsart wird mit den Daten der Buchung initialisiert

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_NeuesAnlagenkontoDialog.png" alt="" /></picture>

* Jetzt Nummer, Bezeichnung, Buchungsklasse, Buchungsart und AfA Buchungsart auswählen
* Als Nutzungsdauer den Wert 0 eintragen für sofortige Abschreibung
* Dann mit Übernehmen weiter machen
* Es wird jetzt das neue Anlagenkonto angezeigt
* Hier den Button "Auto Anlagenwert" auswählen. Damit wird das Buchungsdatum in das Anschaffungsdatum übernommen und die Anschaffungskosten mit dem Wert der Buchung gefüllt
* Nutzungsdauer sollte schon auf 0 stehen wenn es im Dialog wie vorher beschreiben gesetzt wurde
* Anlagen Restwert sollte auf 0€ gesetzt werden
* Der AfA Mode kann bei Auto AfA bleiben
* Jetzt das Anlagenkonto Speichern

### Pool Abschreibung

Bei der Pool Abschreibung werden mehrere Anlagen zu einem Anlagenkonto zusammen gefasst.

Bei der ersten Anlage zum Pool wird so vorgegangen:

* In der Buchungsliste wird der ersten Buchung des Pools eine passende Buchungsart wie oben erzeugt zugewiesen
* Über das Menü der Buchung wird "Neues Anlagenkonto" ausgewählt. Dieses erzeugt ein neues Anlagenkonto, einen Anfangsbestand Eintrag für das Konto (0€) und die entsprechende Gegenbuchung im Anlagenkonto. (Bei Umsatzsteuerpflicht wird nur der Nettobetrag als Gegenguchung erstellt, die Steuer ist direkt als Ausgabe abziehbar und wird im Buchungsklassensaldo ausgeweiesen).
* Es wird der Neues Anlagenkonto Dialog angezeigt. Buchungsklasse und Buchungsart wird mit den Daten der Buchung initialisiert
* Jetzt Nummer, Bezeichnung z.B. Abschreibung Pool 2024, Buchungsklasse, Buchungsart und AfA Buchungsart auswählen
* Als Nutzungsdauer den Wert 5 eintragen (Pools werden mit einer Dauer von 5 Jahren abgeschrieben)
* Dann mit Übernehmen weiter machen
* Es wird jetzt das neue Anlagenkonto angezeigt
* Hier den Button "Auto Anlagenwert" noch **nicht** auswählen
* Nutzungsdauer sollte schon auf 5 stehen wenn es im Dialog wie vorher beschreiben gesetzt wurde
* Anlagen Restwert sollte auf 0€ gesetzt werden da der Pool ganz abgeschrieben wird
* Jetzt das Anlagenkonto Speichern

Bei allen weiteren Anlagen für den Pool wird so vorgegangen:

* In der Buchungsliste wird der Anlagen Buchung des Pools eine passende Buchungsart wie oben erzeugt zugewiesen
* Über das Menü der Buchung wird "Gegenbuchung" ausgewählt
* Im Konto Auswahl Dialog das Pool Anlagenkonto auswählen und übernehmen
* Es wird die Gegenbuchung angezeigt
* Die Gegenbuchung mit Speichern speichern

Aktion nach Erzeugen der letzten Buchung für den Pool:

* Das Pool Anlagenkonto öffnen
* Hier den Button "Auto Anlagenwert" auswählen. Damit wird das Buchungsdatum der letzten Buchung in das Anschaffungsdatum übernommen und die Anschaffungskosten mit dem Summenwert aller Buchungen im Anlagenkonto gefüllt
* Der AfA Mode sollte nach persönlichen Vorlieben gewählt werden (siehe Abschreibungen Buchen unten)
* Jetzt das Anlagenkonto Speichern

### Reguläre Abschreibung

Handling eines einzelnen Wirtschaftsgut:

* Hier kann wie bei einem geringwertigen Wirtschaftsgut vorgegangen werden mit kleinen Abweichungen
* Es ist die korrekte Nutzungsdauer die sich aus den Vorgaben der Finanzverwaltung ergibt einzutragen
* Der Restwert kann beliebig gesetzt werden
* Der AfA Mode sollte nach persönlichen Vorlieben gewählt werden (siehe Abschreibungen Buchen unten)

Handling von Wirtschaftsgütern mit mehreren Ausgaben wie z.B. Hauskauf. Hier gehören alle Kosten im Zusammenhang der Erstehung des Hauses zu den Anschaffungskosten. Die Vorgehensweise ist wie folgt:

* Hier kann wie bei einer Pool Abschreibung vorgegangen werden mit kleinen Abweichungen
* Es ist die korrekte Nutzungsdauer die sich aus den Vorgaben der Finanzverwaltung ergibt einzutragen
* Der Restwert kann beliebig gesetzt werden
* Der AfA Mode sollte nach persönlichen Vorlieben gewählt werden (siehe Abschreibungen Buchen unten)

PS: Es kann sein, dass die erste Buchung auf dem Anlagenkonto in einem anderen Jahr statt fand als die letzte Buchung. Hier beginnt die Abschreibung auch erst mit dem Datum der letzten Buchung! Im Vorjahr gibt es keine AfA Buchungen, sondern nur Zugang.

### Anlagenkonten für bereits laufende Abschreibung

Es kann sein, dass man neu in JVerein einsteigt und bereits Anlagen besitzt die man in das Anlagenverzeichnis aufnehmen möchte. In diesem Fall sind bereits Abschreibungen getätigt und auch die Anschaffung liegt in der Zeit vor dem Datum mit dem man in JVerein beginnt.

In diesem Fall bietet sich folgendes Vorgehen an:

* Erstellen eines Anlagenkontos über den Neu Button in der Konto Liste
* Die Kontodaten mit den Daten der Anlage ausfüllen. Also hier mit dem echten Datum der Anschaffung und dem echten damaligen Anlagenwert allerdings als Konto Eröffnungsdatum den ersten Tag des Geschäftsjahres
* Unter [Anfangsbestände](anfangsbestand.md) einen Eintrag für den ersten Tag des aktuellen Geschäftsjahres erstellen und dort den aktuellen Buchungswert der Anlage eintragen
* Bei der automatischen Berechnung der AfA Beträge wird dann mit diesem Anfangsbestand gerechnet. Im regulären Verfahren wie oben beschrieben muss der Anfangsbestand 0€ sein. Dieser wird dort automatisch erzeugt

## Workflow für die Buchung der AfA

Für das Erstellen der AfA Buchungen auf den Anlagenkonten gibt es drei Möglichkeiten die über den AfA Mode im Anlagenkonto konfiguriert werden.

* Manuelle AfA: Die AfA Buchungen werden manuell von Benutzer als reguläre Buchung mit einer AfA Buchungsart im Anlagenkonto erzeugt
* Angepasste AfA: In diesem Fall kann man die Abschreibungswerte manuell anpassen. Hier sollten aber die steuerlichen Vorschriften beachtet werden. Ist diese Option ausgewählt kann man über den "Auto-AfA" Button die Abschreibungen automatisch berechnen lassen. Diese werden dann wenn nötig anteilig für das erste Jahr und für die Folgejahre berechnet und in die Felder eingetragen. Die Werte können manuell geändert werden. Für das letzte anteilige Jahr wird der Abschreibungsbetrag anhand des letzten Kontostandes und des verbleibenden Restwertes automatisch berechnet.\
  Da JVerein nur lineare Abschreibung unterstützt könnte man hier auch Werte entsprechend der degressiven Abschreibung eingeben. Für die Folgejahre müsste der Wert aber dann jedes Jahr angepasst werden.
* Auto AfA: Die Abschreibungswerte werden automatisch an Hand des aktuellen Kontostandes auf die Restlaufzeit verteilt.

PS: Bei Angepasste und Auto AfA werden die Jahresabschreibungen automatisch generiert. Es ist aber weiter möglich zusätzlich auch Sonderabschreibungen manuell zu erzeugen.

Bei angepasste und Auto AfA können die AfA Buchungen mit zwei Alternativen generiert werden. Die jeweilige Option wird unter Administration->Einstellungen->Anzeige konfiguriert.

* Button im Anlagenbuchungen View: Durch betätigen des Buttons werden die Abschreibung Buchungen entsprechend dem Setting im Anlagenkonto erzeugt. Das Buchungsdatum ist der letzte Tag des Geschäftsjahres. Der Button sollte natürlich nur einmal im Jahr gedrückt werden. Es muss allerdings eben nicht am letzten Tag des Geschäftsjahres passieren.\
  Diese Option hat den Vorteil, dass man das Kontensaldo bereits mit den Abschreibungen vor dem Jahresabschluss sehen kann
* Checkbox im Jahresabschluss View: Wird die Option im Jahresabschluss View aktiviert werden die Abschreibung Buchungen beim Erstellen des Jahresabschlusses erzeugt. Sie sind also auch vorher nicht im Buchungsklassen Saldo sichtbar

### Berechnung der AfA

Die AfA wird in JVerein folgendermaßen berechnet:

* AfA Folgejahre = (Anschaffungswert - Anlagen Restwert) / Nutzungsdauer
* AfA Erstes Jahr = AfA Folgejahre \* Monate bis Geschäftsjahres Ende / 12

Bei Auto AfA werden zusätzlich noch:

* Die AfA Beträge zu vollen Beträgen aufgerundet
* Der AfA Erstes Jahr nach dem aufrunden um die Nachkommastellen des Anschaffungswertes ergänzt. Dadurch ergibt sich nach dem ersten Jahr ein runder Betrag.

### Unterschied zwischen Angepasste AfA und Auto AfA

Werden bei der Angepasste AfA die eingetragenen Werte über den Auto-AfA Button generiert sollte es im Normalfall zu keinem Unterschied bei den berechneten AfA Beträgen kommen.

Folgende Unterschiede kann es geben:

* Da Auto AfA jedes Jahr den Abschreibungsbetrag anhand der bisher getätigten Abschreibungen und der Restlaufzeit neu berechnet kann es zu Abweichungen von 1€ wegen der Rundung kommen. Bei Angepasste AfA wird immer der fest vorgegebene Wert verwendet
* Auto AfA berücksichtigt auch manuell eingegebene Sonderabschreibungen und reduziert dann automatisch die restlichen Jahresabschreibungen. Bei Angepasste AfA bleibt der Abschreibungsbetrag bei getätigten Sonderabschreibungen gleich. Es wird der Wert aus dem Anlagenkonto genommen.\
  Es hängt hier vom Anwendungsfall ab ob eine Reduktion erlaubt ist oder nicht. Bei Sonderabschreibungen kann man aber auch den AfA-Mode im Konto entsprechend anpassen auf das Verfahren welches man aktuell braucht
