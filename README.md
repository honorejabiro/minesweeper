# 🧠 Minesweeper AI (CS50 AI)

This project is a logic-based AI implementation of the classic **Minesweeper** game, developed in Python. The AI uses **propositional logic**, **constraint propagation**, and **inference** to determine safe moves and identify mines — similar to how a human logically plays Minesweeper.

This project was created as part of [CS50’s Introduction to Artificial Intelligence with Python](https://cs50.harvard.edu/ai/).

---

## 🎮 Project Overview

The project includes:
- A game environment (`Minesweeper`) that randomly places mines on a board.
- A logical AI agent (`MinesweeperAI`) that reasons through the board to identify safe cells and mines using knowledge representation.
- A `Sentence` class to represent logical statements about cell groups and their mine counts.

---

## How the AI Works

When the AI uncovers a cell:
1. It records the number of surrounding mines.
2. It creates a `Sentence` describing unknown neighbors and the count.
3. It adds this to its **knowledge base**.
4. It continually infers:
   - Which neighboring cells are definitely **mines**.
   - Which are definitely **safe**.
   - And derives new logical **sentences** from subsets of existing ones.

The AI chooses its next move using:
- `make_safe_move()` → chooses a move known to be safe.
- `make_random_move()` → makes a random move if no safe one is known.

---

## Concepts Used

- **Propositional Logic**
- **Knowledge Representation**
- **Inference Rules**
- **Constraint Satisfaction**
- **Subset-based Inference**

---

## 📁 File Structure

