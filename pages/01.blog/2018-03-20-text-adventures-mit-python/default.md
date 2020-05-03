---
title: Text-Adventures mit Python
author: a.sbl
type: post
date: 20-03-2018

custom_total_hits:
  - 000000222
categories:
  - Informatikunterricht
  - Python

---
3. Stunde Python: Nachdem die Schüler mit Turtle-Grafik erste Erfahrungen gemacht haben und im [Online-Kurs][1] parallel die Grundlagen trainiert haben stand nun in der dritten Stunde das Thema Text-Adventures auf dem Programm.

Prinzipiell ist es mein Ziel, den &#8220;langweiligen&#8221; Teil des Programmieren-Lernens auf den Online-Kurs zu verschieben und dann im Unterricht selbst spannende Anwendungsfälle untersuchen zu können. Text-Adventures sind deshalb besonders gut geeignet, da man hier sehr gut den Umgang mit Kontrollstrukturen lernen kann (man benötigt eine Mainloop und einen Haufen verschachtelte If-Elif-Else Abfragen) und sieht, wie selbst sehr simple Programme schnell aus sehr komplexen Code bestehen (der Umgang mit Komplexität ist einer der Dinge, die die Informatik als Disziplin ausmacht).

Der Grundaufbau eines Textadventures in Python kann so aussehen:

<pre class="EnlighterJSRAW" data-enlighter-language="python">zustand="start"
while (zustand!="ende"):
    if zustand=="start":
        print("Situationsbeschreibung")
        eingabe = input("Was tust du (f: In den Flur, a: Abhauen)")
        if eingabe=="f":
            zustand="flur"
        else:
            zustand="ende"
    elif zustand=="flur":
        print("Du betrittst den Flur")
        eingabe = input("Was tust du?")
    elif zustand=="ende":
        print("Du läufst davon...")
            


</pre>

Das ganze wird natürlich schnell extrem unübersichtlich&#8230; daher enstand bei einigen Schülern von sich aus bereits der Wunsch den Code irgendwie übersichtlicher zu gestalten, was hier zum Thema Funktionen führt:

<pre class="EnlighterJSRAW" data-enlighter-language="python">def flur():
    print("Du gehst in den Flur... oben hörst du Geräusche...")
    eingabe=input("""Was tust du?
        [r]ückwärts: Ich gehe zurück zum Haupteingang
        [o]ben: Ich gehe die Treppen hoch""")
    if eingabe=="r":
        return "haupteingang"
    if eingabe=="o":
        return "Erster Stock"</pre>

Weiterhin bietet es sich auch an Zufallsfunktionen einzuführen (um z.B. Kämpfe oder Gefahren zu simulieren). Das nächste mal werde ich daher diese Einheit mit einer Lerntheke ergänzen, auf der man die wichtigsten Funktionen nochmal nachlesen kann.

&nbsp;

Interessanterweise kamen **alle** Schüler sehr ordentlich mit den Aufgaben zurecht. Eine Erfahrung, die ich mit Java+Guis oder Java+Greenfoot so noch nicht gemacht habe. Wenn wir über Probleme gesprochen haben, dann meist nicht über einfache Syntaxfehler, sondern über grundlegende Logik-Fehler, die von den Schülern mit etwas Hilfestellung selbst entdeckt wurden. So macht mir das Unterrichten viel mehr Spaß und ich habe das Gefühl, dass viele Schüler schneller und mehr lernen, als in meinen bisherigen Java/Lazarus Kursen.

 [1]: https://stepik.org/course/6229/syllabus