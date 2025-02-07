# DID's chess engine

This project is a simple chess engine with a web interface built using Flask. It integrates **chessboard.js** and **chess.js** for the frontend chessboard logic, while **python-chess** handles the backend chess logic. All chess move calculations are performed server-side using Python.

## Features

- Interactive chessboard using **chessboard.js**
- Chess move validation and game rules handled by **chess.js**
- Backend chess logic powered by **python-chess**
- Flask server to manage game state and communication between frontend and backend
- Supports legal move generation and algebraic notation input

---

## Installation

To run this application on your local machine, follow these steps:

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/DID'SChessEngine.git

```

### 2. Create a Virtual Environment (Optional but Recommended)

```sh
python -m venv venv
source venv/bin/activate  # On macOS/Linux
venv\Scripts\activate  # On Windows
```

### 3. Install Dependencies

```sh
pip install flask
pip install python-chess[uci,gaviota]
```

### 4. Run the Flask Server

```sh
python app.py
```

### 5. Access the Application

Once the server is running, open your web browser and go to:

```
http://127.0.0.1:5000
```

---

## How It Works

### **Frontend**

The frontend utilizes **chessboard.js** and **chess.js**:

- **chessboard.js** provides a visual representation of the chessboard and allows players to move pieces interactively.
- **chess.js** ensures only legal moves are made and keeps track of game state on the client-side.

### **Backend**

The backend is implemented using Flask and **python-chess**:

- **python-chess** is a chess library that provides move generation, validation, and game rules enforcement.
- When a move is made on the frontend, it is sent to the Flask server.
- The server updates the game state, checks for legality, and returns the updated board state to the frontend.

### **Example Code Explanation**

```python
import chess

board = chess.Board()

# Print all legal moves from the initial position
for move in board.legal_moves:
    print(move)

# Play moves using algebraic notation
d.board.push_san("e4")
d.board.push_san("e5")

# Print the board state
print(board)
```

This script:

1. Creates a chessboard instance.
2. Prints all legal moves from the starting position.
3. Plays the moves **e4** and **e5**.
4. Displays the updated board state.

---

## Theory Behind The Chess Engine

### **1. Move Generation**

- The engine generates all possible legal moves using **python-chess**.
- It ensures that illegal moves (such as putting the king in check) are not allowed.

### **2. Game Rules Enforcement**

- The backend ensures rules like check, checkmate, and stalemate are followed.
- It tracks game state changes, including captures and special moves (castling, en passant, promotion).

### **3. Communication Between Frontend and Backend**

- The frontend sends move data to the Flask backend.
- The backend validates the move using **python-chess** and updates the board.
- The new game state is returned to the frontend to update the board.

---

## Future Improvements

- AI opponent using **Stockfish** for move suggestions.
- Multiplayer support with WebSockets.
- Database integration to save game history.
- Enhanced UI/UX with animations.

---

## License

This project is open-source under the MIT License.

---

## Contributing

Feel free to submit issues and pull requests to improve the project!

### Contact

For any questions, reach out to **[rdidhitpatel2002@gmail.com](mailto\:your.email@example.com)**.



