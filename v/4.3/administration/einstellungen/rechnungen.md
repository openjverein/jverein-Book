# Rechnungen

### Aktivierung

Zur Nutzung der Rechnungen ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.

### Konfiguration

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_EinstellungenRechnungen.png" alt="" /></picture>

Die Rechnung Nummer kann mit der Variable $rechnung_nummer in das Formular der Rechnung eingefügt werden.

Die Rechnung Nummer kann Variablen enthalten. Der Rechnung Zähler kann mit der Variable $rechnung_zaehler in die Rechnung Nummer eingebaut werden (zB. 2026-$rechnung_zaehler). Der Zähler wird automatisch bei jeder erstellten Rechnung hochgezählt. Er kann hier aber auch manuell bearbeitet werden. ZB. am Jahresanfang auf 0 gesetzt werden.

PS: Aus Kompatibilität zu Versionen vor 4.3.0 ist der Defaultwert für die Rechnungsnummer die Variable $rechnung_id. Sie kann aber nun entsprechend den eigenen Gegebenheiten angepasst werden.

Weiter lassen sich Texte für die einzelnen Zahlungswege für den Rechnungsdruck eingeben. In diesen Texten können Variablen eingemischt werden. Siehe [Variablen](../../../../sonstiges/variable.md).

Der Text für Abbuchung, Überweisung, Bar und Gutschrift kann mit der Variable $rechnung_zahlungsweg_text in das Formular der Rechnung eingefügt werden.

Es ist möglich einen QR Code mit den Rechnungsdaten auf die Rechnung zu platzieren. Dazu sind die entsprechenden Felder zu konfigurieren.
