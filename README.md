# Stone Automata

A rule-based cellular automata game where each cell can have its own unique rules for moving stones.

## What is this?

A grid where each cell holds stones. Every cell has a rule that decides what to do with its stones. The rules run all at the same time, and stones move to new cells based on those rules.

## How to Play

1. Select cells by clicking or dragging (ctrl+click for multiple)
2. Set up stones using number keys (0-9), arrow keys (up/down), or Backspace to clear
3. Write rules in the editor panel
4. Press `.` (period) while in the editor to apply rules to selected cells
5. Press Play to watch the stones move

## Controls

- **Mouse**: Click or drag to select cells
- **Ctrl+Click**: Toggle individual cell selection
- **Arrow Up/Down**: Increase/decrease stones in selected cells
- **Number keys (0-9)**: Set exact stone count
- **Backspace/Delete**: Clear stones from selected cells
- **Shift+C**: Copy selected cells to internal clipboard
- **Shift+X**: Cut selected cells (copy and reset to default)
- **Shift+V**: Paste from internal clipboard at selected cell
- **Shift+Arrows**: Move single-cell selection
- **`.` (period)**: Apply rule while in editor

## Rules Syntax

Rules are written in a Python-like syntax:

**Simple commands:**
- `send [amount] [direction]` - Move stones in a direction
- `wait` - Do nothing (stones stay in place)

**Directions:** `up`, `down`, `left`, `right`

**Examples:**
# Single line

if stones == 1: send 1 up

# Multi-line with conditions

if stones == 2:  
send 1 up  
send 1 down  
elif stones > 2 and stones < 6:  
send stones right  
else:  
wait

**Operators:** `==`, `!=`, `<`, `>`, `<=`, `>=`, `%` (modulo), `and`, `or`, `not`

## Import/Export

- **Export**: Copies the board as text to your system clipboard
- **Import**: Reads board data from your system clipboard and restores it

## Example Board: Adder

See `adder_board.txt` for an example board that adds two numbers.

## License

MIT License - feel free to fork and modify!

Created by Carson B with DeepSeek coding assistance.