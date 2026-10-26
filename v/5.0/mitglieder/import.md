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

Ab Version 4.1 lassen sich auch Zugehörigkeit zu einem Familienverband und abweichende Zahler importieren. Der entsprechende Vollzahler bzw. Abweichende Zahler muss allerdings schon in JVerein existieren.

Ab Version 4.3 lässt sich ein Familienverband auch mit einem einmaligen Import durchführen. Voraussetzung ist, dass Externe Mitgliedsnummer aktiv ist.

Die entsprechenden Attribute sind:
* zahlerid Id des Vollzahlenden Mitglieds
* externezahlerid Externe Mitgliedsnummer des Vollzahlenden Mitglieds (nur wenn unter Einstellungen die externe Mitgliedsnummer aktiviert ist, nicht zusammen mit zahlerid)
* alternativer_zahlerid Id des abweichenden Zahlers

Mit externezahlerid kann ein Familienverband in einem einzigen Import angelegt werden. Der Vollzahler kann in derselben Datei stehen, die Reihenfolge der Zeilen spielt keine Rolle. Zeilen mit externezahlerid werden nach allen anderen Zeilen verarbeitet.

Im Falle eines  Abweichenden Zahlers bzw. wenn Externe Mitgliedsnummer nicht aktiv ist, auch bei Vollzahler, ist erst ein Import durchzuführen bei dem nur die Mitglieder importiert werden. In einem zweiten Import kann dann die Mitglieder nochmals importiert werden, die einem Vollzahler zugewiesen werden sollen bzw. bei denen ein abweichender Zahler gesetzt werden soll.
