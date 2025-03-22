## README for Packman Game

### Overview

This repository contains the source code and assets for a classic Pac-Man game implemented using Python and the Pygame library. The game features a maze-like board, multiple ghosts with distinct behaviors, power-ups, and various gameplay mechanics inspired by the original Pac-Man arcade game.

### Features

1. **Gameplay Mechanics**
   - **Player Control**: Navigate the player character (Pac-Man) through the maze using arrow keys.
   - **Ghost Behavior**:
     - **Blinky**: Chases the player directly.
     - **Pinky**: Pursues the player but aims to predict their movement.
     - **Inky**: Uses a combination of the player's position and Blinky's position to determine its path.
     - **Clyde**: Prefers to stay away from the player unless it is scared.
   - **Power-Ups**: Eating a large dot (power-up) temporarily turns the ghosts blue, allowing the player to eat them for points.
   - **Lives System**: The player has three lives. Losing all lives ends the game.
   - **Victory Condition**: Clearing all dots in the maze wins the game.

2. **Graphics and Assets**
   - **Player Character**: Animated sprites for different directions (up, down, left, right).
   - **Ghosts**: Distinct images for each ghost (Blinky, Pinky, Inky, Clyde), including their scared and dead states.
   - **Maze Design**: A detailed maze layout defined in a 2D array (`boards`).

3. **Scoring System**
   - Points are awarded for eating dots and ghosts.
   - Scoring multiplies based on how many ghosts have been eaten consecutively during a power-up.

4. **Game States**
   - **Game Over**: Displays a "Game Over" screen when the player loses all lives.
   - **Victory**: Displays a "Victory" screen when the player clears all dots.
   - **Restart**: Allows the player to restart the game after losing or winning.

### Directory Structure

```
PACKMAN/
├── assets/
│   ├── ghost_images/
│   │   ├── blue.png
│   │   ├── dead.png
│   │   ├── orange.png
│   │   ├── pink.png
│   │   ├── powerup.png
│   │   └── red.png
│   └── player_images/
│       ├── 1.png
│       ├── 2.png
│       ├── 3.png
│       └── 4.png
├── __pycache__/
├── board.py
├── packman.py
├── pacman_pieces.png
└── pacmanlvl1.jpg
```

- **assets/**: Contains all image files used in the game.
  - **ghost_images/**: Images for the ghosts (Blinky, Pinky, Inky, Clyde, etc.).
  - **player_images/**: Animated sprites for the player character.
- **board.py**: Defines the maze layout as a 2D array.
- **packman.py**: Main game file containing the logic for the game loop, player movement, ghost AI, collision detection, and rendering.
- **pacman_pieces.png**: Image file for rendering the maze pieces (dots, lines, etc.).
- **pacmanlvl1.jpg**: Optional image file for visualizing the maze layout.

### How to Run the Game

1. **Prerequisites**
   - Python 3.x installed.
   - Pygame library installed. Install it using:
     ```bash
     pip install pygame
     ```

2. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/packman.git
   cd packman
   ```

3. **Run the Game**
   ```bash
   python packman.py
   ```

4. **Controls**
   - Use the arrow keys to move the player character.
   - Press the space bar to restart the game after losing or winning.

### Code Highlights

1. **Maze Representation**
   - The maze is represented as a 2D array (`boards`) where each cell contains an integer representing different elements:
     - `0`: Empty black rectangle.
     - `1`: Small dot.
     - `2`: Large dot (power-up).
     - `3`: Vertical line.
     - `4`: Horizontal line.
     - `5-8`: Corners and intersections.
     - `9`: Gate (used for ghost movements).

2. **Ghost AI**
   - Each ghost has a unique behavior:
     - **Blinky**: Directly chases the player.
     - **Pinky**: Predicts the player's movement and moves towards that location.
     - **Inky**: Combines the player's position and Blinky's position to determine its path.
     - **Clyde**: Avoids the player unless it is scared.

3. **Collision Detection**
   - Detects collisions between the player and ghosts, dots, and power-ups.
   - Implements logic to handle power-ups, such as turning ghosts blue and allowing the player to eat them.

4. **Animation**
   - Player character animations are achieved by cycling through sprite images.
   - Ghosts change their appearance when scared or defeated.

### Future Enhancements

1. **Additional Levels**: Implement more levels with varying maze designs.
2. **Sound Effects**: Add sound effects for eating dots, ghosts, and power-ups.
3. **High Scores**: Track and display high scores.
4. **Menu Screen**: Add a start menu and options menu.
5. **AI Improvements**: Refine ghost AI for more challenging gameplay.

### Credits

- **Assets**: All images and sounds used in this project are either created by the developer or sourced from free resources.
- **Inspiration**: Classic Pac-Man arcade game.

### License

This project is open-source and released under the MIT License. Feel free to use, modify, and distribute the code as per the terms of the license.

---

This README provides a comprehensive overview of the Pac-Man game, its features, structure, and how to run it. It serves as a guide for both users and developers interested in exploring or contributing to the project.
