# 🏓 Pong Game - JavaScript

![Pong Game Screenshot](https://github.com/user-attachments/assets/5cad7513-5d07-41ab-b701-81fb9773c782)

A classic Pong game built with vanilla JavaScript, HTML5 Canvas, and CSS. This implementation features smooth gameplay, responsive controls, and competitive scoring for two players.

## 🎮 Features

- **Two-player local multiplayer** (keyboard controls)
- **Real-time score tracking**
- **Dynamic ball physics** with speed acceleration
- **Responsive game board**
- **Reset game functionality**
- **Clean, minimalist design**

## 🚀 Getting Started

1. Clone the repository:
```bash
git clone https://github.com/your-username/pong-game.git
```
2. Open index.html in your browser  
3. Play the game:  
- Player 1: W (up) / S (down)  
- Player 2: Arrow Up / Arrow Down

  ## 🛠️ Technical Implementation
**Core Components**
```
// Game board setup
const gameBoard = document.querySelector("#gameBoard");
const ctx = gameBoard.getContext("2d");
const gameWidth = gameBoard.width;
const gameHeight = gameBoard.height;
```

**Game Loop**
```
function nextTick() {
  intervalID = setTimeout(() => {
    clearBoard();
    drawPaddles();
    moveBall();
    drawBall(ballX, ballY);
    checkCollision();
    nextTick();
  }, 10)
}
```

**Collision System**
```
function checkCollision() {
  // Paddle collision
  if(ballX <= (paddle1.x + paddle1.width + ballRadius)) {
    if(ballY > paddle1.y && ballY < paddle1.y + paddle1.height) {
      ballXDirection *= -1;
      ballSpeed += 0.5;
    }
  }
  // Wall collision
  if(ballY <= 0 + ballRadius) {
    ballYDirection *= -1;
  }
}
```

## 📂 Project Structure

pong-game/  
├── index.html       # Main HTML file  
├── style.css       # CSS styles  
├── script.js       # JavaScript game logic  
├── assets/         # Game assets  
└── README.md       # This file  

## 📝 Key Features

1. Responsive Controls:  
Smooth paddle movement with keyboard inputs  
Boundary checking to keep paddles on screen  
2. Game Physics:  
Realistic ball trajectory  
Speed increases with each paddle hit  
Accurate angle calculation on paddle contact  
3. Game State Management:  
Score tracking for both players  
Ball reset after scoring  
Game reset functionality  

## 👩💻 Author
**Munique Feitoza**  
GitHub: [Munique-Feitoza](https://github.com/Munique-Feitoza)  
LinkedIn: [Munique Feitoza](https://www.linkedin.com/in/munique-feitoza-77034b231/)  

## 📜 License
This project is licensed under the MIT License - see the LICENSE file for details.[

---

⭐ Feel free to star the repository if you like this project!

