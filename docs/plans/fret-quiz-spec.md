# Fret Quiz - Spec

Stripped-down fork of [RiffHound/webui/quiz](https://github.com/titzer/RiffHound/tree/main/webui/quiz) for bass fretboard note recognition.

## Core mechanic

- **Direction:** Fret-to-note. Given a fret number displayed on a specific bass string, identify the note letter.
- **Input:** A-G buttons (click or keyboard).
- **Notes:** Naturals only (no sharps/flats).

## Instrument

- **4-string bass**, standard tuning: E1 (MIDI 28), A1 (33), D2 (38), G2 (43)
- String labels top-to-bottom: G, D, A, E (high to low)

## Fretboard display

- Horizontal SVG layout (same style as original)
- 4 string lines with labels on the left
- Fret numbers in rounded boxes on the string lines
- **Fret dot markers** at frets 3, 5, 7, 9, 12 (double dot) — rendered as small circles between strings
- Nut bar for open position, fret number indicator for other positions

## Position ranges

| Label   | Min fret | Max fret |
|---------|----------|----------|
| Open    | 0        | 4        |
| 3-6     | 3        | 6        |
| 6-10    | 6        | 10       |
| 10-14   | 10       | 14       |
| 12-17   | 12       | 17       |

## Sequences

- Sequence length selector: 1-4 notes per question
- Notes played in order, answered left-to-right

## Audio

- Web Audio API synth (same as original)
- Plays note(s) when question appears
- Plays note when user guesses (correct or wrong)

## Stats & history

- Side panel: Completed count, first-try count, pass rate
- Scrollable history table: #, Question, Tries
- **Persisted in localStorage** across browser sessions
- Reset button clears everything

## Theme

- **Light/dark/system toggle** in header (sun/moon icon button)
- Defaults to system (`prefers-color-scheme`)
- User choice persisted in localStorage
- Dark theme colors: dark background, light text, muted borders, SVG elements adapt

## Removed (vs original)

- Note Quiz / Key Quiz mode selector
- Sheet Music / Ear modality selector
- All sheet music rendering (treble/bass staves, clefs, noteheads, stems, ledger lines, key signatures, triads)
- Ear training (audio sequences, chord playback, choice buttons, step ladders, distractor generation)
- Key filter checkboxes (sharps/flats/minor/letters)
- Ear training options (key select, octave, length, choices)
- Treble/bass clef checkboxes
- Key quiz buttons (accidental, quality, submit, skip, hint)
- "Mode" column from history table (only one mode now)

## File structure

Single self-contained `index.html` — all CSS and JS inline. No build step.

## Title

"Fret Quiz"
