# Buchführung Grundsätze

Bei der JVerein-Buchführung handelt es sich um eine einfache Einnahme-Überschuss-Rechnung. Dabei werden alle Zahlungsvorgänge in eine Tabelle nach folgendem Muster eingetragen:

```
+---------+--------------------+------------------------+--------+
| Bu-Nr.  | Name               | Verwendungszweck       |Betrag  |
+---------+--------------------+------------------------+--------+
|       1 | Meier, Fritz       | Mitgliedsbeitrag       |  50,00 |
+---------+--------------------+------------------------+--------+
|       2 | Müller & Co.       | Getränke f. Versamml.  | 123,45 |
+---------+--------------------+------------------------+--------+
```

Die Informationen aus den Kontoauszügen der Banken können im idealen Fall aus Hibiscus übernommen werden. Für Barkassen oder wenn Hibiscus nicht genutzt wird, können alle Buchungen manuell erfasst werden.

Jeder Buchung wird eine Buchungsart zugeordnet. Damit kann nachgewiesen werden, für welche Zwecke Geld eingenommen und ausgegeben wurde:

```
+---------+--------------------+------------------------+--------+--------------+
| Bu-Nr.  | Name               | Verwendungszweck       |Betrag  | Buchungsart  |
+---------+--------------------+------------------------+--------+--------------+
|       1 | Meier, Fritz       | Mitgliedsbeitrag       |  50,00 |     1035     |
+---------+--------------------+------------------------+--------+--------------+
|       2 | Müller & Co.       | Getränke f. Versamml.  | 123,45 |     2080     |
+---------+--------------------+------------------------+--------+--------------+
```

Zur Abbildung von idiellem und wirtschaftlichem Betrieb können mit Hilfe von Buchungsklassen Buchungsarten zusammengefasst werden.

Jede Buchung kann einem Mitgliedskonto zugeordnet werden \(Istbuchung: "Geld ist geflossen"\):

```
+---------+--------------------+------------------------+--------+--------------+--------------+
| Bu-Nr.  | Name               | Verwendungszweck       |Betrag  | Buchungsart  | Mitglieds-Nr.|
+---------+--------------------+------------------------+--------+--------------+--------------|
|       1 | Meier, Fritz       | Mitgliedsbeitrag       |  50,00 |     1035     |         4711 |
+---------+--------------------+------------------------+--------+--------------+--------------+
|       2 | Müller & Co.       | Getränke f. Versamml.  | 123,45 |     2080     |              |
+---------+--------------------+------------------------+--------+--------------+--------------+
```

Durch Sollbuchungen im Mitgliedskonto wird festgelegt, für welche Zwecke das Mitglied etwas zahlen soll \(z. B. Mitgliedsbeitrag\). Sollbuchungen werden für Mitgliedsbeiträge und Zusatzbeträge durch die Abrechnung automatisch erstellt. Sie können auch manuell angelegt werden.

