# Formulare

## Allgemeines

In JVerein werden für [Spendenbescheinigungen](../../mitglieder/spendenbescheinigung.md), [Mahnung](../../druckmail/mahnungen.md), [Rechnungen](../../druckmail/rechnungen.md), [Pre-Notification](../../druckmail/pre-notification.md) und diverse Zwecke [Freie Formulare](../../druckmail/freiesformular.md) hinterlegt.

Bei der Generierung von PDF Dokumenten können die Formulare mit Formularfeldern bedruckt werden.

Bei fest eingebauten Reports ohne Formular z.B. Kontoauszug oder Personalbogen kann ein fester Hintergrund und Vordergrund platziert werden. Hintergründe und Vordergründe müssen ebenfalls als Formulare definiert werden. Sie werden so genommen wie sie sind. Es lassen sich keine Formularfelder platzieren.

## Liste der Formulare

Eine Liste der Formulare kann über den Eintrag Administration->Mitglieder->Formulare im Navigationsbaum angezeigt werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_FormulareListeView.png" alt="" /></picture>

Mit Neu kann ein neues Formular eingerichtet werden.

Durch einen Doppelklick wird die Bearbeitung eines Formular eingeleitet.

Das Kontextmenü bietet folgende Optionen:

* Bearbeiten: Der ausgewählte Eintrag wird zum Bearbeiten geöffnet
* Anzeigen: Das fertige Formular wird als PDF generiert und angezeigt
* Duplizieren: Es wird eine Kopie des Formulars erzeugt
* Löschen: Damit kann ein Formular, welches noch nicht verwendet wurde, gelöscht werden
* Exportieren: Damit können die selektierten Formulare inklusive Formular Datei und Formularfelder exportiert werden

Mit dem Button Importieren können vorher exportierte Formulare importiert werden.

## Formular

Über die Funktion Neu oder Bearbeiten wird ein Formular Dialog angezeigt.

Der Dialog beinhaltet die Formular Attribute und zeigt eine Liste der Formularfelder die auf die Datei Vorlage gedruckt werden sollen.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/402_FormularView.png" alt="" /></picture>

## Formular Attribute

### Bezeichnung

Name des Formulars.

### Art

Art des Formulars. Es gibt an für welche Ausgabe das Formular verwendet werden kann. Optionen sind:

* Spendenbescheinigung
* Rechnung
* Mahnung
* Freies Formular
* Sammelspendenbescheinigung
* SEPA-Prenotification
* Sachspendenbescheinigung
* Hintergrund/Vordergrund
* Buchungsreport

### Datei

Datei für das Formular.

Man erstelle ein einfaches Dokument/Formular in Word, Open-/LibreOffice oder was auch immer (Dankeschönschreiben, Rundschreiben, whatsoever...) und lasse an den entsprechenden Stellen im Schreiben einfach leeren Platz (weisse unbeschriebene Stellen) als Platzhalter für die später von JVerein einzufügenden Daten.

Macht Euch hier genau Gedanken, wie Euer Formular aussehen soll und was Ihr später alles an Daten einfügen möchtet.

Bitte in der Textverarbeitungssoftware KEIN FORMULAR erstellen - nur einfach ein Dokument mit weißen/leeren Stellen als Platzhalter für später!! Das reicht.

Nun muss aus dem Dokument noch ein PDF gemacht werden. Das geht mit einem virtuellen PDF-Drucker (z.B. FreePDF XP oder PDFCreator) oder mit Adobe Acrobat (nicht mit dem Reader, der kann halt nur lesen :-) ) oder einfach in Open-/LibreOffice mit dem PDF-Export. Das fertige PDF (mit den weißen/leeren Stellen für die späteren Daten aus jVerein) hat keinerlei Funktionen eingebaut (keine Formularfelder, nur weiße/leere Stellen im Text an der richtigen Stelle).

Dann erstellt man in JVerein unter "Administration->Formulare" ein neues Formular. Dazu unten auf "neu" gehen, Bezeichnung und Art auswählen ("Art" gibt an, wann und wo dieses Formular in JVerein verfügbar sein wird).

Nun noch die gerade erstellte PDF-Datei auswählen und auf "speichern" klicken.

### Fortlaufende Nummer

Fortlaufende Nummer z.B. bei Rechnungen. Über das Feld lässt sich die Nummer zurücksetzen.

### Formularverknüpfung

Formulare können verknüpft werden um Abhängigkeiten untereinander aufzubauen. Die Spalte "Verknüpft mit" in der Formular-Übersicht zeigt die Abhängigkeiten an. Bei verknüpften Formularen werden die fortlaufenden Nummern (Formularfeld "zaehler") gleichgesetzt und untereinander aktualisiert. Eine Vererbung der Verknüpfung ist nicht implementiert. Formulare können nicht mit sich selbst verknüpft werden. Ein verknüpftes Formular kann nicht gelöscht werden, bis die Abhängigkeiten entfernt wurden.

## Formular Buttons

### Anzeigen

Das fertige Formular wird als PDF generiert und angezeigt.

### Speichern

Nach Eingabe oder ändern der Formular Attribute muss das Formular gespeichert werden.

## Formularfelder Buttons

### Export

Exportiert die Formularfelder des aktuellen Formulars.

### Import

Importiert Formularfelder aus einer Datei die mit Export erzeugt wurde. Es werden alle bestehenden Formularfelder der aktuellen Formulars vor dem Import gelöscht.

### Neu

Erzeugt ein neues Formularfeld für das aktuelle Formular.

## Formularfelder

Bevor Formularfelder angelegt werden können muss das Formular gespeichert werden.

Nun kommt die eigentliche Arbeit:

Bei den Formularfelder Buttons klickt Ihr auf "Neu", um das erste einzufügende Datenfeld auszuwählen und zu positionieren: (Die spätere Reihenfolge Eurer Datenfelder ist egal! Ihr könnt auch erst hinten anfangen)

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/400_Formularfeld.png" alt="" /></picture>

### Name

Unter "Name" könnt Ihr nun Text gemischt mit Variablen eingeben. Der Inhalt wird mit Velocity geparst, es können also auch alle Velocity Befehle verwendet werden (#if #else, #for etc.) Siehe auch [Velocity](https://velocity.apache.org/engine/1.7/user-guide.html) 

Außerdem ist es in Formularfeldern möglich, HTML zu verwenden. So können auch komplexe Tabellen, Listen etc. mit unterschiedlichen Formatierungen in einem Feld erstellt werden. Es sind die meisten HTML Tags sowie Css-Styles möglich. (Das HTML wird mit iText XMLWorker geparst). Das Einbinden externer Resourcen (Bilder, css) ist aus Sicherheitsgründen nicht möglich.

Es ist möglich, den Inhalt eines Feldes über mehrere Seiten verteilt auszugeben. Dafür ist das Feld [[newPage]] nötig. Dort wo dieses Feld ist, wird eine neue Seite erstellt (mit der gleichen Seite wie die Ursprungsseite als Vorlage), und der Folgende Text dort auf der gleichen Position ausgegeben. Bei der Nutzung von HTML zusammen mit [[newPage]] ist darauf zu achten, dass alle Tags vor [[newPage]] geschlossen sind. Es wird als komplett neues HTML geparst.

Zusammen mit Velocity, HTML und dem [[newPage]] Tag lassen sich komplexe Dokumente erstellen. Hier ein Beispiel:
Rechnung mit vielen Positionen und ggf. mehreren Seiten, inkl Übertrag.
```
#set($positionenProSeite=10)
#set($positionenProSeiteFolgeseiten=16)
#set($tageZahlungsziel=14)
#set($versatzErsteSeite=100)
#macro(kopf $first)
<html>
<head>
    <style>
        table{border-spacing:0px; }
        td,th{padding:1px;vertical-align:top;}
        th{border-bottom:1px solid black;}
	tr.sum td{border-top:1px solid black;}
	.betrag{text-align:right;}
    </style>
</head>
#if($first)
<div style="height:${versatzErsteSeite}mm"></div>
#else
#set($positionenProSeite=$positionenProSeiteFolgeseiten)
<p><small>Rechnung: $rechnung_nummer vom $rechnung_datum | $rechnung_vorname $rechnung_name</small></p>
#end
<body>
    <table>
        <tr><th width="80">Datum</th><th width="350">Bezeichnung</th><th width="60" class="betrag">Betrag</th></tr>
#end

#macro(fuss $last)
    </table>
#if($last)
    #set($date = $dateformat.parse($rechnung_datum))
    #set($time = $date.getTime() + 1000*60*60*24*$tageZahlungsziel)
    $date.setTime($time)
    <p>Bitte überweisen Sie den Betrag bis zum $dateformat.format($date) auf das angegebene Konto.</p>
    <p><br /><br />Mit freundlichen Grüßen</p>
#end
<table><tr><td style="height:100%;vertical-align:bottom;padding-bottom:10mm;padding-left:2px;">
<table><tr><td width="350">
<pre>$verein_name
$verein_strasse
$verein_plz $verein_ort</pre>
</td><td width="300">
<pre>$verein_bank_name
IBAN: $verein_iban
BIC: $verein_bic
Steuernummer: $verein_steuer_nr</pre></td></tr></table>
</td></tr></table>
</body>
</html>
#end

#set($daten=$rechnung_buchungsdatum.split("\n"))
#set($betraege=$rechnung_betrag.split("\n"))
#set($texte=$rechnung_zahlungsgrund.split("\n"))
#set($n=0)
#set($uebertrag=0.0)

#kopf(true)
#foreach($zeile in $texte)
    #set($i=-1+$foreach.count)
    #set($n=1+$n)
    #if($n>$positionenProSeite && $texte.size()>1+$foreach.count)
        <tr class="sum"><td></td><td></td><td>Übertrag</td><td></td><td></td><td class="betrag">$decimalformat.format($uebertrag)</td></tr>
        #fuss(false)[[newPage]]#kopf(false)
        <tr><td></td><td></td><td>Übertrag</td><td></td><td></td><td  class="betrag">$decimalformat.format($uebertrag)</td></tr>
        #set($n=1)
    #end
    <tr #if($texte.size()==$foreach.count)class="sum"#{end}>
        <td>#if($daten.size()>$i)$daten[$i]#{end}</td>
        <td>$zeile</td>
        <td class="betrag">
            #set($betrag=$betraege[$i])
            #if($betrag.length()>0)
		$betrag
                #if($betrag.contains(","))#set($betrag=$betrag.replace(".","").replace(",","."))#end
                #set($uebertrag=$uebertrag + $uebertrag.parseDouble($betrag))
            #end
        </td>
    </tr>
#end
#fuss(true)
```

### Seite

Seite auf der das Formularfeld platziert werden soll.

### Von links, Von unten

Dieses Datenfeld müsst Ihr nun Millimetergenau auf euer gerade eben generiertes PDF händisch setzen. der Punkt (0,0) liegt unten links auf der Seite!

Tipp: Druckt das Dokument aus und messt mit einem Lineal die Positionen aus.

Speichert das Ganze und zeigt euch das Ergebnis über den Anzeigen Button an.

Das müsst Ihr solange wiederholen, bis das Datenfeld an der richtigen Stelle eingefügt wurde.

Übrigens: Da das System noch nicht weiß, welchen Datensatz es beim Austesten nehmen soll, hat der Entwickler einen Dummy-Datensatz automatisch für das Erstellen und Testen des neuen Formulars bereitgestellt.

### Schriftart

Schriftart für den Text.

### Schriftgröße

Schriftgröße des Textes.

## Buttons

### Variablen anzeigen

* Zeigt einen Dialog mit verfügbaren Variablen die in das Textfeld platziert werden können
* Als Formularfelder können alle Variablen verwendet werden. Siehe [Variablen](../../../../sonstiges/variable.md)

### Speichern

* Speichert das Formularfeld

### Speichern und neu

* Speichert das Formularfeld und öffnet eine neues




## Vorlagen

Hier einige Vorlagen zum so verwenden oder weiter anpassen. Sie können herunter geladen und als Formular importiert werden.

Einfache Standardrechnung:

{% file src="../../../../assets/320_rechnung-standard.xml" %}
Einfache Standardrechnung
{% endfile %}

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_rechnung-standard.png" alt="" /></picture>

## Beispiele

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Formularroh.jpg" alt="" /></picture>

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/320_Formularausgefuellt.jpg" alt="" /></picture>
