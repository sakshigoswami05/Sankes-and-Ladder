# Sankes-and-Ladder
# 🎲 Snakes & Ladders

> A classic board game brought to life with **HTML, CSS & JavaScript**.

🎮 [**Play the Game**](https://sakshigoswami05.github.io/Sankes-and-Ladder/) · 💻 [**View Source Code**](https://github.com/sakshigoswami05/Sankes-and-Ladder)

---

## 📖 About

**Snakes & Ladders** is an interactive, browser-based **two-player board game** developed using vanilla **HTML, CSS, and JavaScript**.

The project recreates the traditional Snakes & Ladders experience with a dynamic game board, customizable players, dice-based movement, turn management, snakes, ladders, and automatic winner detection.

The game was built from scratch without using a game engine or frontend framework, focusing on implementing the complete gameplay logic and user interaction using core JavaScript concepts.

---

## ✨ Features

* 🎮 **Two-player gameplay** with turn-based interaction
* 👤 **Custom player names** for a personalized experience
* 🧑 **Player avatar selection**
* 🎲 **Random dice rolling** from 1 to 6
* 🔄 **Automatic turn management**
* ⭐ **Extra turn** when a player rolls a 6
* 🪜 **Ladder mechanics** for moving forward
* 🐍 **Snake mechanics** for moving backward
* 📍 **Dynamic player positioning** on the board
* 🏆 **Automatic winner detection**
* 🎨 **Interactive and visually designed game board**
* 🌐 **Deployed using GitHub Pages**

---

## 🎮 How to Play

1. Enter the names of both players.
2. Select an avatar for each player.
3. The first player rolls the dice.
4. Move the player according to the dice value.
5. If you land on a **ladder**, climb to the corresponding higher position.
6. If you land on a **snake**, move down to its corresponding lower position.
7. Rolling a **6** gives the current player another turn.
8. The first player to reach **100** wins the game.

---

## 🧠 Game Logic

The game is driven entirely by JavaScript and maintains the state of the players throughout the game.

### 🎲 Dice System

A random number between **1 and 6** is generated whenever the active player rolls the dice.

```javascript
let dice = Math.floor(Math.random() * 6) + 1;
```

The generated value determines how many positions the player moves.

---

### 👥 Player Management

The game stores information about each player, including their name and selected avatar.

Player positions are maintained separately so that the game can update each player's location after every dice roll.

The active player's turn is also tracked to ensure that only the correct player can make a move.

---

### 🔄 Turn Management

After each valid move, the turn changes to the other player.

There is one exception:

> **Rolling a 6 gives the same player another turn.**

This logic is handled directly through JavaScript and keeps the gameplay state synchronized with the interface.

---

### 🪜 Ladder System

The game contains predefined ladder positions.

| Start | Destination |
| :---: | :---------: |
|   4   |      36     |
|   28  |      49     |
|   45  |      64     |
|   54  |      92     |

When a player lands on the starting position of a ladder, the game automatically updates their position to the ladder's destination.

For example:

```text
Player lands on 28
        ↓
Ladder detected
        ↓
Player moves to 49
```

---

### 🐍 Snake System

Snake positions are also predefined.

| Start | Destination |
| :---: | :---------: |
|   34  |      8      |
|   40  |      2      |
|   66  |      35     |
|   83  |      59     |
|   95  |      56     |
|   99  |      21     |

When a player lands on a snake's starting position, their position is automatically changed to the corresponding destination.

For example:

```text
Player lands on 95
        ↓
Snake detected
        ↓
Player moves to 56
```

---

### 🏆 Winning Condition

After every movement, the game checks the player's updated position.

If the player reaches:

```text
100
```

the game enters the winning state and announces that player as the winner.

---

## 🏗️ Application Flow

```text
Player Setup
     │
     ▼
Select Player & Avatar
     │
     ▼
     🎲 Roll Dice
     │
     ▼
Calculate New Position
     │
     ▼
Check Snake / Ladder
     │
     ├──── 🐍 Snake ────► Move Down
     │
     ├──── 🪜 Ladder ───► Move Up
     │
     └──── Normal ──────► Stay
     │
     ▼
Check Winner
     │
     ├──── Position = 100 ───► 🏆 Winner
     │
     └──── Otherwise ────────► Next Turn
```

---

## 🛠️ Tech Stack

| Technology       | Purpose                                       |
| ---------------- | --------------------------------------------- |
| **HTML5**        | Structure and game elements                   |
| **CSS3**         | Layout, styling and visual design             |
| **JavaScript**   | Game logic, state management and interactions |
| **Git & GitHub** | Version control and source management         |
| **GitHub Pages** | Deployment                                    |

---

## 🧩 Core Concepts Used

This project demonstrates practical implementation of several frontend and JavaScript concepts:

* **DOM Manipulation**
* **Event Handling**
* **JavaScript Classes & Objects**
* **Arrays**
* **Conditional Statements**
* **Random Number Generation**
* **State Management**
* **Dynamic UI Updates**
* **Turn-Based Logic**
* **Game State Validation**
* **Client-Side Application Development**

---

## 📂 Project Structure

```text
Sankes-and-Ladder/
│
├── index.html          # Game structure
├── style.css           # Styling and layout
├── script.js           # Complete game logic
│
├── imgs/               # Game assets
│   ├── backgrounds
│   ├── dice
│   ├── players
│   ├── snakes
│   └── ladders
│
└── README.md           # Project documentation
```

### `index.html`

Defines the structure of the game interface, including the board, player sections, dice controls and game screens.

### `style.css`

Handles the visual appearance of the application, including the board layout, player interface, backgrounds, positioning and overall styling.

### `script.js`

Contains the core gameplay implementation, including dice generation, player movement, turn handling, snake and ladder detection, position updates and winner detection.

### `imgs/`

Contains the visual assets used by the game, including player images, dice, snakes, ladders and backgrounds.

---

## 🚀 Run Locally

### 1. Clone the repository

```bash
git clone https://github.com/sakshigoswami05/Sankes-and-Ladder.git
```

### 2. Navigate to the project

```bash
cd Sankes-and-Ladder
```

### 3. Run the application

Open `index.html` directly in your browser.

For development, you can also use **Live Server** in VS Code.

---

## 🌐 Live Demo

🎮 [**Play Snakes & Ladders**](https://sakshigoswami05.github.io/Sankes-and-Ladder/)

---

## 🔮 Future Improvements

The project can be extended with several additional features:

* 🤖 **Single-player mode** with an AI opponent
* 🔊 **Sound effects** for dice, snakes, ladders and winning
* ✨ **Smooth player movement animations**
* 📱 **Improved mobile responsiveness**
* 🔄 **Restart / New Game functionality**
* 🏅 **Game statistics and match history**
* 🎨 **Multiple board themes**
* ⏱️ **Game timer**
* 💾 **Local Storage** for saving game progress
* 🌐 **Real-time multiplayer** using WebSockets

---

## 👩‍💻 Author

### Sakshi Goswami

**B.Tech — Information Technology**
**National Institute of Technology, Raipur**

[GitHub](https://github.com/sakshigoswami05)

---

<div align="center">

⭐ **If you enjoyed the game, consider starring the repository!**

🎲 **Have fun playing!**

</div>
