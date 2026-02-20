# Migration

## Der Import von Mitgliedern

Zur Zeit ist der Import von Daten über das durch das Programm SPG-Verein (Sparkasse) vorgegebene CSV-Format realisiert. Diese Datenstruktur kann auch von anderen Programmen (auch Excel, LibreOffice und Co.) erzeugt werden (wird weiter unten beschrieben).

Einige zusätzliche Datenfelder können importiert werden. Der Dateiname muss eine Endung haben. Z.b..csv oder .txt. Der Dateiname darf keine Leerstellen enthalten. Es kann jede beliebige Endung verwendet werden. Die Daten werden in SPG-Verein unter Extras - Daten exportieren mit folgenden Parametern ausgegeben:

* Vorlage: Winword
* Dateiendung: .doc
* Feldseparator: ;=Strichpunkt/Semikolon
* Feldeinrahmung: keine
* Zeichensatz: ISO-8859-1
* Feldnamen: Ankreuzen

Als Feldtrennzeichen wird das Semikolon verwendet. Jede Zeile muss die gleiche Anzahl Semikola enthalten. Die Datei darf keine Anführungszeichen enthalten. Bei jedem Mitglied müssen die Spalten Beitragsart 1 und Beitrag 1 gefüllt sein.

Jede Datei enthält eine Kopfzeile und pro Mitglied eine Zeile. Beim Import werden sowohl die Beitragsgruppen-Tabelle als auch die Mitgliedertabelle aufgebaut. Ein erneuter Import löscht die vorhandenen Daten nach einer entsprechenden Warnung.

Sofern vor dem Import Zusatzfelder definiert wurden, können diese auch importiert werden. Die Datenfelder sind entsprechend der Bezeichnung in der Felddefinition in die Datei einzustellen.

Die Eingabedatei muss ISO-8859-1-codiert sein.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_ImportMenüpunkt.JPG)

Vor jedem Import sollten Sie sich im klaren sein, welche Einstellungen sie vorgenommen haben. Z.B. wenn sie Eintrittsdatum als Pflichtfeld definieren, dann muss für jedes Mitglied das Eintrittsdatum auch definiert sein. Außerdem sollten sie die, in der Tabelle definierte, maximale Länge, die jeder Eintrag haben darf, berücksichtigen. Wenn Sie dann noch die unterstützten Formate berücksichtigen sollte einem Import nicht mehr viel im Weg stehen.

Das Augenscheinlichste, was sich am Importer verändert hat, ist die Oberfläche; diese ist nun zweigeteilt. Auf der linken Seite befindet sich eine Tabelle mit allen nötigen ( rot hinterlegt ) und allen optionalen Spalten. Auf der rechten Seite erscheinen nach der Auswahl der zu importierenden Datei die in dieser definierten Spaltennamen. Nach dem Öffnen werden automatisch die Spalten zugeordnet, die den gleichen Namen besitzen, wobei die Groß/Kleinschreibung ignoriert wird. Falls Sie Zusatzfelder definiert haben, so werden diese ebenfalls angezeigt. Wenn es Eigenschaftsfelder in der Importdatei gibt werden diese nach dem Öffnen ebenfalls direkt anzeigt und einander zugeordnet. Die restlichen Felder müssen sie dann mittels Drag & Drop den enstprechenden Spalten zuweisen. Sollte eine Zuweisung falsch sein, so können sie diese wieder leicht mit der Entf-Taste löschen.

Es gibt nicht nur sichtbare Änderungen sondern ein paar auch unter der Haube. Deshalb hat sich die Tabelle ein wenig geändert, vor allem die möglichen Formatierungen wurden erweitert. Falls Ihre Einträge in Anführungsstrichen eingefasst ist z.B. "Name", dann werden diese automatisch entfernt.

## Importfelder

<details>

<summary>Mitglieds_Nr</summary>

**Inhalt:**\
Mitgliedsnummer, muss eine eindeutige ID sein, ansonsten kommt es zu einem Fehler. Wird bei der Verwendung von externen Mitgliedsnummern auch in die entsprechende Spalte eingetragen.

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

**MySQL:**\
\`id\` bigint(20) NOT NULL AUTO\_INCREMENT, \`externemitgliedsnummer\` varchar(50) DEFAULT NULL, PRIMARY KEY (\`id\`), UNIQUE KEY \`id\` (\`id\`), UNIQUE KEY \`externemitgliedsnummer\` (\`externemitgliedsnummer\`)

</details>

<details>

<summary>Personenart</summary>

**Inhalt:**\
n = natürliche Person\
j = juristische Person (Firma, Organisation, Behörde)\
Wenn die Spalte Personenart nicht in der Importdatei existiert, wird defaultmäßig 'n' übernommen.

**Max. Länge:**\
1

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
char(1) DEFAULT NULL

</details>

<details>

<summary>Anrede</summary>

**Inhalt:**\
Herrn / Frau

**Max. Länge:**\
40

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
varchar(40) DEFAULT NULL

</details>

<details>

<summary>Titel</summary>

**Inhalt:**\
Dr. ...

**Max. Länge:**\
40

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
varchar(40) DEFAULT NULL

</details>

<details>

<summary>Nachname</summary>

**Inhalt:**\
Nachname, wenn Personenart = j,\
dann Firmenname Zeile 1

**Max. Länge:**\
40

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

**MySQL:**\
\`name\` varchar(40) NOT NULL

</details>

<details>

<summary>Vorname</summary>

**Inhalt:**\
Vorname, wenn Personenart = j,\
dann Firmenname Zeile 2

**Max. Länge:**\
40

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

**MySQL:**\
varchar(40) DEFAULT NULL

</details>

<details>

<summary>Adressierungszusatz</summary>

**Inhalt:**\
Adressierungszusatz

**Max. Länge:**\
40

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
varchar(40) DEFAULT NULL

</details>

<details>

<summary>Straße</summary>

**Inhalt:**\
Straßenname inkl. Hausnummer

**Max. Länge:**\
40

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

**MySQL:**\
varchar(40) NOT NULL

</details>

<details>

<summary>Plz</summary>

**Inhalt:**\
Postleitzahl

**Max. Länge:**\
10

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

**MySQL:**\
varchar(10) NOT NULL

</details>

<details>

<summary>Ort</summary>

**Inhalt:**\
Ort

**Max. Länge:**\
40

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

**MySQL:**\
varchar(40) NOT NULL

</details>

<details>

<summary>Staat</summary>

**Inhalt:**\
Staat bei Auslandsanschriften

**Max. Länge:**\
50

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
varchar(50) DEFAULT NULL

</details>

<details>

<summary>Geburtsdatum</summary>

**Inhalt:**\
Geburtsdatum im Format:\
TT.MM.JJJJ\
TT.MM.JJ\
TT/MM/JJJJ\
TT/MM/JJJJ

JJ funktioniert für alle Mitglieder jünger 100.Ffür ältere Menschen muss es angepasst werden. Eine Warnung wird ausgegeben.

**Max. Länge:**\
10

* [x] **Spalte muss existieren**

**Leere Spalte erlaubt:**\
Abhängig von den Einstellungen

**MySQL:**\
date DEFAULT NULL

</details>

<details>

<summary>Sterbetag</summary>

**Inhalt:**\
Sterbetag, Austritt sollte auch definiert sein, ansonsten wird das Sterbedatum als Austrittsdatum angenommen. Unterstützte Formate siehe Geburtsdatum

**Max. Länge:**\
10

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
date DEFAULT NULL

</details>

<details>

<summary>Geschlecht</summary>

**Inhalt:**\
Muss mit einem kleinen oder großen m, w oder o beginnen z.B. gültig: Weiblich, männlich, ohne Angabe, M, w, o. Ist diese Spalte bei einem Mitglied leer so wird man bei der nächsten Bearbeitung des Mitglieds in JVerein aufgefordert das Geschlecht nachzutragen. Möchte man dies vermeiden, sollte man vor dem Import leere Daten in dieser Spalte mit bspw. o belegen.

**Max. Länge:**\
1

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
char(1) DEFAULT NULL

</details>

<details>

<summary>BIC</summary>

**Inhalt:**\
BIC

**Max. Länge:**\
11

* [x] **Spalte muss existieren**

**Leere Spalte erlaubt:**

Wenn Zahlungsart Lastschrift: nein, sonst ja

**MySQL:**\
varchar(11) DEFAULT NULL

</details>

<details>

<summary>IBAN</summary>

**Inhalt:**\
IBAN

**Max. Länge:**\
35

* [x] **Spalte muss existieren**

**Leere Spalte erlaubt:**

Wenn Zahlungsart Lastschrift: nein, sonst ja

**MySQL:**\
varchar(34) DEFAULT NULL

</details>

<details>

<summary>Mandat_Datum</summary>

**Inhalt:**\
Datum des Mandates TT.MM.JJJJ

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
date DEFAULT NULL

</details>

<details>

<summary>Zahlungsart</summary>

**Inhalt:**\
l (Kleinbuchstabe L) oder Lastschrift oder Abbuchung oder Bankeinzug für Lastschrift, b oder bar für Barzahlung u oder ueberweisung für Überweisung

**Max. Länge**\
1

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
1 SEPA, 2 Überweisung, 3 Bar, \`zahlungsweg\` int(11) DEFAULT NULL

</details>

<details>

<summary>Zahlungsrythmus</summary>

**Inhalt:**\
1 = monatlich\
3 = vierteljährlich\
6 = halbjährlich\
12 = jährlich\
wenn keine Angabe erfolgt, wird jährlich angenommen.

**Max. Länge**\
2

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
int(11) DEFAULT NULL

</details>

<details>

<summary>Kontoinhaber</summary>

**Inhalt:**\
Kontoinhaber

**Max. Länge:**\
70

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
varchar(70) DEFAULT NULL

</details>

<details>

<summary>Zahlungstermin</summary>

**Inhalt:**\
1 = monatlich,\
31 = Vierteljährlich (Jan./Apr./Juli/Okt)\
32 = Vierteljährlich (Feb./Mai /Aug./Nov.)\
33 = Vierteljährlich (März/Juni/Sep./Dez.)\
61 = Halbjährlich (Jan./Juli)\
62 = Halbjährlich (Feb./Aug.)\
63 = Halbjährlich (März/Sep.)\
64 = Halbjährlich (Apr./Okt.)\
65 = Halbjährlich (Mai /Nov.)\
66 = Halbjährlich (Juni/Dez.)\
1201 = Jährlich (Jan.)\
1202 = Jährlich (Feb.)\
1203 = Jährlich (März)\
1204 = Jährlich (Apr.)\
1205 = Jährlich (Mai )\
1206 = Jährlich (Juni)\
1207 = Jährlich (Juli)\
1208 = Jährlich (Aug.)\
1209 = Jährlich (Sep.)\
1210 = Jährlich (Okt.)\
1211 = Jährlich (Nov.)\
1212 = Jährlich (Dez.)

**Max. Länge**\
1-4

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

**MySQL:**\
int(11) DEFAULT NULL

</details>

<details>

<summary>Telefon_privat</summary>

**Inhalt:**\
private Telefonnummer

**Max. Länge**\
20

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Telefon_dienstlich</summary>

**Inhalt:**\
dienstliche / geschäftliche Telefonnummer

**Max. Länge**\
20

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Handy</summary>

**Inhalt:**\
Mobile Telefonnummer

**Max. Länge**\
20

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>E-Mail</summary>

**Inhalt:**\
E-Mail Adresse

**Max. Länge**\
50

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Eintritt</summary>

**Inhalt:**\
Eintrittsdatum, unterstützte Formate siehe Geburtsdatum

**Max. Länge**\
10

* [x] **Spalte muss existieren**

**Leere Spalte in Abhängigkeit von den Einstellungen erlaubt**

</details>

<details>

<summary>Beitragsart_1</summary>

**Inhalt:**\
Bezeichnung der Beitragsart. Z. B. Jugendliche, Erwachsene, Familien

**Max. Länge**\
30

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

</details>

<details>

<summary>Beitrag_1</summary>

**Inhalt:**\
Höhe des Beitrages in Euro (Format xxx,xx)

* [x] **Spalte muss existieren**
* [ ] **Leere Spalte erlaubt**

</details>

<details>

<summary>individuellerbeitrag</summary>

**Inhalt:**\
Höhe des individuellen Beitrages in Euro (Format xxx,xx)

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Austritt</summary>

**Inhalt:**\
Datum des Austritts, je nach Vereinssatzung ist die Kündigung erst zum Jahresende wirksam. Hier wird das Wirksamwerden der Kündigung vermerkt. Unterstützte Formate siehe Geburtsdatum.

**Max. Länge**\
10

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Kuendigung</summary>

**Inhalt:**\
Datum der Kündigung. Unterstützte Formate siehe Geburtsdatum

**Max. Länge**\
10

* [x] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Vermerk1</summary>

**Inhalt:**\
1\. Vermerk

**Max. Länge**\
255

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Vermerk2</summary>

**Inhalt:**\
1\. Vermerk

**Max. Länge**\
255

* [ ] **Spalte muss existieren**
* [x] **Leere Spalte erlaubt**

</details>

<details>

<summary>Eigenschaft_xxxxx</summary>

**Inhalt:**\
Eigenschaft eines Mitglieds. Diese Spalte kann mehrfach vorkommen. Anstatt von xxxxx wird die Eigenschaftengruppe eingetragen. Die importieren Eigenschaften dieser Gruppe zugeordnet.

**Max. Länge**\
30

* [ ] **Spalte muss existieren**

</details>

## Beispieldatei

### **Mit den Pflichtfeldern**

```
Mitglieds_Nr;Anrede;Titel;Nachname;Vorname;Straße;Plz;Ort;Geburtsdatum;Geschlecht;BIC;IBAN;Bankleitzahl;Kontonummer;Mandat_Datum;Zahlungsart;Telefon_privat;Telefon_dienstlich;Email;Eintritt;Beitragsart_1;Beitrag_1;Austritt;Kündigung;Sterbetag
22;Herrn;Dr.;Meier;Hans;Ackerstr.1;12345;Testenhausen;22.02.1970;m;MARKDEFF;DE68210501700012345678;12345678;12345;01.01.2000;l;01234-56789;;hans.meier@web.de;01.01.2000;Erwachsene;22,00;;;
```

### Mit allen Feldern (außer Eigenschaften)

```
Mitglieds_Nr;Personenart;Anrede;Titel;Nachname;Vorname;Adressierungszusatz;Straße;Plz;Ort;Staat;Geburtsdatum;Sterbetag;Geschlecht;BIC;IBAN;Bankleitzahl;Kontonummer;Mandat_Datum;Mandat_Version;Zahlungsart;Zahlungsrhytmus;Zahlungstermin;Kontoinhaber;Telefon_privat;Telefon_dienstlich;Handy;Email;Eintritt;Beitragsart_1;Beitrag_1;individuellerbeitrag;Austritt;Kündigung;Vermerk1;Vermerk2
22;Herrn;n;Dr.;Meier;Hans;;Ackerstr.1;12345;Testenhausen;Deutschland;22.02.1970;;m;MARKDEFF;DE68210501700012345678;12345678;12345;01.01.2000;1;l;12;1201;;01234-56789;;0170-1234567890;hans.meier@web.de;01.01.2000;Erwachsene;22,00;44,00;;;;
```

## Vorbereiten einer Mitgliederdatei in Office

In LibreOffice/OpenOffice/Excel müssen in der ersten Zeile die Feld- bzw- Spaltenbezeichnungen stehen und zwar genau in der oben angegebenen Schreibweise. Auf jeden Fall müssen Spalten für alle Pflichtfelder angelegt werden. Es können aber auch für alle Felder Spalten vorhanden sein, die dann leer bleiben.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Dateiaufbau.png" alt="" /></picture>

Standardmäßig müssen "Geburtsdatum" und "Eintritt" (Eintrittsdatum) angegeben werden. Unter Administration->Einstellungen->Anzeige kann dies vorab geändert werden. Speichern nicht vergessen.

In der Spalte "Beitragsart\_1" muss die Bezeichnung einer vorhandenen Beitragsgruppe eingetragen werden. Man kann sie unter Administration->Einstellungen->Beitragsgruppen nachschauen oder eine neue anlegen.

Gültige Werte für die Spalte "Zahlungsart" sind b für bar, u für Überweisung oder l für Lastschrift oder Abbuchung oder Bankeinzug. b,u oder l müssen klein geschrieben sein. Wenn l angegeben wird muss auch die IBAN angegeben werden. Ein Feld kann auch leer bleiben, dann wird vom Programm "Barzahlung" angenommen. Keins der Felder darf einen Zeilenumbruch beinhalten. Dies führt zu einer nicht importierbaren CSV Datei.

Beim speichern als CSV Datei (Comma Seperated Values) muss man zumindest in LibreOffice einen Haken bei "Edit filter settings" machen, um weitere Einstellungen vornehmen zu können.

## Anfängerfehler beim Importieren

Nach dem ausführlichen Testen von JVerein ist man gewillt, seine Stammdaten in die Software zu importieren. Dies kann sich unter Umständen als sehr schwierig erweisen. Je nach Aufwand, den man beim Testen betrieben hat, existieren in der Datenbank Verknüpfungen, die nicht automatisch gelöscht werden können. Dies betrifft unter anderem Beispielmitglieder und einen virtueller Buchungslauf. Der Buchungslauf blockiert das Überschreiben der Mitgliederdaten und führt damit zu Fehlern beim Importieren.

Im Idealfall baut man einen ganz neuen Ordner (Datenbankordner) für den produktiven Einsatz. Damit erledigen sich auch Fragen nach "Rücksetzen" der Buchungsnummern nach mehreren Testläufen.

## Formatierung von Beträgen

Beträge können entweder als Ganzzahl oder mit Euro und Cent getrennt durch ein Komma angegeben werden. Wichtig ist, dass die Daten in der CSV-Datei ohne führende oder angehängte Leerzeichen geschrieben werden. Es wurde von Problemen mit Excel berichtet.
