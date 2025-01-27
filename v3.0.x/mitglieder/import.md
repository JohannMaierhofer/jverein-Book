# Mitglieder Import

## Allgemein

Über den Import Button im Mitglieder oder Nicht-Mitglieder View lassen sich neue Mitglieder importieren.

Im Gegensatz zur bisherigen Funktion [Migration](../administration/erweitert/migration.md) werden bestehende Mitglieder nicht gelöscht.

## CSV Format

Die Importdatei muss im CSV Format sein und kann folgende Spalten haben:

* vorname Pflichtfeld
* name Pflichtfeld
* geschlecht Pflichtfeld (m=Mänlich,w=Weiblich,o=Ohne Angabe)
* geburtsdatum Pflichtfeld bei Mitgliedern wenn unter Einstellungen gesetzt
* adresstyp ID wie in Einstellungen->Mitglied->Mitgliedstypen angezeigt, default 1=Mitglied
* personenart (n=natürliche Person,j=juristische Person) default n
* titel
* anrede
* strasse
* adressierungszusatz
* ort
* plz
* staat
* email
* telefondienstlich
* telefonprivat
* handy
* beitragsgruppe Pflichtfeld bei Mitgliedern (Name wie angezeigt)
* eintritt Pflichtfeld bei Mitgliedern
* austritt
* kuendigung
* sterbetag
* beitragsgruppe Pflichtfeld bei Mitgliedern
* iban Pflichtfeld bei Mitgliedern mit Zahlungsweg Basislastschrift
* bic wird automatisch ermittelt
* individuellerbeitrag
* zahlungsweg (1=Basislastschrift,2=Überweisung,3=Barzahlung) default Basislastschrift
* zahlungsrhythmus nur wenn Beitragsmodell "Monatlich zu festen Terminen" Zahl oder text möglich (1=Monatlich, 3=Vierteljährlich, 6=halbjährlich, 12=Jährlich) default: Monatlich
* zahlungstermin nur bei Beitragsmodell "Flexiebel" (1,31,32,33,61,62,63,64,65,66,1201,1202,1203,1204,1205,1206,1207,1208,1209,1210,1211,1212) Default 1=monatlich
* mandatdatum Pflichtfeld bei Mitgliedern mit Zahlungsweg Basislastschrift
* mandatversion default 0
* externemitgliedsnummer Pflicht wenn unter Einstellungen gesetzt
* ktoivorname
* ktoiname
* ktoianrede
* ktoistrasse
* ktoiadressierungszusatz
* ktoiplz
* ktoiort
* ktoistaat
* ktoiemail
* ktoipersonenart (n=natürliche Person,j=juristische Person)
* ktoititel
* ktoigeschlecht (m=Mänlich,w=Weiblich,o=Ohne Angabe)
* vermerk1
* vermerk2
* eigenschaft_NAME (wird bei allem anderen als nein, false gesetzt)
* zusatzfeld_NAME
* sekundaer_NAME für sekundäre Beitragsgruppen (wird bei allem anderen als nein, false gesetzt)

Felder mit anderem Namen werden ignoriert
