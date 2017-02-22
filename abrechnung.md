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

#### Abrechnungsmodus

##### keine Beitragsabrechnung

Es werden keine Beiträge abgerechnet. Dieser Parameter ist zu setzen, wenn ausschließlich Kursteilnehmer oder Zusatzbeträge abgerechnet werden sollen.

##### Alle

Es werden alle Mitglieder entsprechend des eingestellten [/beitragsmodelle.md](/beitragsmodelle.md "Beitragsmodell") abgerechnet. Es werden alle Mitglieder abgerechnet, die zum Stichtag bereits eingetreten sind und die zum Stichtag noch nicht ausgetreten sind. Dabei werden [/beitragsgruppen.md](/beitragsgruppen.md) und Zahlungsrhythmus sowie ggfls. individuelle Beiträge berücksichtigt.

##### Eingetretene Mitglieder

Es werden die neu eingetretenen Mitglieder abgerechnet. JVerein verwendet das Eingabedatum zur Selektion der eingetretenen Mitglieder.

Tipp zum Workflow: Zuerst noch neue Mitglieder anlegen. Danach die Abrechnung machen und dabei als Datum für Von Eingabedatum den Tag nach der letzten Abrechnung für eingetretene Miglieder \(ersatzweise den Tag nach der letzten Abrechnung für Alle\) verwenden. Nach der Abrechnung am selben Tag keine neuen Mitglieder mehr erfassen, die würden bei diesem Workflow sonst nicht mehr abgerechnet.

Hinweis: Das Eingabedatum wird beim Import von Mitgliedern nicht gesetzt.

##### Fälligkeit SEPA \(Erst-/Einzel-Lastschrift\)

Die Fälligkeit von Erst- bzw. Einzel-Lastschriften muss mindestens 5 [/bankarbeitstage.md](/bankarbeitstage.md) nach Einreichung liegen. JVerein macht ausgehend vom aktuellen Datum einen Vorschlag mit dem frühestmöglichen Datum. Das Datum kann überschrieben werden. Es wird 1:1 in die SEPA-Datei eingetragen. Weitere Auswirkung auf die Abrechnung hat das Datum nicht.

