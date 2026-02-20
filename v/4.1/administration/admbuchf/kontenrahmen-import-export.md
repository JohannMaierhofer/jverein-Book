# Kontenrahmen Import Export

## Allgemeines

Die JVerein-Buchführung beruht auf Buchungsarten (könnte man auch als Konten bezeichnen) und auf Buchungsklassen (Kontenrahmen). Für den Austausch von Kontenrahmen zwischen Vereinen gibt es den Export und Import im XML-Format.

Im Forum ist der SKR42 unter [https://jverein-forum.de/viewtopic.php?t=7394](https://jverein-forum.de/viewtopic.php?t=7394) zu finden, danke an tomtu.

Der SKR49 unter [https://jverein-forum.de/viewtopic.php?t=1265](https://jverein-forum.de/viewtopic.php?t=1265), danke an mgmf.

Sofern ihr einen allgemeingültigen Kontenrahmen für einen bestimmten Vereinstypen (z. B. Schulfördervereine) erstellt habt, bzw. in JVerein erfasst habt, könnt ihr ihn dort den Vereinskollegen zur Verfügung stellen.

## Export

Beim Export ist ein Verzeichnis und ggf. ein Dateiname auszuwählen.

Ein Export ist nur möglich, wenn Buchungsklassen existieren.

## Import

Beim Import ist die Datei auszuwählen.

Ein Import ist nur möglich, wenn weder Buchungsklassen noch Buchungsarten existieren.

## Datenformat

In JVerein 2.8.23 wurde zur Unterstützung des SKR 42 Kontenrahmens die feste Zuordnung zwischen Buchungsklasse und Buchungsart aufgehoben.

Hierzu musste das Format für den Kontenrahmen Export/Import angepasst werden.

Im alten Format wurde eine Versionsnummer 1 hinzugefügt. Das neue Format enthält die Versionsnummer 2.

Der Import für das Format V1 kann auch alte Dateien importieren in denen noch keine Versionsnummer enthalten ist.

Das V1 Format kann nur benutzt werden wenn es eine feste Zuordnung von Buchungsklassen zur Buchungsart gibt.

Das V2 Format muss verwendet werden wenn die feste Zuordnung von zwischen Buchungsklasse und Buchungsart aufgehoben ist. Es kann allerdings auch bei einer festen Zuordnung verwendet werden.

Beispiel für ein V1 Format:

```
<kontenrahmen>
  <version version="1"/>
  <buchungsklassen>
    <buchungsklasse bezeichnung="Klasse 1000" nummer="1000">
      <buchungsarten><buchungsart nummer="1000" bezeichnung="Mitgliedsbeitrag" art="0" spende="false" steuersatz="0.0" steuer_buchungsart="" status="0" abschreibung="false"/>
      <buchungsart nummer="1005" bezeichnung="Anf&#xe4;ngerschwimmen" art="0" spende="false" steuersatz="19.0" steuer_buchungsart="1000" status="0" abschreibung="false"/>
      <buchungsart nummer="1010" bezeichnung="Allg. Spenden" art="0" spende="true" steuersatz="0.0" steuer_buchungsart="" status="0" abschreibung="false"/>
      </buchungsarten>
    </buchungsklasse>
    <buchungsklasse bezeichnung="Klasse 2000" nummer="2000">
      <buchungsarten>
      <buchungsart nummer="2000" bezeichnung="Personalkosten" art="1" spende="false" steuersatz="0.0" steuer_buchungsart="" status="0" abschreibung="false"/>
      </buchungsarten>
    </buchungsklasse>
  </buchungsklassen>
</kontenrahmen>
```

Beispiel für ein V2 Format:

```
<kontenrahmen>
  <version version="2"/>
  <buchungsklassen>
    <buchungsklasse bezeichnung="Klasse 1000" nummer="1000"/>
    <buchungsklasse bezeichnung="Klasse 2000" nummer="2000"/>
  </buchungsklassen>
  <buchungsarten>
    <buchungsart nummer="1000" bezeichnung="Mitgliedsbeitrag" art="0" spende="false" buchungsklasse="1000" steuersatz="0.0" steuer_buchungsart="" status="0" abschreibung="false"/>
    <buchungsart nummer="1005" bezeichnung="Anf&#xe4;ngerschwimmen" art="0" spende="false" buchungsklasse="1000" steuersatz="19.0" steuer_buchungsart="1000" status="0" abschreibung="false"/>
    <buchungsart nummer="1010" bezeichnung="Allg. Spenden" art="0" spende="true" buchungsklasse="1000" steuersatz="0.0" steuer_buchungsart="" status="0" abschreibung="false"/>
    <buchungsart nummer="2000" bezeichnung="Personalkosten" art="1" spende="false" buchungsklasse="2000" steuersatz="0.0" steuer_buchungsart="" status="0" abschreibung="false"/>
  </buchungsarten>
</kontenrahmen>
```
