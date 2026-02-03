# How to Use

Gehe zur main.tex und stelle die grundlegenden Dokumenteneigenschaften ein. Dies sind meistens Vorgaben von dem jeweiligen Lehrstuhl. 
    Die einzelnen Einstellungen sind in der main.tex Zeile für Zeile kommentiert, sodass man von oben nach unten durchgehen kann und ggf. Änderungen vornehmen kann, um das Dokument an seine Bedingungen anzupassen.
    Hier besonders hervorzuheben ist die Einstellung der Schriftgröße in Zeile 3, die Angabe, wie Referenziert werden soll in den Zeilen 44 - 46 und die Art der Literatur-Referenzierung in Zeile 55 (Hier Standardmäßig IEEE)

Grundsätzlich ist die main.tex sozusagen die Hauptplattform für das Dokument, hier wird dem Programm gesagt was und wie es geladen werden soll. Die eigentliche PDF beginnt also mit dem Kommando in Zeile 75.

Mit dem ```\include{}``` Befehl werden Teile zu dem PDF hinzugefügt, damit die einzelnen Abschnitte des Dokumentes übersichtlich in einzelnen Files bearbeitet werden kann. (Jedes Chapter hat eine eigene .tex File in der dann der eigentliche Inhalt der Arbeit steht).

Standardmäßig ist das Dokument auf ein wissenschaftliches Paper eingestellt, das heißt, dass die Seiten, welche nicht den Inhalt der Arbeit enthalten (Inhaltsverzeichnis, Abkürzungsverzeichnis, etc.) mit romanischen Zahlen gezählt werden und ab der Einleitung, bzw. dem ersten eigentlichen Kapitel, wird dann in arabischen Nummer weitergezählt. (Siehe Zeile 77 und Zeile 109)

Sollten einzelne Inhalte nicht gebraucht werden, können die zugehörigen Zeilen einfach durch ein vorstehendes % Auskommentiert werden.

Der eigentliche Inhalt der Arbeit findet sich in den Chaptern wieder, diese sind extra in dem Unterordner chapters zu finden und die Unterteilung der einzelnen Files ist der Struktur der eigenen Arbeit zu entnehmen.
Dort kann für jedes Kapitel in der Arbeit eine neue Datei mit dem jeweiligen Kapitelnamen angelegt werden.

Jedes Chapter fängt mit dem Kommando ```\chapter{Name des Kapitels}``` an, dadurch weiß LaTeX, dass es sich um ein Kapitel handelt und kann es dementsprechend einfügen.
Unterkapitel werden innerhalb des ```\chapter``` mit ```\section{Name des Unterkapitels}``` angegeben und weitere Einrückungen mit ```\subsection{}```, ```\subsubsection{}``` usw.

Dadruch ergibt sich dann eine Einteilung, die wiefolgt aussieht:

```text

1. Kapitel 1
    1.1 Unterkapitel 1
    1.2 Unterkapitel 2
        1.2.1 Unterunterkapitel 1
        ...
            ...
2. Kapitel 2

```

Alle Grafiken, die in die Arbeit eingebettet werden sollen, befinden sich in dem Unterordner img.
Es empfiehlt sich die Bilder im Vorhinein so zu formatieren, dass das Bild keine Weißen Ränder mehr hat und genau zugeschnitten wurde. So sieht es am Ende in dem PDF am besten aus. Alle gängigen Bildformate sollten unterstützt werden. Wie das Einfügen von Grafiken genau geht sollte im Einzelnen nachgeschlagen werden (LaTeX Dokumentation, oder ChatGPT helfen hier enorm).

Tabellen werden in LaTeX direkt erstellt, es empfiehlt sich dafür einen online LaTeX Tabelleneditor zu verwenden und den Code dann am jeweiligen Punkt einzufügen (https://www.latex-tables.com/). 

Das Literaturverzeichnis befindet sich im Unterordner litrature und beinhaltet genau eine Datei mit dem Namen Literaturverzeichnis.bib.
In dieser Datei befinden sich alle Referenzen in dem BibLaTeX Format.
Um die Referenzen in diesem Format einfach zu erhalten, empfiehlt sich ein Literaturprogramm wie z.B. Zotero oder Citavi, welche die Bibliotheken einfach in diesem Format exportieren können. Dabei ist es nicht relevant, ob in der Datei Referenzen vorkommen, die in der Arbeit nicht verwendet werden, da in dem Literaturverzeichnis nur diese Aufgeführt werden, welche auch in dem Text referenziert wurden.

Weiterführende ein paar der wichtigsten Kommandos in LaTeX und deren Funktion.
1. ```\chapter{Name des Kapitels}``` -> Erstellt ein neues Kapitel
2. ```\section{Name der Unterkapitels}``` -> Erstellt ein neues Unterkapitel
3. ```\subsection{}``` -> Neues Unterunterkapitel
4. ```\label{Name des Labels}``` -> Ordnet ein Label zu, auf das man sich später beziehen kann
z.B.  
```\chapter{Einleitung}```  
```\label(chap\Einleitung)```   
Hier wird ein Label: chap\Einleitung erstellt, so kann man im späteren Verlauf einfach auf dieses Kapitel referenzieren, indem man das Label verwendet.
Label werden für alles erstellt: Kapitel, Unterkapitel, Bilder, Tabellen, usw. Kurz gesagt, alles worauf man in dem Text möglicherweise verweisen möchte, muss ein Label bekommen.
5. ```\cite{Nambe der Referenz}``` -> Erstellt eine Referenzierung
6. ```\autoref{Name des Labels}``` -> Erstellt eine Referenzierung zu einem Label
7. ```\ac{}``` und ```\acp{}``` -> Fügt eine vorher definierte Abkürzung ein, sodass dies immer Einheitlich ist und auf das Abkürzungsverzeichnis referenziert.

Hierzu muss die Abkürzung vorher im Abkürzungsverzeichnis.tex definiert werden (Beispiele wie das aussehen kann sind in der Datei enthalten)

\acp{} fügt die Abkürzung als Plural ein


Eine gute Einführung wie man Bilder ordentlich in LaTeX einfügt findest du hier: https://www.learnlatex.org/de/lesson-07.
Dort findet man darüber hinaus auch zu anderen Bereichen schnelle und übersichtliche Infos (ansonsten kann ChatGPT das im Großen und Ganzen auch alles).