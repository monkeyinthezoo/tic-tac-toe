# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project

A browser-based two-player Tic Tac Toe game delivered as a single self-contained HTML file (`tictactoe.html`). No build step, no dependencies, no package manager.

## Running

Open `tictactoe.html` directly in a browser:

```bash
open tictactoe.html
```

## Architecture

Everything lives in `tictactoe.html` in three inline sections:

- **`<style>`** — all layout and theming (CSS grid board, cell states, score display)
- **`<div id="board">`** — 9 `.cell` elements with `data-i` indices 0–8
- **`<script>`** — game logic: `board[]` array, `WINS` constant (all 8 winning lines), click handler, `checkWinner()`, score tracking across games

Game state is held in three module-level variables: `board` (array), `current` (player), and `over` (boolean). `init()` resets all three and clears the DOM.

## Git & GitHub

- Remote: `https://github.com/monkeyinthezoo/tic-tac-toe` (origin/main)
- After every change: commit with a descriptive message and push to origin
