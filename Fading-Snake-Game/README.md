# 🐍 Fading Snake Game

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

## 🎮 How It Works

The game runs in an animation loop controlled by **requestAnimationFrame**, ensuring smooth movements. Below is a breakdown of the key functions that drive the game logic.

---

## 🛠️ Key Functions Explained

### 1️⃣ `main(timestamp)`

This is the **game loop** function that keeps updating the game state.

- It calculates the time elapsed since the last frame.
- Determines if it's time to move the snake forward.
- Calls `stepAndTransition(percentageOfStep)` to animate the snake's movement.

**🔧 Visual Representation:**

```plaintext
[ Frame 1 ] -> [ Frame 2 ] -> [ Frame 3 ] -> ...
    🟩        🟩🟩        🟩🟩🟩  (Snake Grows & Moves)
```

---

### 2️⃣ `stepAndTransition(percentageOfStep)`

Handles **both** stepping forward and transitioning between frames.

- Determines how far the snake has progressed in the current step.
- Calls `transition(percentageOfStep)` to apply fading and movement effects.

**🎥 Visual:**

```plaintext
(50% step) -> 🟩🟩🟩  (fading starts)
(100% step) -> 🟩🟩  (previous part fades out)
```

---

### 3️⃣ `transition(percentageOfStep)`

Applies **smoothing effects** to movement and opacity changes.

- Uses `percentageOfStep` to determine the snake's fade level.
- Creates smooth animations instead of abrupt movements.

**🎨 Visual Effect:**

```plaintext
█ █ █ → █ ░ █ → █ ░ ░ (Fading Effect)
```

---

### 4️⃣ `getNextPosition()`

Calculates the **next position** of the snake based on its current direction.

- Prevents moving backward to avoid collisions.
- Ensures the snake follows a logical path.

**📍 Example Path Calculation:**

```plaintext
⬆️  Move Up  → New Position (x, y - 1)
➡️  Move Right → New Position (x + 1, y)
⬇️  Move Down  → New Position (x, y + 1)
⬅️  Move Left → New Position (x - 1, y)
```

---

### 5️⃣ `addNewApple()`

Adds a new apple randomly on the grid.

- Ensures it does not appear inside the snake's body.
- Increases the snake's length upon consumption.

**🍏 Example Grid with Apple Placement:**

```plaintext
.  .  .  🍏  .  .
.  🟩  🟩  🟩  .  .
.  .  .  .  .  .
```

---

## 🚀 Features

✅ **Smooth fading animation** for the snake.
✅ **Dynamic apple placement** to keep gameplay interesting.
✅ **Frame-by-frame transitions** for fluid movement.
✅ **Optimized for performance** with requestAnimationFrame.

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

<img src="./Assets/game pc.png" alt="Alt text" width="200" height="100">
<img src="./Assets/game mobile.jpg" alt="Alt text" width="100" height="200">

## 🏗️ Installation

1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/fading-snake-game.git
   ```
2. Open `index.html` in a browser.
3. Enjoy the game!

## 🏆 Contribute

Feel free to fork this project, submit pull requests, or suggest improvements!

📌 **Happy Coding! 🎉**
