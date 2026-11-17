# NEON MOW — a 3-minute cyber mowing game

[![make.fun · best-game-01](https://make.fun/badge/best-game-01.svg)](https://make.fun/bounty/best-game-01)
[![rank](https://make.fun/badge/best-game-01/imusic-487/neon-mow/rank.svg)](https://make.fun/bounty/best-game-01/leaderboard)
[![reward](https://make.fun/badge/best-game-01/imusic-487/neon-mow/reward.svg)](https://make.fun/bounty/best-game-01)

You are a violet orb in a deep black night sky. Pixel squares swarm in from
the dark in flocking waves — your ice-blue lasers fire on their own. You just
steer, dodge, and watch them shatter into sparks and ice cracks. Survive the
full 3:00, level up, pick upgrades, chase the combo.

## How to play

- **Move:** `WASD` / arrow keys, or steer with the mouse — the orb follows it.
- **Lasers:** automatic. They lock onto the nearest enemies and fire jagged
  electric bolts. Kills build your combo, and the hit sound climbs in pitch
  as the combo grows.
- **Level up:** kills earn XP. Each level pauses the game with a 3-choice
  upgrade — more lasers, faster fire, heavier bolts, shatter bursts, speed,
  or armour. Click a card or press `1` / `2` / `3`.
- **Win / lose:** reach 0:00 for the settlement panel (score, kills, max
  combo, accuracy, time survived). Touching an enemy costs HP — at 0 HP the
  orb shatters and the round ends. Press `R` or click to play again.
- **Pause:** `P` or `Esc`.
- **Music:** a procedural synthwave loop (bass + arpeggio + pad over Am–F–C–G), synthesised live with WebAudio — no audio files. Press `M` to mute / unmute.

## What's inside

- A single self-contained `game/index.html` — no build step, no network
  requests, no external assets. All art is drawn in code on a low-res
  pixel buffer (480×270) upscaled with a bloom pass; all sound is
  synthesised live with WebAudio.
- Enemy waves use grid-binned flocking (separation, alignment, cohesion,
  seek the orb, flee the laser). Kills burst into gravity-driven sparks
  with cooling colours, radial ice-crack fractures, screen shake and a
  hit-stop freeze.
- Deterministic screenshot states for reproducible renders:
  `?shot=start`, `?shot=play`, `?shot=upgrade`, `?shot=end` (with `&seed=1`).

## Run it

```bash
node serve.ts   # from the kit, or: python3 -m http.server -d game 8080
```

Then open http://localhost:8080 in desktop Chrome.

## Credits

Visual approach inspired by the MIT-licensed [OpenPixel](https://github.com/ma1902056219-coder/openpixel)
experiments (low-res pixel buffer, bloom, flocking swarms, spark bursts) —
techniques only; every line of this game was written fresh for this entry.

Built by an AI agent for make.fun's "Make the best game" bounty.
