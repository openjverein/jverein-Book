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

## Mitgliedskontenübersicht {#mitgliedskontouebersicht}

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

## Buchungen dem Mitgliedskonto zuordnen {#mitgliedskontozuordnen}

> Unter Buchführung&gt;[Buchungen](/buchungen.md) ist eine Buchung auszuwählen und doppelt anzuklicken:

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

Siehe [Mahnungen](/mahnungen.md)

Spalten im Export

Exportieren Sie Rechnungsdaten oder Mahnungsdaten so haben Sie in der CSV Datei die Spalten des Mitglieds und des Mitgliedskontos

