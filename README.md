Console Lane-Dodge Game (C Project – 1st Year CSE)

Overview

This project is a simple console-based game written in C where the player controls a character moving between three lanes to avoid falling obstacles. The game uses basic keyboard input, ASCII graphics, and loop-based game logic.

The project was originally a simple “obstacle falls, player dodges” setup.
For this assignment, three major improvements were implemented:

A structured Start Menu System

A Game Restart feature

A simple High Score System using file handling

3. How the Original Game Works

The player moves between three lanes using the LEFT and RIGHT arrow keys.

A randomly positioned obstacle falls from top to bottom.

If the obstacle reaches the bottom and stays in the same lane as the player → GAME OVER.

The game uses:

system("cls") to clear the screen

_kbhit() and getch() for input

Sleep() for timing

rand() for obstacle lane selection

4. Features Added (Improvements)
✔ 1. Start Menu System

A menu appears before gameplay begins providing basic options such as:

Start Game

View High Score

Exit

It uses a loop + user input handling (switch or if-else) to navigate between options.

✔ 2. Game Restart Option

The player can restart without closing the program.
This is achieved by:

Wrapping the game loop inside another loop

Resetting variables (player position, step counter, obstacle position)

Returning to the menu after game over or restart request

✔ 3. High Score Storage (File Handling)

The game now stores the player’s highest score using:

A file (e.g., highscore.txt)

fopen(), fprintf(), fscanf() for reading/writing

Score updates only when the current score exceeds the saved high score

This adds persistence — even after closing the program, the high score remains saved.
