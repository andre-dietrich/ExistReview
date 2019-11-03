<!--
author:   André Dietrich & Sebastian Zug

email:    LiaScript@web.de

version:  0.0.1

language: de

narrator: Deutsch Male

comment:  Feedback zur Begründung der Ablehnung des Exist-Antrags 2019.

import: https://raw.githubusercontent.com/liaTemplates/rextester/master/README.md

-->

# Feedback Exist Review

Dieser Kurs soll als Feedback des Gutachtens zu LiaScript dienen und geht auf
alle vier Sätze der Ablehnung im Detail ein.


Die interaktive LiaScript-Interpretation dieses Kurses finden sie unter:

https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/ExistReview/master/README.md#1

Siehe das original Projekt auf GitHub:

https://github.com/liaScript/ExistReview

## 1. Satz

> Die Vorarbeiten erscheine als Basis für eine eigene Plattform nicht
> hinreichend zumal diverse Open Source LMS und Content Aggregatoren verfügbar
> sind.

    --{{1}}--
LiaScript wurde an mehreren Instituten zur Lehre eingesetzt, nicht nur zur
Programmierung in verschiedenen Sprachen.

    {{1}}
``` js     -EvalScript.js
let who = data.first_name + " " + data.last_name;

if(data.visit) {
  who + " did visit LiaScript"; }
else {
  who + " did NOT visit LiaScript"; }
```
``` json    +Data.json
{
  "first_name" :  "Sammy",
  "last_name"  :  "Shark",
  "visit"      :  false
}
```
<script>
  let data = @input(1);
  eval(`@input(0)`);
</script>


    --{{2}}--
Siehe eine Übersicht über verschiedene frei nutzbare Templates. Diese können
über ein einfaches `import` Statement in verschiedene Kurse integriert werden:


      {{2}}
[Template-Index](https://liascript.github.io/course/?https://raw.githubusercontent.com/liaTemplates/Index/master/README.md#1)

      {{2}}
```cpp
#include <iostream>

int main()
{
  int i = 0;

  std::cin >> i;

  for(; i; i--)
    std::cout << "I can say Hello World in 45 languages! " << i << std::endl;
}
```
``` bash stdin
45
```
@Rextester.CPP(true,`@input(1)`)

    --{{3}}--
Andere Systeme skalieren nicht, das heißt, ein Austausch von Lehrinhalten
zwischen den Systemen wird nicht vollständig und von allen Systemen unterstützt.
Im Gegensatz zu anderen kommerziellen SCORM-kompatiblen Autorensystemen, enthält
ein LiaScript-Dokument alle Informationen und Konfigurationen in einer für einen
Menschen einfach zu lesenden und erweiterbaren Form und wird zurzeit nur im
Browser ausgeführt, das heißt, kein Backend ist erforderlich.



## 2. Satz

> Zudem trafen ähnlich gelagerte Ansätze in der Vergangenheit auf überschaubare
> Resonanz (z.B. [Oppia](https://www.oppia.org)).

    --{{1}}--
Bei Oppia handelt es sich um eine freie Plattform, jedoch existieren Kurse nur
in einer Version, man benötigt für jeden Schritt eine Internetverbindung.
LiaScript im Gegensatz ist dezentral, die Kurse werden extern gehostet und durch
die Verbindung zu Markdown und Versionsverwaltungssystemen wie Github, können
diese in unzähligen Versionen und Übersetzungen zur Verfügung gestellt werden.
Des Weiteren wird nur eine Internetverbindung während des Ladevorgangs eines
Dokumentes benötigt, danach kann der gesamte Kurs auch offline genutzt werden.


                             {{1}}
                        Versions-Zeit-Diagram
         100 |                                    r
             |                              r
             |                        r
             |                  r
    (Version)|            r
             |      r
             |r
             |*  *  *  *  *  *  *  *  *  *  *  *  *
           1 +-------------------------------------
             1              (Zeit)               100


    --{{2}}--
Des Weiteren stellt der Vergleich mit Oppia ein sogenanntes
[Totschlagargument](https://de.wikipedia.org/wiki/Totschlagargument) dar. Mit
der gleichen Begründung hätte man auch alle weiteren Konstruktionen eines
Flugapparates "widerlegen" können oder weitere Entwicklungen am autonom
fahrenden Auto. Außerdem hätte ebenfalls Udemy als positives Beispiel
herangezogen werden können.


## 3. Satz

> Die proprietäre Beschreibungssprache erscheint zur Einbindung in gängig LMS
> nicht optimal, da sie u.a mit Ansätzen zur Standardisierung / Modularisierung
> von Lerninhalten (z.B. edu-sharing initiative) sowie integrierten
> Didaktik-Konzepten (z.B. Lernpfade und didaktische Szenarien) kolidieren.

      --{{1}}--
Handelt es sich bei LiaScript um eine proprietäre Beschreibungssprache?

         {{1}}
    [( )] Ja
    [( )] Vieleicht
    [(X)] **Auf gar keinen Fall!**
****************************************************

LiaScript basiert auf Markdown, einem sogenannten "Open Format" zum Speichern
digitaler Inhalte. Alle damit erstellten Inhalte können auch ohne
LiaScript-Interpreter mit gängigen Markdown-Viewern oder nur einem Texteditor
gelesen werden.

Die Lizenz wird ausschließlich durch den Autor bestimmt, der auch alle Rechte an
seinem Werk behält. Er teilt nur einen Link über die Plattform.

_Siehe:_ https://en.wikipedia.org/wiki/List_of_open_formats

****************************************************

    --{{2}}--
LiaScript ist Open-Source und kann direkt in jede Webseite oder Kurs eingebaut
werden. Das Beispiel zeigt, wie dies mithilfe eines iframes gemacht werden kann.
Was noch fehlt, sind Connectors, die in der Lage sind, die Zustände eines Kurses
auch in einem LMS zu speichern, zurzeit geschieht dies noch im Browser des
Nutzers.


    {{2}}
```html
<iframe src="https://liascript.github.io/course/?https://raw.githubusercontent.com/liaScript/ExistReview/master/README.md#1">
</iframe>
```

    --{{3}}--
Bezüglich des didaktischen Konzeptes steht es dem Autor frei, sich für dasjenige
seiner Wahl zu entscheiden. LiaScript ist eine (Programmier-) Sprache, die
gängige Web-Technologien wie CSS, JavaScript, HTML nativ einbindet und somit
auch die Möglichkeit bietet Lernpfade, Metriken, etc. zu integrieren. Es sei
hierbei auf die Nutzung von Macros hingewiesen aus Satz [1](#2).


## 4. Satz

> Ein entsprechender Machbarkeitsnachweis steht noch aus.

      --{{1 UK English Male}}--
This small course could only give a brief overview on the capabilities of
LiaScript, but it should be enough, to disprove the unscientific statements that
were used against a funding of LiaScript.
