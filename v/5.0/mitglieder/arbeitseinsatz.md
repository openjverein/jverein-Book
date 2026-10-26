# Arbeitseinsätze

### Aktivierung

Zur Nutzung der Arbeitseinsätze ist die Option unter Administration->Einstellungen->Anzeige zu aktivieren.


### Allgemeines

Neben Geldzahlungen kann als Beitrag auch Arbeitsleistung dienen.

In den betroffenen [Beitragsgruppen](../administration/mitglieder/beitragsgruppen.md) wird die Anzahl der Pflichtstunden und der Betrag für nicht erbrachte Stunden hinterlegt

### Erstellung

Die Arbeitseinsätze können erstellt werden

* in den Mitglied Details (siehe [Arbeitseinsatz](content/arbeitseinsatz.md))
* über das Kontextmenü eines Mitglieds (siehe [Mitglieder](content/mitglieder.md))
* aber auch in der Liste der Arbeitseinsätze

## Liste der Arbeitseinsätze

Der Übersicht View für Arbeitseinsätze zeigt alle vorhandenen Arbeitseinsätze an.

Über den Filterbereich lässt sich nach verschiedenen Kriterien filtern.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_ArbeitseinsaetzeListeView.png" alt="" /></picture>

Folgende Buttons sind vorhanden:
* Hilfe: Ruft die Online Hilfe auf
* Auswertung: Öffnet den Auswertung Dialog (siehe unten)
* Zusatzbeträge generieren: Öffnet den Dialog zum generieren von Zusatzbeträgen für nicht geleistete Arbeitsstunden
* Abrechnung: Öffnet den Dialog zur Abrechnung von nicht geleistete Arbeitsstunden
* Neu: Damit kann ein neuer Arbeitseinsatz eingerichtet werden

Durch einen Doppelklick wird die Bearbeitung eines Arbeitseinsatzes eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Löschen: Damit kann ein Arbeitseinsatz gelöscht werden
* Mitglied anzeigen: Damit können die Daten des Mitglieds angezeigt werden

## Arbeitseinsatz

Mit einem Klick auf Neu oder Bearbeiten öffnet sich folgender Dialog:

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_ArbeitseinsatzView.png" alt="" /></picture>

Im Feld Mitglied lässt sich das Mitglied auswählen.

Geben Sie das Datum ein, an dem die Stunden geleistet wurden, die Anzahl der Stunden und, im Feld Bemerkung, was geleistet wurde.

In den Einstellungen von JVerein auf der Ansicht Beiträge können Sie ein Arbeitsstunden Modell ändern und negative Stunden einstellen.

Danach kann hier beim Erfassen von Arbeitsstunden im Feld Stunden auch ein negativer Wert eingetragen und damit die Sollstunden des Mitglieds erhöht werden. Damit kann man Dienstleistungen des Vereins, die mit Arbeitsstunden gegengerechnet werden können, einfach erfassen und abrechnen.

### Auswertung

Der Auswertung Dialog wird über den entsprechenden Button aufgerufen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_ArbeitseinsaetzeAuswertungDialog.png" alt="" /></picture>

Im Filterbereich kann nach Jahr und der Art der Auswertung gefiltert werden.

Die Listeneinträge lassen sich als PDF oder CSV exportieren. Die zu exportierenden Spalten lassen sich in dem erscheinenden Dialog einstellen. Die Relation der Spaltenbreiten im Dialog entspricht der in der angezeigten Liste.

### Zusatzbeträge generieren

Über den Button Abrechnung (siehe unten) lassen sich nicht geleistete Arbeitsstunden direkt abrechnen. Sollen die Forderungen wegen der Arbeitsstunden mit weiteren Forderungen wie z.B. Mitgliedsbeiträgen gemeinsam abgerechnet werden, lassen sich Zusatzbeträge für die nicht geleisteten Arbeitsstunden generieren. Diese können dann in einem separaten Abrechnungslauf mit abgerechnet werden. 

Der Dialog zum generieren von Zusatzbeträgen wird über den entsprechenden Button aufgerufen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_ArbeitseinsaetzeZusatzbetraegeDialog.png" alt="" /></picture>

Im Filterbereich kann nach Jahr gefiltert werden. Als Art wird automatisch Minderleistung benutzt.

In den Parametern für die generierten Zusatzbeträge lässt sich folgendes einstellen:
* Zahlungsgrund: Dieser wird beim Zusatzbetrag gesetzt und erscheint später auch in der Lastschrift
* Fälligkeit: Fälligkeit der Forderung
* Zahlungsweg: Hier kann ein abweichender Zahlungsweg eingegeben werden
* Mitglied zahlt selbst: Falls beim Mitglied ein abweichender Zahler für Beiträge konfiguriert ist, kann hier ausgewählt werden ob trotzdem da Mitglied den Zusatzbetrag bezahlen soll

Neben der Liste der betroffenen Mitglieder werden auch Fehler und Warnungen angezeigt ähnlich wie bei einem Abrechnungslauf (siehe [Abrechnung](../abrech/abrechnung.md)).

### Abrechnung

Über den Button Abrechnung lassen sich nicht geleistete Arbeitsstunden direkt abrechnen. Es wird dabei direkt ein Abrechnungslauf durchgeführt ohne dass Zusatzbeträge generiert werden.

Die Funktionalität entspricht dabei weitgehend dem Feature [Forderung](forderung.md). Lediglich der Betrag ist individuell für die jeweiligen Mitglieder. Für eine genauere Beschreibung siehe dort.

Der Dialog zur Abrechnung wird üben den entsprechenden Button aufgerufen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_ArbeitseinsaetzeAbrechnungDialog.png" alt="" /></picture>
