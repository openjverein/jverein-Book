# OpenOfficeDB

## H2 Datenbank mit OpenOffice-Base öffnen

**Wichtig!** Beim Zugriff mit OpenOffice-Base auf die JVerein-Datenbank muss JVerein geschlossen sein.

## H2.jar in den Classpath aufnehmen

Die Bibliothek h2.jar mit dem Datenbank-Treiber ist in den OpenOffice-Classpath aufzunehmen. Dazu irgendein OpenOffice-Modul \(z. B. Writer\) öffnen. Unter Extras&gt;Optionen&gt;OpenOffice.org&gt;Java&gt;Class Path den Pfad zur h2.jar auswählen \(Archiv hinzufügen\). Im Normalfall ist die Bibliothek im Jameica-Verzeichnis im Lib-Verzeichnis vorhanden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/oobaseh2classpath1.png" alt="" /></picture>

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/oobaseh2classpath2.png" alt="" /></picture>

## Datenbankassistent

OpenOffice-Base aufrufen.

Im Datenbankassistenten den Punkt "Verbindung zu einer bestehenden Datenbank herstellen" auswählen. Im dazugehörigen Dropdown-Menü die Standardeinstellung "JDBC" übernehmen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/oobaseh2datenbankassistent0.png" alt="" /></picture>

Im Feld "URL der Datenquelle" muss der Pfad zu H2-Datenbank eingetragen werden. Der Pfad beginnt mit h2: \(Linux\) bzw. h2:file: \(Windows\):

Beispiele:

Linux: `h2:/home/heiner/jameica.buch/jverein/h2db/jverein`

Windows: `h2:file:C:/Pfad/zur/Datenbank/.jameica/jverein/h2db/jverein`

Unter JDBC-Treiberklasse muss der Datenbanktreiber eingetragen werden: `org.h2.Driver`

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/oobaseh2datenbankassistent1.png" alt="" /></picture>

Nach einem Klick auf Weiter müssen die Zugangsdaten zur Datenbank eingetragen werden:

Benutzername: `jverein,` Kennwort erforderlich

Nach einem Klick auf "Verbindungstest" kann das Passwort eingegeben werden

Passwort: `jverein`

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/oobaseh2datenbankassistent2.png" alt="" /></picture>

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/oobaseh2passwort.png" alt="" /></picture>

Anschließend muss der Datenbank-Assistenten angewiesen werden die Datenbank anzumelden und sie anschließend zum Bearbeiten zu öffnen.

Nach einem Klick auf "Fertigstellen" muss die neu geschaffene OpenOffice-Datenbank gespeichert werden. Die OpenOffice-Datenbank dient praktisch als Hülle. Hier wird der Zugang zur JVerein-Datenbank, sowie eure in OpenOffice angelegten Abfragen u.ä. gespeichert. Hierzu einfach einen beliebigen Dateinamen und Speicherort angeben.

Anschließend öffnet sich OpenOffice-Base. Wenn alles geklappt hat fragt Base nun nach Benutzernamen und Passwort für die Datenbank. Hier erneut die oben angegebenen Daten eingeben.

Nun solltet ihr unter "Tabellen" einen Reiter "JVEREIN" finden. Im Unterordner "PUBLIC" findet ihr alle Tabellen, die JVerein angelegt hat. Ihr könnt nun nach Herzenslust auf die Datenbank zugreifen und z.B. Abfragen erstellen.

