# Spendenbescheinigung

Mit JVerein können Spendenbescheinigungen ausgestellt und gespeichert werden. Vorbereitend können ein oder mehrere [Formulare](../administration/mitglieder/formulare.md) für den individuellen Druck eingerichtet werden.

## Übersicht

Im View Spendenbescheinigungen werden bereits erstellte Spendenbescheinigungen angezeigt.

Der Filterbereich erlaubt es nach verschiedenen Kriterien zu filtern.

Über den Filter "Mail" lassen sich z.B. Spendenbescheinigungen finden für deren Spender keine Mail Adressen hinterlegt sind. Diese können dann nicht per Mail verschickt werden sondern nur per Brief.

![](../../assets/spendenbescheinigungen.png)

In der Liste können ein oder mehrere Einträge markiert werden. Über ein Kontextmenu \(rechter Mausklick\) stehen verschiedene Aktionen zur Verfügung:

Sind mehrere Einträge markiert, wird die Aktion auf alle markierten Einträge angewendet. Das Drucken beschränkt sich darauf, die Dokumente in dem in den Einstellungen angegebenen Verzeichnis zu speichern.

Über die Buttons in der Buttonleiste stehen die Erzeugung einer neuen bzw. die automatische Generierung \(siehe unten\) von Spendenbescheinigungen zur Verfügung.

Mit einem Doppelklick auf eine Spendenbescheinigung öffnet sich das Bearbeitungsfenster \(siehe unten\).

Mit einem Rechtsklick öffnet sich ein Kontextmenü.

![](../../assets/spendenbescheinigung_menu3.png)

Damit können Spendenbescheinigungen gelöscht oder als Vorlage gespeichert werden.

Es ist möglich eine Mail an den Spender zu schreiben oder die ausgewählten Spendenbescheinigungen per Mail an die Spender zu schicken (siehe weiter unten).

Durch einen Klick auf PDF wird die Spendenbescheinigung im PDF-Format ausgegeben. Dabei gibt es mehrere Möglichkeiten:
* PDF (Standard): Dies benötigt kein Formular und benutzt einen festen Aufbau.
* PDF (Standard, Mit Adressblatt): Dies benötigt kein Formular und benutzt einen festen Aufbau. Drucken ist gedacht wenn die Spendenbescheinigung per Brief versand werden soll. Es wird eine Anschrift auf einer zusätzlichen Seite ausgedruckt welche in ein Brieffenster passt.
* PDF (Individuell): Es wird eine Spendenbescheinigung unter Verwendung des für die Spendenbescheinigung konfigurierten Formulars erzeugt.
* PDF (Individuell, Mit Adressblatt)): Es wird eine Spendenbescheinigung unter Verwendung des für die Spendenbescheinigung konfigurierten Formulars erzeugt. Es wird eine Anschrift auf einer zusätzlichen Seite ausgedruckt welche in ein Brieffenster passt.

Tipp:

In der Mitgliedersuche kann man mit einem Klick auf die rechte Maustaste ein Kontextmenü öffnen. Darin den Menüpunkt Geldpendenbescheinigung oder Sachspendenbescheinigung auswählen. Dann wird das Spendenbescheinigungsformular mit den Daten des Mitglieds gefüllt. Geldspendenbescheinigungen werden dabei automatisch erzeugt (siehe unten).

![](../../assets/spendenbescheinigung_menu1.png)

Alternativ kann im Mitglieds View unter dem Tab Mitgliedskonto das Mitglied bzw. eine Istbuchung ausgewählt werden. Mit einem Klick auf die rechte Maustaste ein Kontextmenü um die Spendenbescheinigungen zu erstellen.

![](../../assets/spendenbescheinigung_menu2.png)

Neben der manuellen Erstellung von Spendenbescheinigungen können Geldspendenbescheinigungen auch automatisch aus dem Mitgliedskonto erzeugt werden.

Voraussetzungen für die automatische Generierung von Geldspendenbescheinigungen:

* Administration\|Allgemein Daten zum Verein und zu den Spendenbescheinigungen werden gespeichert.
* Administration\|Buchungsarten mindestens eine Buchungsart hat ein Häkchen im Feld Spende
* Buchung wurde einer Sollbuchung und einer Buchungsart mit dem Merkmal Spende zugeordnet.

Im Spendenbescheinigung View lässt sich die Spendenbescheinigung bearbeiten. Ebenso lässt sich die Spendenbescheinigung über die Drucken Buttons ausdrucken bzw. eine Sachspende mit den Spender Daten der aktuellen Spendenbescheinigung erstellen.

![](../../assets/spendenbescheinigung.png)

## Einzel- oder Sammelbestätigungen

Spendenbescheinigungen können in Form von Einzelbestätigungen oder Sammelbestätigungen erzeugt werden. Es sind zwei Formular-Arten \(Spendenbescheinigung und Sammelbestätigung\) hierfür vorgesehen.

### Einzelbestätigungen

Einzelbestätigungen können auf drei Arten erzeugt werden:

* manuell durch Eingabe aller Daten
* aus einem Mitglied / Mitgliedskonto \(rechts Klick auf Istbuchung\) heraus für eine einzelne Buchung. In diesem Fall werden die Mitgliedsdaten komplett in die Spendenbescheinigung übernommen, die Buchung bestimmt den Betrag und das Spendendatum.
* Automatische Generierung \(siehe unten\)

### Sammelbestätigungen

Sammelbestätigungen für Geldspenden können auf zwei Arten erzeugt werden:

* aus einem Mitglied oder einem Mitglied / Mitgliedskonto \(rechts Klick auf Mitgliedsname\) heraus für alle Buchungen im Mitgliedskonto. Es werden nur die Buchungen erfasst, die noch auf keiner Spendenbescheinigung oder Sammelbestätigung ausgewiesen wurden. In diesem Fall werden die Mitgliedsdaten komplett in die Spendenbescheinigung übernommen, die erste Buchung bestimmt das Spendendatum, der Betrag ist die Summe der Beträge aller Buchungen.
* Automatische Generierung \(siehe unten\)

### Automatische Generierung von Spendenbescheinigungen

In der Übersicht über Spendenbescheinigungen können über den Button \"Neu \(Geldspenden\)\" Geldspendenbescheinigungen generiert werden. Hier kommen die Einstellungen zum Tragen. Es werden nur für die Mitglieder oder Spender Spendenbescheinigungen erzeugt, die eine vollständige Adresse \(Straße und PLZ und Ort\) eingetragen haben. Außerdem werden nur die Mitglieder oder Spender erfasst, deren Spendenbetrag &gt;= dem Mindestbetrag in den Einstellungen ist.

![](../../assets/spendenbescheinigung_auto.png)

In der Übersicht werden zunächst alle Namen und Buchungen angezeigt, die schließlich als Spendenbescheinigung angelegt werden. Der Typ der Spendenbescheinigungen \(Einzel / Sammel\) macht sich an der Anzahl Buchungen fest, die erfasst wurden.

Über den Button _erstellen_ werden Spendenbescheinigungen erzeugt.

### Spendenbescheinigung \(Einzeldarstellung\)

In der Einzeldarstellung wird der Ausdruck über Buttons ebenfalls angeboten. Im Unterschied zum Druck aus der Liste heraus wird zunächst der Datei-Dialog mit der Voreinstellung des Spendenbescheinigungsverzeichnisses aus den Einstellungen und dem erzeugten Namen angeboten. Hier kann das Verzeichnis und der Name noch einmal korrigiert werden.

Der Ausdruck über die Buttons funktioniert nur, wenn die Spendenbescheinigung bereits einmal gespeichert wurde. Die Aktionen neu und drucken direkt hintereinander werden mit einer Fehlermeldung abgewiesen.


## Weitere Anpassungen

### Formulare

Vorlagen von [Formulare](../administration/mitglieder/formulare.md) können auch mehrere Seiten umfassen. Formularfelder können auch auf anderen Seiten als der ersten platziert werden \(siehe auch Formularfelder\).

### Formularfelder

Formularfelder können nun auch auf anderen Seiten als nur der ersten Seite platziert werden. Hierzu gibt es die Spalte "Seite", mit der die Seitennummer angegeben wird.

Für Spendenbescheinigungen stehen nun ergänzend folgende zusätzlichen Felder zur Verfügung:

* Spendenzeitraum Datum der ersten und letzten Buchung auf der Sammelbestätigung
* Buchungsliste
* Alle Buchungen als Liste formatiert:

`Datum Betrag Verzicht Zuwendungsart`

Für eine korrekte Formatierung sollte eine Schriftart mit fester Zeichenbereite gewählt werden.

### Einstellungen

#### Lang-Name

Langer Name des Vereins, bis 70 Zeichen

#### BegünstigterZweck

Bis zu 100 Zeichen

#### Straße

Bis zu 50 Zeichen

#### Ort

Bis zu 50 Zeichen

#### Dateinamenmuster Spende

Für die Generierung von Dokumenten mit Mitglieds-Bezug. Zunächst nur für Spendenbescheinigungen genutzt, könnte aber auch für Kontoauszug des Mitgliedskontos oder den Personalbogen genutzt werden.

#### Mindestbetrag für Spendenbescheinigungen

Allgemeine Einstellung ab welchem Betrag eine Spendenbescheinigung erstellt werden soll. Diese Einstellung kommt bei der automatischen Generierung von Spendebescheinigungen zum Tragen. Bei der Erzeugung einer Spendenbescheinigung aus einem Mitglkiedskonto heraus, wird diese Einstellung nicht beachtet.

#### Verzeichnis für Spendenbescheinigungen

Um ein flüssiges Erzeugen von mehreren Dokumenten zu ermöglichen, kann hier das Verzeichnis für die PDF-Dateien festgelegt werden. Wenn aus der Liste der Spendenbescheinigungen heraus die Dokumente generiert werden, werden sie in diese Verzeichnis geschrieben. Das Verzeichnis wird auch vorbelegt, wenn eine Dokumentenerstellung aus der Detailansicht Spendenbescheinigung erfolgt. Hier wird jedoch der Dateidialog angeboten.

#### Drucke Buchungsart

Ist das Häkchen gesetzt, wird in der Buchungsliste nicht der Zweck aus der Buchung, sondern die der Buchung zugewiesene Buchungsart verwendet. Bei sprechenden Namen eine einheitlichere Darstellung.

#### Unterschrift drucken

Ist das Häkchen gesetzt, wird beim Standard Druck eine Unterschrift in die Spendenbescheinigung eingefügt.

#### Unterschrift

Hie lässt sich ein Bild der Unterschrift einfügen welche entsprechend der selektierten Option eingefügt wird.

#### Spendenbescheinigung Anhang bei Mail Versand in DB spechern

Ist das Häkchen gesetzt, wird die Spendenbescheingung bei Mailversand zusammen mit der Mail in der Datenbank gespeichert. Öffnet man die Mail erneut wird der Anhang mit angezeigt.

