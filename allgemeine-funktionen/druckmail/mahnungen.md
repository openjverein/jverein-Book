# Mahnungen drucken/mailen

## Allgemeines

Für alle offenen Sollbuchungen können Mahnungen erstellt werden. Dabei hat man die Möglichkeit eine Mahnung selektiv oder automatisch zu erstellen. Eine Buchung ist offen, wenn der Betrag der Spalte Zahlungseingang kleiner ist als der Wert in der Spalte Betrag.

Ein Mahnung kann ein PDF Dokument sein das direkt aus JVerein erstellt wird oder Sie exportieren die Daten in eine CSV Datei und erstellen die Mahnung als Serienbrief mit z.B. Microsoft Office oder Open Office.

## Mahnungen selektiv erstellen

Möchten Sie eine Mahnung selektiv erstellen, so öffnen Sie den Dialog Sollbuchungen. Wählen Sie den Filter so, dass die gewünschten Daten angezeigt werden. Selektieren Sie einen oder mehrere Einträge und drücken die rechte Maustaste. Es öffnet sich ein Kontext-Menü. Wählen Sie hier den Menüpunkt "Mahnung erstellen". Es öffnet sich hier der Dialog Mahnung der Sie bei der Erstellung der Mahnung unterstützt.

Hier lässt sich bei der Ausgabe zwischen Drucken oder Versenden per Mail wählen.

Im Info Feld wird angezeigt wieviele Sollbuchungen selektiert wurden und ob  zugehörige Mitglieder keine Mailadresse haben. Haben sie keine Mail Adresse werden sie beim Versand per Mail ignoriert.

![](../../assets/mitgliedmahnung2.png)

Über die Buttons lässt sich eine gespeicherte Mailvorlage auswählen bzw. die Mahnung exportieren.

Das drücken des Startknopf löst bei korrekt eingestellten E-Mail-Server-Daten den Versand der E-Mails aus. Es ist daher ratsam, diese Funktion im Vorfeld zu testen, ohne mit echten Mitgliederdaten/E-Mails zu hantieren.

## Mahnungen automatisch erstellen

Um automatisch Mahnungen zu erstellen wählen Sie im Navigations Baum dem Menü Eintrag "Mahnungen" aus. Es öffnet sich ebenfalls der Dialog Mahnungen.

Im Gegensatz zum selektiven Erstellen wird hier der gleiche Filter Bereich angezeigt wie im Sollbuchungen Dialog. Es werden dann Mahnungen für alle Sollbuchungen die die Filter Kriterien erfüllen gedruckt bzw. per Mail versendet.

![](../../assets/mitgliedmahnung1.png)

Tip:

Falls Sie Mahnungen per Mail versenden wollen, wählen Sie erst bei Mail die Option "Nur mit Mailadresse" und als Ausgabe MAIL. Damit versenden sie die Mahnung an alle Mitglieder die eine Mail Adresse haben.

Falls nicht alle Mitglieder eine Mail Adresse haben, wählen Sie anschliesend bei Mail die Option "Nur ohne Mailadresse" und die Ausgabe DRUCK. Diese können Sie dann per Post verschicken.

## Mahnungen drucken

Möchten Sie Mahnungen direkt als JVerein druckfertig generieren, so müssen Sie mindestens ein Mahnungsformular angelegt haben. Die Erstellung von Mahnungsformularen ist unter Administration\|Formulare beschrieben.

Wählen Sie in der Auswahlbox Formular dasjenige Formular, mit dem Sie die Mahnungen erstellen möchten und drücken Sie dann den Schalter starten. Es öffnet sich ein Dialog der den Speicherort und den Dateinamen der PDF Datei abfragt, in die alle Mahnungen erstellt werden. Mit Bestätigen dieser Eingaben werden die Mahnungen generiert und die fertige PDF geöffnet. Diese können Sie nun ausdrucken.

## Mahnungsdaten exportieren

Sollen die Mahnungsdaten exportiert werden, so drücken Sie im Dialog Mahnung den Schalter Export. Es öffnet sich ein Dialog der den Speicherort und den Dateinamen der CSV abfragt. Bestätigen Sie diesen Dialog, werden die Mahnungsdaten in diese Dateien exportiert und können danach z.B. für einen Serienbrief verwendet werden.
