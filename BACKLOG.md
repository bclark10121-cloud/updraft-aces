# Updraft Aces: backlog

Updated 2026-11-20. BC decides the order. Plan: `ideas/n63/PLAN.md` in game-studio.

## Done

- 0.6.0 (2026-11-20): BC's "Do 1,2,4,5,6". Painted start screen (Gemini sun, side-view clouds, cloud bank). Trademark search (`docs_name_check.md`). The game runs on kit 1.22.0: K2 Waves, K8 easy pack, the LDtk reader and T1 tester notes. Its own copies are gone. Same bot trace before and after.
- 0.5.0 (2026-11-20): Stage 2, Amber Canyon (BC's picks: Amber Canyon, Bombers, At Launch). `data/stage2.ldtk` from `tools/make_stage2_ldtk.py`, 42 waves in six sections. Bombers in pairs drop flak that bursts into rings. Canyon ground in the sea shader (`land`). Menu rows pick a stage, Stage 2 opens after a Cloud Harbor clear. Achievements Sundown and Flak Dancer.
- 0.4.1 (2026-11-20): the start screen line says "A pilot" in place of "A bearded pilot" (BC: "change a bearded pilot, to just say pilot on the start screen, remove bearded"). The game page and Shelf tag match.
- 0.4.0 (2026-11-20): painted islands (lighthouse, windmill, dock) and clouds, the side-view twin-engine on the start screen, the app icon (BC's pick C, repainted with the twin-engine), the name check (web search: no game named Updraft Aces).
- 0.3.1 (2026-11-20): the play area fills the whole screen, upright and sideways, so you fly edge to edge (BC: "I need to be able to go edge to edge in flying in the game"). The player plane's left wing tip and the pilot's edge were clipped by the cut and are whole again (BC: "Left side of wing seems to be cutoff").
- 0.3.0 (2026-11-20): BC's picks in. Twin-engine plane, coral monoplane wingmen, the storm olive and teal enemy set (fighter, swooper, gunner), the braided ginger pilot on the start screen, Titan One, Call to Adventure on the start screen and Beachfront Celebration in flight. Pilots: a sea shader under the planes and GPU particles for the smoke trail and bursts. Art cut from Gemini by `art_src/cut_art.py`.
- 0.2.0 (2026-11-20): Spread, Wingmen and Shield power-ups dropped by full formation clears (set per wave in LDtk). Wingmen take a bullet each. Stage 1 now lives in `data/stage1.ldtk` (LDtk pilot I5, read straight from JSON, no plugin). The K8 easy mode pack, built here first: extra shield, slower enemies, softer hits, more checkpoints and a bullet glow, each its own switch.
- 0.1.0 gray box (2026-11-20): vertical scroll, drag or stick to fly, auto-fire, five formation kinds (line, vee, loop, swoop, gunner), formation bonus, the roll with three charges per checkpoint, shield and score (kit K12), six checkpoints, soft fail rewind, Breeze, Standard and Ace, Stage 1 Cloud Harbor (about 3 minutes, final wave section, no boss), the T1 tester note and red marker (test builds only).

## Now

- Waiting on BC: play 0.6.0. The painted start screen.

## Asked for by BC, not built yet

- Nothing open.

## Review 2026-11-20 (0.6.0, four reviewers: gameplay, look and feel, genre, code)

BC: "take a few minutes to review this game again with multiple agents and suggest a backlog of ideas". BC picks by number.

### Bugs (fix first)

- B1. Old saves: a player who cleared Cloud Harbor before 0.5 finds Amber Canyon locked. `main.gd` merges `SAVE0` (`unlocked: 1`) before `play.start()` reads its `clears > 0` fallback. Verified. S.
- B2. The "slower enemies" assist adds enemy fire: movement uses `easy.speed_k()` but `fire_t` counts real time, so gunners and bombers stay longer and fire about a third more. Verified. S.
- B3. The plane can slide half off the right edge (side limit 16 is less than half the plane's width). S.
- B4. Spread level marks draw under the Menu button in wide landscape. S.
- B5. A Shield pickup at full shield does nothing but says "Shield +1". S.
- B6. No save upgrade test: load `tests/saves/v1.json` and round-trip a Stage 2 save at a checkpoint. Would have caught B1. S.

### Ace with teeth (the bot takes zero hits on Ace in both stages)

1. Enemy fire patterns: small planes fire short fans or streams, swoopers fire too. Today each small plane fires one aimed shot and most die in 1.4 s, so moving beats every shot. M.
2. Ace different in kind: small planes fire twice, Ace-only waves (a new LDtk field). S to M.
3. Difficulty that rises across a stage: bullets per Stage 1 section run 13, 14, 6, 2, 12, 12. Fewer power-up drops (14 in 48 waves), denser late waves. M.
4. Give the roll a job: threats only a roll beats (close flak, bullet walls), points and a "Close shave!" pop for rolling through bullets. S to M.
5. Pressure checks in the test gate: minimum bullets per section and a weaving bot that takes some hits on Ace. S.

### Feel and readability

6. Haptics: Settings already has Rumble but play never calls it. Buzz on hit, roll, formation clear and shield down. S.
7. Hits that feel like hits: a white flash and spark on enemy hits, and "+1000" pops at the last plane instead of a mid-screen banner. S.
8. Canyon bullets: a dark outline or a cooler color so bullets read on sand and mesas. Dust clouds no longer draw over bullets near the plane. S.
9. HUD: three charge pips and an icon on the Roll button, a dark pill behind shield and score, a bigger score, no HUD shake. S.
10. Sideways phones: cap the play width so the plane stays big, and put the HUD in the side margins. M.
11. Power-ups with their own shapes and icons in the game font (Spread is the same cream as your shots today). S to M.
12. Softer shot sound (it plays 9 times a second) and a rising combo chime. Softer default hurt flash (35 percent). S.
13. Start screen on upright phones: pilot not cut off, bigger hint text. Records panel and menu header polish. S.
14. Bigger menu rows on phones (32 px today, 48 is the phone norm). Kit change. M.

### Replay value (from the genre review)

15. Stage medals, four per stage: clear every formation, no hits, rescue everyone, close shaves. As in Sky Force. M.
16. Formation chain: back-to-back full clears build a chain bonus, a miss breaks it. As in Ikaruga. S.
17. Shootable flak shells: pop them early for points. S.
18. Ace score multiplier or a best score per level. S.
19. Breathers before checkpoints and a "Grand Armada" finale fly-past (not a boss). M.
20. Rescue pickups: castaways on islands and mesas, hover to rescue. As in Sky Force. M.
21. Gold pickups from ground targets (boats, windmills, carts), worth most on their bright frame. As in Strikers 1945. S.
22. Score Attack: a 2 or 5 minute run for a top 10 on the device. As in Star Soldier R. S to M.
23. Updraft gauge: coins fill it, trigger for a few seconds of bullet soaking and a multiplier. As in Jamestown. M.
24. Daily Flight: a date-seeded stage with a twist, local best only. M.
25. A hangar of two or three more planes unlocked by medals. L.
26. Local co-op on two controllers. L.

### Under the hood

27. Stage table: each stage row holds its music, scenery, clear achievement and unlock text, and the menu builds from it. Makes Stage 3 a data job. M.
28. Split `play.gd` (1,194 lines): enemies, drawing, bot and test hooks into their own files. M.
29. Canyon shader skips the sea math it throws away. S.
30. Tests for the 0.5 features: flak hits and rolls, the Flak Dancer bonus, the locked menu row, stage and unlock after a reload. M.
31. Smaller music (re-encode at about 72 kbps, about 2 MB less on the web). S.
32. Measure the checkpoint save on a real phone (1 to 2 ms spikes here, every 30 s). S.
33. Build folder cleanup: 779 MB of old APKs and web folders. S.
34. Kit candidates (needs BC's yes): the focus fix in `main.gd` and the particle helpers. S.

### Needs a decision from BC

- D1. A rewind clears Spread and Wingmen. BRIEF.md says a rewind keeps everything. Keeping them makes the game gentler. Clearing them is more classic. Which?
- D2. Rolling stops your guns. Keep it as the roll's cost, or let auto-fire run through a roll?

## Later

- Stage 3.
- A trademark attorney's clearance and a filing for "Updraft Aces" before a paid Play Store launch (search done in 0.6).

## Not planned (they break the pillars)

- Boss battles (BC, 2026-11-20: "No boss battles").
- Lives and game over (soft fail, G4.1).
- Real WWII aircraft, markings or history (fantasy skies, BC 2026-11-20).

## Decisions from BC

- 2026-11-20, 9:51 AM: "I want to do the 1942 style plane shooter game". Soft fail, fantasy skies, clean toy render. Pilots: LDtk, particles and the sky shader, T1. Skip Pixelwright.
- 2026-11-20, 9:57 AM: "No boss battles", "yes on name decision page", "a adult male pilot with a beard".
- 2026-11-20, 9:59 AM: "N63 name: Updraft Aces."
- 2026-11-20, 12:01 PM: "C for app icon". Gemini repainted C with the twin-engine (it had drawn the wingman's plane).
- 2026-11-20, 11:44 AM: "move to next steps". 0.4 started.
- 2026-11-20, 11:47 AM: "Left side of wing seems to be cutoff". Fixed in 0.3.1.
- 2026-11-20, 11:49 AM: "I need to be able to go edge to edge in flying in the game. the width seems very narrow especially when playing turning my phone to the side mode on phone". Fixed in 0.3.1.
- 2026-11-20, 10:49 AM: "move to the next release". 0.3 started.
- 2026-11-20, 10:58 AM: picks from the look and sound page: pilot C (braided ginger beard, flap cap), plane C (twin-engine), Titan One, Call to Adventure (start screen), Beachfront Celebration (play).
- 2026-11-20, 11:21 AM: "Enemy set: B. Storm olive and teal."
- 2026-11-20, 10:39 AM: "first play thorugh was good, move forward with next release". 0.2 built.
