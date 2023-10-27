# Dokumente

## Voraussetzungen

Die Dokumentenarchivierung wird über den ArchiveService von [http://www.willuhn.de/products/jameica](http://www.willuhn.de/products/jameica) realisiert. Entweder erfolgt die Installation lokal oder innerhalb eines LANs. Bei der Installation im LAN wird in einer Jameica-Instanz der Archive-Service installiert und gestartet. In den weiteren Jameica-Instanzen ist keine Installation erforderlich. Jameica findet die zentrale Instanz automatisch im LAN. Unter Einstellungen ist die Dokumentenspeicherung zu aktivieren.

Für den ArchiveService müssen folgende Jameica-Plugins zusätzlich installiert werden:

* jameica.messaging
* jameica.soap
* jameica.webadmin
* jameica.xmlrpc

Die Plugins stehen als Nightly-Builds unter [http://www.willuhn.de/products/jameica/download\_ext.php](http://www.willuhn.de/products/jameica/download_ext.php) zur Verfügung. Zur Installation werden die Installationsdateien in das plugins-Verzeichnis von Jameica entpackt.

## Allgemein

Zu Mitgliedern und Buchungen können Dokumente beliebiger Art und Anzahl gespeichert werden. Die Funktionalität steht nach der Installation der zusätzlichen Plugins ohne weitere Konfiguration zur Verfügung.

## Neue Dokument speichern

![](../assets/dokumenteneu1.png)

Mit einem Klick auf neu öffnet sich folgendes Formular:

![](../assets/dokumenteneu2.png)

Es wird eine Datei ausgewählt. Standardmässig wird das Tagesdatum vorgegeben. Es kann hier z. B. auch das Datum des Beleges eingetragen werden. Zusätzlich kann zu jedem Dokument ein Kommentar eingetragen werden.

## Dokumente anzeigen oder löschen

Mit einem Rechtsklick auf ein Dokument öffnet sich ein Kontextmenü. Mit den Menüpunkten kann ein Dokument entweder angezeigt oder gelöscht werden.

## Datensicherung

Die gespeicherten Dokumente werden **nicht** durch die Sicherung von Jameica erfasst. Am einfachsten ist es, dass .jameica-Verzeichns komplett zu sichern.

