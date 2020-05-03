---
title: Miniworldmaker
author: a.sbl
type: post
date: 24-03-2019

custom_total_hits:
  - 000000174
categories:
  - Informatikunterricht
  - Python

---
Aus Gamegridp wird [MiniWorldMaker][1].

Das System nähert sich langsam einer stabilen Version an (Zeitplan: Nach den Osterferien soll die API weitgehend nicht mehr verändert werden) und ich bin zunehmend zufriedener mit der Code-Basis.<figure class="wp-block-image">

<img src="https://it-teaching.de/wp/wp-content/uploads/2019/03/image.png" alt="" class="wp-image-399" /></figure> 

So sieht der Code für dieses Beispiel aus:

<pre class="EnlighterJSRAW" data-enlighter-language="python" data-enlighter-theme="" data-enlighter-highlight="" data-enlighter-linenumbers="" data-enlighter-lineoffset="" data-enlighter-title="" data-enlighter-group="">from miniworldmaker import *


class MyBoard(PixelBoard):

    def __init__(self):
        super().__init__(columns=200, rows=200)
        self.add_image(path="images/stone.jpg")
        self.add_to_board(Robot(), position=(50, 50))


class Robot(Actor):

    def __init__(self):
        super().__init__()
        self.size = (30, 30)
        self.add_image("images/robo_green.png")

    def act(self):
        pass

    def get_event(self, event, data):
        if event == "key":
            if "A" in data:
                self.turn_left(10)
            if "D" in data:
                self.turn_right(10)
            if "W" in data:
                self.move(distance=3)


board = MyBoard()
board.show()
</pre>

 [1]: http://miniworldmaker.it-teaching.de/