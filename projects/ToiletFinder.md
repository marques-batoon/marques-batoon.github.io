---
layout: project
type: project
image: img/logo.png
title: "Toilet Finder"
date: 2023
published: true
labels:
  - JavaScript
  - HTML5
  - CSS
  - Bootstrap
  - ReactJSX
  - MongoDB

summary: "Final project for ICS 314. Full Stack application for UH Manoa students to find and rate bathrooms on UH campus."
---

<div class="text-center p-4">
  <!-- <img width="120px" src="../img/math-marques.png" class="img-thumbnail" > -->
  <img width="200px" class="img-thumbnail" src="../img/logo.png">
</div>

This is the first dynamic website web application I created using JavaScript making dynamic HTML and CSS.

It's a Web Application game made with JavaScript where the user needs to input the correct answer to a basic arithmetic equation. However, there is a time limit of 10 seconds for which the user can input the correct answer and progress to the next question. High scores are recorded and displayed using RESTful API.

My goal of this web application was to practice and solidify everything I've just learned about HTML, CSS, and JavaScript. Math has always been my favorite class since I was a kid so I decided to make this arithmetic game. I made sure to display everything to the user in an easy-to-understand fashion that's easy on the eyes using my own as well as bootstrap styling. 

Before this project I had learned how to write to and read from restFUL API by making a to-do-list. Learning from this I wanted to implement that into this web application and did so by implementing a high score section that saves for users that score over 10 points. Each arithmetic option holds its own list of high scores. Using JavaScript methods I also implemented different images with varying messagees depending on what score the user had just completed.

Try the app here: [Good luck. Hope to see you on the leaderboards!](https://arithmetic-marques-batoon.netlify.app/)

Below is a sample of the countdown function used in the app and the live updates made to the HTML.

```js
// vvv countdown function vvv
var timeleft = 10;
var timerStart = function() {
    $('img').fadeOut("fast");
    $('button').prop("disabled", true);
    $('#userAnswer').prop("disabled", false);
    $('.form-check-input').prop("disabled", true);
    document.getElementById("userAnswer").focus();
    var downloadTimer = setInterval(function(){
    if(timeleft <= 0){
        clearInterval(downloadTimer);
        timeleft = 10;
        document.getElementById("countdown").innerHTML = timeleft + " seconds left";
        $('#userAnswer').val('');
        $('#userAnswer').prop("disabled", true);
        $('button').prop("disabled", false);
        $('.form-check-input').prop("disabled", false);
        if(currentScore > globalHighScore){
            addScore(currentScore);
            $('small').html('Nice Job!');
            alert("Congratluations on getting the new high score!"); 
            $('#tanuki').attr("src", "./pics/chouureshii.png");
            $('#goodluck').attr("src", "./pics/nice.png");
        }
        else if(currentScore > 10){
            $('small').html('Nice Job!');
            addScore(currentScore);
            alert("You made it to the leaderboard!");
            $('#tanuki').attr("src", "./pics/chouureshii.png");
            $('#goodluck').attr("src", "./pics/nice.png");
        }
        else if(currentScore < highScore){
            $('#tanuki').attr("src", "./pics/akiramenaide.png");
            $('#goodluck').attr("src", "./pics/goodluck.png");
        }
        else if(currentScore > 1) {
            $('#tanuki').attr("src", "./pics/yatta.png");
            $('#goodluck').attr("src", "./pics/keepgoing.png");
        }
        $('img').fadeIn("slow");
    } else {
        document.getElementById("countdown").innerHTML = timeleft + " seconds left";
    }
    timeleft -= 1;
    }, 1000);
    currentScore = 0;
    $('#score').html('Score: ' + currentScore);
    timeleft = 10;
    $('#countdown').html(timeleft + ' seconds left');
}
```
