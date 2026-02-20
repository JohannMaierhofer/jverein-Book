# SEPA-Bugs

## SEPA-Fehler

Bei der Abrechnung gibt es einen Knopf "Hinweise/Warnungen/Fehler". Damit kann vor einer Abrechnung auf potentielle Probleme geprüft werden. U.a. wird geprüft, ob beim Zahlungsweg "Basislastschrift" auch ein Mandats-Datum gespeichert ist. Ohne Mandatsdatum kann keine Lastschrift erstellt werden. Weiterhin wird geprüft, ob die letzte (SEPA-)Lastschrift älter als 36 Monate ist. Auch in diesem Falle wird nicht abgerechnet.
