# Spendenbescheinigung drucken/mailen

## Spendenbescheinigungen selektiv drucken

Im View Spendenbescheinigungen werden bereits erstellte Spendenbescheinigungen angezeigt.

![](../../assets/spendenbescheinigungen.png)

In der Liste können ein oder mehrere Einträge markiert werden. Über ein Kontextmenu \(rechter Mausklick\) stehen verschiedene Aktionen zur Verfügung.

![](../../assets/spendenbescheinigung_menu3.png)

Durch einen Klick auf PDF wird die Spendenbescheinigung im PDF-Format ausgegeben. Dabei gibt es mehrere Möglichkeiten:
* PDF (Standard): Dies benötigt kein Formular und benutzt einen festen Aufbau.
* PDF (Standard, Mit Adressblatt): Dies benötigt kein Formular und benutzt einen festen Aufbau. Drucken ist gedacht wenn die Spendenbescheinigung per Brief versand werden soll. Es wird eine Anschrift auf einer zusätzlichen Seite ausgedruckt welche in ein Brieffenster passt.
* PDF (Individuell): Es wird eine Spendenbescheinigung unter Verwendung des für die Spendenbescheinigung konfigurierten Formulars erzeugt.
* PDF (Individuell, Mit Adressblatt)): Es wird eine Spendenbescheinigung unter Verwendung des für die Spendenbescheinigung konfigurierten Formulars erzeugt. Es wird eine Anschrift auf einer zusätzlichen Seite ausgedruckt welche in ein Brieffenster passt.

In der Einzeldarstellung einer Spendenbescheinigung wird der Ausdruck über Buttons ebenfalls angeboten. Im Unterschied zum Druck aus der Liste heraus wird zunächst der Datei-Dialog mit der Voreinstellung des Spendenbescheinigungsverzeichnisses aus den Einstellungen und dem erzeugten Namen angeboten. Hier kann das Verzeichnis und der Name noch einmal korrigiert werden.

Der Ausdruck über die Buttons funktioniert nur, wenn die Spendenbescheinigung bereits einmal gespeichert wurde. Die Aktionen neu und drucken direkt hintereinander werden mit einer Fehlermeldung abgewiesen.

## Spendenbescheinigung selektiv per Mail versenden

Möchten Sie eine Spendenbescheinigung selektiv versenden, so öffnen Sie den Dialog für Spendenbescheinigungen. Wählen Sie den Filter so, dass die gewünschten Spendenbescheinigungen angezeigt werden. Selektieren Sie einen oder mehrere Einträge und drücken die rechte Maustaste. Es öffnet sich ein Kontext-Menü. Wählen Sie hier den Menüpunkt "Spendenbescheinigungen versenden". Es öffnet sich hier der Dialog Spendenbescheinigungen der Sie beim Versenden der Spendenbescheinigungen unterstützt.

![](../../assets/spendenbescheinigung_mail.png)

Im Info Feld erfolgt eine Information über die Anzahl der ausgewählten Spendenbescheinigungen ausgegeben.

Danach wird angezeigt für welche Mitglieder keine Mail Adresse konfiguriert ist und ihre Spendenbescheinigungen damit nicht verschickt werden.

Es wird ebenfalls angezeigt für welche Spendenbescheinigung kein Mitglied zugeordnet ist. In diesem Fall wird der Inhalt von Zeile 1..3 ausgegeben und keine Mail verschickt.

In den Parametern lässt sich einstellen ob das Standard oder ein individuelles Format verwendet werden soll. Ebenso lässt sich einstellen ob eine extra Seite mit einer Anschrift ausgedruckt werden soll, welche in ein Brieffenster passt.

Im Bereich Mail lässt sich der Betreff und der Mailtext eingeben.

Durch Klick auf den Starten Button werden die Spendenbescheinigungen an die Mitglieder versendet.

## Spendenbescheinigung automatisch drucken oder per Mail versenden

Neben der individuellen Auswahl für Drucken und Versenden über das Kontextmenü im Spendenbescheinigungen Dialog lässt sich dies auch über den Eintrag im Navigations Menü erreichen.

Der Dialog enthält hier die Filter Optionen wie im Spendenbescheinigungen Dialog und zusätzlich die Auswahl der Ausgabe DRUCK/MAIL.

Es werden hier alle Spendenbescheinigungen gedruckt bzw. versendet die die Filterkriterien erfüllen. Eine individuelle Auswahl aus den gefilterten Einträgen ist hier nicht möglich.

![](../../assets/spendenbescheinigung_mail2.png)
