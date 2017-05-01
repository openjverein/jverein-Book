# Abrechnung

## Voraussetzungen

Unter Administration \| Einstellungen \| Allgemein muss das Konto eingetragen sein, auf das die Lastschriften gutgeschrieben werden sollen. Weiterhin muss die Gläubiger-ID eingetragen werden. Gläubiger-ID können unter [https://extranet.bundesbank.de/scp/](https://extranet.bundesbank.de/scp/) oder [http://www.oenb.at/idakilz/cid?lang=de](http://www.oenb.at/idakilz/cid?lang=de) beantragt werden. Zu Testzwecken kann DE98ZZZ09999999999 eingesetzt werden.

Das Konto für die Gutschriften muss auch in der Buchführung eingerichtet sein. Unter "Nr" ist entweder die komplette IBAN einzutragen oder die Kontonummer ohne führende Nullen.

## SEPA-Fehler

Vor einer Abrechnung sollte die SEPA-Fehlerliste überprüft werden. In der Liste werden Mitglieder mit fehlenden oder ungültigen Bankverbindungen sowie Mandate angezeigt, die seit mehr als 36 Monaten nicht mehr genutzt wurden.

![](/assets/SEPAFehler.png)

## Abrechnung

Die Abrechnung wird mit dem untenstehenden Bildschirm initiiert. Es können

* Mitgliedsbeiträge je nach Beitragsmodell
* Beiträge für im laufenden Jahr eingetretene Mitglieder
* Zusatzbeträge
* Kursgebühren

verarbeitet werden.

![](/assets/Abrechnung.png)

Sofern als Modus nicht 'keine Beitragsabrechnung' ausgewählt wurde, werden für alle Mitglieder, die nicht ausgetreten sind oder deren Austrittsdatum nach dem Stichtag liegt, die Beiträge gemäß eingetragener Beitragsgruppe und Zahlungsrhytmus eingezogen.

Für Mitglieder, die im Laufe des Jahres eingetreten sind, können ebenfalls die Beiträge eingezogen werden. Dazu wird das Eingabedatum eingetragen, ab dem die Beiträge für nachträglich eingetretene Mitglieder abgebucht werden sollen.

Die Abrechnungsdaten werden in das Mitgliedskonto geschrieben.

### Parameter

#### Abrechnungsmodus {#abrechnungsmodus}

##### keine Beitragsabrechnung

Es werden keine Beiträge abgerechnet. Dieser Parameter ist zu setzen, wenn ausschließlich Kursteilnehmer oder Zusatzbeträge abgerechnet werden sollen.

##### Alle

Es werden alle Mitglieder entsprechend des eingestellten [Beitragsmodelle](/beitragsmodelle.md) abgerechnet. Es werden alle Mitglieder abgerechnet, die zum Stichtag bereits eingetreten sind und die zum Stichtag noch nicht ausgetreten sind. Dabei werden [Beitragsgruppen](/beitragsgruppen.md) und Zahlungsrhythmus sowie ggfls. individuelle Beiträge berücksichtigt.

##### Eingetretene Mitglieder

Es werden die neu eingetretenen Mitglieder abgerechnet. JVerein verwendet das Eingabedatum zur Selektion der eingetretenen Mitglieder.

Tipp zum Workflow: Zuerst noch neue Mitglieder anlegen. Danach die Abrechnung machen und dabei als Datum für Von Eingabedatum den Tag nach der letzten Abrechnung für eingetretene Miglieder \(ersatzweise den Tag nach der letzten Abrechnung für Alle\) verwenden. Nach der Abrechnung am selben Tag keine neuen Mitglieder mehr erfassen, die würden bei diesem Workflow sonst nicht mehr abgerechnet.

Hinweis: Das Eingabedatum wird beim Import von Mitgliedern nicht gesetzt.

##### Fälligkeit SEPA \(Erst-/Einzel-Lastschrift\)

Die Fälligkeit von Erst- bzw. Einzel-Lastschriften muss mindestens 5 Bankarbeitstage[ ](/bankarbeitstage.md)nach Einreichung liegen. JVerein macht ausgehend vom aktuellen Datum einen Vorschlag mit dem frühestmöglichen Datum. Das Datum kann überschrieben werden. Es wird 1:1 in die SEPA-Datei eingetragen. Weitere Auswirkung auf die Abrechnung hat das Datum nicht.

##### Fälligkeit SEPA \(Folge-/Letzte-Lastschrift\)

Analog zum Fälligkeitsdatum für Erst-/Einzellastschriften mit 2 Bankarbeitstagen.

##### Stichtag

Stichtag für die Berechnung der Mitgliedschaft und der Fälligkeit von Zusatzbeträgen.

##### Zahlungsgrund für Beiträge

Hier kann ein Text erfasst werden \(z.B. ''Jahresbeitrag 2015''\). Dieser Text wird auf [Rechnungen](/rechnungen.md), [Mahnungen](/mahnungen.md) und bei Lastschriften im Verwendungszweck \(hier zwischen der Bezeichnung der [Beitragsgruppen](/beitragsgruppen.md) und dem Betrag\) ausgegeben.

Der Text sollte aussagekräftig und knapp gewählt werden da er sonst evtl. abgeschnitten wird \(Länge des Verwendungszwecks bei Lastschriften max. 140 Zeichen für alles, einschließlich ggf. [Zusatzbeträge](/zusatzbetrage.md)\).

##### Zusatzbeträge

Mit dieser Option werden die [Zusatzbeträge](/zusatzbetrage.md) abgerechnet. Diese Option kann zu allen \[\[Abrechnung\#Abrechnungsmodus\|Abrechnungsmodi\]\] zusätzlich gesetzt werden.

##### Kursteilnehmer

Teilnehmer von Kursen können abgerechnet werden. Kursteilnehmer sind Personen, die nicht Mitglieder des Vereins sind. Sofern Mitglieder an Kursen teilnehmen, die zusätzlich abgerechnet werden, bieten sich die [/zusatzbetrage.md](/zusatzbetrage.md) an.

##### Kompakte Abbuchung

Alle Abbuchungen eines Mitgliedes \(Beträge und Zusatzbeträge\) werden in eine Abbuchung zusammengefasst.

##### SEPA-Datei drucken

Optional können die SEPA-Daten in zwei PDF-Dokumente \(FRST \(Erste\) + RCUR \(Folgelastschrift\)\) zum Ausdruck ausgegeben werden.

Für die Lastschrift werden die Daten entweder in eine SEPA-XML-Datei geschrieben oder direkt zu Hibiscus ausgegeben. Die IBAN in den Stammdaten \(siehe \[\[Einstellungen\]\]\), alternativ der Kontonummernanteil der IBAN wird mit den Kontonummern in Hibiscus abgeglichen. Gibt es eine übereinstimmende Bankverbindung, wird diese verwendet. Ansonsten erscheint der Hibiscus-Konto-Auswahldialog.

### Weitere Informationen

Verwandte Themen: [Abrechnungslauf](/abrechnungslauf.md), [Pre-Notification, ](/pre-notification.md)[Rücklastschrift](/rucklastschrift.md), [Rechnungen, ](/rechnungen.md)[Mitgliedskonto](/mitgliedskonto.md)

[https://de.wikipedia.org/wiki/Bankarbeitstag](https://de.wikipedia.org/wiki/Bankarbeitstag)

