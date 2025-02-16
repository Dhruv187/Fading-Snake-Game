# Fading Snake Game

A unique twist on the classic Snake game, where the snake gradually fades away over time! Can you keep it alive and achieve the highest score before it disappears?

## 🚀 Features

- **Fading Mechanic:** The snake gradually loses opacity, adding a unique challenge.
- **Hard Mode:** A more difficult version with a faster fading effect.
- **Mobile Support:** Play using swipe gestures on touch devices.
- **Sound Effects:** Enjoy immersive audio feedback for actions like eating and collisions.

## 🎮 How to Play

1. Use arrow keys (or swipe on mobile) to control the snake's direction.
2. Eat the apple to increase your score and restore the snake's visibility.
3. Avoid hitting walls or biting yourself.
4. Your snake will fade over time—keep eating to survive!

## 🛠️ Important Functions

### 1. `resetGame()`

Resets the game state, initializes the snake, and places an apple.

### 2. `startGame()`

Begins the game loop using `requestAnimationFrame`.

### 3. `main(timestamp)`

The core game loop that handles movement, fading, and collision detection.

### 4. `handleTouchStart(event) & handleTouchMove(event)`

Enable swipe gestures for mobile control.

### 5. `toggleButton Event Listener`

Switches between Easy and Hard mode dynamically.

## 🕹️ Controls

| Action           | Key / Gesture             |
| ---------------- | ------------------------- |
| Move Left        | Left Arrow / Swipe Left   |
| Move Right       | Right Arrow / Swipe Right |
| Move Up          | Up Arrow / Swipe Up       |
| Move Down        | Down Arrow / Swipe Down   |
| Restart Game     | Spacebar / Start Button   |
| Toggle Hard Mode | H (Hard) / E (Easy)       |

## 📸 Screenshots

_Add some screenshots here to showcase the game!_

## 🏗️ Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/fading-snake-game.git
   ```
2. Open `index.html` in a browser.
3. Enjoy the game!

## 🏆 Contribute

Feel free to fork this project, submit pull requests, or suggest improvements!
