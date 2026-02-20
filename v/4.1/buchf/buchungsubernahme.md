# Buchungsübernahme

Nach der Kontensynchronisation in Hibiscus werden innerhalb von ca. 10 Sekunden die Buchungen aller Konten automatisch zu JVerein übernommen. Alle übernommenen Buchungen werden in einem Dialog angezeigt. Tritt bei der Buchungsübernahme ein Fehler auf, wird ein entsprechender Hinweis ausgegeben.

Die automatische Buchungsübernahme kann deaktiviert werden (siehe Einstellungen#Buchführung).

Die Vorraussetzungen für ein Funktionieren der Buchungsübernahme sind folgende:

* Die Übernahme muss aktiviert sein in JVerein/Administration/Buchführung
* Die Buchungs-IDs der Umsätze, die aus Hibsicus übernommen werden sollen müssen größer sein als die größte ID in JVerein. Spätere IDs wachsen von dort dann weiter und müssen nicht mehr bearbeitet werden.
* Das Konto in JVerein muss mit dem Konto in Hibiscus verknüpft sein. Siehe JVerein->Buchführung->Konten->Konto->Hibiscus-Konto
* Es müssen neue Umsätze in Hibiscus abgerufen werden, um die Übernahme anzustoßen. Siehe Hibiscus Konten Kontextmenü: Umsätze/Salden abrufen oder in Buchführung->Buchungen->Hibiscus-Import "Import Starten" klicken.
* Wenn bereits eine Übernahme lief, müssen neue Umsätze reinkommen, bevor eine erneute Übernahme angestoßen wird.
