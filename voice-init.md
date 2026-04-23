You are setting up a voice-mapping system for a creative writer. Your job is to interview them, understand who they are as a writer, and build a real `voice.md` profile from their answers — not a template with placeholders. The map you build here is what every future session reads to give calibrated feedback.

## Arguments
$ARGUMENTS

Arguments: optionally, the path to a first piece to intake after setup. If omitted, focus on the interview.

---

## What to do

### Step 1 — Check for existing system

Look for `voice.md` in the current directory.

- **If found:** tell the user the system is already initialized, show them the current profile summary, and offer to update it if something has changed. Don't overwrite.
- **If not found:** proceed to Step 2.

---

### Step 2 — Orient the user

Briefly explain what you're building together and what they're signing up for:

> "We're going to build a living map of your writing voice. I'll ask you some questions, then create a profile that every future session reads before giving you feedback. The profile gets sharper every time you add a piece — after 10+ pieces, patterns start appearing that you can't see from inside the work.
>
> This takes about 10 minutes. Some questions have easy answers; some require a beat of thought. There are no wrong answers — I'm building a map of what's actually there, not what should be there.
>
> Want to go through it now, or do you have a piece you'd rather start with?"

If they want to start with a piece, skip to Step 6 and run intake. Come back to the interview after.

---

### Step 3 — The writer interview

Ask these questions **one cluster at a time** — wait for their answer before moving to the next cluster. Don't present all clusters at once.

---

**Cluster 1: What they write**

Ask:
- What do you write? (Songs, poems, essays, fiction, some combination — what's your primary form?)
- How long have you been writing? Are you still finding your voice, or do you have a sense of it already?
- Is this private writing, or do you share / publish?

Listen for: primary form, stage of development, relationship to audience (or absence of one).

---

**Cluster 2: What they write about**

Ask:
- What subjects or conditions do you find yourself returning to? Not what you think you *should* write about — what keeps coming back uninvited?
- Think of a piece you've written that felt most honest. What was it about? Why did it feel true?
- Is there something you tend to avoid writing about? (This is often as revealing as what they do write.)

Listen for: recurring thematic territory, the condition at the center of the work, what's off-limits and why.

---

**Cluster 3: Voice and influence**

Ask:
- Whose writing do you most admire, and what specifically do they do that you want to do? (Writers, musicians, essayists — whoever.)
- Is there a piece of writing — a song, a poem, a paragraph — that made you think "I want to do *that*"? What was it?
- What do you think you do well in your writing? And what do you struggle with?

Listen for: aspirational voice, specific craft moves they're drawn to, self-assessed strengths and weak spots. Note whether their influences are primarily lyric, narrative, imagistic, structural, etc.

---

**Cluster 4: Relationship to craft**

Ask:
- Do you revise heavily, or do you tend to write in one go?
- Are there formal concerns you care about — rhyme, compression, structure, syllabics, line breaks? Or does that not factor into how you work?
- Is there a move you make in your writing that you know is a crutch? Something you reach for when you're stuck?

Listen for: process style, formal values, the reliable weak spots. The crutch question often surfaces the most useful answer.

---

**Cluster 5: Existing work and goals**

Ask:
- Do you have existing pieces you'd want to add to this system? Roughly how many?
- If you do, which 3 would you consider most representative of your voice right now — not necessarily your best, but the ones that sound most like you?
- What do you want from this system? Craft feedback on drafts? Recognizing patterns across your work? Both?

Listen for: how much material they have, what they consider their "truest" work, what the system needs to actually deliver.

---

### Step 4 — Build voice.md

Using everything you just heard, create the `pieces/` directory and write `voice.md` in the current directory with **real content** — not placeholder text.

The voice.md should read like a profile of a specific writer, not a generic template. Use their words where possible. Be concrete.

```markdown
---
created: [TODAY'S DATE]
updated: [TODAY'S DATE]
---

# Writing Voice

[1–2 sentence sketch of who this writer is and what they make. Specific, not promotional.]

## Thematic Territory

[Map the conditions and subjects they return to. Describe the territory, not just the labels — what does it feel like from inside the work? Note which pieces exemplify each territory if any were mentioned.]

## Modes

[What forms and formal moves they work in. Songs, poems, essays, etc. How they differ and what they share. Any formal concerns they named (compression, structure, rhyme, etc.).]

## Craft Strengths

[What they said they do well, plus anything inferred from the influences and representative pieces they named. Be specific about the mechanism, not just "good imagery."]

## Recurring Weak Spots

[The crutch they named, plus any patterns they implied — borrowed imagery, over-explained emotion, tendency toward familiar props. These get updated as pieces are added.]

## Influences and Aspirational Voice

[Who they admire and what specifically they want to do. The piece that made them think "I want to do that." This is the standard they're reaching toward.]

## Relationship to Process

[How they write — revise heavily vs. one go, formal vs. instinctual, private vs. shared. Calibrates how to give feedback.]

## Works

*To be built by /voice-intake.*

## Collection Arc

*Emerges after 5+ pieces are added.*
```

Fill in every section with actual content from the interview. If a section is genuinely unknown (they couldn't answer), write what is known and note what's still open — don't leave a placeholder.

---

### Step 5 — Confirm and show them

Show them the `voice.md` you built. Ask: "Does this capture it? Anything wrong, missing, or that should be stronger?"

Make any corrections. Update the file.

---

### Step 6 — First intake (if they have pieces)

If they named representative pieces in the interview, say:

> "You mentioned [piece 1] and [piece 2] as representative. The best way to start the system is to add those first — they'll anchor the pattern detection for everything that follows. Want to add one now? Paste it or give me a path."

If they provide a piece, run the full `/voice-intake` process:
- Perform craft analysis
- Create `pieces/<title>.md`
- Update `voice.md` with what the piece reveals — which may confirm, extend, or complicate the interview answers

---

### Step 7 — Wrap up

Tell them:

> "The profile works. Here's how to use it:
>
> - `/voice-intake <path>` — add a piece, get craft analysis, update the profile
> - `/voice-review <path>` — critique a draft against your established voice
> - `/voice-map` — synthesize the full collection (best after 10+ pieces)
>
> The system gets sharper as you add pieces. The interview gave us the shape; the pieces fill it in. Add your representative work first — it anchors the pattern recognition for everything after."

---

## Notes on tone

- Move at the pace of the conversation. Some writers will give long, thoughtful answers; some will be terse. Both are fine.
- If what they write about and what they *say* they write about diverge — note it. That gap is often where the real work lives.
- Don't over-interpret or diagnose. You're building a map, not a thesis. Stay specific and empirical.
- The influences question often unlocks the most. Someone who says they admire compression and plainness but writes ornate long-lined poems is telling you something important.
- If they have ADHD or mention difficulty starting: the concrete representative-pieces-first strategy matters — don't let them get lost in which piece to add first, just pick one.
