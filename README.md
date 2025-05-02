# 🧩 Roman Numeral Sudoku (Godot)

A 9x9 Sudoku game using **Roman numerals (I–IX)** instead of digits. Built in **Godot**, this version adds chaos: the board rotates continuously as you play.

## 🎮 Features

- ✅ 9×9 classic Sudoku layout using Roman numerals `I` through `IX`
- 🔄 Constant rotation animation (`12 degrees/second`) for challenge and flair
- 🎨 Two-tone coloring for visual contrast
- 💡 Menu navigation via `Exit` button (`res://menu.tscn`)
- 📜 Built with GDScript and Godot's Node2D structure

## 📁 Project Structure

- `sudoku.gd` – main script for the Sudoku scene  
  - `_process()` spins the board  
  - `_on_exit_pressed()` handles exit button  
- `SudokuBoard` – contains the 81 cells and board logic  
- Roman numerals rendered in cells, likely via `Label` nodes

## 🔧 How It Works

- On each frame, the Sudoku board rotates via:  
  ```gdscript
  $SudokuBoard.rotation_degrees += 12 * delta
