# Release Notes

## Allgemeines

Mit 3.0.0 wurde die Versionsnummerierung auf die Art MAJOR.MINOR.PATCH umgestellt:

* MAJOR wird bei inkompatiblen API Änderungen hochgezählt
* MINOR wird bei neuer Funktionalität hochgezählt
* PATCH wird bei Fehlerkorrekturen hochgezählt

Achtung: Nach einem Update der Datenbank auf eine höhere MAJOR Version kann diese Datenbank nicht mehr mit einer früheren MAJOR Version benutzt werden.

## The Big Ones

### Wirtschaftsplanung

* Es gibt eine neu Funktionalität für die Wirtschaftsplanung
* Damit können Plandaten für die Geschäftsjahre gepflegt werden

### Spendenbescheinigungen

* Sachspendenbescheinigung können jetzt auch nur noch mit zugehöriger Buchung erstellt werden
* Die Angaben zu Sachspende werden in der Buchung gemacht
* Dadurch können Sachspendenbescheinigungen auch automatisch erzeugt werden und es ist in den Menüs keine Unterscheidung zwischen Geldspende und Sachspende mehr nötig (siehe [Spendenbescheinigungen](../4.0/mitglieder/spendenbescheinigung.md))

### Editierbare Dateinamen

* Für Dateinamen existieren Vorlagen die editiert werden können
* Damit lassen sich Namen individuell mit Variablen anpassen (siehe [Vorlagen](administration/einstellungen/vorlagen.md))

### Empfänger Liste Vorschau

* In den Druck und Mail Views gibt es einen neuen Button "Empfänger Liste"
* Es erscheint ein Dialog mit allen Empfänger Daten die gedruckt oder per Mail versendet werden

### Vor und Zurück Buttons

* In allen Detail Views gibt es die Buttons für die Vor und Zurück Navigation. Die Buttons sind verfügbar wenn ein Detail View aus einer Listenanzeige aufgerufen wird z.B. Buchungen aus der Buchungsliste
* Die Reihenfolge der Navigation entspricht der Sortierreihenfolge in der Liste aus der aufgerufen wurde

### Speichern und neu Button

* Der "Speichern und neu" Button ist jetzt für die meisten Detail Views verfügbar
* Der Button wird nur angezeigt wenn ein neuer Eintrag erzeugt wird
* Wird nur ein bestehender Eintrag editiert, dann ist der Button nicht verfügbar

### Einträge in Listen per Mehrfachauswahl löschen

* Bis auf Jahresabschluss und Abrechnungslauf können jetzt alle Listen Einträge per Mehrfachauswahl gelöscht werden
* Schlägt das Löschen bei einem Eintrag fehl, wird trotzdem bei den anderen weiter gemacht
* Im Status Fenster welches bei Mehrfachauswahl angezeigt wird, werden Informationen zum Löschvorgang ausgegeben

### Wiedervorlage Box

* Beim Start von JVerein wird im Willkommen Fenster eine Info Box mit fälligen Wiedervorlagen eingeblendet falls welche existieren

### Überprüfung der Datenbank Version

* Beim Start von JVerein wird überprüft, ob die MAJOR Version der Datenbank größer ist als die der gestarteten JVerein Version
* Ist dies der Fall, dann wird die Benutzung von JVerein gesperrt, da MAJOR Versionen nicht rückwärts kompatibel sind und es sonst zu Fehlfunktionen kommen wird

## Kleinere Korrekturen und Erweiterungen

### Einstellungen Allgemein

* Pflichtfelder aus Einstellungen Anzeige verschoben
* Pflichtfeld "Nicht-Mitglied Geburtsdatum" eingeführt"
* Pflicht Eigenschaften für Nicht-Mitglieder und Juristische Personen abwählbar

### Einstellungen Anzeige

* Layout verbessert
* Familienbeitrag und Zusatzfelder als neue Option für ihre Aktivierung eingeführt (Aktivierung nicht mehr implizit)
* Aktivierung von Anlagenkonten, Rücklagenkonten und Forderungen/Verbindlichkeiten Konten eingeführt
* Einige Konfigurationen welche die Anzeige betreffen aus Einstellungen Buchführung hier her verschoben

### Einstellungen Mitglieder Ansicht

* Anzahl Spalten für Lesefelder entfernt, da die Ansicht nun als Liste implementiert ist
* Option "Zeige Dokumente in Tab" eingeführt. Die Option ist nur verfügbar wenn Dokumentspeicherung aktiviert ist

### Einstellungen Abrechnung

* Die Option "Zusatzbeträge auch für Ausgetretene abrechnen" aus Einstellungen Anzeige hier her verschoben
* Die Option "Keine Istbuchung bei Lastschriften erzeugen" eingeführt

### Einstellungen Spendenbescheinigungen

* Default Formulare für Spendenbescheinigungen werden nun in diesem Dialog konfiguriert
* Damit können sie auch bei der automatischen Generierung über Kontextmenüs verwendet werden

### Lesefelder Liste View

* Der Lesefelder Liste View wurde neu implementiert und zeigt die Lesefelder in einer Tabelle so wie auch bei anderen Listen üblich

### Nicht editierbare Buchungen und Sollbuchungen

* Sind Sollbuchungen oder Buchungen nicht editierbar, dann werden jetzt auch die Eingabefelder gesperrt und nicht nur der Speichern Button

### Filter nach Differenz in Mitglieder und Nicht-Mitglieder Liste View

* Im Filter in der Mitglieder und Nicht-Mitglieder Liste gibt es einen neuen Tab mit den Filter Optionen für Differenz. Damit lässt sich z.B. nach Mitgliedern filtern die einen Fehlbetrag haben

## Sonstiges

* In der Liste der Buchungen gibt es eine Spalte Spendenbescheinigung
* Zusatzbeträge Import Fehlerbehandlung und Log Ausgabe verbessert
* Einige Fehler beim Mitglied Import behoben
* Die "Geprüft" Checkbox ist auch im Buchung Dialog verfügbar
* Dateinamen mit Leerzeichen beim CSV Import erlauben
* Erfolgsmeldung beim Mitglied Speichern
* Bei einigen Dialogen wie Beitragsgruppe, EigenschaftGruppe, Eigenschaft etc. wird beim Speichern auf Eindeutigkeit der Bezeichnungen geprüft und Pflichtfelder farbig markiert
