# Zusatzbeträge importieren

Zusatzbeträge können auch importiert werden. Der Import kann über eine CSV-Datei (Default-Format), die nachfolgend beschrieben wird, erfolgen. Der Dateiname muss eine Endung haben. Z. B. .csv oder .txt. Es kann jede beliebige Endung verwendet werden. Der Dateiname darf keine Punkte, Sonderzeichen oder Leerstellen enthalten. Die Datenfelder werden durch Semikolon getrennt. Das Encoding kann beim Import ausgewählt werden.

Zur Zuordnung des Zusatzbetrages zum Mitglied muss entweder die Mitglieds\_ID, Ext\_Mitgieds\_ID oder Nachname und Vorname angegeben werden. Die nicht benötigten Spalten sind wegzulassen. Die Angabe von Nachname und Vorname setzt voraus, dass es keine Dubletten bei den Namen gibt.

Vorlage mit Mitglieds\_ID:

```
Mitglieds_Nr;Betrag;Buchungstext;Fälligkeit;Intervall;Endedatum
123;53.25;Jahresbeitrag;1.1.2011;12;01.01.2020
```

Vorlage mit Ext\_Mitglieds\_ID:

```
Ext_Mitglieds_Nr;Betrag;Buchungstext;Fälligkeit;Intervall;Endedatum
5555;53.25;Jahresbeitrag;1.1.2011;12;01.01.2020
```

Vorlage mit Nachname und Vorname:

```
Nachname;Vorname;Betrag;Buchungstext;Fälligkeit;Intervall
Schmitt;Monika;53.25;Jahresbeitrag;1.1.2011;12
```

Vorlage mit Nachname und Vorname und Endedatum:

```
Nachname;Vorname;Betrag;Buchungstext;Fälligkeit;Intervall;Endedatum
Schmitt;Monika;53.25;Jahresbeitrag;1.1.2011;12;1.1.2015
```

Die Datenfelder selbst sind folgendermaßen definiert

## Nachname

Nachname. Muss in Kombination mit dem Vornamen abgegeben werden, wenn die Mitglieds\_Nr nicht angegeben wurde.

## Vorname

Vorname. Muss in Kombination mit dem Nachnamen abgegeben werden, wenn die Mitglieds\_Nr nicht angegeben wurde.

## Betrag

Betrag. Anstatt eines Komma ist ein Punkt anzugeben.

## Buchungstext

Buchungstext. Max 140 Stellen. Darf kein Semikolon enthalten.

## Fälligkeit

Datum der Fälligkeit des Betrages. Format TT.MM.JJJJ

## Intervall

Intervall der Zahlung. 0=keine Wiederholung, 1 = monatlich, 2 = zweimonatlich, 3 = vierteljährlich, 6 = halbjährlich, 12 = jährlich

## Endedatum (optional)

Endedatum der Zahlung

## Buchungsart (optional)

Nummer der Buchungsart

## Buchungsklasse (optional)

Nummer der Buchungsklasse

## Zahlungsweg (optional)

Zahlungsweg der Zahlung. 0 = Standard, 1 = Basislastschrift, 2 = Überweisung, 3 = Barzahlung

Jede Datei enthält eine Kopfzeile und pro Zusatzbuchung eine Zeile.

## Steuer (optional)

Steuersatz
