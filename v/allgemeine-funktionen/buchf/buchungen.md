# Buchungen

## Liste der Buchungen

Die im System gespeicherten Buchungen können nach folgenden Kriterien selektiert werden:

* Konto
* Buchungsart
* Projekt
* Von Datum
* Bis Datum
* Betrag
* Enthaltener Text
* Mitglied zugeordnet

![](img/BuchungenListeView.png)

Mit einem Doppelklick auf eine Buchung wird die Detailansicht zur Bearbeitung geöffnet. Mit einem rechten Mausklick öffnet sich ein Kontextmenü. Damit können Buchungen bearbeitet werden und bestehende Buchungen gelöscht werden. Der Export der Daten ins PDF oder CSV Format wird durch einen Klick auf PDF/CSV angestoßen.

Folgende Buttons sind vorhanden:

* Import: Import von Buchungen aus einer CSV Datei. Siehe [Buchungsimport](../buchf/buchungsimport.md)
* CSV: Die über die Suchkriterien ausgewählten Buchungen können mit einem Klick auf CSV als CSV-Datei ausgegeben werden. Dabei werden bei Nutzung des Mitgliedskontos ggfls. auch die Daten des Mitgliedes ausgegeben.
* PDF Buchungsjournal: Auflistung aller Buchungen nach verschiedenen Sortierungen
* PDF Einzelbuchungen: Auflistung aller Buchungen nach Buchungsarten
* PDF Summen: Ausgabe der Summen pro Buchungsart
* Zuordnung: Zuordnung von Buchungen zu Sollbuchungen (siehe unten)
* Neu: Neue Buchung erzeugen

Die PDF-Auswertungen sind hier abrufbar. Ausführlich beschrieben werden sie im Artikel [Buchführung Zusammenhänge](../../../sonstiges/buchfuhrung-zusammenhange.md).

Folgende Menü Einträge sind vorhanden:

* Bearbeiten: Öffnet die Detailansicht für die selektierte Buchung
* Duplizieren: Öffnet die Detailansicht für eine neue Buchung mit den Daten der selektierten Buchung
* Gegenbuchung: Öffnet die Detailansicht für eine neue Buchung um eine Gegenbuchung zur selektierten Buchung zu erstellen Der Menüpunkt ist nur verfügbar wenn die Buchungsart der selektierten Buchung der Art "Umbuchung" ist. In der Gegenbuchung ist der negative Betrag der selektierten Buchung eingetragen. Nach Auswahl der Aktion wird erst ein Dialog zur Auswahl des Gegenkontos geöffnet. Dieser Dialog wird übersprungen wenn in der Konfiguration eines Kontos die Buchungsart der selektierten Buchung konfiguriert ist. In diesem Fall wird sofort das entsprechende Konto eingetragen. Siehe [Konten](konten.md).
* Splitbuchung: Erzeugt eine Splitbuchung. Siehe [Splittbuchungen](../buchf/splittbuchungen.md)
* Auflösen: Löst eine oder mehrere selektierte Splitbuchungen auf. Es werden die Gegenbuchung und die enthaltenen Buchungen gelöscht
* Neues Anlagenkonto: Für die selektierte Buchung wird ein Anlagenkonto erzeugt
* Buchungsart zuordnen: Es öffnet ein Dialog zur Zuordnung einer Buchungsart
* Sollbuchung zuordnen: Es öffnet ein Dialog zur Zuordnung einer Sollbuchung
* Projekt zuordnen: Es öffnet ein Dialog zur Zuordnung eine Projekts
* Kontoauszug zuordnen: Es öffnet ein Dialog zur Zuordnung eines Kontoauszugs
* Löschen: Löscht die Buchung

Buchungen können nur neu aufgenommen, geändert oder gelöscht werden, wenn sie nicht durch einen [Jahresabschluss](jahresabschluss.md) abgeschlossen wurden.

## Automatische Zuordnung von Buchungen zu Sollbuchungen

In der Ansicht Buchführung -> Buchungen gibt es den Button "Zuordnung", mit dem eine automatische Zuordnung von Buchungen zu Sollbuchungen vorgenommen werden kann. Diese kann auf Basis einer eindeutigen IBAN, der Mitgliedsnummer im Verwendungszweck und/oder den eindeutigen Vor- und Nachname im Verwendungszweck vorgenommen werden. Über das Start- und Enddatum kann der Suchbereich von aktiven Mitgliedern, Buchungen und Sollbuchungen eingeschränkt werden.

![](img/AutomatischeSollbuchungZuordnung.png)

Folgende Zuordnungsregeln bestehen:

* Ist eine IBAN, oder der Vor- und Nachname über den angegeben Suchzeitraum eines aktiven Mitglieds nicht eindeutig, findet keine Zuordnung mit dieser Zuordnungsart für dieses Mitglied statt.
* Wurden mehrere Zuordnungsarten auf einmal angegeben (IBAN, Mitgliedsnummer, Vor- und Nachname) wird eine Zuordnung in der genau dieser Reihenfolge versucht.
* Wurde unter Administration -> Einstellungen -> Anzeige „externe Mitgliedsnummer“ angegeben, wird anstatt der Mitgliedsnummer mit der externe Mitgliedsnummer im Verwendungszweck gesucht, falls diese Zuordnungsart gewählt wurde findet eine Zuordnung nur statt, wenn sowohl das Mitglied als auch die Sollbuchung den Zahlungsweg Überweisung aufweist.
* Der Betrag der Buchung muss genau mit dem offenen Betrag der Sollbuchung übereinstimmen, damit eine Zuordnung erfolgt.
* Gibt es mehrere Buchungen und Sollbuchungen, die in den angegebenen Zeitraum passen würden, erfolgt die Zuordnung mit dem jeweils ältesten zuerst.

Nach der Suche wird ein Dialog angezeigt, der die Zuordnungen dem Nutzer präsentiert. Dieser kann diese Zuordnungen auf Wunsch dann persistieren lassen.

![](img/AutomatischeZuordnungBestaetigen.png)

## Buchung

![](img/BuchungDialog.png)

Siehe auch [Sollbuchungen](../mitglieder/mitgliedskonto.md), [Splittbuchungen](../buchf/splittbuchungen.md)
