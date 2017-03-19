# Pre-Notification

Mit der Pre-Notification Funktion ist es einfach möglich, den Ansprüchen der SEPA Regelung bzgl. der Ankündigung einer SEPA-Lastschrift gerecht zu werden. Die Pre-Notification Benachrichtigung kann erst erstellt werden, wenn der Buchungsvorgang abgeschlossen ist. Die Buchungen \(d.h. die Abrechnung\) müssen dafür nur erstellt sein. Eine Onlinebuchung/ -übertragung zur Bank ist für diese Funktion nicht erforderlich.

In JVerein stehen folgende Alternativen für die Pre-Notifications zur Verfügung:

* Schriftlich an alle Mitglieder
* Per E-Mail an alle Mitglieder mit E-Mail-Adresse und schriftlich an die Übrigen
* Als 1ct-Überweisung an alle Mitglieder

## Aufruf der Pre-Notification-Funktion\[Bearbeiten\]

Die Pre-Notification Funktion ist etwas versteckt und kann nur über folgenden Weg aufgerufen werden:

![](/assets/SEPA_Pre-Notification_Abrechnungsverlauf_Menu.png)

Klick auf Abrechnungslauf.

Mit einem rechts-Klick auf den entsprechenden Abrechnungsverlauf öffnet sich ein Kontextmenü, mit dem man die Pre-Notification Mail erstellen kann.

![](/assets/SEPA_Pre-Notification_Abrechnungsverlauf_Knopf_zur_E-Mail.png)

## Pre-Notification schriftlich und per E-Mail

Bevor Pre-Notification erstellt werden können muss zunächst muss ein [Formulare](/formulare.md "Formular") dafür angelegt werden.![](/assets/SEPA_Pre-Notification_E-Mail_Erstellung.png)In diesem Fenster kann die Pre-Notification erstellt werden, und zwar auf der Karte Mail + PDF .

## Schriftliche Pre-Notification an alle Mitglieder

Im Block Parameter bei Ausgabe muss PDF \(alle\) eingestellt werden und das Formular passend ausgewählt werden, dann den Startknopf drücken.

Über die Einstellung zu "PDF als" kann gesteuert werden, ob die PDF als eine einzige, mehrseitige Datei erzeugt wird, die alle einzelnen Schreiben enthält \(Einstellung "eine PDF-Datei"\), oder ob jedes Schreiben an einen Benutzer in einer separaten Datei abgelegt wird. In jedem Fall muss der Benutzer über den aufkommenden Dialog Ausgabedatei wählen das Ablageverzeichnis und den Namen \(bzw. das Prefix\) der PDF-Datei\(en\) festlegen.

Sollen separate Dateien erzeugt werden, so wird der ausgewählte Dateiname vor der Endung .PDF um eine fortlaufende Nummer \("einzelne PDF-Dateien, nummeriert"\), um die Mitgliedsnummer des angeschriebenen Mitglieds \("einzelne PDF-Dateien, mit Mitgliedsnummer"\) oder um beide Werte \("einzelne PDF-Dateien, nummeriert mit Mitgliedsnummer"\) ergänzt, je nach dem, was in der Einstellung "PDF als" ausgewählt wurde.

Die direkte Erzeugung einzelner PDF-Dateien ist hilfreich, wenn für das Versenden der Briefe ein Online-Dienstleister herangezogen werden soll.

## E-Mail-Pre-Notification an Mitglieder mit E-Mail-Adresse

Im Block Parameter bei Ausgabe muss EMail eingestellt werden.

Im Block Mail wird der Mail-Text eingegeben und schließlich der Startknopf gedrückt.

Hinweis: Für die Pre-Notification-Mail gibt es keine E-Mail Vorlage\(n\). Der Inhalt des E-Mailformulars wird jedoch gespeichert und steht für zukünftige Versendungen zur Verfügung sobald der Startknopf gedrückt wurde. Dies löst bei korrekt eingestellten E-Mail-Server-Daten den Versand der E-Mails aus. Es ist daher ratsam, diese Funktion im Vorfeld zu testen, ohne mit echten Mitgliederdaten/e-mails zu hantieren.

Die versendeten Pre-Notification-E-Mails werden nach dem Versand beim jeweiligen Mitglied in der Mail-Historie gespeichert.

### Beispiel für eine Pre-Notification Mail

```
NAME_DES_VEREINS___  - SEPA  Ankündigung

$lastschrift_empfaenger

ORT____, den  $lastschrift_abrechnungslauf_datum

aufgrund des von Dir erteilten Mandats zieht DER_VEREIN___ mittels SEPA-Lastschrift
von Deinem unten angegebenen Konto folgende Forderung am $lastschrift_abrechnungslauf_faelligkeit ein.

unsere Gläubiger-ID: DE___
Deine Mandats-ID: $lastschrift_mandatid
Das Mandats-Datum: $lastschrift_mandatdatum
Deine BIC: $lastschrift_bic
Deine IBAN: $lastschrift_iban
Das Fälligkeitsdatum: $lastschrift_abrechnungslauf_faelligkeit
Der Verwendungszweck: $lastschrift_verwendungszweck
Der Betrag: $lastschrift_betrag Euro

Fragen und Korrekturen bitte an: EMAILADRESSE___ 

Mit freundlichen Grüßen
die Verwaltung
```



