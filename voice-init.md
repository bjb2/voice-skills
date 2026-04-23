You are setting up a voice-mapping system for a creative writer. This system builds a living map of their writing voice through craft analysis — tracking themes, formal patterns, signature moves, and blind spots across every piece they write. The map becomes useful after 5+ pieces and invaluable after 20+.

## Arguments
$ARGUMENTS

Arguments: optionally, the path to a first piece to intake during setup (e.g., `./my-poem.md`). If omitted, just create the structure and explain the system.

---

## What to do

### Step 1 — Check for existing system

Look for `voice.md` in the current directory.

- **If found:** report the current state (how many pieces in `pieces/`, when last updated) and stop. Don't overwrite. If a piece path was provided, run `/voice-intake` instead.
- **If not found:** proceed to Step 2.

---

### Step 2 — Create the structure

Create the `pieces/` directory (for individual piece files).

Create `voice.md` in the current directory:

```markdown
---
created: [TODAY'S DATE]
updated: [TODAY'S DATE]
---

# Writing Voice

## Thematic Territory

*To be built as pieces are added. This section maps the interior world — what conditions, states, and subjects the writer returns to, and at what angles.*

## Modes

*What formal moves the writer makes: lyric song, image inventory, dramatic monologue, essay, prose poem, etc. How they differ and what they share.*

## Craft Strengths

*Patterns that work reliably — structural moves, image types, line-ending strategies, emotional delivery methods.*

## Recurring Weak Spots

*What slips in when the writer isn't paying attention: borrowed imagery, over-explained emotion, familiar props. Worth flagging when they appear.*

## Signature Moves

*Distinctive patterns that recur across pieces — not weaknesses, not just strengths, but fingerprints. The things that make the writing recognizably theirs.*

## Works

*To be built as pieces are added.*

## Collection Arc

*How the body of work reads as a whole — not just a list but a shape. The emotional journey across all the pieces.*
```

---

### Step 3 — Intake first piece (if provided)

If a file path was given in arguments, run the full intake process (same as `/voice-intake`):
- Read the file
- Determine type (song / poem / flash / essay / other)
- Perform craft analysis
- Create `pieces/<slugified-title>.md`
- Update `voice.md` with what this first piece reveals

---

### Step 4 — Explain the system

Tell the user:

```
Voice system initialized.

How it works:
- Each time you add a piece with /voice-intake, it gets craft-analyzed and voice.md updates
- The profile gets sharper with each piece — patterns that look like one-offs become signatures
- After ~10 pieces you'll have a map of your actual voice, not the voice you think you have

Commands:
  /voice-intake <path>   Add a piece, extract craft notes, update the profile
  /voice-review <path>   Critique a draft against your established voice
  /voice-map             Synthesize the full collection (best after 10+ pieces)

Run /voice-intake next with your first piece (or paste it directly).
```
