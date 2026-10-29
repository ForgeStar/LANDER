# LANDER — Classic Arcade LUNAR LANDER Clone

A single-file clone of Atari's 1979 arcade **LUNAR LANDER** (the first vector arcade game) in vanilla JS + canvas, rendered inside a LANDER cabinet bezel with a CRT glass shader (barrel distortion, scanlines, reflections).

## Play

- Open [index.html](index.html) — that's the whole game (no build step, no dependencies).
- Up/W: main thrust · Left/Right or A/D: rotate (±80°) · X/Space: abort burn · Any key: start
- Touch: tap to start · drag up = thrust, drag sideways = rotate
- P: pause · M: mute · C: cycle CRT glass mode

## Mechanics (per the 1979 original)

- **Fuel pool** of 750 units persists across missions; thrusting burns 30/s, rotating burns 4/s, an abort burn costs 120.
- **Level** is a single screen (like the arcade original): the whole jagged straight-line moonscape fits on screen at once, with no scrolling. Mountains live in the lower half of the view — peaks never rise above the middle.
- **Pads**: 3–4 flat landing pads per level — a fixed mix of two small, one medium, one large (3-pad levels drop the medium), shuffled and dropped onto the relief so a small pad on a steep slope is a real challenge. Marked **2X–5X** — the narrowest pad pays 5X.
- **Spawn**: the ship starts at the top-left corner and drifts in sideways, so the first thing you see is the full level and you plan your descent from there.
- **Camera**: the wide view is completely static — it never follows the ship. Below 120 altitude the view hard-cuts to a locked 2.5× close-up, and below 60 it cuts again to a 4.5× close-up; each region stays fixed until you leave it left, right, or keep descending, then it re-centers on a new region. Back out to wide above 200 altitude.
- **Scoring**: good landing (≤10 down, ≤12 sideways) = 50 × pad multiplier + 50 fuel bonus · hard landing = 15 × multiplier · crash = 5. A crash ends the game; score is cumulative.
- **HUD**: SCORE / TIME / FUEL on the left; ALTITUDE / HORIZONTAL SPEED / VERTICAL SPEED (with direction arrows) on the right, like the arcade cabinet.
- **Abort** (X): straightens the ship, kills sideways velocity, shoves you up off the surface — costs 120 fuel.
- Difficulty ramps each mission: steeper terrain, narrower pads.

## GitHub Pages

This repo is deployed as-is from the root, so the game lives at:

    https://forgestar.github.io/LANDER/
