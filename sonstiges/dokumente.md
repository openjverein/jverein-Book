# Dokumente

## Allgemein

Zu Mitgliedern und Buchungen können Dokumente beliebiger Art und Anzahl gespeichert werden. 

Es gibt ab der Version 4.3 zwei Möglichkeiten Dokumente zu speichern. Entweder als lokale Speicherung (neu) oder wie bisher über Jameica Messaging.

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
* einem festen Root Anteil der unter Administration->Einstellungen->Verzeichnisse konfiguriert wird. Als Defaultwert sind hier Pfade in das Jameica Verzeichnis gesetzt
* einem Pfad relativ zum Root Anteil. Dieser wird unter Administration->Einstellungen->Vorlagen konfiguriert und kann Variablen aus dem Mitglied bzw. der Buchung enthalten

PS: Der relative Pfadanteil wird in der Datenbank zum Dokument gespeichert. Der Root Anteil wird lokal auf dem Rechner gespeichert. Wird z.B. der komplette Datensatz mit Datenbank und den gespeicherten Dokumenten auf einen anderen Rechner oder auch lokal in ein anderes Verzeichnis verschoben, muss nur der Root Anteil neu gesetzt werden.


## Neue Dokument speichern

Liste er Dokumente:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/dokumenteneu1.png" alt="" /></picture>

Ab Version 4.3:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_DokumenteListe.png" alt="" /></picture>

Bei lokalen Dokumenten wird in der Liste auch der lokale Pfad angezeigt.

Über den Button "Neues Dokument" lässt sich ein Dokument hinzufügen. Es öffnet sich folgendes Formular:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/dokumenteneu2.png" alt="" /></picture>

Ab Version 4.3:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_DokumenteNeuDialog.png" alt="" /></picture>

Es wird eine Datei ausgewählt. Standardmäßig wird das Tagesdatum vorgegeben. Zusätzlich kann zu jedem Dokument ein Kommentar eingetragen werden.

Ab 4.2 lässt sich das Datum nicht mehr konfigurieren, es ist immer das Datum an dem der Beleg hinzugefügt wurde.

## Dokumente anzeigen oder löschen

Mit einem Rechtsklick auf ein Dokument öffnet sich ein Kontextmenü. Mit den Menüpunkten kann ein Dokument entweder angezeigt oder gelöscht werden. Auch lässt sich die Info anzeigen.

## Datensicherung

Die gespeicherten Dokumente werden **nicht** durch die Sicherung von Jameica erfasst. Am einfachsten ist es, dass .jameica-Verzeichnis komplett zu sichern.

