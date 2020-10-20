# Snake Coffee Talk Outline

1. What is the Canvas API?
    - JavaScript system built around the HTML5 canvas element
    - Allows for drawing 2D and 3D objects quickly in the browser without the need for Flash or other libraries
    - Has built in functions for drawing text, shapes, defining colors, et cetera
    - Has a ton of advanced features that we won't get into today.

2. How is it used at Synthesis?
    - The JavaScript charting library that Kraken is being built off of, ChartJS, utilizes the Canvas API to build charts
    - This gives us direct control over the chart that ChartJS builds - allowing us to draw custom objects or manipulate the final chart. An example for people who have used it is the recent Blackrock chart project - the legend that project uses is a custom plugin created and drawn on the chart using the Canvas API
    - Basic knowledge of the Canvas API and how ChartJS uses it allows us to offload most of the heavy lifting in chart rendering (taking datasets and creating a chart out of them) to ChartJS while maintaining control over the final product

3. Snake Game Overview
	- To practice using the Canvas API, I built the classic "Snake" game in JavaScript/HTML/CSS 
	- No libraries, and around 440 lines of total code including HTML and CSS for the page, coming out at 21.3 KB for the entire game file (uncompressed and unminified so further reductions are very possible).
	- For the uninitiated: you control a "snake" that eats food pieces to both grow in size and add to the score for the game.
	- the .html file includes: the document and CSS, all javascript to run the game, basic state management ("initial" state vs. "in game" state vs. "game over" state, plus a current and high score system), game control properties like speed and color, and more.

4. Quick Demo

5. Code Overview
	- Properties overview (global variables, canvas definition)
	- Starting the game (setupAndPlay(), play())
	- Drawing the snake (drawSnake(), drawPiece())
	- Moving the snake (moveSnake())
	- Game over state and collision detection (moveSnake() calling isGameOver(), doPiecesOverlap())
	- Changing direction (checkDirection(), direction queue, arrow keys)
	- Food system (checkFood(), consumeFood(), buildFood(), drawFood())

6. Future Enhancements
    - Make mobile friendly by changing sizes from static dimensions to responsive ones
    - Allow for customizing game during runtime (raising or lowering static speed, allowing for velocity to increase when current score does, colors, etc.)
    - Improving canvas performance (layering canvas elements to prevent having to redraw background using clear() every game cycle)