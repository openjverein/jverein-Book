# Variablen

## Variablen

Für folgende Zwecke gibt es Variablen, mit Nennung der verfügbaren Variablengruppen

## Formulare

Rechnungen, Mahnungen: Allgemein, Rechnung, Mitglied

Spendenbescheinigung, Sammelspendenbescheinigung: Allgemein, Spendenbescheinigung, \(Mitglied wenn einem Mitglied zugeordnet\)

Pre-Notification: Allgemein, Lastschrift

Freie Formulare: Allgemein, Mitglied

## Sonstige

Bei diesen Feldern muss die Variable jeweis in der Form $VARIABLENNAME angegeben werden, wenn direkt von einem Zeichen gefolgt muss die Form ${VARIABLENNAME} verwendet werden.

Zahlungsgrund bei der Abrechnung, Zweck von Zusatzbeträgen: Allgemein, Mitglied, Abrechnung

Rechnung Text bei der Abrechnung: Allgemein, Rechnung, Mitglied

1Ct Überweisung Zahlungsgrund: Allgemein, Lastschrift

Mails \(auch bei Druck & Mail\): Allgemein, Mitglied

### Allgemeine Variablen

* zaehler: Eine fortlaufende natürliche Zahl die bei jeder Verwendung des Formulares um 1 hochgezählt wird (z.B. für Rechnungsnummern).
  * ACHTUNG: Der Zähler wird wirklich bei jeder Verwendung, also bei jedem Erstellen des PDFs hochgezählt. Wenn also die selbe Rechnung oder Spendenbescheinigung mehrfach bei Druck & Mail gedruckt oder versand wird, hat sie einen unterscheidlichen zaehler!
  * Der Zähler hat eine Mindestlänge. Die Länge wird unter Administration > Einstellungen > Rechnungen > Zählerlänge f  estgelegt. Die Standard-Zählerlänge ist 5.
  * Der Zähler wird mit Nullen (0) als Präfix aufgefüllt bis die Mindestlänge erreicht ist.
  * Der Zähler wird als Spalte "Fortlaufende Nr." in der Formularübersicht ausgegeben.
  * Der Zähler wird beim Anzeigen (Vorschau) von Formularen hochgezählt aber nicht gespeichert.
  * Der Wert kann in der Detailansicht des Formulares überschrieben werden.
* aktuellermonat Monat in der Form 01.2025
* aktuellesjahr Jahr in der Form 2025
* folgejahr Folgejahr in der Form 2026
* folgemonat Folgemonat in der Form 02.2025
* tagesdatum Datum in der Form 01.01.2025
* tagesdatumtt Tag in der Form 01
* tagesdatummm Monat in der Form 01
* tagesdatumjjjj Jahr in der Form 2025
* vormonat Vormonat in der Form 12.2024
* vorjahr Vorjahr in der Form 2024
* verein_name Der Vereinsmane wie in den Einstellungen eingetragen
* verein_strasse Die Strasse wie in den Einstellungen eingetragen
* verein_plz Die PLZ wie in den Einstellungen eingetragen
* verein_ort Der Ort wie in den Einstellungen eingetragen
* verein_staat Der Staat wie in den Einstellungen eingetragen
* verein_absender Der Vereinsadresse in einer Zeile
* verein_iban Die IBAN wie in den Einstellungen eingetragen
* verein_bic Die BIC wie in den Einstellungen eingetragen
* verein_glaeubiger_id Die Gläubiger-ID wie in den Einstellungen eingetragen
* verein_ust_id Die USt-Id wie in den Einstellungen eingetragen
* verein_steuer_nr Die Steuernummer wie in den Einstellungen eingetragen


### Mitglieds Variablen

* mitglied\_empfaenger Formatierte Anschrift -> Erste Zeile: Herr Frau / Zweite Zeile: Vorname Nachname / ...
* mitglied\_anrede
* mitglied\_anrede\_du Informelle Anrede \(Hallo ...\)
* mitglied\_anrede\_foermlich Name mit förmlicher Anrede \(Sehr geehrter ...\)
* mitglied\_titel Titel
* mitglied\_name Name
* mitglied\_namevorname Name, Vorname
* mitglied\_vorname Vorname
* mitglied\_vornamename Vorname Name
* mitglied\_strasse Straße
* mitglied\_adressierungszusatz
* mitglied\_plz Postleitzahl
* mitglied\_ort Ort
* mitglied\_staat Staat
* mitglied\_telefon\_dienstlich Telefon dienstlich
* mitglied\_telefon\_privat Telefon privat
* mitglied\_handy Handy
* mitglied\_email Email-Adresse
* mitglied\_adresstyp interne Nummer des Adresstyps
* mitglied\_geburtsdatum Geburtsdatum - Format: tt.mm.jjjj
* mitglied\_sterbetag Sterbetag - Format: tt.mm.jjjj
* mitglied\_geschlecht Geschlecht o, m oder w
* mitglied\_personenart Personentyp: n=natürliche Person, j=juristische Person
* mitglied\_vermerk1 1.Vermerk
* mitglied\_vermerk2 2.Vermerk
* mitglied\_zahlungsrhythmus Schlüssel des Zahlungsrhytmus
* mitglied\_zahlungstermin Beitragsmodel "flexibel": Zahlungstermin und Zahlungsrhytmus als Text. Beispiele: "Vierteljährlich (Feb./Mai /Aug./Nov.)", "Halbjährlich (Mai /Nov.)"
* mitglied\_zahlungsweg Schlüssel des Zahlungsweges
* mitglied\_zahlungsweg\_text Text des Zahlungsweges wie in den Einstellungen eingestellt.
* mitglied\_zahlerid Interne Mitgliedsnummer des zahlenden Mitglieds
* mitglied\_arbeitseinsatz\_betrag Betrag pro Stunde fehlenden Arbeitseinsatzes - Format: 0,00
* mitglied\_arbeitseinsatz\_stunden Anzahl Stunden Arbeitseinsatz - Format: 0,00
* mitglied\_beitragsgruppe\_bezeichnung Bezeichnung der Beitragsgruppe.
* mitglied\_beitragsgruppe\_betrag Betrag der Beitragsgruppe.
* mitglied\_beitragsgruppe\_id Schlüsselnummer der Beitragsgruppe.
* mitglied\_mandatdatum
* mitglied\_mandatid
* mitglied\_iban IBAN
* mitglied\_iban\_maskiert IBAN, die in dieser Lastschrift verwendet wird, in maskierter Form
* mitglied\_bic BIC
* mitglied\_bankname Name der Bank
* mitglied\_eintritt Eintrittsdatum - Format: tt.mm.jjjj
* mitglied\_eingabedatum Datum der Ersteingabe des Datensatzes - Format: tt.mm.jjjj
* mitglied\_austritt Austrittsdatum - Format: tt.mm.jjjj
* mitglied\_kuendigung Kündigungsdatum - Format: tt.mm.jjjj
* mitglied\_letzte.aenderung Datum der letzten Änderung des Mitgliedsdatensatzes - Format: tt.mm.jjjj
* mitglied\_externe\_mitgliedsnummer externe Mitgliedsnummer
* mitglied\_id Interne Mitgliedsnummer
* mitglied\_individuellerbeitrag Individueller Beitrag
* mitglied_eigenschaft_???? Statt ???? steht eine Eigenschaft, die Sie für Mitglieder definiert haben. Ist die Eigenschaft für dieses Mitglied gesetzt wird als Wert ein X angegeben.
* mitglied_zusatzfeld_???? Statt ???? steht der Name des Zusatzfeldes.
* mitglied_lesefelder_???? Statt ???? steht der Name des Lesefeldes.

Die Daten des Kontoinhabers

* mitglied\_kontoinhaber
* mitglied\_kontoinhaber\_personenart
* mitglied\_kontoinhaber\_anrede
* mitglied\_kontoinhaber\_titel
* mitglied\_kontoinhaber\_name
* mitglied\_kontoinhaber\_vorname
* mitglied\_kontoinhaber\_strasse
* mitglied\_kontoinhaber\_adressierungszusatz
* mitglied\_kontoinhaber\_plz
* mitglied\_kontoinhaber\_ort
* mitglied\_kontoinhaber\_staat
* mitglied\_kontoinhaber\_email
 
### Variablen für Spendenbescheinigungen

* spendenbescheinigung\_anrede: Zusammengesetzer Wert aus Zeile 1 und 2
* spendenbescheinigung\_empfaenger: Zusammengesetzt aus den Empfängerzeilen der Spendenbescheinigun
* spendenbescheinigung\_datum: Datum der Spendenbescheinigung. Dieses Datum wird verwendet, um zwischen den Formularen zu unterscheiden:
  * Bis 31.12.2012 altes Formular
  * Ab 01.01.2013 neues Formula
* spendenbescheinigung\_betrag: Betrag aus der Spendenbescheinigun
* spendenbescheinigung\_betraginworten: Betrag aus der Spendenbescheinigung in Worten
* spendenbescheinigung\_spendenart: Art aus der Spendenbescheinigung \(Geldspende, Sachspende\
* spendenbescheinigung\_spendedatum: Datum der Spende \(Einzelspendenbescheinigung\) oder Festtext: "s. Anlage" \(Sammelspendenbescheinigung\
* spendenbescheinigung\_spendenzeitraum: Zeitraum der Spenden \(Sammelspendenbescheinigung\) "&lt;Datum der ersten Buchung&gt; bis &lt;Datum der letzten Buchung&gt;". Hinweis: ab 2013 muss dieser Zeitraum auf der ersten Seite angegeben werden
* spendenbescheinigung\_ersatzaufwendungen: Kennzeichen, ob es sich auf einen "Verzicht auf Erstattung von Aufwendungen" handel
  * Bis 31.12.2012: "X", wenn das Häkchen gesetzt ist
  * Ab 01.01.2013: "Ja", wenn das Häkchen gesetzt ist, sonst "Nein"
* spendenbescheinigung\_ersatzaufwendungen_ja ab 01.01.2013: "X", wenn das Häkchen gesetzt ist
* spendenbescheinigung\_ersatzaufwendungen_nein ab 01.01.2013: "X", wenn das Häkchen gesetzt ist
* spendenbescheinigung\_buchungsliste: Für Sammelbestätigungen die aufbereitete Liste der Buchungen, die bescheinigt werden
  * Bis 31.12.2012: alte Variante, Liste mit folgenden Spalten
    * Datum Betrag Verwendun
    * Summenzeil
    * Legende, ob es sich um einen Verzicht auf Erstattung von Aufwendungen handelt
  * Ab 01.01.2013: den Vorgaben entsprechende neue Liste
    * "Datum der Zuwendung" "Art der Zuwendung" "Verzicht auf die Erstattung..." Betra
    * Summenzeil
    * In den Spalten "Verwendung" und "Art der Zuwendung" wird in Abhängigkeit von der Einstellungen "Spendenbescheinigung / Buchungsart drucken" entweder der Name der Buchungsart oder der Zweck aus der Buchung verwendet
    * Die Splaten sind auch einzeln Verfügbar als:
      * spendenbescheinigung\_buchungsliste_daten
      * spendenbescheinigung\_buchungsliste_art
      * spendenbescheinigung\_buchungsliste_verzicht
      * spendenbescheinigung\_buchungsliste_betrag
* spendenbescheinigung\_bezeichnungsachzuwendung: Bezeichung des Gegenstandes aus der Spendenbescheinigun
* spendenbescheinigung\_herkunftsachzuwendung
  * Bis 31.12.2012: Herkunft des Gegenstandes aus der Spendenbescheinigung \(keine Angaben, Privatvermögen, Betriebsvermögen\)
  * Ab 01.01.2013: Herkunft des Gegenstandes aus der Spendenbescheinigung, Festtexte
    * bei keine Angaben: "Der Zuwendende hat trotz Aufforderung keine Angaben zur Herkunft der Sachzuwendung gemacht.
    * bei Privatvermögen: "Die Sachzuwendung stammt nach den Angaben des Zuwendenden aus dem Privatvermögen.
    * bei Betriebsvermögen: "Die Sachzuwendung stammt nach den Angaben des Zuwendenden aus dem Betriebsvermögen und is
    * mit dem Entnahmewert \(ggf. mit dem niedrigeren gemeinen Wert\) bewertet.
* spendenbescheinigung\_unterlagenwertermittlung: Wenn das Kennzeichen in der Spendenbescheinigung gesetzt ist, der Festtext: "Geeignete Unterlagen, die zur Wertermittlung gedient haben, z. B. Rechnung, Gutachten, liegen vor.
* spendenbescheinigung\_zeile1 - spendenbescheinigung_zeile7: Wert der entsprechenden Zeil
* spendenbescheinigung\_finanzamt das Finanzamt wie in den Einstellungen hinterlegt
* spendenbescheinigung\_steuer\_nummmer die Steuernummer wie in den Einstellungen hinterlegt
* spendenbescheinigung\_datum\_bescheid das Bescheiddatum vom Finanzamt wie in den Einstellungen hinterlegt
* spendenbescheinigung\_veranlagungszeitraum der Veranlagungszeitraum wie in den Einstellungen hinterlegt
* spendenbescheinigung\_beguenstigter_zweck der begünsigte Zweck wie in den Einstellungen hinterlegt
* spendenbescheinigung\_unterschrift die Unterschrift wie in den Einstellungen hinterlegt

### Variablen für Rechnungen und Mahnungen \(Erst ab Version 3.0.0\)

Folgende Formularfelder stehen für Rechnungen zur Verfügung \(die alten Variablen die mit "mitgliedskonto_" beginnen sollten ab Version 3.0.0 nicht mehr verwendet werden\):

* Für jede Rechnungspositionen wird jeweils eine Zeile zu folgenden Variablen hinzugefügt:
  * rechnung\_zahlungsgrund Der Zahlungsgrund
  * rechnung\_buchungsdatum Das Datum
  * rechnung\_nettobetrag Nettobetrag
  * rechnung\_steuersatz Steuersatz
  * rechnung\_steuerbetrag Bruttobetrag
* rechnung\_betrag Die Rechnungssumme
* rechnung\_ist Der bereits bezahlte Betrag
* rechnung\_stand Der Forderungsstand \(Ist - Rechnungsbetrag\)
* rechnung\_summe\_offen Der noch zu zahlende Rechnungsbetrag \(Rechnungsbetrag - Ist\)
* qrcode\_summe Der QR-Code
* qrcode\_intro Text für QR-Code wie in Einstellungen eingestellt
* rechnung\_datum Rechnungsdatum
* rechnung\_nummer Rechnungsnummer, eindeutig für jede Rechnung \(sollte statt zaehler verwendet werden\).

sowie alle Felder des Zahlungspflichtigen:

* rechnung\_anrede
* rechnung\_titel
* rechnung\_name
* rechnung\_vorname
* rechnung\_strasse
* rechnung\_adressierungszusatz
* rechnung\_plz
* rechnung\_ort
* rechnung\_staat
* rechnung\_geschlecht
* rechnung\_anrede\_du
* rechnung\_anrede\_foermlich
* rechnung\_personenart
* rechnung\_mandatid
* rechnung\_mandatdatum
* rechnung\_bic
* rechnung\_iban
* rechnung\_ibanmaskiert
* rechnung\_empfaenger
* rechnung\_zahlungsweg\_text

### Variablen für SEPA-PreNotification

Folgende Formularfelder stehen für die PreNotification zur Verfügung:

* lastschrift\_empfaenger: Empfänger der PreNotification \(=Kontoinhaber\), formatiert für ein Adressfeld.
* lastschrift\_verwendungszweck: Der Verwendungszweck wie per SEPA ausgegeben.
* lastschrift\_mandatid: Die Mandatsreferenz
* lastschrift\_mandatdatum: Datum des SEPA-Lastschrift-Mandats
* lastschrift\_bic: Der BIC.
* lastschrift\_iban: Die IBAN
* lastschrift\_betrag: Der Abbuchungsbetrag
* lastschrift\_abrechnungslauf\_nr: Datum des Abrechnungslaufs.
* lastschrift\_abrechnungslauf\_datum: Datum des Abrechnungslaufs.
* lastschrift\_abrechnungslauf\_faelligkeit: Das Buchungsdatum der Lastschrift.

sowie alle Felder des Zahlungspflichtigen \(=Kontoinhaber\) 

* lastschrift\_anrede\_du
* lastschrift\_anrede\_foermlich
* lastschrift\_personenart
* lastschrift\_geschlecht
* lastschrift\_anrede
* lastschrift\_titel
* lastschrift\_name
* lastschrift\_vorname
* lastschrift\_strasse
* lastschrift\_adressierungszusatz
* lastschrift\_plz
* lastschrift\_ort
* lastschrift\_staat
* lastschrift\_email
* lastschrift\_ibanmaskiert

## Abrechnungs Variablen

* abrechnungsparameter\_abrechnungsmodus Text des Abrechnungsmodus
* abrechnungsparameter\_abrechnungsmonat Abrechnungsmonat \(nur bei entsprechendem Beitragsmodell\)
* abrechnungsparameter\_faelligkeit Fälligkeit
* abrechnungsparameter\_stichtag Stichtag
* abrechnungsparameter\_vondatum Von-Datum bei Abrechnung von neu eingetretenen Mitgliedern
* abrechnungsparameter\_bisdatum Bis-Datum bei Abrechnung von ausgetretenen Mitgliedern
* abrechnungsparameter\_stichtag\_monat Der Monat des Stichtags im Format 01 \(Erst ab Version 3.0.0\)
* abrechnungsparameter\_stichtag\_monat\_text Der Monatsname des Stichtages z.B. Januar \(Erst ab Version 3.0.0\)
* abrechnungsparameter\_stichtag\_jahr Das Jahr des Stichtages z.B. 2025 \(Erst ab Version 3.0.0\)
* abrechnungsparameter\_verwendungszweck Der Zahlugsgrund
* abrechnungsparameter\_zusatzbetraege Merkmal, ob Zusatzbeträge abgerechnet werden sollen
* abrechnungsparameter\_kursteilnehmer Merkmal, ob Kursteilnehmer abgerechnet werden sollen
* abrechnungsparameter\_kompakteabbuchung Merkmal, ob die Abbuchung von gleichen Konten zusammengefasst werden sollen
* abrechnungsparameter\_sepaprint Merkmal, ob die SEPA-Listen gedruckt werden sollen
