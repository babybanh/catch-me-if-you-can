# Catch Me If You Can!

First playable browser-game draft for the student game series.

## Run Locally

```bash
npm install
npm run dev
```

The main tuning file is:

```text
src/gameConfig.js
```

That file controls the square stage size, play area, character sizes, speeds, hitboxes, UI positions, button sizes, joystick zone, z-order, spawn margins, and phase thresholds.

## Current Draft

- Placeholder BunBun, banana, and Aidan shapes.
- Keyboard movement with arrow keys and WASD.
- Floating joystick for mouse/touch.
- Banana collection, score, banana count, hearts, gorilla spawn, hit invincibility, game over, and restart.
- Debug panel toggled with the `D` key.

## Intentionally Simple

- No final art yet.
- No sound/music implementation yet.
- No asset optimization pipeline yet.
- Later phase behavior is only prepared in config/state, not implemented.
