# Release Notes

## Allgemeines

Die Version 4.3 ist eine Minor Version und rückwärts kompatibel mit einer 4.2, 4.1 und 4.0.

## The Big Ones

### Allgemeiner Export bei Tabellen erweitert

Beim PDF Export der Tabellen über die Buttons im oberen Panel wurde ein weiterer Tab zur Konfiguration der Schriftarten hinzugefügt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogSchriftart.png" alt="" /></picture>

Für die Tabellen Header Zeile und den Tabelleninhalt lässt sich jeweils die Schriftart, Schriftgröße und Hintergrundfarbe (für spezielle Zellen) einstellen. Weiter kann festgelegt werden ob negative Zahlen in roter Farbe ausgegeben werden. [Allgemeines](allgemeines.md)

### Export Profile

Für den CSV und PDF Tabellen Export über die Buttons im oberen Panel Buttons wurden Profile implementiert. Dialog Einstellungen lassen sich in Profilen speichern und später wieder anwenden. [Allgemeines](allgemeines.md)

### Konfigurierbarkeit von PDF Reports

Für Saldenreports, PDF Reports die über die Export Buttons generiert werden, sowie für Kontoauszug und Personalbogen lässt sich der Report in ähnlicher Weise konfigurieren wie die Tabellenausgabe über die Panel Buttons. Es ist der gleiche Dialog verfügbar allerdings ohne die Spaltenauswahl. [Allgemeines](allgemeines.md)

### Konfigurierbare Rechnungsnummer

Das Format der Rechnungsnummer lässt sich nun unter Administration->Einstellungen->Rechnungen festlegen. Für die Nummer werden Variablen unterstützt. [Rechnungen](administration/einstellungen/rechnungen.md)

### Buchungsreport

Über das Kontextmenü der Buchungen lassen sich Buchungsreports generieren z.B. Ersatzbeleg. Der Report basiert auf Nutzer definierten Formularen. Hierfür wurde eine neue Formularart "Buchungsreport" eingeführt. In den Formularen sind neben den allgemeinen Variablen auch die Buchung Variablen verfügbar.

### Tastaturkürzel (Shortcuts)

Einige Buttons sind jetzt mit Tastaturkürzel hinterlegt. Dies sind:
* Löschen: Entf
* Speichern: Ctrl + S
* Speichern und Neu: Ctrl + Alt + S
* Vor: Ctrl + Pfeil-Rechts
* Zurück: Ctrl + Pfeil-Links
* Hilfe: F1
* Neu: Ctrl + N
* PDF: Ctrl + P
* View ohne Speichern verlassen Dialog: Ohne Speichern Verlassen: Ctrl + SHIFT + W
* Neues Mitglied: Alt + M
* Neue Buchung: Alt + B
* Neuer Abrechnungslauf: Alt + A

[Allgemeines](allgemeines.md)

### Filter Profile

Bisher wurden Filter Profile nur für die Mitglieder Liste unterstützt. Nun werden sie für alle Listen mit Filtern unterstützt.

Die Funktionalität wurde wie folgt geändert:
* Beim Aufruf für Filter Profile erscheint nun ein Dialog
* Im Dialog können Profile erstellt, überschrieben, gelöscht und angewendet werden
* Der Dialog zeigt auch die Werte der gesetzten Filter Felder an

### HTML Unterstützung in Formularfeldern

Text in Formularfeldern lässt sich mit HTML Tags formatieren. Hier sind auch mehrseitige Ausgaben möglich. [Formulare](administration/mitglieder/formulare.md)

## Kleinere Korrekturen, Erweiterungen oder Modifikationen

### Auswertungen Menüeinträge gelöscht

Die Einträge im Navigationsmenü für Auswertungen wurden entfernt. Die Reports sind jetzt über den Export Button in der Liste der Mitglieder bzw. Nicht-Mitglieder verfügbar. Damit ist für sie auch die Möglichkeit der individuellen Konfigurierbarkeit vorhanden, wie oben beschrieben.

PS: Die Möglichkeit über externe CSV Files die zu exportierenden Spalten zu definieren wurde ebenfalls entfernt. Über die bestehende allgemeine Export Möglichkeit der Tabellen lässt sich ebenfalls festlegen welche Spalten exportiert werden sollen. Darum ist diese Möglichkeit hier nicht mehr nötig.

### Mail Dialog überarbeitet

* "Speichern und Senden" wurde in "Senden" umbenannt, macht aber das gleiche wie bisher und sendet an Empfänger an die die Mail noch nicht versendet wurde
* "Speichern und erneut senden" wurde entfernt. Diese Funktion macht keinen Sinn mehr, weil bereits versendete Mails nicht mehr editiert werden können. Als Alternative gibt es jetzt den Button "Duplizieren". Dieser erstellt eine Kopie der Mail welche sich wieder editieren lässt

Eine bereits versendete Mail lässt sich nicht mehr ändern. Es lassen sich aber neue Empfänger hinzufügen und die gleiche Mail nochmals an die neu hinzugefügten Empfänger versenden, selbst an Empfänger an die sie schon einmal versendet wurde, falls der Empfänger neu hinzugefügt wurde. Beim Empfänger ist nach dem Versenden jeweils gespeichert wann sie an ihn versendet wurde.

### Abrechnungslauf Abschließen überarbeitet

* Ein abgeschlossener Abrechnungslauf kann wieder aufgeschlossen werden
* Die Menüeinträge haben Icons
* Die Tabelle der Abrechnungsläufe hat eine Spalte für Abgeschlossen
* In Abrechnungslauf Tabellenspalten bei Buchung, Sollbuchung und Lastschrift wird im Text ein Icon eingeblendet wenn der Abrechnungslauf abgeschlossen ist und es in den Einstellungen aktiviert ist
* Abschließen und Aufschließen sind ausgegraut wenn das Fälligkeitsdatum in einem Jahresabschluss liegt
* Prenotification wird nicht mehr blockiert
* Löschen wird bei abgeschlossenen Abrechnungsläufen nicht ausgegraut, es gibt aber eine Fehlermeldung. Wenn man in den Einstellungen den Haken wieder weg macht, würde man sich sonst wundern, warum Löschen ausgegraut ist
* Buchungen, Sollbuchungen und Lastschriften von abgeschlossenen Abrechnungsläufen können nicht mehr gelöscht oder editiert werden
* Ein abgeschlossener Abrechnungslauf kann in DBBereinigen gelöscht werden

### Natürliche Sortierung von Spalten mit Text

Die Variablen für Kontonummer, Nummer der Buchungsart und externe Mitgliedsnummer sind als String implementiert. Es lassen sich neben Ziffern auch Buchstaben verwenden. Wurden Tabellen mit diesen Spalten sortiert, dann wurde lexikografisch sortiert, also so wie auch der Duden sortiert. Bei reinen Zahlen führt dies zu einer unnatürlichen Sortierung.

In der neuen Implementierung werden Zahlenanteile in den Variablen nach Wert der Zahl sortiert. Damit werden reine Zahlenwerte wie erwartet sortiert.

### HTML Mailvorschau

Wird im Text Feld einer Mail der Text als HTML eingegeben, dann wird in der Vorschau dieser als HTML ausgegeben. Die HTML Anzeige in der Vorschau erfolgt falls im Text "<html" vorkommt.

### Tooltip in Tabellen

Wird in einer Tabelle ein Text nicht vollständig angezeigt weil er länger ist als die Spaltenbreite, dann wird der ganze Text als Tooltip angezeigt, wenn man mit der Maus darüber geht.

### Spaltenauswahl über Menü

Klickt man mit der rechten Maustaste auf die Kopfzeile in einer Tabelle, dann wird die Spaltenauswahl Liste angezeigt. Es kann dann direkt eine Spalte aktiviert oder deaktiviert werden.

### Zugeordnete Buchungen im Abrechnungslauf

Im Abrechnungslauf wird ein neuer Tab "Zugeordnete Buchungen" angezeigt. Im Tab "Buchungen" sind nur Buchungen aufgelistet, die durch den Abrechnungslauf erzeugt wurden, also im Falle von Lastschrift.

Im neuen Tab "Zugeordnete Buchungen" werden alle Buchungen angezeigt die den Sollbuchungen des Abrechnungslaufes zugeordnet sind. Man sieht hier also auch die Buchungen die per Überweisung oder Barzahlung erzeugt wurden und später den Sollbuchungen zugeordnet wurden.

### GoBD Konformität

GoBD = Grundsätze zur ordnungsmäßigen Führung und Aufbewahrung von Büchern, Aufzeichnungen und Unterlagen in elektronischer Form sowie zum Datenzugriff

OpenJVerein ist nicht ohne weitere Maßnahmen GoBD konform. So wird z.B. in OpenJVerein keine Historie geführt, diese muss über externe Mechanismen sichergestellt werden. Es wurden mit dieser Version aber Änderungen durchgeführt um allgemein besser GoBD konform zu sein.

Die einzelnen Änderungen sind:
* Falls Konten Buchungen abgeschlossener Geschäftsjahre zugeordnet sind, können nicht mehr alle Felder der Konten geändert werden
* Falls Buchungsarten von Buchungen abgeschlossener Geschäftsjahre verwendet werden, können nicht mehr alle Felder der Buchungsart geändert werden
* Versanddatum von Rechnung, Spendenbescheinigung und Lastschrift lässt sich nicht mehr editieren und löschen
* Bereits versendete versendete Rechnungen und Spendenbescheinigungen können nicht mehr gelöscht werden


## Sonstiges

* Einige Fehlerkorrekturen
* Carlito Schriftart (Calibri kompatibel) hinzugefügt
* Kommentar bei Buchungen lässt sich in der Liste der Buchungen als optionale Spalte anzeigen (per Default wird sie nicht angezeigt)
* Der Verwendungszweck für den QR Code in Rechnungen lässt sich jetzt mit Variablen anpassen
* Fix für Zeilenumbruch in der Mailsignatur
* Der Variablen Dialog zeigt unter Windows nur noch die erste Zeile des Textes an. Der Grund ist, dass mehrzeilige Texte unter Windows nicht umgebrochen werden
* Bei Mailversand wird nun des Zip File nur temporär erzeugt und wieder gelöscht. Es erfolgt dann keine Abfrage für den Ordner mehr
* Die Infobox bei Splitbuchungen wird nur noch angezeigt wenn mehr als eine Buchung selektiert wurde
* Der Spaltenauswahl Dialog und die beiden CSV und PDF Export Dialoge bieten eine Reset Funktion
* Beim Mitglied Import lässt sich auch die Mandatid importieren
* Das Kommentarfeld von Buchungen lässt sich optional in der Buchungsliste einblenden
* Die QR-Code Größe lässt sich jetzt individuell einstellen
* Falls Externe Mitgliedsnummer aktiviert ist, lässt sich beim Mitglieder Import die Zuordnung in einem Familienverband über die externe Mitgliedsnummer Referenz erstellen. Dadurch ist kein zweiter Import mehr nötig

