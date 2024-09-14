# Spendenbescheinigung

Mit JVerein können Spendenbescheinigungen ausgestellt und gespeichert werden. Vorbereitend können ein oder mehrere [Formulare](../administration/mitglieder/formulare.md) für den individuellen Druck eingerichtet werden.

## Allgemeines

JVerein unterstützt das Erstellen von Spendenbescheinigungen für:
* Sachspenden
* Aufwandsspenden
* Vergütungsspenden (Rückspenden)
* Leistungsspenden
* Geldspenden

Im View Spendenbescheinigungen werden bereits erstellte Spendenbescheinigungen angezeigt.

Der Filterbereich erlaubt es nach verschiedenen Kriterien zu filtern.

Über den Filter "Mail" lassen sich z.B. Spendenbescheinigungen finden für deren Spender keine Mail Adressen hinterlegt sind. Diese können dann nicht per Mail verschickt werden sondern nur per Brief.

![](../../assets/spendenbescheinigungen.png)

In der Liste können ein oder mehrere Einträge markiert werden. Über ein Kontextmenu \(rechter Mausklick\) stehen verschiedene Aktionen zur Verfügung.

![](../../assets/spendenbescheinigung_menu3.png)

Damit können Spendenbescheinigungen gelöscht oder als Vorlage gespeichert werden.

Mit einem Doppelklick auf eine Spendenbescheinigung öffnet sich das Bearbeitungsfenster.

Es ist möglich eine Mail an den Spender zu schreiben oder die ausgewählten Spendenbescheinigungen zu drucken oder per Mail an die Spender zu schicken. Eine Beschreibung zum Drucken und Verschicken siehe [Spendenbescheinigungen](../druckmail/spendenbescheinigungen.md).

Sind mehrere Einträge markiert, wird die Aktion auf alle markierten Einträge angewendet. Das Drucken beschränkt sich darauf, die Dokumente in dem in den Einstellungen angegebenen Verzeichnis zu speichern.

## Sachspendenbescheinigungen erstellen

Sachspendenbescheinigungen können auf verschiedene Art erzeugt werden:

* In der Mitgliedersuche kann man mit einem Klick auf die rechte Maustaste ein Kontextmenü öffnen. Darin den Menüpunkt Sachspendenbescheinigung auswählen. Es wird das Spendenbescheinigungsformular mit den Daten des Mitglieds gefüllt.

  ![](../../assets/spendenbescheinigung_menu1.png)

* Alternativ kann im Mitglieds View unter dem Tab Mitgliedskonto das Mitglied ausgewählt werden. Mit einem Klick auf die rechte Maustaste öffnet sich ein Kontextmenü um die Spendenbescheinigungen zu erstellen. Es wird das Spendenbescheinigungsformular mit den Daten des Mitglieds gefüllt.

  ![](../../assets/spendenbescheinigung_menu2.png)

* In der Detailansicht einer Spendenbescheinigung kann über den Button "Neu \(Sachspende\)" eine neue Spendenbescheinigung erstellt werden. Es werden die Spender Daten aus der bisher angezeigten Spendenbescheinigung übernommen. Zu beachten ist, dass auch die Referenz auf das Mitglied übernommen wird. Wird die Spendenbescheinigung später per Mail versendet, wird sie an dieses Mitglied verschickt auch wenn man die Spender Daten ändert!

* Als vierte Möglichkeit kann in der Liste Spendenbescheinigungen der Button "Neu \(Sachspende\)" gedrückt werden. Da hier kein Mitglied ausgewählt ist müssen die Daten des Spenders eingetragen werden. Es ist zu beachten, dass dabei kein Bezug zu einem Mitglied hergestellt wird und darum z.B. ein Versenden per Mail aus JVerein heraus später nicht möglich ist da keine Mail Adresse hinterlegt ist.

## Spendenbescheinigung für Aufwandsspenden, Vergütungsspendespenden (Rückspende) und Leistungsspenden erstellen

Bei dieser Art von Spende handelt es sich um den Verzicht auf Erstattung von Aufwand, Vergütung oder Leistungen. Diese werden über die Spendenart Geldspende bescheinigt wobei auf dem Spendenformular die Frage nach dem Verzicht auf Aufwendungen mit Ja beantwortet wird.

In JVerein kann diese Art der Spendenbescheinigung nur über das Anlegen einer Buchung mit dem zu bescheinigenden Betrag erzeugt werden. In der Buchung ist die Checkbox "Erstattungsverzicht" zu setzen.

Das Erzeugen der Spendenbescheinigung erfolgt wie nachfolgend bei Geldspendenbescheinigungen beschrieben.

Zu beachten ist, dass bei Sammelbescheinigungen diese Art der Spende mit Geldspenden gemischt sein kann. Auf der zweiten Seite der Spendenbescheinigung wird dann für jede enthaltene Buchung ausgewiesen ob es sich um Verzicht auf Erstattung von Aufwänden handelt oder nicht.

## Geldbescheinigungen erstellen

### Voraussetzungen

Um Geldspendenbescheinigungen erstellen zu können müssen verschiedene Voraussetzungen erfüllt sein:
* Es muss eine Buchung \(Istbuchung\) in einem Konto existieren.
* Die Buchungsart der Buchung muss vom Typ Spende sein. Siehe Administration\|Buchführung\|Buchungsart Checkbox Spende.
* Die Buchung muss einer Sollbuchung zugeordnet sein.

Die Zuordnung einer Buchung zu einer Sollbuchung kann auf verschiede Arten erzeugt werden.
* Wird bei einem Abrechnungslauf bei Mitgliedern mit Lastschrift eine Sollbuchung erzeugt, wird automatisch auch eine Buchung ezeugt und diese der Sollbuchung zugeordnet.
* Wird bei einem Abrechnungslauf bei Mitgliedern ohne Lastschrift eine Sollbuchung erzeugt muss die später erfolgte Buchung manuell der Sollbuchung zugeordnet werden. Siehe [Sollbuchungen](mitgliedskonto.md).
* Wurde die Buchung ohne einen Abrechnungslauf erzeugt muss eine Sollbuchung erzeugt und die Buchung zugeordnet werden. Dies kann in einem Schritt erfolgen. Siehe zweite Option in [Sollbuchungen](mitgliedskonto.md).
* Alternativ besteht natürlich die Möglichkeit manuell eine Sollbuchung zu erzeugen und ihr später die Buchung zuzuordnen. Für das Erstellen einer Sollbuchung siehe [Mitgliedskonto](content/mitgliedskonto.md).

### Geldspendenbescheinigung manuell erstellen

Ähnlich einer Sachspendenbescheinigungen kann eine Geldspendenbescheinigung manuell erzeugt werden:

* Im Mitglieds View unter dem Tab Mitgliedskonto eine Istbuchung auswählen \(Buchung mit Euro Symbol\). Mit einem Klick auf die rechte Maustaste öffnet sich ein Kontextmenü um die Geldspendenbescheinigung zu erstellen. In diesem Fall werden die Mitgliedsdaten komplett in die Spendenbescheinigung übernommen, die Buchung bestimmt den Betrag und das Spendendatum.

  ![](../../assets/spendenbescheinigung_menu2.png)

### Geldspendenbescheinigung automatisch erstellen

Voraussetzungen für die automatische Generierung von Geldspendenbescheinigungen:

* Ein Mitglied wird nur berücksichtigt wenn Straße, Postleitzahl und Ort eingetragen ist.
* Der Betrag der Bescheinigung muss gleich oder größer sein als der Mindestbetrag der unter Administration\|Einstellungen\|Spendenbescheinigungen eingetragen ist.

Bei der automatischen Generierung werden nur die Buchungen erfasst, die noch keiner Spendenbescheinigung oder Sammelbestätigung zugewiesen wurden. Es werden niemals für eine Buchung mehrere Bescheinigungen generiert.

Werden für ein Mitglied mehrere Buchungen gefunden werden sie zu einer Sammelbestätigung zusammen gefasst.

Geldspendenbescheiniguungen können automatisch auf mehrere Arten erzeugt werden:

* In der Mitgliedersuche kann man mit einem Klick auf die rechte Maustaste ein Kontextmenü öffnen. Darin den Menüpunkt Geldspendenbescheinigung auswählen. In diesem Fall werden die Mitgliedsdaten komplett in die Spendenbescheinigung übernommen, die erste Buchung bestimmt das Spendendatum, der Betrag ist die Summe der Beträge aller Buchungen.

  ![](../../assets/spendenbescheinigung_menu1.png)

* Alternativ kann im Mitglieds View unter dem Tab Mitgliedskonto das Mitglied ausgewählt werden. Mit einem Klick auf die rechte Maustaste öffnet sich ein Kontextmenü um die Spendenbescheinigungen zu erstellen. In diesem Fall werden die Mitgliedsdaten komplett in die Spendenbescheinigung übernommen, die erste Buchung bestimmt das Spendendatum, der Betrag ist die Summe der Beträge aller Buchungen.

  ![](../../assets/spendenbescheinigung_menu2.png)

* In der Übersicht über Spendenbescheinigungen können über den Button \"Neu \(Automatisch\)\" Geldspendenbescheinigungen generiert werden.


  ![](../../assets/spendenbescheinigung_auto.png)

In der Übersicht werden zunächst alle Namen und Buchungen angezeigt, die schließlich als Spendenbescheinigung angelegt werden. Der Typ der Spendenbescheinigungen \(Einzel / Sammel\) macht sich an der Anzahl Buchungen fest, die erfasst wurden.

Über den Button _Erstellen_ werden die Spendenbescheinigungen erzeugt.

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

Mögliche Einstellungen zu Spendenbescheinigungen siehe [Einstellungen](../administration/einstellungen.md).
