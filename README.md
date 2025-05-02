# 🧩 Roman Numeral Sudoku (Godot)

A wild twist on classic Sudoku: this puzzle uses **Roman numerals** (`I` to `IX`) and spins constantly as you play. Built in **Godot**, it's both a logic game and a visual challenge.

## 🎮 Features

- 9×9 Sudoku grid using Roman numerals instead of digits
- Classic rules: every row, column, and 3×3 box must have `I` through `IX` exactly once
- Constant board rotation (`12 degrees per second`) for added chaos
- Simple UI: just **click a box and type** your answer directly
- Input validation ensures only valid Roman numerals are accepted
- Win-state detection alerts you when the puzzle is solved
- Exit button to return to main menu (full game on itch.io)

## 🧩 UI & Controls

- Click any cell and type your answer (keyboard input)
- Valid inputs: Roman numerals `I` to `IX` only
- When the puzzle is solved correctly, win feedback is triggered
- Press the exit button to return to the main menu

## 🗂️ Project Structure

- `sodoku.tscn` – main scene containing the board
- `sodoku.gd` – rotates the board and manages scene switching
- `SodokuBoard.gd` – handles board logic, input checking, and win detection
- `global.gd` – stores shared state like number of correct cells
- Cell scripts (e.g., `(0,3).gd`) – control individual input boxes
- `TextEdit.gd` – manages user input and text rendering
  $SodokuBoard.rotation_degrees += 12 * delta
