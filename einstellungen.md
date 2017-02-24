# Einstellungen

## Allgemein

Name und Anschrift des Vereins sowie die Bankverbindung und Gläubiger-ID für die Abbuchung müssen hier eingegeben werden \(Pflichtangaben\).

Die Pflichtfelder werden von der Abrechnung für die Erstellung der Lastschriften zwingend benötigt. Die weiteren Angaben werden überwiegend bei Spendenbescheinigungen eingesetzt.

![](/assets/Einstellungenallgemein.png)

## Anzeige

![](/assets/Einstellungenanzeige.png)Durch die Einstellungen kann das Verhalten von JVerein beeinflußt werden.

Nach Änderungen der mit Stern gekennzeichneten Werte ist ein Neustart von Jameica erforderlich.



Folgende Einstellungen können vorgenommen werden:

### Geburtsdatum Pflichtfeld

Beim Mitglied muss ein Geburtsdatum eingetragen sein, damit der Datensatz gespeichert werden kann.

### Eintrittsdatum Pflichtfeld

Beim Mitglied muss ein Eintrittsdatum eingetragen sein, damit der Datensatz gespeichert werden kann.

### Sterbedatum

Das Eingabefeld für das Sterbedatum ist vorhanden und auswertbar

### Kommunikationsdaten anzeigen

Beim Mitglied können folgende Kommunikationsdaten gepflegt werden:

* private Telefonnummer
* Handynummer
* Dienstliche Telefonnummer
* E-Mail Adresse

### Zusatzbeträge anzeigen

Tab Zusatzabbuchungen beim Mitglied anzeigen. Impliziert, dass die Übersicht der Zusatzabbuchungen \(nicht\) angezeigt wird und die Option bei der Abbuchung \(in\)aktiv ist.

### Vermerke anzeigen

Tab Vermerke beim Mitglied anzeigen. Beim Mitglied können 2 mal 255 Zeichen Vermerke gespeichert werden.

### Wiedervorlage anzeigen

Tab Wiedervorlage beim Mitglied anzeigen. Impliziert, dass die Übersicht der Wiedervorlagen \(nicht\) angezeigt wird.

### Kursteilnehmer anzeigen

Kursteilnehmer ein-/ausblenden. Auswirkung auf die Abbuchung.

### Lehrgänge anzeigen.

Zu einem Mitglied können die durchgeführten Lehrgänge mit Ergebnissen gespeichert werden.

### Juristische Personen erlaubt.

Die Eingabe von Firmen, Organisationen und Behörden als Mitglieder wird erlaubt. Anstatt Name und Vorname werden Name-Zeile1 und Name-Zeile2 erfasst. Geburtsdatum und Geschlecht werden nicht erfasst.

### Mitgliedsfoto.

zu jedem Mitglied kann ein Foto gespeichert werden.

### Lesefelder anzeigen

Tab Lesefelder beim Mitglied anzeigen. Lesefelder können unter Administration - Lesefelder definiert werden

### Zusätzliche Adressen

In einem eigenen Dialog können weiteren Adressen von z.B. Spender, Lieferanten, Trainer gespeichert werden.

### Auslandsadressen

Beim Mitglied kann zusätzlich der Wohnsitz-Staat gespeichert werden

### Arbeitseinsatz

Beim Mitglied können Arbeitseinsätze erfasst werden. 

In einem eigenen Dialog können Buchungen von Arbeitsstunden angezeigt und geprüft werden.

### Dokumentenspeicherung

Speicherung von Dokumenten zu Mitgliedern und Buchungen. Wird diese Einstellung aktiviert muss das Plugin jameica.messaging installiert sein.

### individuelle Beiträge

Grundsätzlich zahlt das Mitglied den Beitrag, der in der Beitragsgruppe angegeben wurde. Sofern diese Option aktiviert wurde, kann bei jedem Mitglied ein abweichender individueller Beitrag angegeben werden.

### externe Mitgliedsnummer

Vereine, die auf Bundes- oder Landesebene organisiert sind und eine durchgängige Mitgliedsnummer verwalten möchten, können in JVerein eine externe Mitgliedsnummer speichern.

### Basis für Berechnung des Alters.

In der Ansicht Tabellen kann in der Mitgliederliste in einer Spalte das Alter angezeigt werden. Hier mit diesem Feld bestimmen Sie welches Referenzdatum bei der Berechnung des Alters verwendet wird.Zur Auswahl stehen:

* Aktuelles Datum. Das Alter berechnet sich aus dem Geburtsdatum und dem aktuellen Datum.
* Jahres Start. Das Alter berechnet sich aus dem Geburtstag und dem 01.01. des aktuellen Jahres.
* Jahres Ende. Das Alter berechnet sich aus dem Geburtstag und dem 31.12. des aktuellen Jahres.

### Buchungsart Auswahl

Hier kann eingestellt werden wie sich bei Buchungen das Feld für die Buchunsgart verhält:

Bei Suche bei Eingabe tippt man den Wortteil der Bezeichnung der Buchungsart ein, nach ein paar Millisekunden wird einer Auswahlliste mit den Treffern angezeigt aus der man dann die gewünschte Buchungsart übernehmen kann.

Anzeige der kompletten Liste stellt eine Drop-Down-Liste mit allen Buchungsarten zur Verfügung.

### Buchungsart Sortierung

Wie sollen die Buchungsarten sortiert werden: nach Bezeichnung, nach Nummer oder nach Bezeichnung/Nummer.

## Beiträge

![](/assets/Einstellungenbeitraege.png)

Beitragsmodell, siehe auch [Beitragsmodelle](/beitragsmodelle.md)

Die Standardwerte für den Zahlungsrhytmus und den Zahlungsweg bei der Speicherung neuer Mitglieder kann eingestellt werden.

Für die SEPA-Konvertierung ist das SEPA-Land auszuwählen.

### Arbeitsstundenmodell

Mit dem Arbeitsstundenmodel wird die Buchung von Arbeitsstunden eingestellt.

Mögliche Werte sind:

#### Standardverfahren

Es können beim Erfassen der Arbeitsstunden nur positive Werte im Stundenfeld eingegeben werden.

#### negative Stunden erlaubt

Beim Erfassen der Arbeitsstunden vom Mitgliedern können im Stundenfeld positive und negative Werte eingetragen werden. Positive und negative Werte können sich gegenseitig aufheben. Negative Werte können die Gesamtschuld an Arbeitsstunden bei einem Mitglied erhöhen und zu einer höheren Buchung von Zusatzbeiträgen führen.

## Dateinamenmuster

![](/assets/Einstellungendateinamen.png)

Bei der Ausgabe von Dateien \(Abbuchung, Auswertungen...\) werden die Dateinamen nach dem vorgegebenen Muster aufgebaut. Es können zusätzliche, vom Betriebssystem unterstützte Zeichen, in das Muster aufgenommen werden. Bleibt das Muster leer, wird kein Vorschlag für den Dateinnamen angezeigt. Spendenbescheinigungen werden jeweils für den einzelnen Spender ausgestellt. Daher sollten zur leichteren Identifizierung Name und Vorname in den Dateinamen aufgenommen werden.

Folgende Variable stehen zur Verfügung:

* a$ : Aufgabe \(z. B. auswertung, abbuchung\)
* d$ : Aktuelles Datum
* s$ : Sortierung. Wird nur bei Auswertungen gefüllt. Ansonsten leer.
* z$ : Aktuelle Zeit
* n$ : Name des Mitglieds
* v$ : Vorname des Mitglieds

Verzeichnis für CSV-Vorlagen.



