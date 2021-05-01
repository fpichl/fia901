# Wissenssammlung der FIA901
Ziel dieses Repos ist es, zu sämtlichen für die Ausbildung relevanten Bereiche Informationen zu sammeln.

Das Grundprinzip: Die [.rst-Dateien](https://de.wikipedia.org/wiki/ReStructuredText), die sich in source befinden, werden durch [Sphinx](https://www.sphinx-doc.org/) in HTML umgewandelt. Diese können dann mit einem Apache Webserver unter [fia901.ddns.net](http://fia901.ddns.net/) bereitgestellt werden. Bei Fragen dazu gerne auf mich zukommen.

## Ansehen der Sammlung
Wenn du die Sammlung einfach nur anschauen möchtest, besuche [fia901.ddns.net](http://fia901.ddns.net/). Unter [fia901.ddns.net/Wissenssammlung.pdf](http://fia901.ddns.net/Wissenssammlung.pdf) kanst du dir alles auch als ein großes Dokument herunterladen.

## Wünsche, Anregungen & Verbesserungen
Wenn du irgendwelche Anmerkungen hast, eröffne einfach ein Issue!

## Selber Beitragen
Wenn du auch beisteuern möchtest (danke!), dann wird dir die unten stehende Anleitung helfen. Man selber merkt sich den Stoff natürlich auch einfacher, wenn man ihn nochmal runtergeschrieben hat ;)

### Git
Wenn du [git](https://git-scm.com/downloads) installiert hast, kannst du mit ``git clone https://github.com/pichlerer/fia901.git`` ganz einfach das Repo herunterladen.
Falls du eine auffrischung zu Git brauchst kannst du einfach in der bestehenden Wissensammlung nachschauen.
Änderungen bitte als Pull Request formulieren. Wenn du dabei Schwierigkeiten hast, gib gerne Bescheid!

### .rst Dateien
In .rst Dateien wird mit Markdown Syntax und speziellen Befehlen das Aussehen und der Inhalt der generierten Dokumente festgelegt. Die ausführliche Dokumentation findet sich [auf der Sphinx Website](https://www.sphinx-doc.org/en/master/usage/restructuredtext/basics.html), weiter unten findest du aber einen kurzen Abriss. Wenn du keine Lust hast Sphinx aufzusetzen empfielt sich [dieses nützliche Tool](https://livesphinx.herokuapp.com/) um die Syntax zu prüfen.

- Normaler Text kann einfach runtergeschrieben werden
- Zwischen Zwei Absätzen muss eine Leerzeile gelassen werden. Generell gilt dies auch für andere Befehle: Immer auf Leerzeilen bzw. Leerzeichen und Einrückung achten!
- Überschriften müssen "unterstrichen" werden
  - ```
    ========================
    Ich bin eine Überschrift
    ========================
    ```
  - ```
    Ich bin eine kleinere Überschrift
    =================================
    ```
  - ```
    Ich bin noch kleiner
    --------------------
    ```
    Möchte man noch kleinere Überschriften, kann man [hier](https://docutils.sourceforge.io/docs/ref/rst/restructuredtext.html#sections) nachschauen
- Besonderer Text wird mit Sternchen und Backticks gekennzeichnet
  - ``*Ich bin kursiv*``
  - ``**Ich bin fett**``
  - ``` ``Ich bin ein codeschnipsel`` ```
- Listen werden durch Sternchen oder Zahlen gekennzeichnet. Bei untergeordneten Listen auf die Leerzeile achten!
  - ```
    * Ich bin der erste Eintrag einer Liste
    * Ich bin der zweite Eintrag

      1. Ich bin eine Unterliste und habe Zahlen vorne stehen!
      2. Ich bin der zweite Eintrag. Achte auf die Leerzeile zu der "Elternliste"!
    ```
- Sphinx unterstützt auch ganze Code-Blöcke mit Syntax-Highlighting.
  - ```
    .. code-block:: java
    
      for (int i = 0; i > 10; i++){
          System.out.println("Leerzeile beachten!");
      }
    ```
- Bilder bitte in ``images`` ablegen. Eingebunden werden sie so:
  - ```
    .. image:: images/MeinBild.png
      :width: 400
    ```
