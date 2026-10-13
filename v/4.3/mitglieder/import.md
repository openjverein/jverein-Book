# Mitglieder Import

## Allgemein

Über den Import Button im Mitglieder oder Nicht-Mitglieder View lassen sich neue Mitglieder importieren.

Im Gegensatz zur bisherigen Funktion [Migration](../administration/erweitert/migration.md) werden bestehende Mitglieder nicht gelöscht.

## CSV Format

Über den Import ist es sowohl möglich neue Mitglieder zu importieren als auch bestehende Mitglieder zu ändern. Wenn die Spalte "id" existiert, werden die bestehenden Mitglieder mit der jeweiligen id geändert. In dem Fall sind alle weiteren Spalten optional. Wenn es keine Spalte "id" gibt, werden neue Mitglieder erstellt.

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
* iban Pflichtfeld bei Mitgliedern bzw Nicht-Mitgliedern mit Zahlungsweg Basislastschrift
* bic wird automatisch ermittelt
* kontoinhaber
* individuellerbeitrag
* zahlungsweg (1=Basislastschrift,2=Überweisung,3=Barzahlung) default Basislastschrift
* zahlungsrhythmus nur wenn Beitragsmodell "Monatlich zu festen Terminen" Zahl oder text möglich (1=Monatlich, 3=Vierteljährlich, 6=halbjährlich, 12=Jährlich) default: Monatlich
* zahlungstermin nur bei Beitragsmodell "Flexiebel" (1,31,32,33,61,62,63,64,65,66,1201,1202,1203,1204,1205,1206,1207,1208,1209,1210,1211,1212) Default 1=monatlich
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

Ab Version 4.1 lassen sich auch die Zugehörigkeit zu einem Familienverband und abweichende Zahler importieren. Die entsprechenden Attribute sind:

* zahlerid Vollzahlendes Mitglied. Wird nur bei Mitgliedern in einer Beitragsgruppe der Art "Familienangehöriger" ausgewertet.
* alternativer_zahlerid Abweichender Zahler

Ab Version 4.4 können Vollzahler und abweichende Zahler auch im selben Import angelegt werden, auf den sich andere Zeilen beziehen. Die in Version 4.3 eingeführte Spalte externezahlerid gibt es nicht mehr, stattdessen steht in zahlerid die externe Mitgliedsnummer.

### Inhalt von zahlerid und alternativer_zahlerid

* Ist unter Einstellungen die externe Mitgliedsnummer nicht aktiviert, steht dort die Id eines Mitglieds, das schon in JVerein existiert.
* Ist die externe Mitgliedsnummer aktiviert, steht dort die externe Mitgliedsnummer des Zahlers. Der Zahler kann schon in JVerein existieren oder in derselben Datei in der Spalte externemitgliedsnummer stehen. Die Reihenfolge der Zeilen spielt dabei keine Rolle.
* `#17` steht immer für die Id 17, auch wenn die externe Mitgliedsnummer aktiviert ist. Das braucht man für Zahler ohne externe Mitgliedsnummer, z. B. Nicht-Mitglieder.
* `^` verweist auf die nächste Zeile darüber, bei der die Zelle in derselben Spalte leer ist. So können Familienmitglieder direkt unter dem Vollzahlenden stehen, ohne dass eine Nummer nötig ist. `^` funktioniert mit und ohne externe Mitgliedsnummer.
* Eine leere Zelle setzt keinen Zahler. alternativer_zahlerid muss also nicht für alle Mitglieder gefüllt sein.

Jede Zeile ohne eigenen Vollzahler beginnt einen neuen Familienverband: Folgt auf ein Familienmitglied mit `^` ein weiterer Vollzahler (oder eine Einzelperson), verweist das nächste `^` darunter auf diese Zeile. Zeilen dazwischen, die selbst einen Verweis haben (Nummer, `#17` oder `^`), werden übersprungen und ändern nicht, worauf ein `^` weiter unten verweist.

zahlerid und alternativer_zahlerid können gemeinsam angegeben werden, Familienzugehörigkeit und abweichender Zahler sind unabhängig voneinander. Der abweichende Zahler zahlt dann den Beitrag des Familienmitglieds. Sind abweichende Zahler unter Einstellungen nicht aktiviert, wird alternativer_zahlerid trotzdem importiert, bei Zahlungen aber nicht berücksichtigt. Darauf wird einmal im Importprotokoll hingewiesen.

### Reihenfolge der Verarbeitung

Der Import berücksichtigt Verweise auf Zeilen derselben Datei automatisch: Ein Vollzahler bzw. abweichender Zahler wird immer vor den Mitgliedern gespeichert, die auf ihn verweisen. Die Zeilennummern in Meldungen und Fehlermeldungen beziehen sich immer auf die Position in der Datei (ohne Kopfzeile), unabhängig von der Verarbeitungsreihenfolge.

Der Import bricht ab und es wird nichts importiert, wenn ein Zahler nicht gefunden wird, `^` keine Zeile darüber hat, eine externe Mitgliedsnummer mehrfach vorkommt oder Mitglieder sich gegenseitig als Zahler angeben.

### Beispiele

Mit externer Mitgliedsnummer. Anna steht vor ihrem Vollzahler Max, Eva gehört per `^` zu Hans, Willi hat Max als abweichenden Zahler:

```text
externemitgliedsnummer;name;vorname;beitragsgruppe;zahlerid;alternativer_zahlerid
M-2;Mustermann;Anna;Familienangehöriger;M-1;
M-1;Mustermann;Max;Vollzahler;;
M-3;Meier;Hans;Vollzahler;;
M-4;Meier;Eva;Familienangehöriger;^;
M-5;Wichtig;Willi;Vollzahler;;M-1
```

Ohne externe Mitgliedsnummer. Anna und Tom stehen mit `^` direkt unter Max, Eva unter Hans. Willi hat das schon vorhandene Mitglied mit der Id 1 als abweichenden Zahler:

```text
name;vorname;beitragsgruppe;zahlerid;alternativer_zahlerid
Mustermann;Max;Vollzahler;;
Mustermann;Anna;Familienangehöriger;^;
Mustermann;Tom;Familienangehöriger;^;
Meier;Hans;Vollzahler;;
Meier;Eva;Familienangehöriger;^;
Wichtig;Willi;Vollzahler;;1
```

### Bestehendes Vorgehen mit zwei Importen

Wie bisher können auch zwei Importe nacheinander durchgeführt werden: Im ersten Import werden die Mitglieder ohne zahlerid und alternativer_zahlerid importiert. Im zweiten Import werden die Mitglieder importiert, bei denen mit der Id der bereits vorhandenen Mitglieder ein Vollzahler oder abweichender Zahler gesetzt werden soll.
