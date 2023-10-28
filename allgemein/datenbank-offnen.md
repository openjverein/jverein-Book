# Datenbank öffnen

## H2-Datenbank mit JDBC öffnen

Auf die H2-Datenbank kann über JDBC direkt zugegriffen werden. Dies hilft beispielsweise dabei,
Abfragen zu erstellen, einzelne Informationen aus der Datenbank auszulesen oder Serienbriefe
zu schreiben. Treiberklasse ist dabei `org.h2.Driver`, und die URL ist
`jdbc:h2:file:[Pfad];IFEXISTS=TRUE`. Der Pfad ist
* `[Benutzerordner]\jverein\h2db\jverein` unter Windows und
* `[Benutzerordner]/jverein/h2db/jverein` unter Linux.

Das Suffix `;IFEXISTS=TRUE` ist optional und verhindert nur, dass eine neue Datenbank
erstellt wird, wenn an dem angegebenen Pfad keine existiert.

Als Benutzername kann entweder `jverein` gewählt werden, wenn auch Änderungen vorgenommen
werden sollen, oder `readonly` für Lesezugriff ohne Schreibrechte. Passwort ist in beiden
Fällen `jverein`.

Der Datenbankzugriff funktioniert nur, wenn JVerein geschlossen ist.

### H2-Datenbankzugriff bei laufendem JVerein

Um bei laufendem JVerein auf die H2-Datenbank zugreifen zu können, muss die Textdatei

`[Benutzerordner]\cfg\de.jost_net.JVerein.rmi.JVereinDBService.properties`

mit dem Inhalt

`database.driver.h2.auto_server=true`

bei geschlossenem JVerein angelegt werden. Dann funktioniert der JDBC-Zugriff bei laufendem
JVerein mit der URL

`jdbc:h2:file:[Pfad];IFEXISTS=TRUE;AUTO_SERVER=TRUE`

Da es keine gute Idee ist, bei laufendem JVerein Änderungen an der Datenbank vorzunehmen,
sollte dafür der Benutzer `readonly` verwendet werden. Außerdem empfiehlt es sich, erst
JVerein zu starten und danach das Programm für den externen Zugriff. Wenn das externe Programm
vor JVerein auf die Datenbank zugreift, verliert JVerein die Verbindung zur Datenbank, wenn
das externe Programm geschlossen wird.

### H2-Datenbankzugriff mit Python

Aus Python heraus kann mit dem Paket JayDeBeApi auf die Datenbank zugegriffen werden:

`jaydebeapi.connect('org.h2.Driver', 'jdbc:h2:file:[Pfad];IFEXISTS=TRUE;AUTO_SERVER=TRUE', jars=h2_jar, driver_args=['readonly', 'jverein'])`

Dabei muss die Umgebungsvariable `JAVA_HOME` gesetzt sein; `h2_jar` ist der Pfad zum H2-Treiber,
z.B. `[Jameica-Programmordner]/lib/h2/h2-1.4.199.jar`

### H2-Datenbank mit OpenOffice/LibreOffice-Base öffnen

Die Datenbank von JVerein kann mit dem Datenbankmodul \(Base\) von  [OpenOfficeDB](openofficedb.md) bzw.
[LibreOfficeDB](libreofficedb.md) geöffnet werden.


## H2-Datenbank mit ODBC öffnen

Es ist auch möglich eine ODBC-Datenquelle für die JVerein-Datenbank einzurichten. Damit kann man z.B. mit MicroSoft-Office auf die Datenbank von JVerein zugreifen und dann z.B. \(mit Access\) Abfragen erstellen oder \(mit Word\) Serienbriefe schreiben.

Wie der Datenbankzugriff auf H2-Datenbanken allgemein eingerichtet werden kann wird unter [http://www.h2database.com/html/advanced.html\#odbc\_driver](http://www.h2database.com/html/advanced.html#odbc_driver) beschrieben. Das Verfahren setzt jedoch voraus dass ein [http://www.h2database.com/html/download.html](http://www.h2database.com/html/download.html) installiert ist und hat leider bisher nur den Status "experimentell" \(02/2014\).

