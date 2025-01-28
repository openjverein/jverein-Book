# Release Notes Version 3.0.0

## Allgemeines

Mit dieser Version wird die Versionsnummerierung auf die Art MAJOR.MINOR.PATCH umgestellt:
* MAJOR wird bei inkompatiblen API Änderungen hochgezählt
* MINOR wird bei neuer Funktionalität hochgezählt 
* PATCH wird bei Fehlerkorrekturen hochgezählt

Die Idee ist, zukünftig auch in kürzeren Abständen reine Bugfixes freizugeben, bei denen keine neuen Funktionen enthalten sind.

Ab dieser Version wird auch eine für jede Version spezifische Dokumentation angelegt. Damit können Anwender einer älteren Version auf ihre passende Dokumentation zugreifen. Bisher war die Dokumentation immer nur für die neueste Version vorhanden.

**Die Version 3.0.0 ist eine neue MAJOR Version und damit nicht kompatibel mit den Vorgängern. Ist man also auf diese Version umgestiegen kann man mit der migrierten Datenbasis nicht mehr zu einer älteren Version zurück wechseln.** 

**Es ist also empfohlen, eine Kopie der aktuellen Datenbank anzulegen. Will man später wieder auf die alte Version zurück, kann man die gesicherte Datenbank verwenden.**

## The Big Ones

### Rechnungen

In Version 3.0.0 von JVerein wurde das Konzept für Rechnungen komplett überarbeitet.

Rechnungen werden jetzt nicht mehr beim Drucken generiert, sondern werden wie Spendenbescheinigungen in der Datenbank gespeichert. Eine Rechnung ist dabei genau einer Sollbuchung zugeordnet. Um dennoch mehrere Forderungen wie z.B. Beiträge und Zusatzbeträge zu einer Rechnung zusammen fassen zu können wurde das Konzept der Sollbuchungspositionen eingeführt.

In einem Abrechnungslauf lassen sich jetzt Beiträge und Zusatzbeträge nicht nur für Lastschriften sondern auch für Sollbuchungen zusammen fassen. Die einzelnen Beiträge und Zusatzbeträge bilden dabei die Sollbuchungspositionen, wobei Positionen mit gleicher Buchungsart zu einer Position zusammen gefasst werden.

Die Sollbuchungspositionen werden dann als Rechnungspositionen in die Rechnung aufgenommen.

Siehe [Rechnung](mitglieder/rechnung.md).

### E-Rechnung

* Rechnungen werden jetzt im ZUGFeRD Format erstellt. Die generierte Rechnung im PDF Format enthält ein eingebettetes XML Dokument für die elektronische Verarbeitung der Rechnung

### Spendenbescheinigungen

* PDFs für Spendenbescheinigungen werden verschlüsselt und sind damit schreibgeschützt aber lesbar und druckbar
* Die gedruckte Unterschrift ist jetzt auch bei Spendenbescheinigung Formularen verfügbar. Sie kann als Formularfeld platziert werden
* Die gedruckte Unterschrift wird nur bei reinen Geldspenden ausgegeben. Sachspenden und Geldspenden mit Verzicht auf Erstattung von Aufwendungen müssen weiterhin, laut steuerlichen Vorgaben, per Hand unterschrieben werden
* Spendenbescheinigungen werden jetzt auf den Zahler ausgestellt. Zahlt z.B. ein anderes Mitglied (Vollzahler im Familienverband) oder ein alternativer Kontoinhaber den Beitrag oder Zusatzbeträge, so wird in der Sollbuchung neben dem Mitglied auch der Zahler gespeichert. Die Spendenbescheinigung für Buchungen, die dieser Sollbuchung zugewiesen sind, wird dann auf den eingetragenen Zahler ausgestellt und nicht mehr auf das Mitglied selbst

### Rücklagen Konten

Für die Konten wurden neue Kontoarten für Rücklagen und Vermögen eingeführt.

Damit kann ein Verein seine eingestellten Rücklagen in JVerein hinterlegen. Bucht ein Verein Rücklagen auf ein eigenes Bankkonto so ist dieses weiter als Geldkonto zu führen. Man könnte aber die Rücklagen zusätzlich in Rücklagenkonten führen um sie weiter aufzuschlüsseln. 

Diese separaten Konten werden bei der Mittelverwendungsrechnung (siehe [Mittelverwendung](buchf/mittelverwendung.md)) benötigt.

Buchungen auf diesen Konten gehen nicht in das Buchungsklassensaldo und Kontensaldo ein, weil die Buchungen bereits in regulären Konten enthalten sind. Die Konten werden im Kontensaldo separat aufgelistet.

### Mittelverwendungsreport

* Es gibt eine neue Ansicht "Mittelverwendung" (siehe [Mittelverwendung](buchf/mittelverwendung.md))
* Diese Funktionalität muss in Administration->Einstellungen->Anzeige aktiviert werden

## Sonstige Features

#### Abrechnungsläufe

* Der Menüeintrag Abrechnung wurde aus dem Navigationsbaum entfernt. Ein Abrechnungslauf wird jetzt über den Button "Neu" im View der Abrechnungsläufe erstellt
* Der Dialog für den Abrechnungslauf wurde bezüglich der neuen Rechnung Funktionalität erweitert
* Bei einem Abrechnungslauf werden die Lastschrift Bedingungen geprüft. Es muss ein Lastschriftmandat vorhanden sein und falls das Mandat älter als 3 Jahre ist, müssen in den letzten drei Jahren Lastschriften durchgeführt worden sein. JVerein prüft hierzu ob entsprechende Lastschriften existieren. Wurden diese aber gelöscht oder ist man von einem anderen Tool nach JVerein gewechselt, dann gibt es hier noch keine Lastschriften, obwohl welche durchgeführt wurden. Mit der Option "SEPA-Check temporär deaktivieren" kann der Check dann temporär ausgeschaltet werden

#### Verrechnungskonto für Lastschriften

* Bei Lastschriften wird beim Abrechnungslauf für die erzeugten Buchungen nicht mehr das Konto aus den allgemeinen Einstellung des Vereins genommen. Es lässt sich jetzt unter Administration->Einstellungen->Abrechnung setzten

#### Hibiscus Buchungsimport

* Der Menüeintrag Hibiscus-Buchungen wurde aus dem Navigationsbaum entfernt. Die Import Funktion ist jetzt über den "Hibiscus Import" Button in der Buchungsliste verfügbar

#### Variablen für Feldfunktionen

* In den Views für Mail, Mailvorlagen und Lesefeldern wird die Auswahl der Variablen und eine Vorschau unterstützt

#### Abweichender Zahlungsweg bei Zusatzbeträgen

* Bei Zusatzbeträgen kann jetzt ein von der Standard Konfiguration beim Mitglied abweichender Zahlungsweg spezifiziert werden

#### Sortierung von Tabellen

* In Tabellen konnte die Sortierung durch Klick auf einen Spaltenkopf geändert werden. Bei einer Änderung des Filters wurde beim Update der Tabelle die Sortierung bei den meisten Tabellen ignoriert. Jetzt wird die Sortierung überall beibehalten

#### Rechnungen Löschen in der Funktion Datenbank Bereinigung

* In der Datenbank Bereinigung wurde die Option zum Löschen von Rechnungen eingefügt

#### Eigenschaften bei Mitgliedern ändern

* Mit dem Eigenschaften Dialog aus dem Kontextmenü von ausgewählten Mitgliedern lassen sich jetzt auch Eigenschaften editieren die in einer Eigenschaften Gruppe mit Pflicht oder maximal 1 konfiguriert sind

#### Export/Import von Formularen

* Formulare können jetzt als Ganzes (Formular Dokument und Formularfelder) exportiert und importiert werden

#### Export der Liste der Spendenbescheinigungen

* Die Liste der Spendenbescheinigungen lässt sich als PDF und CSV ausdrucken

#### Vor/Zurück Buttons im Filterbereich für Datumseingaben

* Mit den Vor/Zurück Buttons kann man den eingestellten Datumsbereich schnell vor und zurück blättern z.B. monatsweise

#### Filtermöglichkeiten beim Projekte Dialog

* In der Liste der Projekte (unter Administration->Buchführung) kann jetzt gefiltert werden

#### Erweiterter Filter im Buchungsarten Dialog

* In der Liste der Buchungsarten (unter Administration->Buchführung) gibt es weitere Filter Attribute

#### Eine Buchung mehreren Sollbuchungen zuordnen

* Es ist jetzt möglich im Dialog zur Zuordnung von Sollbuchungen mehrere Sollbuchungen auszuwählen. Die Buchung wird dann entsprechend der Sollbuchungspositionen in eine Splitbuchung umgewandelt. Die einzelnen Splitbuchungen werden dann zugeordnet


## Kleinere Korrekturen und Erweiterungen

* Prüfung ob das Mandatsdatum in der Zukunft liegt
* Das Datum der Gegenbuchung zu den Buchungen eines Abrechnungslaufes wird auf das Datum der Fälligkeit gesetzt
* Spendenbescheinigungen lassen sich auch für Buchungen aus abgeschlossenen Jahren erzeugen
* Die Details einer Lastschrift können angezeigt werden
* Beim Import von Zusatzbeträgen ist das Endedatum nun ein optionaler Parameter im CSV File
* Zusatzbeträge Import unterstützt jetzt auch den Zahlungsweg
* Zusätzlich gab es einige Fehlerkorrekturen
* In der Buchungsliste wir neben dem Gesamtbetrag auch das aktuelle Kontosaldo ausgegeben
* Bei allen Filterbereichen für Listen wurde in den Auswahlboxen das "Bitte auswählen" durch "Alle" ersetzt. Es muss ja nichts ausgewählt werden
* Die Drop Down Liste für Formulare ist jetzt sortiert
* Der Fehler bei der Abrechnung von Zusatzbeträgen wurde korrigiert
* Der Fehler in der Jahrgangsstatistik wurde korrigiert

