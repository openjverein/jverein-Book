# Mitglieder Import

## Allgemein

Über den Import Button im Mitglieder oder Nicht-Mitglieder View lassen sich neue Mitglieder importieren.

Im Gegensatz zur bisherigen Funktion [Migration](../administration/erweitert/migration.md) werden bestehende Mitglieder nicht gelöscht.

## CSV Format

Über den Import ist es sowohl möglich neue Mitglieder zu importieren als auch bestehende Mitglieder zu ändern. Wenn die Spalte "id" existiert, werden die bestehenden Mitglieder mit der jeweiligen id geändert. In dem Fall sind alle weiteren Spalten optional. Wenn es keine Spalte "id" gibt, werden neue Mitglieder erstellt.

Die Importdatei muss im CSV Format sein und kann folgende Spalten haben:

* vorname Pflichtfeld
* name Pflichtfeld
* geschlecht Pflichtfeld (m=Männlich,w=Weiblich,o=Ohne Angabe)
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
* iban Pflichtfeld bei Mitgliedern bzw Nicht-Mitgliedern mit Zahlungsweg Basislastschrift
* bic wird automatisch ermittelt
* kontoinhaber
* individuellerbeitrag
* zahlungsweg (1=Basislastschrift,2=Überweisung,3=Barzahlung) default Basislastschrift
* zahlungsrhythmus nur wenn Beitragsmodell "Monatlich zu festen Terminen" Zahl oder text möglich (1=Monatlich, 3=Vierteljährlich, 6=halbjährlich, 12=Jährlich) default: Monatlich
* zahlungstermin nur bei Beitragsmodell "Flexibel" (1,31,32,33,61,62,63,64,65,66,1201,1202,1203,1204,1205,1206,1207,1208,1209,1210,1211,1212) Default 1=monatlich
* mandatid Pflichtfeld bei Mitgliedern bzw Nicht-Mitgliedern mit Zahlungsweg Basislastschrift, wenn Quelle für Mandatsreferenz auf "Individuelle ID" gesetzt ist. Bei Nicht-Mitgliedern auch wenn Quelle für Mandatsreferenz auf "Externe Mitgliedsnummer" gesetzt ist
* mandatdatum Pflichtfeld bei Mitgliedern bzw Nicht-Mitgliedern mit Zahlungsweg Basislastschrift
* mandatversion default 0
* externemitgliedsnummer Pflicht wenn unter Einstellungen gesetzt
* vermerk1
* vermerk2
* eigenschaft\_NAME (wird bei allem anderen als nein, false gesetzt)
* zusatzfeld\_NAME
* sekundaer\_NAME für sekundäre Beitragsgruppen (wird bei allem anderen als nein, false gesetzt)

Felder mit anderem Namen werden ignoriert

## Familienverband und abweichende Zahler

Ab Version 4.1 lassen sich auch die Zugehörigkeit zu einem Familienverband und abweichende Zahler importieren. Für jede der beiden Rollen gibt es zwei Spalten, eine für die Id und eine für die externe Mitgliedsnummer des Zahlers:

| Rolle | Id des Zahlers | Externe Mitgliedsnummer des Zahlers |
| --- | --- | --- |
| Vollzahler | zahlerid | externezahlerid |
| Abweichender Zahler | alternativer_zahlerid | externealternativer_zahlerid |

* zahlerid bzw. externezahlerid werden nur bei Mitgliedern in einer Beitragsgruppe der Art "Familienangehöriger" ausgewertet.
* Pro Rolle dürfen auch beide Spalten gefüllt sein, siehe "Id und externe Mitgliedsnummer gleichzeitig".
* Eine leere Zelle setzt keinen Zahler. Die Spalten müssen also nicht für alle Mitglieder gefüllt sein.
* Ab Version 4.4 können Zahler auch im selben Import angelegt werden, auf den sich andere Zeilen beziehen.

### Id des Zahlers

zahlerid und alternativer_zahlerid enthalten die Id eines Mitglieds, das schon in JVerein existiert. Die Id ist unabhängig von der Einstellung "Externe Mitgliedsnummer". Das ist auch der Weg für Zahler, die keine externe Mitgliedsnummer haben, z. B. Nicht-Mitglieder.

### Externe Mitgliedsnummer des Zahlers

externezahlerid und externealternativer_zahlerid enthalten die externe Mitgliedsnummer des Zahlers. Der Zahler wird in dieser Reihenfolge gesucht:

1. In der Spalte externemitgliedsnummer einer Zeile derselben Datei. Die Reihenfolge der Zeilen spielt keine Rolle.
2. Nur wenn unter Einstellungen die externe Mitgliedsnummer aktiviert ist: bei den vorhandenen Mitgliedern in JVerein.

Ist die externe Mitgliedsnummer nicht aktiviert, werden die Nummern in der Spalte externemitgliedsnummer nicht gespeichert, sie dienen nur als Schlüssel innerhalb der Datei.

### Id und externe Mitgliedsnummer gleichzeitig

Sind in einer Rolle beide Spalten gefüllt (z. B. zahlerid und externezahlerid), gilt:

* Findet die Id ein Mitglied, wird dieses verwendet. Die externe Nummer wird dann nur geprüft.
* Verweist die externe Nummer auf ein anderes Mitglied als die Id, bricht der Import mit einer Meldung ab.
* Findet die Id kein Mitglied, wird die externe Nummer verwendet.
* Findet keine der beiden Angaben ein Mitglied, bricht der Import ab.
* `^` kann nicht zusammen mit einer zweiten Angabe zur selben Rolle stehen.

### ^ für die Zeile darüber

In jeder der vier Spalten verweist `^` auf die nächste Zeile darüber, die in dieser Rolle keinen Zahler angibt. So können Familienmitglieder direkt unter dem Vollzahlenden stehen, ohne dass Nummern nötig sind. `^` funktioniert mit und ohne externe Mitgliedsnummer.

Jede Zeile ohne eigenen Vollzahler beginnt einen neuen Familienverband: Folgt auf ein Familienmitglied mit `^` ein weiterer Vollzahler (oder eine Einzelperson), verweist das nächste `^` darunter auf diese Zeile. Zeilen dazwischen, die selbst einen Zahler angeben (Id, externe Nummer oder `^`), werden übersprungen und ändern nicht, worauf ein `^` weiter unten verweist.

### Vollzahler und abweichender Zahler zusammen

Familienzugehörigkeit und abweichender Zahler sind unabhängig voneinander. Der abweichende Zahler zahlt dann den Beitrag des Familienmitglieds. Sind abweichende Zahler unter Einstellungen nicht aktiviert, wird der abweichende Zahler trotzdem importiert, bei Zahlungen aber nicht berücksichtigt. Darauf wird einmal im Importprotokoll hingewiesen.

### Reihenfolge der Verarbeitung

Der Import berücksichtigt Verweise auf Zeilen derselben Datei automatisch: Ein Zahler wird immer vor den Mitgliedern gespeichert, die auf ihn verweisen. Die Zeilennummern in Meldungen und Fehlermeldungen beziehen sich immer auf die Position in der Datei (ohne Kopfzeile), unabhängig von der Verarbeitungsreihenfolge.

Der Import bricht ab und es wird nichts importiert, wenn ein Zahler nicht gefunden wird, `^` keine Zeile darüber hat, eine verwiesene externe Mitgliedsnummer in der Datei mehrfach vorkommt oder Mitglieder sich gegenseitig als Zahler angeben.

### Beispiele

Mit externer Mitgliedsnummer. Anna steht vor ihrem Vollzahler Max, Eva gehört per `^` zu Hans, Willi hat Max als abweichenden Zahler:

```text
externemitgliedsnummer;name;vorname;beitragsgruppe;externezahlerid;externealternativer_zahlerid
M-2;Mustermann;Anna;Familienangehöriger;M-1;
M-1;Mustermann;Max;Vollzahler;;
M-3;Meier;Hans;Vollzahler;;
M-4;Meier;Eva;Familienangehöriger;^;
M-5;Wichtig;Willi;Vollzahler;;M-1
```

Ohne externe Mitgliedsnummer. Die Nummern in der Spalte externemitgliedsnummer sind nur Schlüssel dieser Datei und werden nicht gespeichert. Ben verweist auf Hans weiter unten, Tom auf Max, Anna und Eva stehen mit `^` unter ihrem Vollzahler. Willi hat das schon vorhandene Mitglied mit der Id 1 als abweichenden Zahler:

```text
externemitgliedsnummer;name;vorname;beitragsgruppe;zahlerid;externezahlerid;alternativer_zahlerid
;Meier;Ben;Familienangehöriger;;h;
a;Mustermann;Max;Vollzahler;;;
;Mustermann;Anna;Familienangehöriger;^;;
;Mustermann;Tom;Familienangehöriger;;a;
h;Meier;Hans;Vollzahler;;;
;Meier;Eva;Familienangehöriger;;^;
;Wichtig;Willi;Vollzahler;;;1
```

### Umstellung auf externe Mitgliedsnummern

Sollen alle Mitglieder von internen auf externe Mitgliedsnummern umgestellt werden, wird zuerst unter Einstellungen die externe Mitgliedsnummer aktiviert. Im Import wählt die Spalte id das vorhandene Mitglied (Id) und externemitgliedsnummer setzt die neue Nummer. Bestehende Zahler bleiben bei leeren Zellen unverändert.

### Bestehendes Vorgehen mit zwei Importen

Wie bisher können auch zwei Importe nacheinander durchgeführt werden: Im ersten Import werden die Mitglieder ohne Zahler importiert. Im zweiten Import werden die Mitglieder importiert, bei denen mit zahlerid bzw. alternativer_zahlerid ein Vollzahler oder abweichender Zahler gesetzt werden soll.
