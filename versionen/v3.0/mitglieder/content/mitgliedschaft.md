# Mitgliedschaft

Beitragsgruppe ist ein Pflichtfeld. Die Beitragsgruppen können unter [Beitragsgruppen](../../administration/mitglieder/beitragsgruppen.md) für jeden Verein individuell konfiguriert werden. Siehe auch [Beitragsmodelle](../../../../allgemein/beitragsmodelle.md). Beim Austrittsdatum wird das Datum des satzungsgemäßen Austritts (z. B. der 31.12. des jeweiligen Jahres) eingetragen. Unter Kündigung wird das Datum des Eingangs der Kündigung vermerkt.

Standardaussehen des Formulars:

![](../../../../v3.0.x/mitglieder/content/img/MitgliedschaftTab.png)

In Administration->Einstellungen->Anzeige lässt sich einstellen, ob Eintrittsdatum ein Pflichfeld ist.

## Sekundäre Beitragsgruppen

Für ein Mitglied können auch Beiträge aus mehreren Beitragsgruppen abgerechnet werden. Dazu muss unter Administration->Einstellungen->Anzeige das Häkchen bei "sekundäre Beitragsgruppen anzeigen" gesetzt werden und unter Administration->Beitragsgruppen muss für mindestens eine Beitragsgruppe das Häkchen "sekundäre Beitragsgruppe" gesetzt werden. Dann kann beim Mitglied eine entsprechende Auswahl vorgenommen werden.

![](../../../../v3.0.x/mitglieder/content/img/SekundaereBeitragsGruppen.png)

## Familienverband

Sofern eine Beitragsgruppe ausgewählt wurde, die mit "Familienangehöriger" gekennzeichnet ist, wird folgendes Formular angezeigt.

Die Person (ebenfalls ein Mitglied), die im Familienverband den vollen Beitrag zahlt, kann im Tab "Vollzahlendes Familienmitglied" aus einer Liste ausgewählt werden.

![](../../../../v3.0.x/mitglieder/content/img/VollZahler.png)

Im Tab "Familienverband" werden die Personen angezeigt, die am Familienverband beteiligt sind.

![](../../../../v3.0.x/mitglieder/content/img/FamilienVerband.png)

Sinn und Zweck dieser Familienverknüpfung ist es, die Voraussetzungen für die Familienmitgliedschaft prüfen zu können. Tritt ein Mitglied aus, dass für andere Mitglieder als Vollzahlendes Familienmitglied eingetragen ist, kommt eine entsprechende Fehlermeldung.

Dann sind die Beitragsgruppen der Familienmitglieder zu verändern oder es ist ein anderes Vollzahlendes Familienmitglied einzutragen.

Siehe auch: [Familientarife](../../../../allgemein/familientarife.md)

## Zukünftige Beitragsgruppen

![](../../../../v3.0.x/mitglieder/content/img/ZukuenftigeBeitragsGruppen.png)

Hier kann man Beitragsgruppen eintragen, die für dieses Mitglied ab einem definierten Datum gültig sein soll. Hat man z.B. im ersten Jahr einen vergünstigten Probebeitrag, trägt man diesen oben unter Beitragsgruppe ein. Die Beitragsgruppe für den normalen Beitrag, der gültig werden soll, sobald die Probezeit beendet ist, kann man sofort in dieser Tabelle zukünftige Beitragsgruppen eintragen.

Bei Programmstart wird geprüft, ob das Datum für eine Änderung der Beitragsgruppe erreicht wurde. Alle zu ändernden Mitglieder werden in einer Liste angezeigt und es können die neuen Beitragsgruppen für ausgewählte Mitglieder oder alle angezeigten übernommen werden. Damit die Daten angezeigt werden, ist einmal die Box "künftige Beitragsgruppen" zu aktivieren:

![](../../../../v3.0.x/mitglieder/content/img/Boxactivate.png)

Hinweis: Die Box ist nur sichtbar, wenn im Menü "Start" ausgewählt wurde.

Zum Erfassen einer zukünftigen Beitragsgruppe klicken Sie mit der rechten Maustaste in die Tabelle. Im Kontextmenü wählen Sie den Punkt Beitragsgruppe hinzufügen. Es öffnet sich eine Ansicht, in der Sie die neue Beitragsgruppe auswählen und das Datum erfassen, ab dem diese Gruppe gültig werden soll. Sie können in einem Bemerkungsfeld noch hinterlegen, warum diese Änderung durchgeführt werden sollte.

Bei Mitgliedern von Beitragsgruppen der Beitragsart Normal können Sie nur andere Beitragsgruppen mit der Beitragsart Normal als zukünftige Beitragsgruppe eintragen.

Bei Mitgliedern von Beitragsgruppen der Beitragsart Familienangehöriger können Sie keine zukünftigen Beitragsgruppen hinterlegen, weil hier u.U. Zahlungsdaten fehlen.
