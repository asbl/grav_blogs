---
title: Python als Programmiersprache im Unterricht
author: a.sbl
type: post
date: 21-02-2018

custom_total_hits:
  - 000000269
categories:
  - Informatikunterricht
  - Schulpolitik

---
Im hessischen Abitur werden zum Thema &#8220;Objektorientierte Programmierung&#8221; die Programmierbeispiele in zwei Sprachen angeboten: JAVA und Delphi.

Delphi bzw. Lazarus als Open Source Alternative hat inzwischen einen gewissen historischen Wert. die Sprache wird außerhalb des deutschen Informatikunterrichtes praktisch nirgends mehr benutzt. In Hessen ist sie nur deshalb noch von Bedeutung, da diese lange Zeit Grundlage der Informatikausbildung war und vor allem viele Quereinsteiger keine andere Sprache sprechen.

JAVA ist da schon ein anderes Kaliber. JAVA ist die meist verbreitetste Sprache überhaupt und wird auch von vielen Universitäten als erste Programmiersprache verwendet. Mit Greenfoot, BlueJ, dem [JavaEditor][1], [Gamegrid][2], [Kara][3], dem [Hamstersimulator][4] verfügt JAVA über zahlreiche gute Entwicklungsumgebungen und Frameworks, die zum Unterrichten mit der Sprache geeignet sind. Gleichzeitig ist das Lehren mit JAVA auch mit zahlreichen Fallstricken versehen, da die Sprache für die professionelle Entwicklung in großen Teams gut geeignet ist, aber nicht als erste Programmiersprache für Programmieranfänger vorgesehen ist. Dies fängt mit dem üblichen Grundkonstrukt an:

<pre class="EnlighterJSRAW" data-enlighter-language="java">public static void main(String args[]) {
}</pre>

verbunden mit zahlreichen Problemen, die dem ersten Problemlösen in Java im Weg stehen:

  * Installation des SDKs und richtiges Setzen der Pfadvariablen.
  * Zahlreiche Syntaxfehler beim Vergessen von runden oder geschweiften Klammern oder des Semikolons am Ende einer Zeile.
  * Durch das Strong Typing wird mehr &#8220;Fingertyping&#8221; benötigt, es dauert dadurch einfach länger bis man zu Ergebnissen kommt. Und spätestens wenn man in der Objektorientierung mit Containern und Casts beschäftigt, muss man sowieso darüber nachdenken was für einen Typ das aktuell verwende Objekt gerade haben könnte.
  * In Kombination mit Greenfoot: Zahlreiche Programmierkonzepte müssen &#8220;gleichzeitig&#8221; gelernt werden um einfache Programme zu schreiben (Objektorientierung, Interaktion von Objekten, Vererbung)
  * In Kombination mit GUIS: Komplizierte Klassenhierarchie (man verwende nur mal ein JTextField, auch hier müssen wieder viele Konzepte (imperative Programmierung, Objektorientierung) gleichzeitig gelernt werden.
  * Lesen und Schreiben in Dateien ist eine einzige Qual. Auch das Lesen von Tastatureingaben ist umständlich
  * Man muss sich als Lehrer und Lernender entscheiden, ob man statische Arrays oder direkt mit den objektorientierten ArrayLists anfängt. In der Regel benötigt man für objektorientierte Programmierung letzteres. Sollte man dann also die Arrays direkt überspringen?
  * [und vieles mehr&#8230;][5]

Meine persönliche Erfahrung aus mehreren Java-Kursen an der Schule und der Universität war folgende: Java wird von Lernenden als extrem schwergewichtige Sprache wahrgenommen. Alleine der Gedanken nach einiger Zeit Programmierpause sich wieder in Java einarbeiten zu müssen, verursacht Stöhnen. Ich kenne auch fast niemanden -außer Informatikstudenten-, der Java gelernt hat und anschließend für irgendeinen Zweck noch einmal freiwillig verwendet hat.

Schön wäre es daher, wenn man statt Java auf eine leichtgewichtige Sprache setzt, die leicht zu lernen ist, besser im Kopf behalten werden kann und daher besser dazu befähigt, Probleme zu lösen. Das Lösen von Problemen mit Hilfe eines geeigneten Werkzeuges sollte meiner Meinung nach einer der Kernkompetenzen sein, die Schüler im Informatikunterricht lernen sollten. Siehe dazu auch eine der ersten Fragen im großartigen Buch [&#8220;How to think like a computer scientist&#8221;:][6]

What is the most important skill for a computer scientist

a) To think like a computer
  
b) To be able to code really well
  
c) To be able to solve problems
  
d) To be really good at math.

Die richtige Antwort ist ganz klar c). Doch wenn Schüler eine Programmiersprache später nicht mehr benutzen, weil ihnen diese als schwergewichtig und umständlich erscheint, dann haben wir als Informatiklehrer unser Ziel verfehlt.

Ich setze daher in meinem neuen E-Phasen Kurs auf Python als erste Programmiersprache und werde zu einem späteren Zeitpunkt meine Erfahrungen teilen. Gegebenenfalls werden wir später in der Objektorientierung nochmal auf Java wechseln, so wie es von dem großartigen deutschen Online-Lehrbuch [Informatik in der Schule][7] vorgeschlagen wird.

Der Vorteil von Java ist natürlich, dass es sehr gute Tools gibt um die Objektorientierung zu lernen, wie z.B. den Java Editor oder BlueJ. Insbesondere das interaktive erzeugen von Objektdiagrammen, die Kombination von Klassen- und Objektdiagrammen kann ein Riesenvorteil für den Unterricht sein. Ich finde es aber falsch den Hauptfokus des Fachs Informatik auf die Objektorientierung zu legen. Objektorientierung ist ein wichtiges Paradigma um zu verstehen, was notwendig ist, damit Programme im großen Stil und im Team programmiert werden können. Wie bedeutend Objektorientierung oder die Verwendung von Java ist, ist tatsächlich aber umstritten (siehe [[1]][8], [[2]][9], [[3]][10]), siehe dazu auch folgende Zitate. Damit ich nicht falsch verstanden werde: Es ist schon wichtig im Unterricht objektorientierte Programmierung zu lernen. Viel wichtiger ist es aber das Programmieren zu lernen und zu lernen wie man Probleme löst. Wie so oft versperrt die Objektorientierung hier auch in der Lehre schnell den Blick auf das Wesentliche.

Würde das Abitur in Hessen nicht Java als Programmiersprache vorsehen (wobei bisher noch kein Schüler an unserer Schule das schriftliche Abitur absolviert hat), dann würde ich auch erwägen komplett auf Python umzusteigen.

Meine erste Erfahrungen sind übrigens durchweg positiv: Die Schüler können mit wenigen Sprachkonstrukten schon schnell vielfältige Programme schreiben. Sie sind produktiv. Sie lernen keinen Sprachbalast, sondern direkt, wie sie Aufgaben lösen können. Vieles deutet darauf hin, dass ich mich mit diesem Weg anfreunden könnte.

Was spricht noch für Python:

  * [Python wird von fast allen großen US Universitäten als erste Programmiersprache verwendet.][11]
  * Verbreitung: Python ist nach [TIOBE][12] die meistverwendeste, leichtgewichtige Programmiersprache, nach [Redmonk][13] ebenfalls im Spitzenfeld mit Java und C#, nach [PYPL][14] direkt hinter JAVA. In allen Vergleichen sieht man aber, dass die Verbreitung von Python zunimmt, während die Verbreitung von Java konstant bleibt oder sogar abnimmt. Es ist durchaus vorstellbar, dass Python meistverbreitetste Programmiersprache sein könnte.
  * Durch die Einfachheit haben Schüler von Tag 1 an direkt tolle Erfahrungen und Erfolgserlebnisse.
  * Hervorragende Standardbibliothek, so dass auch echte Probleme (z.B. Bildbearbeitung) früh gelöst werden können.
  * Python ist Open Source! (Im Gegensatz zur Standard-Runtime-Environment von Java)

 [1]: http://javaeditor.org/doku.php
 [2]: http://www.java-online.ch/gamegrid/index.php
 [3]: https://www.swisseduc.ch/informatik/karatojava/javakara/
 [4]: http://www.java-hamster-modell.de/simulator.html
 [5]: https://pythonconquerstheuniverse.wordpress.com/03-10-2009
 [6]: http://interactivepython.org/runestone/static/thinkcspy/GeneralIntro/Algorithms.html
 [7]: https://www.inf-schule.de/content/14-lehrkraefte/3-umsetzunglehrplaene/2-grundfach/2-objectsfirstjava/WarumJavaPython.pdf
 [8]: https://www.codeproject.com/Articles/580877/Is-Object-Oriented-Programming-Overrated-Another-V
 [9]: https://content.pivotal.io/blog/all-evidence-points-to-oop-being-bullshit
 [10]: http://wiki.c2.com/?ArgumentsAgainstOop
 [11]: https://cacm.acm.org/blogs/blog-cacm/176450-python-is-now-the-most-popular-introductory-teaching-language-at-top-u-s-universities/fulltext
 [12]: https://www.tiobe.com/tiobe-index/
 [13]: http://redmonk.com/sogrady/08-06-2017
 [14]: http://pypl.github.io/PYPL.html