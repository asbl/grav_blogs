---
title: "Turtle-Grafik in Moodle"
date: 02-10-2020
published: true
type: post
author: asbl

---
Heute habe ich ein Experiment gestartet:

Mit [Skulpt](https://skulpt.org/) habe ich in mein Moodle Turtle-Grafik eingebunden.

Dafür habe ich -[wie hier beschrieben](https://skulpt.org/using.html)- Skulpt in den Moodle-Ordner hochgeladen und die beiden Javascript-Dateien unter "Website-Administration->Design->Zusätzliches HTML einbinden" eingebunden.

Anschließend habe ich folgenden Code in ein Textfeld eingegeben:

Mit Turtle-Grafik kannst du viele Arten von Bildern und Figuren zeichnen.

  * Zeile 1 importiert die turtle-Bibliothek von Python.
  * Zeile 2 erstellt eine Turtle
  * Zeile 3 steuert die Turtle 100 Einheiten nach vorne.

Führe das Programm aus.
```
<div class="flex-container">
    <div class="flex-item skulpt-column">
        <div id="editor" cols="40" rows="10">import turtle
turtle = turtle.Turtle()
turtle.forward(100)
        </div>
    </div>

    <div class="flex-item skulpt-column">
        <!-- If you want turtle graphics include a canvas -->
        <div id="canvas"></div>
        <pre id="output"></pre>
    </div>
</div>


<script type="text/javascript">
    var editor = ace.edit("editor");
    editor.session.setMode("ace/mode/python");

    function outf(text) {
        var mypre = editor.getValue();
        mypre.innetextarearHTML = mypre.innerHTML + text;
    }

    function builtinRead(x) {
        if (Sk.builtinFiles === undefined || Sk.builtinFiles["files"][x] === undefined)
            throw "File not found: '" + x + "'";
        return Sk.builtinFiles["files"][x];
    }
    function skulpt_clear() {
        $("#canvas").empty();
         console.info("clear");
    }
    function skulpt_runit() {
        skulpt_clear();
        console.info("run");
        var prog = editor.getValue();
        var mypre = document.getElementById("output");
        mypre.innerHTML = '';
        Sk.configure({
            output: outf,
            read: builtinRead,
    __future__: Sk.python3,
        });
        (Sk.TurtleGraphics || (Sk.TurtleGraphics = {})).target = 'canvas';
        var myPromise = Sk.misceval.asyncToPromise(function() {
            return Sk.importMainWithBody("<stdin>", false, prog, true);
        });
        myPromise.then(function(mod) {
                console.log('success');
            },
            function(err) {
                console.log(err.toString());
               $("#output").text(err.toString());
            });
    }
</script>



<style type="text/css" media="screen">
    #editor {
        position: relative;
        height: 400px;
        min-width: 300px;
        border: 1px solid grey;
    }

    #canvas {
        border: 1px solid grey;
        min-width: 300px;
        height: 400px;
    }

    .flex-container {
        display: flex;
    }
   .skulpt-column {
       width: 48%
    }
</style>
 <button type="button" onclick="skulpt_runit()">Run</button>
 <button type="button" onclick="skulpt_clear()">Clear</button>
```

Das Ergebnis sieht so aus:

![](2020-11-18-21-03-06.png)