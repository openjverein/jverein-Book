# Release Notes Version 3.1.0

## Allgemeines

Mit 3.0.0 wurde die Versionsnummerierung auf die Art MAJOR.MINOR.PATCH umgestellt:
* MAJOR wird bei inkompatiblen API Änderungen hochgezählt
* MINOR wird bei neuer Funktionalität hochgezählt 
* PATCH wird bei Fehlerkorrekturen hochgezählt

## The Big Ones

### Steuer Handling (Konzeptänderung ab 3.1.0)

Bis zur Version 3.0.x war es nötig Buchungen mit Steuern über eine Splittbuchung in eine Nettobuchung und eine Steuerbuchung aufzuteilen.

Dieses ist in ab der Version 3.1.0 nicht mehr nötig.

**Neues Konzept:**

* Eine Buchung mit zugeordneter Steuer braucht nicht mehr in zwei Buchungen aufgesplittet werden. In den relevanten Views wie z.B. Buchungsklassensaldo werden die Buchungen automatisch gesplittet und die Nettobeträge und Steuern den entsprechenden Buchungsarten/Buchungen zugeordnet
* Wegen der Kompatibilität mit alten bereits gesplitteten Buchungen werden diese korrekt in die Berechnung einbezogen wenn ihnen bereits eine Steuer zugeordnet ist. Steuer Zuordnung in neuen Splittbuchungen wird nicht mehr unterstützt. Hat die gesetzte Buchungsart eine Steuer so wird sie berücksichtigt, auch wenn sie Teil einer neuen Splittbuchung ist. 
* Ähnlich wie bei der Zuordnung der Buchungsklasse zur Buchung, entweder implizit über die Buchungsart oder als Parameter in der Buchung, ist das auch mit der Zuordnung der Steuer. Unter Administration->Einstellungen->Buchführung lässt sich einstellen ob die Steuer der Buchungsart entnommen werden soll oder ob sie individuell als Attribut in der Buchung gesetzt werden kann. In letzterem Fall erscheint das Attribut "Steuer" als Spalte in der Buchungsliste und als Parameter in der Buchung. Als weiteres kann in diesem Fall die Steuer in Zusatzbeiträgen und Beitragsgruppen gesetzt werden. Diese wird dann im Abrechnungslauf auf die erzeugten Buchungen übertragen
* Bisher waren die Steuersätze fest in JVerein eingebaut. Ab Version 3.1.0 werden sie manuell angelegt. Siehe (siehe [Steuer](administration/admbuchf/steuer.md)). Wurden bisher bereits Steuern verwendet, so werden für diese automatisch bei der Migration auf die 3.1.0 Steuer Einträge erzeugt. Ansonsten müssen sie manuell angelegt werden



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

#### Weitere Menüpunkte über Administration->Einstellungen->Anzeige aktivierbar

Die Anzeige von Projekten, Spendenbescheinigungen und Rechnungen/Mahnungen lässt sich in den Einstellungen konfigurieren.

#### Rechnungen für mehrere Sollbuchungen erstellen

Es lässt sich eine Rechnung über mehrere Sollbuchungen erstellen.

#### Rechnungen Kommentar

Bei der Rechnung lässt sich ein Kommentar setzen der auch in Mails und Formularen benutzt werden kann.

Das Formular und der Kommentar lässt sich bei bestehenden Rechnungen editieren.

#### Neue Buttons bei Druck und Mail Views

Bei den Druck und Mail Views gibt es neu die folgenden Buttons:
* Variablen anzeigen: Öffnet den Dialog der die Variablen anzeigt die für den aktuellen Report geeignet sind. Diese lassen sich  zum Kopieren in die Zwischenablage auswählen um sie dann in den Text zu platzieren
* Vorschau: Zeigt eine Vorschau des Mail Textes. Wird ein Mitglied ausgewählt, dann werden seine Daten verwendet
* Als Vorlage übernehmen: Übernimmt den aktuellen Text als Vorlage. Eine bestehende Vorlage lässt sich überschreiben

#### Spendenbescheinigungen über das Buchung Kontextmenü erzeugen

Über das Kontextmenü einer Buchung lässt sich direkt eine Geldspendenbescheinigung erzeugen ohne der Notwendigkeit ein Mitglied bzw. Nicht-Mitglied zu erzeugen und ohne eine Sollbuchung zuordnen zu müssen.

#### Differenzfilter mit Limit

In den Filtern für Sollbuchungen und Kontoauszüge lässt sich ein Limit für die Differenz konfigurieren. Bei  Differenz Fehlbetrag werden nur Sollbuchungen bzw. Mitglieder ausgewählt bei denen der Fehlbetrag größer als das Limit ist. Bei Überzahlung nur wenn der über zahlte Betrag größer als das Limit ist.

## Kleinere Korrekturen und Erweiterungen

* Reports starten in der Fußzeile wieder mit Seite 1 statt mit 0
* Weitere Filter im Wiedervorlage Liste View

