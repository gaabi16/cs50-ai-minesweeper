# CS50 - Introduction to AI with Python

## Minesweeper AI

This project implements an AI that can play the classic game of **Minesweeper** using logical reasoning. The AI uses a knowledge base of sentences to deduce which cells are safe and which contain mines.

### Features

- Represents the Minesweeper board as a grid of cells.  
- Tracks which cells are **safe**, which are **mines**, and which moves have been made.  
- Uses logical inference to update knowledge about the board.  
- Can make **safe moves** based on its knowledge.  
- Can make **random moves** when no safe moves are known.  

### How the AI Works

1. **Knowledge Representation**  
   - A `Sentence` represents a set of cells and the number of mines among them.  
   - The AI maintains a knowledge base of these sentences and updates it as the game progresses.

2. **Updating Knowledge**  
   - When a safe cell is revealed, the AI:
     1. Marks the cell as a move made.  
     2. Marks the cell as safe.  
     3. Adds a new sentence to the knowledge base based on the number of neighboring mines.  
     4. Marks additional cells as safe or as mines if they can be deduced.  
     5. Adds new inferred sentences to the knowledge base.

3. **Making Moves**  
   - `make_safe_move()`: Returns a move that is guaranteed to be safe.  
   - `make_random_move()`: Returns a random move among cells that are not known to be mines and have not been played yet.  

### Running the Project

1. Clone this repository.  
2. Navigate to the project directory.  
3. Install the required Python package (`pygame`) if you don’t already have it:

```bash
pip3 install -r requirements.txt
```
4. Run the file:
```bash
python3 runner.py
```
5. The AI will play a game of Minesweeper, displaying the moves it makes and the state of the board.

## Note

This project is part of the **CS50 - Introduction to AI with Python** course.