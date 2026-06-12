# Fret Quiz

Bass fretboard note recognition trainer. Given a fret number on a specific string, identify the note.

## Features

- 4-string bass in standard tuning (E-A-D-G)
- Position ranges: Open, 3-6, 6-10, 10-14, 12-17
- Sequences of 1-4 notes
- Audio feedback (Web Audio API)
- Stats and history with localStorage persistence
- Light/dark/system theme

## Usage

Open `index.html` in a browser. No build step, no dependencies.

**Keyboard:** A-G to answer, Space to replay.

## Attribution

Derived from [RiffHound](https://github.com/titzer/RiffHound) by Ben L. Titzer — specifically the [webui/quiz](https://github.com/titzer/RiffHound/tree/main/webui/quiz) module. Stripped to bass-only tab quiz with dark mode and localStorage persistence.

## License

Apache License 2.0 — see [LICENSE](LICENSE).
