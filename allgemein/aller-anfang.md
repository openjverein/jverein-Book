# Aller Anfang

## Grundlagen einrichten

### Bankzugang einrichten

Die Einrichtung der Bankzugänge etc. in Hibiscus ist hier beschrieben: [https://willuhn.de/wiki/doku.php?id=handbuch](https://willuhn.de/wiki/doku.php?id=handbuch)

### JVerein einrichten

Nach dem Einrichten von Hibiscus, muss JVerein eingerichtet werden. Dazu wählt man entweder den Knopf "Einstellungen" oder Navigiert über die "Navigation" nach unten zu "OpenJVerein" dort zu "Administration" und dort ebenfalls zu "Einstellungen".

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/aller_anfang_-_erster_start_-_hauptuebersicht_2.png" alt="" /></picture>

Die vorzunehmenden Einstellungen sind selbsterklärend. Man sollte jeden Reiter sorgfältig prüfen und nach besten Wissen ausfüllen. Am besten können dazu auch die entsprechenden Hilfeseiten kontaktiert werden.

<picture><img src="https://github.com/openjverein/jverein-Book/raw/master/assets/aller_anfang_einstellungen.png" alt="" /></picture>

#### Allgemein

* Vereinsdaten ausfüllen
* IBAN und Gläubiger-ID werden benötigt falls Lastschriften eingezogen werden sollen
* Sollen altersbezogene Mitgliedsbeiträge (Altersstaffel) bestehen, dann muss "Mitglieder Geburtsdatum" gesetzt werden

#### Anzeige

OpenJVerein ist sehr umfangreich und startet darum mit einem minimalen Oberfläche. Weitere Funktionen können hier aktiviert werden. Diese erscheinen dann in der Oberfläche.

Auch lässt sich das Verhalten der Anzeige konfigurieren.

####  Mitglieder Ansicht

Kann so bleiben.

####  Abrechnung

Hier sollte die Entscheidung über das [Beitragsmodell](beitragsmodelle.md) getroffen werden. 

Entscheidung! Externe oder von JVerein vergebene Mitgliedsnummern für die Mandatsreferenznummer! Diese kann und sollte im Nachhinein nicht geändert werden.

Bei Abbuchung der Mitgliedsbeiträge per Lastschirft, muss bei "Verrechnungskonto für Lastschriften" ein Konto ausgewählt werden. (Erst unter Buchführung->Konten anlegen).

#### Verzeichnisse

Zum aktuellen Zeitpunkt weniger von Interesse.

#### Vorlagen

Zum aktuellen Zeitpunkt weniger von Interesse.

#### Spendenbescheinigung

Falls unter Anzeige "Spendenbescheinigungen" aktiviert wurde, hier alles ausfüllen. Falls eigene Vorlagen für Spendenbescheinigungen benutzt werden sollen, müssen diese erst unter "Administration->Mitglieder->Formulare" eingerichtet werden.

#### Buchführung

Für Umsatzsteuer pflichtige Vereine sind hier die entsprechenden Optionen auszuwählen.

#### Rechnungen

Bei der Verwendung von Rechnungen sollte hier die Form der Rechnungsnummer angegeben werden (Z.B. 2026-$rechnung_nummer).

#### Mail

Alles ausfüllen falls Mails verschickt werden sollen.

Tipp: die IMAP Funktion zur Speicherung von ausgehenden E-Mails ist hilfreich. Dies ist jedoch auch mit der "Immer Bcc an Adresse" ausreichend 'protokolliert'.

#### Statistik

Kann so bleiben (vorerst).

#### Reports

Kann so bleiben (vorerst).

### Weitere Einstellungen

Folgende Einstellungen müssen noch vorgenommen werden, um JVerein produktiv zu machen:

* Buchführung->Konten: Konten aus Hibiscus "importieren" / übernehmen
* Administration->Mitglieder-Beitragsgruppen - hier mindesten eine Beitragsgruppe einrichten
* Bei Verwendung von Rechnungen muss unter Administration->Mitglieder->Formulare ein  Rechnungsformular erstellt werden
* Administration->Buchführung->Buchungsklassen: - hier mindestens den "Ideellen Bereich" einrichten
* Administration->Buchführung->Buchungsart - hier mindestens "Mitgliedsbeitrag" einrichten
* Administration->Buchführung->Steuer - Bei Umsatzzteuerpflicht hier die Steuersätze anlegen

Buchungsklassen und Buchungsarten können alternativ auch als ganzer Kontenrahmen importiert werden. Administration->Buchführung->Kontenrahmen-Import

{% file src="skr42.xml" %}
Download SKR42 (Kontenrahmen-Import XML V 2)
{% endfile %}
{% file src="skr49.xml" %}
Download SKR49 (Kontenrahmen-Import XML V 1)
{% endfile %}

An diesem Punkt sollte JVerein beendet werden um den Benutzerordner zu sichern. Der Sinn dahinter ist, dass das folgenden Ausprobieren Spuren in den Datenbanken hinterlässt. Einige Benutzer möchten mit einer "sauberen" Datenbank arbeiten. Sauber wird hierbei unter anderem so definiert, dass keine Testbuchungen oder Testkategorien existieren UND die Datenbankzähler (stetig fortlaufende Nummern) "richtig" bei 1 starten. Das Ausprobieren und Testen der Software treibt die Datenbankzähler jedoch in die Höhe. Funktionell dürfte sich bei der einen oder anderen Variante kein Unterschied ergeben.

Wie man sich auch entschieden hat, einige Testungen sind erforderlich, um die Software und ihr Potential richtig zu verstehen. Folgendes Vorgehen ist ratsam:

ca. 3 Mitglieder anlegen (je nach dem: es ist ratsam, einen "echten" Benutzer - z.B. sich selbst - anzulegen um eine ECHTE Test SEPA Lastschrift durchführen zu können.

* die eingetragenen E-Mail Adressen sollten echt sein und zu Ihnen führen (demjenigen, der das hier liest). Damit können die versandten E-Mail kontrolliert werden.
