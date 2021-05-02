ich teste
# Wissenssammlung der FIA901
Ziel dieses Repos ist es, zu sämtlichen für die Ausbildung relevanten Bereiche Informationen zu sammeln. 

Das Grundprinzip: Die [.rst-Dateien](https://de.wikipedia.org/wiki/ReStructuredText), die sich in source befinden, werden durch [Sphinx](https://www.sphinx-doc.org/) in HTML umgewandelt. Diese können dann mit einem Apache Webserver unter [fia901.ddns.net](http://fia901.ddns.net/) bereitgestellt werden. Bei Fragen dazu gerne auf mich zukommen.

## Ansehen der Sammlung
 - Wenn du die Sammlung einfach nur anschauen möchtest, besuche [fia901.ddns.net](http://fia901.ddns.net/).
 - Unter [fia901.ddns.net/Wissenssammlung.pdf](http://fia901.ddns.net/Wissenssammlung.pdf) kanst du dir alles auch als pdf herunterladen. (Achtung: Hübsch sieht die nicht aus!)
 - Unter [fia901.ddns.net/Wissenssammlung.html](http://fia901.ddns.net/Wissenssammlung.html) kannst du dir alles als ein einziges html Dokument anschauen. Das ist etwas unübersichtlicher, aber lässt sich auch mit ``strg+s`` wegspeichern

## Wünsche, Anregungen & Verbesserungen
Wenn du irgendwelche Anmerkungen hast, eröffne einfach ein Issue oder gib mir so Bescheid!

## Selber Beitragen
Wenn du auch beisteuern möchtest (danke!), dann wird dir die unten stehende Anleitung helfen. Man selber merkt sich den Stoff natürlich auch einfacher, wenn man ihn nochmal runtergeschrieben hat ;)

### Git
Wenn du [git](https://git-scm.com/downloads) installiert hast, kannst du mit ``git clone https://github.com/pichlerer/fia901.git`` ganz einfach das Repo herunterladen.
Falls du eine auffrischung zu Git brauchst kannst du einfach in der bestehenden Wissensammlung nachschauen.
Änderungen bitte als Pull Request formulieren. Wenn du dabei Schwierigkeiten hast, gib gerne Bescheid!

### .rst Dateien in /source
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
### Selber Sphinx installieren
Um hier beitragen zu können brauchst du Sphinx nicht selber installieren. Nutze einfach [diesen Online-Editor](https://livesphinx.herokuapp.com/). Wenn du es aber schöner findets mit dem richtigen Programm zu arbeiten, oder wenn dieses Projekt dein Interesse an Sphinx geweckt hat, dann solltest du folgenden Schritten folgen:
- Installiere [python](https://www.python.org/downloads/). Wenn du nicht die neueste Version benutzen möchtest, die pip bereits dazu installiert, dann [installiere auch pip](https://www.liquidweb.com/kb/install-pip-windows/). Pip ist ein paketmanager der es erlaubt, zusätzliche python libraries zu installieren
- Installiere sphinx über die Powershell mit ``pip install sphinx`` bzw. mit ``pip3 install sphinx``
- Installiere das Read The Docs Theme mit ``pip install spinx_rtd_theme`` bzw. ``pip3 install spinx_rtd_theme``. Das ändert das Aussehen des generierten Dokumentes, wenn so in der ``source/config.py`` konfiguriert.
- Wenn du ein neues Projekt erstellen möchtest ist es das einfachste, in einem leeren Ordner ``sphinx-quickstart`` auszuführen
- Wenn du ein Projekt "bauen", also ein fertiges Dokument generieren möchtest, führe einfach ``make.bat <Dokumenttyp>`` aus. Es stehen [viele Dokumenttypen](https://www.sphinx-doc.org/en/master/man/sphinx-build.html) zu Auswahl, die wichtigsten sind ``html`` und ``pdf``.
