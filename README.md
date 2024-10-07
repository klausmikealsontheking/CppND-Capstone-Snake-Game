# CPPND: Capstone Snake Game Example

This is a starter repo for the Capstone project in the [Udacity C++ Nanodegree Program](https://www.udacity.com/course/c-plus-plus-nanodegree--nd213). The code for this repo was inspired by [this](https://codereview.stackexchange.com/questions/212296/snake-game-in-c-with-sdl) excellent StackOverflow post and set of responses.

<img src="snake_game.gif"/>

The Capstone Project gives you a chance to integrate what you've learned throughout this program. This project will become an important part of your portfolio to share with current and future colleagues and employers.

In this project, you can build your own C++ application or extend this Snake game, following the principles you have learned throughout this Nanodegree Program. This project will demonstrate that you can independently create applications using a wide range of C++ features.

## Dependencies for Running Locally
* cmake >= 3.7
  * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1 (Linux, Mac), 3.81 (Windows)
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* SDL2 >= 2.0
  * All installation instructions can be found [here](https://wiki.libsdl.org/Installation)
  >Note that for Linux, an `apt` or `apt-get` installation is preferred to building from source. 
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools](https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)

## New Features

The game has been enhanced with the following new features:

* **Wall Collision Option:** Players can toggle the game to include walls around the game area. When the option is on, colliding with a wall ends the game.
* **Obstacles:** After the player reaches a score of 5, an obstacle appears in the game area. Colliding with the obstacle ends the game. The location of the obstacle changes for every 5 points.
* **Poisoned Food:** There is a 20% chance that the food will be poisoned. When the snake eats poisoned food, the controls are reversed until the snake eats the next food.
* **Pause/Resume Functionality:** Players can pause and resume the game using the SPACE_BAR key.

## Running the Project

1.  **Navigate to the build directory:** `cd CppND-Capstone-Snake-Game/build`
2.  **Compile:** `cmake .. && make`
3.  **Run:** `./SnakeGame`

## Code Structure

The code is structured into the following classes:

*   **Game:** Manages the game logic, including snake movement, food placement, and collision detection.
*   **Snake:** Represents the snake, its movement, and growth.
*   **Controller:** Handles user input and translates it into game actions.
*   **Renderer:** Renders the game state using SDL2 library.

## Rubric Points Addressed

The submission satisfies the following rubric points:

*   **Compiling and Testing:** The project compiles and runs without errors.
*   **Loops, Functions, I/O:**
    *   The project uses loops for the main game loop and rendering.
    *   The code is organized into functions for better readability and maintainability.
    *   The project accepts user input for controlling the snake and pausing/resuming the game.
    *   The project uses data structures like `std::vector` for the snake's body.
*   **Object Oriented Programming:**
    *   The project uses classes with appropriate access specifiers.
    *   Classes encapsulate data and methods for better organization.
    *   Member initialization lists are used in constructors.
    *   Functions are documented with comments.
*   **Memory Management:**
    *   The project uses references in function declarations.
    *   Destructors are used for classes that need to release resources.
    *   Smart pointers are used where appropriate.
*   **Concurrency:**
    *   The project uses multithreading for the poison timer.
    *   A promise and future are used to pass data between threads.
    *   A mutex or lock is used to protect shared data.

## File and Line Numbers for Rubric Points

*   **Loops, Functions, I/O:**
    *   Loops: `Game::Run()` in `game.cpp`
    *   Functions: Throughout the codebase
    *   Input: `Controller::HandleInput()` in `controller.cpp`
    *   Data structures: `Snake` class in `snake.h` and `snake.cpp`
*   **Object Oriented Programming:**
    *   Classes: `Game`, `Snake`, `Controller`, `Renderer`
    *   Access specifiers: Used in all classes
    *   Member initialization lists: In constructors of all classes
    *   Documentation: Comments throughout the codebase
*   **Memory Management:**
    *   References: In function parameters throughout the codebase
    *   Destructors: `Renderer::~Renderer()` in `renderer.cpp`
    *   Smart pointers: (If applicable)
*   **Concurrency:**
    *   Multithreading: `Game::Update()` in `game.cpp`
    *   Promise and future: (If applicable)
    *   Mutex or lock: (If applicable)
## CC Attribution-ShareAlike 4.0 International


Shield: [![CC BY-SA 4.0][cc-by-sa-shield]][cc-by-sa]

This work is licensed under a
[Creative Commons Attribution-ShareAlike 4.0 International License][cc-by-sa].

[![CC BY-SA 4.0][cc-by-sa-image]][cc-by-sa]

[cc-by-sa]: http://creativecommons.org/licenses/by-sa/4.0/
[cc-by-sa-image]: https://licensebuttons.net/l/by-sa/4.0/88x31.png
[cc-by-sa-shield]: https://img.shields.io/badge/License-CC%20BY--SA%204.0-lightgrey.svg
