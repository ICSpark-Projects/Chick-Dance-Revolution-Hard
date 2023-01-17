# chick-dance-revolution

## Description
This project builds on skills in handling events and making javascript functions. Create a game where you are a dancing chick!
This chick can move up, down, left, and right, and must do so in time to the arrows on the music board, which will be moving up
at different times.

## Difficulty
Intermediate/Advanced

## Prerequisites
- HTML structures and attributes
- Changing elements in HTML using DOM
- CSS Flexbox
- CSS keyframe animations
- JS Functions
- JS Arrays
- JS Events

## Make Note
For this project, save your work frequently, and to see your changes reflected in webview, always refresh the page.

## Setting Up

- Download the directory zip file (click green "Code" button, then click "download ZIP").
- Create the files: index.html, styles.css, and app.js.
- Open the zip and upload the assets folder into the directory you are working.
- Set up and link your index.html, styles.css, and app.js.

For the last step, follow these steps:
1. In your index.html file, initialize the file using the shortcut ```!```, then press tab. You should get something like the following.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>

</body>
</html>
```

2. Link your CSS and JS files as follows. You should have the link to the CSS stylesheet within the head tags
and the JS script within the body tags to ensure your CSS and JS are linked properly. Also make sure to title your file!

``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link rel="stylesheet" href="style.css">
  <title>Chick Dance Revolution</title>
</head>
<body>

  <script src="script.js"></script>
</body>
</html>
```

## Part 1: HTML

### 1. Create the following HTML elements within the body tags, following the nested structure.

- div with the id "container". This div will hold all our elements.
  - h1 with the inner HTML "Chick Dance Revolution".
  - div with the id "game". This div will hold all game elements.
    - div with the id "dance-board". This div will hold chick and the dancefloor.
    - div with the id "music-board". This div will hold the music note arrows.
      - div with the id "top-notes". This div will hold the arrows at the top of the music board.
      - div with the id "move-notes". This div will hold the arrows at the bottom of the music board, which will move up to the top.
  - button with the id "play" and inner HTML "Play". This button will start the game.
  - div with the id "score". This div will hold the score text.
    - h2 with the id "score-text" and the inner HTML "Score: 0". This div represents the score text.

Your HTML should look like this:

```
  <div id='container'>
    <h1>Dance Chick Revolution</h1>
    <div id='game'>
      <div id='dance-board'></div>
      <div id='music-board'>
        <div id='top-notes'></div>
        <div id='move-notes'></div>
      </div>
    </div>
    <button id='play'>Play</button>
    <div id='score'>
      <h2 id='score-text'>Score: 0</h2>
    </div>
  </div>
```

### 2. Add the following within each of the respective divs:

div with id "dance-board":
```
        <img src="assets/blue-arrow.png" alt="left blue arrow" id='dancearrow-upperleft' class='dancearrow'>
        <img src="assets/blue-arrow.png" alt="up blue arrow" id='dancearrow-up' class='dancearrow'>
        <img src="assets/blue-arrow.png" alt="upperright blue arrow" id='dancearrow-upperright' class='dancearrow'>
        <img src="assets/blue-arrow.png" alt="left blue arrow" id='dancearrow-left' class='dancearrow'>
        <img src="assets/chick-base.png" alt="chick" id='chick'>
        <img src="assets/blue-arrow.png" alt="right blue arrow" id='dancearrow-right' class='dancearrow'>
        <img src="assets/blue-arrow.png" alt="lowerleft blue arrow" id='dancearrow-lowerleft' class='dancearrow'>
        <img src="assets/blue-arrow.png" alt="down blue arrow" id='dancearrow-down' class='dancearrow'>
        <img src="assets/blue-arrow.png" alt="lowerright blue arrow" id='dancearrow-lowerright' class='dancearrow'>
```

The above code adds the chick element and the arrow elements to the dance board.

div with id "top-notes":
```
          <img src="assets/blue-arrow.png" alt="up blue arrow" id='toparrow-up' class='toparrow'>
          <img src="assets/blue-arrow.png" alt="right blue arrow" id='toparrow-right' class='toparrow'>
          <img src="assets/blue-arrow.png" alt="down blue arrow" id='toparrow-down' class='toparrow'>
          <img src="assets/blue-arrow.png" alt="left blue arrow" id='toparrow-left' class='toparrow'>
```

The above code adds 4 arrow elements to the music board. These are the arrows at the top of the board that don't move.

div with id "move-notes":
```
          <img src="assets/blue-arrow.png" alt="up blue arrow" id='movearrow-up' class='movearrow'>
          <img src="assets/blue-arrow.png" alt="right blue arrow" id='movearrow-right' class='movearrow'>
          <img src="assets/blue-arrow.png" alt="down blue arrow" id='movearrow-down' class='movearrow'>
          <img src="assets/blue-arrow.png" alt="left blue arrow" id='movearrow-left' class='movearrow'>
```

The above code adds 4 arrow elements to the music board. These are the arrows at the bottom of the board that will move upwards.

Don't forget to check your webview to make sure everything is correct!

Check and save your changes before moving on.

## Part 2: CSS

Next up, head to your style.css file. We are going to add style to our elements.

### 1. Main elements styling

Copy the below code and follow the directions in the comments.

```
body {
  /* Set the background image to the asset farm.jpg */
}

#container {
  /* Set the position to fixed. This will ensure no elements move out of place. */
}

#chick {
  /* Set height and width to 250px */
}

h1 {
  /* Style title font how you want */
}

#game {
  /* Set the display to flex. This will help organize the main divs */
}

#dance-board {
  /* Set border to 2px solid black */
  /* Set height and width to 750px */
  /* Set background color to reasonable color like gray */
  /* Set the left margin to 300px. This helps position the dance board correctly. */
}

#music-board {
  /* Set border to 2px solid black */
  /* Set height to 750px and width to 700px */
  /* Set background color to reasonable color like orange */
  /* Set right margin to 300px */
  /* Set display to flex */
  /* Set justify content to center */
}
```

### 2. Arrow elements styling

Copy the below code and follow the directions in the comments.

```
.dancearrow {
  /* Set height and width to 240px */
}

#dancearrow-up {
 /* Set transform to rotate(180deg) */
}

#dancearrow-upperright {
  /* Set transform to rotate(225deg) */
  /* Set opacity to 50% */
}

#dancearrow-right {
  /* Set transform to rotate(-90deg) */
}

#dancearrow-lowerright {
  /* Set transform to rotate(-45deg) */
  /* Set opacity to 50% */
}

#dancearrow-lower {
  /* Set transform to rotate(90deg) */
}

#dancearrow-upperleft {
  /* Set transform to rotate(135deg) */
  /* Set opacity to 50% */
}

#dancearrow-left {
  /* Set transform to rotate(90deg) */
}

#dancearrow-lowerleft {
  /* Set transform to rotate(45deg) */
  /* Set opacity to 50% */
}

.toparrow, .movearrow {
  /* Set height and width to 150px */
}

#toparrow-up, #movearrow-up {
  /* Set transform to rotate(180deg) */
}

#toparrow-right, #movearrow-right {
  /* Set transform to rotate(-90deg) */
}

#toparrow-down, #movearrow-down {
  /* Set transform to rotate(0deg) */
}

#toparrow-left, #movearrow-left {
  /* Set transform to rotate(90deg) */
}

#top-notes {
  /* Set display to flex */
  /* Set self align to flex-start */
}

#move-notes {
  /* Set opacity to 80% */
}

#movearrow-up {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 800px */
}

#movearrow-right {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 650px */
}

#movearrow-down {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 500px */
}

#movearrow-left {
  /* Set position to absolute */
  /* Set bottom to 500px */
  /* Set right to 350px */
}
```

This code sets up some important formatting for the dance board and music board. For example, we transform our arrows to point them in the correct direction. Make sure your move arrows and top arrows are in the correct position. Don't worry if the move arrows appear higher up than they should be. This will be fixed when we style the last elements.

The movearrows are going to be animated and will need keyframes. This brings us to the next step.

Copy the below code and follow the directions in the comments. If you are stuck, follow the formatting [here](https://www.w3schools.com/cssref/css3_pr_animation-keyframes.php).

```
@keyframes moveUp {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}

@keyframes moveLeft {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}

@keyframes moveDown {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}

@keyframes moveRight {
  /* Have the keyframe go from bottom: 500px to bottom: 1100px */
}
```

### 3. End elements styling

Finally, we must add styling to our play button and score text so that they appear on the page correctly and neatly.
Copy the below code and follow the directions in the comments.

Style the play button
```
#play {
  /* Set left and bottom margins to 300px */
  /* Set the display to inline block */
  /* Style the font size, background color, border radius, color, etc. */
}
```

Style the score text
```
#score {
  /* Set left margin to 1000px */
  /* Set bottom margin to 300px */
  /* Set the display to inline block */
  /* Set height to 200px */
  /* Set width to 300px */
  /* Style the font size, background color, border radius, color, etc. */
}
```

Check and save your changes before moving on.

## Part 3: JS

Now we are finally into the JavaScript section. Head to your script.js file and follow along.

### 1. Set up variables, storing references for elements using DOM method ```document.getElementById(elementId)```.
- Create variable for element chick called "chick"
- Create variables for elements with ids dancearrow-up, dancearrow-left, dancearrow-right, dancearrow-down called "danceArrowUp", "danceArrowLeft",
"danceArrowRight", and "danceArrowDown"
- Create variables for elements with ids movearrow-up, movearrow-left, movearrow-right, movearrow-down called "moveArrowUp", "moveArrowLeft",
"moveArrowRight", and "moveArrowDown"
- Create variable for element score text called "scoreText"
- Create integer variable for keeping track of player's score called "score". It should be set to 0.
- Create empty array variable called "moves" for holding game moves
- Create integer variable called "currentMove" with the value 0 to keep track of the current move in the "moves" array.

### 2. Detecting player movement

An essential part of Chick Dance Revolution is the chicken moving up, down, left, and right. For this to occur,
we need to be able to detect what keys the player is pressing. In particular, the controls are the arrow keys.
So we need to add an event listener.

#### 2.1. Create an event listener on document to detect the 'keydown' event.

Remember, an event listener takes in two parameters, the type of event and a function. Pass in the parameter "event"
into the event listener function.

Then, within the event listener function, write the following code.

```
var key = event.key; // "ArrowRight", "ArrowLeft", "ArrowUp", or "ArrowDown"
```

The variable key will tell us exactly what key was pressed, and for the arrow keys, I've commented exactly
what these values can be.

Knowing what key was pressed will help us determine what actions to take. The chick needs to be able to move in 4 directions,
and the arrows need to change accordingly as well.

Set up if/else if statements to check whether the variable key is equal to "ArrowRight", "ArrowLeft", "ArrowUp", or "ArrowDown".

Within those statements, make the following changes:
- Change the source of the chick to the right direction
  - Ex: chick.src = 'assets/chick-left.png';
- Change the source of the appropriate dance board arrow and music board moving arrow to the orange arrow image.
  - Ex: danceArrowUp.src = 'assets/orange-arrow.png';
  - Ex: moveArrowUp.src = 'assets/orange-arrow.png';

Now try moving the chick using the arrow keys. You should notice arrows changing from blue to orange and the chick changing
direction. But do you see the issue? Once you stop pressing the keys, we should see the orange arrows go back to blue and the chick
reset to its default position, but this is not the case. As such, we need to add another event listener.

#### 2.2. Create an event listener to detect the 'keyup' event. 

Format this event listener similar to the 'keydown' event listener.
Once again, create the key variable and the if/else if statements corresponding to whether key equals "ArrowRight", "ArrowLeft", "ArrowUp", or "ArrowDown".

Outside your if/else statements, reset the source of the chick to the chick base image.

Within your if/else if statements, reset the source of each appropriate arrow to the blue arrow image.

Now try moving the chick again. You should see the chick's movement and the arrows' colors reset appropriately.

What comes next? Now that we can move our character, it is time to make the game functional.

### 3. Function to play game

#### 3.1. Create a function called "playGame()" to run the Chick Dance Revolution game.

Then, go back to your index.html and look for the play button. In this button, add the attribute ```onclick=playGame()```.
This is another way to add an event listener besides just doing it in JavaScript. With this in place, if a user presses the
button, the playGame() function will execute.

Head back to script.js. Within the playGame() function, we are going to focus on making the music board arrows move in response to a premade
array of moves. To do this, let's first assign values to the moves array that we created at the top of the file.

#### 3.2. Creating moves

At the top of the script.js file below your "currentMove" variable statement, make a for loop that runs however many iterations you want the game to be. For instance, the for loop could run 30 times for 30 moves. Do not use the "currentMove" to iterate through the for loop!

Within this for loop, add the following code:
```
moves.push(Math.floor(Math.random() * 4));
```

This will push a random value from 0 to 3 (inclusive) onto the moves array. We are considering 0 = up, 1 = down, 2 = right, and 3 = left.
So for instance, if the value 0 was pushed onto the moves array, that indicates we added an up arrow move to our array.

Now that we have the moves array all set, now we can implement the functionality of the arrows on the music board moving up according to
what the current move is. To do so, we must use something called setInterval.

#### 3.3. Creating set interval function

setInterval is a function that enables us to call a function repeatedly after a set period of time, which will be useful for our game.

Add the following code into your playGame() function:
```
  var intervalID = setInterval(function movingNotes() {
    clearInterval(intervalID);
    // check moves, 0 = up, 1 = down, 2 = right, and 3 = left
    // increment i
    // check whether to continue or end game
  }, 1500);
```
This code will form the basis for what we need.

Right after the clearInterval(intervalID) statement, create if/else if statements to check if moves[currentMove] == 0, moves[currentMove] == 1, moves[currentMove] == 2, or moves[currentMove] == 3. 

Increment "currentMove" after all these if/else if statements because we want to keep iterating through the moves array after making a move.

Then, at the end we must check whether to continue or end the game based on the value of currentMove.
If currentMove < moves.length, call the playGame() function. Else if currentMove == moves.length, create a new audio using the "chicken-sound.mp3" in the assets folder and play the audio. Follow [here](https://stackoverflow.com/questions/9419263/how-to-play-audio) for reference. The audio signifies the end of the game.

#### 3.4. Implementing arrow up animation functionality

Notice how we haven't put anything within the if/else if statements to check each of the moves made. This is where we need to set the
arrow elements to have an animation. Add the following code within the first if statement that checks if moves[currentMove] == 0:

```
moveArrowUp.style.animation = 'moveUp 1s linear 1';
```

Copy this code into the other else if statements and adjust it appropriately.

Now try playing the game. Things should be coming together! One issue you may notice is the arrow moving up animation stops immediately.

To fix this, we must add more event listeners. For each of the moving arrow variables, add an event listener for "animationend".
Within each of the event listener functions, set the animation state for the appropriate arrow back to "none".

Now if we play the game again, the moving arrows should reset correctly.

### 4. Keeping Score

The final task to make this game work is to implement the scoreboard.

To do so, go back to your 'keydown' event listener code. Here, within the if statement to check if key == "ArrowRight", add the following code and follow the directions in the comments:
```
    var rect = moveArrowRight.getBoundingClientRect();
    // Check a certain range that the arrow was hit
    if (rect.top >= 100 && rect.top <= 300) {
      // increment "score"
      // change "scoreText" inner HTML to reflect updated score
    }
```

Paste the same code into each of your else if statements and adjust it appropriately.

You should see the score increase when you correctly hit the arrow.

Congrats! You have successfully implemented Dance Chick Revolution! Make sure to save your work!

## Stretch Goals
- Add a button to reset the game after it is complete.
- Create a menu to adjust the speed of the moving arrows.
- Add sound effects for each of the moving arrows when they correctly hit the top arrows.
- Make the length of the game adjustable for the player
- Decrease from the score when the player misses the top arrow



