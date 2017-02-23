# Anleitung Jameica Portable

**Erstellung einer portablen Version von Jameica mit Plugins für/unter Windows mit „fixen“ Pfaden.**

_Beitrag von Marco Hügel_

## Quellen

Zur Erstellung einer portablen Version wird das Java Framework Jameica benötigt, sowie die gewünschten Plugins. Downloads finden sich wie gehabt unter folgenden Links:

* [http://www.willuhn.de](http://www.willuhn.de) \(Jameica Framework, Hibiscus, Syntax, …\)
* [http://www.jverein.de](http://www.jverein.de)\(Vereinsverwaltung\)
* Weitere: [https://www.willuhn.de/products/jameica/plugins.php](https://www.willuhn.de/products/jameica/plugins.php)

Weiterhin benötigt man noch die portable Version von Java \(jPortable\), die man sich hier herunterladen kann:

* [http://portableapps.com/apps/utilities/java\_portable](http://portableapps.com/apps/utilities/java_portable)

Nachfolgend beschreibe ich die portable Installation auf einem USB-Stick, welcher als Laufwerk E: in meinem System eingebunden ist. Sofern dies bei Euch anders ist, bitte entsprechend berücksichtigen.

Auf dem Stick habe ich ein Verzeichnis E:\Portable angelegt, worunter meine portablen Anwendungen, als auch Daten liegen sollen. Unterhalb dieses Verzeichnisses, habe ich ein Verzeichnis „Data“ angelegt, also E:\Portable\Data. Hier sollen künftig die Daten meiner portablen Anwendungen liegen. Zur Unterscheidung der Daten pro Anwendungen, habe ich hierunter nochmals einen Ordner „jameica“ angelegt. In diesem Ordner E:\Portable\Data\jameica sollen also künftig die Daten von Jameica mit den Plugins liegen. Das ganze sieht dann so aus:

![](/assets/Jamport01.png)

Nun werden Jameica und die Plugins auf den Stick entpackt, hierzu verwende ich bei mir das Programm 7zip. Natürlich kann jedes andere Packprogramm dafür verwendet werden.

Das Java Framework Jameica, entpacke ich dann direkt nach E:\Portable:

![](/assets/Jamport02.png)

Ergebnis:

![](/assets/Jamport03.png)

Anschließend werden die Plugins auf gleichem Wege nach E:\Portable\jameica\plugins entpackt. Beispielhaft anhand der Plugins Hibiscus \(Onlinebanking\) und JVerein \(Vereinsverwaltung\), sieht das dann so aus:

![](/assets/Jamport04.png)

Zur Installation der portablen Java-Version bitte die entsprechende Datei starten. Bei der Pfadauswahl dann den Pfad E:\Portable\CommonFiles\Java wählen wie hier:

![](/assets/Jamport05.png)

Da noch einige Dateien aus dem Internet heruntergeladen werden müssen, kann die Installation je nach Internetverbindung einige Minuten dauern.

Nach Fertigstellung der Java-Installation wären die Vorbereitungen abgeschlossen, und es geht an den portablen Starter für Jameica.

Die Startdateien die wir zur Erstellung der portablen Starter benötigen, liegen im Verzeichnis E:\Portable\jameica, und lauten wie folgt:

* jameica-win32.jar \(für Windows 32bit\)
* jameica-win64.jar \(für Windows 64bit\)

Die ebenfalls vorhandenen EXE-Files können an der Stelle nicht genutzt werden, da wir für die volle Portabilität natürlich das portable Java nutzen wollen.

## Wo sollen die portablen Starter angelegt werden?

Zunächst einmal sollte festgelegt werden, in welchem Verzeichnis die portablen Startdateien abegelegt werden sollen. Denkbar wäre das Programmverzeichnis von Jameica \(E:\Portable\jameica\), denkbar aber auch das übergeordnete Verzeichnis E:\Portable.

Ich beschreibe das ganze zunächst auf Basis des Verzeichnisses E:\Portable\jameica.

Zunächst legen wir uns per rechter Maustaste ein neues Textdokument im Ordner E:\Portable\jameica an:

![](/assets/Jamport06.png)

Das Textdokument bitte gleich umbenennen nach „JameicaPortableWin32.bat“ wie folgt:

![](/assets/Jamport07.png)

Die erscheinende Meldung bzgl. der Umbenennung mit „Ja“ bestätigen.

Nun per rechter Maustaste die so erstellte Datei bearbeiten:

![](/assets/Jamport08.png)

Es öffnet sich der normale Windows Editor \(Notepad\) und wir können nun den Startbefehl in diese Datei eingeben, der Da lautet:

![](/assets/Jamport09.png)

...oder zum kopieren&einfügen:

```
start ..\CommonFiles\Java\bin\java.exe -jar jameica-win32.jar -f ..\Data\jameica
```

Die Datei noch über Datei → Speichern sichern, und wir wären an der Stelle schon fertig und könn\(t\)en den Startvorgang mit dieser Datei testen.

Wer Windows 64bit einsetzen möchte, kann analog eine neue Textdatei „JameicaPortableWin64.bat“ anlegen und diese anschließend bearbeiten.

Der Inhalt der Datei ist dann analog der Datei für Windows 32bit, nur eben mit dem Aufruf der Jameica-Version für 64bit:

```
start ..\CommonFiles\Java\bin\java.exe -jar jameica-win64.jar -f ..\Data\jameica
```



