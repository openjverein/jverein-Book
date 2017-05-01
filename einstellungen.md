# Einstellungen {#einstellungen}

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

## Spendenbescheinigungen

![](/assets/Einstellungenspendenbescheinigungen.png)

Hier können die Werte zur Erstellung von Spendenbescheinigungen eingestellt werden.

Mindestbetrag: Es werden nur Spendenbescheinigungen für Einzelspenden ausgestellt, die diesen Betrag übersteigen.

Verzeichnis: In einem Durchlauf können mehrere Spendenbescheinigungen erstellt werden. Jede Spendenbescheinigung wird in ein eigenes Dokument ausgegeben und in das angegebene Verzeichnis gespeichert.

Buchungsart drucken: Im Normalfall wird der Verwendungszweck aus der Buchung in die Spendenbescheinigung übernommen. Sofern diese Option aktiviert wurde, wird der Text aus der Buchungsart genommen.

## Buchführung

![](/assets/Einstellungenbuchfuehrung.png)

Hier sind folgende Eingaben nötig bzw. möglich:

Beginn des Geschäftsjahres in der Form TT.MM.

Automatische Übernahme von Buchungen aus Hibiscus \(Standard: aktiviert\).

Unterdrückung nicht bebuchter Buchungsarten in Listen/Auswertungen \(Standard: nicht aktiviert\).

## Rechnungen

![](/assets/Einstellungenrechnungen.png)

Texte für die einzelnen Zahlungswege für den Rechnungsdruck. In den Text zur Abbuchung können die Variablen ${IBAN}, ${BIC}, ${MANDATID} ${Konto} und ${BLZ} eingemischt werden.

## Tabellen

![](/assets/Einstellungentabellen.png)

Festlegung der Spalten, die in Tabellen angezeigt werden sollen.

## Mail {#mail}

![](/assets/Mail-einstellungen-screenshot.png)

Alternativ zur EMail-Adresse kann auch der Name zur Absenderadresse hinzugefügt werden: "Mein Name &lt;vorstand@verein.de&gt;" Wichtig ist dabei das Format: \(Name\) \(Spitze Klammer auf\) \(Email\) \(Spitze Klammer zu\)

Hinweis: Die Passwörter werden aber JVerein 2.6.1 verschlüsselt in einer Jameica-Wallet-Datei abgelegt \(im Jameica Datenordner, Unterordner "cfg"\), und sind mit dem Jameica-Masterpasswort gesichert, das beim Starten von JVerein eingegeben wird.

Um versendete EMails auch im EMail-Postfach \(und nicht nur in JVerein\) abzulegen, gibt es zwei Möglichkeiten:

1. Eine Kopie \(Cc\) oder Blindkopie \(Bcc\) der EMail verschicken. Dazu das Feld "Immer Cc an Adresse" oder "Immer Bcc an Adresse" mit einer EMailadresse ausfüllen.
2. Die EMail in den "Gesendete"-Ordner eines ggf. vorhandenen IMAP-Kontos ablegen. Dazu den Bereich "IMAP 'Gesendete'-Ordner mit den IMAP-Zugangsdaten ausfüllen und "Kopie in 'Gesendete'-Ordner IMAP ablegen" anklicken. Der technische Name des "Gesendete"-Ordners kann variieren, ist aber meist "Sent".

Beide Möglichkeiten können auch kombiniert werden.

## Statistik

![](/assets/Einstellungenstatistik.png)

Für statistische Zwecke können Altersgruppen angegeben werden. Erfassen Sie die Gruppen wie im folgendem Beispiel

1-5,6-10,11-17,18-25,26-50,50-100

Zur Ausgabe einer Jubiläumsliste werden die Jubeljahre durch Komma getrennt eingetragen. Ohne Eingabe werden die Standardwerte 10,25,40,50 verwendet.

Es kann eine Liste der Altersjubilare ausgegeben werden. Ohne Eingabe werden die Standardwerte 50,60,65,70,75,80,85,90,95 verwendet.

Ab Version 2.5 gibt es das Feld Mindestalter f. Mitgliedschaftsjubiläum

Geben Sie hier eine Zahl ein, dann werden Mitgliedsjahre, die vor diesem Alter liegen beim Errechnen eines Mitglieds-Jubiläums nicht mit gerechnet.

Für weitere technische Details siehe: Informationen für Entwickler //TODO

