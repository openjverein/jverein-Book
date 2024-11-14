# Sollbuchungen

### Aktivierung

Zur Nutzung der Sollbuchungen ist keine extra Aktivierung notwendig.

### Allgemeines

Sollbuchungen d.h. Beiträge, Zusatzbeträge etc. dienen dazu den Kontostand von Mitgliedern zu führen. Durch die Zuweisung von Istbuchungen kann der Kontostand ausgeglichen werden. 

Die [Abrechnung](../abrech/abrechnung.md) schreibt Sollbuchungen zu Mitgliedsbeiträgen und Zusatzbeträge in die Tabelle [Mitgliedskonto](content/mitgliedskonto.md) des Mitglieds.

### Erstellung 

Die Zusatzbeträge können erstellt werden
* über einen Abrechnungslauf (siehe [Abrechnung](../abrech/abrechnung.md) )
* in den Mitglied Details (siehe [Mitgliedskonto](content/mitgliedskonto.md)) 
* aber auch in der Liste der Sollbuchungen


## Liste der Sollbuchungen <a id="mitgliedskontouebersicht"></a>

Es gibt eine zentrale Übersicht über alle Sollbuchungen. Die Buchungen können über einen Zeitraum oder über einen Namen, bzw. Namensfragment gefiltert werden. Zusätzlich kann angegeben werden, ob nur Sollbuchungen mit Differenzen zwischen Soll und Ist \(Offene Posten oder Überzahlungen\) angezeigt werden.

Zudem lässt sich filtern ob das Mitglied per Lastschrift zahlt oder eine Mail Adresse hat. Letzteres ist interessant wenn die Rechnungen bzw. Mahnungen per Mail versendet werden sollen.

![](img/SollbuchungenListeView.png)

Durch einen Doppelklick auf die Sollbuchung wird die Sollbuchung angezeigt.

Folgende Buttons stehen zu Verfügung:
* Exportieren: Damit können die Sollbuchungen als CSV Datei exportiert werden
* Neu: Damit kann eine neue Sollbuchung eingerichtet werden

Durch einen Rechtsklick auf einen Abrechnungslauf öffnet sich ein Kontextmenü mit mehreren Optionen:
* Sollbuchung bearbeiten: Bearbeiten der Sollbuchung
* Sollbuchung löschen: Löschen der Sollguchungen
* Mitglied anzeigen: Öffnet das Mitglied zur Sollbuchung
* Rechnung erstellen: Erstellt Rechnungen für die selektierten Sollbuchungen.
* Mahnung erstellen: Erstellt Mahnungen für die selektierten Sollbuchungen.

## Sollbuchung

Mit einem Klick auf Neu oder Bearbeiten öffnet sich folgender Dialog:

![](img/SollbuchungView.png)

## Buchungen einer Sollbuchung zuordnen <a id="mitgliedskontozuordnen"></a>

Unter Buchführung&gt;[Buchungen](../buchf/buchungen.md) ist eine Buchung auszuwählen und doppelt anzuklicken:

![](ing/BuchungView.png)

Durch einen Klick auf ... neben Sollbuchung erscheint folgender Dialog:

![](img/SollbuchungZuordnungIst.png)

Der Name aus der Buchung wird in das Namensfeld übernommen. Der Inhalt wird in Wörter zerlegt und in den Spalten Name und Vorname gesucht.

PS: Alternativ erreicht man diesen Dialog auch mit einem rechten Mausklick auf einen Buchung und wählt dann den Menüpunkt "Sollbuchung zuordnen" aus.

Zur Filterung des Buchungen steht weiterhin Egal \(= eine beliebige Differenz\), Fehlbetrag oder Überzahlung zur Verfügung. Durch einen Klick auf entfernen wird die Mitgliedskontoinformation aus der Buchung entfernt. Damit können Fehleingaben korrigiert werden.

Der obige Dialog hat zwei Registerkarten:
- Istbuchung einer Sollbuchung zuordnen \(Option 1\)
- Sollbuchung erzeugen und Istbuchung zuordnen \(Option 2\)

Die erste Karte dient der Zuordnung einer Istbuchung auf eine vorhandene Sollbuchung \(z.B. aus einem Abrechnungslauf\).

Auf der zweiten Karte kann alternativ in einem Schritt automatisch zuerst eine \(neue\) Sollbuchung erzeugt werden und dieser dann sogleich die Istbuchung zugeordnet werden. So können z.B. Spenden bequem bei einem Mitglied oder Nicht-Mitglied verbucht werden.

![](img/SollbuchungZuordnungSollIst.png)

Hier kann nur nach dem Namen gefiltert werden.

In der zweiten Karte kann zusätzlich "Erlaube Teilstring Vergleich" angehakt werden. Mit dieser Option werden auch Namensteile gefunden \(Suchbegriff "Anna" liefert alle Mitglieder in deren Vor- oder Nachname anna, bspw. Hannah Muster, Anna Test, Maria Hannauer...\). Sonst werden nur vollständige Namen gefunden \(Suchbegriff "Max Mustermann" findet alle Mitglieder deren Vor- oder Nachname genau Max ist oder deren Vor- oder Nachname exakt Mustermann ist, bspw. Max Mustermann, Anna Mustermann, Karl Max\).

## Spalten im Export

Exportieren Sie Rechnungsdaten oder Mahnung Daten so haben Sie in der CSV Datei die Spalten des Mitglieds und des Mitgliedskontos
