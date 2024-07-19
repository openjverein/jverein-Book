# MySQL/MariaDB Support

## Vorbemerkungen

JVerein verwendet standardmäßig eine embedded Datenbank \(H2\), die beim ersten Start automatisch eingerichtet wird. Es wird auch MySQL/MariaDB unterstützt.

## Erstellung der MySQL-Datenbank

Verwenden Sie Ihr bevorzugtes Administrationswerkzeug \(z.B. [PhpMyAdmin](https://www.phpmyadmin.net/) oder [MySQL-Workbench](https://dev.mysql.com/downloads/workbench/)\), um eine Datenbank mit dem Namen "jverein" sowie einen Benutzer anzulegen. Der angelegte Benutzer muss Lese- und Schreibrechte in dieser Datenbank besitzen. Sie können auch der nachfolgenden Anleitung für die Kommandozeile folgen, um Datenbank und Benutzer mit dem Linux Kommandozeilen-Werkzeug "mysql" \("mysql.exe" unter Windows\) anzulegen. 

- Als Benutzer "root" auf dem Datenbanksystem anmelden.
- Datenbank anlegen.
- Benutzer "jverein" anlegen und Passwort vergeben. Esetzen Sie "\<passwort\>" mit dem persönlichen Kennwort für den Benutzer "jverein".
- Benutzerrechte vergeben. Wenn die Datenbank im ganzen Intranet erreichbar sein soll, verwenden Sie statt "localhost" beispielsweise "192.168.1.%", wenn die IP-Adressen aller PCs in Ihrem LAN mit "192.168.1." beginnen. Sie können auch "%" verwenden, wenn keine IP-Einschränkung gelten soll. 
<!-- -->
    mysql -u root -p
    mysql> create database jverein;
    mysql> CREATE USER 'jverein'@'localhost' IDENTIFIED BY '<passwort>';
    mysql> GRANT ALL PRIVILEGES ON jverein.* TO 'jverein'@'localhost';

## Erstellung eines Install-Bundles und der Datenbank

Damit JVerein auf eine MySQL/MariaDB-Datenbank zugreifen kann, muss eine Konfigurationdatei erstellt werden. Da diese beim ersten Start noch nicht existiert, würde JVerein auf jedem Arbeitsplatz eine H2-Datenbank anlegen, die anschliessend nicht gebraucht wird. Bereiten Sie daher mit den folgenden Schritten ein vorkonfiguriertes Install-Bundle vor, welches anschließend auf alle Arbeitsplatz-PCs kopiert wird.

- Installieren sie wie beschrieben. Falls sie ein "heterogenes" Netz mit Windows- und Linux-Arbeitsplätzen nutzen, dann verwenden Sie die All-In-One-Version von Jameica, welche unter beiden Betriebssystemen lauffähig ist. Andernfalls können Sie die Windows- oder Linux-Version verwenden.
- Erstellen Sie ein Verzeichnis "cfg" im Programm-Verzeichnis von Jameica (Ordner ".jameica").
- Erstellen Sie im cfg-Verzeichnis eine Datei mit dem Namen "de.jost\_net.JVerein.rmi.JVereinDBService.properties". 
- Öffnen Sie die Datei "de.jost\_net.JVerein.rmi.JVereinDBService.properties" mit einem Texteditor und tragen Sie folgende Inhalte ein:
<!-- -->
    database.driver=de.jost_net.JVerein.server.DBSupportMySqlImpl
    database.driver.mysql.username=<username>
    database.driver.mysql.password=<password>
    database.driver.mysql.scriptprefix=mysql-

für MySQL:

    database.driver.mysql.jdbcurl=jdbc:mysql://<ip>:<port>/<database>?useUnicode=Yes&characterEncoding=ISO8859_1

für MariaDB:

    database.driver.mysql.jdbcurl=jdbc:mariadb://<ip>:<port>/<database>?useUnicode=Yes&characterEncoding=ISO8859_1

für Jameica ab Version 2.11 (aktuell in Entwicklung)

    database.driver.mysql.jdbcdriver=org.mariadb.jdbc.Driver

- Ersetzen Sie die Werte &lt;username&gt;, &lt;password&gt;, &lt;ip&gt;, &lt;port&gt; und &lt;database&gt; durch den Benutzername und Passwort des MySQL-Benutzers, den Hostnamen/IP-Adresse des MySQL-Servers, den Port \(Standard: 3306\), sowie den Datenbanknamen. \(Siehe folgender Schritt für die Einrichtung der Datenbank\).

Bei **Datenbanksystemen ohne Serverzertifikat** muss die Zertifikatsprüfung deaktiviert werden. Setzen Sie dafür die Parameter "&trustServerCertificate=true&allowPublicKeyRetrieval=true&useSSL=false" ans Ende der Zeile von "database.driver.mysql.jdbcurl=...".

Beispiel für MySQL:

    database.driver.mysql.jdbcurl=jdbc:mysql://<ip>:<port>/<database>?useUnicode=Yes&characterEncoding=ISO8859_1&trustServerCertificate=true&allowPublicKeyRetrieval=true&useSSL=false

## Test und Verteilung der Konfiguration auf die Arbeitsplätze

**Wichtig:** Die soeben erstellte Konfigurationsdatei wird nur dann verwendet, wenn noch kein Jameica-Benutzerverzeichnis mit abweichenden Angaben existiert. Prüfen Sie also vor dem ersten Start, ob dieses existiert und benennen Sie es ggf. während des Tests um:

### Linux

    /home/<username>/.jameica

### Windows

    C:\Benutzer\<username>\.jameica

- Verteilen Sie das vorkonfigurierte Install-Bundle samt Ordnerstruktur auf alle teilnehmenden Arbeitsplatz-PCs.
- Starten Sie nun diese Jameica-Installation durch Aufruf von "jameica.sh" bzw. "jameica.bat". JVerein sollte nun keine H2-Datenbank erstellen sondern auf die MySQL/MariaDB Datenbank zugreifen.
- Beachten Sie, dass auch auf den anderen Arbeitsplatz-PCs noch kein Jameica-Benutzerverzeichnis existieren darf, da sonst die dort angegebene Datenbank-Konfiguration \(welche auf die interne H2-Datenbank verweist\) verwendet wird.

**Hinweis:** Auf allen Arbeitsplätzen muss die gleiche Version von JVerein im Einsatz sein. Durch neue Versionen wird unter Umständen die Datenbankstruktur so verändert, dass ältere Versionen damit nicht klar kommen.

## Sicherheitshinweise

Nutzen Sie MySQL/MariaDB nur in gesicherten und vertrauenswürdigen Netzwerken, da die Datenübertragung von MySQL/MariaDB ggf. unverschlüsselt erfolgt. Lesen Sie alternativ die entsprechenden Dokumentation zu Grundlegenden SSL-Konzepten sowie der Einrichtung von SSL für MySQL/MariaDB. Die manuelle Erstellung sowie der Import des Server-Zertifikats sollte auf den Arbeitsplätzen jedoch nicht nötig sein, da Jameica einen eigenen Keystore verwendet und den Benutzer automatisch bei Bedarf zum Import des Zertifikats auffordert.

### Probleme

Unter Debian/Ubuntu: Gegebenfalls muss das Paket libmariadb-java (für MariaDB und MySQL) oder libmysql-java (für MySQL) installiert werden.