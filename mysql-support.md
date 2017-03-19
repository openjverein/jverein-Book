# MySQL-Support

## Vorbemerkungen

JVerein verwendet standardmäßig eine embedded Datenbank \(H2\), die beim ersten Start automatisch eingerichtet wird. Seit JVerein 1.0 wird auch MySQL unterstützt. 

## Erstellung der MySQL-Datenbank

Verwenden Sie Ihr bevorzugtes Administrationswerkzeug \(z.Bsp. PhpMyAdmin \[[http://www.phpmyadmin.net/](http://www.phpmyadmin.net/)\] oder MySQL-Administrator\[[http://dev.mysql.com/downloads/gui-tools/5.0.html](http://dev.mysql.com/downloads/gui-tools/5.0.html)\]\), um eine Datenbank mit dem Namen "jverein" sowie einen Benutzer anzulegen oder führen Sie folgende Kommandos aus, um Datenbank und Benutzer mit dem Kommandozeilen-Werkzeug "mysql" \("mysql.exe" unter Windows\) anzulegen. Der angelegte Benutzer muss Lese- und Schreibrechte in dieser Datenbank besitzen.

* Als Benutzer root auf der Datenbank anmelden: `mysql -u root -p `\(girls. mit Pfadangabe vor mysql oder Anpassung von PATH\)
* Datenbank anlegen: `mysql> create database jverein;`
* Benutzer anlegen: Wenn die Datenbank im ganzen Intranet erreichbar sein soll, verwenden Sie statt "localhost" beispielsweise "192.168.1.%", wenn die IP-Adressen aller PCs in Ihrem LAN mit "192.168.1." beginnen oder "%", wenn keine Einschränkungen gelten sollen.
  * `mysql> CREATE USER 'jverein'@'localhost' IDENTIFIED BY '<passwort>';`
  * `mysql> GRANT ALL PRIVILEGES ON jverein.* TO 'jverein'@'localhost';`





