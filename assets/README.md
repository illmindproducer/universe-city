# Asset drop-in folder

The engine automatically uses real art from here and falls back to built-in
procedural pixel art for anything missing. No code changes needed.

## Characters — `characters/`
- `player.png` — the player sprite sheet. Standard RPG Maker single-character format:
  **3 frames wide x 4 directions tall** (rows top-to-bottom: down, left, right, up).
  Any frame size works (48x48, 48x72, etc.) — the engine derives it from the image.

## Tiles — `tiles/`
- Tileset images (48px grid) + a `manifest.json` mapping map characters to tiles:
  ```json
  {
    ".": ["floors.png", 0, 0],
    "#": ["walls.png", 2, 1]
  }
  ```
  Format: `"mapChar": ["file.png", column, row]` (0-indexed, 48px cells).
  Map characters are defined in src/maps.js (legend at the top of the file).

## Licensing rule (non-negotiable)
Only put assets here that we have the rights to ship: licensed packs (check the
license allows commercial, non-RPG-Maker use), commissioned work, or AI-generated
art we've verified. Never ripped game assets — treat those like uncleared samples.
