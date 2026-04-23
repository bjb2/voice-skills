# Voice Skills for Claude Code

Four Claude Code slash commands that build a living map of a writer's voice through craft analysis. The system gets richer with each piece you add — after 10+ pieces you'll have a map of your actual voice, not the voice you think you have.

---

## What it does

Each piece you intake gets deep craft analysis: standout images, structural moves, borrowed imagery, thematic territory, how it connects to everything else. The analysis accumulates into a `voice.md` profile that updates automatically. When you share a draft for review, Claude reads that profile and evaluates the draft against *your specific voice* — not a generic writing rubric.

The core insight: most writers have a coherent interior world across their work that they can't fully see from inside it. Enough pieces analyzed consistently, and the map starts revealing patterns you didn't know were there.

---

## Installation

Copy all `.md` files to your Claude Code commands directory:

```bash
# macOS / Linux
cp *.md ~/.claude/commands/

# Windows
copy *.md %USERPROFILE%\.claude\commands\
```

Then use them as slash commands in any Claude Code session.

---

## Usage

### 1. Initialize

```
/voice-init
```

Creates `voice.md` and `pieces/` in your current directory. Run from your writing project root. Optionally pass a first piece to intake immediately:

```
/voice-init ./my-first-poem.md
```

### 2. Add a piece

```
/voice-intake ./poem.md
/voice-intake ./lyrics.md
```

Claude reads the piece, performs craft analysis, saves it to `pieces/`, and updates `voice.md`. Repeat for every piece in your collection.

### 3. Review a draft

```
/voice-review ./draft.md
```

Claude loads your voice profile and existing pieces, then evaluates the draft against your established voice. Flags what's working, what's borrowed, and what needs attention.

Optionally focus the review:

```
/voice-review ./draft.md imagery
/voice-review ./draft.md structure
```

### 4. Map the collection

```
/voice-map
```

Full synthesis of everything: thematic territory, craft signatures, formal range, through-lines, collection arc, and unexplored territory. Most useful after 10+ pieces.

### 5. Generate for Suno

```
/suno a melancholic indie folk song about leaving home
/suno upbeat 80s synth-pop, female vocals, about chasing dreams
```

Takes a song concept and produces a precision-crafted Style Prompt + structured Lyrics ready to paste into [Suno](https://suno.com) Custom Mode. Handles genre, mood, vocals, instrumentation, BPM, and all section tags.

---

## Directory structure

After setup, your writing project will look like:

```
your-writing-project/
├── voice.md          # Living voice profile — auto-updated by /voice-intake
└── pieces/
    ├── wanting.md    # Text + craft notes
    ├── becoming.md
    └── ...
```

`voice.md` is the map. `pieces/` is the evidence. Both grow together.

---

## Skills in this repo

| Skill | Purpose |
|-------|---------|
| `voice-init` | Onboarding interview → builds a real voice profile from scratch |
| `voice-intake` | Add a piece, get craft analysis, update the profile |
| `voice-review` | Critique a draft against your established voice |
| `voice-map` | Synthesize the full collection (best after 10+ pieces) |
| `suno` | Generate Style Prompt + Lyrics for Suno AI Custom Mode |

The first four work together as a system. `suno` is standalone — use it anytime you want to generate a song for Suno, with or without the voice profile.

## Works with

Songs, poems, flash fiction, essays, prose poems, lyric essays — any short-to-medium form writing. The intake skill adjusts its analysis framework based on type.

---

## Tips

- **Run /voice-intake on old work first.** Feed in everything you've already written before using /voice-review on new drafts. The review is only as good as the profile, and the profile is only as good as the input.
- **Trust the borrowed imagery flag.** It's not an attack — it's the skill protecting your distinctive work from the familiar props.
- **The first 5 pieces are the foundation.** Choose pieces that represent your actual range, not your best work.
- **Re-run /voice-map periodically.** The synthesis shifts as more pieces are added.

---

## Built with

[Claude Code](https://claude.com/claude-code) slash commands. No external dependencies, no API keys, no configuration files. Just `.md` files in `~/.claude/commands/`.
