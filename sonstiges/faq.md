# FAQ

## Wie kann ich JVerein auf einen neuen Rechner bringen?

Q: Ich habe mir einen neuen Laptop zugelegt. Nun möchte ich von meinem alten Laptop alles auf den Neuen übertragen. Welche Dateien bzw. Ordner muss ich mitnehmen? Muss ich das Prog. neu installieren?

A: Es muss der Programm- und der Datenordner auf den neuen Rechner übertragen werden.

## Wo liegt der JVerein-Programmordner?

Q: Wo finde ich den Programmordner?

A: Es gibt keinen fest definierten Platz für den Programmordner. Sofern die Jameica-Suite installiert wurde, ist der Ordner unter C:\Programme\Jameica zu finden. Unter Linux wird oft unter /opt/jameica oder \~/jameica installiert.

## Wo liegt der JVerein-Datenordner standardmäßig?

Q: Wo finde ich den Datenordner standardmäßig?

A:

| Betriebssystem  | Verzeichnis                                                           |
| --------------- | --------------------------------------------------------------------- |
| Linux           | /home/\<username>/.jameica                                            |
| Windows 7 + 8   | C:\Users\&lt;username>.jameica                                        |
| Windows 2000/XP | C:\Dokumente und Einstellungen\&lt;username>.jameica                  |
| Windows Vista   | C:\Users\&lt;username>.jameica oder C:\Benutzer\&lt;username>.jameica |
| MacOS           | /Users/\<username>/.jameica oder /Users/\<username>/Library/jameica   |

## Wie kann ich den Datenordner an einen Nichtstandardplatz legen?

Q: Wie kann ich den Datenordner an einen Nichtstandardplatz legen?

A: Beim Aufruf von Jameica wird der Schalter `-f pfad`angegeben.

Beispiel: `jameica.bat -f c:/meinejameicadaten`

siehe auch [http://www.willuhn.de/wiki/doku.php?id=support:faq#abweichendes\_benutzerverzeichnis\_nutzen](http://www.willuhn.de/wiki/doku.php?id=support:faq#abweichendes_benutzerverzeichnis_nutzen)

Unter Windows kann mit einem rechten Mausklick auf das Jameica-Icon > Eigenschaften folgendes Bild geöffnet werden:

![](../.gitbook/assets/jameicasuiteeigenschaften.png)

Im Feld Ziel wird der Schalter -f VERZEICHNIS wie angegeben verändert.

## Wie kann ich mit JVerein mehrere Vereine verwalten?

Q: Wie kann ich mit JVerein mehrere Vereine verwalten?

A: Für jeden Verein wird ein separates Verzeichnis angelegt. Wie die Verzeichnisse beim Aufruf von Jameica zugeordnet werden, ist der vorherigen Antwort zu entnehmen.

## Kann JVerein über ein Netzwerk/Internet betrieben werden?

Q: Kann JVerein übers Netzwerk/Internet betrieben werden?

A: JVerein kann seine Daten in einer MySQL-Datenbank speichern. Siehe auch MySQL-Support. Beim Betrieb über das Internet ist darauf zu achten, dass die Daten verschlüsselt übertragen werden. Weiterhin wird darauf hingewiesen, dass Jameica, Hibiscus und JVerein keine Benutzerverwaltung haben. Jeder, der Zugriff auf das Verfahren hat, kann alles machen. Beim Umgang mit Geld sicher eine nicht befriedigende Angelegenheit. Es ist auch nicht nachvollziehbar, wer welche Änderung vorgenommen hat. Mir stellt sich allerdings immer wieder die Frage nach dem "Warum?". Meines Erachtens können die Daten durch eine Person gepflegt werden. Ich bin selber Kassenwart eines Vereins mit ca. 400 Mitgliedern und weiß somit wovon ich rede. Den übrigen Vorstandsmitgliedern können PDF-Dokumente oder CSV-Dateien zur Serienbriefgenerierung zur Verfügung gestellt werden. Darin kann auch ohne Probleme gesucht werden.

## Warum kann ich eine Bankverbindung nicht speichern/importieren?

Q: Warum kann ich eine Bankverbindung nicht speichern/importieren?

A: Die Banken verwenden Prüfziffernmethoden zur Überprüfung der Kontonummern. Siehe Prüfziffernberechnung bei der Deutschen Bundesbank. JVerein verwendet zur Berechnung der Prüfziffern die Bibliothek HBCI4Java. Bisher ist mir kein Fehler in der Prüfziffernberechnung bekannt. Daher gehe ich davon aus, das die Meldung immer korrekt ausgegeben wird. Die Prüfziffernberechnung kann unter Hibiscus | Einstellungen | Grundeinstellungen | Kontonummern und Bankleitzahlen mittels Prüfziffern testen ausschalten. Damit wird die Prüfziffernberechnung generell ausgeschaltet. Das gilt sowohl für Hibiscus als auch für JVerein.

## Bei mir erscheint der Fehler java.lang.NoSuchMethodError

Q: Bei mir erschein der Fehler java.lang.NoSuchMethodError. Was muss ich tun?

A: Mit 99%iger Sicherheit liegt ein Versionsmix vor. Jameica in ein leeres Verzeichnis entpacken. Hibiscus und JVerein über Datei|Einstellungen|Plugin installieren.
