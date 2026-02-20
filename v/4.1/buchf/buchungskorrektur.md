# Buchungskorrektur

## Allgemeines

Banken können bei Überweisungen zusätzliche Daten zum Zweck hinzufügen die der Benutzer nicht eingegeben hat. Diese sind mit Tags versehen. Typische Tags sind:

* SVWZ: SEPA-Verwendungszweck, enthält den Text den der Benutzer eingegeben hat
* EREF: SEPA End to End-Referenz
* KREF: Kundenreferenz Customer Reference
* MREF: SEPA Mandatsreferenz
* CRED: SEPA Creditor Identifier
* DBET: Originator Identifier
* ABWA: Abweichender SEPA Auftraggeber
* IBAN: SEPA IBAN Auftraggeber
* BIC: SEPA BIC Auftraggeber
* PIN: PIN bei Überweisung

Diese Daten werden von Hibiscus mitgeliefert wenn sie von der Bank eingefügt wurden. In JVerein möchte man diese Textabschnitte außer SVWZ nicht unbedingt haben.

Hierzu gibt es das Feature Buchungskorrektur.

## Automatische Buchungskorrektur

In den Einstellungen unter Buchführung lässt sich neben der automatischen Buchungsübernahme aus Hibiscus auch die automatische Korrektur der Verwendungszwecke aktivieren.

Ist dies aktiviert werden die von Hibiscus gelieferten Verwendungszwecke automatisch korrigiert und die Verwendungszwecke unter SVWZ extrahiert.

PS: Es kann sein, dass eine Bank das SVWZ nicht enthält aber die anderen Tags. In diesem Fall beginnt der Verwendungszweck direkt mit dem Zweck. Auch das wird richtig extrahiert.

## Manuelle Buchungkorrektur

Hat man die automatische Buchungskorrektur nicht aktiviert oder hat man bereits Buchungen die nicht korrigiert sind, kann man die manuelle Buchungskorrektur unter dem Menüpunkt Buchführung->Buchungskorrektur aufrufen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_BuchungskorrekturView.png" alt="" /></picture>

Der View zeigt alle nicht abgeschlossenen Buchungen in denen eines der Tags EREF, KREF, MREF, CRED, DBET, SVWZ, ABWA, IBAN+, IBAN:, BIC gefunden wurde.

Es wird der aktuelle Eintrag des Verwendungszwecks unter "Verwendungszweck alt" angezeigt. Unter "Verwendungszweck neu" findet man die korrigierte Version.

Durch einen Klick auf den Korrektur Button werden die korrigierten Texte in die Buchungen übernommen.
