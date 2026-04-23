You are generating a formal academic calibration of a writer's voice. Your job is to produce a precise, field-grounded specification — the kind a literary critic or music theorist could use as a vocabulary guide when analyzing this body of work. Two parts: a reference parameter sheet (definitions of the relevant terms), then a calibration (this writer's work mapped onto those terms).

## Arguments
$ARGUMENTS

Arguments: optional. If a path is provided, use it as the project root. Otherwise use the current directory.

---

## What to do

### Step 1 — Load the evidence

1. Read `voice.md` — the living voice profile
2. Read all files in `pieces/` — every piece in the collection
3. Note what types of writing are present: songs, poems, flash fiction, lyric essays, dramatic monologues, image-inventory pieces, satire, etc.

If `voice.md` does not exist, tell the user to run `/voice-init` first and stop.

If fewer than 5 pieces exist, note this and proceed — the calibration will be preliminary.

---

### Step 2 — Determine which academic domains apply

Before writing anything, assess what fields are actually evidenced in the work:

- **Poetics / Prosody**: include if any verse or song lyrics — meter, rhyme, stanza form, line behavior
- **Narratology**: include if any narrative structure, speaker positioning, or story-time manipulation is present — even lyric "I" positioning counts
- **Stylistics / Rhetoric**: include for any writing — sentence-level, figure-level, register analysis
- **Genre Theory**: include if the work crosses or plays with genre signals
- **Music Theory / Musicology**: include only if songs are present with specified or implied musical form, tempo, texture, or production
- **Semiotics of Music**: include only if musical topic theory or isotopy analysis is warranted
- **Popular Music Genre Taxonomy**: include only if songs are present

Omit any section with no evidence in the actual work. The parameter sheet should reflect this writer's actual range, not a complete textbook index.

---

### Step 3 — Write Part 1: Academic Parameter Sheet

For each domain that applies, write a focused parameter sheet: the terms and definitions a critic would need to analyze this body of work precisely. Do not reproduce a complete textbook chapter — only include terms that are actually relevant to what this writer does.

Format each section:

```
### [Domain Name]

- **[Term]**: [definition, concise, precise]
- **[Term]**: [definition]
...
```

Include 6–20 terms per domain, selected for relevance. A term is relevant if you expect to use it in Part 2. If you can't see yourself using a term in the calibration, leave it out.

---

### Step 4 — Write Part 2: Calibration

Map this writer's actual work onto the parameter sheet. Each section should read like a scholar's characterization of a specific, named writer — not a generic description. Quote lines and cite pieces.

Required sections (use only those whose domain appeared in Part 1):

**Genre / Mode**
- Principal mode and generic dominant
- Subgenre crossings and hybridity moves
- Generic contract the reader is asked to accept

**Narratology**
- Narrator type (homodiegetic/heterodiegetic, person, reliability)
- Focalization type and range
- Narrative distance and dominant discourse mode
- Duration and frequency signatures

**Poetics / Prosody**
- Metrical base (accentual? syllabic? which feet or stress patterns?)
- Line length tendency and compression strategies
- Rhyme type and scheme preferences
- Enjambment vs. end-stopping
- Anaphora and refrain behavior — especially: does the refrain mutate on final pass?
- Sound texture: alliteration, assonance, consonance patterns
- Stanza form norms and deviations

**Stylistics / Rhetoric**
- Register and its range
- Diction (Anglo-Saxon vs. Latinate, concrete vs. abstract, monosyllabic vs. polysyllabic)
- Syntactic mode: parataxis vs. hypotaxis, sentence types
- Cohesion strategy: what ties the text together
- Trope inventory: which tropes recur, at what structural weight
- Scheme inventory: which arrangement figures recur
- Modality and stance
- Characteristic deviation types (graphological, dialectal, register-crossing)

**Semiotics / Topic**
- Dominant topical register
- Isotopies: what semantic planes run through the collection
- Markedness: what features stand out against the unmarked norm

**Music Theory / Production** *(if songs present)*
- Dominant song form
- Tempo range and feel
- Implied modal/tonal character
- Texture type
- Vocal delivery taxonomy
- Production aesthetic range
- Structural device signatures

**Form-Content Relation**
- Where structure enacts subject — name the specific moves, quote the pieces
- Any self-imposed formal constraints

**Characteristic Weak Spot**
- The recurrent stylistic risk zone — the place where the voice slips into borrowed language or underpowered imagery. Be specific: quote an example if one exists.

---

### Step 5 — Write the summary paragraph

One paragraph, final section of the document. Formal vocabulary throughout — precise enough to hand to another critic as a spec. Should name the dominant mode, metrical base, syntactic habit, dominant tropes/schemes, isotopy, and signature formal device. Around 100–150 words.

---

### Step 6 — Save to style-taxonomy.md

Write the full document to `style-taxonomy.md` in the project root. Use this structure:

```
---
type: knowledge
created: [today's date]
updated: [today's date]
tags: [writing, voice, taxonomy]
---

# Style Taxonomy & Calibration

[brief framing line: what this document is and what evidence it draws from]

---

## Part 1: Academic Dimensions by Field

[parameter sheet — only relevant sections]

---

## Part 2: [Writer's Name / The Collection]'s Style Calibration

Evidence drawn from: [list pieces by short title]

[calibration sections]

---

## Summary

[the single formal paragraph]

---

## Related

- [[voice]] — impressionistic voice profile; this document is the formal counterpart
- [[writing-voice]] — if present
```

After saving, tell the user:
- The file has been saved to `style-taxonomy.md`
- What sections were included (and which were omitted and why)
- That `/voice-review` and `/voice-map` will now load this vocabulary automatically

---

### Guidelines

- Quote lines from the actual pieces. Claims need evidence.
- Use the academic vocabulary precisely — if you use "homodiegetic," it should be because the narrator is in the story, not as decoration.
- The calibration is about *this* writer, not a writer in general. Every statement should be falsifiable against the actual work.
- If the evidence is thin on a parameter (fewer than 3 pieces touching it), flag the uncertainty: "appears in limited samples."
- Do not include sections that have no evidence. A music-theory section for a writer with no songs is noise.
- The summary paragraph should be quotable as a critical characterization — formal, exact, no hedging.
