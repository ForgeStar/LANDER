# LANDER — Classic Arcade LUNAR LANDER Clone

A single-file clone of Atari's 1979 arcade **LUNAR LANDER** (the first vector arcade game) in vanilla JS + canvas, rendered inside a LANDER cabinet bezel with a CRT glass shader (barrel distortion, scanlines, reflections).

## Play

- Open [index.html](index.html) — that's the whole game (no build step, no dependencies).
- Up/W: main thrust · Left/Right or A/D: rotate (±80°) · X/Space: abort burn · Any key: start
- Touch: tap to start · drag up = thrust, drag sideways = rotate
- P: pause · M: mute · C: cycle CRT glass mode

## Mechanics (per the 1979 original)

- **Fuel pool** of 750 units persists across missions; thrusting burns 30/s, rotating burns 4/s, an abort burn costs 120.
- **Terrain** is a jagged straight-line moonscape (no curves, like the vector hardware) with flat landing pads marked **2X–5X** — narrower pads pay more.
- **Zoom**: the view switches to a close-up as you near the surface.
- **Scoring**: good landing (≤10 down, ≤12 sideways) = 50 × pad multiplier + 50 fuel bonus · hard landing = 15 × multiplier · crash = 5. A crash ends the game; score is cumulative.
- **HUD**: SCORE / TIME / FUEL on the left; ALTITUDE / HORIZONTAL SPEED / VERTICAL SPEED (with direction arrows) on the right, like the arcade cabinet.
- **Abort** (X): straightens the ship, kills sideways velocity, shoves you up off the surface — costs 120 fuel.
- Difficulty ramps each mission: steeper terrain, narrower pads.

## GitHub Pages

This repo is deployed as-is from the root, so the game lives at:

    https://forgestar.github.io/LANDER/
