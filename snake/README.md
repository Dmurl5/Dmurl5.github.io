# Snake Game - Overview and Purpose

### What is the Canvas API?

1. JavaScript system built around the HTML5 canvas element
2. Allows for drawing 2D and 3D objects quickly in the browser without the need for Flash or other libraries
3. Has built in functions for drawing text, shapes, defining colors, et cetera
4. Has a ton of advanced features that we won't get into today.
5. Cool 3D (WebGL) example: https://webglfundamentals.org/webgl/background.html 

### Why is it important?

1. The JavaScript charting library that we're beginning to use, ChartJS, utilizes the Canvas API to build charts
2. This gives us direct control over the chart that ChartJS builds - allowing us to draw custom objects or manipulate the final chart. An example for people who have used it is the recent Blackrock chart project - the legend that project uses is a custom plugin created and drawn on the chart using the Canvas API
3. Basic knowledge of the Canvas API and how ChartJS uses it allows us to offload most of the heavy lifting in chart rendering (taking datasets and creating a chart out of them) to ChartJS while maintaining control over the final product

### Snake Game Overview

1. To practice using the Canvas API, I built the classic "Snake" game in JavaScript/HTML/CSS 
2. No libraries, and around 430 lines of total code including HTML and CSS for the page. The unminified version comes out at 21.3 KB, while the minified version (white spaces, line breaks, and comments removed) clocks it at only 7.15 KB - pretty good for a fully functioning game!
3. For the uninitiated: you control a "snake" that eats food pieces to both grow in size and add to the score for the game.
4. the .html file includes: the HTML document, associated CSS, all javascript to run the game, basic state management ("initial" state vs. "in game" state vs. "game over" state, plus a current and high score system), game control properties like speed and color, and more.

### Quick Demo and Code Overview

1. Properties overview (global variables, canvas definition)
2. Starting the game and game cycles (setup(), tick(), play())
3. Drawing the snake (drawSnake(), drawPiece())
4. Moving the snake (moveSnake())
5. Game over state and collision detection (moveSnake() calling isGameOver(), doPiecesOverlap())
6. Changing direction (checkDirection(), direction queue, arrow keys)
7. Food system (checkFood(), consumeFood(), buildFood(), drawFood())

### Future Enhancements

1. Make mobile friendly by changing sizes from static dimensions to responsive ones
2. Allow for customizing game during runtime (raising or lowering static speed, allowing for velocity to increase when current score does, colors, etc.)
3. Improving canvas performance (layering canvas elements to prevent having to redraw background using clear() every game cycle)