# Mittelverwendung

### Aktivierung

Zur Nutzung der Mittelverwendung ist die Option in den Einstellungen->Administration->Einstellungen->Anzeige zu aktivieren.

Anschließend sollte JVerein neu gestartet werden, damit der Menüpunkt "Mittelverwendung" zur Verfügung steht.

### Allgemeines

Gemeinnützige Vereine müssen ihre Einnahmen (Geld!) im aktuellen und den zwei folgenden Jahren ausgegeben haben (zeitnahe Verwendung). Dieses müssen sie dem Finanzamt nachweisen. Sie dürfen aber Rücklagen bilden. Diese sind der zeitnahen Verwendung entzogen.

Es gibt keine feste Vorgabe wie ein Mittelverwendung Nachweis auszuschauen hat. JVerein zeigt einen Report der den Mittel Zufluss und Abfluss zeigt (Einnahmen/Ausgaben Rechnung).

Es werden auch pro Sphäre die Einnahmen und Ausgaben aufgelistet. Daraus kann man z.B. ableiten wie viel freie Rücklagen man bilden darf (höchstens ein Drittel des Überschusses aus der Vermögensverwaltung und zusätzlich maximal 10% der Einnahmen im Ideellen Bereich und maximal 10% der Überschüsse in den Zweckbetrieben und den wirtschaftlichen Geschäftsbetrieben).

Aus dem Report kann man z.B. auch sehen ob die vorhandenen Mittel kleiner sind als die Summe der Ausgaben. Falls ja wurde alles in diesem Jahr ausgegeben und die zeitnahe Mittelverwendung wäre erfüllt. Wird nicht alles ausgegeben muss es im folge Jahr passieren.

Bei dem Report habe ich folgende Annahmen getroffen. Es wäre hier oder im Forum zu besprechen ob diese richtig sind und ob etwas geändert werden sollte. Da dies nur eine Aufbereitung vorhandener Daten ist greift das Feature nicht in die sonstige Logik der SW ein.



### Anzeige

Der Mittelverwendung Report lässt sich über den entsprechenden Menüeintrag in der Navigation öffnen.

Der Report listet folgende Informationen auf:
* Summe der Bestände der Geldkonten zum Ende des letzten Geschäftsjahres (berechnet aus den Anfangsbeständen der Geldkonten des aktuellen Geschäftsjahres)
* Summe der Bestände der Rücklagen zu Ende des letzten Geschäftsjahres (berechnet aus den Anfangsbeständen der Rücklagenkonten  des aktuellen Geschäftsjahres)
* Verwendungsüberhang/Rückstand: Dies ist der Bestand der Geldkonten abzüglich des Bestandes der Rücklagen. Diese Summe muss im aktuellen und folge Jahr ausgegeben werden
* Je Sphäre wird die Summe der Einnahmen und Ausgaben und das Ergebnis aufgelistet
* Zusätzlich werden die Einnahmen und Ausgaben über alle Sphären aufgelistet
* Pro Rücklagenkonto Art werden die zugeführten und entnommen Rücklagen aufgelistet
* Aus den berechneten Summen wird der Kontostand der Geld- und Rücklagenkonten berechnet und angezeigt
* Diese Summen sind der Übertrag in das nächste Geschäftsjahr

PS: Die Endsummen werden aus den getätigten Buchungen berechnet. Sie sollten mit den Anfangsbeständen der Konten des nächsten Geschäftsjahres überein stimmen. Ist das nicht der Fall, dann sind einige Buchungen nicht richtig verbucht worden z.B. wegen fehlender Buchungsart.

Ist in den Einstellungen->Administration->Einstellungen->Buchführung die Checkbox "Listen: Buchungsarten ohne Buchung unterdrücken" ausgewählt werden Sphären und Anlagenkonten Arten ohne Buchung im Report nicht angezeigt.

Die Zeilen in der Mittelverwendung sind nummeriert damit man bei einem evtl. Begleitschreiben an das Finanzamt auf die Zeilen Bezug nehmen kann.

![](img/MittelverwendungListeView.png)

Der Report kann über die Buttons CSV und PDF ausgegeben werden.

### Annahmen

Für eine korrekte Berechnung der Daten des Reports sind folgende Annahmen getroffen:
* Alle Konten auf denen vorhandene Mittel (Geld) verwaltet ist, ist die Kontoart Geldkonto zugewiesen
* Konten für Schulden wie z.B. Darlehen, Kredite etc. sind als Verbindlichkeitskonto gekennzeichnet
* Rücklagen sind auf Rücklagenkonten verbucht
* Buchungen muss die korrekte Buchungsart mit korrekter Klassifikation als Einnahme, Ausgabe oder Umbuchung zugewiesen sein

Einnahmen und Ausgaben werden wie folgt berechnet:
* Zu den Einnahmen zählen alle Buchungen der Art Einnahme die auf Geldkonten eingehen
* Zu den Ausgaben zählen alle Buchungen der Art Ausgabe die von Geldkonten abgehen
* Umbuchungen zwischen Geldkonten werden nicht berücksichtigt weil sie weder Einnahmen noch Ausgaben sind
* Umbuchungen zu Verbindlichkeitskonten und Anlagenkonten werden berücksichtigt. Dazu werden positive Umbuchungen auf diesen Konten als Ausgabe bei Geldkonten betrachtet und negative Umbuchungen als Einnahmen. Es wird davon ausgegangen, dass alle Umbuchungen auf diesen Konten von Geldkonten kommen
* Es darf also keine Umbuchungen innerhalb Verbindlichkeitskonten und Anlagenkonten geben

Hinweise:

Bei einem Abrechnungslauf werden bei Lastschriften einzelne Buchungen generiert und eine Gegenbuchung. Später wird der Betrag der Gegenbuchung per Lastschrift eingezogen.

Es ist darauf zu achten, dass die Gegenbuchung die Buchungsart Einnahme hat. Hätte sie die Art Ausgabe, wären die Angaben zu den Ausgaben im Report falsch. Dann wären auch die Einnahmen doppelt, wegen der Buchungen und eingegangenen Lastschrift. Die Summe würde zwar stimmen aber nicht die Angaben zu den Einnahmen und Ausgaben.

