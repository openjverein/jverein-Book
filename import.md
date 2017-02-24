# Import

## Der Import

Zur Zeit ist der Import von Daten über das durch das Programm SPG-Verein \(Sparkasse\) vorgegebene CSV-Format realisiert. Diese Datenstruktur kann auch von anderen Programmen \(auch Excel, LibreOffice und Co.\) erzeugt werden \(wird weiter unten beschrieben\).

Einige zusätzliche Datenfelder können importiert werden. Der Dateiname muss eine Endung haben. Z.b..csv oder .txt. Der Dateiname darf keine Leerstellen enthalten. Es kann jede beliebige Endung verwendet werden. Die Daten werden in SPG-Verein unter Extras - Daten exportieren mit folgenden Parametern ausgegeben:

* Vorlage: Winword
* Dateiendung: .doc
* Feldseparator: ;=Strichpunkt/Semikolon
* Feldeinrahmung: keine
* Zeichensatz: ISO-8859-1
* Feldnamen: Ankreuzen

Als Feldtrennzeichen wird das Semikolon verwendet. Jede Zeile muss die gleiche Anzahl Semikola enthalten. Die Datei darf keine Anführungszeichen enthalten. Bei jedem Mitglied müssen die Spalten Beitragsart 1 und Beitrag 1 gefüllt sein.

Jede Datei enthält eine Kopfzeile und pro Mitglied eine Zeile. Beim Import werden sowohl die Beitragsgruppen-Tabelle als auch die Mitgliedertabelle aufgebaut. Ein erneuter Import löscht die vorhandenen Daten nach einer entsprechenden Warnung.

Sofern vor dem Import Zusatzfelder definiert wurden, können diese auch importiert werden. Die Datenfelder sind entsprechend der Bezeichnung in der Felddefinition in die Datei einzustellen.

Die Eingabedatei muss ISO-8859-1-codiert sein.

![](/assets/EinstellungenImport.png)

Vor jedem Import sollten Sie sich im klaren sein, welche Einstellungen sie vorgenommen haben. Z.B. wenn sie Eintrittsdatum als Pflichtfeld definieren, dann muss für jedes Mitglied das Eintrittsdatum auch definiert sein. Außerdem sollten sie die, in der Tabelle definierte, maximale Länge, die jeder Eintrag haben darf, berücksichtigen. Wenn Sie dann noch die unterstützten Formate berücksichtigen sollte einem Import nicht mehr viel im Weg stehen.

Das Augenscheinlichste, was sich am Importer verändert hat, ist die Oberfläche; diese ist nun zweigeteilt. Auf der linken Seite befindet sich eine Tabelle mit allen nötigen \( rot hinterlegt \) und allen optionalen Spalten. Auf der rechten Seite erscheinen nach der Auswahl der zu importierenden Datei die in dieser definierten Spaltennamen. Nach dem Öffnen werden automatisch die Spalten zugeordnet, die den gleichen Namen besitzen, wobei die Groß/Kleinschreibung ignoriert wird. Falls Sie Zusatzfelder definiert haben, so werden diese ebenfalls angezeigt. Wenn es Eigenschaftsfelder in der Importdatei gibt werden diese nach dem Öffnen ebenfalls direkt anzeigt und einander zugeordnet. Die restlichen Felder müssen sie dann mittels Drag & Drop den enstprechenden Spalten zuweisen. Sollte eine Zuweisung falsch sein, so können sie diese wieder leicht mit der Entf-Taste löschen.

Es gibt nicht nur sichtbare Änderungen sondern ein paar auch unter der Haube. Deshalb hat sich die Tabelle ein wenig geändert, vor allem die möglichen Formatierungen wurden erweitert. Falls Ihre Einträge in Einführungstrichen eingefasst ist z.B. "Name", dann werden diese automatisch entfernt.

## Importfelder

| Spalte | Inhalt | Max. Länge | Spalte muss existieren | Leere Spalte erlaubt | MySQL |
| :--- | :--- | ---: | :--- | :--- | :--- |
| Mitglieds\_Nr | Mitgliedsnummer, muss eine eindeutige ID sein, ansonsten kommt es zu einem Fehler. Wird bei der Verwendung von externen Mitgliedsnummern auch in die entsprechende Spalte eingetragen. |  | ja | nein | \`id\` bigint\(20\) NOT NULL AUTO\_INCREMENT, \`externemitgliedsnummer\` varchar\(50\) DEFAULT NULL, PRIMARY KEY \(\`id\`\), UNIQUE KEY \`id\` \(\`id\`\), UNIQUE KEY \`externemitgliedsnummer\` \(\`externemitgliedsnummer\`\) |
| Personenart | n = natürliche Person, j = juristische Person \(Firma, Organisation, Behörde\). Wenn die Spalte Personenart nicht in der Importdatei existiert, wird defaultmäßig 'n' übernommen. | 1 | nein | ja | char\(1\) DEFAULT NULL |
| Anrede | Herrn / Frau | 40 | ja | ja | varchar\(40\) DEFAULT NULL |
| Titel | Dr. .... | 40 | ja | ja | varchar\(40\) DEFAULT NULL |
| Nachname | Nachname, wenn Personenart = j, dann Firmenname Zeile 1 | 40 | ja | nein | \`name\` varchar\(40\) NOT NULL |
| Vorname | Vorname, wenn Personenart = j, dann Firmenname Zeile 2 | 40 | ja | nein | varchar\(40\) DEFAULT NULL |
| Adressierungszusatz | Adressierungszusatz | 40 | nein | ja | varchar\(40\) DEFAULT NULL |
| Strasse | Straßenname inkl. Hausnummer | 40 | ja | nein | varchar\(40\) NOT NULL |
| Plz | Postleitzahl | 10 | ja | nein | varchar\(10\) NOT NULL |
| Ort | Ort | 40 | ja | nein | varchar\(40\) NOT NULL |
| Staat | Staat bei Auslandsanschriften | 50 | nein | ja | varchar\(50\) DEFAULT NULL |
| Geburtsdatum | Format TT.MM.JJJJ oder TT.MM.JJ oder TT/MM/JJJJ oder TT/MM/JJJJ. Bei JJ wird funktioniert fuer alle Mitglieder jünger hundert richtig, für älter Menschen muss es angepasst werden. Eine Warnung wird ausgegeben. | 10 | ja | in Abhängigkeit von den Einstellungen | date DEFAULT NULL |
| Sterbetag | Sterbetag, Austritt sollte auch definiert sein, ansonsten wird das Sterbedatum als Austrittsdatum angenommen. Unterstützte Formate siehe Geburtsdtatum | 10 | ja | ja | date DEFAULT NULL |
| Geschlecht | muss mit einem kleinen oder großen m, w oder o beginnen z.B. gültig: Weiblich, männlich, ohne Angabe, M, w, o. Ist diese Spalte bei einem Mitglied leer so wird man bei der nächsten Bearbeitung des Mitglieds in JVerein aufgefordert das Geschlecht nachzutragen. Möchte man dies vermeiden, sollte man vor dem Import leere Daten in dieser Spalte mit bspw. o belegen. | 1 | ja | ja | char\(1\) DEFAULT NULL |
| BIC | BIC | 11 | ja | Wenn Zahlungsart Lastschrift: nein, sonst ja | varchar\(11\) DEFAULT NULL			 |
| IBAN | IBAN | 35 | ja | Wenn Zahlungsart Lastschrift: nein, sonst ja | varchar\(34\) DEFAULT NULL |
| Mandat\_Datum | Datum des Mandates TT.MM.JJJJ |  | ja |  | date DEFAULT NULL |
| Zahlungsart | l \(Kleinbuchstabe L\) oder Lastschrift oder Abbuchung oder Bankeinzug für Lastschrift, b oder bar für Barzahlung u oder ueberweisung für Überweisung | 1 | ja | ja | 1 SEPA, 2 Überweisung, 3 Bar, \`zahlungsweg\` int\(11\) DEFAULT NULL |
| Zahlungsrhytmus | 1 monatlich, 3 vierteljährlich, 6 halbjährlich, 12 jährlich, wenn keine Angabe erfolgt, wird jährlich angenommen. | 2 | nein | ja | int\(11\) DEFAULT NULL |
| Zahlungstermin | 1 = Monatlich, 31 = Vierteljährlich \(Jan./Apr./Juli/Okt,\), 32 = Vierteljährlich \(Feb./Mai /Aug./Nov.\), 33 = Vierteljährlich \(März/Juni/Sep./Dez.\), 61 = Halbjährlich \(Jan./Juli\), 62 = Halbjährlich \(Feb./Aug.\), 63 = Halbjährlich \(März/Sep.\), 64 = Halbjährlich \(Apr./Okt.\), 65 = Halbjährlich \(Mai /Nov.\), 66 = Halbjährlich \(Juni/Dez.\), 1201 = Jährlich \(Jan.\), 1202 = Jährlich \(Feb.\), 1203 = Jährlich \(März\), 1204 = Jährlich \(Apr.\), 1205 = Jährlich \(Mai \), 1206 = Jährlich \(Juni\), 1207 = Jährlich \(Juli\), 1208 = Jährlich \(Aug.\), 1209 = Jährlich \(Sep.\), 1210 = Jährlich \(Okt.\), 1211 = Jährlich \(Nov.\), 1212 = Jährlich \(Dez.\) | 1-4 | nein | ja | int\(11\) DEFAULT NULL |
| KtoiPersonenart | Personenart des abweichenden Kontoinhabers, n = natürliche Person, j = juristische Person | 1 | nein | nein |  |
| KtoiAnrede | Anrede des abweichenden Kontoinhabers | 10 | nein | nein |  |
| KtoiTite | Titel des abweichenden Kontoinhabers \(Dr. o. ä.\) | 10 | nein | nein |  |
| KtoiName | Name des abweichenden Kontoinhabers | 40 | nein | nein |  |
| KtoiVorname | Vorname des abweichenden Kontoinhabers | 40 | nein | nein |  |
| KtoiStrasse | Straße des abweichenden Kontoinhabers | 40 | nein | nein |  |
| KtoiAdressierungszusatz | Adressierungszusatz des abweichenden Kontoinhabers | 40 | nein | nein |  |
| KtoiPlz | Postleitzahl des abweichenden Kontoinhabers | 10 | nein | nein |  |
| KtoiOrt | Ort des abweichenden Kontoinhabers | 40 | nein | nein |  |
| KtoiStaat | Staat des abweichenden Kontoinhabers | 40 | nein | nein |  |
| KtoiEMail | EMail-Adresse des abweichenden Kontoinhabers | 50 | nein | nein |  |
| Telefon\_privat | private Telefonnummer | 20 | ja | ja |  |
| Telefon\_dienstlich | dienstliche / geschäftliche Telefonnummer | 20 | ja | ja |  |
| Handy | Mobile Telefonnummer | 20 | nein | ja |  |
| Email | EMail-Adresse | 50 | ja | ja |  |
| Eintritt | Eintrittsdatum, unterstützte Formate siehe Geburtsdatum | 10 | ja | in Abhängigkeit von den Einstellungen |  |
| Beitragsart\_1 | Bezeichnung der Beitragsart. Z. B. Jugendliche, Erwachsene, Familien ... | 30 | ja | nein |  |
| Beitrag\_1 | Höhe des Beitrages in Euro \(Format xxx,xx\) |  | ja | nein |  |
| individuellerbeitrag | Höhe des individuellen Beitrages in Euro \(Format xxx,xx\). |  | nein | ja |  |
| Austritt | Datum des Austritts, je nach Vereinssatzung ist die Kündigung erst zum Jahresende wirksam. Hier wird das Wirksamwerden der Kündigung vermerkt. Unterstützte Formate siehe Geburtsdatum. | 10 | ja | ja |  |
| Kuendigung | Datum der Kündigung. Unterstützte Formate siehe Geburtsdatum | 10 | ja | ja |  |
| Vermerk1 | 1. Vermerk | 255 | nein | ja |  |
| Vermerk2 | 2. Vermerk | 255 | nein | ja |  |
| Eigenschaft\_xxxxx | Eigenschaft eines Mitglieds. Diese Spalte kann mehrfach vorkommen. Anstatt von xxxxx wird die Eigenschaftengruppe eingetragen. Die importieren Eigenschaften dieser Gruppe zugeordnet. | 30 | nein |  |  |

				

## Beispieldatei

### **Mit den Pflichtfeldern**	

```
Mitglieds_Nr;Anrede;Titel;Nachname;Vorname;Straße;Plz;Ort;Geburtsdatum;Geschlecht;BIC;IBAN;Bankleitzahl;Kontonummer;Mandat_Datum;Zahlungsart;Telefon_privat;Telefon_dienstlich;Email;Eintritt;Beitragsart_1;Beitrag_1;Austritt;Kündigung
22;Herrn;Dr.;Meier;Hans;Ackerstr.1;12345;Testenhausen;22.02.1970;m;MARKDEFF;DE68210501700012345678;12345678;12345;01.01.2000;l;01234-56789;;hans.meier@web.de;01.01.2000;Erwachsene;22,00;;;			
```

### Mit allen Feldern \(außer Eigenschaften\)

```
Mitglieds_Nr;Personenart;Anrede;Titel;Nachname;Vorname;Adressierungszusatz;Straße;Plz;Ort;Staat;Geburtsdatum;Sterbetag;Geschlecht;BIC;IBAN;Bankleitzahl;Kontonummer;Mandat_Datum;Mandat_Sequence;Mandat_Version;Zahlungsart;Zahlungsrhytmus;Zahlungstermin;KtoiPersonenart;KtoiAnrede;KtoiTitel;KtoiName;KtoiVorname;KtoiStrasse;KtoiAdressierungszusatz;KtoiPlz;KtoiOrt;KtoiStaat;KtoiEMail;Telefon_privat;Telefon_dienstlich;Handy;Email;Eintritt;Beitragsart_1;Beitrag_1;individuellerbeitrag;Austritt;Kündigung;Vermerk1;Vermerk2
22;Herrn;n;Dr.;Meier;Hans;;Ackerstr.1;12345;Testenhausen;Deutschland;22.02.1970;;m;MARKDEFF;DE68210501700012345678;12345678;12345;01.01.2000;1;l;12;1201;;;;;;;;;;;;01234-56789;;0170-1234567890;hans.meier@web.de;01.01.2000;Erwachsene;22,00;44,00;;;;
```

## Vorbereiten einer Mitgliederdatei in Office

n LibreOffice/OpenOffice/Excel müssen in der ersten Zeile die Feld- bzw- Spaltenbezeichnungen stehen und zwar genau in der oben angegebenen Schreibweise. Auf jeden Fall müssen Spalten für alle Pflichtfelder angelegt werden. Es können aber auch für alle Felder Spalten vorhanden sein, die dann leer bleiben.

![](/assets/Datei_Aufbau.png)

Standardmäßig müssen "Geburtsdatum" und "Eintritt" \(Eintrittsdatum\) angegeben werden. Unter "Administration" -&gt; "Einstellungen" -&gt; "Anzeige" kann dies vorab geändert werden. Speichern nicht vergessen.

![](/assets/Geburtsdatum_Eintrittsdatum_Einstellung.png)

In der Spalte "Beitragsart\_1" muss die Bezeichnung einer vorhandenen Beitragsgruppe eingetragen werden. Man kann sie unter "Administration" -&gt; "Einstellungen" -&gt; "Beitragsguppen" nachschauen oder eine neue anlegen.

![](/assets/Beitragsart.png)

Gültige Werte für die Spalte "Zahlungsart" sind b für bar, u für Überweisung oder l für Lastschrift oder Abbuchung oder Bankeinzug. b,u oder l müssen klein geschrieben sein. Wenn l angegeben wird muss auch die IBAN angegeben werden. Ein Feld kann auch leer bleiben, dann wird vom Programm "Barzahlung" angenommen. Keins der Felder darf einen Zeilenumbruch beinhalten. Dies führt zu einer nicht importierbaren CSV Datei.

Beim speichern als CSV Datei \(Comma Seperated Values\) muss man zumindest in LibreOffice einen Haken bei "Edit filter settings" machen, um weitere Einstellungen vornehmen zu können.

![](/assets/Save_Dialog.png)

Die Einstellungen sind wie folgt:

![](/assets/Mitgliederimport_Einstellungen_fuer_CSV.png)

## Anfängerfehler beim Importieren

Nach dem ausführlichen Testen von JVerein ist man gewillt, seine Stammdaten in die Software zu importieren. Dies kann sich unter Umständen als sehr schwierig erweisen. Je nach Aufwand, den man beim Testen betrieben hat, existieren in der Datenbank Verknüpfungen, die nicht automatisch gelöscht werden können. Dies betrifft unter anderem Beispielmitglieder und einen virtueller Buchungslauf. Der Buchungslauf blockiert das Überschreiben der Mitgliederdaten und führt damit zu Fehlern beim Importieren. 

Im Idealfall baut man einen ganz neuen Ordner \(Datenbankordner\) für den produktiven Einsatz. Damit erledigen sich auch Fragen nach "Rücksetzen" der Buchungsnummern nach mehreren Testläufen.

## Formatierung von Beträgen

Beträge können entweder als Ganzzahl oder mit Euro und Cent getrennt durch ein Komma angegeben werden. Wichtig ist, dass die Daten in der CSV-Datei ohne führende oder angehängte Leerzeichen geschrieben werden. Es wurde von Problemen mit Excel berichtet.

