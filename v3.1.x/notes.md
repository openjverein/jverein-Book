# Release Notes Version 3.1.0

## Allgemeines

Mit 3.0.0 wurde die Versionsnummerierung auf die Art MAJOR.MINOR.PATCH umgestellt:
* MAJOR wird bei inkompatiblen API Änderungen hochgezählt
* MINOR wird bei neuer Funktionalität hochgezählt 
* PATCH wird bei Fehlerkorrekturen hochgezählt

## The Big Ones

### Wirtschaftsplan



### Mittelverwendung (ab Version 3.0.0)

* Für das Feature Mittelverwendung gibt eine neue Ansicht "Mittelverwendungsaldo" (siehe [Mittelverwendung](buchf/mittelverwendungsaldo.md))

**Bei dem Feature Mittelverwendung handelt es sich um ein experimentelles Feature.**

Das JVerein Team hat dieses Feature aus Informationen aus dem Internet entwickelt, aber selbst bisher keine Erfahrung mit der Mittelverwendung Berechnung.

Wir bitten darum die Anwender welche bereits Mittelverwendungsreports erstellt haben zu prüfen, ob die Art der Berechnung, die ausgegeben Werte und die Darstellung den Anforderungen entsprechen.

Wir würden uns über ein Feedback der Anwender freuen, um es als ausgereiftes Feature anbieten zu können.

## Sonstige Features

#### Sollbuchung Neu Dialog

Beim Erzeugen einer neuen Sollbuchung öffnet sich ein Dialog mit dem automatisch eine Sollbuchung und eine erste Sollbuchungsposition erzeugt wird. Siehe [Sollbuchung](mitglieder/mitgliedskonto.md) 

#### Individuelle Mandats ID

Für SEPA Lastschriften lässt sich jetzt neben der Mitgliedsnummer und externen Mitgliedsnummer eine individuelle Mandats-ID benutzen.

#### Mitgliedsnummer bzw. externe Mitgliedsnummer bei Mitgliedsauswahl anzeigen

Bei Auswahl dieser Option in den Einstellungen->Anzeige wird in Tabellen oder bei der Mitglieder Auswahl an den Mitglied Namen in Klammern die Mitgliedsnummer, oder falls Externe Mitgliedsnummer aktiviert ist, die externe Mitgliedsnummer angezeigt.

Dies ist nützlich falls es mehrere Mitglieder mit dem gleichen Namen gibt. Diese lassen sich so unterscheiden.

#### Speichern und neu Button

Bei folgenden View gibt es einen neuen Button "Speichern und neu".
* Buchung
* (Nicht) Mitglied
* Kursteilnehmer
* Buchungsart
* Formularfeld

Es wird der aktuelle Datensatz gespeichert und es kann ein weiterer eingegeben werden.

#### Anzeige der Summen in der Fußzeile von Tabellen

Bei einigen Tabellen werden, bei der Auswahl mehrerer Einträge, in der Fußzeile die Summen Beträge der selektierten Einträge ausgegeben. Dies gilt für:
* Buchungen
* Anlagenbuchungen
* Kontensaldo
* Buchungsklassensaldo
* Projektsaldo
* Mittelverwendungsaldo

#### Verbesserte Fehlerausgabe bei Mailversand

Ein Mailversand wir jetzt als Erfolgreich angezeigt wenn die Mail erfolgreich versendet wurde, obwohl evtl. das Übermitteln in den Ordner für gesendete Mails fehlgeschlagen ist. In diesem Fall wird eine entsprechende Meldung ausgegeben.

#### Buchungen ohne Buchungsart werden im Kontensaldo und Buchungsklassensaldo berücksichtigt

Buchungen ohne Buchungsart werden im Kontensaldo berücksichtigt und der Betrag auch in der Spalte Bemerkung ausgegeben.

Buchungen ohne Buchungsart werden im Buchungsklassensaldo berücksichtigt.


#### Abrechnungslauf für eingetretene Mitglieder

Bei einem Abrechnungslauf für eingetretene Mitglieder wird die Option "Eingabedatum" wieder angeboten.

Es ist ausreichend entweder Eingabedatum oder Eintrittsdatum zu wählen.

#### Eigenschaften Gruppen als Spalten bei Mitgliedern

Eigenschaften Gruppen lassen sich jetzt auch in den Einstellungen->Mitglieder Spalten auswählen und damit in der Liste der Mitglieder anzeigen.

## Kleinere Korrekturen und Erweiterungen

* Reports starten in der Fußzeile wieder mit Seite 1 statt mit 0

