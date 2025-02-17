# README - Go Game Implementation in Python

## Project Overview
This project is an implementation of the ancient board game **Go** in Python. The goal is to create a program that allows two players to compete by placing stones on a Go board while following the game's rules. The program is structured using Abstract Data Types (ADTs) to handle the game logic efficiently.

## Game Description
Go is a strategy board game played between two players, one using black stones and the other using white stones. The objective is to **control the largest territory** on the board by surrounding empty intersections. Capturing opponent stones and maintaining liberties for one's own stones are crucial aspects of gameplay.

### Board and Pieces
- The **Goban** (board) is typically **19×19**, but smaller sizes like **13×13** and **9×9** are also supported.
- Players place stones on intersections.
- Stones of the same color that are connected form **chains**.
- Chains must have **liberties** (adjacent empty intersections) to remain on the board.
- The game ends when both players pass their turns consecutively.
- The player with the most territory and captured stones wins.

## Implementation Details
This project defines and implements **three key ADTs**:

### 1. **TAD Intersecao (Intersection)**
- Represents a single point on the board.
- Provides methods to create, retrieve coordinates, and compare intersections.

### 2. **TAD Pedra (Stone)**
- Represents a stone placed by a player.
- Supports white, black, and neutral (empty) stones.

### 3. **TAD Goban (Board)**
- Represents the Go board and stores the positions of stones.
- Handles placement, removal, and capturing of stones.
- Tracks connected chains and their liberties.
- Determines legal and illegal moves (suicide, Ko rule).

## Functions Implemented
The following functions facilitate gameplay and board management:

### Board Management
- `cria_goban_vazio(n)`: Creates an empty board of size `n × n`.
- `coloca_pedra(g, i, p)`: Places a stone `p` on intersection `i`.
- `remove_pedra(g, i)`: Removes a stone from `i`.
- `remove_cadeia(g, t)`: Removes a chain of stones.
- `obtem_territorios(g)`: Identifies controlled territories.

### Game Rules and Logic
- `jogada(g, i, p)`: Executes a move, checking for captures.
- `eh_jogada_legal(g, i, p, l)`: Verifies if a move is legal.
- `calcula_pontos(g)`: Calculates player scores.
- `turno_jogador(g, p, l)`: Manages a player's turn, allowing pass or move.
- `go(n, tb, tp)`: Main game loop, allowing two players to play a full match.

## How to Run the Program
1. Ensure **Python 3** is installed.
2. Run the Python script containing the implementation.
3. The game prompts users to input moves or pass.
4. The game continues until both players pass consecutively.
5. The final board state and scores are displayed.


