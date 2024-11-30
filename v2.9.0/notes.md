# Release Notes Version 2.9.0

## The big ones

### Rechnungen

TODO

### E-Rechnung

* E-Rechnungen können im ZUGFeRD Format erstellt werden

### Spendenbescheinigungen

* PDFs für Spendenbescheinigungen werden verschlüsselt und sind damit schreibgeschützt aber lesbar und druckbar
* Die gedruckte Unterschrift ist jetzt auch bei Spendenbescheinigung Formularen verfügbar. Sie kann als Formularfeld platziert werden
* Die gedruckte Unterschrift wird nur bei reinen Geldspenden ausgegeben. Sachspenden und Geldspenden mit Verzicht auf Aufwendungen müssen weiterhin laut steuerlichen Vorgaben per Hand unterschrieben werden
* Spendenbescheinigungen werden nicht mehr auf das Mitglied ausgestellt sondern auf den, der den Betrag bezahlt hat. Das ist relevant wenn bei einem Mitglied ein abweichender Kontoinhaber oder der Zahlungsweg durch Vollzahler eingestellt ist

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

## Kleinere Korrekturen

* Prüfung ob das Mandatsdatum in der Zukunft liegt
* Das Datum der Gegenbuchung zu den Buchungen eines Abrechnungslaufes wird auf das Datum der Fälligkeit gesetzt
* Spendenbescheinigungen lassen sich auch für Buchungen aus abgeschlossenen Jahren erzeugen
* Die Details einer Lastschrift können angezeigt werden

