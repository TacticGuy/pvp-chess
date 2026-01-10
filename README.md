# RawChess

A lightweight, client-side chess engine and renderer built with pure web technologies.

RawChess is a high-performance, offline-first implementation of Chess designed for zero-latency gameplay. It runs entirely in the browser, using a custom DOM-based rendering engine and a JavaScript logic layer to handle complex game rules without requiring a backend server.

## Game Development Overview

This project demonstrates how to implement a complex board game state machine using only standard web technologies. It focuses on separating the game logic (Engine) from the view layer (DOM), ensuring a smooth 60fps experience even on low-end devices.

### Key Technical Features

- **Client-Side Move Validation** — The engine internally validates all FIDE chess rules, including edge cases like castling, en passant, and pawn promotion.
- **DOM-Based Rendering** — Instead of using Canvas or WebGL, the board is rendered using efficient DOM manipulation and CSS3 transforms, making the UI fully responsive and accessible.
- **Zero-Latency Hotseat Play** — By removing server-side dependencies, the game provides an instant response loop for local PvP matches.
- **State Management** — The game state is tracked in a centralized JavaScript object, allowing for potential future expansions like move history or FEN string export.

## Tech Stack

- **Engine & Logic** — JavaScript (ES5+)
- **Renderer** — HTML5 / CSS3
- **UI Animations** — CSS Transitions & Sprites
- **Dependencies** — jQuery, jQuery UI
- **Deployment Target** — Static hosting (Vercel, Netlify, GitHub Pages)

## Installation & Setup

RawChess is fully static and requires no build steps, package managers, or backend configuration.

### Local Development

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/rawchess.git
    ```
2. Open `index.html` directly in your browser.

### Deployment

Upload the repository to any static site provider:
- **Vercel/Netlify** — Import the repository and deploy
- **GitHub Pages** — Enable Pages in repository settings

## Implemented Logic

The internal engine handles the complete rule set:

- [x] Movement — Standard moves for King, Queen, Rook, Bishop, Knight, Pawn
- [x] Special Moves — Castling (Kingside/Queenside), En Passant, Promotion
- [x] Game States — Check, Checkmate, Stalemate detection

## Project Structure

```
/
├── css/             # Visual theming and board layout
├── js/
│   ├── game.min.js  # Core engine and move validation logic
│   └── lib/         # External DOM libraries
├── img/             # Sprite sheets for chess pieces
└── index.html       # Main entry point
```
