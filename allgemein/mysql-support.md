# MySQL-Support

## Vorbemerkungen

JVerein verwendet standardmäßig eine embedded Datenbank \(H2\), die beim ersten Start automatisch eingerichtet wird. Seit JVerein 1.0 wird auch MySQL unterstützt.

## Erstellung der MySQL-Datenbank

Verwenden Sie Ihr bevorzugtes Administrationswerkzeug \(z.Bsp. PhpMyAdmin \[[http://www.phpmyadmin.net/](http://www.phpmyadmin.net/)\] oder MySQL-Administrator\[[http://dev.mysql.com/downloads/gui-tools/5.0.html](http://dev.mysql.com/downloads/gui-tools/5.0.html)\]\), um eine Datenbank mit dem Namen "jverein" sowie einen Benutzer anzulegen oder führen Sie folgende Kommandos aus, um Datenbank und Benutzer mit dem Kommandozeilen-Werkzeug "mysql" \("mysql.exe" unter Windows\) anzulegen. Der angelegte Benutzer muss Lese- und Schreibrechte in dieser Datenbank besitzen.

* Als Benutzer root auf der Datenbank anmelden: `mysql -u root -p`\(girls. mit Pfadangabe vor mysql oder Anpassung von PATH\)
* Datenbank anlegen: `mysql> create database jverein;`
* Benutzer anlegen: Wenn die Datenbank im ganzen Intranet erreichbar sein soll, verwenden Sie statt "localhost" beispielsweise "192.168.1.%", wenn die IP-Adressen aller PCs in Ihrem LAN mit "192.168.1." beginnen oder "%", wenn keine Einschränkungen gelten sollen.
  * `mysql> CREATE USER 'jverein'@'localhost' IDENTIFIED BY '<passwort>';`
  * `mysql> GRANT ALL PRIVILEGES ON jverein.* TO 'jverein'@'localhost';`

## Erstellung eines Install-Bundles und der Datenbank

Damit JVerein auf eine MySQL-Datenbank zugreifen kann, muss eine Konfigurationdatei angepasst werden. Da diese beim ersten Start noch nicht existiert, würde JVerein auf jedem Arbeitsplatz unnötig eine Embedded H2-Datenbank anlegen, die anschliessend nicht gebraucht wird. Bereiten Sie daher mit den folgenden Schritten ein vorkonfiguriertes Bundle vor, welches anschließend einfach 1:1 auf alle Arbeitsplatz-PCs kopiert werden kann.

* Installieren sie wie beschrieben. Falls sie ein "heterogenes" Netz mit Windows- und Linux-Arbeitsplätzen nutzen, dann verwenden Sie die All-In-One-Version von Jameica, welche unter beiden Betriebssystemen lauffähig ist. Andernfalls können Sie die Windows- oder Linux-Version verwenden.
* Erstellen Sie nun manuell ein Verzeichnis "cfg" im Programm-Verzeichnis von Jameica.
* Erstellen Sie in diesem Verzeichnis eine Datei mit dem Namen "de.jost\_net.JVerein.rmi.JVereinDBService.properties". Öffnen Sie diese mit einem Texteditor und tragen Sie folgenden Inhalt ein:

`database.driver=de.jost_net.JVerein.server.DBSupportMySqlImpl`

`database.driver.mysql.jdbcurl=jdbc\:mysql\://<Server-IP>\:<port>/<datenbankname>?useUnicode\=Yes&characterEncoding\=ISO8859_1`

`database.driver.mysql.username=<Username des MySQL-Users>`

`database.driver.mysql.password=<Passwort des MySQL-Users>`

`database.driver.mysql.scriptprefix=mysql-`

* Ersetzen Sie die Werte &lt;datenbankname&gt;, &lt;port&gt;, &lt;Username des MySQL-Users&gt;, &lt;Server-IP&gt; und &lt;Passwort des MySQL-Users&gt; durch den Datenbanknamen, den Hostnamenoder die IP-Adresse des MySQL-Servers, den Port \(Standard: 3306\), sowie Username und Passwort des MySQL-Benutzers. \(Siehe folgender Schritt für die Einrichtung der Datenbank\).
* Erstellen Sie auf der MySQL-Datenbank auf dem Server einen neuen Benutzer sowie eine Datenbank mit einem beliebigen Namen. Der angelegte Benutzer muss Lese- und Schreibrechte in dieser Datenbank besitzen.

## Test und Verteilung auf die Arbeitsplätze

**Wichtig:** Die gerade manuell erstellte Konfigurations-Datei wird nur dann verwendet, wenn noch kein Jameica-Benutzerverzeichnis mit abweichenden Angaben existiert. Prüfen Sie also vor dem ersten Start, ob dieses existiert und benennen Sie es ggf. während des Tests um:

### Linux

/home/&lt;username&gt;/.jameica

### Windows

C:\Dokumente und Einstellungen\&lt;username&gt;.jameica

* Starten Sie nun diese Jameica-Installation durch Aufruf von "jameica.sh" bzw. "jameica.bat". JVerein sollte nun keine eigene Datenbank erstellen sondern stattdessen direkt auf die MySQL-Datenbank zugreifen.
* Verteilen Sie nun das vorkonfigurierte Install-Bundle \(im Beispiel also "C:\download\jameica"\) auf alle teilnehmenden Arbeitsplatz-PCs.
* Beachten Sie, daß auch auf den anderen Arbeitsplatz-PCs noch kein Jameica-Benutzerverzeichnis existieren darf, da sonst die dort angegebene Datenbank-Konfiguration \(welche auf die interne H2-Datenbank verweist\) verwendet wird.

Hinweis: Auf allen Arbeitsplätzen muss die gleiche Version von JVerein im Einsatz sein. Durch neue Versionen wird u. U. die Datenbankstruktur so verändert, dass ältere Versionen damit nicht klar kommen.

## Sicherheitshinweise

Nutzen Sie MySQL nur in gesicherten und vertrauenswürdigen Intranets, da die Datenübertragung von MySQL standardmäßig unverschlüsselt erfolgt. Lesen Sie alternativ die MySQL-Dokumentation zu Grundlegenden SSL-Konzepten sowie der Einrichtung von SSL für MySQL. Die manuelle Erstellung sowie der Import des Server-Zertifikats sollte auf den Arbeitsplätzen jedoch nicht nötig sein, da Jameica einen eigenen Keystore verwendet und den Benutzer automatisch bei Bedarf zum Import des Zertifikats auffordert.

### Probleme

Unter Ubuntu: Das Paket libmysql-java muss installiert sein.

Außerdem gibt es bei 16.04 Xenial das Problem dass phpmyadmin eine missing gettext dependency hat, das Paket php-gettext muss manuell installiert werden. Siehe auch [https://bugs.launchpad.net/ubuntu/+source/phpmyadmin/+bug/1569128](https://bugs.launchpad.net/ubuntu/+source/phpmyadmin/+bug/1569128)

