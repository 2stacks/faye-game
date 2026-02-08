# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Purpose

This project was created as a fun demonstration for an 11-year-old who loves video games, showing how easy it is to use AI-assisted coding to create games and applications. The goal is to build simple, impressive browser games together — keeping things accessible, fun, and visually polished. Games should be easy to understand and enjoyable to play.

## Project Overview

This is a collection of browser-based games built as single-file HTML/CSS/JavaScript applications. No build tools, bundlers, or package managers are used.

## Games

- **flappy.html** — "Flappy Faye", a Flappy Bird clone with an animated bird, scrolling pipes, clouds, score tracking, and high score persistence.

## Running Games

Open any `.html` file directly in a browser:
```
xdg-open <game>.html
```

## Architecture

Each game is a self-contained single HTML file that includes inline CSS and JavaScript. Games use the HTML5 Canvas API for rendering with `requestAnimationFrame` for the game loop. No external dependencies or frameworks.

### Game Structure Pattern

Games follow this structure:
- **Constants** at the top for tuning (gravity, speed, sizes)
- **Game state** managed in plain variables, reset via an `init()` function
- **Separate update/draw functions** called each frame in a `gameLoop()`
- **Input handling** via DOM event listeners (keyboard, mouse, touch)
- **Local storage** for persisting high scores across sessions
