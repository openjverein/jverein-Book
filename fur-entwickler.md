# Für Entwickler

## Video: Entwicklungsumgebung installieren

[https://youtu.be/xhPIkeO4jco](https://youtu.be/xhPIkeO4jco)

## Video: Projekte aktualisieren und Patches erstellen

[https://youtu.be/UFDvKRNLGk8](https://youtu.be/UFDvKRNLGk8)

## Sortierung von Tabellen verhindern

Standardmäßig können Tabellen durch einen Klick in den Header einer Spalte sortiert werden. In einigen Situationen ist das nicht erwünscht. Mit folgendem Code kann das verhindert werden:

```
xxxList = new TablePart(gi, null)
{
  @Override
  protected void orderBy(int index)
  {
    return;
  }
};
```



