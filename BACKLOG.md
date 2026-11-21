# Updraft Aces: backlog

Updated 2026-11-21. BC decides the order. Plan: `ideas/n63/PLAN.md` in game-studio.

## Done

- 0.16.0 (2026-11-21): Stage 4, Thunderhead Reach (BC's picks: Thunderhead Reach, dive gliders, Achilles). Storm sea, rain, lightning (soft with Reduce flashing, off with Reduce motion), dive gliders, achievement Eye of the Storm.
- 0.15.0 (2026-11-21): A13 (new Gemini scenery, sharper in the APK), A16 (kit 1.25.0: safe area, halo glow piece, baker in signing) and A17 (HDR glow on the play field only, off by default, Tester tools > Look). BC: "a13 a16 a17".
- 0.14.0 (2026-11-21): the Android release. BC: "what are improvments that can be made to the android version that we are not using today?", then "move forward and add 1-11" and "actually do add tilt controls". All twelve items from the Android review below. Kit 1.24.1.
- 0.13.0 (2026-11-20): BC's ask "a little faster when playing on widescreen, maybe add speed power ups": side to side speed grows with the screen's width, plus a pink Speed power-up (two levels). Review ideas 4 (bullet walls only a roll beats), 14 (menu rows at least 48 dp on phones, kit 1.24.0), 21 (gold coins), 28 (`play.gd` split in three), 32 (checkpoint save measured) and 34 (focus guard and particle helpers moved into kit 1.24.0). D1 answered: keep power-ups through a rewind. D2 answered: the guns keep firing through a roll. Stage 4 decision page out.
- 0.12.0 (2026-11-20): review ideas 20 (rescue rafts), 22 (Score Attack) and 30 (tests for the 0.5 features).
- 0.11.0 (2026-11-20): review ideas 11 (power-up tokens), 12 (sound and combo chime), 13 (start screen), 19 (breathers and the Grand Armada), 29 (lighter shader) and 31 (smaller music). BC: "game plays good, move to the next release".
- 0.10.0 (2026-11-20): Stage 3, Aurora North (BC's picks: Aurora North, Balloon mines, Heroic Age). `data/stage3.ldtk` from `tools/make_stage3_ldtk.py`, 42 waves in six sections. Balloon mines, a night sea in the shader, four more medals, achievement Northern Lights.
- 0.9.0 (2026-11-20): review idea 10, sideways phones. A shorter play area sideways keeps everything bigger, still edge to edge.
- 0.8.0 (2026-11-20): review ideas 15 (medals), 16 (chain), 17 (shootable flak), 18 (Ace points) and 27 (stage table).
- 0.7.0 (2026-11-20): review ideas 1, 2, 4, 5, 6, 7, 8 and 9 (Ace with teeth plus feel). D1 set to keep power-ups through a rewind, D2 left as is. Both still BC's call.
- 0.6.1 (2026-11-20): bugs B1 to B6 from the review. BC: "fix bugs first and go in your suggested order".
- 0.6.0 (2026-11-20): BC's "Do 1,2,4,5,6". Painted start screen (Gemini sun, side-view clouds, cloud bank). Trademark search (`docs_name_check.md`). The game runs on kit 1.22.0: K2 Waves, K8 easy pack, the LDtk reader and T1 tester notes. Its own copies are gone. Same bot trace before and after.
- 0.5.0 (2026-11-20): Stage 2, Amber Canyon (BC's picks: Amber Canyon, Bombers, At Launch). `data/stage2.ldtk` from `tools/make_stage2_ldtk.py`, 42 waves in six sections. Bombers in pairs drop flak that bursts into rings. Canyon ground in the sea shader (`land`). Menu rows pick a stage, Stage 2 opens after a Cloud Harbor clear. Achievements Sundown and Flak Dancer.
- 0.4.1 (2026-11-20): the start screen line says "A pilot" in place of "A bearded pilot" (BC: "change a bearded pilot, to just say pilot on the start screen, remove bearded"). The game page and Shelf tag match.
- 0.4.0 (2026-11-20): painted islands (lighthouse, windmill, dock) and clouds, the side-view twin-engine on the start screen, the app icon (BC's pick C, repainted with the twin-engine), the name check (web search: no game named Updraft Aces).
- 0.3.1 (2026-11-20): the play area fills the whole screen, upright and sideways, so you fly edge to edge (BC: "I need to be able to go edge to edge in flying in the game"). The player plane's left wing tip and the pilot's edge were clipped by the cut and are whole again (BC: "Left side of wing seems to be cutoff").
- 0.3.0 (2026-11-20): BC's picks in. Twin-engine plane, coral monoplane wingmen, the storm olive and teal enemy set (fighter, swooper, gunner), the braided ginger pilot on the start screen, Titan One, Call to Adventure on the start screen and Beachfront Celebration in flight. Pilots: a sea shader under the planes and GPU particles for the smoke trail and bursts. Art cut from Gemini by `art_src/cut_art.py`.
- 0.2.0 (2026-11-20): Spread, Wingmen and Shield power-ups dropped by full formation clears (set per wave in LDtk). Wingmen take a bullet each. Stage 1 now lives in `data/stage1.ldtk` (LDtk pilot I5, read straight from JSON, no plugin). The K8 easy mode pack, built here first: extra shield, slower enemies, softer hits, more checkpoints and a bullet glow, each its own switch.
- 0.1.0 gray box (2026-11-20): vertical scroll, drag or stick to fly, auto-fire, five formation kinds (line, vee, loop, swoop, gunner), formation bonus, the roll with three charges per checkpoint, shield and score (kit K12), six checkpoints, soft fail rewind, Breeze, Standard and Ace, Stage 1 Cloud Harbor (about 3 minutes, final wave section, no boss), the T1 tester note and red marker (test builds only).

## Now

- Waiting on BC: play 0.16.0 on the phone (Stage 4 and the gliders, tilt direction, buzzes, camera hole, frame rate, HDR glow in Tester tools).
- D3. Glider balance: about 14 of 48 gliders dive on Standard because the plane shoots them first. Keep, or make more dive (faster slide-in, or no hits until they hang)?

## Android review 2026-11-21 (0.13.0, read from the code, the export settings and the studio's Android research)

BC picked all twelve. Built in 0.14.0.

- A1. Done in 0.14. Android back swipe: closes the top panel or opens the Menu (E6.6). S.
- A2. Done in 0.14. Safe area: the HUD keeps clear of the camera hole, corners and gesture bar. S to M.
- A3. Done in 0.14. Buzz styles: 14 events on the kit's named styles, a climbing buzz for the Grand Armada. S.
- A4. Done in 0.14. Feel check at 60, 90 and 120 Hz (`tests/feel_check.gd`). S.
- A5. Done in 0.14 for nine sprites (plane, wingmen, four enemies, three rafts), APK only. The mine, islands and clouds need new, bigger art. S to M.
- A6. Done in 0.14. Soft shadows, wrecks that fall and splash, spray under a roll. S.
- A7. Done in 0.14 as soft halos, not a bloom pass (measured: the bloom pass cut the browser build to a third). Settings > Glow. S.
- A8. Done in 0.14. Wing tip vapor, smoke on damaged gunners and bombers, round soft particles. "Spray at low passes" became spray under a roll. M.
- A9. Done in 0.14. Richer sea on Android in its own shader file: foam rings, shallows, sun and moon glitter, river sparkle. S to M.
- A10. Done in 0.14. App category Game. S.
- A11. Done in 0.14. Mobile renderer (Vulkan) for the APK, Swappy mode 0, baked shaders. Real HDR glow tried and left out (menu text got harder to read). M.
- A12. Done in 0.14. Tilt to steer: Settings switch, three strengths, Recenter tilt. Android only. S to M.

Follow-ups from 0.14 (BC picks by number):

- A13. Done in 0.15. Sharper islands, clouds and the balloon mine: new Gemini pictures at twice the size, APK only. S to M.
- A14. A Flip tilt switch if tilt flies the wrong way on a phone, or if BC likes it reversed. S.
- A15. Measure on the Fold and the Retroid: frame rate at 120 Hz, battery and heat of the Mobile renderer against 0.13.0, the checkpoint save (idea 32). Needs BC's phone. S.
- A16. Done in 0.15 (kit 1.25.0). Kit ideas, each needs BC's yes: the safe area in `screen_fit.gd` so the start screen and Settings keep clear of the camera hole too, the back swipe in the starter's `main.gd`, a baker option in `sign_android.sh` (today `tools/godot_baker.sh` stands in), the halo layer as a kit piece for Sunset Static and Tiny Tailwind. S each.
- A17. Done in 0.15: HDR glow on the play field only, in its own layer. Off by default (software Vulkan: 31 to 54 ms a frame). Try it on the phone in Tester tools > Look. M.
- A18. Kit fixes found in 0.15: `sync_common.sh` deletes the committed `.uid` files in the kit folders. Panel covers under an inset safe root leave a thin undimmed strip at the camera hole. Needs BC's yes. S.

## Asked for by BC, not built yet

- Nothing open.

## Review 2026-11-20 (0.6.0, four reviewers: gameplay, look and feel, genre, code)

BC: "take a few minutes to review this game again with multiple agents and suggest a backlog of ideas". BC picks by number.

### Bugs (fix first)

- B1. Fixed in 0.6.1. Old saves: a player who cleared Cloud Harbor before 0.5 finds Amber Canyon locked. `main.gd` merges `SAVE0` (`unlocked: 1`) before `play.start()` reads its `clears > 0` fallback. Verified. S.
- B2. Fixed in 0.6.1. The "slower enemies" assist adds enemy fire: movement uses `easy.speed_k()` but `fire_t` counts real time, so gunners and bombers stay longer and fire about a third more. Verified. S.
- B3. Fixed in 0.6.1. The plane can slide half off the right edge (side limit 16 is less than half the plane's width). S.
- B4. Fixed in 0.6.1. Spread level marks draw under the Menu button in wide landscape. S.
- B5. Fixed in 0.6.1. A Shield pickup at full shield does nothing but says "Shield +1". S.
- B6. Fixed in 0.6.1. No save upgrade test: load `tests/saves/v1.json` and round-trip a Stage 2 save at a checkpoint. Would have caught B1. S.

### Ace with teeth (the bot takes zero hits on Ace in both stages)

1. Done in 0.7. Enemy fire patterns: small planes fire short fans or streams, swoopers fire too. Today each small plane fires one aimed shot and most die in 1.4 s, so moving beats every shot. M.
2. Done in 0.7. Ace different in kind: small planes fire twice, Ace-only waves (a new LDtk field). S to M.
3. Difficulty that rises across a stage: bullets per Stage 1 section run 13, 14, 6, 2, 12, 12. Fewer power-up drops (14 in 48 waves), denser late waves. M.
4. Done in 0.13 (bullet walls, close shave points from 0.7). Give the roll a job: threats only a roll beats (close flak, bullet walls), points and a "Close shave!" pop for rolling through bullets. S to M.
5. Done in 0.7. Pressure checks in the test gate: minimum bullets per section and a weaving bot that takes some hits on Ace. S.

### Feel and readability

6. Done in 0.7. Haptics: Settings already has Rumble but play never calls it. Buzz on hit, roll, formation clear and shield down. S.
7. Done in 0.7. Hits that feel like hits: a white flash and spark on enemy hits, and "+1000" pops at the last plane instead of a mid-screen banner. S.
8. Done in 0.7. Canyon bullets: a dark outline or a cooler color so bullets read on sand and mesas. Dust clouds no longer draw over bullets near the plane. S.
9. Done in 0.7. HUD: three charge pips and an icon on the Roll button, a dark pill behind shield and score, a bigger score, no HUD shake. S.
10. Done in 0.9 (shorter area sideways, not a capped width, to keep BC's edge to edge). Sideways phones: cap the play width so the plane stays big, and put the HUD in the side margins. M.
11. Done in 0.11. Power-ups with their own shapes and icons in the game font (Spread is the same cream as your shots today). S to M.
12. Done in 0.11. Softer shot sound (it plays 9 times a second) and a rising combo chime. Softer default hurt flash (35 percent). S.
13. Done in 0.11. Start screen on upright phones: pilot not cut off, bigger hint text. Records panel and menu header polish. S.
14. Done in 0.13 (kit 1.24.0 phone fit). Bigger menu rows on phones (32 px today, 48 is the phone norm). Kit change. M.

### Replay value (from the genre review)

15. Done in 0.8. Stage medals, four per stage: clear every formation, no hits, rescue everyone, close shaves. As in Sky Force. M.
16. Done in 0.8. Formation chain: back-to-back full clears build a chain bonus, a miss breaks it. As in Ikaruga. S.
17. Done in 0.8. Shootable flak shells: pop them early for points. S.
18. Done in 0.8. Ace score multiplier or a best score per level. S.
19. Done in 0.11. Breathers before checkpoints and a "Grand Armada" finale fly-past (not a boss). M.
20. Done in 0.12. Rescue pickups: castaways on islands and mesas, hover to rescue. As in Sky Force. M.
21. Done in 0.13 (gold coins from gunners and bombers, no ground targets yet). Gold pickups from ground targets (boats, windmills, carts), worth most on their bright frame. As in Strikers 1945. S.
22. Done in 0.12. Score Attack: a 2 or 5 minute run for a top 10 on the device. As in Star Soldier R. S to M.
23. Updraft gauge: coins fill it, trigger for a few seconds of bullet soaking and a multiplier. As in Jamestown. M.
24. Daily Flight: a date-seeded stage with a twist, local best only. M.
25. A hangar of two or three more planes unlocked by medals. L.
26. Local co-op on two controllers. L.

### Under the hood

27. Done in 0.8. Stage table: each stage row holds its music, scenery, clear achievement and unlock text, and the menu builds from it. Makes Stage 3 a data job. M.
28. Done in 0.13 (`play_core.gd`, `play_draw.gd`, `play.gd`). Split `play.gd` (1,194 lines): enemies, drawing, bot and test hooks into their own files. M.
29. Done in 0.11. Canyon shader skips the sea math it throws away. S.
30. Done in 0.12. Tests for the 0.5 features: flak hits and rolls, the Flak Dancer bonus, the locked menu row, stage and unlock after a reload. M.
31. Done in 0.11. Smaller music (re-encode at about 72 kbps, about 2 MB less on the web). S.
32. Done in 0.13 on a desktop: 0.2 ms median, 0.7 ms worst. A real phone is still unmeasured. Measure the checkpoint save on a real phone (1 to 2 ms spikes here, every 30 s). S.
33. Build folder cleanup: 779 MB of old APKs and web folders. S.
34. Done in 0.13 (kit 1.24.0, BC said yes). Kit candidates: the focus fix in `main.gd` and the particle helpers. S.

### Needs a decision from BC

- D1. Answered 0.13: keep them (BC). (0.7 default: kept.) A rewind clears Spread and Wingmen. BRIEF.md says a rewind keeps everything. Keeping them makes the game gentler. Clearing them is more classic. Which?
- D2. Answered 0.13: the guns keep firing (BC). Rolling stops your guns. Keep it as the roll's cost, or let auto-fire run through a roll?

## Later

- Done in 0.16.0. Stage 4 (BC's picks 2026-11-21, 10:31 AM): Thunderhead Reach, dive gliders, Achilles. After 0.15.0 ("then afterwards"). Gemini art made 2026-11-21: `art_src/gemini/s4_*.png` (sea stacks, a reef with a wreck, a lighthouse islet, a hut islet, four thunderheads, the dive glider).
- A trademark attorney's clearance and a filing for "Updraft Aces" before a paid Play Store launch (search done in 0.6).

## Not planned (they break the pillars)

- Boss battles (BC, 2026-11-20: "No boss battles").
- Lives and game over (soft fail, G4.1).
- Real WWII aircraft, markings or history (fantasy skies, BC 2026-11-20).

## Decisions from BC

- 2026-11-21, 10:30 AM: "a13 a16 a17". A13: "New Gemini art" (picked over an upscale of the 0.14 art).
- 2026-11-21, 10:31 AM: "Stage 4 setting: Thunderhead Reach. New enemy kind: Dive gliders. Stage 4 play music: Achilles." To build after A13, A16 and A17.
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
