---
layout: project
type: project
image: img/math-marques.png
title: "Arithmetic Game"
date: 2021
published: true
labels:
  - JavaScript
  - HTML5
  - CSS
  - Bootstrap
  - RESTful API 

summary: "A Web Application made with JavaScript. High scores are recorded and displayed using RESTful API."
---

<div class="text-center p-4">
  <!-- <img width="200px" src="../img/math-marques.png" class="img-thumbnail" > -->
  <img class="img-fluid" src="../img/math-marques.png>
</div>

This is the first Web Application I created that used JavaScript to change HTML and CSS to make a dynamic website.

It's a Web Application game made with JavaScript where the user needs to input the correct answer to a basic arithmetic equation. However, there is a time limit of 10 seconds for which the user can input the correct answer and progress to the next question. High scores are recorded and displayed using RESTful API.

Here is the code.

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

You can learn more at the [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
