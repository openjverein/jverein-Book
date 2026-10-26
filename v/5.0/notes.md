# Release Notes

## Allgemeines

Die Version 5.0 ist eine Major Version und nicht rückwärts kompatibel mit einer 4.x.

Man kann also mit einer migrierten Datenbank nicht mehr auf eine ältere Version von JVerein zurück. Es empfiehlt sich ein Backup der Datenbank vor dem Update anzulegen. Mit diesem kann auch wieder eine ältere Version benutzt werden.

Gründe für die Inkompatibilität:
* Für die Belegverwaltung musste die Datenbank Struktur geändert werden


## The Big Ones

### Lokale Dokumentspeicherung

Neben der Speicherung von Dokumenten über Jameica Messaging (bisherige Methode) kann in den Einstellungen diese Option abgewählt werden. Dann erfolgt die Speicherung der Dokumente lokal.

Unter Administration->Einstellungen->Belege können die Wurzelverzeichnisse für die Dokumentspeicherung gesetzt werden. Diese können geändert werden wenn die Dokumente verschoben werden bzw. auf einen anderen Benutzer übertragen werden. Die Verzeichnisse stehen nicht in der Datenbank sondern sind lokal gespeichert.

Unter Administration->Einstellungen->Vorlagen lassen sich die relativen Pfade für die Belege mit Variablen definieren. Ein Beleg wird unter dem  Wurzelverzeichnis und dem relativen Pfad zusammengesetzt.


### Belegverwaltung

 Alle hinterlegten Belege werden in einem neuen View (Buchführung->Belege) angezeigt. Hier gibt es auch eine Filter Möglichkeit.
 
Belege (Dokumente) lassen sich bei den Buchungen und Mitgliedern erstellen aber auch direkt aus der Anzeige der Liste. Erstellte Belege lassen sich auch nachträglich einer Buchung bzw. einem Mitglied zuordnen. Es ist z.B. auch möglich, einen Beleg mehreren Buchungen zuzuordnen. Ein Beleg kann auch von einer Buchung entfernt werden ohne ihn zu löschen.


## Kleinere Korrekturen, Erweiterungen oder Modifikationen

### Weitere PDF Export Optionen

Im Export Dialog für PDF Reports gibt es einen neuen Reiter "Optionen". Er wird nur angezeigt wenn auch eine Option für den Report vorhanden ist.

Dieser bietet folgende Schalter:
* Filterparameter ausgeben: Für Reports die gefilterte Tabellen ausgeben, kann ausgewählt werden ob am Ende des Reports eine Tabelle mit den aktiven Filtern ausgegeben wird. Die Tabelle wird nur gezeichnet wenn auch mindesten ein Filter aktiv ist
* Zeige Kontonummer in Buchungsliste: Diese Option wird bei, Buchungsexport "PDF Einzelbuchungen" angeboten
* Wirtschaftsplan Ist-Beträge von laufendem Zeitraum ausgeben: Diese Option wird beim PDF Export der Wirtschaftspläne angeboten

### Gesperrt Spalte

Bei Tabellen gibt es eine neue Spalte "Gesperrt" bzw. "Abgeschlossen". Sie ist standardmäßig ausgeblendet. Sie zeigt ein Schlosssymbol wenn der Eintrag nicht gelöscht werden kann. 


## Sonstiges

* Bei Rechnungsformularen sind in den Variablen jetzt auch die Attribute des Zahlers verfügbar

