# CompBox Studio — Nand to Tetris Capstone Project

**Created by:** Prabhat Tewatia  
**Roll No.:** 2501730207  
**Personal Number (K):** 07

## Project overview

CompBox Studio demonstrates a Hack computer screen simulator and a configurable box-drawing program. The dashboard provides a live screen, CPU register monitor, memory address map, keyboard controls, and a box-configuration panel.

## Display number: 07

- **Starting row:** 24
- **Starting column:** 0 (left edge)
- **Height:** 20 rows (rows 24–43)
- **Width:** `16 × ((24 mod 4) + 1) = 16` pixels (1 word)
- **Screen start address:** `16384 + 32 × 24 = 17152`
- **Last screen word:** `16384 + 32 × 43 = 17760`
- **K mod 3:** 0

The 16 × 20 pixel box is drawn while any key is held. The white pixel digits **07** appear centered inside the black box. Releasing the key clears both the box and the number.

## Project structure

- `index.html` — responsive dark-theme simulator dashboard
- `capstone/CPU.hdl`, `Memory.hdl`, `Computer.hdl` — Hack computer hardware description files
- `capstone/Box.asm` — box drawing assembly program, configured to display 07
- `capstone/Box.hack` — assembled machine code
- `capstone/assembler.py` — two-pass Hack assembler
- `tests/` — assembler and box-program test files
- `report/` — project report

## Run the project

Open `index.html` in a modern browser. No build step is required.

To assemble the program again:

```bash
python capstone/assembler.py capstone/Box.asm
```

## Dashboard features

- Live 512 × 256 Hack screen simulation with the number 07 rendered inside the box while a key is held
- CPU registers and program-counter display
- Keyboard press, toggle, pause, step, and reset controls
- RAM / SCREEN / KBD memory address inspection
- Interactive box position and dimension controls
- Magnified screen preview
- Responsive dark navy and violet interface


## Expanded dashboard workspace

- Part A: CPU, Memory and Computer HDL source viewer with official test summary
- Part B: Python assembler source viewer and in-browser assembler demo
- Part C: Box assembly / machine-code viewer and keyboard-state verification table
- Copy-to-clipboard controls for displayed source code
- Responsive layout retaining the existing dark navy and violet theme
