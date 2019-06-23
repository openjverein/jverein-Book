# Changelog

[Version 2.8.18](https://github.com/jverein/jverein/milestone/2?closed=1) vom 23.6.2019

[Version 2.8.17](https://github.com/jverein/jverein/milestone/1?closed=1) vom 18.02.2018

[Version 2.8.17](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.16) vom 31.12.2017

[Version 2.8.15](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.15) vom 21.02.2017

[Version 2.8.14](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.14) vom 02.02.2016

[Version 2.8.13](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.13) vom 28.02.2016

[Version 2.8.12](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.12) vom 06.12.2015

[Version 2.8.11](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.11) vom 09.08.2015

[Version 2.8.10](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.10) vom 09.06.2015

[Version 2.8.9](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.9) vom 27.04.2015

[Version 2.8.8](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.8) vom 26.04.2015

[Version 2.8.7](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.7) vom 01.03.2015

[Version 2.8.6](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.6) vom 05.01.2015

[Version 2.8.4](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.4) vom 23.12.2014

[Version 2.8.3](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.3) vom 02.11.2014

[Version 2.8.2](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.2) vom 01.11.2014

[Version 2.8.1](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.1) vom 20.09.2014

[Version 2.8.0](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.8.0) vom 16.08.2014

[Version 2.6.3](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.6.3) vom 16.03.2014

[Version 2.6.2](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.6.2) vom 09.03.2014

[Version 2.6.1](https://sourceforge.net/p/jverein/tickets/search/?q=status%3Aclosed+%26%26+labels%3A2.6.1) vom 28.12.2013

### Version 2.6.0 vom 18.12.2013

#### Neu

* Beim Mitglied kann in der Mailübersicht eine Mail gelöscht werden. Siehe [http://www.jverein.de/forum/viewtopic.php?f=4&t=1248](http://www.jverein.de/forum/viewtopic.php?f=4&t=1248)
* Für den Mail-Absender kann jetzt auch ein Anzeigename gespeichert werden. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1278](http://jverein.de/forum/viewtopic.php?f=1&t=1278)
* Buchungen duplizieren. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1000&p=5122\#p5122](http://jverein.de/forum/viewtopic.php?f=5&t=1000&p=5122#p5122)
* BIC und IBAN bei Einstellungen, Mitgliedern und Kursteilnehmern eingefügt
* Konvertierungsmodul BIC und IBAN.
* IBAN-Check implementiert.
* SEPA-Konvertierung erweitert: Mandatsdatum kann bei allen Mitgliedern auf ein Datum gesetzt werden. Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=1&t=1433&p=6365](http://www.jverein.de/forum/viewtopic.php?f=1&t=1433&p=6365) und [http://www.jverein.de/forum/viewtopic.php?f=1&t=1580](http://www.jverein.de/forum/viewtopic.php?f=1&t=1580)
* Spenden für JVerein um SEPA erweitert.
* Import: Mandat\_Sequence und Mandat\_Version können jetzt importiert werden. [http://jverein.de/forum/viewtopic.php?f=5&t=1666&p=6763](http://jverein.de/forum/viewtopic.php?f=5&t=1666&p=6763)
* Bei den Mitgliedern die Mandats-Sequenz eingefügt. Damit kann angegeben werden, ob das Mandat erstmalig, in Folge oder letztmalig genutzt wird. Momentan muss nach der Erstnutzung des Mandats die Sequenz händisch auf Folgenutzung umgestellt werden. Künftig wird das automatisch erledigt.
* SEPA-Lastschriften direkt zu Hibiscus übergeben.
* Buchführung: Anpassung an SEPA. Für die Mitgliederabrechnung muss ein Konto in der Buchführung existieren, dass entweder die IBAN des Vereinskontos oder die Kontonummer des Vereinskontos hat.
* Löschen von Adresstypen eingebaut.
* Mindestalter für die Berechnung des Mitgliedschaftsjubliäum. Patch von Rolf Mamat.
* Banken aus Österreich in die Bankentabelle aufgenommen. Weitere SEPA-Optimierung f. Österreich.
* Formulare duplizieren. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1365](http://jverein.de/forum/viewtopic.php?f=1&t=1365)
* Auswertung der Adressen. Siehe [http://jverein.de/forum/viewtopic.php?f=8&t=1307&p=5233](http://jverein.de/forum/viewtopic.php?f=8&t=1307&p=5233)
* Datum des SEPA-Mandats kann jetzt bei den Mitgliedern und Kursteilnehmern gespeichert werden. Bei bestehenden Mitgliedern wird das Eintrittsdatum eingesetzt.
* Splitbuchunen. Siehe [http://www.jverein.de/wiki/index.php?title=Splitbuchung](http://www.jverein.de/wiki/index.php?title=Splitbuchung)
* Import von Quickenbuchungen. Patch von Rolf Mamat.
* Automatisierte Änderung der Beitragsgruppe
* CSV-Export von Rechnungen und Mahnungen. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=273&p=1120\#p1120](http://www.jverein.de/forum/viewtopic.php?f=1&t=273&p=1120#p1120). Patch von Rolf Mamat.
* Neue Variable: Mitgliedskonto\_Stand = aktueller Kontostand dieses Mitglieds. Dieser Wert ist negativ wenn was offen ist. Weitere neue Variale: Mitgliedskonto\_Summe\_Offen = wert wie oben, allerdings ist er positiv wenn er offen ist. Siehe [http://www.jverein.de/forum/viewtopic.php?f=8&t=1547&p=6248](http://www.jverein.de/forum/viewtopic.php?f=8&t=1547&p=6248). Patch von Rolf Mamat
* Aufnahme der Buchungsnummer \(buchung\_id\) zu den Variablen und damit auch in den CSV-Export. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1635](http://jverein.de/forum/viewtopic.php?f=1&t=1635)

#### Geändert

* Beim löschen eines Mitgliedes werden die verknüpften Mails gelöscht. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=1268](http://www.jverein.de/forum/viewtopic.php?f=5&t=1268)
* Eigenschaftsbezeichnungen müssen nur noch innerhalb einer Eigenschaftengruppe eindeutig sein. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1249](http://jverein.de/forum/viewtopic.php?f=1&t=1249)
* Statistik DSB umbenannt in Statistik Jahrgänge. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1195\#p4934](http://jverein.de/forum/viewtopic.php?f=1&t=1195#p4934)
* Formularaufbereitung: Die Größe des Vorlagedokumentes wird jetzt für die Generierung gesetzt. Siehe [http://jverein.de/forum/viewtopic.php?f=8&t=1287](http://jverein.de/forum/viewtopic.php?f=8&t=1287)
* Standardadresstypen einrichten, wenn sie fehlen.
* Mitglied: Neu-Knöpfe bei Arbeitseinsätzen, Zusatzbeträgen, Wiedervorlage und Lehrgängen nach oben verschoben. Siehe auch [http://jverein.de/forum/viewtopic.php?f=5&t=1336](http://jverein.de/forum/viewtopic.php?f=5&t=1336)
* Kontonummern auf 12 Stellen erweitert \(Österreich und Schweiz\)
* Mitglied: Suchfelder für Name, Vorname und Strasse in normale Textfelder umgebaut.
* Externe Mitgliedsnummer in die Mitglieds-PDF-Auswertung aufgenommen.
* Mitglieder-Suche: Reset des Filters. Siehe [http://www.jverein.de/forum/viewtopic.php?f=8&t=1255](http://www.jverein.de/forum/viewtopic.php?f=8&t=1255)
* Erweiterung: Auf den Personalbögen werden jetzt Informationen zum Beitragszahler ausgeben.
* Arbeitseinsätze werden jetzt auch im Jahr des Austritts abgerechnet.
* Bei den Spendenbescheinigungen werden jetzt die zugrundeliegenden ausgegeben. Änderung von Rolf-Dieter.
* Das Mitgliedskonto wird jetzt standardmäßig geführt. Es kann nicht mehr abgeschaltet werden. Daraus ergibt sich, dass in der Buchführung das Konto, über das abgebucht wird, eingerichtet sein muss.
* Kontext-Menü bei der Buchungsübernahme entfernt. Siehe [http://www.jverein.de/forum/viewtopic.php?f=4&t=1431](http://www.jverein.de/forum/viewtopic.php?f=4&t=1431)
* Bei der Mitgliederauswertung kann jetzt das Format der CSV-Datei festgelegt werden. Patch von Rüdiger Wurth.
* Das Layout der Mitglieder-Suche und der Mitgliederauswertung wurde aneinander angepasst. Patch von Rüdiger Wurth.
* Anpassung der Datentypen der H2- und der MySQL-Datenbank.
* Zusätzliche Anzeige der Buchungsart-Nummer bei der Auswahl einer Buchungsart. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1425](http://jverein.de/forum/viewtopic.php?f=1&t=1425)
* Automatische Übernahme der Hibiscusbuchungen zu JVerein nach der Kontensynchronisation in Hibiscus. Siehe [http://www.jverein.de/forum/viewtopic.php?t=1456&p=5854](http://www.jverein.de/forum/viewtopic.php?t=1456&p=5854)
* Optional können jetzt auch negative Arbeitseinsätze erfasst werden. Patch von Rolf Mamat.
* Patch mit Bugfixes von Rolf-Dieter Clavery für [http://jverein.de/forum/viewtopic.php?f=7&t=1272](http://jverein.de/forum/viewtopic.php?f=7&t=1272) \(--&gt; Der Text wird nun mit Kästchen bzw. Kreuzchen dargestellt, entsprechend den Einstellungen\) und [http://jverein.de/forum/viewtopic.php?f=5&t=1427](http://jverein.de/forum/viewtopic.php?f=5&t=1427) \(--&gt; Betrag wird nun richtig dargestellt\)
* Zusatzbetrag-Import um Endedatum erweitert.
* Erweiterung des File-Dialoges beim Mitglieder-Import. Patch von Rolf Mamat.
* Zusätzliche Kontoinformationen in der Buchungsübersicht. Patch von Rolf Mamat.
* Optimierung der Anzeige der Familienangehörigen. Patch von Rolf Mamat.
* Buchführung: Vereinheitlichte Vorgabe des Kontos. Patch von Rolf Mamat.
* Variable "mitglied\_bankname" aufgenommen. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=1540](http://www.jverein.de/forum/viewtopic.php?f=1&t=1540). Patch von Rolf Mamat.
* Anzeige des Alters des Mitglieds. Patch von Rolf Mamat
* Check externe Mitgliedsnumer. Patch von Rolf Mamat
* Einstellungen: Bislang gab es in den Einstellungen den Vereinsnamen in der Länge 27 und der Länge 100. Durch SEPA wurde die Begrenzung auf 27 Stellen aufgehoben. Der Vereinsname ist jetzt 70 Stellen lang. Die 100-Stellige Variante wurde in die 70-Stellige übertragen und gelöscht.
* Neue Sollbuchung im Mitgliedskonto: Zahlungsweg des Mitglieds wird übernommen. Siehe jverein.de/forum/viewtopic.php?f=5&t=1507&p=6396
* Plausi in der Buchführung gelockert. Betrag 0 € ist zuläassig.
* Zusatzbeträge überarbeitet. Buchungstexte 1 + 2 zu einem zusammengefasst und auf 140 Zeichen verlängert.
* Zusatzbeträge-Import erweitert um Zugriff über externe Mitgliedsnummer.
* Mitglieder können jetzt mit dem Geschlecht "ohne Angabe" gespeichert werden.
* Abrechnung von Zusatzbeträgen auch für ausgetretene Mitglieder. Unter Administration\|Einstellungen\|Anzeige kann diese Option aktiviert werden.
* Korrekte Darstellung der Bankverbindung im Jameica-Adressbuch. [http://www.jverein.de/forum/viewtopic.php?f=5&t=1638](http://www.jverein.de/forum/viewtopic.php?f=5&t=1638)

#### Korrigiert

* Korrekter Link zur Formular-Hilfeseite
* Alters- und Mitgliedschaftsjubiläen werden jetzt für das korrekte Jahr ausgegeben. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1291](http://jverein.de/forum/viewtopic.php?f=5&t=1291) \(Backport zu 2.4.2\)
* Adressierungszusatz des Mitglieds wird in die Spendenbescheinigung übernommen. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1293&p=5140](http://jverein.de/forum/viewtopic.php?f=5&t=1293&p=5140). \(Backport zu 2.4.2\)
* Bugfix zu den Spendenbescheinigungen von Rolf. Siehe auch [http://jverein.de/forum/viewtopic.php?f=5&t=1292&p=5166\#p5166](http://jverein.de/forum/viewtopic.php?f=5&t=1292&p=5166#p5166) und [http://jverein.de/forum/viewtopic.php?f=7&t=1272&p=5165\#p5165](http://jverein.de/forum/viewtopic.php?f=7&t=1272&p=5165#p5165) \(Backport zu 2.4.2\)
* Vermeidung NPE bei der Eingabe neuer Mitglieder
* Bugfix Arbeitseinsätze. Patch von Rolf Mamat.
* Bugfix bei der Erstellung von Formularen. Zusatzfelder und Lesefelder werden nur ausgegeben, wenn auch Mitgliedsdaten ausgegeben werden.
* Mitgliedersuche nach Name funktioniert jetzt auch unter MySQL case-insensitiv. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1318&p=5432](http://jverein.de/forum/viewtopic.php?f=1&t=1318&p=5432)
* Bugfix: Mitgliedskontenexport.
* Bugfix Feldlänge Adressen von Spendern. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1320&p=5601](http://jverein.de/forum/viewtopic.php?f=5&t=1320&p=5601). Änderung von Rolf-Dieter.
* Bugfix Länge des Verwendungszwecks in der Tabelle Abrechnungslauf. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=1461&p=5868](http://www.jverein.de/forum/viewtopic.php?f=5&t=1461&p=5868)
* Buchungen: Fehlermeldungen an die Oberfläche bringen. Transaktionsklammer eingebaut. Patch von Rolf Mamat.
* Keinen Defaultwert bei fehlender Geschlechtsauswahl. Patch von Rolf Mamat.
* Bugfix Adressaufbereitung von Rolf Mamat.
* Bugfix Reset Mitglied-Filter-Bug von Rolf Mamat
* Bugfix Gegenbuchung im Mitgliedskonto bei Kursteilnehmern. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1629](http://jverein.de/forum/viewtopic.php?f=5&t=1629)
* Vermeidung von NoSuchMethodException. [http://www.jverein.de/forum/viewtopic.php?f=5&t=1640](http://www.jverein.de/forum/viewtopic.php?f=5&t=1640)
* Bugfix Buchungsübernahme von Rolf Mamat
* MySQL-Konfiguration: Leerzeichen am Ende der Zeile entfernen. [http://www.jverein.de/forum/viewtopic.php?f=5&t=1252&p=6727\#p6727](http://www.jverein.de/forum/viewtopic.php?f=5&t=1252&p=6727#p6727)
* Jameica-Termine: Bei Wiedervorlagen werden jetzt auch Name und Vorname des Mitglieds ausgegeben

### Version 2.4.2 vom 13.01.2013

* Bugfix: Alters- und Mitgliedschaftsjubiläen werden jetzt für das korrekte Jahr ausgegeben. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1291](http://jverein.de/forum/viewtopic.php?f=5&t=1291)
* Adressierungszusatz des Mitglieds wird in die Spendenbescheinigung übernommen. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1293&p=5140](http://jverein.de/forum/viewtopic.php?f=5&t=1293&p=5140).
* Bugfix zu den Spendenbescheinigungen von Rolf. Siehe auch [http://jverein.de/forum/viewtopic.php?f=5&t=1292&p=5166\#p5166](http://jverein.de/forum/viewtopic.php?f=5&t=1292&p=5166#p5166) und [http://jverein.de/forum/viewtopic.php?f=7&t=1272&p=5165\#p5165](http://jverein.de/forum/viewtopic.php?f=7&t=1272&p=5165#p5165)

### Version 2.4.1 vom 29.12.2012

* Erweiterung der Spendenbescheinigungen für das Jahr 2013. Patch von Rolf.
* Bugfix: Bei mehrzeiligen Datenfeldern in Formularen. Siehe [http://www.jverein.de/forum/viewtopic.php?t=884&p=4970](http://www.jverein.de/forum/viewtopic.php?t=884&p=4970).
* Bugfix beim Import von Zusatzbeträgen. Siehe [http://jverein.de/forum/viewtopic.php?f=5&t=1237](http://jverein.de/forum/viewtopic.php?f=5&t=1237). Patch von NotDifficult.
* Erste Vorarbeiten für SEPA-Lastschriften
* Bugfix Betragsfeld bei neuen Buchungen. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1270](http://jverein.de/forum/viewtopic.php?f=1&t=1270)
* Buchungsarten: Bugfix. Korrekte Position nach Rücksprung. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=1271](http://www.jverein.de/forum/viewtopic.php?f=1&t=1271)
* CSV-Export Mitglieder: Vermeidung NullPointerException bei der Ausgabe von Mitgliedern. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=1251&p=4954](http://www.jverein.de/forum/viewtopic.php?f=5&t=1251&p=4954)

### Version 2.4.0 vom 02.12.2012

#### Neu

* Import von Buchungen. Siehe [Buchungsimport](http://www.jverein.de/wiki/index.php?title=Buchungsimport)
* Projekte in der Buchführung. Projekte können unter Administration erfasst werden und den betreffenden Buchungen zugeordnet werden. Die Suche nach Projekten ist möglich. Die Projekteinformationen werden bei der CSV-Ausgabe berücksichtigt.
* "Abrechnungslauf rückgängig" setzt jetzt auch die Zusatzbeträge zurück.
* Export der Mitgliedskonten
* Export und Import von Kontenrahmen. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=886&p=3485](http://www.jverein.de/forum/viewtopic.php?f=1&t=886&p=3485) und [Kontenrahmen\_Export\_Import](http://www.jverein.de/wiki/index.php?title=Kontenrahmen_Export_Import)
* Lesefelder. Siehe [Lesefelder](http://www.jverein.de/wiki/index.php?title=Lesefelder). Patch von NotDifficult.
* Bei Mails gibt es jetzt eine Vorschau auf die Variablen und die Mail an ein Mitglied. Patch von NotDifficult.
* Mailübersicht pro Mitglied
* Mitgliedskonto \(Soll-, ggfls. Istbuchungen\) jetzt auch für Zusatzbeträge
* Patch von Julian: Unter Einstellungen kann die Mitglieds- und Adressmaske konfiguriert werden \(Spalten/Tabs\).
* Ausgabe der Jahrgangszahlen für die DSB-Statistik. Siehe auch [http://www.jverein.de/forum/viewtopic.php?t=1195&p=4747](http://www.jverein.de/forum/viewtopic.php?t=1195&p=4747)

#### Geändert

* Mitglieder-Suche: Tabs entfernt. Gründe: Unterschiedliches Verhalten der Tabellen innerhalb der Tabs und Performance-Optimierung.
* Variable "aktuellesjahr" aufgenommen. Siehe [http://www.jverein.de/forum/viewtopic.php?t=962&p=3774](http://www.jverein.de/forum/viewtopic.php?t=962&p=3774)
* Jubiläumsauswertungen \(Mitgliedschafts- und Altersjubliäen\) überarbeitet. Jetzt auch CSV-Export möglich.
* Suche im Jameica-Adressbuch über die JVerein-Adressen ist nicht mehr casesensitiv. Siehe www.jverein.de/forum/viewtopic.php?t=988&p=3865
* Personalbogen: Mitgliedsnummer aufgenommen.
* Abrechnung: Bei der Abbuchung werden die Vornamen der Familienangehörigen mit ausgegeben. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=914&p=3600](http://www.jverein.de/forum/viewtopic.php?f=1&t=914&p=3600)
* Versanddatum von Mails wird gespeichert. Eine Mail wird nur noch einmal pro Mitglied versandt. Zusätzlich gibt es einen Resend-Button. Patch von NotDifficult.
* Familienverband: Tabs mit Beschriftungen versehen. Bug bei der Löschung von Familienangehörigen. Patch von Difficult.
* Familienverband wird nur noch bei den betreffenden Beitragsarten angezeigt. Patch von NotDifficult.
* Zusätzliche Plausi bei der Verarbeitung von Beitragsarten. Bei Familienangehörigen muss der Betrag 0 sein. Patch von NotDifficult.
* Eigenschaften stehen jetzt auch für Nicht-Mitglieder zur Verfügung. Patch von Rolf.
* Codeoptimierung im Bereich des Mitgliedskontos
* Zusätzliche Variable MITGLIEDSKONTO\_IST und MITGLIEDSKONTO\_DIFFERENZ aufgenommen. [Forum](http://www.jverein.de/forum/viewtopic.php?f=1&t=909&p=4130)
* Optimierung der Mitglieder-View. Patch von NotDifficult.
* Keine Silbentrennung in der Spalte der Kommunikationsdaten bei den Mitgliedschaftsjubiläen und Altersjubiläen.
* Kontoauszug kann jetzt für einen vorgegebenen von-bis-Zeitraum ausgegeben werden.
* Erweiterung des Verwendungszwecks von 2 mal 27 Stellen auf 500 Stellen mit Zeilenumbruch
* Buchungsimport: Die BuchungsartNummer ist jetzt optional. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=1079&p=434](http://www.jverein.de/forum/viewtopic.php?f=1&t=1079&p=434)
* Anpassung an neue Jameica-Funktionalität zur Erhöhung der Barrierefreiheit.
* Punkte in Variablennamen wurden durch Unterstriche ersetzt.
* Spendenbescheinigungsformulare: Felder für die Sachspenden aufgenommen. Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=8&t=1163](http://www.jverein.de/forum/viewtopic.php?f=8&t=1163)
* Mail-Empfänger-Auswahl-Dialog: Jetzt werden auch die Datensätze von Spendern und andere Adressen angezeigt. Siehe auch [http://www.jverein.de/forum/viewtopic.php?t=1194&p=4742](http://www.jverein.de/forum/viewtopic.php?t=1194&p=4742)
* Box, die beim ersten Start von JVerein angezeigt wird aufgehübscht.
* Verzeichnis für die Auswahl eines Mail-Anhanges speichern und wiederherstellen. Siehe auch [http://jverein.de/forum/viewtopic.php?f=1&t=1231](http://jverein.de/forum/viewtopic.php?f=1&t=1231)

#### Korrigiert

* Bugfix: Fehlendes Konto bei 1. Buchung. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=946](http://www.jverein.de/forum/viewtopic.php?f=5&t=946)
* Bugfix: Übersicht Lehrgänge. Die Such-Lehrgangsart wurde immer wieder zurückgesetzt.
* Bugfix bei der Speicherung von Formularen unter MySQL. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=957](http://www.jverein.de/forum/viewtopic.php?f=5&t=957)
* Bei abgeschlossenen Buchungen konnten gespeicherte Dokumente nicht mehr angezeigt werden. Siehe [http://www.jverein.de/forum/viewtopic.php?f=8&t=688](http://www.jverein.de/forum/viewtopic.php?f=8&t=688)
* Fehler beim MySQL-Update beseitigt. Siehe [http://www.jverein.de/forum/viewtopic.php?t=974&p=3822](http://www.jverein.de/forum/viewtopic.php?t=974&p=3822)
* Jameica-changed-pluginloader.patch von Olaf
* Spalte FONT in der Tabelle formularfeld auf 50 Stellen verlängert.
* Bugfix Buchungssummenliste: [http://www.jverein.de/forum/viewtopic.php?f=5&t=1033&p=4046\#p4046](http://www.jverein.de/forum/viewtopic.php?f=5&t=1033&p=4046#p4046)
* Bugfix Pfad Spendenbescheinigungen. Siehe [Forum](http://www.jverein.de/forum/viewtopic.php?t=987&p=3864#p3864). Patch von Rolf.
* Buchungssummen Bugfix. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=1037&p=4059\#p4059](http://www.jverein.de/forum/viewtopic.php?f=5&t=1037&p=4059#p4059)
* Korrekte Ausgabe der Eigenschaften in der Mitgliedsauswertung im PDF-Format.
* Korrekte Prüfung der Kontonummer beim Buchungsimport. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=1077](http://www.jverein.de/forum/viewtopic.php?f=5&t=1077)
* Geburtsdatumsprüfung unter Berücksichtigung des Sterbedatums
* Korrekte Abschlussmeldung bei der Abrechnung
* Fehlermeldung auf der Benutzeroberfläche, wenn bei der Rechnungserstellung kein Formular existiert. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=1093](http://www.jverein.de/forum/viewtopic.php?f=5&t=1093)
* Buchungsdatum: Plausibilitätsprüfung auf 10 Jahre in die Vergangenheit und 0 Tage in die Zukunft. Siehe [http://jverein.de/forum/viewtopic.php?f=1&t=1104](http://jverein.de/forum/viewtopic.php?f=1&t=1104)
* Buxfix MailView: Label anstatt Textfeld. Siehe auch [http://www.jverein.de/forum/viewtopic.php?t=1130&p=4522](http://www.jverein.de/forum/viewtopic.php?t=1130&p=4522)
* Bugfix bei der Suche nach Adressen. Adresstyp bleibt jetzt erhalten. Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=5&t=1131&p=4559\#p4559](http://www.jverein.de/forum/viewtopic.php?f=5&t=1131&p=4559#p4559)
* Bei der Erstellung von Formularen werden in der Vorschau jetzt auch Testdaten des Mitgliedskontos zur Verfügung gestellt.
* Kursteilnehmer: Bugfix Geschlecht. Siehe auch [http://jverein.de/forum/viewtopic.php?f=5&t=1164](http://jverein.de/forum/viewtopic.php?f=5&t=1164)
* Bugfix Import bei mehrfachen Eigenschaften. Patch von Christian Lutz.
* Status der Tabelle für den Rücksprung speichern. Siehe [http://www.jverein.de/forum/viewtopic.php?t=1218&p=4803](http://www.jverein.de/forum/viewtopic.php?t=1218&p=4803)

### Version 2.2.1 vom 04.03.2012

* Bugfix bei der Neuaufnahme von neuen Mitgliedern wenn die Option "juristische Personen" aktiviert wurde. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=940&p=3742](http://www.jverein.de/forum/viewtopic.php?f=5&t=940&p=3742)
* Bugfix Abrechung Zusatzbeträge bei Austrittsdatum in der Zukunft. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=950&p=3732](http://www.jverein.de/forum/viewtopic.php?f=5&t=950&p=3732)
* Bugfix Personalbogen. Scalierung des Bildes unter Windows entfernt. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=237&p=3724\#p3724](http://www.jverein.de/forum/viewtopic.php?f=5&t=237&p=3724#p3724)
* Bugfix Import: Bei fehlender Spalte Adresstyp wurde der Zahlungsrhytmus überschrieben. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=417&p=3655](http://www.jverein.de/forum/viewtopic.php?f=5&t=417&p=3655)
* Bugfix Formularfeld "Anrede\_du": Komma fehlte am Ende. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=934](http://www.jverein.de/forum/viewtopic.php?f=5&t=934)

### Version 2.2.0 vom 14.02.2012

* Import benutzerfreundlicher. Patch von Julian.
* Erweiterung des Imports. Zuordnung der Spaltennamen im Dialog. Änderung von Christian Lutz.
* Neu: Spenden für JVerein.
* Neu: Ausgabe Kontoauszug Mitgliedskonto.
* Neu: BLZ-Update mit Hilfe der BLZ-Datei der Bundesbank
* Am 16.10.2011 erfolgte der Umzug von Berlios zu Sourceforge
* Teil 1: Erweiterung Spendenbescheinigung um Sammelbescheinigung. Patch von Danzelot.
* Teil 2: Überarbeitung der Spendenbescheinigungen. Siehe auch [Spendenbescheinigung](http://www.jverein.de/wiki/index.php?title=Spendenbescheinigung). Patch von Rolf
* Neu: Buchungsexport im CSV-Format
* Basisdaten des Mitglieds können mit einem Rechtsklick kopiert werden. Siehe auch [http://www.jverein.de/forum/viewtopic.php?t=542&p=2418'](http://www.jverein.de/forum/viewtopic.php?t=542&p=2418%27)
* Beim Import von Zusatzbeträgen sind jetzt auch Anführungszeichen als Feldbegrenzer erlaubt.
* Neu: Übersicht Familienbeiträge. Doppelklick öffnet das Mitglied. Rechtsklick bietet die Möglichkeit, das Mitglied aus dem Famlilienverband zu entfernen.
* Sterbedatum ist jetzt optional. Unter Einstellungen\|Ansicht\|Sterbedatum kann die Einstellung vorgenommen werden.
* Mitglied: Anzeige der Mitgliedsnummer.
* Neue Filteroption "alle" bei der Überprüfung Arbeitseinsätze. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=678'](http://www.jverein.de/forum/viewtopic.php?f=5&t=678%27)
* Abrechnung/Beitragsmodell: Vereinfachung der Parameter, jährlich, halbjährlich, vierteljährlich und monatlich zu 'alle' bzw. 'gleicher Termin für alle'
* Mitgliedskonto: Bei der Auswahl können jetzt nicht nur Mitglieder oder Spender sondern alle Adressen ausgewählt werden.
* Mehreren Buchungen ein Mitgliedskonto gleichzeitig zuordnen. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=699&p=2740'](http://www.jverein.de/forum/viewtopic.php?f=1&t=699&p=2740%27)
* Terminkalender zu Jameica verschoben. Termin-Box gelöscht.
* Unter Einstellungen\|Beiträge kann der DTAUS-Textschlüssel ausgewählt werden. Standardmäßig ist Lastschrift eingestellt. Wer aus Abbuchung umstellt, sollte sich über die Bedeutung im Klaren sein. Ggfls. nach Rücksprache mit der Hausbank.
* Zusatzbeträge-Import: Zusätzliche Plausi zum Aufbau der Datei. [http://www.jverein.de/forum/viewtopic.php?f=5&t=744](http://www.jverein.de/forum/viewtopic.php?f=5&t=744)
* Adresstyp beim Import eingefügt.
* Mitgliedauswertungen: Selektion nach Mailadressen erweitert.
* Trefferliste der Mitglieder: Mit einem Rechtsklick können die sichtbaren Daten in die Zwischenablage kopiert werden. Patch von NotDifficult.
* Mehr Fehlertoleranz bei der Buchungsübernahme aus Hibiscus.
* Initialer Wert 1 für Primary Key bei H2-Datenbank, siehe [http://www.onlinebanking-forum.de/phpBB2/viewtopic.php?p=80884](http://www.onlinebanking-forum.de/phpBB2/viewtopic.php?p=80884)
* Einstellungen: Spendenbescheinigungsinformationen vom Tab Allgemein in den Tab Spendenbescheinigungen verschoben.
* Fehlerbehandlung bei der Mitgliedsstatistik
* Numerische Sortierung der Hibiscus-Buchungen bei der Übernahme zu JVerein.
* Bugfix bei der Mitgliedersuche, sofern mit Zusatzfeldern experimentiert wurde.
* Mitgliederübersicht: Korrekte Sortierung nach ID. Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=5&t=582&p=2436](http://www.jverein.de/forum/viewtopic.php?f=5&t=582&p=2436)
* Sofortige Aktualisierung der Anzeige nach Ist-Löschung im Mitgliedskonto. Patch von Julian.
* Import: Spalte individuellerbeitrag ist keine Pflichtspalte
* Mitglieder-Statistik: Anpassung Ein- und Austritte an das Geschäftsjahr.
* Geschäftsjahr: Bugfix bei der Berechnung des Endes des Geschäftsjahres.
* Zusatzbeträge: Bugfix Default-Wert für das Fälligkeitsdatum
* Bei der Löschung von Eigenschaften wird jetzt auch die Zuordnung von Mitgliedern zur Eigenschaft gelöscht.
* Vermeidung NPE bei der Aufbereitung der Variablen für die Mahnung.
* Abrechnung: Vermeidung NPE bei fehlendem Stichtagsdatum.
* Mahnung: Korrekte Verarbeitung der Mitgliedskonto\*-Variablen.
* Bugfix bei der Tabellenhöhe der Arbeitsdienstüberprüfung.
* Bugfix "Übernahme"-Button für Soll+Ist im Mitgliedskontoauswahldialog. [http://www.jverein.de/forum/viewtopic.php?f=5&t=680](http://www.jverein.de/forum/viewtopic.php?f=5&t=680) Patch von Danzelot.
* Bugfix Filter Überprüfung Arbeitseinsätze. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=678](http://www.jverein.de/forum/viewtopic.php?f=5&t=678)
* Mitgliedskontoauswahl: Bugfix OperationCanceledException und Widged is disposed. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=679](http://www.jverein.de/forum/viewtopic.php?f=5&t=679)
* Bei der Speicherung der Einstellungen wird auf notwendige Plugins geprüft, wenn Dokumentenspeicherung aktiviert wurde.
* Bugfix Sortierung Buchungsartenliste. Siehe [http://www.jverein.de/forum/viewtopic.php?t=693&p=2709\#p2709](http://www.jverein.de/forum/viewtopic.php?t=693&p=2709#p2709)
* Individuelle Spendenbescheinigung: Check ob auch ein Formular ausgewählt wurde - Patch von Christian Lutz
* Bugfix Sortierung Buchungsübersicht.
* Bugfix bei der Abrechnung von Zusatzbeträgen neuer Mitglieder.
* Terminübersicht: Ausgetretene Mitglieder werden nicht mehr angezeigt. [http://www.jverein.de/forum/viewtopic.php?f=5&t=753](http://www.jverein.de/forum/viewtopic.php?f=5&t=753)
* Bugfix Adressbuch-Export für Hibiscus: NPE beseitigt bei Nichtmitgliedern mit Bankverbindung. [http://www.jverein.de/forum/viewtopic.php?f=5&t=755&p=2944](http://www.jverein.de/forum/viewtopic.php?f=5&t=755&p=2944)
* Bugfix CSV-Export: Bei Akademikerinnen wurde der Titel nicht ausgegeben. [http://www.jverein.de/forum/viewtopic.php?f=5&t=757](http://www.jverein.de/forum/viewtopic.php?f=5&t=757)
* Bugfix "neue Buchung / Mitgliedskontoauswahl". [http://www.jverein.de/forum/viewtopic.php?f=5&t=773](http://www.jverein.de/forum/viewtopic.php?f=5&t=773)
* Bugfix. Klick in der Mitgliedskontenübersicht auf eine Adresse öffnete Mitglied. [http://www.jverein.de/forum/viewtopic.php?f=5&t=776](http://www.jverein.de/forum/viewtopic.php?f=5&t=776)
* Bugfix Adressensuche. [http://www.jverein.de/forum/viewtopic.php?f=5&t=781](http://www.jverein.de/forum/viewtopic.php?f=5&t=781)
* Codeoptimierung bei den Mitgliederauswertungen.
* Adressbuch-Export von Mail zu den den Mitgliederauswertungen verschoben.
* Bugfix in der Kontenübersicht bei Wechsel der ID des Hibiscus-Kontos
* Mitglieder-Suche: Bugfix Speicherung der Suchkriterien. [http://www.jverein.de/forum/viewtopic.php?f=5&t=838](http://www.jverein.de/forum/viewtopic.php?f=5&t=838)
* Bugfix Sortierung der Familienbeiträge. Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=5&t=839](http://www.jverein.de/forum/viewtopic.php?f=5&t=839)
* Buchungklassen: Bugfix "Anzahl Buchungen ohne Buchungsart". Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=5&t=849](http://www.jverein.de/forum/viewtopic.php?f=5&t=849)
* Buchungsliste: Bugfix fehlende Einzelbuchungen bei Auswahl "Alle Buchungsarten". Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=5&t=819](http://www.jverein.de/forum/viewtopic.php?f=5&t=819)
* Bugfix "leere Nummer" bei Speicherung von Buchungsarten. Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=845](http://www.jverein.de/forum/viewtopic.php?f=5&t=845)
* Bugfix bei den Zusatzbeträgen: "monatlich" wurde mehrfach als Intervall angeboten. [http://www.jverein.de/forum/viewtopic.php?f=5&t=894](http://www.jverein.de/forum/viewtopic.php?f=5&t=894)
* Bugfix Zusatzbeträge: keine Abrechnung bei ausgetretenen Mitgliedern. [http://www.jverein.de/forum/viewtopic.php?f=5&t=895](http://www.jverein.de/forum/viewtopic.php?f=5&t=895)
* Bugfix Variable "anrede\_du"
* Patch von Rolf zur Buchungsliste und zum Buchungsjournal.
* Numerische Sortierung der Hibiscus-Buchungen bei der Übernahme zu JVerein.
* 2-spaltiges Layout bei den Buchungen wiederhergestellt. Patch von Rolf.

### Version 2.0.1 vom 29.6.2011

* Bugfix Autovervollständigung Name beim Mitglied.
* Bugfix Erstinstallation mit H2-Datenbank
* Bugfix Summierung bei der kompakten Abbuchung.
* Personalbogen: Sortierung der Zusatzbeträge nach Fälligkeitsdatum.
* Bugfix Speicherung der Suchkriterien von- und bis-Datum bei Buchungen
* Vermeidung NPE bei Mitgliedskonto-Zuordnung
* Buchungsklassen-Saldo: Sortierung der Buchungsarten innerhalb der Buchungsklassen nach Nummer. Siehe [http://www.jverein.de/forum/viewtopic.php?f=1&t=834](http://www.jverein.de/forum/viewtopic.php?f=1&t=834)

### Version 2.0.0 vom 23.6.2011

* Terminübersicht Geburtstage und Wiedervorlagen.
* Die Boxen "aktuelle Geburtstage" und "Wiedervorlagen" für die Startseite entfernt. Ersatz ist die neue Terminübersicht.
* Neue Box "Termine" für die Startseite erstellt
* Arbeitseinsätze
* Speicherung zusätzlicher Adressen \(u. a. Spender/innen\) ermöglicht.
* Speicherung von Dokumenten zu Buchungen und Mitgliedern. Siehe [http://developer.berlios.de/bugs/?func=detailbug&bug\_id=17106&group\_id=7335'](http://developer.berlios.de/bugs/?func=detailbug&bug_id=17106&group_id=7335%27)&gt;\#17106
* Eigenschaftengruppen können so markiert werden, dass maximal eine Eigenschaft ausgewählt werden kann. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=17741&group\_id=7335'](https://developer.berlios.de/bugs/?func=detailbug&bug_id=17741&group_id=7335%27)&gt;\#17741
* Erzeugung Sollbuchung bei Zuordnung des Mitgliedskontos.
* Stammdaten des Vereins in die Einstellungen verschoben.
* Neu: Individueller Beitrag pro Mitglied. Überschreibt Betrag in der Beitragsgruppe.
* Beitragsgruppen können jetzt Buchungsarten zugewiesen werden. Diese werden bei der Verwendung des Mitgliedskontos bei der Abrechung \(z. Z. nur neue Version\) in die Istsätze der Abbuchungsbeträge geschrieben.
* Freie Formulare eingeführt. Unter Administration\|Formulare können die Formulare eingerichtet werden. Mit einem rechten Mausklick auf ein Mitglied werden im Kontextmenü auch die freien Formulare angezeigt. Ein Klick darauf erzeugt das Formular
* Buchungen können jetzt auch dem "Mitgliedskonto" eines Spenders zugewiesen werden.
* Zusätzliche Datenfelder in Mails und Formatierung von Datums- und Betragsfeldern [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=17648&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=17648&group_id=7335)
* CSV-Export \(Mitgliederauswertung\) total überarbeitet. Neue Spaltennamen. Eigenschaften werden mit ausgegeben. Zur Aktivierung des alten Exports in der Datei .jameica/cfg/de.jost\_net.JVerein.gui.control.MitgliedControl.properties eine Zeile mit "auswertung.csv.kompatibilitaet=true" einfügen
* Neu: PDF-Liste der Buchungsarten
* Buchungsarten kann jetzt auch die Eigenschaft "Spende" gegeben werden.
* Unterstützung für das neue jameica.ical-Plugin. Installation siehe [http://jameica.berlios.de/doku.php?id=support:install:jameica.ical](http://jameica.berlios.de/doku.php?id=support:install:jameica.ical)
* Vereinheitlichung im Umgang mit den Variablen bei Formularen. Neue Variablennamen. Teilweise wurden die Werte konvertiert, teilweise muss von Hand nachgebessert werden. An den meisten Stellen stehen jetzt sämtliche Daten des Mitglieds, Eigenschaften und Zusatzfelder zur Verfügung.
* Neu: Funktion zur gleichzeitigen Zuordnung einer Eigenschaft an viele Mitglieder
* &gt;Neu: Spendenbescheinigung aus dem Mitgliedskonto \(Automatische Spendenbescheinigung\)
* Neu: Standardformular für Spendenbescheinigungen
* Neu: Spendenbescheinigung für Sachspenden
* Neu: Neues Abrechnungsmodul. Damit ist es möglich, mit dem Parameter "kompakte Abbuchung" mehrere Abbuchungen von einem Konto zu einer Abbuchung zusammenfassen. Die interne Struktur des Moduls musste generell überarbeitet werden. Daher ausgiebig testen. Das neue Modul steht zunächst über den Parameter "Test neue Abbuchung" zur Verfügung.
* Das Datum der letzten Änderung wird bei Mitgliedern und Adressen gespeichert. Die Anzeige erfolgt in der Trefferübersicht. Dazu muss unter Administration\|Einstellungen\|Tabellen das entsprechende Häkchen gesetzt werden.
* Beim Versand von Mails können die Zusatzfelder mit $zusatzfeld.ZUSATZFELDNAME ausgegeben werden.
* Manuelle Zahlungseingänge und Rechnungen \(bis 1.3\) entfernt.
* Bugfix beim Import von Zusatzfeldern. Bislang wurde nur der Datentyp "Zeichenfolge" korrekt importiert.
* Bugfix beim Import. Sortierung der Daten ist nicht mehr erforderlich.
* Mitgliedsstatus in die Mitgliedsauswertung aufgenommen.
* Zusatzbeträge: Bugfix bei Buchungen ohne Intervall wird jetzt das Fälligkeitsdatum korrekt behandelt.
* Personalbogen: Bugfix Eigenschaften.
* Abbuchung: Verwendungszweck 2 ist jetzt auch 27 Zeichen \(vorher 25 Zeichen\) lang
* Mitgliedskonto: Bugfix Summen
* Bugfix bei der Erfassung von Buchungen \(Vorgabe Konto\). [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=17827&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=17827&group_id=7335)
* Tastatursteuerung wegen Problemen mit Jameica/Hibiscus wieder entfernt.
* Bugfix in der Altersstatistik. Über 100-jährige wurden in der Summe nicht berücksichtigt.Siehe [http://www.jverein.de/forum/viewtopic.php?f=5&t=339](http://www.jverein.de/forum/viewtopic.php?f=5&t=339)
* In den Einstellungen im Tab Anzeige kann jetzt die Verzögerungszeit für die Suchfelder Name, Vorname und Strasse der Mitglieder und Adressen eingestellt werden.
* Mailversand: Unterschiedliche Mitglieder können mit gleicher Adresse angeschrieben werden.
* Bugfix: Änderungen an den Einstellungen werden sofort wirksam.
* Bugfix: Bei den Spendenbescheinigungen wird der Betrag wie in der Vorschau positioniert.
* Warnung bei der Neuaufnahme von Arbeitseinsätzen, Lehrgängen, Wiedervorlagen und Zusatzbeträgen, wenn das neue Mitglied noch nicht gespeichert ist.
* Colins Patch zur MySQL-Performancesteigerung.
* Bugfix bei der Umschlüsselung eines Mitgliedes von einer Beitragsart mit der Art Familie/Angehöriger in eine andere Beitragsart.
* Bugfix Diagnose-Backup
* Liste Zusatzbeträge: Sortierung nach Namen aufgenommen. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=17793&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=17793&group_id=7335)
* Lehrgangsart in die Übersicht aufgenommen.
* Vermeidung NPE bei der Erfassung von Lehrgängen.
* Zusatzbeträge: In den Verwendungszweck können nur noch die für DTAUS zulässigen Zeichen eingegeben werden.
* Keine Abrechnung von Zusatzbeträgen bei ausgetretenen Mitgliedern
* Korrekte Sortierung von Ganzzahl-Zusatzfeldern in der Mitgliederübersicht.
* Neu: Filter für die Lehrgangsübersicht.
* Bugfix Abrechnung DTAUS mit äöüß größer 27 Stellen.
* Bugfix Zusatzbeträge nächste Fälligkeit.
* Bugfix Sollbuchung bearbeiten. Irrtümlich wurde generell der Default-Zahlungsweg vorgegeben.
* Selektion der Mitglieder \(Dialog und Auswertung\) nach Zusatzfeldern.
* Die Texte von Mails und Mailvorlagen können jetzt 10.000 Zeichen lang sein.
* Arbeitseinsätze werden auf dem Personalbogen ausgegeben.
* Bugfix: Sortierung der Buchungen bleibt nach Bearbeitung der Buchungsart erhalten.
* Alternative Sortierung des Buchungsjournals nach Buchungsnummer
* Bei der Eingabe einer \(Ist-\)Buchung \(Barzahlung\) kann zunächst das Mitgliedskonto ausgewählt werden. Name und Vorname des Mitgliedes, Betrag und Verwendungszweck der Sollbuchung sowie das aktuelle Tagesdatum werden in die Buchung eingetragen.
* Neu: Istbuchung kann vom Mitgliedskonto gelöst werden.
* Änderung der Zuordnung des Hibiscus-Kontos zum JVerein-Konto ermöglicht.
* Mitgliederliste: Bugfix bei der Sortierung nach Namen und Vornamen
* Korrektes Encoding beim Mailversand unter Ubuntu
* Buchungstext2 für Zusatzbeträge.
* Jahressaldo: Bugfix abweichendes Geschäftsjahr.
* Neu: Bei der Erstellung von Rechnungen können Abbucher ausgeschlossen werden.
* Bei der Erfassung der Mails kann mit einem Rechtsklick auf eine Mail-Adresse ein Dialog mit einer Liste aller Variablen angezeigt werden.
* Zusätzliche Variablen: mitglied\_anrede\_foermlich und mitglied\_anrede\_du
* Abrechnung: Bugfix Textschlüssel bei Hibiscusbuchungen
* Korrekte Darstellung von Buchungen in der globalen Suche.
* Buchung zum Mitgliedskonto zuordnen: Spezialsuche bei Namen mit Namensvorsätzen \(von, di, de ...\)
* In der Datenbank den Datentyp für booleans von char\(5\) auf boolean \(H2\) bzw. tinyint \(MySQL\) umgestellt.
* Foreign Key Arbeitseinsatz-&gt;Mitglied aufgenommen.
* Bei Zusatzbeträgen und Wiedervorlagen Button zum Mitglied eingebaut. [http://www.jverein.de/forum/viewtopic.php?t=583&p=2246\#p2246](http://www.jverein.de/forum/viewtopic.php?t=583&p=2246#p2246)

### Version 1.4.0 vom 10.11.2010

* Box der aktuellen Geburtstage: Durch Doppelklick kann das Mitglied direkt bearbeitet werden.
* Das Kontextmenü steht ebenfalls zur Verfügung.Zusätzlich Telefonnummern und Email-Adresse aufgenommen.
* Scrollbar f. Buchung aufgenommen.
* Größe der Kontoauswahlbox der Buchführung verändert.
* Bugfix beim Import des Zahlungsrhytmusses
* Erste Version des Mitgliedskontos
* Rechnungen: Für ein Mitglied werden ggfls. mehrere Positionen auf eine Rechnung zusammengefasst. Achtung! Die Formularfelder "Zahlungsgrund1" und "Zahlungsgrund2" sind durch das Formularfeld "Zahlungsgrund" zu ersetzen.
* Im Formularfeldeditor kann jetzt auch direkt das Formular angezeigt werden.
* Featurerequest [http://developer.berlios.de/bugs/?func=detailbug&bug\_id=17284&group\_id=7335](http://developer.berlios.de/bugs/?func=detailbug&bug_id=17284&group_id=7335)
* Unter Einstellungen&gt;Rechnungen können die Texte eingegeben werden. Beim Text für die Abbuchung können die Variablen ${Konto} und ${BLZ} in den Text eingemischt werden.
* Bugfix: Abgeschlossene Buchungen können nicht mehr gelöscht werden.
* Optimierung der Bedienung per Tastatur. Siehe auch [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=17221&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=17221&group_id=7335)und [http://www.jverein.de/forum/viewtopic.php?f=1&t=143](http://www.jverein.de/forum/viewtopic.php?f=1&t=143) Tastaturbedienung
* Foto des Mitglieds kann gespeichert werden.
* Ausdruck von Personalbögen mit allen Daten eines Mitgliedes.
* Buchungen werden bei der Sortierung nach ID jetzt numerisch sortiert. Siehe auch [http://www.jverein.de/forum/viewtopic.php?f=5&t=182&p=731\#p731](http://www.jverein.de/forum/viewtopic.php?f=5&t=182&p=731#p731)
* Eigenschaftengruppen können jetzt das Merkmal 'Pflicht' haben. Dann muss mindestens eine Eigenschaft ausgewählt werden. Siehe auch [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=17217&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=17217&group_id=7335)und [http://www.jverein.de/forum/viewtopic.php?f=1&t=142](http://www.jverein.de/forum/viewtopic.php?f=1&t=142)
* Mitgliederliste im PDF-Format: Ausgabe der Eigenschaften.
* Buchführung: Überall, wo ein Bankkonto auszuwählen ist, wird das zuletzt genutzte vorgegeben.
* Bugfixes bei der Erstellung des Diagnose-Backups.
* Maximale Länge des Textes für Mails und Mailvorlagen auf 10.000 Zeichen verlängert.
* Bei der Erstellung eines Jahresabschlusses werden jetzt die Anfangsbestände des Folgejahres eingetragen. Bei der Löschung von Jahresabschlüssen werden die Anfangsbestände des Folgejahres gelöscht. Siehe auch [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=16845&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=16845&group_id=7335)
* Länge der Kontobezeichnung auf 255 Zeichen verlängert.
* Hibiscus-Import der Konten checkt jetzt auf doppelte Konten.
* Ausgabe der Zusatzbuchungen im PDF-Format. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=17513&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=17513&group_id=7335)
* Datenimport: Klare Fehlermeldung bei korrupter Import-Datei im Bereich der Eigenschaften. Patch von Umbilo.
* Datenimport: Eigenschaftengruppen können jetzt auch importiert werden.
* Buchungen können die Kontoauszugsinformationen \(Auszug, Blatt\) en bloc zugewiesen werden.
* Vermeidung NullPointerException bei der Suche nach Kursteilnehmern.
* Intern: Hilfe in die Views verlagert
* Import Hibiscus-Konten: Check auf doppelte Konten
* Bei der Neuaufnahme einer manuellen Buchung wird sofort nach der Speicherung die ID angezeigt.
* Korrekter Hinweis auf fehlende Stammdaten bei der Abrechnung.
* Buchung: Dropdown-Liste Buchungsart alphabetisch sortiert
* Import: Vermerk1 und Vermerk2 können jetzt importiert werden.
* Mitglieder im Ausland: Unter Einstellungen kann jetzt ein entsprechendes Häkchen gesetzt werden. Anschließend kann der Staat beim Mitglied erfasst werden.
* Sterbetag aufgenommen.
* Bugfix bei leerer/neuer Datenbank.
* Zusatzbeträge-Import: Im Fehlerfall wird der Name des Mitglieds mit ausgegeben.

### Version 1.3.2 vom 18.05.2010

* Bugfix bei der Behandlung ausgetretener Mitglieder

### Version 1.3.1 vom 16.05.2010

* Zusätzliche Prüfung der Bankverbindung bei der Abrechnung
* Fehlendes Foreign-Key-Constraint Eigenschaften/Mitglied eingefügt.
* Bugfix Eigenschaften
* Aktuelle Geburtstage: Korrekte Behandlung ausgetretener Mitglieder
* Buchungsklassen-Saldo: Überschrift korrigiert.
* Programminterner einheitlicher Umgang mit ausgetretenen Mitgliedern
* Bugfix Einrichtung MySQL-Datenbank

### Version 1.3.0 vom 09.04.2010

* Abrechnung: Mitgliedsnummer in den Verwendungszweck aufgenommen.
* Bugfix beim Import des Eintrittsdatums.
* Adressbuchexport ins Mail-Menü verschoben.
* Mailfunktion um Dateianhänge erweitert.
* IBAN direkt bei der Eingabe von Kontonummer und BLZ berechnen
* Liste der Zusatzbeträge: true/false wird als X bzw. \_ dargestellt
* Mitgliedsdaten: Der zuletzt ausgewählte Tab wird bei Betätigung von "zurück" aktiviert.
* Erste Version eines einfachen Programms zum Versand von Mails.
* Standardwerte für Zahlungsweg und Zahlungsrhytmus bei der Neueingabe von Mitgliedern können unter Administration\|Einstellungen\|Beiträge eingestellt werden. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=16605&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=16605&group_id=7335)
* Spendenbescheinigung: Existierende Spendenbescheinigung kann als Vorlage für eine neue Spendenbescheinigung verwendet werden.
* Neu: Konkrete Fehlermeldung, wenn bei der Erstellung der Altersjubiläumsliste der Eintrag in den Stammdaten fehlt.
* Zusatzfeldern können jetzt Datentypen zugeordnet werden
* Zusatzfelder: Bei der Löschung einer Felddefinition wird nach Rückfrage auch der Inhalt der Datenfelder beim Mitglied gelöscht.
* Buchführung: Mehrere Buchungen können gleichzeitig gelöscht werden.
* Buchführung: Mehrfache Buchungsübernahme verhindert.
* Bugfix beim Austritt aller Mitglieder einer Familie \(Familienbeitrag\)
* Bugfix fehlerhafte Kontonummer bei der Eingabe und bei der Abrechnung
* Bei Manuellen Zahlungseingängen gibt es jetzt Mehrfachselektion. [http://developer.berlios.de/bugs/?func=detailbug&bug\_id=16431&group\_id=7335](http://developer.berlios.de/bugs/?func=detailbug&bug_id=16431&group_id=7335)
* Neu: Eigenschaften können jetzt in Eigenschaftengruppen zusammengefasst werden.
* Eigenschaften können importiert werden. [https://developer.berlios.de/bugs/?func=detailbug&group\_id=7335&bug\_id=16162](https://developer.berlios.de/bugs/?func=detailbug&group_id=7335&bug_id=16162)
* DB-Update restore: Meldung bei nicht leerer Datenbank
* Mitglied: Anzeige IBAN
* Neu: Import von Zusatzbeträgen. Sowohl Default-Format als auch individuelle Formate. [https://developer.berlios.de/bugs/?func=detailbug&group\_id=7335&bug\_id=16336](https://developer.berlios.de/bugs/?func=detailbug&group_id=7335&bug_id=16336)
* Die Art der Buchungsart \(Einnahme, Ausgabe, Umbuchung\) wurde bei der Bearbeitung generell auf Einnahme gesetzt.
* Lauffähigkeit mit den aktuellen Nightly-Builds von Jameica 1.9 und Hibiscus 1.11 hergestellt.
* Vermeidung NullPointerException beim Jahressaldo.
* Neu: Buchungsklassen zur Zusammenfassung von Buchungsarten. siehe auch [Zusammenhänge](http://www.jverein.de/wiki/index.php?title=Zusammenh%C3%A4nge).
* Neu: Buchungsjournal, Feature Request [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=16103&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=16103&group_id=7335)
* Auswertung Mitglieder: Mitglieder mit Austrittsdatum in der Zukunft werden mit ausgewertet. Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=16223&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=16223&group_id=7335)
* Bugfix beim Import des Feldes Zahlungsrhytmus.

### Version 1.2.0 vom 23.08.2009

* Bugfix beim Import von Mitgliedern mit dem Zahlungsweg "Barzahlung"
* Bugfix bei den Abrechungen. Überlange Namen.
* Bugfix bei den Abrechungen. Spezialfall mehrere Fälligkeiten im Jahr und gleichzeitig beitragsfreie Beitragsgruppe.
* Neue Box "aktuelle Geburtstage". Wird unter dem Menüpunkt Jameica mit dem Button "Startseite anpassen" aktiviert.
* Bugfix bei der Erstellung von Rechnungen
* Mitglied: Zahlungsdaten in eignen Tab verschoben. Platzoptimierung
* Bessere Fehlermeldung bei der Löschung von Beitragsgruppen, denen noch Mitglieder zugeordnet sind. Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=16223&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=16223&group_id=7335)
* Bei der Auswahl des Geschlechts werden jetzt die Langtexte männlich und weiblich angezeigt.
* Bugfix FirstStart: Jetzt wird auch die Existenz von Beitragsgruppen abgefragt
* Die Menüpunkte von Plugins&gt;JVerein ins Hauptmenü kopiert
* Mitglied: Name, Vorname und Straße als Suchfelder \(Auto-Vervollständigung\)
* Bugfix: Löschen von Mitgliedern mit Zusatzfeldern.
* Neu: Juristische Personen \(Firmen, Organisationen, Behörden\) können als Mitglied gespeichert werden.
* Neu: [Lehrgänge](http://www.jverein.de/wiki/index.php?title=Lehrg%C3%A4nge)
* Zusätzliche Felder zur Rechnungserstellung. Siehe [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=15062&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=15062&group_id=7335)
* Bugfix "Fehler nach Löschung einer Beitragsgruppe". [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=15301&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=15301&group_id=7335)
* Mitgliederstatistik: Bugfix Altersgruppen und Berücksichtigung des Eintrittsdatums.
* Konfiguration: EMail-Adresse kann als Spalte ausgewählt werden.
* Abrechnung: Formularwerte speichern und wiederherstellen.
* Anrede in die Spaltenauswahl aufgenommen.
* Bugfix Zusatzbeträge
* Silbentrennung in Reports aufgenommen
* Icons auf Buttons
* Spendenbescheinigung um 'Ersatz für Aufwendungen' erweitert
* Mitglieder ohne Eintrittsdatum werden jetzt berücksichtigt. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=15132&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=15132&group_id=7335)

### Version 1.1.1 vom 19.01.2009

* Unter MySQL kam es zu einem Fehler beim Löschen von Zusatzfeldern. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=15024&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=15024&group_id=7335)
* Mehreren Buchungen kann gleichzeitig eine Buchungsart zugeordnet werden.
* Abrechnung erfolgt irrtümlicherweise auch für ausgetretene Mitglieder \(da hatte ich einen Bug entfernt und gleichzeitig einen neuen eingebaut ;-\) [http://developer.berlios.de/bugs/?func=detailbug&bug\_id=14996&group\_id=7335](http://developer.berlios.de/bugs/?func=detailbug&bug_id=14996&group_id=7335)
* Rechnungen auch für Zusatzbeträge
* Beim Löschen von Rechnungen wurde eine NullPointerException geworfen. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=14989&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=14989&group_id=7335)
* Icons auf 16x16 Pixel skaliert. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=14979&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=14979&group_id=7335)
* Fehlende Icons in Kontextmenüs ergänzt. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=14980&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=14980&group_id=7335)
* Summenzeilen in der Buchungsliste korrekt ausgeben. [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=14978&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=14978&group_id=7335)
* Anpassung an neue Jameica-Versionierung.

### Version 1.1.0.1 vom 29.12.2008

* Korrekte Verarbeitung wenn Eintritts- und/oder Geburtsdatum des Mitglieds fehlen. [http://developer.berlios.de/bugs/?func=detailbug&bug\_id=14975&group\_id=7335](http://developer.berlios.de/bugs/?func=detailbug&bug_id=14975&group_id=7335)
* Bugfix Foreign Key unter MySQL
* Bugfix Formularanzeige
* Bugfix Tabelle buchungsart für MySQL

### Version 1.1.0 vom 28.12.2008

* Bugfix Booleans aus MySQL-DB lesen
* About-Dialog gibt jetzt auch Build-Datum und -Nummer aus.
* JVerein prüft, ob die passende Jameica-Version installiert wurde.
* Bei Altersjubiläen wird jetzt das Geburtsdatum anstatt des Eintrittsdatums ausgegeben.
* Vermeidung von NullpointerExceptions nach Import von leeren Kommunikationsdaten
* Zusatzabbuchungen-&gt;Zusatzbetrag
* Icons ins Menü und in die Kontextmenüs aufgenommen.
* Telefonnummern auf 20 Stellen verlängert.
* Bugfix MySQL-Support.
* Bugfix Fälligkeitsberechnung Zusatzabbuchungen
* Bugfix Import: Adressierungszusätze
* Bugfix Dropdown-Box Zahlungsweg
* Abrechnung: Mitglieder mit einem Eintrittsdatum in der Zukunft bleiben unberücksichtigt.
* Abrechnung: Beim Beitragsmodell 'monatlich mit monatl., viertel-, halb- oder jährlicher Zahlungsweise' wird jetzt auch 'eingetretene Mitglieder' angeboten.
* Bug im Zusammenhang mit Drop-Down-Boxen gefixed.
* Redaktionelle Änderung an der Buchungsliste.
* Handy in den CSV-Export aufgenommen.
* Buchungen der Buchführung um Auszugs- und Blattnummer erweitert.
* Spalten der Mitgliederübersicht sind jetzt konfigurierbar. Die Konfiguration für alle Übersichten ist vorgesehen und wird später realisiert.
* Bugfix: Für die Auswertung Zusatzabrechnungen erfolgt jetzt auch der Aufruf des Anzeigeprogrammes.
* Verschiebung der Speicherung der Programmeinstellungen von einer Property-Datei in die Datenbank zur Vermeidung von Problemen in Multi-User-Umgebungen.
* Mitglied: Adressierungszusatz aufgenommen \(Mitgliedsdaten, PDF-Liste, CSV-Export, Import\)
* Einstellungen: Neu gruppiert und mit Scrollbars versehen.
* Mitglieder: Suche nach Geschlecht im Dialog und in den Auswertungen implementiert. Such-Masken 2spaltig formatiert.
* Kursteilnehmer können nach Namen oder Eingabedatum gefiltert werden.
* Abrechnungsinformationen können nach Datum oder Verwendungszweck gefiltert werden.
* Unter Plugins\|JVerein\|Erweitert kann jetzt ein Backup im XML-Format erzeugt und anschließend in eine leere Datenbank importiert werden. Benötigt Jameica-Nightly-Build &gt;= 30.9.2008
* Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=14496&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=14496&group_id=7335)gefixed.
* Beim Start wird geprüft, ob die korrekten Versionen von Jameica und Hibiscus installiert sind.
* Bei den Jubiläen können jetzt Altersjubilare ausgewertet werden. Unter Stammdaten werden die Geburtstage konfiguriert.
* Neu: Rechnung
* Abbuchung heißt jetzt Abrechnung.
* SearchProvider für die neue Jameica-Suchmaschine \(Mitglieder und Kursteilnehmer\)
* Neu: Formulare
* Neu: Spendenbescheinigung
* Bugfix beim CSV-Export mit leeren Zusatzfeldern
* PDF-Export der Buchungen jetzt entweder als Einzelbuchungen oder als Summen
* Optimierung der internen Reporter-Klasse
* Mitgliederliste auf den Reporter umgestellt. Kommunikationsdaten aufgenommen.
* Bugfix im Script zur Erzeugung der Datenbank
* Abbuchung: Fehlermeldungen von OBanToo werden an die Oberfläche gebracht
* Freigabe der Buchführung zum allgemeinen Test
* Neues Datenfeld zur Speicherung der Handy-Nummer des Mitglieds. Import angepasst.
* Bugfix: "von-Datum" bei der Abbuchung wird jetzt korrekt dargestellt
* Beim wiederholten Import werden jetzt alle notwendigen Tabellen gelöscht
* Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=13726&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=13726&group_id=7335)gefixed
* Bugfix NPE bei Zusatzfeldern
* Speicherung von Zusatzfeldern bei den Mitgliedern
* Länge des Feldes Titel auf 20 verlängert, Länge des Feldes PLZ auf 10 verlängert.
* Bugfix: Anzeige der Hilfe unter Windows.
* Scrollbars in der Mitglieder-Detail-Ansicht von Olaf übernommen. Neues Nightly von Jameica erforderlich.

### Version 1.0.0 vom 25.03.2008

* Import des Zahlungsrhytmusses implementiert.
* Neu: In die Jameica-Startseite kann eine Übersicht über die Wiedervorlagen eingeblendet werden.
* Die Statistik bezieht sich jetzt auf einen Stichtag. Mitglieder, die nach dem Stichtag ausgetreten sind, werden noch als Mitglieder gewertet.
* In der Statistik wird jetzt die Anzahl der Anmeldungen und Abmeldungen zwischen dem 1.1. und dem eingegebenen Stichtag ausgegeben.
* Bei der Abbuchung kann jetzt die DTAUS-Datei ins PDF-Format konvertiert werden.
* PDF-Dokumentation durch Link zu diesem Wiki ersetzt.
* Neu: Jubiläumsliste
* Direkte Übernahme der Lastschriften als Einzel- oder Sammellastschriften in Hibiscus.
* Bei den &lt;a href="administration\_einstellungen.php"&gt;Einstellungen&lt;/a&gt; können jetzt Dateinamenmuster vorgegeben werden. Dieses Muster wird bei der Erzeugung von Dateinamen verwendet.
* Erweiterung um Hilfefunktion.
* Bei Neuinstallationen wird jetzt standardmäßig die H2-Datenbank installiert.
* Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=12860&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=12860&group_id=7335)gefixed
* Zu jedem Mitglied können Eigenschaften gespeichert werden. Diese Eigenschaften können im Dialog und bei der Auswertung in die Selektion einbezogen werden. Siehe [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=12862&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=12862&group_id=7335)
* Erweiterung der Filterkriterien bei der Mitgliedersuche.
* h2.jar entfernt. Wird durch Jameica mitgeliefert.
* MySQL-Support von Michael Trapp übernommen.
* Bei der Abbuchung wird jetzt ein Stichtag abgefragt. Dieser Stichtag wird zur Prüfung herangezogen, ob ein ausgetretenes Mitglied noch zahlen muss. Siehe [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=12861&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=12861&group_id=7335)
* Bei der Abbuchung können jetzt die Jahres-, Halbjahres- und Vierteljahresabbuchungen auch separat ausgeführt werden. Siehe [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=12861&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=12861&group_id=7335)und [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=13021&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=13021&group_id=7335)
* Bugfix bei der Berücksichtigung des Austrittsdatums bei der Mitgliederauswertung.
* Bugfix bei der Abbuchung: Zusatzabbuchung und Kursteilnehmer nur abbuchen, wenn entsprechendes Häkchen gesetzt ist.
* MySQL-Treiber entfernt. Wird jetzt von Jameica mitgeliefert.
* CSV-Export erweitert um die Bezeichnung der Beitragsgruppe.
* Bugfix: Bei der Mitgliedersuche wurden auch Eintritts- und Austrittsdaten der Auswertung berücksichtigt.
* Workaround f. Bug in Jameica

### Version 0.9.4 vom 16.12.2007

* Bugfix Update-Mimik/Migration. Update und Migration 'überholten sich'.

### Version 0.9.3 vom 03.12.2007

* Deployment-Bug: Es wurde nicht alles komplett ausgeliefert.

### Version 0.9.2 vom 02.12.2007

* Mitgliedersuche: Einschränkung auf angemeldete oder abgemeldete Mitgliedschaft
* Umstellung auf die H2-Datenbank
* Bugfix bei Zusatzabbuchungen ohne Interval
* Dokumentation: SPG-Export-Hardcopy auf Forderung von SPG durch textuelle Beschreibung ersetzt.
* Wegfall der Einstellung "Standardtab bei Mitgliedersuche". Es wird immer der zuletzt ausgewählte Tab angezeigt.
* Neu: Geburtstagsliste bei der Auswertung der Mitglieder
* Intern: Neue Mimik für das Update der Datenbankstruktur
* Neues Beitragsmodell
* Bugfix wiederkehrende Zusatzabbuchungen

### Version 0.9.1 vom 04.09.2007

* Beschränkung der Länge des Vereinsnamens auf 27 Stellen wegen Problemen mit der Abbuchung
* Bugfix bei der Abbuchung, wenn es keine beitragsfreie Beitragsgruppe gibt
* Neuer Konfigurationsbildschirm im Plugins-Menü: Es kann bestimmt werden, ob das Geburtsdatum und das Eintrittsdatum ein Pflichtfeld ist und ob die Reiter Kommunikationsdaten, Zusatzabbuchungen, Vermerke und Wiedervorlage sowie die Kursteilnehmer angezeigt werden.
* Einstellungsdialog erweitert um den Standard-Tab für die Mitglieder-Suche
* Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=11763&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=11763&group_id=7335)gefixed
* Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=11764&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=11764&group_id=7335)gefixed
* Bug [https://developer.berlios.de/bugs/?func=detailbug&bug\_id=11819&group\_id=7335](https://developer.berlios.de/bugs/?func=detailbug&bug_id=11819&group_id=7335)"gefixed
* Korrekte Anzeige der Pflichtfelder beim Mitglied. Achtung! Wer Wert auf dieses Feature legt, muss ein Jameica- Nighly-Build &gt;= 30.8.2007 einsetzen. Ansonsten werden BLZ und Kontonummer nicht als Pflichtfeld angezeigt.
* Mitglieder können jetzt über das Context-Menü bearbeitet und gelöscht werden
* Beitragsgruppen können jetzt über das Context-Menü mit einem rechten Mausklick oder einen Button gelöscht werden.

### Version 0.9.0 vom 20.07.2007

* Überprüfung der Datenbank-Struktur beim Startup.
* Wiederkehrende Zusatzabbuchungen
* Bei der Neuerfassung von Mitgliedern wird nach der Eingabe der PLZ der Ort automatisch ermittelt, sofern er bereits bei mindestens einem Mitglied gespeichert ist
* Bugfix in der SQL-DDL-Update-Routine
* Vermeidung ClassNotFoundException
* Bugfix bei der Abbuchung mit mehr als einer beitragsfreien Beitragsgruppe
* Neu: Wiedervorlagetermin bei jedem Mitglied und Übersicht über alle Termine
* Neu: Auswertung Kursteilnehmer
* Bugfix: Stammdatenverwaltung
* Neu: Handbuch im PDF-Format
* Neu: Handbuch kann über Plugins\|JVerein\|Handbuch aufgerufen werden

### Version 0.7.0 vom 27.03.2007

* Zeit-Optimierung bei der Anzeige der Mitglieder-Suche
* Neu: Bei der Suche der Mitglieder gibt es jetzt einen Tab mit allen Mitgliedern
* Kursteilnehmer: Abbuchungsdatum kann zurückgesetzt werden
* Beitragsgruppe: Beitragsart kann jetzt festgelegt werden
* Bugfix Import. Jetzt können, wie dokumentiert, beliebige Dateinamen verwenden werden
* Erweiterung Import um Zahlungsweg
* Zusätzliche Plausibilitätsprüfung der Import-Datei
* Herstellung von Familienverbänden für Familientarife
* Zusätzliche Plausi bei der Abbuchung

### Version 0.6.0 vom 18.03.2007

* Neu: Zahlungsweg beim Mitglied
* Neu: Tabelle zur Überwachung der manuellen Zahlungseingänge
* Bugfix: Bei der Abbuchung von Kursteilnehmern wird das Abbuchungsdatum jetzt korrekt gesetzt
* Anpassung an Jameica/Hibiscus: Kennzeichnung der Pflichtfelder

### Version 0.5.0 vom 10.03.2007

* Neu: Kursteilnehmer
* Bugfix Mitgliederstatistik. Nur aktive Mitglieder werden berücksichtigt.
* Randeinstellungen der Mitgliederliste geändert.
* Konfiguration aus dem Extras-Menü zur Jameica-Konformität in das Plugins-Menü am oberen Rand verschoben
* Buchführung entfernt. Mit dem aktuellen Nightly-Build von Jameica und Hibiscus kann diese Aufgabe viel besser erledigt werden
* Zusätzliche Vermerkfelder bei den Mitgliedern

