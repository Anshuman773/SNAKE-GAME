


 Snake Game

 Introduction
This project is a simple implementation of the classic Snake game in C. The snake moves around the screen, eating fruit and growing longer, while avoiding collisions with the walls or itself.

 Features
- Dynamic Snake Movement: The snake moves continuously in the direction specified by the user.
- Fruit Generation: Fruits appear at random positions on the board, and eating a fruit increases the snake's length and score.
- Collision Detection: The game ends when the snake collides with the walls or itself.
- Score Display: The player's score is displayed on the screen, and the game can be exited by pressing 'X'.
- Memory Consumption Display: The game displays the memory consumed by the snake's nodes.

 Code Overview
 Structure Definitions
- Node: A struct representing a segment of the snake, with `x` and `y` coordinates and a pointer to the next segment.

 Global Variables
- `height`, `width`: Dimensions of the game board.
- `gameover`, `score`: Flags for game state and player score.
- `fruitx`, `fruity`: Coordinates of the current fruit.
- `direction`: Current direction of the snake's movement.
- `head`: Pointer to the head of the snake (linked list).

 Function Definitions
 `void setup()`
Initializes the game state, including the snake's initial position and the first fruit's location.

 `void generateFruit()`
Generates a new fruit at a random location on the board, avoiding the boundaries.

 `void draw()`
Clears the screen and redraws the game board, including the snake, fruit, and boundaries. Displays the current score and instructions to quit the game.

 `void input()`
Reads user input to change the snake's direction or exit the game. Ensures the snake cannot reverse direction directly.

 `void logic()`
Handles the game logic, including:
- Moving the snake in the current direction by creating a new head node and updating the linked list.
- Checking if the snake has eaten a fruit and growing the snake if it has.
- Removing the tail node if the snake hasn't eaten a fruit.
- Checking for collisions with the walls or itself, setting `gameover` if a collision occurs.

 `void space()`
Displays the size of each node and the total memory consumed by the snake's nodes.

 Main Function
Initializes the game and enters the main game loop, which repeatedly calls the `draw`, `input`, `logic`, and `space` functions, with a delay between iterations. Frees allocated memory before exiting.

 Detailed Logic
1. Setup: 
   - Initialize the snake with a single node at the center of the board.
   - Generate the first fruit at a random location.
   
2. Draw:
   - Clear the screen.
   - Draw the boundaries, snake, and fruit on the board.
   - Display the score and exit instructions.

3. Input:
   - Detect user key presses to change the direction of the snake or exit the game.
   - Prevent the snake from reversing direction directly.

4. Logic:
   - Move the snake by creating a new head node in the direction of movement and updating the linked list.
   - Check if the snake has eaten a fruit, increase the score and generate a new fruit if true.
   - Remove the tail node if the snake hasn't eaten a fruit.
   - Check for collisions with the walls or itself, setting `gameover` if a collision occurs.

5. Memory Consumption Display:
   - Display the memory consumed by the snake's nodes during each game loop iteration.

6. Game Loop:
   - Continuously execute the `draw`, `input`, `logic`, and `space` functions until `gameover` is set.
   - Introduce a delay between iterations to control the game's speed.

This project demonstrates fundamental concepts of dynamic memory allocation, linked lists, and game development in C.

