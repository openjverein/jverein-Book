# Mitglieder

## Suche

### Allgemein

Das Fenster der Mitglieder-Suche besteht aus zwei Teilen: Filter \(oben\) und Mitgliedertabelle \(unten\). Die angezeigten Mitglieder können nach verschiedenen Kriterien gefiltert werden:

* Nachname
* Mitgliedschafts-Status "Angemeldet", "Abgemeldet" und "Beide"
* Externe Mitgliedsnummer \(optional\)
* Eigenschaften
* Beitragsgruppe
* Zusatzfelder
* Geburtsdatum
* Geschlecht
* Eintritts- und Austrittsdatum

Jeweils beim Verlassen eines Feldes wird die Suche ausgelöst.

Nach einem Doppelklick auf das Mitglied werden die kompletten Daten angezeigt. Mit einem Rechtsklick auf ein Mitglied öffnet sich ein Kontextmenü. Damit kann das Mitglied bearbeitet oder gelöscht werden. Außerdem ist die Ausstellung einer [/spendenbescheinigung.md](/spendenbescheinigung.md) möglich.

Die Filterkriterien können für eine spätere Verwendung in einem [/suchprofil.md](/suchprofil.md)  gespeichert werden.![](/assets/MitgliedSuche.png)

### Filterung nach Eigenschaften

Es können eine oder mehrere Eigenschaften ausgewählt werden \(STRG-Taste beim Mausklick gedrückt halten\). Die Eigenschaften sind "und-verknüpft". D. h. es werden die Mitglieder angezeigt, die alle Eigenschaften haben.

![](/assets/Mitgliedsucheeigenschaften13.jpg)

### Filterung nach Zusatzfeldern

Soll nach Zusatzfelder gefiltert werden, kommt es auf den Datentyp des jeweiligen Zusatzfeldes an. Bei einem Ja/Nein Feld kann nur nach Ja-Einträgen gefiltert werden. Bei einem Textfeld gelten zur Filterung die SQL-Regeln für einen Textvergleich: Hier können die Wildcards % \(0...n beliebige Zeichen\) und \_ \(genau 1 beliebiges Zeichen\) eingesetzt werden. Durch die Verwendung der Kombination \_% kann man nach allen nicht leeren Textfeldern filtern.

![](/assets/MitgliedSucheZusatzfelder.jpg)

## Grunddaten des Mitglieds

![](/assets/Mitgliedgrunddaten.png)

Im oberen Teil sind die allgemeinen Daten des Mitgliedes zu finden. Wird eine Postleitzahl eingegeben, für die bereits ein Mitglied gespeichert ist, wird der entsprechende Ort übernommen.

Hinweis zur E-Mail-Adresse: In JVerein kann aktuell je Mitglied nur eine E-Mail-Adresse gespeichert werden. Hat ein Mitglied aber mehrere E-Mail-Adressen, kann man sich derzeit mit der 'Group'-Notation behelfen, Details dazu im [http://www.jverein.de/forum](http://www.jverein.de/forum).

Sofern in den [/einstellungen.md](/einstellungen.md) der Parameter "Juristische Personen erlaubt" gesetzt ist, wird bei der Neuaufnahme von Mitgliedern folgender Dialog eingeblendet:

![](/assets/MitgliedPersonenart.png)

