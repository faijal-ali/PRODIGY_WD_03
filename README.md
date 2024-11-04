# PRODIGY_WD_03
This project is a basic implementation of the classic Tic-Tac-Toe game using HTML, CSS, and JavaScript. It offers a clean, interactive user interface where two players can compete by taking turns on a 3x3 grid. The game automatically checks for a winner after each turn and displays a winning message when one player aligns three marks consecutively. Players can also reset or start a new game easily using dedicated buttons.

Features

Two-Player Gameplay: Alternates turns between Player O and Player X.
Automatic Winner Detection: Checks for a win condition (three consecutive marks in a row, column, or diagonal) after each move.
Game Controls:
New Game: Clears the board and allows players to start a fresh game.
Reset: Similar to New Game, resets the board and any game status messages.
Winning Message: Displays a congratulatory message with the winning player’s symbol (O or X).
Disable/Enable Game Boxes: Prevents players from overwriting each other’s moves or continuing after a win.
Code Explanation

Selecting Elements:

boxes: The 9 boxes (cells) on the game board.
reseBtn and newGameBtn: Buttons to reset or start a new game.
msgContainer and msg: Elements to display a message with the game result.

Game Variables:

turnO: Boolean that tracks which player's turn it is (true for Player O, false for Player X).
winPattern: Array of winning patterns based on index positions on the board.
Resetting the Game (resetGame function):

Resets turnO to true (starting with Player O).
Enables all boxes and clears any displayed messages.

Event Listeners:


Each box listens for a click event, marking it with an "O" or "X" depending on turnO.
The clicked box is disabled to prevent overwriting.
After each move, checkWinner is called to see if the game has been won.
Checking for a Winner (checkWinner function):

Iterates through winPattern to compare the values in each potential winning position.
If a match is found, it calls showWinner and disables the remaining boxes.
Displaying the Winner (showWinner function):
Reveals a message showing the winner’s symbol.

Enabling/Disabling Boxes:

disableBoxes: Disables all boxes once a win is detected.
enableBoxes: Re-enables all boxes and clears their content for a new game.
Usage Instructions

Start a New Game: Click on any box to start the game. The first player to play will be Player O.
Take Turns: Players alternate turns by clicking on available boxes.
Win Condition: The game will announce a winner once three consecutive marks are aligned. The game board is disabled after a win.
Reset/New Game: Use the Reset or New Game buttons to clear the board and start over.
