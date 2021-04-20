---
title: "Hack: Weniger Clicks in Moodle-Tests"
date: 22-12-2020
type: post
published: true
author: asbl
---

Für den Tag der offenen Tür hat eine Kollegin ein Quiz (im Rahmen eines Breakout-Kurses) erstellt. Das Quiz besteht aus einer einzelnen simplen Frage, damit die Teilnehmer sich mit dem Prozess vertraut machen.

Es folgen verschiedene Schritte:

  * Man muss in der Kursübersicht auf das Quiz klicken.
  * Man startet dort den *Versuch**.
  * Man beantwortet die Frage.
  * Man klickt auf "Versuch beenden"
  * Dort klickt man auf das öffnende modale Fenster, wo man die Abgabe des Versuches nochmal bestätigen musss.
  * Man kann nun den Versuch überprüfen und sieht nochmal alle richtigen Antworten.
  * Wenn man dies beendet, kommt man wieder zurück zur Startseite, wo man sich nochmal herausklicken muss.

  Es ist gut möglich, dass ich zwischendurch etwas vergessen habe. Das ist einfach nervig.

  Ich habe nun versucht, dies intuitiver zu gestalten. Da es sich um einen Tag der offenen Tür handelt, musste ich nicht alle Randfälle behandeln und es muss schnell gehen. 
  
  Ich bin (noch?) kein Moodle-Programmierer, kann aber ganz ordentlich mit Javscript, CSS und AJAX umgehen. Damit konnte ich diesen "Hack" (richtig schön ist es nicht, aber es dient dem Zweck) umsetzen.
  
   <video width="320" height="240" controls>
  <source src="./2020-12-22 hack-weniger-ckicks-in-moodle/hack.mp4" type="video/mp4">
Your browser does not support the video tag.
</video> 

  

  Hier mein Code:
  ```javascript

    // Load Quiz Result Data from Startpage
    $("#page-mod-quiz-attempt").each(function() {

        $('input:contains("Meine")').addClass("finishattempt");

        /*
        * Hier werden auf der Seite des Versuchs die Punkte angezeigt, wen man das Quiz schonmal durchgeführt hat.
        So wird die Übersichtsseite überflüssig.

        Die Informationen werden von der Übersichtsseite mit AJAX geladen
        */

        var quiz_start_page = $(".breadcrumb-block:last-child a").attr('href');
        console.info(quiz_start_page)
        try {
            var htmltext = $.ajax({
                url: quiz_start_page,
                cache: false,
                async: false,
                dataType: "html",
                success: function(data) {
                    total = parseFloat($.trim($(data).find('th:contains("Punkte")').text().split("/")[1]).replace(",", "."))
                    console.info(total)
                    grades = $(data).find(".cell.c2");
                    console.info(grades)
                    console.info(grades[0])
                    max = 0;
                    actual = 0;
                    for (var i = 0; i < grades.length; i++) {
                        actual = parseFloat($(grades[i]).text().replace(",", "."));
                        console.info(actual)
                        if (actual > max) {
                            max = actual
                        }
                    }
                    console.info(max, total)
                    if (!isNaN(total)) {
                        $("#region-main").prepend('<div class="status">Aktueller Status' + max + ' von ' + total + ' Punkten')
                        if (max == total) {
                            console.info("append")
                            console.info($(document).find(".status"))
                            $(document).find(".status").append('<span><br/> Du hast den Test bereich erfolgreich absolviert</span>');
                            $(document).find(".status").addClass("quiz_completed")
                        }
                    }
                }
            }).responseText;
        } catch (e) {
            console.log('Fehler beim Linkermitteln: ' + e);
        }
    });

    /*
    Von der Überprüfung-Seite kommt man wieder zurück zur Kursseite - Nicht zur Übersichtsseite des Quizzes 
    */

    $("#page-mod-quiz-review .questionflagsaveform").each(function() {
        var main = $(".breadcrumb-block:nth-last-child(1) a").attr('href');
        $("#page-mod-quiz-review .questionflagsaveform").append('<a class="backlink" href="' + main + '">Zurück zur Hauptseite</a>')
        $('a:contains("Überprüfung beenden")').hide()
    });


    $("#page-mod-quiz-review").each(function() {
        punkte = $("#page-mod-quiz-review .generaltable").find('th:contains("Punkte")').next().html()
        feedback = $("#page-mod-quiz-review .generaltable").find('th:contains("Feedback")').next().html()
        console.info(punkte, feedback)
        $("#page-mod-quiz-review #region-main").prepend('<div class="points">Punkte : ' + punkte + ' </div>')
        $("#page-mod-quiz-review #region-main").prepend('<div class="quiz-feedback">' + feedback + ' </div>')
    });

    /*
    Die Übersichtsseite startet automatisch mit einem animierten Icon
    */


    $("#page-mod-quiz-view").each(function() {
        console.info("test")
        var counter = 4;
        var interval = setInterval(function() {
            if (counter > 0) {
                $(".quizstartbuttondiv button").text("Quiz startet in... " + counter + " Sekunden")
                counter--;
                console.info(counter);
            }
            // Display 'counter' wherever you want to display it.
            if (counter == 0) {
                // Display a login box
                $(".quizstartbuttondiv button").click()
            }
        }, 1200);
    });


Mein CSS-Code:

```css

/*
Quiz
--------
*/

#page-mod-quiz-view .generaltable,
#page-mod-quiz-view .quizattemptcounts,
#page-mod-quiz-view h3 {
    display: none;
}

#page-mod-quiz-view #region-main {
    max-width: 500px;
    height: 500px;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    border: 2px solid orange;
    border-radius: 250px;
    padding-left: 30px;
    padding-left: 30px;
    padding-top: 80px;
    position: relative;
    animation: pulse 2s infinite;
}

#page-mod-quiz-review .backlink,
#page-mod-quiz-attempt .submitbtns input {
    width: 280px;
    height: 60px;
    font-size: 1.4em;
    border-radius: 20px;
    background-color: rgb(9, 119, 134);
    border: 2px solid #AEF6C7;
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    color: white;
    padding-top: 10px;
}

#page-mod-quiz-review .backlink:hover,
#page-mod-quiz-attempt .submitbtns input:hover {
    background-color: #F6AF65;
    border: 2px solid rgb(9, 119, 134);
    text-decoration: none;
}

.quiz_completed {
    border: 2px dashed green;
    padding: 20px;
    color: green;
    font-size: 14px;
    margin-bottom: 30px;
    display: block;
}

#page-mod-quiz-review .backlink {
    margin-left: auto;
    margin-right: auto;
    width: 300px;
    display: block;
}


@keyframes pulse {
    0% {
        -moz-box-shadow: 0 0 0 0 rgba(204, 169, 44, 0.4);
        box-shadow: 0 0 0 0 rgba(204, 169, 44, 0.4);
    }

    70% {
        -moz-box-shadow: 0 0 0 30px rgba(204, 169, 44, 0);
        box-shadow: 0 0 0 30px rgba(204, 169, 44, 0);
    }

    100% {
        -moz-box-shadow: 0 0 0 0 rgba(204, 169, 44, 0);
        box-shadow: 0 0 0 0 rgba(204, 169, 44, 0);
    }
}

#page-mod-quiz-review .que.correct {
    border: 4px solid #c0dbd4;
    padding: 20px;
    border-radius: 30px;
}

#page-mod-quiz-review .generaltable {
    display: none;
}

#page-mod-quiz-review .quiz-feedback {
    font-size: 1.6em;
    padding: 30px;
    border: 1px dashed green;
    background-color: #fafafa;
    border-radius: 10px;
    margin-bottom: 50px;
}

#page-mod-quiz-review .points {
    margin-bottom: 50px;
    font-size: 2.4em;
    text-align: center;
}
```

...und ich habe noch zwei Moodle Hacks im Quiz-Modul durchgeführt:

mod/quiz/processatemps.php
```php

 
if ($page == -1) {
   $nexturl = $attemptobj->summary_url();

//   to

if ($page == -1) {
   $finishattempt = 1;
```

mod/quiz/processatemps.php
```php
//Auskommentieren:
//﻿$button->add_action(new confirm_action(get_string('confirmclose', 'quiz'), null,

und in der folgenden Zeile Klammern entfernen

get_string('submitallandfinish', 'quiz')));

// wird zu:

get_string('submitallandfinish', 'quiz');
```
