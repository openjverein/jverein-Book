# Variable

## Variable

Für diverse Zwecke \(z. B. Formulare, Mails, Pre-Notification ...\) gibt es Variable.

### Allgemeine Variable

#### aktuellermonat

Aktueller Monat im Format mm.jjjj

#### aktuellesjahr

Aktuelles Jahr im Format jjjj

#### folgejahr

Folgejahr im Format jjj

#### folgemonat

Folgemonat im Format mm.jjjj

#### tagesdatum

Aktuelles Datum in der Form tt.mm.jjjj

#### tagesdatumtt

Aktuelles Datum in der Form tt

#### tagesdatummm

Aktuelles Datum in der Form mm

#### vormonat

Vormonat im Format mm.jjjj

### Buchung

#### buchung\_auszugsnummer

optional

#### buchung\_betrag

Pflicht

#### buchung\_blattnummer

optional

#### buchung\_buchungsart\_nummer

optional

#### buchung\_buchungsklasse\_nummer

optional

#### buchung\_datum

Pflicht

Format TT.MM.JJJJ

#### buchung\_iban

optional

#### buchung\_kommentar

optional

#### buchung\_kontonummer

Pflicht

#### buchung\_name

Pflicht

#### buchung\_zweck1

Pflicht

Das Feld kann mehrzeilig sein. Gesamtlänge 500 Stellen. Mehrzeilige Verwendungszwecke sind in Anführungszeichen zu setzen.

## Lastschrift

#### lastschrift\_abrechnungslauf\_faelligkeit

Datum der Fälligkeit

#### lastschrift\_anrede

Anrede

#### lastschrift\_anrede\_foermlich

Förmliche Anrede. Z. B. "Sehr geehrter Herr Dr. Wichtig,".

#### lastschrift\_anrede\_du

Informelle Anrede. Z. B. "Hallo Willi,".

#### lastschrift\_betrag EUR

Betrag der eingezogen wird

#### lastschrift\_bic

Bic, die in dieser Lastschrift verwendet wird

#### lastschrift\_email

E-Mail

#### lastschrift\_geschlecht

Geschlecht \(ab Version 2.8.16\)

#### lastschrift\_mandatdatum

Datum des Mandates \(Ausstellungsdatum\)

#### lastschrift\_mandatid

Mandatsnummer

#### lastschrift\_mandatsequence

Mandatssequence - Erste / Wiederholung

#### lastschrift\_iban

vollständige IBAN, die in dieser Lastschrift verwendet wird

#### lastschrift\_ibanmaskiert

IBAN, die in dieser Lastschrift verwendet wird, in maskierter Form

#### lastschrift\_name

Name

#### lastschrift\_ort

Ort

#### lastschrift\_plz

PLZ

#### lastschrift\_strasse

Straße

#### lastschrift\_titel

Titel

#### lastschrift\_vorname

Vorname

#### lastschrift\_verwendungszweck

Verwendungszweck

### Mitglied

#### mitglied\_adressierungszusatz

Adressierungszusatz

#### mitglied\_adresstyp

interne Nummer des Adresstyps

#### mitglied\_anrede

Anrede

#### mitglied\_anrede\_du

Informelle Anrede

#### mitglied\_anrede\_foermlich

Name mit förmlicher Anrede \(Sehr geehrter ...\)

#### mitglied\_arbeitseinsatz\_betrag

Betrag pro Stunde fehlenden Arbeitseinsatzes - Format: 0,00

#### mitglied\_arbeitseinsatz\_stunden

Anzahl Stunden Arbeitseinsatz - Format: 0,00

#### mitglied\_austritt

Austrittsdatum - Format: tt.mm.jjjj

#### mitglied\_bankname

Name der Bank

#### mitglied\_beitragsgruppe\_betrag

Bezeichnung der Beitragsgruppe - Format: 0,00

#### mitglied\_beitragsgruppe\_bezeichnung

Bezeichnung der Beitragsgruppe.

#### mitglied\_beitragsgruppe\_id

Schlüsselnummer der Beitragsgruppe.

#### mitglied\_bic

BIC

#### mitglied\_eingabedatum

Datum der Ersteingabe des Datensatzes - Format: tt.mm.jjjj

#### mitglied\_eintritt

Eintrittsdatum - Format: tt.mm.jjjj

#### mitglied\_email

Email-Adresse

#### mitglied\_empfaenger

Formatierte Anschrift -&gt; Erste Zeile: Herr Frau / Zweite Zeile: Vorname Nachname / ...

#### mitglied\_externe\_mitgliedsnummer

externe Mitgliedsnummer

#### mitglied\_geburtsdatum

Geburtsdatum - Format: tt.mm.jjjj

#### mitglied\_geschlecht

Geschlecht m oder w

#### mitglied\_handy

Handy

#### mitglied\_iban

IBAN

#### mitglied\_iban\_maskiert

IBAN, die in dieser Lastschrift verwendet wird, in maskierter Form

#### mitglied\_id

Interne Mitgliedsnummer

#### mitglied\_individuellerbeitrag

Individueller Beitrag

#### mitglied\_konto

Kontonummer

#### mitglied\_kontoinhaber\_adressierungszusatz

Kontoinhaber

#### mitglied\_kontoinhaber\_anrede

Kontoinhaber

#### mitglied\_kontoinhaber\_email

Kontoinhaber

#### mitglied\_kontoinhaber\_name

Kontoinhaber

#### mitglied\_kontoinhaber\_ort

Kontoinhaber

#### mitglied\_kontoinhaber\_personenart

Kontoinhaber

#### mitglied\_kontoinhaber\_plz

Kontoinhaber

#### mitglied\_kontoinhaber\_staat

Kontoinhaber

#### mitglied\_kontoinhaber\_strasse

Kontoinhaber

#### mitglied\_kontoinhaber\_titel

Kontoinhaber

#### mitglied\_kontoinhaber\_vorname

Kontoinhaber

#### mitglied\_kuendigung

Kündigungsdatum - Format: tt.mm.jjjj

#### mitglied\_letzte.aenderung

Datum der letzten Änderung des Mitgliedsdatensatzes - Format: tt.mm.jjjj

#### mitglied\_mandatdatum

SEPA-Mandat - Formatierung für tt.mm.jjjj: $!{dateformat.format\($mitglied\_mandatdatum\)}

#### mitglied\_mandatid

SEPA-Mandat

#### mitglied\_name

Name

#### mitglied\_namevorname

Name, Vorname

#### mitglied\_ort

Ort

#### mitglied\_personenart

Personentyp: n=natürliche Person, j=juristische Person

#### mitglied\_plz

Postleitzahl

#### mitglied\_staat

Staat

#### mitglied\_sterbetag

Sterbetag - Format: tt.mm.jjjj

#### mitglied\_strasse

Straße

#### mitglied\_telefon\_dienstlich

Telefon dienstlich

#### mitglied\_telefon\_privat

Telefon privat

#### mitglied\_titel

Titel

#### mitglied\_vermerk1

1. Vermerk

#### mitglied\_vermerk2

1. Vermerk

#### mitglied\_vorname

Vorname

#### mitglied\_vornamename

Vorname Name

#### mitglied\_zahlerid

Interne Mitgliedsnummer des zahlenden Mitglieds

#### mitglied\_zahlungsrhytmus

Schlüssel des Zahlungsrhytmus

#### mitglied\_zahlungstermin

Beitragsmodel "flexibel": Zahlungstermin und Zahlungsrhytmus als Text. Beispiele: "Vierteljährlich \(Feb./Mai /Aug./Nov.\)", "Halbjährlich \(Mai /Nov.\)"

#### mitglied\_zahlungsweg

Schlüssel des Zahlungsweges

#### mitglied\_zahlungsweg\_text

Bezeichnung des Zahlungsweges

#### mitglied\_eigenschaft\_????

Statt ???? steht eine Eigenschaft, die Sie für Mitglieder definiert haben. Ist die Eigenschaft für dieses Mitglied gesetzt wird als Wert ein X angegeben.

#### mitglied\_zusatzfeld\_????

Statt ???? steht der Name des Zusatzfeldes.

#### mitglied\_lesefelder\_????

Statt ???? steht der Name des Lesefeldes.

### Mitgliedskonto

#### mitgliedskonto\_betrag

Betrag dieser Buchung der bezahlt werden muss

#### mitgliedskonto\_buchungsdatum

Datum der Buchung

#### mitgliedskonto\_differenz

mitgliedskonto\_betrag - mitgliedskonto\_ist, also was noch zu zahlen ist.

#### mitgliedskonto\_ist

Betrag dieser Buchung der bereits bezahlt wurde

#### mitgliedskonto\_zahlungsgrund

Ein Grund warum bezahlt werden muss z.B. Mitgliedsbeitrag oder Arbeitsstunden

#### mitgliedskonto\_zahlungsgrund1

Noch eine Begründung für diese Buchung

## Spendenbescheinigung

#### spendenbescheinigung\_betrag

Betrag

#### spendenbescheinigung\_betraginworten

Betrag in Worten

#### spendenbescheinigung\_datum

Datum der Spendenbescheinigung

#### spendenbescheinigung\_bezeichnungsachzuwendung

Bezeichnung der Sachzuwendung

#### spendenbescheinigung\_buchungsliste

Liste der Buchungen

### spendenbescheinigung\_buchungsliste\_art

Liste der Buchungsarten

### spendenbescheinigung\_buchungsliste\_betrag

Liste der Spendenbeträge

### spendenbescheinigung\_buchungsliste\_daten

Liste der Spendendaten

### spendenbescheinigung\_buchungsliste\_verzicht

Liste der Verzichtserklärungen

#### spendenbescheinigung\_empfaenger

Aufbereitetes Adressfeld des Spenders

#### spendenbescheinigung\_ersatzaufwendungen

Ersatz für Aufwendungen

#### spendenbescheinigung\_ersatzaufwendungen\_ja

Ersatz für Aufwendungen

#### spendenbescheinigung\_ersatzaufwendungen\_nein

Ersatz für Aufwendungen

#### spendenbescheinigung\_herkunftsachzuwendung

Herkunft der Sachzuwendung

#### spendenbescheinigung\_spendenart

Art der Spendenbescheinigung

#### spendenbescheinigung\_spendedatum

Datum der Spende

#### spendenbescheinigung\_spendenzeitraum

Sammelspendenbescheinigungen: Zeitraum der Spende

#### spendenbescheinigung\_unterlagenwertermittlung

Unterlagen zur Wertermittlung

### Abrechnungsparameter

Diese Parameter stehen nur beim Abrechnungslauf zur Verfügung. Die Variablen können im Verwendungszweck und im Verwendungszweck des Zusatzbetrages benutzt werden.

#### abrechnungsparameter\_abrechnungsmodus

Text des Abrechnungsmodus

#### abrechnungsparameter\_abrechnungsmonat

Abrechnungsmonat \(nur bei entsprechendem Beitragsmodell\)

#### abrechnungsparameter\_bisdatum

Bis-Datum bei Abrechnung von ausgetretenen Mitgliedern

#### abrechnungsparameter\_faelligkeit

Fälligkeit

#### abrechnungsparameter\_kompakteabbuchung

Merkmal, ob die Abbuchung von gleichen Konten zusammengefasst werden sollen

#### abrechnungsparameter\_kursteilnehmer

Merkmal, ob Kursteilnehmer abgerechnet werden sollen

#### abrechnungsparameter\_sepaprint

Merkmal, ob die SEPA-Listen gedruckt werden sollen

#### abrechnungsparameter\_stichtag

Stichtag

#### abrechnungsparameter\_vondatum

Von-Datum bei Abrechnung von neu eingetretenen Mitgliedern

#### abrechnungsparameter\_zusatzbetraege

Merkmal, ob Zusatzbeträge abgerechnet werden sollen

