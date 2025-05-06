Hallo! Klar, hier ist eine mkdocs_formatting_examples.md-Datei, die du als Referenz für deine MkDocs-Seite mit dem Material-Theme verwenden kannst. Sie enthält Beispiele für verschiedene Formatierungsmöglichkeiten, einschließlich Info- und Warnkästen (Admonitions), Codeblöcke, Tabellen, Listen und mehr.

Markdown


# MkDocs Material Formatierungsbeispiele

Willkommen zu dieser Übersicht verschiedener Formatierungsmöglichkeiten, die mit MkDocs und dem Material-Theme verfügbar sind.

## Admonitions (Hinweis-Kästen)

Admonitions sind eine großartige Möglichkeit, um bestimmte Textabschnitte hervorzuheben.

Die grundlegende Syntax ist:
```markdown
!!! type "Optionaler Titel"
    Inhalt des Hinweises hier.
    Dieser kann sich über mehrere Zeilen erstrecken.


Es gibt viele vordefinierte Typen. Hier sind einige gängige Beispiele:
Note / Seealso

Markdown


!!! note
    Dies ist ein Hinweis. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nulla et euismod nulla.



Markdown


!!! seealso "Siehe auch"
    Dieser Kasten verweist auf verwandte Informationen.


Abstract / Summary / Todo

Markdown


!!! abstract "Zusammenfassung"
    Eine kurze Zusammenfassung des Inhalts.



Markdown


!!! summary
    Eine weitere Möglichkeit für eine Zusammenfassung.



Markdown


!!! todo
    - [ ] Eine zu erledigende Aufgabe
    - [x] Eine bereits erledigte Aufgabe


Info / Tip / Hint / Important

Markdown


!!! info
    Eine Informationsbox für neutrale Hinweise.



Markdown


!!! tip "Profi-Tipp"
    Ein nützlicher Tipp für den Leser.



Markdown


!!! hint
    Ein kleiner Hinweis.



Markdown


!!! important
    Wichtige Information, die beachtet werden sollte.


Success / Check / Done

Markdown


!!! success "Erfolg!"
    Diese Aktion wurde erfolgreich abgeschlossen.



Markdown


!!! check
    Ein weiterer Kasten für erfolgreiche Operationen.



Markdown


!!! done
    Zeigt an, dass etwas erledigt ist.


Warning / Caution / Attention

Markdown


!!! warning
    Achtung! Hier ist Vorsicht geboten.



Markdown


!!! caution "Vorsicht"
    Eine explizite Warnung vor möglichen Problemen.



Markdown


!!! attention
    Fordert die Aufmerksamkeit des Lesers.


Failure / Fail / Missing / Error

Markdown


!!! failure
    Etwas ist fehlgeschlagen.



Markdown


!!! fail "Fehlgeschlagen"
    Zeigt einen Fehler an.



Markdown


!!! missing
    Informationen oder Schritte fehlen.



Markdown


!!! error "Fehler"
    Ein kritischer Fehler ist aufgetreten.


Danger / Bug

Markdown


!!! danger "Gefahr!"
    Dies ist eine sehr wichtige Warnung vor kritischen Gefahren.



Markdown


!!! bug "Fehler gemeldet"
    Hier könnte ein bekannter Fehler beschrieben werden.


Example / Snippet

Markdown


!!! example
    Ein Beispiel zur Illustration.
    ```python
    print("Hallo Welt im Beispiel!")
    ```



Markdown


!!! snippet
    Ein Code-Snippet oder eine kleine Demonstration.


Quote / Cite

Markdown


!!! quote
    "Das ist ein Zitat."
    <cite>Max Mustermann</cite>



Markdown


!!! cite
    Noch ein Zitat, etwas anders dargestellt.


Einklappbare Admonitions
Man kann Admonitions auch einklappbar machen, indem man ??? anstelle von !!! verwendet. Mit ???+ ist der Kasten standardmäßig ausgeklappt.

Markdown


??? note "Einklappbarer Hinweis (standardmäßig zu)"
    Dieser Inhalt ist anfangs verborgen.

???+ warning "Einklappbare Warnung (standardmäßig offen)"
    Dieser Inhalt ist anfangs sichtbar, kann aber eingeklappt werden.


Codeblöcke
Codeblöcke sind essentiell für technische Dokumentationen.
Einfacher Codeblock

Markdown


```python
# Ein einfacher Python-Codeblock
def greet(name):
  print(f"Hallo, {name}!")

greet("MkDocs Benutzer")





### Codeblock mit Zeilennummern
Man kann Zeilennummern hinzufügen, indem man `linenums="1"` (oder eine andere Startzahl) angibt.
```markdown
```python linenums="1"
# Python-Code mit Zeilennummern
import os

def list_files(path):
  return os.listdir(path)

print(list_files("."))





### Hervorheben von Zeilen
Einzelne Zeilen oder Bereiche können hervorgehoben werden.
```markdown
```python hl_lines="3 5-6"
# Python-Code mit hervorgehobenen Zeilen
def calculate_sum(a, b):
  # Diese Zeile wird hervorgehoben
  result = a + b
  # Die folgenden zwei Zeilen werden hervorgehoben
  print(f"Die Summe ist: {result}")
  return result

calculate_sum(10, 5)





### Inline Code
Man kann auch `Inline-Code` mit Backticks (`) einfügen.
Um Inline-Code mit Syntaxhervorhebung darzustellen (erfordert die `InlineHilite` Erweiterung):
`#!python print("Hallo")`

## Tabellen

Tabellen können mit Markdown-Syntax erstellt werden.

```markdown
| Überschrift 1 | Überschrift 2 | Überschrift 3 (Rechtsbündig) |
|---------------|:-------------:|-----------------------------:|
| Zelle 1       | Zelle 2       | Zelle 3                      |
| Inhalt A      | Inhalt B      | Inhalt C                     |
| *Markdown* | `Code`        | **Fett** |


Das ergibt:
Überschrift 1
Überschrift 2
Überschrift 3 (Rechtsbündig)
Zelle 1
Zelle 2
Zelle 3
Inhalt A
Inhalt B
Inhalt C
Markdown
Code
Fett

Listen
Ungeordnete Listen

Markdown


* Ein Eintrag
* Noch ein Eintrag
  * Ein Untereintrag
  * Noch ein Untereintrag
+ Ein anderer Listentyp-Marker
- Und noch einer


Ein Eintrag
Noch ein Eintrag
Ein Untereintrag
Noch ein Untereintrag
<!-- end list -->
Ein anderer Listentyp-Marker
<!-- end list -->
Und noch einer
Geordnete Listen

Markdown


1. Erster Punkt
2. Zweiter Punkt
   1. Unterpunkt 2.1
   2. Unterpunkt 2.2
3. Dritter Punkt


Erster Punkt
Zweiter Punkt
Unterpunkt 2.1
Unterpunkt 2.2
Dritter Punkt
Aufgabenlisten (Task Lists)
(Erfordert die pymdownx.tasklist Erweiterung in mkdocs.yml)

Markdown


* [x] Aufgabe 1 erledigt
* [ ] Aufgabe 2 offen
* [ ] Aufgabe 3
  * [ ] Unteraufgabe 3.1
  * [x] Unteraufgabe 3.2 erledigt


[x] Aufgabe 1 erledigt
[ ] Aufgabe 2 offen
[ ] Aufgabe 3
[ ] Unteraufgabe 3.1
[x] Unteraufgabe 3.2 erledigt
Definitionslisten
(Erfordert die def_list Erweiterung in mkdocs.yml)

Markdown


Begriff 1
:   Definition von Begriff 1. Lorem ipsum dolor sit amet, consectetur adipiscing elit.

Begriff 2 mit *Markdown*
:   Definition von Begriff 2.
    Kann auch mehrere Absätze haben.


Begriff 1
: Definition von Begriff 1. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
Begriff 2 mit Markdown
: Definition von Begriff 2.
Kann auch mehrere Absätze haben.
Blockquotes (Zitatblöcke)

Markdown


> Dies ist ein Zitatblock.
> Er kann sich über mehrere Zeilen erstrecken.
>
> > Man kann Zitatblöcke auch verschachteln.
>
> #### Zitate können auch Markdown enthalten
> * Wie Listen
> * Oder **fettgedruckten Text**


Dies ist ein Zitatblock.
Er kann sich über mehrere Zeilen erstrecken.
Man kann Zitatblöcke auch verschachteln.
Zitate können auch Markdown enthalten
Wie Listen
Oder fettgedruckten Text
Bilder
Bilder können einfach eingebettet werden.

Markdown


![Alternativtext für das Bild](https://via.placeholder.com/300x150/007BFF/FFFFFF?text=Beispielbild)


Bilder mit Titeln und Ausrichtung
(Erfordert die attr_list Erweiterung für Ausrichtung und pymdownx.blocks.caption für Bildunterschriften)

Markdown


![Ein Bild mit Bildunterschrift](https://via.placeholder.com/200x100/28A745/FFFFFF?text=Grünes+Bild){ align=left }
*Das ist eine Bildunterschrift für das links ausgerichtete Bild.*


{ align=left }
Das ist eine Bildunterschrift für das links ausgerichtete Bild.

Markdown


![Ein rechts ausgerichtetes Bild](https://via.placeholder.com/200x100/FFC107/000000?text=Gelbes+Bild){ align=right }

Und hier ist etwas Text, der um das rechts ausgerichtete Bild fließt. Lorem ipsum dolor sit amet, consectetur adipiscing elit.


{ align=right }
Und hier ist etwas Text, der um das rechts ausgerichtete Bild fließt. Lorem ipsum dolor sit amet, consectetur adipiscing elit.
<br clear="all" /> ### Lightbox für Bilder
Wenn du das glightbox Plugin installiert und in mkdocs.yml konfiguriert hast:



plugins:
  - glightbox


Dann werden Bilder standardmäßig in einer Lightbox geöffnet, wenn man darauf klickt.

Markdown


[![Bild das in Lightbox öffnet](https://via.placeholder.com/150)](https://via.placeholder.com/600x400/DC3545/FFFFFF?text=Großes+Bild+in+Lightbox)



Links
Standard-Links

Markdown


[Ein Link zu Google](https://www.google.com)
[Ein relativer Link zu einer anderen Seite](eine-andere-seite.md)


Ein Link zu Google
Ein relativer Link zu einer anderen Seite
Links mit Titeln

Markdown


[Link mit Titel](https://www.mkdocs.org "Besuche die MkDocs Webseite")


Link mit Titel
Anker-Links (Innerhalb der Seite)

Markdown


[Gehe zum Abschnitt über Admonitions](#admonitions-hinweis-kasten)


Gehe zum Abschnitt über Admonitions
(Hinweis: Die ID für den Anker wird automatisch aus der Überschrift generiert.)
Textformatierung
Fett und Kursiv

Markdown


**Dieser Text ist fett.**
*Dieser Text ist kursiv.*
***Dieser Text ist fett und kursiv.***
~~Dieser Text ist durchgestrichen.~~


Dieser Text ist fett.
Dieser Text ist kursiv.
Dieser Text ist fett und kursiv.
~~Dieser Text ist durchgestrichen.~~
Hervorhebungen (Highlighting)
(Erfordert pymdownx.mark)

Markdown


Man kann Text auch ==hervorheben==.


Man kann Text auch ==hervorheben==.
Tastaturkürzel
(Erfordert pymdownx.keys)

Markdown


Drücke ++ctrl+alt+del++ um den Task-Manager zu öffnen.
Oder einfach ++enter++.


Drücke ++ctrl+alt+del++ um den Task-Manager zu öffnen.
Oder einfach ++enter++.
Horizontale Linien

Markdown


---
***
___


Fußnoten

Markdown


Hier ist ein Text mit einer Fußnote.[^1] Und hier ist eine weitere.[^longnote]

[^1]: Dies ist die erste Fußnote.
[^longnote]: Dies ist eine längere Fußnote, die
    mehrere Zeilen umfassen kann.


Hier ist ein Text mit einer Fußnote.[^1] Und hier ist eine weitere.[^2]
Emojis
(Erfordert pymdownx.emoji)
Konfiguriere in mkdocs.yml:

YAML


markdown_extensions:
  - pymdownx.emoji:
      emoji_index: !!python/name:material.extensions.emoji.twemoji
      emoji_generator: !!python/name:material.extensions.emoji.to_svg



Markdown


Einige Emojis: :smile: :tada: :rocket: :warning:


Einige Emojis: :smile: :tada: :rocket: :warning:
Inhalt-Tabs (Content Tabs)
(Erfordert pymdownx.tabbed und pymdownx.superfences in mkdocs.yml)

Code-Snippet


=== "Tab 1: Python"
    ```python
    print("Hallo von Tab 1")
    ```

=== "Tab 2: JavaScript"
    ```javascript
    console.log("Hallo von Tab 2");
    ```

=== "Tab 3: Gemischter Inhalt"
    Das ist normaler Text in einem Tab.
    * Mit einer Liste
    * Und noch einem Punkt.


=== "Tab 1: Python"
python print("Hallo von Tab 1")
=== "Tab 2: JavaScript"
javascript console.log("Hallo von Tab 2");
=== "Tab 3: Gemischter Inhalt"
Das ist normaler Text in einem Tab.
* Mit einer Liste
* Und noch einem Punkt.
Das waren einige der wichtigsten Formatierungsmöglichkeiten. Für detailliertere Informationen und weitere Optionen, schaue bitte in die offizielle Dokumentation von Material for MkDocs.




**Wichtige Hinweise zu dieser Datei:**

1.  **Speichern:** Speichere diesen Inhalt in einer Datei mit der Endung `.md` (z.B. `formatierungsbeispiele.md`) in deinem `docs`-Verzeichnis deines MkDocs-Projekts.
2.  **`mkdocs.yml` Konfiguration:**
    * Viele der fortgeschrittenen Formatierungen (wie spezielle Admonition-Typen, Aufgabenlisten, Definitionslisten, Bildunterschriften, Code-Hervorhebungen, Emojis, Inhalt-Tabs, etc.) erfordern spezifische Python Markdown-Erweiterungen.
    * Stelle sicher, dass du die notwendigen Erweiterungen in deiner `mkdocs.yml`-Datei im `markdown_extensions`-Abschnitt aktiviert hast. Eine typische Konfiguration für viele der hier gezeigten Beispiele könnte so aussehen:

    ```yaml
    theme:
      name: material
      features:
        # einige Features hier, z.B.
        # - navigation.tabs
        # - navigation.sections
        # - content.code.annotate
        # - content.tabs.link

    markdown_extensions:
      - admonition
      - pymdownx.details # Für einklappbare Admonitions (???), obwohl Admonition selbst das auch kann
      - pymdownx.superfences # Für verschachtelte Codeblöcke und andere Dinge
      - pymdownx.highlight:
          anchor_linenums: true
      - pymdownx.inlinehilite
      - pymdownx.snippets
      - tables
      - pymdownx.tasklist:
          custom_checkbox: true # Für schönere Checkboxen
      - def_list
      - attr_list # Für Attribute wie { align=left } bei Bildern
      - md_in_html
      - pymdownx.blocks.caption # Für Bildunterschriften
      - pymdownx.emoji:
          emoji_index: !!python/name:material.extensions.emoji.twemoji
          emoji_generator: !!python/name:material.extensions.emoji.to_svg
      - pymdownx.tabbed:
          alternate_style: true
      - footnotes
      - pymdownx.mark # Für ==hervorheben==
      - pymdownx.keys # Für ++Tasten++
    ```
3.  **Testen:** Baue deine MkDocs-Seite (`mkdocs build`) oder starte den Entwicklungsserver (`mkdocs serve`), um zu sehen, wie diese Formatierungen gerendert werden.

Ich hoffe, diese umfangreiche Beispiel-Datei hilft dir beim Erstellen deiner MkDocs Material Seite!


[^1]:
Dies ist die erste Fußnote.
[^2]:
Dies ist eine längere Fußnote, die
mehrere Zeilen umfassen kann.
Quellen
1. https://github.com/adrienbrignon/mkdocs-exporter/issues/13
2. https://github.com/google/yggdrasil-decision-forests
3. https://github.com/BaryshevRS/angular-docs
