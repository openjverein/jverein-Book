# Mitgliedskonto

## Abrechnung

Die Abrechnung schreibt Informationen zu Mitgliedsbeiträgen und Zusatzabrechnungen in die Tabelle Mitgliedskonto \(Soll\). Zusätzlich werden für den Zahlungsweg Abbuchung Informationen \(Ist\) in die Buchungstabelle der Buchführung geschrieben.

Fehlerhafte oder Test-Abrechnungen können rückgängig gemacht werden. In dem Abrechnungsformular kann durch klick auf _Rückgängig._

![](/assets/MitgliedskontoRueckgaengig.png)

eine Übersicht der Abrechnungsläufe geöffnet werden:

![](/assets/MitgliedskontoAbrechnungslaeufe.png)

Durch einen Rechtsklick auf einen Abrechnungslauf öffnet sich ein Kontextmenü mit der Option löschen:

![](/assets/MitgliedskontoAbrechnungslaeufeLoeschen.png)

Nach einer Bestätigung werden die verknüpften Datensätze aus der Mitgliedskontotabelle und der Buchungstabelle gelöscht.

## Mitgliedskontenübersicht

Es gibt eine zentrale Übersicht über alle Buchungen der Mitgliedskonten-Tabelle. Die Buchungen können über einen Zeitraum oder über einen Namen, bzw. Namensfragment gefiltert werden. Zusätzlich kann angegeben werden, ob nur Mitgliedskonten mit Differenzen zwischen Soll und Ist \(Offene Posten oder Überzahlungen\) angezeigt werden.

![](/assets/MitgliedskontenUebersicht.png)

Durch einen Doppelklick auf die Buchung erscheint das Mitglied.

![](/assets/MitgliedskontoMitglied.png)

## Mitgliedskonto beim Mitglied

![](/assets/MitgliedskontoMitglied-2.png)

In der Baumansicht werden die Summen pro Mitglied, die einzelnen Mitgliedskonten-Sollbuchungen \(Soll und zugeordnetes Ist, Rechnersymbol\), sowie die einzelnen zugeordneten Istbuchungen \(Geldscheine-Symbol\) angezeigt.

Mit einem rechten Mausklick auf das Mitglied öffnet sich ein Kontextmenü. Damit können neue Sollbuchungen aufgenommen werden.

![](/assets/MitgliedskontoNeu.png)

Mit einem rechten Mausklick auf eine Mitgliedskonto-Soll-Buchung öffnet sich ein Kontextmenü. Damit kann die Sollbuchung bearbeitet, oder, sofern keine Istbuchung zugeordnet ist, auch gelöscht werden.

## Buchungen dem Mitgliedskonto zuordnen

> Unter Buchführung&gt;Buchungen //TODO Link  ist eine Buchung auszuwählen und doppelt anzuklicken:

![](/assets/MitgliedskontoBuchungen.png)

Durch einen Klick auf ... neben Mitgliedskonto erscheint folgender Dialog:![](/assets/Mitgliedskonto-zuordnung-ist.png)

Der Name aus der Buchung wird in das Namensfeld übernommen. Der Inhalt wird in Wörter zerlegt und in den Spalten Name, Vorname und Verwendungszweck 1 gesucht.

Zur Filterung des Buchungen steht weiterhin Egal \(= eine beliebige Differenz\), Fehlbetrag oder Überzahlung zur Verfügung. Durch einen Klick auf entfernen wird die Mitgliedskontoinformation aus der Buchung entfernt. Damit können Fehleingaben korrigiert werden.

![](/assets/Mitgliedskonto-zuordnung-soll+ist.png)

Der obige Dialog hat zwei Registerkarten: nur Ist und Soll u. Ist.

Die erste Karte nur Ist dient der Zuordnung einer vorhandenen Soll-Buchung auf einem Mitgliedskonto \(z.B. aus einem Abrechnungslauf\).

Mitgliegskonto-Auswahl -&gt; Soll u. Ist

Auf der zweiten Karte Soll u. Ist kann alternativ in einem Schritt bei der Zuordnung einer Adresse automatisch zuerst eine \(neue\) Soll-Buchung erzeugt und diese dann sogleich darauf zugeordnet werden. So können z.B. Spenden bequem verbucht bei einem Mitglied oder einer weiteren Adresse verbucht werden.

Hier kann nur nach dem Namen gefiltert werden, dabei kann aber zusätzlich "Spezial-Suche" angehakt werden. Mit der Spezial-Suche werden auch Namensteile gefunden \(Suchbegriff "Anna" liefert alle Mitglieder in deren Vor- oder Nachname anna, bspw. Hannah Muster, Anna Test, Maria Hannauer...\). Sonst werden nur vollständige Namen gefunden \(Suchbegriff "Max Mustermann" findet alle Mitglieder deren Vor- oder Nachname genau Max ist oder deren Vor- oder Nachname exakt Mustermann ist, bspw. Max Mustermann, Anna Mustermann, Karl Max\).

## Rechnungen

Siehe [Rechnungen.](/rechnungen.md)

## Mahnungen

Für alle offenen Buchungen in den Mitgliedskonten können Mahnungen erstellt werden. Dabei hat man die Möglichkeit eine Mahnung für ein bestimmtes Mitglied, für eine Auswahl von Mitglieder oder für alle Mitglieder zu erstellen. Eine Buchung ist offen, wenn der Betrag der Spalte Zahlungseingang kleiner ist als der Wert in der Spalte Betrag.

Ein Mahnung kann ein PDF Dokument sein das direkt aus JVerein erstellt wird oder Sie exportieren die Daten in eine CSV Datei und erstellen die Mahnung als Serienbrief mit z.B. Microsoft Office oder Open Office.

### Mahnung für ein Mitglied

Möchten Sie eine Mahnung für ein bestimmtes Mitglied erstellen, so öffnen Sie den Dialog Mitgliedskonten. Wählen Sie den Filter so, dass die gewünschten Daten dieses Mitglieds angezeigt werden. Selektieren Sie einen Datensatz des Mitglieds und drücken die rechte Maustaste. Es öffnet sich ein Kontext-Menü. Wählen Sie hier den Menüpunkt Mahnung. Es öffnet sich hier der Dialog Mahnungen der Sie bei der Erstellung der Mahnung unterstützt.

### Mahnungen für viele Mitglieder

Möchten Sie Mahnungen für alle Mitgliedern erstellen, so öffnen Sie den Dialog Mahnungen. Sie können nun Filter setzen und damit begrenzen, dass nur Buchungen in Mitgliedskonten berücksichtigt werden, die innerhalb der Datumsgrenzen liegen.

### Mahnungen drucken

Möchten Sie Mahnungen direkt als JVerein druckfertig generieren, so müssen Sie mindestens ein Mahnungsformular angelegt haben. Die Erstellung von Mahnungsformularen ist unter Administration\|Formulare beschrieben.

Wählen Sie in der Auswahlbox Formular dasjenige Formular, mit dem Sie die Mahnungen erstellen möchten und drücken Sie dann den Schalter starten. Es öffnet sich ein Dialog der den Speicherort und den Dateinamen der PDF Datei abfragt, in die alle Mahnungen erstellt werden. Mit Bestätigen dieser Eingaben werden die Mahnungen generiert und die fertige PDF geöffnet. Diese können Sie nun ausdrucken.

### Mahnungsdaten exportieren

Sollen die Mahnungsdaten exportiert werden, so drücken Sie im Dialog Mahnung den Schalter Export. Es öffnet sich ein Dialog der den Speicherort und den Dateinamen der CSV abfragt. Bestätigen Sie diesen Dialog, werden die Mahnungsdaten in diese Dateien exportiert und können danach z.B. für einen Serienbrief verwendet werden.

## Spalten im Export

Exportieren Sie Rechnungsdaten oder Mahnungsdaten so haben Sie in der CSV Datei die Spalten des Mitglieds und des Mitgliedskontos



