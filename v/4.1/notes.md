# Release Notes

## Allgemeines

Die Version 4.1 ist eine Minor Version und rückwärts kompatibel mit eine 4.0.


## The Big Ones

### Druck & Mail Vereinheitlichung

* Die Views für Druck & Mail wurden vereinheitlicht
* Die Parameter "Ausgabe" und "PDF als" wurden zusammen gelegt unter Ausgabe. Hier kann zwischen den drei Optionen "Mail", "Eine PDF Datei" und "Einzelne PDF Dateien" gewählt werden"
* Bei PDF Druck lässt sich auswählen ob das Versanddatum beim Druck gesetzt werden soll z.B. nicht bei Probeausdrucken
* Bei Spendenbescheinigungen wird bei Mailversand auch eine Zip Datei erzeugt wie bei den anderen Einträgen. Der Dateipfad für die Ausgabe wird nicht mehr in den Einstellungen konfiguriert sondern es wird sich der letzte benutze Pfad gemerkt und jeweils abgefragt

### Personalbogen in Druck & Mail

* Bisher wurde der Personalbogen bei Selektion des entsprechenden Menüeintrages beim Mitglied direkt gedruckt
* In 4.1 wird jetzt der Druck & Mail Dialog aufgerufen
* Der Druck & Mail Dialog bietet dann auch die oben genannten Ausgabeoptionen
* Zusätzlich lässt sich auswählen welche Informationen in den Report übernommen werden sollen
* Es werden nun auch folgende Daten ausgegeben: Abweichender Zahler, Kontoinhaber, Mandat und Spendenbescheinigungen

### Mail-Text-Vorschau Dialog Update in Druck & Mail

* Im Mail-Text-Vorschau Dialog konnte man bisher in der Empfänger Auswahl alle Mitglieder auswählen. Es wurden in der Vorschau nur allgemeine und Mitglied Variablen ersetzt. Variablen aus den Anhängen wie z.B. Rechnungen wurden nicht ersetzt und mit dummy Daten angezeigt
* In der neuen Version wird für jede zu versendende Mail ein Eintrag in der Empfänger Auswahl erzeugt. Die Variablen Ersetzung basiert dann auf dem Mail Empfänger und dem jeweiligen Anhang. Es sind damit auch nur so viele Einträge in der Empfänger Auswahl  wie auch Mails versendet werden. PS: wenn mehrere Mails an das gleiche Mitglied gesendet werden, ist das Mitglied mehrmals zur Auswahl, jeweils für eine spezifische Mail

### Forderungen

* Mit diesem Feature lassen sich einmalige Forderungen wie z.B. Kursgebühren direkt abrechnen. Es ist damit nicht mehr nötig einen Zusatzbetrag mit einmaliger Ausführung zu erzeugen und dann eine Abrechnungslauf durchzuführen
* Bei der Erstellung werden auch keine Zusatzbeträge generiert, lediglich Sollbuchungen und gegebenenfalls Lastschriften und Buchungen
* Es wird aber ein Eintrag in der Liste der Abrechnungsläufe erzeugt. Bei Fehlern kann dieser gelöscht werden, was dann wie bei regulären Abrechnungsläufen alle generierten Daten löscht
* Siehe [Forderung](mitglieder/forderung.md)

### Gutschriften

* Mit diesem Feature lassen sich bestehende Rechnungen, Sollbuchungen oder Lastschriften zurückerstatten z.B. wenn ein Kurs gestrichen wurde
* Es wird bei Rechnungen und Sollbuchungen eine Storno Rechnung/Sollbuchung mit dem negativen Betrag der ursprünglichen Forderung erzeugt. Ein bereits gezahlter Betrag wird zurück überwiesen, bei teilweiser Bezahlung eben auch nur der bereits bezahlte Teilbetrag
* Alternativ kann auch ein fester Betrag erstattet werden
* Ein fester Betrag kann auch bei der Auswahl von Mitgliedern an diese überwiesen werden
* Siehe [Gutschrift](mitglieder/gutschrift.md)

### Erweiterungen für Abweichende Zahler

* Ähnlich wie beim Familienverband gibt es jetzt auch einen View der die Zahler Beziehungen anzeigt
* Siehe [Abweichende Zahler](mitglieder/abweichendezahler.md)
* In den Mitglied Details unter dem Tab Zahlung wird eine Tabelle angezeigt mit den Mitgliedern für den das selektierte Mitglied bezahlt
* Der Support für abweichende Zahler lässt sich unter Administration->Einstellungen->Anzeige aktivieren bzw. deaktivieren

### Abrechnungslauf View

* Im Abrechnungslauf View werden in neuen Tabs,  die durch den Abrechnungslauf erzeugten Buchungen, Sollbuchungen und Lastschriften, sowie die abgerechneten Zusatzbeträge angezeigt.

### Abrechnung Dialog

* Der View für die Abrechnung wurde in einen Dialog umgewandelt, analog zu den Dialogen für Forderungen und Gutschriften
* Dabei wurde die bisher separate Tabelle für die SEPA Fehler in den Dialog integriert
* Bevor ein Abrechnungslauf gestartet durchgeführt wird wird automatisch auf Fehler getestet



## Kleinere Korrekturen und Erweiterungen

### Variable Auswahl Dialog 

* Falls in einem Dialog oder View bei Eingabefeldern wie z.B. Verwendungszweck, Variablen verwendet werden können, dann existiert jeweils ein Button der eine Vorschau der unterstützten Variablen anzeigt

### Import von Vollzahler und Zahler

* Beim Mitglieder Import gibt es die Option auch Vollzahler und Zahler zu importieren
* Die betroffenen Mitglieder müssen schon in JVerein existieren evtl. müssen diese erst separat importiert werden

### Bezeichnung bei Lehrgängen

* Bei den Lehrgängen konnte man bisher nur eine Lehrgangsart eingeben
* Mit einem neuen Feld lässt sich auch eine Bezeichnung für den Lehrgang eingeben und danach filtern

### Spendenbescheinigungen

* Bei der manuellen Erstellung von Spendenbescheinigungen aus dem Mitgliedskonto von Mitgliedern lassen sich jetzt auch Sammelbescheinigungen erstellen. Dafür können mehrere Istbuchungen selektiert werden
* Bei der automatischen Generierung über das Mitgliedmenü wird jetzt über einen Dialog das Jahr abgefragt für welches die Buchungen berücksichtigt werden sollen. Auch wird hier die Prüfung auf den Mindestbetrag nicht mehr durchgeführt

## Sonstiges

* Buchungskorrektur wurde aus dem Navigationsbaum entfernt und als Button in die Buchungsliste aufgenommen
* Beim Abrechnungslauf gibt es die neue Option, die Rechnung als Buchungsdokument in der erzeugten Buchung zu speichern
* Das Kontoinhaber Attribut wurde zu Kursteilnehmer hinzugefügt
* In allen Liste Views mit Beträgen wird bei der Selektion mehrerer Einträge, in der Zeile unterhalb der Tabelle, die Summe der Beträge angezeigt
* Im Mail View wurden einige Buttons verschoben
* Bei Sollbuchungen mit negativem Betrag (Erstattung) lässt sich beim manuellen Erstellen einer Rechnung ein Erstattungsformular auswählen
* Das Mitglied wird in der Lastschrift angezeigt
* Der QR-Code wird nur bei Überweisung in der Rechnung angezeigt
* Beim Anlegen eines neuen Kontos wird automatisch ein Anfangsbestand zum Eröffnungsdatum des Kontos mit Betrag 0€ erstellt
* Bei neuen Mitgliedern und Buchungen können direkt auch Buchungsdokumente hinzugefügt werden


