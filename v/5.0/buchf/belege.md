# Belege

## Aktivierung

Zur Nutzung der Beleg ist die Option unter Administration->Einstellungen->Anzeige Dokumentenspeicherung zu aktivieren.


## Einstellungen

Unter Administration->Einstellungen->Belege können die Wurzelverzeichnisse für die Dokumentspeicherung gesetzt werden. Diese können geändert werden wenn die Dokumente verschoben werden bzw. auf einen anderen Benutzer übertragen werden. Die Verzeichnisse stehen nicht in der Datenbank sondern sind lokal gespeichert.

Unter Administration->Einstellungen->Vorlagen lassen sich die relativen Pfade für die Beleg mit Variablen definieren. Ein Beleg wird unter dem  Wurzelverzeichnis und dem relativen Pfad zusammengesetzt.


## Liste der Belege

In der Liste werden alle Belege aufgelistet und können nach verschiedenen Kriterien gefiltert werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegeListeView.png" alt="" /></picture>

Folgende Buttons sind vorhanden:
* Hilfe: Zeigt diese Hilfe an
* Neu: Neuen Beleg erzeugen

Folgende Menü Einträge sind vorhanden:
* Bearbeiten: Öffnet den Beleg zum Bearbeiten
* Anzeigen: Zeigt den Beleg an
* Löschen: Löscht den Beleg

## Neuer Beleg

Mit dem Neu Button wird ein neuer Beleg angelegt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegNeuView.png" alt="" /></picture>

Folgende Eingabefelder sind vorhanden:
* Belegart: Sie bestimmt welcher Pfad zum Speichern verwendet wird und wie die Belegnummer generiert wird
* Datum: Hinterlegtes Datum
* Bemerkung: Text zum Beleg
* Datei: Hier wird die Datei ausgewählt, die als Beleg gespeichert wird

Belege die hier erzeugt werden sind keiner Buchung oder keinem Mitglied zugeordnet. Das kann später in der Ansicht der Buchung oder des Mitglieds erfolgen.

## Neuer Beleg über Buchung und Mitglied erzeugen

Im Dialog eine Buchung und Mitglied werden bei aktivierter Dokumentspeicherung die zugeordneten Dokumente in einer Tabelle angezeigt. Dort lassen sich Belege neu erstellen bzw. bestehende Belege zuordnen.

Siehe hierzu [Dokumente](../../../sonstiges/dokumente.md)

Bei zugeordneten Belegen werden die Belegnummern in der Liste der Buchungen bzw. der Mitglieder in einer Spalte angezeigt.

## Beleg

Über den Bearbeiten Button kann die Beleginformation angezeigt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegView.png" alt="" /></picture>

Folgende Felder sind vorhanden:
* Belegnummer: Nummer des Belegs
* Belegart: Sie bestimmt welcher Pfad zum Speichern verwendet wird und wie die Belegnummer generiert wird
* Datum: Hinterlegtes Datum
* Bemerkung: Text zum Beleg
* Pfad: Pfad unter dem der Beleg gespeichert ist. Diese Information ist nur bei lokaler Speicherung verfügbar

In der Tabelle Buchungen werden diejenigen Buchungen aufgelistet, denen der Beleg zugeordnet ist.