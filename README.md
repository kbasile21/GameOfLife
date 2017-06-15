# GameOfLife
#
# The javascript is part of the index.html file to make the project contain as few files as possible. 
# The only other file needed is the style.css file, which is linked in the index file.
#
# The index loads the initial game board upon opening in a web browser.
# 'New game' refreshes the page giving the user a new game board and clearing the page.
# 'Play' loads the next iteration of the game board, calculating the outcome.
# The user is to click 'Play' until the game is either stuck in a stalemate or every spot on the board is deemed 'dead'.
#
#
# I chose to create a multidimensional array for the game board because I felt it was appropriate in this solution, and the two key values used to reference a spot in the MD array help me visualize the game board. Key 1 was row and key 2 was column, so picturing the game board array felt easier like reading a graph. Next, I chose to make each spot on the board contain an object, called a 'square'. This object contained its current value, new value, and position on the board. To determine if the square was to live, die, or remain the same, I looped through the MD array checking each individual square object. This algorithm works by receiving a square object, checking all of its neighbors on the game board, and returning its new state given the 'rules' of the game. To elaborate, finding a square's neighbors is equivalent to eight or less combinations of the key pair + or - 1. This 'new state' is stored simultaneously in a new state property with the current state so it does not interfere with the calculations that still need to be done on current state squares. Once all squares on the board have their outcomes determined, the 'new state' is written over the current state property. Now, when the next iteration of the board needs to be calculated it will use the new state and so forth. Finally, if all squares have 'died' you are no longer given the option to continue the current game. You must start with a new board.   
