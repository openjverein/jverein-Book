# Kontenrahmen Import Export

## Allgemein

Die JVerein-Buchführung beruht auf \(könnte man auch als Konten bezeichnen\) und auf Buchungsklassen \(Kontenrahmen\). Für den Austausch von Kontenrahmen zwischen Vereinen gibt es den Export und Import im XML-Format.

Für den Austausch gibt es ein Forum unter [http://www.jverein.de/forum/viewforum.php?f=12](http://www.jverein.de/forum/viewforum.php?f=12). Sofern ihr einen allgemeingültigen Kontenrahmen für einen bestimmten Vereinstypen \(z. B. Schulfördervereine\) erstellt habt, bzw. in JVerein erfasst habt, könnt ihr ihn dort den Vereinskollegen zur Verfügung stellen.

## Export

Beim Export ist ein Verzeichnis und ggfls. ein Dateiname auszuwählen.

Ein Export ist nur möglich, wenn Buchungsklassen existieren.

## Import

Beim Import ist die Datei auszuwählen.

Ein Import ist nur möglich, wenn weder Buchungsklassen noch Buchungsarten existieren.

## Datenformat

```text
<kontenrahmen>
  <buchungsklassen>
    <buchungsklasse bezeichnung="Klasse 1000" nummer="1000">
      <buchungsarten>
         <buchungsart nummer="1000" bezeichnung="Mitgliedsbeitrag" art="0" spende="false"/>
         <buchungsart nummer="1005" bezeichnung="Anfängerschwimmen" art="0" spende="false"/>
         <buchungsart nummer="1010" bezeichnung="Allg. Spenden" art="0" spende="true"/>
      </buchungsarten>
    </buchungsklasse> 
    <buchungsklasse bezeichnung="Klasse 2000" nummer="2000"> 
      <buchungsarten> 
        <buchungsart nummer="2000" bezeichnung="Personalkosten" art="1" spende="false"/> 
  :
  :
  :
</kontenrahmen>
```

:

:

