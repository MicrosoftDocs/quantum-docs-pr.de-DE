# <a name="articles"></a>Artikel

In diesem Verzeichnis finden Sie die Artikel für die Dokumentation des quantumentwicklungskit. Dieses Verzeichnis enthält Folgendes:

- **Artikelverzeichnisse**: enthält die Artikel zu den einzelnen Abschnitten der Dokumentation. In diesen Verzeichnissen finden Sie den folgenden Inhalt:
  
  - Jedes Verzeichnis enthält eine `toc.yml` Datei, um den Inhalt des Verzeichnisses im Hauptinhalts Verzeichnis (Inhaltsverzeichnis, Inhaltsverzeichnis) anzuzeigen.
  - Markdown-Artikel, die die Dokumentation enthalten. Diese Artikel sollten den Richtlinien des [Handbuchs für Microsoft-Dokumentation mitwirk](https://docs.microsoft.com/en-us/contribute/)Ende entsprechen.
  - Artikel Unterverzeichnisse. Diese Unterverzeichnisse sollten auch Ihre eigene Datei enthalten `toc.yml` .

> :p-Daten: Obwohl es möglich ist, die `*.md` Dateien direkt in der übergeordneten `TOC.yml` Datei zu verweisen, werden Sie nur aus dem Ihres aktuellen Verzeichnisses bezogen, um die Bestellung zu erhalten `toc.yml` .

- **Hauptinhalts Verzeichnis (Inhaltsverzeichnis): `TOC.yml` **in dieser Datei werden die Abschnitte des Website-Inhaltsverzeichnisses und der Verweis auf die Haupt `toc.yml` Datei des Verzeichnisses jedes Abschnitts aufgeführt.
- **`index.yml`** YAML mit der Konfiguration der Landing Page der Dokumentation.
- **`\media`**: Ein Verzeichnis, in dem alle in der Dokumentation verwendeten Images gespeichert werden. Sie enthält ein `\media\src` Unterverzeichnis zum Speichern der Quelldateien der Bilder.
- **Lizenzdateien**: Dateien mit rechtlichen Lizenzen
- **Technische Dateien**: Dateien mit Makros und Metadaten.

## <a name="guidelines"></a>Richtlinien

Einige allgemeine Richtlinien zur Organisation dieses Verzeichnisses für Mitwirkende:

- Jedes Verzeichnis oder Unterverzeichnis sollte eine eigene Datei enthalten `toc.yml` , in der die Artikel auf derselben Ebene oder die Dateien der untergeordneten Verzeichnisse referenziert werden `toc.yml` .
- Die Organisation der Verzeichnisse des Repository sollte so nah wie möglich an der Organisation des Inhaltsverzeichnisses der Dokumentations Website sein.
- Alle Images sollten in `articles\media` und nicht im Artikel Ordner gespeichert werden.
- Die Titel der Artikel, die Namen im Inhaltsverzeichnis und die *UID* der Metadaten sollten so nah wie möglich sein und den H1-Header des markdown-Dokuments eindeutig darstellen.

## <a name="adding-images"></a>Hinzufügen von Bildern

Damit die Bilder ordnungsgemäß im Dunkel Modus gerendert werden, müssen Sie Transparenz vermeiden.
- Für `*.jpg` Dateien müssen Sie nichts tun, da das Dateiformat keine transparenten Elemente unterstützt.
- Für `*.png` Dateien müssen Sie einen weißen Hintergrund hinzufügen oder den Wert des Alphakanals in 100 ändern. Die einfachste Möglichkeit, dies in Windows zu erreichen, besteht darin, die Datei in Paint und Save zu öffnen und die ursprüngliche Datei zu überschreiben.
- Für `*.svg` Dateien müssen Sie ein weißes Rechteck in der untersten Ebene hinzufügen. Dies kann mit Inkscape durchzuführen sein:
  - Öffnen Sie die Datei `*.svg` .
  - Wählen Sie das Tool Square Maker aus, und zeichnen Sie ein weißes Rechteck oberhalb der ursprünglichen Abbildung.
  - Wählen Sie das Tool "SELECT-und Transform Objects" aus, indem Sie auf den dunklen Pfeil klicken oder F1 drücken.
  - Wenn Sie das Rechteck ausgewählt haben, klicken Sie auf das Symbolleisten Element "untere Auswahl nach unten (Ende)".
  - Passen Sie das Rechteck mit der Maus oder den Pfeiltasten an.
