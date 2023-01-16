# chick-dance-revolution

This project builds on skills in handling events and making javascript functions. Create a game where you are a dancing chick!

## Step 1: Setting Up

- Download the img files 
- Create the files: index.html, styles.css, and app.js
- Upload the img folder into the directory you are working
- Set up and link the files

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
and the JS script within the body tags to ensure your CSS and JS are linked properly.

``` html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <link rel="stylesheet" href="styles.css">
  <title>Document</title>
</head>
<body>

  <script src="app.js"></script>
</body>
</html>
```

## Step 2: HTML

1. Create the following HTML elements, following the nested structure.

- div with the id "container". This div will hold all our elements.
  - h1 with the inner HTML "Dance Chick Revolution".
  - div with the id "game". This div will hold all game elements.
    - div with the id "gameBoard". This div will hold chick and the dancefloor.
    - div with the id "musicBoard". This div will hold the music note arrows.
      - div with the id "topNotes". This div will hold the arrows at the top of the music board.
      - div with the id "moveNotes". This div will hold the arrows at the bottom of the music board, which will move up to the top.
  - button with the id "play" and inner HTML "Play". This button will start the game.
  - div with the id "score". This div will hold the score text.
    - h2 with the id "score-text" and the inner HTML "Score: 0". This div represents the score text.

Your HTML should look like this:

```
  <div id='container'>
    <h1>Dance Chick Revolution</h1>
    <div id='game'>
      <div id='danceBoard'></div>
      <div id='musicBoard'>
        <div id='topNotes'></div>
        <div id='moveNotes'></div>
      </div>
    </div>
    <button id='play'>Play</button>
    <div id='score'>
      <h2 id='score-text'>Score: 0</h2>
    </div>
  </div>
```

2. Add the following within each of the respective divs:

div with id "danceBoard":
```
   <img src="blue-arrow.png" alt="blue arrow" id='arrow-upperleft' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-up' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-upperright' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-left' class='arrow'>
        <img src="img/chick-base.png" alt="chick" id='chick'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-right' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-lowerleft' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-down' class='arrow'>
        <img src="blue-arrow.png" alt="blue arrow" id='arrow-lowerright' class='arrow'>
```

The above code adds arrow elements to the dance board where the chick will be dancing.

div with id "topNotes":
```
<img src="blue-arrow.png" alt="blue arrow" id='toparrow-up' class='toparrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='toparrow-right' class='toparrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='toparrow-down' class='toparrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='toparrow-left' class='toparrow'>
```

The above code adds arrow elements to the music board. These are the arrows at the top of the board that don't move.

div with id "moveNotes":
```
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-up' class='movearrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-right' class='movearrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-down' class='movearrow'>
          <img src="blue-arrow.png" alt="blue arrow" id='movearrow-left' class='movearrow'>
```

The above code adds arrow elements to the music board. These are the arrows at the bottom of the board that will move upwards.







