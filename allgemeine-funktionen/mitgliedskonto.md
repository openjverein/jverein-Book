# Mitgliedskonto

## Abrechnung

Die Abrechnung schreibt Informationen zu Mitgliedsbeiträgen und Zusatzabrechnungen in die Tabelle Mitgliedskonto \(Sollbuchung\). Zusätzlich werden für den Zahlungsweg Abbuchung Informationen \(Istbuchung\) in die Buchungstabelle der Buchführung geschrieben.

Fehlerhafte oder Test-Abrechnungen können rückgängig gemacht werden. In dem Abrechnungsformular kann durch klick auf _Rückgängig._

![](../assets/mitgliedskontorueckgaengig.png)

eine Übersicht der Abrechnungsläufe geöffnet werden:

![](../assets/mitgliedskontoabrechnungslaeufe.png)

Durch einen Rechtsklick auf einen Abrechnungslauf öffnet sich ein Kontextmenü mit der Option löschen:

![](../assets/mitgliedskontoabrechnungslaeufeloeschen.png)

Nach einer Bestätigung werden die verknüpften Datensätze aus der Mitgliedskontotabelle und der Buchungstabelle gelöscht.

## Sollbuchungenübersicht <a id="mitgliedskontouebersicht"></a>

Es gibt eine zentrale Übersicht über alle Sollbuchungen der Mitgliedskonten-Tabelle. Die Buchungen können über einen Zeitraum oder über einen Namen, bzw. Namensfragment gefiltert werden. Zusätzlich kann angegeben werden, ob nur Sollbuchungen mit Differenzen zwischen Soll und Ist \(Offene Posten oder Überzahlungen\) angezeigt werden.

![](../assets/sollbuchungenliste.png)

Durch einen Doppelklick auf die Sollbuchung erscheint das Mitglied.

## Mitgliedskonto beim Mitglied

![](../assets/mitgliedskontomitglied.png)

In der Baumansicht werden die Summen pro Mitglied, die einzelnen Sollbuchungen \(Rechnersymbol\), sowie die einzelnen zugeordneten Istbuchungen \(Euro-Symbol\) angezeigt.

Mit einem rechten Mausklick auf das Mitglied öffnet sich ein Kontextmenü. Damit können neue Sollbuchungen aufgenommen werden.

![](../assets/sollbuchungneu.png)

Mit einem rechten Mausklick auf eine Sollbuchung öffnet sich ein Kontextmenü. Damit kann die Sollbuchung bearbeitet, oder, sofern keine Istbuchung zugeordnet ist, auch gelöscht werden.

Mit einem rechten Mausklick auf eine Istbuchung öffnet sich ein Kontextmenü. Damit kann die Istbuchung von der Sollbuchung gelöst werden.

## Buchungen dem Mitgliedskonto zuordnen <a id="mitgliedskontozuordnen"></a>

> Unter Buchführung&gt;[Buchungen](buchf/buchungen.md) ist eine Buchung auszuwählen und doppelt anzuklicken:

![](../assets/mitgliedskontobuchungen.png)

Durch einen Klick auf ... neben Sollbuchung erscheint folgender Dialog:

![](../assets/sollbuchung-zuordnung-ist.png)

Der Name aus der Buchung wird in das Namensfeld übernommen. Der Inhalt wird in Wörter zerlegt und in den Spalten Name und Vorname gesucht.

Zur Filterung des Buchungen steht weiterhin Egal \(= eine beliebige Differenz\), Fehlbetrag oder Überzahlung zur Verfügung. Durch einen Klick auf entfernen wird die Mitgliedskontoinformation aus der Buchung entfernt. Damit können Fehleingaben korrigiert werden.

![](../assets/sollbuchung-zuordnung-soll+ist.png)

Der obige Dialog hat zwei Registerkarten:
- Istbuchung einer Sollbuchung zuordnen
- Sollbuchung erzeugen und Istbuchung zuordnen

Die erste Karte dient der Zuordnung einer Istbuchung auf eine vorhandene Sollbuchung \(z.B. aus einem Abrechnungslauf\).

Auf der zweiten Karte kann alternativ in einem Schritt automatisch zuerst eine \(neue\) Sollbuchung erzeugt werden und dieser dann sogleich die Istbuchung zugeordnet werden. So können z.B. Spenden bequem bei einem Mitglied oder Nicht-Mitglied verbucht werden.

Hier kann nur nach dem Namen gefiltert werden

Bei beiden Karten kann zusätzlich "Erlaube Teilstring Vergleich" angehakt werden. Mit dieser Option werden auch Namensteile gefunden \(Suchbegriff "Anna" liefert alle Mitglieder in deren Vor- oder Nachname anna, bspw. Hannah Muster, Anna Test, Maria Hannauer...\). Sonst werden nur vollständige Namen gefunden \(Suchbegriff "Max Mustermann" findet alle Mitglieder deren Vor- oder Nachname genau Max ist oder deren Vor- oder Nachname exakt Mustermann ist, bspw. Max Mustermann, Anna Mustermann, Karl Max\).

## Rechnungen

Siehe [Rechnungen.](rechnungen.md)

## Mahnungen

Siehe [Mahnungen](mahnungen.md)

Spalten im Export

Exportieren Sie Rechnungsdaten oder Mahnungsdaten so haben Sie in der CSV Datei die Spalten des Mitglieds und des Mitgliedskontos

