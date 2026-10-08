# Installation

OpenJVerein ist ein Plugin innerhalb von Jameica, daher muss zuerst Jameica installiert werden.

## Jameica-Installation

Die zum Betriebssystem passende Jameica-Version ist von [http://www.willuhn.de/products/jameica/download.php](http://www.willuhn.de/products/jameica/download.php) herunter zu laden. Sofern Jameica in einer älteren Version bereits installiert ist, ist das Verzeichnis entweder umzubenennen oder zu löschen. Die heruntergeladene ZIP-Datei ist an der gewünschten Stelle zu entpacken \(z. B. C:\Programme\). In dem entpackten Verzeichnis die zum verwendeten Betriebssystem passende Startdatei starten.

- Linux ./jameica.sh
- Windows jameica-win64.exe
- MacOS Doppelklick auf das Jameica-Symbol

Die Installation von Java ist nur noch bei Linux-Systemen notwendig, bei Windows und MacOS ist diese bereits in Jameica enthalten.

## Der erste Start

Bei jedem Start, bzw. solange nichts Gegenteiliges eingestellt wurde (z.B. "Künftig immer diesen Ordner verwenden"), wird der Benutzerordner abgefragt:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/aller_anfang_-_erster_start_-_anlegen_des_benutzerordners.png" alt="" /></picture>

Dies bietet daher auch die Option mehrere Vereine zu verwalten: diese müssen lediglich verschiedene Benutzerordner haben. Nach der Bestätigung des Ordner wird ein "Master"Passwort benötigt:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/aller_anfang_-_erster_start_-_passwort_festlegen.png" alt="" /></picture>

Nach der Vergabe eines Masterpasswortes, gelangt man zur Hauptübersicht von Jameica.

## JVerein-Installation

Oben im Hauptmenü auf "Datei" -> "Plugins online suchen", Tab "Verfügbare Plugins" -> Im Select "https://openjverein.github.io/jameica-repository" auswahlen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/install6.png" alt="" /></picture>

Passende JVerein-Version auswählen und "Installieren..." anklicken.

Für die Nutzung von OpenJVerein ist das Banking-Plugin Hibiscus erforderlich. Wenn dieses noch nicht installiert ist, erscheint folgendes Fenster, dass mit "Ja" bestätigt werden muss.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/install15.png" alt="" /></picture>

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/install7.png" alt="" /></picture>

"Ja" anklicken.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/install9.png" alt="" /></picture>

Passenden Plugin-Ordner auswählen. Wichtig! Eine einmal getroffene Auswahl sollte beibehalten werden.

Nun werden OpenJVerein und ggf. Hibiscus heruntergeladen. Sobald das abgeschlossen ist, erscheint eine Erfolgsmeldung und Jameica muss beenden und neu gestartet werden.

### Wichtig

Die Installation muss immer auf dem oben beschriebenen Weg erfolgen. Das direkte Entpacken in das Plugins-Verzeichnnis wird nicht empfohlen.

## MySQL/MariaDB

JVerein unterstützt auch MySQL/MariaDB. Zur Installation siehe [MySQL-Support.](mysql-support.md)
