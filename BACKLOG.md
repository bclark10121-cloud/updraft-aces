# Updraft Aces: backlog

Updated 2026-11-20. BC decides the order. Plan: `ideas/n63/PLAN.md` in game-studio.

## Done

- 0.3.0 (2026-11-20): BC's picks in. Twin-engine plane, coral monoplane wingmen, the storm olive and teal enemy set (fighter, swooper, gunner), the braided ginger pilot on the start screen, Titan One, Call to Adventure on the start screen and Beachfront Celebration in flight. Pilots: a sea shader under the planes and GPU particles for the smoke trail and bursts. Art cut from Gemini by `art_src/cut_art.py`.
- 0.2.0 (2026-11-20): Spread, Wingmen and Shield power-ups dropped by full formation clears (set per wave in LDtk). Wingmen take a bullet each. Stage 1 now lives in `data/stage1.ldtk` (LDtk pilot I5, read straight from JSON, no plugin). The K8 easy mode pack, built here first: extra shield, slower enemies, softer hits, more checkpoints and a bullet glow, each its own switch.
- 0.1.0 gray box (2026-11-20): vertical scroll, drag or stick to fly, auto-fire, five formation kinds (line, vee, loop, swoop, gunner), formation bonus, the roll with three charges per checkpoint, shield and score (kit K12), six checkpoints, soft fail rewind, Breeze, Standard and Ace, Stage 1 Cloud Harbor (about 3 minutes, final wave section, no boss), the T1 tester note and red marker (test builds only).

## Now

- Waiting on BC: play 0.3. The new look, the music and the particles.

## Asked for by BC, not built yet

3. 0.3: particles (smoke trails, debris, bursts) and a scrolling sky and sea shader (pilots).
1. Full name check for Updraft Aces (G4.8): stores and trademarks. A web search only so far.
2. Painted islands, clouds and the side-view plane on the start screen through Gemini.
3. Stage 2.

## Ideas to choose from (BC picks by number)

1. Move the enemy wave code into the kit with Sunset Static (K rule 1). Needs BC's yes for `common/`.
2. Make the T1 note tool a kit piece for every game if the pilot works.
3. Move the K8 easy mode pack (`scripts/easy_pack.gd`) into the kit for every combat game. Needs BC's yes for `common/`.
4. Make the bot harder to fool: Ace has zero hits in the 0.1 bot run, so Ace may need more bullets.

## Later

- Stage 2.

## Not planned (they break the pillars)

- Boss battles (BC, 2026-11-20: "No boss battles").
- Lives and game over (soft fail, G4.1).
- Real WWII aircraft, markings or history (fantasy skies, BC 2026-11-20).

## Decisions from BC

- 2026-11-20, 9:51 AM: "I want to do the 1942 style plane shooter game". Soft fail, fantasy skies, clean toy render. Pilots: LDtk, particles and the sky shader, T1. Skip Pixelwright.
- 2026-11-20, 9:57 AM: "No boss battles", "yes on name decision page", "a adult male pilot with a beard".
- 2026-11-20, 9:59 AM: "N63 name: Updraft Aces."
- 2026-11-20, 10:49 AM: "move to the next release". 0.3 started.
- 2026-11-20, 10:58 AM: picks from the look and sound page: pilot C (braided ginger beard, flap cap), plane C (twin-engine), Titan One, Call to Adventure (start screen), Beachfront Celebration (play).
- 2026-11-20, 11:21 AM: "Enemy set: B. Storm olive and teal."
- 2026-11-20, 10:39 AM: "first play thorugh was good, move forward with next release". 0.2 built.
