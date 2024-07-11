# Tic-Tac-Toe Game
This project is a simple implementation of the Tic-Tac-Toe game using React. The game allows two players to take turns marking spaces on a 3x3 grid, aiming to align three of their marks horizontally, vertically, or diagonally to win.

## Features
- Two-player gameplay
- Interactive game board
- Display of the next player
- Display of the game winner
- History of moves with the ability to jump to a previous move

## Components

### 1. Square
The `Square` component represents a single square on the Tic-Tac-Toe board. It takes two props:
- `value`: The current value of the square ('X', 'O', or null).
- `onSquareClick`: A function to handle the click event on the square.

### 2. Board
The `Board` component represents the entire Tic-Tac-Toe board and contains the logic for handling player moves. It takes three props:
- `xIsNext`: A boolean indicating if the next player is 'X'.
- `squares`: An array representing the current state of the board.
- `onPlay`: A function to handle the state update when a move is played.

### 3. Game
The `Game` component manages the state of the game, including the history of moves and the current move. It also handles the display of the game's status and the move history. It contains:
- `history`: An array of board states, representing the history of moves.
- `currentMove`: The index of the current move in the history.
- `xIsNext`: A boolean indicating if the next player is 'X'.
- `currentSquares`: The current state of the board.

### 4. calculateWinner
The `calculateWinner` function determines if there is a winner based on the current state of the board. It returns 'X', 'O', or null.

## Getting Started

### Prerequisites
- Node.js and npm installed

### Installation
1. Clone the repository:
   ```sh
   git clone <repository-url>
   cd tic-tac-toe
   ```

2. Install the dependencies:
   ```sh
   npm install
   ```

### Running the Game
1. Start the development server:
   ```sh
   npm start
   ```

2. Open [http://localhost:3000](http://localhost:3000) in your browser to view the game.

### Usage
- Click on a square to make a move.
- The status above the board shows the next player or the winner.
- Use the move history on the right to jump to any previous move.

## Code Structure
- `src/`
  - `index.js`: The entry point of the application.
  - `App.js`: The main component that renders the `Game` component.
  - `Game.js`: Contains the `Square`, `Board`, and `Game` components, and the `calculateWinner` function.
  - `index.css`: Basic styling for the game.
