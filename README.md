# Mindcraft — approved editorial UI implementation (v3)

Implements the approved five-screen visual direction with original local SVG illustrations and the agreed brand palette. Screens: Home, Practice/Daily Quest, Skill Tree with Achievements, Journal, and Settings. This is a working offline-first PWA, not a static mockup.

## Run

`python3 -m http.server 8080` from this directory; open http://localhost:8080. For iPhone installation deploy to HTTPS and use Safari > Share > Add to Home Screen.

## Preserved functionality

30 cognitive-thinking quests, multiple-choice exercises, local reflections, XP, skill progress, achievements, journal autosave, JSON export/import, and Light/Dark/System modes. Data stays in IndexedDB on the device.

## Known limitations

- Illustrations are original simplified SVG implementations inspired by the approved visual direction; they are not pixel-perfect reproductions of the generated preview.
- LINE Seed is specified in the font stack but no font file is bundled; devices without the font use a system fallback.
- No live AI feedback, cloud backup, or Firebase account. JSON exports are unencrypted.
- GitHub deployment has not occurred; connector previously returned 403 for write operations.
