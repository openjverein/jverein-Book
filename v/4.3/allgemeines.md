# Allgemeines

## Panel Buttons

In der Panelleiste oben sind verschiedene Buttons verfügbar. Sie werden bei Ansichten mit Tabellen angezeigt.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_Panelbuttons.png" alt="" /></picture>

Die ersten drei Buttons werden von JVerein bereit gestellt:
* Spaltenauswahl: Es lässt sich auswählen, welche Spalten in der Tabelle angezeigt werden sollen
* CSV: Gibt die ausgewählten Spalten der angezeigten Tabelle als CSV Datei aus
* PDF: Gibt die ausgewählten Spalten der angezeigten Tabelle als PDF aus

### Spaltenauswahl

Beim Spaltenauswahl Dialog erfolgt eine Dialogabfrage in dem man die anzuzeigenden Spalten auswählen kann. 

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_SpaltenauswahlDialog.png" alt="" /></picture>

Buttons:
* Help: Zeigt diese Hilfe an
* Reset: Setzt die selektierten Spalten auf Defaultwerte zurück
* Speichern: Übernimmt die Auswahl in die Tabelle
* Abbrechen: Beendet den Dialog

### CSV Export Dialog

Die im Dialog ausgewählten Spalten lassen sich als CSV exportieren.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogCSV.png" alt="" /></picture>

Buttons:
* Help: Zeigt diese Hilfe an
* Reset: Setzt die selektierten Spalten auf Defaultwerte zurück
* Starten: Startet den Export der Daten
* Abbrechen: Beendet den Dialog

PS: Die Spaltenreihenfolge lässt sich durch Umsortieren (Drag & Drop) mit der Maus ändern.

### PDF Export Dialog

Die im Dialog ausgewählten Spalten lassen sich als PDF exportieren.

Allgemeine Buttons:
* Help: Zeigt diese Hilfe an
* Starten: Startet den Export der Daten
* Abbrechen: Beendet den Dialog

#### Spalten Lasche

In de Lasche Spalten werden die zu exportierenden Spalten ausgewählt und es lässt sich das relative Verhältnis der Spaltenbreiten im PDF Report einstellen.
 
Defaultmäßig werden die Breiten aus der angezeigten Tabelle übernommen. Die Breiten sind keine absoluten Werte sondern geben nur das Verhältnis der Breiten zueinander an. Bei der Ausgabe wird die verfügbare Breite im PDF im Verhältnis der Breitenwerte aufgeteilt. Eine Spalte mit doppeltem Wert von einer anderen Spalte wird also bei der Ausgabe doppelt so breit.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogPDF.png" alt="" /></picture>

Buttons:
* Breiten zurücksetzen: Setzt die Breiten im Verhältnis zur angezeigten Tabelle zurück
* Reset: Setzt die Spaltenauswahl und die Breiten auf Defaultwerte zurück

PS: Die Spaltenreihenfolge lässt sich durch Umsortieren (Drag & Drop) mit der Maus ändern.

Wird ein Report über die Export Buttons z.B. bei den Mitgliedern oder Buchungen generiert fehlt diese Lasche im Dialog weil die entsprechenden Werte im Ausgabecode implementiert sind.

#### Ränder Lasche

Im Ränder Tab kann der Randabstand der Tabelle im PDF Report eingestellt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogRaender.png" alt="" /></picture>

Buttons:
* Reset: Setzt die Werte auf Defaultwerte zurück

#### Formular Lasche

Im Formular Tab kann das Vordergrund und Hintergrund Formular ausgewählt werden, ob Header oder Zellen transparent sein sollen oder ob im Querformat gedruckt werden soll.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogFormular.png" alt="" /></picture>

Buttons:
* Reset: Setzt die Werte auf Defaultwerte zurück

#### Schriftart Lasche

Für die Tabellen Header Zeile und den Tabelleninhalt lässt sich jeweils die Schriftart, Schriftgröße und Hintergrundfarbe (für spezielle Zellen) einstellen. Weiter kann festgelegt werden ob negative Zahlen in roter Farbe ausgegeben werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/403_TabelleExportDialogSchriftart.png" alt="" /></picture>

Buttons:
* Reset: Setzt die Werte auf Defaultwerte zurück


