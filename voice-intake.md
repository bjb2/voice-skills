You are adding a piece of writing to a living voice system. Your job is to perform deep craft analysis, save the piece with annotations, and update the master voice profile. The goal is to extract what makes this piece work (or not), how it connects to existing work, and what patterns are emerging or deepening.

## Arguments
$ARGUMENTS

Arguments: a file path to the piece (e.g., `./my-poem.md` or `pieces/draft.md`). If no path is given, ask the user to paste the piece directly in their next message and wait.

---

## What to do

### Step 1 — Load the piece

If a file path was provided, read the file. If the user pasted text, use that.

Determine:
- **Type:** song / poem / flash fiction / essay / prose poem / lyric essay / other
- **Approximate title** (from filename, or ask if unclear)
- **Rough form:** rhymed/unrhymed, lineated/prose, formal/free, etc.

---

### Step 2 — Load existing voice profile

Read `voice.md` if it exists in the current directory. If it doesn't exist, tell the user to run `/voice-init` first, then stop.

Scan `pieces/` to understand how many pieces already exist and what territory has been mapped.

---

### Step 3 — Deep craft analysis

This is the core work. Be specific — quote lines, identify mechanisms, resist general praise.

**For songs, analyze:**

*Structure*
- How many sections, what types (verse/chorus/bridge/etc.)
- Does the refrain behave consistently or mutate across returns?
- Does the final pass through the central phrase carry a changed variant, or just repeat?
- Is the structure earned — does it mirror what the song is doing emotionally?

*Imagery and language*
- What are the 2–3 images doing the most work? What makes them effective?
- Are there borrowed images (phrases the writer didn't invent, familiar props from pop culture or tradition)?
- What metaphors are present — are they consistent, or do they mix registers?
- What's the vocabulary register? (vernacular / literary / technical / slang)

*Emotional arc*
- Where does the song start emotionally and where does it land?
- Does the bridge genuinely shift something, or is it just a contrast section?
- Does the song earn its emotional payload, or announce it?

*Form-content relationship*
- Does the structure enact the subject? (circular refrain for paralysis; compressed lines for entrapment)
- Is there a moment where form and content are in tension? Is that tension productive?

*Delivery and rhythm*
- Where does the natural stress fall in the lines?
- Are there lines that feel awkward to sing/speak, or lines with natural musicality?
- Is there compulsive repetition — and if so, is it structural or just filler?

**For poems, analyze:**

*Form choice*
- What form is this? (free verse, formal meter, invented structure, image inventory, prose poem)
- Does the form earn itself — would a different form lose something, or would the same content work in prose?

*Mode*
- Lyric (speaker's interiority), image inventory (no "I", accumulated images), dramatic monologue (character voice), meditative, satirical, celebratory, other?
- Is the speaker inside or outside the condition being described?

*Speaker*
- First person or other? Singular or collective?
- Does the speaker have a consistent position, or do they shift (usefully or awkwardly)?

*Compression*
- What is being left out? Is the omission productive?
- Are there lines that over-explain what the images already do?
- What's the ratio of stated meaning to enacted meaning?

*Images*
- What are the 2–3 images that carry the most weight?
- Are any borrowed (familiar, from tradition, not invented)?
- Is there a standout image — one that does more than one thing simultaneously?

*Endings*
- How does the poem close? (statement, image, question, silence, gesture)
- Does the ending earn its finality, or does it trail off or over-explain?

**For prose (flash, essay, other):**

*Voice consistency*
- Does the prose voice stay consistent throughout? Where does it slip?
- Is the register appropriate to the subject?

*Structure*
- What does the structure do? (linear, circular, braided, fragmented)
- Are scene and summary balanced appropriately?

*Sentences*
- Rhythm variety — are sentences the same length throughout, or do they modulate?
- Any weak verbs propped by adverbs? Any filtering constructions ("she saw", "he noticed")?

*Key passages*
- Quote 2–3 sentences/passages that are doing the most work. What makes them effective?
- Quote 1–2 passages that need attention. What specifically is wrong?

---

### Step 4 — Connect to existing voice

Using what you found in `voice.md` and `pieces/`:

- **Thematic home:** Which existing territory does this sit in? Or is this new ground?
- **Deepening or new:** Does this deepen a pattern already present, or introduce something the writer hasn't done before?
- **Formal range:** Does this form match existing modes, or expand the range?
- **Through-lines:** Does this piece echo or respond to any existing piece? (Same condition from a different angle, same formal move, same image used differently?)
- **Signature moves present:** Which, if any, of the known signature moves appear here?
- **Borrowed imagery:** Any lines that feel like they came from somewhere else, not from this writer?

---

### Step 5 — Save the piece file

Create `pieces/<slugified-title>.md`:

```markdown
---
type: [song|poem|flash|essay|other]
created: [TODAY'S DATE]
tags: [writing, [type], [1-3 thematic tags]]
---

# [Title]

**Type:** [Song / Poem / etc.]
**Collection position:** [N of N] — update when you know total count

## Text

[Full text of the piece here]

## Craft Notes

[2–4 paragraphs of analysis. Be specific — quote lines. Explain mechanisms, not just impressions.]

[Paragraph 1: What the piece is doing structurally / formally]
[Paragraph 2: The strongest elements — standout images, moves that work]
[Paragraph 3: Weak spots or borrowed imagery if present; what to watch]
[Paragraph 4: How it connects to the rest of the work]

## Related

- [[voice]] — full voice profile
- [[piece-title]] — [why it connects]
```

---

### Step 6 — Update voice.md

Read the current `voice.md`. Make targeted, additive updates:

**Thematic Territory**
- If this piece introduces a new theme/condition: add it with a one-line description and cite the piece
- If it deepens an existing theme: add a note indicating the deepening ("also in [new piece]")
- Don't rewrite — expand and annotate

**Modes**
- If this piece uses a mode not yet documented: add it
- If it exemplifies an existing mode particularly well: note it

**Craft Strengths**
- If a new strength is visible: add it
- If an existing strength shows up again: leave it (it's already documented)

**Recurring Weak Spots**
- If borrowed imagery or other weak patterns appear: add or reinforce the note
- If a previously flagged weak spot is absent: note the improvement

**Signature Moves**
- If a new recurring pattern is visible for the second or third time: add it as a signature
- Don't add something from a single piece as a signature — wait for recurrence

**Works**
- Add: `N. "[Title]" ([type]) — [one-line description of what it does and where it sits]`

**Collection Arc**
- Update the arc description to incorporate this piece
- If this piece changes the emotional shape of the collection, describe how

---

### Step 7 — Report

Tell the user:
- What was saved and where
- The 2–3 most interesting things you found in the craft analysis
- Any patterns you noticed connecting to existing work
- Any weak spots flagged (be direct)
- What the addition means for the collection arc
