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

Ab Version 4.1 lassen sich auch die Zugehörigkeit zu einem Familienverband und abweichende Zahler importieren. Ab Version 4.3 kann ein Familienverband mit externezahlerid in einem einzigen Import angelegt werden. Ab Version 4.4 geht das auch ohne externe Mitgliedsnummer, und auch abweichende Zahler lassen sich im selben Import angeben (Verweise mit `#lfdnr`, `#key` und `^`). Die entsprechenden Attribute sind:

* zahlerid Vollzahlendes Mitglied. Wird nur bei Mitgliedern in einer Beitragsgruppe der Art "Familienangehöriger" ausgewertet.
* externezahlerid Externe Mitgliedsnummer des Vollzahlenden Mitglieds (nur wenn unter Einstellungen die externe Mitgliedsnummer aktiviert ist, nicht zusammen mit zahlerid). Ist die externe Mitgliedsnummer nicht aktiviert, wird die Spalte ignoriert und im Importprotokoll darauf hingewiesen.
* alternativer_zahlerid Abweichender Zahler
* lfdnr oder key Schlüssel, über den sich andere Zeilen der Datei auf diese Zeile beziehen können (siehe unten)

### Inhalt von zahlerid und alternativer_zahlerid

* Eine Zahl ist die Id eines Mitglieds, das schon in JVerein existiert.
* `#wert` verweist auf die Zeile der Importdatei, in der die Spalte lfdnr bzw. key den Wert `wert` hat, z. B. `#12`. Das Mitglied muss nicht schon in JVerein existieren, es wird im selben Import angelegt.
* `^` verweist auf die nächste Zeile darüber, bei der die Zelle in derselben Spalte leer ist. So können Familienmitglieder direkt unter dem Vollzahlenden stehen, ohne dass ein Schlüssel nötig ist. Bei zahlerid zählen Zeilen mit externezahlerid nicht als Vollzahler.
* Ist die Zelle leer, wird kein Vollzahler bzw. abweichender Zahler gesetzt. alternativer_zahlerid muss also nicht für alle Mitglieder gefüllt sein.

Sind zahlerid und alternativer_zahlerid in derselben Zeile angegeben, wird eine Warnung im Importprotokoll ausgegeben, der Import läuft aber weiter.

### Schlüssel lfdnr und key

* lfdnr ist eine eindeutige ganze Zahl, z. B. eine in Excel fortlaufend nummerierte Spalte. `01` und `1` sind derselbe Schlüssel.
* key ist ein beliebiger eindeutiger Text, z. B. `mueller-1`.
* Es darf nur eine der beiden Spalten vorhanden sein. Die Groß- und Kleinschreibung der Spaltenüberschrift spielt keine Rolle, die Dokumentation verwendet Kleinbuchstaben.
* Die Spalten werden nicht in das Mitglied übernommen. Ältere JVerein-Versionen ignorieren sie wie alle unbekannten Spalten.
* Mit lfdnr bzw. key spielt die Reihenfolge der Zeilen keine Rolle. Die Datei kann also in Excel beliebig sortiert werden.

### Reihenfolge der Verarbeitung

Der Import berücksichtigt die Verweise automatisch: Ein Vollzahler bzw. abweichender Zahler wird immer vor den Mitgliedern gespeichert, die auf ihn verweisen. Zeilen mit externezahlerid werden nach allen anderen Zeilen verarbeitet. Die Zeilennummern in Meldungen und Fehlermeldungen beziehen sich immer auf die Position in der Datei (ohne Kopfzeile), unabhängig von der Verarbeitungsreihenfolge.

Der Import bricht ab und es wird nichts importiert, wenn ein Verweis nicht aufgelöst werden kann (unbekannter Schlüssel, `^` ohne Zeile darüber, doppelter Schlüssel, lfdnr keine ganze Zahl) oder Mitglieder sich gegenseitig als Zahler angeben.

### Beispiele

Familienverband über die externe Mitgliedsnummer. Anna steht vor ihrem Vollzahler Max, die Reihenfolge spielt keine Rolle:

```text
externemitgliedsnummer;name;vorname;beitragsgruppe;zahlerid;externezahlerid
2;Mustermann;Anna;Familienangehöriger;;1
1;Mustermann;Max;Vollzahler;;
```

Familienverband ohne externe Mitgliedsnummer. Eva verweist mit `#2` auf Hans, der weiter unten steht. Anna und Tom stehen mit `^` direkt unter Max. Willi hat Max als abweichenden Zahler (`#1`):

```text
lfdnr;name;vorname;beitragsgruppe;zahlerid;alternativer_zahlerid
;Meier;Eva;Familienangehöriger;#2;
1;Mustermann;Max;Vollzahler;;
;Mustermann;Anna;Familienangehöriger;^;
;Mustermann;Tom;Familienangehöriger;^;
2;Meier;Hans;Vollzahler;;
;Wichtig;Willi;Vollzahler;;#1
```

### Bestehendes Vorgehen mit zwei Importen

Wie bisher können auch zwei Importe nacheinander durchgeführt werden: Im ersten Import werden die Mitglieder ohne zahlerid und alternativer_zahlerid importiert. Im zweiten Import werden die Mitglieder importiert, bei denen mit der Id der bereits vorhandenen Mitglieder ein Vollzahler oder abweichender Zahler gesetzt werden soll.
