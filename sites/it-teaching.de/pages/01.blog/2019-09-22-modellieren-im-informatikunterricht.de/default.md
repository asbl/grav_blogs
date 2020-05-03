---
title: "Modellieren im Informatikunterricht - Über Begriffe und Fehlvorstellungen"
date: 10-10-2019
draft: false
type: post
author: asbl
draft: false
categories:
  - Informatikunterricht
tags:
  - Informatikunterricht
  - Theorie
---

## Entwurf vom 10.10.2019, überarbeitet am 16.10.2019

Disclaimer: Der Artikel ist noch nicht fertig. Beim schreiben des Artikels ist mir aufgefallen, dass der Sachverhalt mit jedem neuen Gedanken, den ich bedacht habe, immer komplexer wurde. Da meine Zeit durch Umstände in der realen Welt beschränkt ist, schaffe ich es in den verbleibenden Tagen der Herbstferien nicht den Artikel in dem Umfang und in der Qualität aufzuschreiben, die ich mir wünschen würde.

Ich stelle daher den Artikel in der vorliegenden Fassung als Diskussionsgrundlage zur Verfügung, um meine Ideen auf den Prüfstand zu stellen und um möglicherweise weitere Ideen zu erhalten, wie ich den weiteren Bearbeitungsprozess (Winterferien?) einbeziehen werde. Der Artikel wird aktualisiert. Da dieses Blog auf [Github](https://github.com/asbl/it-teaching) versioniert wird, kannst du dort alte Versionen des Artikels lesen.

Achtung: Der Artikel ist trotzdem schon sehr lang. Du solltest also etwas Zeit mitbringen.

# Modellieren

> Modellieren ist die Kernkompetenz und wichtigste Tätigkeit im Informatikunterricht. 

Auf diese Aussage können sich sicherlich Eltern, Lehrer, Fachwissenschaftler, Fachdidaktiker und Lehrer einigen. Code und Informatiksysteme sind vielleicht die komplexesten Artefakte, die der Mensch geschaffen hat und zur Zeiterschafft. Modellierung und das Arbeiten auf unterschiedlichen Abstraktionsebenen ist eine notwendige Tätigkeit, um mit der Komplexität dieser Artefakte umzugehen und Informatik für uns verständlich zu machen. 

Dennoch haben wir auf Twitter zuletzt einige Diskussionen darüber geführt, welche Bedeutung das Modellieren z.B. im Bezug zum Programmieren hat oder wie der Begriff "Informatisches Modellieren" gegenüber dem englischen Pendant "Computational Thinking" einzuordnen ist.

An dieser Stelle möchte ich darlegen, warum ich den Begriff "Modellieren" *trotzdem* auch problematisch finde und warum der Begriff zu Missverständnissen führt.

### Warum sind Begriffe überhaupt so wichtig?

Fachdidaktiker und Lehrer sind Personen, die zwischen Fachwissenschaft und Bevölkerung vermitteln. Wir arbeiten mit Begriffen, Inhalten und Kompetenzen aus der Fachwissenschaft und filtern, ordnen sie so, dass diese an Laien vermittelt werden können und prägen damit das Bild einer Fachwissenschaft in der Bevölkerung. Daher ist es besonders wichtig, dass die Begrifflichkeiten die wir verwenden sowohl aus fachwissenschaftlicher Perspektive als auch aus Perspektive des Laien eindeutig und möglichst unmissverständlich sind.

Marco Thomas führt in seiner [Dissertation](http://www.informatikdidaktik.de/Personen/marco/Informatische_Modellbildung_Thomas_2002.pdf) die Bedeutung informatischer Modellbildung für informatische Allgemeinbildung aus und stellt die Vielfalt informatischer Modelle dar. 

Herausgreifen möchte ich an dieser Stelle die 4 Haupttypen der Modellierung, da diese von besonderer Bedeutung für die spätere Argumentation sind. Thomas unterscheidet 4 allgemeine Funktionen von Modellen, von denen 2 besonders interessant sind:

  * Erkenntnistheoretische Modellierung: Das Modell dient zum "Erkenntnisgewinn zu einem realen Orginal". 

  * Technische Modellierung: Das Modell wird "durch möglichst vollständige Analogie zum *Ersatz* für das Original."

Der Unterschied findet sich in UML z.B. in dem Unterschied zwischen Entwurfsdiagrammen und Implementationsdiagrammen (siehe auch [dieser Beitrag](http://www.u-helmich.de/inf/abitur-informatik/material/Klassendiagramme.html)). 

Das Entwurfsdiagramm hat den Erkenntnisgewinn zum Zweck. Es werden die Ausschnitte modelliert, die von Bedeutung sind das Original besser zu begreifen, während das Implementationsdiagram im besten Fall eine *andere Darstellung* für die Implementierung ist.

Bei der Modellierung mit UML-Klassendiagrammen oder Sequenzdiagrammen sind Diagramme  meist Ausschnitte die den Teil von Original und Modell visualisieren, der nötig ist, um das Verständnis zu unterstützen und Kommunikation in Teams zu unterstützen. Bei ER-Diagramme

Bei Datenbanken sind z.B. ER-Diagramme viel 

### Computational Thinking

Im englischsprachigen Raum findet ein anderer Begriff eine immer größere Bedeutung: "Computational Thinking"

Peter J. Denning definiert den Begriff in seinem Buch [Computational Thinking](https://mitpress.mit.edu/books/computational-thinking) folgendermaßen:

**Computational Thinking** is the mental skills and practices for

* *designing* computations that get computers do job for us, and
* *explaining* and *interpreting* the world as a complex of information processes

Auch wenn das Wort Modellierung in dieser Definition nicht auftaucht, findet man sie hier "versteckt". *Designing*  und *Explaining und interpreting* sind Prozesse, die Modellierung enthalten. Ohne Modellierung können weder "Computations" erstellt werden noch die Welt erklärt und interpretiert werden.

### Modelle nach Schubert Schwill

Die Ähnlichkeit zwischen dem englischen Computational-Thinking Ansatz und Modellierung in der deutschen Fachdidaktik zeigt sich auch an der bekannten Darstellung aus [Schubert/Schwill](https://www.springer.com/de/book/9783827426529):

![Ideen](ideen.png)
(Grafik nach Schubert/Schwill)

In der Darstellung werden die fundamentalen Ideen um den Modellbegriff angeordnet und die Top-Level Ideen "Strukturierte Zerlegung", "Sprache" und "Algorithmisierung" sind drei unterschiedliche Zugänge zum Modellieren. Diese Darstellung unterscheidet sich von Dennings Idee insofern, dass die Zugänge "Simulieren" und "Entwerfen" in Dennings Definition zusammengefasst wurden.

Persönlich gefällt mir dieser Zugang - auch deshalb, weil in Schwills Ideen-Katalog Strukturierte Zerlegung sowohl als Top-Level Idee auftaucht als auch als Teil der Idee "Algorithmisierung" und es damit in sich konsequenter wäre, daraus eine Top-Level Idee zu machen.

Entscheidend ist in beiden Ansätzen, dass man im Kern mit Modellen arbeitet, aber konkrete Tätigkeiten und Ideen nicht als Modellierung beschrieben werden. In beiden Ansätzen werden stattdessen spezifischere Begriffe für die entsprechenden Tätigkeiten gewählt.

### Modellieren und Problemlösen

Neben Modellierung ist Problemlösen die andere bedeutende Tätigkeit im Informatikunterricht. Wenn man sagt, dass informatische Kompetenzen sich aus Modellieren und Problemlösen ableiten, dann hat man die wesentlichen Kompetenzen des Informatikunterrichts erfasst.

Interessant ist der Zusammenhang zwischen modellieren und problemlösen: Ist das Modell das Ergebnis eines Problemlöseprozesses oder ist ein Modell ein Hilfsmittel im Problemlöseprozess?

Die Antwort ist: Beides ist richtig.

Wenn ich ein E-R Modell erstelle, dann ist das fertige E-R Modell das Ergebnis eines Problemlöseprozesses, die Umsetzung in eine Datenbank eine Tätigkeit die theoretisch automatisiert erfolgen kann. Hier ist das E-R Modell das Ergebnis eines Problemlösepozesses.

Wenn man programmiere, dann wird ich bei komplexeren Programmen mehrere Arten von Modellen erstellen, z.B.: 

  * Man entwirft UML-Klassendiagramme, die Teile der Struktur meiner Klassen und Zusammenhänge visualisieren.
  
  * Man entwirft Sequenzdiagramm um die Kommunikation zwischen Objekten zu visualisieren.

  * Man entwirft Flussdiagramme oder Pseudocode (und ggf. auch Struktogramme), um Algorithmen grafisch zu veranschaulichen.
  
  * Man verwendet Metaphern für Bezeichner, damit mehrere Programmierer über diese Metaphern ähnliche mentale Modelle aufbauen.

  * Schnittstellen beschreiben, wie ein Modell verwendet werden kann. Durch die Abstraktion kann eine Bibliothek verwendet werden, wenn die Schnittstellen beschrieben sind ohne dass der User die Details der Implementierung kennen muss.
  
  * Der erstellte Code selbst ist letztendlich auch ein (ausführbares) Modell.

Die Liste ist mit Sicherheit nicht abschließend.

Man kann die Modelle hier grundlegend auf zwei Arten charakterisieren:

  * Modelle, die das Ergebnis eines Problemlöseprozesses sind.
  
  * Modelle, die als Heurismen dienen um den Problemlöseprozess oder das Verständnis über das zu Grunde liegende Informatiksystem zu unterstützen. 

Interessanterweise kann sogar die selbe Art von Modell auf beide Arten verwendet werden: Das UML-Klassendiagramm kann das Ergebnis einer Entwurfsphase sein, als Dokumentation und Arbeitsgrundlage für weitere Implementierungsphasen dienen oder es auch über Reverse-Engineering aus Code automatisch generiert werden und dann als Hilfsmittel dienen um gemeinsam Probleme zu lösen.

Wenn wir lehren wollen, wie mit Informatik die Welt beschrieben werden kann, dann müssen wir vor allem einen Blick darauf werfen, welche Rolle Modelle in realen Problemlöseprozessen haben. Hier spielt ein weiterer Faktor eine bedeutende Rolle: *Komplexität*.

*Komplexität* ist der Aspekt, der informatisches Problemlösen im Unterricht von mathematischen oder anderen Problemlöseprozessen unterscheidet. Mit Code wurden vielleicht die komplexesten Artefakte geschaffen, die der Mensch jemals erzeugt hat. Große Systeme wie google, facebook & co bestehen aus Milliarden Zeilen von Code, die kein Mensch jemals in seinem Leben alleine lesen kann. Aber auch kleinere Projekte können schnell aus vielen Zeilen Code bestehen, wenn man Bibliotheken verwendet und dadurch auf fremden Code vertraut. 

Wenn man sich jetzt einen Problemlöseprozess unter der Bedingung der Komplexität anschaut, dann haben dort Modelle eine entscheidende Funktion: Sie helfen, Komplexität und Details auszublenden und über Aspekte von Code zu sprechen ohne dass das komplette Team den kompletten Code gelesen haben muss (was wie gesagt unmöglich wäre).

Modelle ist sind in diesem Kontext also heuristische Hilfsmittel die dazu dienen den Problemlöseprozess zu unterstützen.

Wenn man im Informatikunterricht die Idee vermittelt, dass die Implementation von Modellen eine rein mechanische Tätigkeit sei, dann wird der entscheidende Aspekt ausgeblendet, dass das Modell als heuristisches Hilfsmittel dient um über Informatiksysteme zu reden und einen Problemlöseprozess zu unterstützen. 

Man sieht, dass ich im letzten Absatz oft den Begriff "Problemlöseprozess" verwendet habe. In der Informatik wird dieser Problemlöseprozess als **"Programmieren"** bezeichnet. Im Umgang unter Informatiklehrern und Didaktikern haftet dem Begriff oft etwas negatives an, weil Programmieren und Implementieren im deutschen Sprachbegriff oft fälschlicherweise gleichgesetzt werden. 

Ich werde die dahinter stehende Fehlvorstellung im Folgenden als **"Programmieren == Implementieren-Fehlvorstellung"** bezeichnen. Eine eigentlich komplexe Tätigkeit, die den kompletten Modellierungsprozess und darüber hinaus weitere Problemlösefähigkeiten enthält wird durch das gleichsetzten mit einer rein mechanischen Tätigkeit abgewertet.

Anmerkung: Natürlich könnte man programmieren auch als implementieren definieren. Wenn man diese Begriffe als Synonyme verwendet, entfernt man sich aber auch vom internationalen Sprachgebrauch des Wortes, was angesichts einer Fachwissenschaft in der vorrangig auf englisch kommuniziert wird, zu weiteren Missverständnissen führt.

### Modelle in der Softwareentwicklung am Beispiel des Wasserfallmodells

![Wasserfall-Modell](wasserfall.png)

Man sieht hier das Modell der Softwarentwicklung nach dem Wasserfall-Modell. Erst werden Anforderungen aufgestellt, anschließend ein informatisches Modell aufgestellt, welches implementiert, getestet und verifiziert und letztendlich gewartet wird. 

Das Wasserfall-Modell ist im Gegensatz zu den meisten neueren Softwareentwicklungsmodellen ein strikt lineares Modell und wird so in dieser Form eigentlich selten umgesetzt - Für die folgenden Erklärungen eignet es sich aber dennoch gut.

Wo finden sich hier Modelle?

* Am offensichtlichsten ist der Aspekt "Modellierung" in der entsprechenden Phase (Entwurf / Design) des Modells. Modellbildung bedeutet hier, ein Prozess, der als Ergebnis ein oder mehrere Artefakte hat (nämlich UML Diagramme und/oder weitere Dokumentation), welche anschließend implementiert werden können. 

* Als nächstes wird der Begriff Modell im "Wasserfallmodell" sichtbar, denn hier beschreibt das Modell den Prozess, in dem sich ein Team organisiert um eine Aufgabe zu lösen. Alternativen wären hier z.B. zyklische Modelle wie sie in der agilen Softwarentwicklung zu Grunde liegen. Diese Modelle verändern nicht nur die Anordnung der Phasen, sondern ganz grundlegende Aspekte:
  
  * Bei agiler Entwicklung hat die Modellierungsphase einen ganz anderen Stellenwert (siehe unten)
  
  * Nicht nur Abläufe, sondern auch auch das Welt- und Menschenbild spielt für das Softwarentwicklungsmodell eine Rolle. Man beachte, dass das [agile Manifest](https://agilemanifesto.org/iso/de/manifesto.html) von Werten ausgeht, aus denen Prinzipien und schließlich Prozesse abgeleitet werden.

* Etwas versteckter findet sich der Begriff Modellieren aber auch in der nächsten Phase, im "Implementieren":

  Im Wasserfall-Modell spielt dies freilich noch eine geringere Rolle. Die Idee des Wasserfall-Modells ist es, erst ein Modell zu erstellen und dieses Modell zu implementieren. Im Wasserfall-Modell ist das Modellieren oft die "anspruchsvolle" Tätigkeit, das implementieren (dann oft fälschlicherweise gleichgesetzt mit Programmieren) eine rein mechanische Tätigkeit. 
  Wenn man aber Probleme des Wasserfall-Modells betrachtet und überlegt, warum dieses Modell von anderen Entwicklungsmodellen verdrängt wurde, wird klar, warum dieser Gedanke irrführend ist: Probleme in allen Stufen des Wasserfall-Modells können dazu führen, dass man wieder beliebig viele Schritte "zurück" gehen muss. Ein Fehler, der beim Implementieren Testen auffällt, kann im schlimmsten Fall zur Änderung des Modells (Designphase) oder sogar der grundlegenden Anforderungen führen.

  Die daraus folgende Schlussfolgerung ist die: Man kann das Implementieren nicht vom Modellieren getrennt betrachten.

  Aus diesem Grund ist in vielen Softwareentwicklungsmodellen nicht mehr das Vorgehen, ein umfangreiches Designdokument zu erstellen, dass dann "nur noch" implementiert werden muss. Mit "Rapid Prototyping" werden in der agilen Entwicklung schnell lauffähige Modelle erstellt, das Ergebnis jedes Sprints ist ein lauffähiges Programm. 

  Die Vorstellung die damit verbunden ist, ist diese:

  Auch Code ist nicht nur Abbild eines Modells, sondern selbst ein (ausführbares) Modell. 

* Die Überlegung aus dem letzten Punkt zieht sich weiter in die nächste Phase: Wenn Code selbst ein ausführbares Modell ist, dann sind Strategien zum Erstellen guten Codes allesamt auch Modellierungstechniken. Das Schreiben von Tests (und insbesondere Test Driven Development) ist demnach auch eine Technik, die dabei hilft zu modellieren.

Im folgenden werde ich von der **"Wasserfall-Fehlvorstellung"** sprechen, wenn Ansätze Informatik zu beschreiben beim Leser das Wasserfall-Modell naheliegen. Diese Fehlvorstellung ist aus folgenden Gründen problematisch:

  1. Es ist beim Entwurf von Programmen nicht gegeben, dass die Entwurfsphasen in der Reihenfolge des Wasserfall-Modells durchlaufen werden müssen (Rapid-Prototyping, Test Driven Development, Refactoring...).
  
  2. Modellieren und Implementieren sind nicht zwei Phasen, die sich immer trennen lassen. Das Ergebnis einer Modellierung muss nicht zwingend ein (grafisches) Modell als Artefakt haben, sondern der Code selbst kann das einzige Artefakt und damit das ausführbare Modell sein.

  3. Modellieren dient oft als heuristisches Hilfsmittel für einen (kollaborativem komplexen) Problemlöseprozess. Ziel ist es meist nicht auf eine selbst Modellierung hinzuarbeiten, sondern meist ist die Modellierung Hilfsmittel um auf ein Ziel hinzuarbeiten

*Hinweis: Die Punkte 1 und 2 gelten für das Programmieren im Allgemeinen. Beim Entwurf von Algorithmen aus Perspektive der theoretischen Informatik wird zuerst ein Algorithmus entworfen  und die Implementierung spielt zum Entwurfszeitpunkt noch keine Rolle. In diesem speziellen Fall ist die Reihenfolge der Schritte durchaus noch von Bedeutung.

Wenn man aber für informatische Modellierung die Perspektive des Algorithmus-Entwurfes einnimmt, so ist dies vergleichbar, wie wenn man SuS in der Mathematik zum Lösen von "Real-World Problems" zunächst das Beweisen beibringt - Wenn es um Modellierung geht spielt diese Perspektive nur eine untergeordnete Rolle.**

## Modellierung und andere Fächer

Modellierung ist natürlich keine Tätigkeit, die auf die Informatik beschränkt ist. Auch in allen anderen Fächern ist Modellieren im Sinne von "die Realität mit Modellen begreifbar machen" und in der Form von"Heurismen zum Lösen komplexer Probleme" unverzichtbar.

Beispiele:

* Ein Schriftsteller erstellt einen Text und verwendet Modellierung in Form einer Gliederung oder Beziehungsnetzen. Die Gliederung ist ein *Modell* des Artefaktes Textes, so wie *Modellierung* in der Programmierung ein Modell des Artefaktes Code darstellen kann. Modellierung dient in diesem Kontext als Problemlösestrategie.
  
* In Geschichte, Politik, Wirtschaft und Erdkunde ist es eine entscheidende Tätigkeit von konkreten Sachverhalten aus der wirklichen Welt (z.B. Quellen) zu abstrahieren um ein Modell aufzustellen, welches anschließend analysiert und reflektiert werden kann. Man kann sagen: Die komplexesten Modellierungstätigkeiten finden in diesen Fächern statt, da es nichts komplexeres gibt als unsere Welt, die Menschen in dieser Welt und ihre Geschichte. Modellierung dient in diesem Kontext als Mittel zum Beschreiben von komplexen Zusammenhängen.

Informatische Modelle werden in beiden Kontexten benutzt. Sie dienen sowohl als Heurismus als auch zur Beschreibung von komplexen Zusammenhängen. Dennoch ist Modellierung **keine Tätigkeit, die spezifisch für die Informatik ist**. Modellierung ist in beiden Zusammenhängen eine grundlegende menschliche Fertigkeit.

Spezifisch für die Informatik ist vor allem das Arbeiten auf unterschiedlichen Abstraktionsebenen. Das OSI-Modell oder das TCP-Modell dienen nur zu diesem Zweck und erlauben es Abstraktionsebenen auszublenden um somit spezielle Gesichtspunkte des zugrunde liegende Modells zu betrachten. Ein UML-Klassendiagramm kann unterschiedlich detailliert sein, je nachdem welcher Aspekt der Modellierung betrachtet wird, selbst die Programmier(hoch-)sprache ist bereits eine Abstraktion des Maschinencodes. 

Zum Teil bietet die Informatik sogar automatisierte Methoden um Abstraktionsebenen zu wechseln, z.B. die Generierung von Code aus einem UML-Diagramm, die Generierung eines UML-Diagrammes aus Code oder das Erstellen eines Schaltwerks aus einem endlichen Automaten.

Daher gefällt mir auch sehr gut die Formulierung, die in englischen Lehrplänen anstelle von Modellierung gewählt wird: ["Working with abstractions"](https://www.doe.k12.de.us/cms/lib/DE01922744/Centricity/Domain/176/CSTA%20Computer%20Science%20Standards%20Revised%202017.pdf)

## Der Modellierungskreislauf

Ich kann nicht über Modellierung sprechen, ohne auch den Modellierungskreislauf nach [Hubert 2004](https://www.researchgate.net/publication/251201036_Essential_Ingredients_of_Literacy_in_Informatics) aufzugreifen

![Modellierungskreislauf nach Humbert](humbert.png)

Der Modellierungskreislauf ähnelt dem Modellierungskreislauf der aus der Mathematik-Fachdidaktik bekannt ist und skizziert, wie ausgehend von Phänomenen Aspekte der wirklichen Welt in informatische Modelle übersetzt und Ergebnisse rückübersetzt werden.

An dieser Stelle möchte ich bereits einhaken: In der Mathematik unterscheidet man in der Regel innermathematisches Arbeiten z.B. Beweise um neue Erkenntnisse über die Welt der Mathematik an sich zu gewinnen und Modellieren, bei dem mit Hilfe von Mathematik ein Erkenntnisgewinn über die Welt außerhalb der Mathematik gewonnen werden soll.

In der Informatik ist dies aber anders. Es gibt Modellierungen, bei denen Erkenntnisse über die reale Welt gewonnen werden, z.B. beim Entwickeln eines E-R Diagramms aus einer Sachsituation. Genauso bedeutend ist aber Modellierung mit dem Ziel Erkenntnisse über ein Informatiksystem zu gewinnen, d.h. die Modellierung findet innerhalb der Informatik statt. Wenn ein Team programmiert und der Code hinreichend komplex ist, dann wird Modellierung verwendet, um das gemeinsame Verständnis des zugrunde liegenden Informatiksystems zu verstehen. 

Die Analogie in der Mathematik wäre z.B. das Waage-Modell um Äquivalenzumformungen an Gleichungen zu verstehen. Dies würde man in der Mathematik-Fachdidaktik nicht unter die Kompetenz Modellierung fallen auch wenn man hier mit Modellen arbeitet. 

In der Informatik verhält sich dies aber anders: Modellierung zum Verstehen eines Informatiksystems ist hier eine Kompetenz, die man benötigt um z.B. komplexere Programme zu entwerfen. Um ein hinreichend komplexes Informatiksystem (z.B. gegeben in Code) zu verstehen, muss man zwangsläufig Modelle enwickeln. Im Gegensatz zum mathematischen Modellierungskreislauf ist die Verwendung von Modellen zum Verstehen "innerinformatischer"-Zusammenhänge grundlegender Bestandteil informatischer Modellierung. 

Ich nenne diese Fehlvorstellung im Folgenden die **"Modellierungskreislauf-Fehlvorstellung"**. Durch diese Fehlvorstellung wird die informatische Modellierung eingeengt auf die Aspekte, die dem Modellierungskreislauf in der Mathematik entsprechen.

Was mir in dem Modell außerdem fehlt ist zudem der Faktor *Kreativität*, ein ganz bedeutender Faktor in der Informatik. Kreativität in der Informatik bedeutet (auch), dass ich alles -egal ob dies seinen Ursprung in der realen Welt hat- mit Hilfe von Informatik in ein informatisches Modell umsetzen kann. Die Bandbreite der Ideen sind nicht durch Phänomene in der realen oder der digitalisierten Welt begrenzt, sondern alleine durch das, was man sich vorstellen kann. Im Modellierungskreislauf wird dieser Aspekt aber nicht sichtbar.

### Informatikstandards

Die [Bildungsstandards Informatik](https://www.informatikstandards.de/docs/Bildungsstandards_SII.pdf) sind ein besonderer politischer Schritt auf dem notwendigen Weg Informatik als Pflichtfach zu etablieren. Nur wenn wir uns einig sind, was wir unterrichten wollen, können wir auch darauf abzielen dies auch in Lehrplänen zu verankern. Wichtig ist , dass man darauf hinarbeitet, dass die Standards als das Dokument, welches beschreibt wie wir Informatikunterricht verstehen, möglichst frei von Missverständnissen und Fehlvorstellungen sind.

Die Standards sind aufgeteilt in Inhaltsbereiche und Kompetenzen.Bei den Kompetenzen findet sich die Kompetenz "Modellieren und Implementieren". 

* Bereits die Benennung dieser Kompetenz halte ich für problematisch, da sie die Fehlvorstellung aus dem veralteten Wasserfall-Modell unterstützt, dass man nur ein hinreichend gutes Modell aufstellen muss, dass man anschließend nur noch implementieren muss, d.h. das Modellierung und Implementierung sich voneinander trennen lassen. Diese Fehlvorstellung wird durch die Angabe des Modellierungs-Kreislaufes unterstützt ([siehe Glossar, S.21](https://www.informatikstandards.de/docs/v142_empfehlungen_kompetenzen-primarbereich_31-01-2019

* In den Bildungsstandards für die Sekundarstufe wird im Glossar sogar geschrieben: "Der Übergang von einem algorithmischen Modell zu einem Programm wird als programmieren bezeichnet." Hier versteckt sich die **"Implementieren == Programmieren-Fehlvorstellung"**. 


### Vorschläge

Begriffe sollten möglichst eindeutig und unmissverständlich verwendet werden. Daher ist es wichtig, bei der Verwendung der Begriffe Modellieren und Programmieren keine Fehlvorstellungen zu triggern. Mein Vorschlag ist es daher, den Begriff Modellieren nur dann zu verwenden, wenn dadurch keine Fehlvorstellungen und Missverständnisse getriggert werden.


## Lizenz

Der Artikel steht unter [CC BY 4.0 Lizenz](https://creativecommons.org/licenses/by/4.0/deed.de)

### Update

16.10: 

  - Erweiterung der Argumentation rund um den Modellierungskreislauf
  - Vergleich mit Modellierung in anderen Fächern.







