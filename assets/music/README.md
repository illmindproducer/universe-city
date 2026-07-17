# Music drop zone

Drop 4-8 bar loopable tracks here. MP3 320kbps (or hand Claude WAVs to convert).
Missing files = silence, no errors. Names are exact:

- lobby.mp3     — castle lobby (also covers stage + studio for now)
- shop.mp3      — inside The BLAP Shop
- hospital.mp3  — inside The Remedy
- world.mp3     — The Outside (meadows)
- wastes.mp3    — The Vinyl Wastes
- cave.mp3      — The Crate Depths (installed 2026-07-08 — "worm cave theme")
- battle.mp3    — combat loop (high energy), regular monsters + duels
- boss.mp3      — BOSS battle loop (installed 2026-07-08 — "worm battle theme");
                  missing file = bosses fall back to battle.mp3
- victory.mp3   — SHORT non-looping sting (2-4s), cues instantly on the kill
- road.mp3      — ⬅ WANTED: The Stone Road (reusing world.mp3 until it lands)
- town2.mp3     — ⬅ WANTED: Bridgetown (reusing world.mp3 until it lands)
- castle2.mp3   — ⬅ WANTED: Castle Crescendo (reusing lobby.mp3 until it lands)
- vale.mp3      — ⬅ WANTED: The Hollow Vale (reusing wastes.mp3 until it lands)
- undercroft.mp3 — ⬅ WANTED: The Undercroft (reusing cave.mp3 until it lands)
  (when a WANTED file lands, also point the map name at the new key in
  src/music.js area() — currently mapped to the reused tracks)

Loops play gapless via WebAudio. M key toggles music in-game (choice persists).
All tracks are LEVEL-MATCHED in-engine to ~-17.5dB RMS via TRACK_GAIN in
src/music.js — when you replace a track, ask Claude to re-measure and retune
its trim (boosts are limited by the file's peak headroom; mastering new tracks
to ≈-17.5dB RMS with ~2dB headroom needs no trim at all).
- starfall.mp3  — ⬅ WANTED: The Starfall crater lands (reusing wastes.mp3 until it lands)
- husk.mp3      — ⬅ WANTED: The Herald's Husk dungeon (reusing cave.mp3 until it lands)
- hall.mp3      — ⬅ WANTED: The Concert Hall (haunted, then triumphant — reusing wastes.mp3)
