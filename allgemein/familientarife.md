# Familientarife

## Allgemein

Es gibt Anwendungsfälle in denen in einer Familie die Beiträge für Partner oder Kinder reduziert oder sogar erlassen sind. Dies gilt aber nur solange auch ein voll zahlendes Familienmitglied existiert.

Um diese Beziehung zu modellieren wurde das Familienkonzept eingeführt. In einer Familie muss es ein voll zahlendes Mitglied geben. Der Familie können mehrere Familienmitglieder zugeordnet werden. Die Zuordnung wird in den [Mitgliedsdaten](../allgemeine-funktionen/mitglieder/content/mitgliedschaft.md) konfiguriert.

Bis zur Version 2.8.22 gab es je eine Beitragsgruppe für das voll zahlende Familienmitglied und eine Beitragsgruppe für die Familienmitglieder. Für Familienmitglieder konnte kein Beitrag konfiguriert werden. Sie wurden als beitragsfrei angenommen.

Mit der Version 2.8.23 wurde das Konzept verallgemeinert.

Voll zahlende Familienmitglieder brauchen keine eigene Beitragsgruppe mehr. Man kann jedem Mitglied mit einer normalen Beitragsgruppe ein Familienmitglied zuweisen.

Für Familienmitglieder sind [Beitragsgruppen](../allgemeine-funktionen/administration/mitglieder/beitragsgruppen.md) der Art Familienangehöriger zu definieren. Für diese können jetzt auch Beiträge konfiguriert werden. Also etwa ein niedrigerer Beitrag oder auch kein Beitrag. Die eigene Beitragsgruppe dient dazu, um überprüfen zu können, dass für ein Mitglied mit Familienbeitrag auch ein voll zahlendes Mitglied existiert.

Die Familienmitglieder sind miteinander verknüpft. Tritt das voll zahlende Mitglied aus, erscheint ein entsprechender Hinweis. Dann muss entweder ein bislang Familienmitglied zum Vollzahler erklärt werden oder der Familienverband wird aufgelöst und es werden Einzelbeiträge erhoben.

## Übersicht

In der Übersicht [Familienbeitrag](../allgemeine-funktionen/mitglieder/familienbeitrag.md) werden alle Familienverbände in Form eines Baumes aufgelistet. Es werden jeweils der Zahler mit den Angehörigen dargestellt.

