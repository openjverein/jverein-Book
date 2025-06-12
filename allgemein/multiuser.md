# Multiuser

Beitrag von DIG aus dem JVerein-Forum

## Vorbemerkungen

Jameica, Hibiscus und JVerein sind offiziell nicht multiuserfähig und haben keine ernstzunehmende Benutzerverwaltung \(d.h. mehrere Benutzer mit unterschiedlichen Berechtigungen\). Alle nachfolgend hier vorgestellten Lösungen für gemeinsamen Datenzugriff setzen also Vertrauen und klare Absprachen/Zuständigkeiten der beteiligten Benutzer untereinander voraus, so dass Datenmissbrauch und inkonsistente Daten \(z.B. durch Fehleingaben\) ausgeschlossen/vernachlässigt werden können.

Ich setze ferner voraus, dass das Thema Datenschutz von allen Beteiligten ernst genommen wird und sämtlicher Datenverkehr mit persönlichen Mitgliederdaten über öffentliche Netze stets geeignet verschlüsselt wird. Wenn ich von Netzwerkzugriff rede dann meine ich damit nicht nur den \(unverschlüsselten\) Zugriff aus einem LAN sondern schließe auch den geeignet verschlüsselten Fernzugriff über das Internet \(z.B. mittels VPN, SSH-Tunnel, SSL\) mit ein ohne diese jeweils einzeln zu erwähnen.

## Datenaustausch

Darunter verstehe ich dass z.B. unter Vorstandsmitgliedern die Daten weitergegeben werden.

### Listenweitergabe

In dieser Variante benutzt nur einer JVerein und er stattet die anderen regelmäßig mit den Listen aus JVerein aus \(z.B. Adressliste, Jubilarliste usw.\).

* Vorteile: sehr einfach und den Empfängern der Listen gibt man nicht mehr Informationen als sie auch bekommen sollen.
* Nachteile: Listen sind nicht immer aktuell und viele JVerein-Features wie bspw. die Suche oder der Mailversand stehen nicht zur Verfügung.

### Datenweitergabe

Hier haben alle Benutzer, die Daten benötigen, JVerein auf ihren Rechnern installiert und haben so den vollen Zugriff auf alle Daten und Funktionen. Alternativ kann auch die Portable-Version von Jameica+JVerein eingesetzt werden, damit muss auf den Benutzer-Rechnern nichts besonderes installiert werden.

* Vorteile: Aktuelle Daten und alle Funktionen für alle.
* Nachteile: Die regelmäßige Datenweitergabe kann lästig werden.

### Mit Schreibrecht für alle

Nach jeder Änderung müssen die Daten an alle anderen Benutzer weitergegeben werden. Dazu eignet sich das manuelle Kopieren des Datenordners auf einen USB-Stick, bequemer dürfte aber der Versand per E-Mail sein.

Die Verwendung der JVerein-Funktion "Diagnose-Backup" eignet sich hier nicht weil der Import eine leere Datenbank voraussetzt, die nach dem ersten Import aber nicht mehr leer ist. Wo man den Datenordner standardmäßig findet, ist in den FAQ nachzulesen.

### Ohne Schreibrecht für alle

Änderungen an den Daten dürfen per Definition nur von einem Verantwortlichen vorgenommen werden, er hat die 'Master'-Kopie der Daten. Alle anderen Benutzen erhalten von ihm zwar regelmäßig eine Kopie der Daten wie oben in "Mit Schreibrecht für alle" beschrieben, jede bleibende Änderung muss aber vom Verantwortlichen selber getätigt werden, die anderen Benutzer müssen Änderungswünsche an den Daten ggf. bei ihm einreichen. \(siehe auch \#Lese- und Schreibrecht\)

## Gemeinsamer Datenzugriff

Hierbei haben alle Benutzer stets den vollen Zugriff auf den aktuellen Datenstand. Da Jameica und JVerein jedoch keinen gleichzeitigen Multiuser-Zugriff unterstützen, sind geeignete Absprachen oder technische Vorkehrungen für eine Nutzung nur nacheinander zu treffen \(siehe dazu \#Lese- und Schreibrecht\).

### MySQL

In einem Netzwerk kann anstelle der sonst verwendeten H2-Datenbank ein zentraler MySQL-Datenbankservers genutzt werden. Jameica und JVerein werden auf allen Rechnern der Benutzer lokal \(empfehlenswert bei Fernzugriff\) oder auf einem Netzwerk-Share \(besser bei LAN-Zugriff\) entsprechend konfiguriert installiert. Mit MySQL können auch reine Nur-Lese-Zugriffe realisiert werden \(siehe \#Mit einer MySQL-Datenbank\).

* Vorteile: Bequemer Datenzugriff, auch anderweitig \(insbesondere mit ODBC usw.\), theoretisch Multiuser-Zugriff \(wird offiziell aber nicht unterstützt\).
* Nachteile: MySQL-Server nötig, ein etwas besseres NAS \(z.B. von QNAP oder Synology\) genügt aber oft schon.

Hinweis: Eine MySQL-Datenbank aus dem Webhostingpaket ist i.d.R. ungeeignet da der Datenbankserver bei vielen Hostern von außen gar nicht direkt erreichbar ist \(z.B. 1&1\) oder falls doch kaum SSL-verschlüsselt sein dürfte. Eine Lösung für Amazon RDS mit Verschlüsselung beschreibt Stephan im Onlinebanking-Forum

Mehr Infos zur Einrichtung einer MySQL-Datenbank gibt es unteri: [MySQL-Support](mysql-support.md)

### Cloud-Computing

Bei einem Cloud-Anbieter der Wahl wird ein Konto \(oder Space\) eingerichtet, das dann von allen Benutzern verwendet wird. Ich habe TeamDrive wegen der eingebauten Verschlüsselung schon vor der Übertragung verwendet und war zufrieden damit, bei Cloud-Anbietern ohne solche Verschlüsselung kann man z.B. mit TrueCrypt zunächst lokal dafür sorgen. Wer keinem der Cloud-Anbietern so richtig traut, kann auch seine eigene Cloud aufsetzen: OwnCloud läuft auch in einem WebSpace \(verwende ich inzwischen mit meinem 1&1-Shared-Webhosting-Paket\).

Auf allen Rechnern der Benutzer müssen stets dieselben Ordner verwendet werden \(z.B. C:\Vereinsname\) und als lokaler Ordner zum Cloudspeicher eingerichtet werden. Jameica und JVerein zusammen mit den Daten am besten komplett dorthin installieren, dann liegt bereits eine so zentrale Speicherung vor dass Updates nur einmal eingespielt werden müssen.

* Vorteile: günstig und recht einfach aufzusetzen
* Nachteile: Setzt hinreichendes Vertrauen in Cloud-Anbieter voraus und kann Geld kosten falls man mit den kostenlosen Angeboten nicht auskommt.

Wichtiger Hinweis: Nachdem man den Cloud-Dienst-Clienten gestartet hat \(bzw. nachdem man seinen Rechner eingeschaltet hat, falls dieser Dienst automatisch gestartet wird\) muss man mit dem Start von Jameica+JVerein so lange abwarten bis der Cloud-Dienst-Client die lokal gespeicherten Daten gegen die in der Cloud gespeicherten vollständig abgeglichen hat. Werden Jameica+JVerein zu früh gestartet so sind einige lokale Dateien dadurch in Bearbeitung und werden zunächst nicht sondern erst später abgeglichen. Ebenso ist stets darauf zu achten, den Cloud-Dienst-Clienten erst zu beenden \(oder den Rechner auszuschalten\) nachdem alle neu geänderten Dateien auch vollständig in die Cloud übertragen wurden. Als Folge von Nichtbeachtung können Versionskonflike auftreten, die schlimmstenfalls eine inkonsistente Datenbank \(d.h. verloren gegangene Änderungen\) bedeuten können. Eine gewisse Disziplin ist hier also von Nöten.

Weitere Infos und Erfahrungsberichte zum Cloud-Computing mit JVerein gibt es im Forum \(Suchbegriffe: z.B. Dropbox oder multiuser\)

#### Mit Schreibrecht für alle

Das ist der Standard beim Speichern in der Cloud, alle Benutzer arbeiten mit Live-Daten und können sie auch ändern.

#### Ohne Schreibrecht für alle

Analog zu "Datenweitergabe ohne Schreibrecht" führt nur ein Verantwortlicher Änderungen an den Daten durch. Der Verantwortliche hat dazu zwei Datenordner auf seinem Rechner: die 'Master'-Kopie der Daten, die nicht in der Cloud gespeichrt sein muss \(aber kann\), und die Benutzer-Kopie, die in der Cloud liegt. Nach jeder Änderung durch den Verantwortlichen kopiert dieser die Daten von seiner 'Master'-Kopie in die Benutzer-Kopie in der Cloud. \(siehe auch \#Lese- und Schreibrecht\)

### Terminal-Server und Verwandte

Hat man die Möglichkeit einen \(Windows\) Terminal-Server zu nutzen \(oder XTerminals bei Linux\), so arbeiten alle Benutzer auf dem selben Rechner, mit zentral gespeicherten Daten und Programmen. Es ist nur eine Jameica und JVerein-Installation nötig, die allerdings nicht in einem Benutzerordner sondern in für alle zugänglichen Ordnern sein muss.

* Vorteile: zentral administrierbar und kann die komplette Arbeitsumgebung \(d.h. auch Office-Anwendungen usw.\) enthalten.
* Nachteile: kräftiger Server, Betrieb und ggf. Lizenzen sowie ein guter Sysadmin nötig, damit wohl recht teuer und eher nur etwas für die Profiliga. Man kann einen Terminal-Server aber auch mieten....

#### Terminal-Server "light"

Man nehme einen gewöhnlichen Windows-PC, aktiviere dort den Remotedesktop und schalte den Benutzerwechsel ab.

* Vorteile: Einfacher und günstiger \(es wird nur ein PC und eine Lizenz benötigt\) als ein echter Terminal-Server bei sonst gleichen Vorteilen
* Nachteile: Eine Single-User-Lösung, aber für Jameica+JVerein ja genau richtig.

### Multiuser-Setup per SVN/Subversion

Die JVerein-H2-Datenbank \(jverein.h2.db\) kann in einem zentralen Subversion-Respository gespeichert werden. Bevor Jameica/JVerein gestartet wird holt man sich zunächst den letzten Stand der Datenbank aus dem Repository und schreibt ihn ggf. nach beendeter Arbeit dorthin wieder zurück \(Commit\).

* Vorteile: Änderungshistorie \(Datenbankstände werden archiviert, welcher SVN-Benutzer hat wann geändert\), Datenbankdatei kann mit einen Schreib-Lock belegt werden \(d.h. nur ein schreibener Benutzer gleichzeitig / Lock-Modify-Write-Workflow\)
* Nachteile: SVN/Subversion erforderlich, Disziplin beim Ablauf absolut notwendig \(SVN-Jameica-SVN\).

Dieses Verfahren hat phfeustel implementiert und im Forum (https://jverein-forum.de/viewtopic.php?t=2717)[https://jverein-forum.de/viewtopic.php?t=2717] ausführlich beschrieben.

#### Mit Schreibrecht für alle

Alle SVN-Benutzer dürfen hochladen/committen.

#### Ohne Schreibrecht für alle

Nur einzelne SVN-Benutzer dürfen hochladen/committen.

## Strategien und technische Lösungen für so etwas wie einen Multiuser-Zugriff

### Lese- und Schreibrecht

Benutzer mit unterschiedlichen Rechten unterstützen Jameica und JVerein nicht. Damit ist es auch nicht möglich Teilberechtigungen abzubilden \(bspw. einzelnen Benutzern die Anzeige der Buchungen vorenthalten\).

#### Mit der H2-Datenbank

Mit dem Rezept aus "Datenweitergabe ohne Schreibrecht für alle" und "Cloud-Computing ohne Schreibrecht für alle" lassen sich zwei Benutzergruppen realisieren: die einen haben Schreibrechte und arbeiten auf einer 'Master'-Kopie der Daten, die Benutzer der zweiten Gruppe arbeiten mit einer Benutzer-Kopie der Daten.

Nach jeder Änderung an der Master-Kopie der Daten wird die Benutzerkopie anschließend überschrieben, damit sind Änderungen, die die Benutzer der zweiten Gruppe eventuell gemacht haben stets flüchtig und de facto ist es damit ein reiner Lese-Zugriff.

Änderungen an den Daten müssen den Benutzern der ersten Gruppe "zugerufen" werden damit diese sie in die Master-Kopie der Daten eintragen können.

* Vorteile: immerhin so etwas ein kleine Benutzerverwaltung
* Nachteile: Die Daten der Benutzerkopie können durch Änderungen der zweiten Benutzergruppe verfälscht werden \(bis sie das nächste mal durch die Master-Kopie überschrieben werden\) und die ständige Kopiererei von Master- auf Benutzer-Kopie der Daten ist lästig und kann auch mal vergessen werden.

#### Mit einer MySQL-Datenbank

Wird eine MySQL-Datenbank verwendet, dann kann man einen separaten MySQL-Benutzer anlegen und diesem nur Leserechte geben. Bei den Jameica+JVerein-Installation von Benutzern, die nur Lesen können sollen, muss dann dieser entsprechend beschränkte MySQL-Benutzer verwendet werden. \[Danke dl7bmg für diesen Hinweis\]

Sofern zeitgleich maximal ein \(MySQL-\)Benutzer mit Schreibrechten zugreift, sehe ich keinen Hinderungsgrund warum nicht weitere Benutzer mit Nur-Lese-Rechten gleichzeitig zugreifen können sollten. Denkbar wäre auch -mit ähnlicher Methode wie in \#Der Nacheinander-MultiUser-Zugriff beim ersten Benutzer Jameica mit einer Konfiguration mit Schreibrecht in der MySQL-Datenbank zu starten und \(solange der erste Benutzer online ist\) alle folgenden Benutzer mit einer Nur-Lese-Konfiguration zu starten. Beides ist aber weder offiziell unterstützt noch von mir getestet, vielleicht postet jemand im Forum mal seine Erfahrungen dazu.

### Der Nacheinander-MultiUser-Zugriff

Denkbar ist es zwar die Nutzung von Jameica+JVerein beim gemeinsamen Datezugriff \(siehe \#Gemeinsamer Datenzugriff\) durch Absprachen so festzulegen, dass stets maximal ein Benutzer Jameica+JVerein geöffnet hat \(z.B. Person A nutzt nur tagsüber, Person B darf nur abends ran\), das ist aber sowohl fehleranfällig als auch unflexibel.

Eine technische Lösung ist folgende: Jameica wird mittels eines Batch \(Windows, bzw. Shell-Script unter Linux & Co.\) gestartet. Dieser Batch legt ein "Lockfile" an, startet Jameica und löscht das Lockfile anschließend wieder. Sollte jedoch das Lockfile existieren, so ist Jameica von einem anderen Benutzer bereits gestartet und es soll ein entsprechender Hinweis ausgegeben werden.

* Vorteile: Simple Lösung um eine SingleUser-Nutzung in einer beliebigen MultiUser-Umgebung \(einschließlich CloudComputing\) sicherzustellen.
* Nachteile: Durch \(unbeabsichtigten\) Batch-Abbruch oder einen Systemabsturz kann das Lockfile bestehen bleiben obwohl tatsächlich keiner \(mehr\) Jameica+JVerein nutzt. Nach einer kleinen Rückfrage beim Mitbenutzer kann das Lockfile ggf. händisch gelöscht werden und alles läuft wieder.
* Variante: Anstelle ein eigenes "Lockfile" anzulegen \(wie im Beispiel unten\) kann auch gegen das Jameica-Lockfile jameica.lock getestet werden. Das ist womöglich zuverlässiger als ein eigenes Lockfile, kann aber keine Informationen zum aktiven Rechner+Benutzer zur Verfügung stellen. Näheres dazu, sowie auch Olaf Willuhns Meinung zum Vorgehen an sich, hier: [https://github.com/willuhn/jameica/pull/8](https://github.com/willuhn/jameica/pull/8)

Beispiele für so einen Batch bzw. Shell-Skript:

Für Windows:

```text
@echo off
 rem Nachfolgende drei set-Zeilen bitte anpassen
 rem JAMEICA_DATADIR muss angegeben werden, selbst wenn der Standard-Pfad verwendet wird
 rem JAMEICA_3264 muss -je nach eigener Umgebung- auf 32 oder 64 eingestellt werden
 set JAMEICA_PROGDIR=C:\Program Files (x86)\jameica\
 set JAMEICA_DATADIR=C:\Users\<DeinBenutzername>\Documents\jameica\
 set JAMEICA_3264=32
 rem
 rem Ab hier keine Änderungen mehr nötig
 set JAMEICA_BIN=jameica-win32.exe
 set JAMEICA_JAR=jameica-win32.jar
 if %JAMEICA_3264%==64 (
   set JAMEICA_BIN=jameica-win64.exe
   set JAMEICA_JAR=jameica-win64.jar
 )
 set LOCKFILE_MY="%JAMEICA_DATADIR%\my.lock"
 rem Prüfen ob Lockfile exitiert
 if exist %LOCKFILE_MY% goto jameica_in_use
   goto jameica_start
 :jameica_start
 echo **********
 echo * Jameica wird gestartet
 echo **********
 echo * ACHTUNG:
 echo *    Dieses Fenster NICHT schliessen, es wird
 echo *    automatisch geschlossen sobald Jameica
 echo *    beendet wurde.
 echo **********
 echo %USERNAME%@%COMPUTERNAME% > %LOCKFILE_MY%
 rem Jameica nicht mit der Starter-EXE aufrufen sondern mit javaw das JAR-Archiv aufrufen
 rem da sonst der Batch gleich weiterläuft und nicht wartet bis Jameica beendet wurde.
 cd %JAMEICA_PROGDIR%
 javaw -jar "%JAMEICA_PROGDIR%\%JAMEICA_JAR%" -f "%JAMEICA_DATADIR%"
 del %LOCKFILE_MY%
 goto ende
 :jameica_in_use
 echo %LOCKFILE_MY%
 set /p JAMEICA_USER=<%LOCKFILE_MY%
 echo **********
 echo * Jameica wird gerade benutzt von
 echo *      %JAMEICA_USER%
 echo **********
 echo * Jameica kann erst gestartet
 echo * werden wenn obiger Benutzer das
 echo * Programm beendet hat.
 echo **********
 pause
 goto ende
 :ende
```

Für MacOS \(\(leicht für Linux anpassbar\), von phfeustel

```text
 #!/bin/sh
 # Nachfolgende drei Zeilen bitte anpassen
 # JAMEICA_DATADIR muss angegeben werden, selbst wenn der Standard-Pfad verwendet wird. 
 #    Es reicht dabei den Pfad bis zur jameica.app anzupassen, falls notwendig.
 JAMEICA_APP_PATH="/Applications/jameica.app/"
 # Pfad zu dem Ort, an dem der jameica-Benutzerordner liegt. Ersetze <DeinUserName> durch Deinen Mac-Benutzernamen. 
 #    Eine Liste aller Benutzer kann man sehen, wenn man unter /Users bzw. 
 #    /Benutzer sich die dort liegenden Ordner ansieht.
 JAMEICA_DATADIR="/Users/<DeinUserName>/Desktop/jameica/"
 # Kopiert aus dem Original jameica-Startskript. Entspricht dem Standard aus OSX 10.10
 JAVACMD="/Library/Internet Plug-Ins/JavaAppletPlugin.plugin/Contents/Home/bin/java"

 ######################################### Ab hier keine Änderungen mehr notwendig
 LOCKFILE_MY="${JAMEICA_DATADIR}/my.lock"
 # Prüfen, ob Lockfile existiert
 if [ -f "$LOCKFILE_MY" ];then #Jameica in Verwendung, da Lock-File existiert
    JAMEICA_USER=$(cat $LOCKFILE_MY)
    echo "**********"
    echo "* Jameica wird gerade benutzt von"
    echo "*      $JAMEICA_USER"
    echo "**********"
    echo "* Jameica kann erst gestartet"
    echo "* werden, wenn obiger Benutzer das"
    echo "* Programm beendet hat."
    echo "**********"
 else #Jameica nicht in Verwendung, da das Lock-File nicht existiert
    echo "**********"
    echo "* Jameica wird gestartet"
    echo "**********"
    echo "* ACHTUNG:"
    echo "*    Dieses Fenster NICHT schließen, es wird"
    echo "*    automatisch geschlossen sobald Jameica"
    echo "*    beendet wurde."
    echo "**********"
    echo "${USER}@${HOSTNAME}\r\n" > $LOCKFILE_MY
    # In das .app-Verzeichnis wechseln
    cd $JAMEICA_APP_PATH
    # Jameica nicht über die jameica.app aufrufen sondern mit java das JAR-Archiv aufrufen
    # da sonst der Batch gleich weiterläuft und nicht wartet bis Jameica beendet wurde.
    $("${JAVACMD}" -Xdock:name="Jameica" -Xmx256m -XstartOnFirstThread -jar "${JAMEICA_APP_PATH}/jameica-macos64.jar" -f "${JAMEICA_DATADIR}" -o "$@" > /dev/null) > /dev/null
    rm -f $LOCKFILE_MY
 fi
```

Ein automatisches Kopieren gemäß \#Lese- und Schreibrecht in den obigen Batch zu integriert ist nicht schwierig.

