# Lesefelder

Lesefelder sind virtuelle Datenbank-Felder. Sie werden mit Hilfe eines Scriptes berechnet und sind daher nur lesbar \(-&gt; Lesefelder \). Jedes Lesefeld besteht aus einer Bezeichnung und Skript-Code.

Lesefeld-Namen können frei, aber eindeutig gewählt werden. Intern wird `mitglied_lesefeld_` vorne angefügt. Um z.B. beim Schreiben einer E-Mail auf Lesefeld Anrede zuzugreifen, muss `${mitglied_lesefeld_Anrede}` eingegeben werden.

Der Inhalt von Lesefeldern wird durch Beanshell-Skripte beschrieben. Damit ist es möglich sehr komplexe Skripte in Java zu erstellen.

Jedes Skript muss als Rückgabe-Wert einen String zurückliefern.

## Lesefelder nutzen

Zunächst muss die Lesefelder-Funktion aktiviert werden. Administration \| Einstellungen \| Anzeige \| Lesefelder anzeigen

.



