# Formulare

## Allgemeines

In JVerein werden für [Spendenbescheinigungen](../../mitglieder/spendenbescheinigung.md), [Mahnung](../../druckmail/mahnungen.md), [Rechnungen](../../druckmail/rechnungen.md), [Pre-Notification](../../druckmail/pre-notification.md) und diverse Zwecke [Freie Formulare](../../druckmail/freiesformular.md) hinterlegt.

## Liste der Formulare

![](../../../../allgemeine-funktionen/administration/mitglieder/img/Formulare.png)

Mit Neu kann ein neues Formular eingerichtet werden.

Durch einen Doppelklick wird die Bearbeitung eines Formular eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Anzeigen: Das fertige Formular wird als PDF generiert und angezeigt
* Duplizieren: Es wird eine Kopie des Formulars erzeugt
* Löschen: Damit kann ein Formular, welches noch nicht verwendet wurde, gelöscht werden

## Formular

Über die Funktion Neu oder Bearbeiten wird ein Formular Dialog angezeigt.

Der Dialog beinhaltet die Formular Attribute und zeigt eine Liste der Formularfelder die auf die Datei Vorlage gedruckt werden sollen.

![](../../../../allgemeine-funktionen/administration/mitglieder/img/Formular.png)

## Formular Attribute

### Bezeichnung

Name des Formulars.

### Art

Art des Formulars. Es gibt an für welche Ausgabe das Formular verwendet werden kann. Optionen sind:

* Spendenbescheinigung
* Rechnung
* Mahnung
* Freies Formular
* Sammelspendenbescheinigung
* SEPA-Prenotification

### Datei

Hintergrund Datei für das Formular.

Man erstelle ein einfaches Dokument/Formular in Word, Open-/LibreOffice oder was auch immer (Dankeschönschreiben, Rundschreiben, whatsoever...) und lasse an den entsprechenden Stellen im Schreiben einfach leeren Platz (weisse unbeschriebene Stellen) als Platzhalter für die später von JVerein einzufügenden Daten.

Macht Euch hier genau Gedanken, wie Euer Formular aussehen soll und was Ihr später alles an Daten einfügen möchtet.

Bitte in der Textverarbeitungssoftware KEIN FORMULAR erstellen - nur einfach ein Dokument mit weißen/leeren Stellen als Platzhalter für später!! Das reicht.

Nun muss aus dem Dokument noch ein PDF gemacht werden. Das geht mit einem virtuellen PDF-Drucker (z.B. FreePDF XP oder PDFCreator) oder mit Adobe Acrobat (nicht mit dem Reader, der kann halt nur lesen :-) ) oder einfach in Open-/LibreOffice mit dem PDF-Export. Das fertige PDF (mit den weißen/leeren Stellen für die späteren Daten aus jVerein) hat keinerlei Funktionen eingebaut (keine Formularfelder, nur weiße/leere Stellen im Text an der richtigen Stelle).

Dann erstellt man in JVerein unter "Administration->Formulare" ein neues Formular. Dazu unten auf "neu" gehen, Bezeichnung und Art auswählen ("Art" gibt an, wann und wo dieses Formular in JVerein verfügbar sein wird).

Nun noch die gerade erstellte PDF-Datei auswählen und auf "speichern" klicken.

### Fortlaufende Nummer

Fortlaufende Nummer z.B. bei Rechnungen. Über das Feld lässt sich die Nummer zurücksetzen.

### Formularverknüpfung

Formulare können verknüpft werden um Abhängigkeiten untereinander aufzubauen. Die Spalte "Verknüpft mit" in der Formular-Übersicht zeigt die Abhängigkeiten an. Bei verknüpften Formularen werden die fortlaufenden Nummern (Formularfeld "zaehler") gleichgesetzt und untereinander aktualisiert. Eine Vererbung der Verknüpfung ist nicht implementiert. Formulare können nicht mit sich selbst verknüpft werden. Ein verknüpftes Formular kann nicht gelöscht werden, bis die Abhängigkeiten entfernt wurden.

## Formular Buttons

### Anzeigen

Das fertige Formular wird als PDF generiert und angezeigt.

### Speichern

Nach Eingabe oder ändern der Formular Attribute muss das Formular gespeichert werden.

## Formularfelder

Bevor Formularfelder angelegt werden können muss das Formular gespeichert werden.

Nun kommt die eigentliche Arbeit:

Bei den Formularfelder Buttons klickt Ihr auf "Neu", um das erste einzufügende Datenfeld auszuwählen und zu positionieren: (Die spätere Reihenfolge Eurer Datenfelder ist egal! Ihr könnt auch erst hinten anfangen)

![](../../../../allgemeine-funktionen/administration/mitglieder/img/Formularfeld.png)

### Name

Unter "Name" könnt Ihr nun aus den möglichen Datenfelder dasjenige aus der Datenbank auswählen, das eingefügt werden soll.

### Seite

Seite auf der das Formularfeld platziert werden soll.

### Von links, Von unten

Dieses Datenfeld müsst Ihr nun Millimetergenau auf euer gerade eben generiertes PDF händisch setzen. der Punkt (0,0) liegt unten links auf der Seite!

Tipp: Druckt das Dokument aus und messt mit einem Lineal die Positionen aus.

Speichert das Ganze und zeigt euch das Ergebnis über den Anzeigen Button an.

Das müsst Ihr solange wiederholen, bis das Datenfeld an der richtigen Stelle eingefügt wurde.

Übrigens: Da das System noch nicht weiß, welchen Datensatz es beim Austesten nehmen soll, hat der Entwickler einen Dummy-Datensatz automatisch für das Erstellen und Testen des neuen Formulars bereitgestellt.

### Schriftart

Schriftart für den Text.

### Schriftgröße

Schriftgröße des Textes.

## Formularfelder Buttons

### Export

Exportiert die Formularfelder des aktuellen Formulars.

### Import

Importiert Formularfelder aus einer Datei die mit Export erzeugt wurde. Es werden alle bestehenden Formularfelder der aktuellen Formulars vor dem Import gelöscht.

### Neu

Erzeugt ein neues Formularfeld für das aktuelle Formular.

## Verfügbare Formularfelder

### Allgemeine Formularfelder

* zaehler: Eine fortlaufende natürliche Zahl die bei jeder Verwendung des Formulares um 1 hochgezählt wird (z.B. für Rechnungsnummern).
  * Der Zähler hat eine Mindestlänge. Die Länge wird unter Administration > Einstellungen > Rechnungen > Zählerlänge festgelegt. Die Standard-Zählerlänge ist 5.
  * Der Zähler wird mit Nullen (0) als Präfix aufgefüllt bis die Mindestlänge erreicht ist.
  * Der Zähler wird als Spalte "Fortlaufende Nr." in der Formularübersicht ausgegeben.
  * Der Zähler wird beim Anzeigen (Vorschau) von Formularen hochgezählt aber nicht gespeichert.
  * Der Wert kann in der Detailansicht des Formulares überschrieben werden.

### Formularfelder für Spendenbescheinigungen

* tagesdatum: Enthält das aktuelle Datum im Format TT.MM.JJJJ
* spendenbescheinigung\_anrede: Zusammengesetzer Wert aus Zeile 1 und 2
* spendenbescheinigung\_empfaenger: Zusammengesetzt aus den Empfängerzeilen der Spendenbescheinigung
* spendenbescheinigung\_datum: Datum der Spendenbescheinigung. Dieses Datum wird verwendet, um zwischen den Formularen zu unterscheiden:
  * Bis 31.12.2012 altes Formular
  * Ab 01.01.2013 neues Formular
* spendenbescheinigung\_betrag: Betrag aus der Spendenbescheinigung
* spendenbescheinigung\_betraginworten: Betrag aus der Spendenbescheinigung in Worten.
* spendenbescheinigung\_spendenart: Art aus der Spendenbescheinigung (Geldspende, Sachspende)
* spendenbescheinigung\_spendedatum: Datum der Spende (Einzelspendenbescheinigung) oder Festtext: "s. Anlage" (Sammelspendenbescheinigung)
* spendenbescheinigung\_spendenzeitraum: Zeitraum der Spenden (Sammelspendenbescheinigung) "\<Datum der ersten Buchung> bis \<Datum der letzten Buchung>". Hinweis: ab 2013 muss dieser Zeitraum auf der ersten Seite angegeben werden!
* spendenbescheinigung\_ersatzaufwendungen: Kennzeichen, ob es sich auf einen "Verzicht auf Erstattung von Aufwendungen" handelt
  * Bis 31.12.2012: "X", wenn das Häkchen gesetzt ist.
  * Ab 01.01.2013: "Ja", wenn das Häkchen gesetzt ist, sonst "Nein".
* spendenbescheinigung\_buchungsliste: Für Sammelbestätigungen die aufbereitete Liste der Buchungen, die bescheinigt werden.
  * Bis 31.12.2012: alte Variante, Liste mit folgenden Spalten:
    * Datum Betrag Verwendung
    * Summenzeile
    * Legende, ob es sich um einen Verzicht auf Erstattung von Aufwendungen handelt.
  * Ab 01.01.2013: den Vorgaben entsprechende neue Liste:
    * "Datum der Zuwendung" "Art der Zuwendung" "Verzicht auf die Erstattung..." Betrag
    * Summenzeile
    * In den Spalten "Verwendung" und "Art der Zuwendung" wird in Abhängigkeit von der Einstellungen "Spendenbescheinigung / Buchungsart drucken" entweder der Name der Buchungsart oder der Zweck aus der Buchung verwendet.
* spendenbescheinigung\_bezeichnungsachzuwendung: Bezeichung des Gegenstandes aus der Spendenbescheinigung
* spendenbescheinigung\_herkunftsachzuwendung:
  * Bis 31.12.2012: Herkunft des Gegenstandes aus der Spendenbescheinigung (keine Angaben, Privatvermögen, Betriebsvermögen)
  * Ab 01.01.2013: Herkunft des Gegenstandes aus der Spendenbescheinigung, Festtexte:
    * bei keine Angaben: "Der Zuwendende hat trotz Aufforderung keine Angaben zur Herkunft der Sachzuwendung gemacht."
    * bei Privatvermögen: "Die Sachzuwendung stammt nach den Angaben des Zuwendenden aus dem Privatvermögen."
    * bei Betriebsvermögen: "Die Sachzuwendung stammt nach den Angaben des Zuwendenden aus dem Betriebsvermögen und ist
    * mit dem Entnahmewert (ggf. mit dem niedrigeren gemeinen Wert) bewertet."
* spendenbescheinigung\_unterlagenwertermittlung: Wenn das Kennzeichen in der Spendenbescheinigung gesetzt ist, der Festtext: "Geeignete Unterlagen, die zur Wertermittlung gedient haben, z. B. Rechnung, Gutachten, liegen vor."
* spendenbescheinigung\_zeile1 - spendenbescheinigung\_zeile7: Wert der entsprechenden Zeile

### Formularfelder für Rechnungen

Folgende Formularfelder stehen für Rechnungen zur Verfügung:

* tagesdatum: Enthält das aktuelle Datum im Format TT.MM.JJJJ
* Empfänger: Empfänger der Rechnung. Formatiert für ein Adressfeld
* Zahlungsgrund: Multipel. Es können mehrere Positionen für ein Mitglied in Rechnung gestellt werden. Zur korrekten Darstellung ist "Zahlungsgrund" zu verwenden.
* Zahlungsgrund1: Sollte ab Version 1.4 nicht mehr verwendet werden
* Zahlungsgrund2: Sollte ab Version 1.4 nicht mehr verwendet werden.
* Buchungsdatum: Multipel
* Betrag: Multipel
* sowie alle Felder des Mitgliedsdatensatzes

### Formularfelder für SEPA-PreNotification

Folgende Formularfelder stehen für die PreNotification zur Verfügung:

* tagesdatum: Enthält das aktuelle Datum im Format TT.MM.JJJJ
* lastschrift\_empfaenger: Empfänger der PreNotification (=Kontoinhaber), formatiert für ein Adressfeld.
* lastschrift\_verwendungszweck: Der Verwendungszweck wie per SEPA ausgegeben.
* lastschrift\_mandatid: Die Mandatsreferenz
* lastschrift\_mandatdatum: Datum des SEPA-Lastschrift-Mandats
* lastschrift\_bic: Der BIC.
* lastschrift\_iban: Die IBAN
* lastschrift\_betrag: Der Abbuchungsbetrag
* lastschrift\_abrechnungslauf\_nr: Datum des Abrechnungslaufs.
* lastschrift\_abrechnungslauf\_datum: Datum des Abrechnungslaufs.
* lastschrift\_abrechnungslauf\_faelligkeit: Das Buchungsdatum der Lastschrift.
* sowie alle Felder des Zahlungspflichtigen (=Kontoinhaber) aus dem Mitgliedsdatensatz mit jeweils vorangestellten lastschrift\_...

## Beispiele

![](../../../../allgemeine-funktionen/administration/mitglieder/img/Formularroh.jpg)

![](../../../../allgemeine-funktionen/administration/mitglieder/img/Formularausgefuellt.jpg)

## Freie Formulare

Freie Formulare haben keinen speziellen Zweck und können mit den verfügbaren Variablen belegt werden. Zuerst wird mit einem beliebigen Programm eine Vorlage erstellt im Format .pdf. Die zu füllenden Bereiche werden frei gelassen. Im Bereich Administration/Formulare. Mit "neu" wird ein neues Formular eingepflegt und in der Datenbank verankert. Nachträgliche Änderungen an der Datei haben damit keine Auswirkungen, solange die Datei nicht neu in jVerein eingepflegt wird. In der Liste der Formulare wird das neu angelegte Formular angezeigt. Mit Rechtsklick auf den Eintrag kann man anwählen, ob man Formularfelder auswählen und platzieren will, die Datei mit Dummydaten anzeigen, duplizieren oder löschen will. Um das noch leere Formular mit Feldern zu füllen wählen wir "Formularfelder". Mit "neu" können nun Felder eingefügt werden. Die Variablen werden aus einer Liste ausgewählt und dann durch Abstand zum linken und unteren Seitenrand platziert. Schriftgröße und -art sind wählbar. Mit "anzeigen" kann die korrekte Platzierung geprüft werden. Es werden Dummy-Daten angezeigt.

Die Ausgabe mit echten Daten erfolgt aus der Mitgliederliste. Man filtert geeignet und markiert alle Zeilen, mit dessen Daten das Formular gefüllt werden soll. Ein Rechtsklick mit Auswahl des Formulars erzeugt dann eine PDF-Datei mit entsprechend vielen Seiten.
