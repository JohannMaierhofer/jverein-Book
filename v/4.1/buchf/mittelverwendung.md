# Mittelverwendung

### **Achtung!**

**Bei diesem Feature handelt es sich um ein experimentelles Feature.**

Das JVerein Team hat dieses Feature aus Informationen aus dem Internet entwickelt aber selbst bisher keine Erfahrung mit der Mittelverwendung Berechnung.

Wir bitten darum die Anwender welche bereits Mittelverwendungsreports erstellt haben zu prüfen, ob die Art der Berechnung, die ausgegeben Werte und die Darstellung den Anforderungen entsprechen.

Wir würden uns über ein Feedback der Anwender freuen, um es als ausgereiftes Feature anbieten zu können.

### Aktivierung

Zur Nutzung der Mittelverwendung ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

Anschließend sollte JVerein neu gestartet werden, damit der Menüpunkt "Mittelverwendung" zur Verfügung steht.

### Allgemeines

Gemeinnützige Vereine müssen ihre Einnahmen (Finanzen und Sachen) im aktuellen und den zwei folgenden Jahren verwenden (zeitnahe Verwendung). Dieses müssen sie dem Finanzamt nachweisen. Sie dürfen aber Rücklagen und Vermögen bilden. Diese sind der zeitnahen Verwendung entzogen.

**Ausnahme**

Das Jahressteuergesetz 2020 für kleine und mittlere Vereine hat eine Erleichterung gebracht. Vereine, die mit ihren Bruttoeinnahmen unter 45.000 Euro pro Jahr bleiben, sind nicht mehr an die zeitnahe Mittelverwendung gebunden. Der § 55 Absatz 1 Nummer 5 der Abgabenordnung (AO) wurde dazu durch das Jahressteuergesetz (JStG) entsprechend ergänzt.

Es gibt keine feste Vorgabe wie ein Mittelverwendung Nachweis auszuschauen hat. JVerein bietet zwei verschiedene Reports an:

* Zufluss-basiert: Dieser Report listet den Verwendungsrückstand/-überhang und den Mittel Zufluss und Abfluss eines Geschäftsjahres. Dies ist ein fortgeschriebener Report, da er zugeflossene Mittel über zwei Jahre verfolgt. In diesem Zeitraum sind zugeflossene Mittel auszugeben
* Saldo-Basiert: Dieser Report berechnet den Verwendungsrückstand/-überhang anhand der Kontensalden. Dies geschieht in Anlehnung an das Muster von Buchna. (Johannes Buchna (verst. 2013) war in der Oberfinanzdirektion Nordrhein-Westfalen tätig und war seit 1988 (Mit-)Autor des Werks „Gemeinnützigkeit im Steuerrecht“, in dem die Vorlage für eine Mittelverwendungsrechnung veröffentlich ist.)

Der Mittelverwendung lässt sich über den entsprechenden Menüeintrag in der Navigation öffnen.

### Mittelverwendungsreport (Zufluss-basiert)

Dieser Report listet folgende Informationen auf:

* Verwendungsrückstand/-überhang am Ende des letzten Geschäftsjahres: Dies ist der Bestand der Geldkonten und zweckfremden Anlagenkonten abzüglich des Bestandes der Rücklagen und des Vermögens
* Ein in Position 1 enthaltener Rest des Verwendungsrückstand aus dem vorletzten Geschäftsjahr
* Eine in Position 1 enthaltene zwanghafte satzungsgemäße Weitergabe von Mitteln
* Insgesamt im aktuellen Geschäftsjahr zugeflossene Mittel
* Zu verwendende Mittel. Dies ist die Summe der beiden Positionen 1 und 4. Diese Summe muss im aktuellen und folgenden Geschäftsjahr ausgegeben werden
* Im aktuellen Geschäftsjahr verwendete Mittel
* Zugeführte Rücklagen (nach Rücklagenart getrennt) als Mittelabfluss
* Entnommene Rücklagen (nach Rücklagenart getrennt) als Mittelzufluss
* Verwendungsrückstand/-überhang zum aktuellen Zeitpunkt. Für das Finanzamt ist dieser Report zum Ende des aktuellen Geschäftsjahres zu erstellen
* Ein in der letzten Position enthaltener nicht verbrauchter Verwendungsrückstand aus dem letzten Geschäftsjahr
* Eine in der letzten Position enthaltene zwanghafte satzungsgemäße Weitergabe von Mitteln aus dem aktuellen Geschäftsjahr

PS: Die Endsummen werden aus den getätigten Buchungen berechnet. Sie sollten mit den Anfangsbeständen der Konten des nächsten Geschäftsjahres überein stimmen. Ist das nicht der Fall, dann sind einige Buchungen nicht richtig verbucht worden z.B. wegen fehlender Buchungsart.

Ist in Administration->Einstellungen->Buchführung die Checkbox "Listen: Buchungsarten ohne Buchung unterdrücken" ausgewählt werden Rücklagenarten ohne Buchungen im Report nicht angezeigt.

Die Zeilen in der Mittelverwendung sind nummeriert damit man bei einem evtl. Begleitschreiben an das Finanzamt auf die Zeilen Bezug nehmen kann.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MittelverwendungFlowReportView.png" alt="" /></picture>

Der Report kann über die Buttons CSV und PDF ausgegeben werden.

Da es sich bei dieser Art der Berechnung um eine fortlaufende Berechnung handelt müssen die beiden letzten Positionen in der Liste persistent gespeichert werden. Dazu werden sie beim Jahresabschluss berechnet und gespeichert.

Da JVerein 3.0.0 neu mit dem Feature beginnt muss der Startwert dieser Daten eingegeben werden. Evtl. möchte man das auch nachträglich für frühere Jahre machen. Ist aber Mittelverwendung aktiv und es sind die Werte in der Datenbank nicht gesetzt, dann kann man die beiden Werte eingeben und auch speichern.

Über den Button "Startwerte setzen" öffnet sich der Dialog zur Eingabe der Startwerte für das angezeigte Geschäftsjahr.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MittelverwendungDialog.png" alt="" /></picture>

In diesen Dialog sind folgende Daten einzugeben:

* Der Rest des Verwendungsrückstand aus dem vorletzten Geschäftsjahr der in das aktuelle Geschäftsjahr übertragen wird
* Der Betrag der zwanghaft satzungsgemäßen Weitergabe von Mittel die im letzten Geschäftsjahr entstanden sind
* Name des Bearbeiters

Startet man ganz neu mit JVerein und möchte bereits im ersten verbuchten Geschäftsjahr die Mittelverwendungsrechnung benutzen, dann müssen die Startwerte für dieses Jahr eingegeben werden. JVerein erzeugt dann einen Jahresabschluss für das Vorjahr in dem diese Werte eingetragen und gespeichert sind.

Hat man bereits JVerein benutzt und bereits Jahresabschlüsse ohne dieses Feature erstellt, kann man die Startwerte für frühere Jahre nachtragen. Will man z.B. 2020 starten, dann wählt man das Geschäftsjahr 2020 und gibt die Startwerte ein. Anschließend geht man zum nächsten Jahr 2021 und öffnet erneut den Dialog zur Eingabe der Startwerte. Da jetzt für das vorangegangene Jahr Startwerte existieren berechnet JVerein die Startwerte aus den Buchungen des letzten Jahres und zeigt diese an. Man muss sie jetzt also nur noch abspeichern. Das gleiche dann für die Folgejahre.

Der Name brauch nur eingegeben zu werden, wenn das Feld leer ist. in diesem Fall wird ein neuer Jahresabschluss erzeugt. In den Fällen, dass nur die Werte in bestehenden Jahresabschlüssen nachgetragen wird, wird bereits im Dialog der Name aus dem betroffenen Jahresabschluss gelesen und angezeigt. Diese wird auch wenn man den Namen ändert nicht überschrieben.

### Mittelverwendungsreport (Saldo-basiert)

Dieser Report berechnet den Verwendungsrückstand/-überhang auf eine andere Art. Das Ergebnis sollte aber das gleiche sein.

In diesem Report wird erst alles vorhandene Vermögen, also Anlagen, Geldkonten und Fremdkapital aufgelistet und das Gesamtvermögen bestimmt.

Davon abgezogen werden vorhandenes nutzungsgebundenes Anlagenvermögen und Fremdkapital.

Dann erfolgt die Verrechnung der Zu- und Abgänge bei Rücklagen und Vermögen. Dieses ist nach der Buchungsklasse der Rücklagen- und Vermögenskonten gegliedert. Hierzu ist diesen Konten eine Buchungsklasse zuzuweisen.

Nach Abzug der verwendeten Mittel vom Gesamtvermögen ergibt sich der neue Verwendungsrückstand/-überhang.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_MittelverwendungSaldoReportView.png" alt="" /></picture>

Ist in Administration->Einstellungen->Buchführung die Checkbox "Listen: Buchungsarten ohne Buchung unterdrücken" ausgewählt werden Rücklagenarten ohne Saldo im Report nicht angezeigt.

Ist in Administration->Einstellungen->Anzeige die Checkbox "Summen Anlagenkonto in Kontosaldo" ausgewählt werden die einzelnen Anlagenkonten nicht aufgelistet, sondern nur die Gesamtsumme über alle Anlagenkonten.

Dieser Report enthält eine Spalte Kommentar. Hier wird die erste Zeile aus dem Kommentarfeld des Kontos ausgegeben. Damit kann man steuerrelevante Information ausgeben. Z.B. kann man ausgeben ob die Anlage nutzungsgebunden ist oder zweckfremd eingesetzt wird.

Der Report kann über die Buttons CSV und PDF ausgegeben werden.

### Annahmen

Für eine korrekte Berechnung der Daten der Reports sind folgende Annahmen getroffen:

* Alle Konten auf denen vorhandene Mittel (Geld) verwaltet ist, ist die Kontoart Geldkonto zugewiesen
* Konten für Schulden wie z.B. Darlehen, Kredite etc. sind als Fremdkapital gekennzeichnet
* Anlagenkonten ist der korrekte Anlagenzweck zugeordnet (entweder als nutzungsgebundene Anlage oder zweckfremde Anlage)
* Rücklagen sind auf Rücklagenkonten verbucht
* Buchungen muss die korrekte Buchungsart mit korrekter Klassifikation als Einnahme, Ausgabe oder Umbuchung zugewiesen sein

Einnahmen und Ausgaben werden wie folgt berechnet:

* Zu den Einnahmen zählen alle Buchungen der Art Einnahme die auf Geldkonten oder zweckfremden Anlagenkonten (Sachspenden) eingehen
* Zu den Ausgaben zählen alle Buchungen der Art Ausgabe die von Geldkonten oder zweckfremden Anlagen abgehen
* Umbuchungen innerhalb Geldkonten, innerhalb zweckfremden Anlagen und zwischen beiden gelten als Umschichtung und sind damit keine Mittelzuflüsse und Abflüsse
* Umbuchungen zu Fremdkapital Konten (Darlehensauszahlung, Tilgung) und nutzungsgebundenen Anlagenkonten (Anschaffung einer Anlage) werden berücksichtigt. Dazu werden positive Umbuchungen auf diesen Konten als Mittelabfluss und negative Umbuchungen als Mittelzufluss betrachtet. Es wird davon ausgegangen, dass alle Umbuchungen auf diesen Konten von Geldkonten kommen
* Es darf also keine Umbuchungen innerhalb Fremdkapital Konten und nutzungsgebundenen Anlagenkonten geben

Hinweise:

Bei einem Abrechnungslauf werden bei Lastschriften einzelne Buchungen generiert und eine Gegenbuchung. Später wird der Betrag der Gegenbuchung per Lastschrift eingezogen.

Es ist darauf zu achten, dass die Gegenbuchung die Buchungsart Einnahme hat. Hätte sie die Art Ausgabe, wären die Angaben zu den Ausgaben im Report falsch. Dann wären auch die Einnahmen doppelt, wegen der Buchungen und eingegangenen Lastschrift. Die Summe würde zwar stimmen aber nicht die Angaben zu den Einnahmen und Ausgaben.

## Buchungsbeispiele

### Aufnahme von Darlehen, Kredite etc.

Die Aufnahme eines Darlehens oder Kredit wird als Mittelzufluss betrachtet. Diese Gelder unterliegen der zeitnahen Mittelverwendung. Sie sind wie folgt zu buchen:

* Auf dem Geldkonto (Kontoart Geldkonto) wird die Darlehenssumme (positiv) mit einer Buchungsart "Umbuchung" gebucht
* Auf dem Darlehenskonto (Kontoart Fremdkapital) wird die Darlehenssumme (negativ) mit einer Buchungsart "Umbuchung" gebucht

### Tilgung von Darlehen, Kredite etc.

Die Tilgung eines Darlehens oder Kredit wird als Mittelabfluss betrachtet. Sie sind wie folgt zu buchen:

* Auf dem Geldkonto (Kontoart Geldkonto) wird der Tilgungsbetrag (negativ) mit einer Buchungsart "Umbuchung" gebucht
* Auf dem Darlehenskonto (Kontoart Fremdkapital) wird der Tilgungsbetrag (positiv) mit einer Buchungsart "Umbuchung" gebucht

### Ein Mitglied spendet ein gegebenes Darlehen oder Kredit

Die Spende wird mit einer Buchungsart "Einnahme" auf dem Darlehenskonto verbucht.

Im Buchungsklassensaldo taucht diese Summe als Einnahme auf. In der Mittelverwendungsrechnung taucht dieser Betrag nicht auf. Es fliesen ja aktuell keine Mittel zu. Die Mittel sind ja schon bei Aufnahme des Darlehens zugeflossen. Lediglich der Mittelabfluss durch Tilgung entfällt zukünftig.

### Anschaffung einer nutzungsgebundenen Anlage

Anschaffungen die dem Zweck des Vereins dienen, also Anschaffungen im Ideellen Bereich oder im Zweckbetrieb werden als Mittelabfluss bewertet. Es handelt sich hier also um eine Mittelverwendung. Die Buchung erfolgt so:

* Es wird ein Anlagenkonto mit dem Anlagenzweck "Nutzungsgebundene Anlage" angelegt
* Die Anschaffungskosten werden auf dem Geldkonto abgebucht (negativ) mit einer Buchungsart "Umbuchung"
* Die Anschaffungskosten werden auf dem Anlagenkonto eingebucht (positiv) mit einer Buchungsart "Umbuchung"

### Verkauf einer nutzungsgebundenen Anlage

Bei Verkauf einer nutzungsgebunden Anlage fliest der gesamte Verkaufspreis einem Geldkonto zu. Dieser gesamte Betrag unterliegt jetzt wieder der zeitnahen Mittelverwendung. Die Buchung erfolgt so:

* Auf dem Geldkonto wird der Verkaufspreis verbucht mit einer Buchungsart "Einnahme"
* Auf dem Anlagenkonto wird der aktuelle Buchwert der Anlage ausgebucht mit einer Buchungsart "Ausgabe"

### Abschreibungen bei einer nutzungsgebundenen Anlage

Abschreibungen werden auf dem Anlagenkonto als Ausgabe gebucht. Sie fliesen nicht in die Mittelverwendungsrechnung ein weil Anlagen hier mit dem Buchwert verrechnet werden.

### Anschaffung einer zweckfremden Anlage

Anschaffungen die nicht dem Zweck des Vereins dienen aber zur Mittelbeschaffung dienen, also Anschaffungen in der Vermögensverwaltung oder im wirtschaftlichen Geschäftsbetrieb, werden nicht als Mittelabfluss bewertet. Diese unterliegen also der zeitnahen Mittelverwendung. Diese Konten werden wie Geldkonten behandelt.

Diese Anlagen dürfen nur aus vorhandenen freien Rücklagen oder aus dem Vermögen finanziert werden. Es müssen also freie Rücklagen oder Vermögen in dieser Höhe vorhanden sein. Die Buchung erfolgt so:

* Es wird ein Anlagenkonto mit dem Anlagenzweck "Zweckfremde Anlage" angelegt
* Die Anschaffungskosten werden auf dem Geldkonto abgebucht (negativ) mit einer Buchungsart "Umbuchung"
* Die Anschaffungskosten werden auf dem Anlagenkonto eingebucht (positiv) mit einer Buchungsart "Umbuchung"

### Verkauf einer zweckfremden Anlage

Bei Verkauf einer zweckgebundene Anlage fliest der gesamte Verkaufspreis einem Geldkonto zu. Der Gewinn aus dem Verkauf wird als Gewinn aus Umschichtungen bezeichnet. Da dieser Gewinn aus freien Rücklagen oder Vermögen finanziert wurde, kann dieser den freien Rücklagen oder dem Vermögen zugeführt werden, je nachdem aus welchen der beiden Mittel er gekauft wurde. Die Buchung erfolgt so:

* Auf dem Geldkonto wird der Verkaufspreis verbucht mit einer Buchungsart "Einnahme"
* Auf dem Anlagenkonto wird der aktuelle Buchwert der Anlage ausgebucht mit einer Buchungsart "Ausgabe"
* Der Gewinn wird im Konto der freien Rücklage oder dem Vermögen als Zuführung (Einnahme) verbucht

### Abschreibungen bei einer zweckfremden Anlage

Anscheinend ist es nicht klar geregelt wie Abschreibungen bei zweckfremden Anlagen behandelt werden sollen. In der Buchführung werden sie als Ausgabe gebucht wie bei nutzungsgebndenen Anlagen, da auch diese Anlagen mit dem Buchwert geführt werden.

Es gibt jetzt wohl zwei Ansätze:

Weg 1:

* Da die Anlage aus freier Rücklage oder Vermögen finanziert wurde reduziert sich das Vermögen. Darum reduziert man auch die freie Rücklage bzw. das Vermögen durch eine gleich hohe Ausgabenbuchung
* Bei Verkauf kann man dann vermutlich die Differenz aus Buchwert und Verkaufserlös wieder dem Vermögen gutschreiben

Weg 2:

* Die freie Rücklage oder das Vermögen wird nicht reduziert
* Bei Verkauf kann man dann vermutlich dann nur die Differenz aus Anschaffungskosten und Verkaufserlös wieder dem Vermögen gutschreiben

Der Weg 2 führt zu einem Mittelverwendungsüberhang weil die vorhandenen Mittel reduziert wurden aber nicht die Rücklagen bzw. das Vermögen.

### Geldspenden

Geldspenden sind Mittelzufluss und unterliegen damit grundsätzlich der zeitnahen Mittelverwendung. Ein Spender sollte davon ausgehen können, dass die Spende auch zeitnah verwendet wird.

§ 62 Abs. 3 AO definiert aber Ausnahmen. Erfolgt die Spende aus einem der genannten Gründe, dann kann diese Spende in das Vermögen überführt werden. Es wird wie folgt gebucht:

* Auf dem Geldkonto wird die Spende verbucht mit einer Buchungsart "Einnahme"
* Die Spende wird zusätzlich auf einem Konto der Kontoart "Vermögen nach § 62 Abs. 3 und 4 AO" als Einnahme verbucht
* Sollte noch kein Konto der Kontoart "Vermögen nach § 62 Abs. 3 und 4 AO" existieren, dann muss es neu angelegt werden

### Sachspende

Eine Sachspende gilt nicht als Mittelzufluss sondern ist grundsätzlich eine Zuführung zum Vermögen (§ 62 Abs. 4 AO). Es wird wie folgt gebucht:

* Es wird ein Anlagenkonto für die gespendete Sache angelegt und der Wert der Anlage als Buchung mit einer Buchungsart "Einnahme" verbucht
* Als Anlagenzweck ist zweckfremde Anlage zu wählen
* Die Spende wird zusätzlich auf einem Konto der Kontoart "Vermögen nach § 62 Abs. 3 und 4 AO" als Einnahme verbucht
* Sollte noch kein Konto der Kontoart "Vermögen nach § 62 Abs. 3 und 4 AO" existieren, dann muss es neu angelegt werden

Wird die Sachspende vom Spender ausdrücklich für satzungsgemäße Zwecke gespendet, dann kann sie auch als nutzungsgebundene Anlage verbucht werden. In diesem Fall darf der Wert nicht in ein Vermögenskonto eingetragen werden.
