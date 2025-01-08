# Release Notes Version 2.9.0

## Allgemeines

Mit dieser Version wird die Versionsnummerierung auf die Art MAJOR.MINOR.PATCH umgestellt:
* MAJOR wird bei inkompatiblen API Änderungen hochgezählt
* MINOR wird bei neuer Funktionalität hochgezählt 
* PATCH wird bei Fehlerkorrekturen hochgezählt

Die Idee ist, zukünftig auch in kürzeren Abständen reine Bugfixes freizugeben bei denen keine neuen Funktionen enthalten sind.

Ab dieser Version wird auch eine für jede Version spezifische Dokumentation angelegt. Damit können Anwender einer älteren Version auf ihre passende Dokumentation zugreifen. Bisher war die Dokumentation immer nur für die neueste Version vorhanden.

## The Big Ones

### Rechnungen

TODO

### E-Rechnung

* Rechnungen werden jetzt im ZUGFeRD Format erstellt. Die generierte Rechnung im PDF Format enthält ein eingebettetes XML Dokument für die elektronische Verarbeitung der Rechnung

### Spendenbescheinigungen

* PDFs für Spendenbescheinigungen werden verschlüsselt und sind damit schreibgeschützt aber lesbar und druckbar
* Die gedruckte Unterschrift ist jetzt auch bei Spendenbescheinigung Formularen verfügbar. Sie kann als Formularfeld platziert werden
* Die gedruckte Unterschrift wird nur bei reinen Geldspenden ausgegeben. Sachspenden und Geldspenden mit Verzicht auf Aufwendungen müssen weiterhin laut steuerlichen Vorgaben per Hand unterschrieben werden

### Rücklagen Konten

Für die Konten wurden neu Kontentypen eingeführt:
* Rücklagenkonto nach § 62 Abs. 1 AO
* Vermögenskonto nach § 62 Ans. 3 und 4 AO
* Konto für sonstige Rücklagen

Damit kann ein Verein seine eingestellten Rücklagen in JVerein hinterlegen. Bucht ein Verein Rücklagen auf ein eigenes Bankkonto so ist dieses weiter als Geldkonto zu führen. Man könnte aber die Rücklagen zusätzlich in Rücklagenkonten führen um sie weiter aufzuschlüsseln. Auch werden die separaten Konten bei der Mittelverwendung benötigt.

Buchungen auf diesen Konten gehen nicht in das Buchungsklassensaldo und Kontensaldo ein, weil die Buchungen bereits in regulären Konten enthalten sind. Die Konten werden im Kontensaldo separat aufgelistet.

### Mittelverwendung

* Es gibt eine neue Ansicht "Mittelverwendung" (siehe [Mittelverwendung](buchf/mittelverwendung.md))
* Diese Funktionalität muss in Administration->Einstellungen->Anzeige aktiviert werden

## Sonstige Features

### Abrechnungsläufe

* Der Menüeintrag Abrechnung wurde aus dem Navigationsbaum entfernt. Ein Abrechnungslauf wird jetzt über den Button "Neu" im View der Abrechnungsläufe erstellt

### Hibiscus Buchungsimport

* Der Menüeintrag Hibiscus-Buchungen wurde aus dem Navigationsbaum entfernt. Die Import Funktion ist jetzt über den "Hibiscus Import" Button in der Buchungsliste verfügbar

### Variablen für Feldfunktionen

* In den Views für Mail, Mailvorlagen und Lesefeldern wird die Auswahl der Variablen und eine Vorschau unterstützt

### Abweichender Zahlungsweg bei Zusatzbeträgen

* Bei Zusatzbeträgen kann jetzt ein von der Standard Konfiguration beim Mitglied abweichender Zahlungsweg spezifiziert werden

### Sortierung von Tabellen

* In Tabellen konnte die Sortierung durch Klick auf einen Spaltenkopf geändert werden. Bei einer Änderung des Filters wurde beim Update der Tabelle die Sortierung bei den meisten Tabellen ignoriert. Jetzt wird die Sortierung überall beibehalten

### Rechnungen Löschen in der Funktion Datenbank Bereinigung

* In der Datenbank Bereinigung wurde die Option zum Löschen von Rechnungen eingefügt

### Eigenschaften bei Mitgliedern ändern

* Mit dem Eigenschaften Dialog beim Mitglied lassen sich jetzt auch Eigenschaften editieren die in einer Eigenschaften Gruppe mit Pflicht oder maximal 1 konfiguriert sind

### Export/Import von Formularen

* Formulare können jetzt als Ganzes (Formular Dokument und Formularfelder) exportiert und importiert werden

### Export der Liste der Spendenbescheinigungen

* Die Liste der Spendenbescheinigungen lässt sich als PDF und CSV ausdrucken

### Vor/Zurück Buttons im Filterbereich für Datumseingaben

* Mit den Vor/Zurück Buttons kann man den eingestellten Datumsbereich schnell vor und zurück blättern z.B. monatsweise

## Kleinere Korrekturen

* Prüfung ob das Mandatsdatum in der Zukunft liegt
* Das Datum der Gegenbuchung zu den Buchungen eines Abrechnungslaufes wird auf das Datum der Fälligkeit gesetzt
* Spendenbescheinigungen lassen sich auch für Buchungen aus abgeschlossenen Jahren erzeugen
* Die Details einer Lastschrift können angezeigt werden
* Beim Import von Zusatzbeträgen ist das Endedatum nun ein optionaler Parameter im CSV File
* Zusatzbeträge Import unterstützt jetzt auch den Zahlungsweg
* Zusätzlich gab es einige Fehlerkorrekturen

