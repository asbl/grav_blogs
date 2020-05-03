---
title: Gamegrid für Python
author: a.sbl
type: post
date: 15-04-2018

custom_total_hits:
  - 000000705
categories:
  - Informatikunterricht
  - Python

---
_**U****PDATE**: Die neue Version von Gamegridp gibt es nun unter neuen Namen hier: [miniworldmaker.it-teaching.de][1]_

Nach dem Umstieg von JAVA auf Python habe ich recherchiert, ob es Alternativen zu BlueJ bzw. Greenfoot (bzw. Gamegrid) für Python gibt. Die schlechte Nachricht: Es gibt leider keine. BlueJ und Greenfoot sind die besten beiden Argumente für die Verwendung von JAVA als erste Programmiersprache. Der dritte Grund ist die Verbreitung. Alle anderen Argumente sprechen aber gegen JAVA. Kaum ein Programmierer würde zustimmen, dass Java durch besondere Zugänglichkeit und didaktische Reduktion besonders gut für Programmieranfänger geeignet sei. Java wirkt für viele Programmieranfänger abschreckend und wird nicht umsonst im englichsprachigen Raum zunehmend als erste Programmiersprache verdrängt.

Eine Alternative zu Greenfoot in Java [Gamegrid][2] , ein stark an Greenfoot angelehntes Framework, welches mittels Jython auch mit Python programmierbar ist. Da ich allerdings ungerne auf Jython wechseln möchte, habe ich begonnen selbst ein Framework zu schreiben, dass Gamegrid bzw. Greenfoot für JAVA ersetzen soll. Das ganze steckt noch in den Kinderschuhen (ich habe einen halben Tag Arbeit investiert), wird aber demnächst weiterentwickelt. Hier findet ihr das GIT-Repository: <https://github.com/asbl/gamegridp> Hier findet ihr das Projekt in Pypi: <https://pypi.python.org/pypi/gamegridp/0.1> .

Ein Projekt für die Sommerferien habe ich mir auch schon ausgeguckt: [Hier][3] findet man einen Ansatz für eine Umsetzung von BlueJ auf Python. Diesen möchte ich gerne weiterentwicklen. Wenn BlueJ auch für Python existieren würde, würde es praktisch keinen Grund geben, Java als erste Programmiersprache zu verwenden.

 [1]: https://miniworldmaker.it-teaching.de
 [2]: http://www.tigerjython.ch/index.php?inhalt_links=navigation.inc.php&inhalt_mitte=gamegrid/gamegrid.inc.php
 [3]: https://github.com/X-Scapin/BlueP