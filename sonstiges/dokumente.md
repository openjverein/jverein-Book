# Dokumente

## Allgemein

Zu Mitgliedern und Buchungen können Dokumente beliebiger Art und Anzahl gespeichert werden. 

Es gibt ab der Version 5.0 zwei Möglichkeiten Dokumente zu speichern. Entweder als lokale Speicherung (neu) oder wie bisher über Jameica Messaging.

Unter Administration->Einstellungen->Anzeige lässt sich Dokumentspeicherung aktivieren und die Speichermethode auswählen.

## Voraussetzungen für Jameica Messaging

Die Dokumentenarchivierung wird über den ArchiveService von [http://www.willuhn.de/products/jameica](http://www.willuhn.de/products/jameica) realisiert. Entweder erfolgt die Installation lokal oder innerhalb eines LANs. Bei der Installation im LAN wird in einer Jameica-Instanz der Archive-Service installiert und gestartet. In den weiteren Jameica-Instanzen ist keine Installation erforderlich. Jameica findet die zentrale Instanz automatisch im LAN. Unter Einstellungen ist die Dokumentenspeicherung zu aktivieren.

Für den ArchiveService müssen folgende Jameica-Plugins zusätzlich installiert werden:

* jameica.messaging
* jameica.soap
* jameica.webadmin
* jameica.xmlrpc


## Voraussetzungen für die lokale Speicherung

Für die lokale Speicherung muss der Dateipfad konfiguriert werden. Er besteht aus:
* einem festen Wurzelverzeichnis Anteil der unter Administration->Einstellungen->Belege konfiguriert wird. Als Defaultwert sind hier Pfade in das Jameica Verzeichnis gesetzt
* einem Pfad relativ zum Wurzelverzeichnisse Anteil. Dieser wird unter Administration->Einstellungen->Vorlagen konfiguriert und kann Variablen enthalten

PS: Der relative Pfadanteil wird in der Datenbank zum Dokument gespeichert. Der Wurzelverzeichnisse Anteil wird lokal auf dem Rechner gespeichert. Wird z.B. der komplette Datensatz mit Datenbank und den gespeicherten Dokumenten auf einen anderen Rechner oder auch lokal in ein anderes Verzeichnis verschoben, muss nur der Wurzelverzeichnisse  Anteil neu gesetzt werden.


## Dokumentliste

Alle bestehenden Dokumente können ab der Version 5.0 in einer Liste angezeigt werden. Siehe hierzu die Beschreibung unter Buchführung->Belege.

## Dokumente in Buchungen und Mitglieder

Bei aktivierter Dokumentspeicherung werden die zugeordneten Dokumente bei der entsprechenden Buchung oder dem Mitglied angezeigt.

Liste er Dokumente z.B. in Buchung:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/dokumenteneu1.png" alt="" /></picture>

Ab Version 4.3:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_DokumenteListe.png" alt="" /></picture>

Folgende Buttons sind vorhanden:
* Neues Dokument: Neues Dokument erzeugen

Folgende Menü Einträge sind vorhanden:
* Anzeigen: Öffnet das Dokument in einer externen Applikation und zeigt es an
* Infos bearbeiten: Öffnet den Dokument Datensatz zum Bearbeiten
* Löschen: Löscht das Dokument


Ab Version 5.0:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegeDetailListe.png" alt="" /></picture>

Folgende Buttons sind vorhanden:
* Neu: Neuen Beleg erzeugen
* Beleg Zuordnen: Ordnet einen bestehenden Beleg zu

Folgende Menü Einträge sind vorhanden:
* Bearbeiten: Öffnet den Beleg Datensatz zum Bearbeiten
* Anzeigen: Öffnet das Dokument in einer externen Applikation und zeigt es an
* Beleg aus Buchung entfernen: Löscht die Dokumentzuordnung, der Beleg selbst bleibt bestehen
* Löschen: Löscht den Beleg


## Neues Dokument

Über den Button "Neues Dokument" lässt sich ein Dokument hinzufügen. Es öffnet sich folgendes Formular:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/dokumenteneu2.png" alt="" /></picture>

Ab Version 4.3:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_DokumenteNeuDialog.png" alt="" /></picture>

Folgende Eingabefelder sind vorhanden:
* Datei: Hier wird die Datei ausgewählt, die als Dokument gespeichert wird
* Datum: Hinterlegtes Datum
* Bemerkung: Text zum Dokument

Es wird eine Datei ausgewählt. Standardmäßig wird das Tagesdatum vorgegeben. Zusätzlich kann zu jedem Dokument ein Kommentar eingetragen werden.

Ab 4.2 lässt sich das Datum nicht mehr nachträglich ändern.

Ab Version 5.0:

Mit dem Neu Button wird ein neuer Beleg angelegt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/500_BelegNeuView.png" alt="" /></picture>

Folgende Eingabefelder sind vorhanden:
* Belegart: Sie bestimmt welcher Pfad zum Speichern verwendet wird und wie die Belegnummer generiert wird
* Datum: Hinterlegtes Datum
* Bemerkung: Text zum Beleg
* Datei: Hier wird die Datei ausgewählt, die als Beleg gespeichert wird

## Liste der Buchungen oder Mitglieder

Bei zugeordneten Belegen werden die Belegnummern in der Liste der Buchungen bzw. der Mitglieder in einer Spalte angezeigt.

## Datensicherung

Die gespeicherten Dokumente werden **nicht** durch die Sicherung von Jameica erfasst. Am einfachsten ist es, dass .jameica-Verzeichnis komplett zu sichern.

