You are generating a comprehensive map of a writer's full body of work. This is the synthesis skill — read everything, find the through-lines, describe the shape. Best used after 10+ pieces, essential after 20+.

## Arguments
$ARGUMENTS

Arguments: optional. If a path is provided, use it as the project root. Otherwise use the current directory. If `--brief` is provided, produce a condensed version (skip collection arc depth, keep theme list and signature inventory).

---

## What to do

### Step 1 — Load everything

1. Read `voice.md` — the existing profile (if it exists, treat it as a starting point; your synthesis may extend, revise, or contradict it)
2. Read all files in `pieces/` — every piece in the collection
3. Note: total count, types (song/poem/etc.), date range if visible
4. If `style-taxonomy.md` exists in the project root, read it. Use the formal vocabulary it provides (narratological, prosodic, rhetorical, music-theoretic terms calibrated to this writer) to ground the synthesis in precise language where impression alone would be vague.

If fewer than 5 pieces exist, tell the user the map works best with more material — but proceed anyway with what's there.

---

### Step 2 — Map thematic territory

For each recurring theme or condition in the work, describe:

- **The condition** (not just a label — describe it as the writing actually renders it)
- **Which pieces** it appears in
- **How it develops** across the collection (does it deepen? shift angle? get resolved or left open?)
- **What's distinctive** about how *this* writer treats it (not the obvious take, but their specific angle)

Look for:
- Conditions the writer returns to repeatedly
- Conditions that appear once but at unusual depth
- Conditions that are conspicuously absent (what doesn't this writer write about?)
- How the "I" of the work relates to the conditions (inside/outside, naming/enacting, resolving/inhabiting)

---

### Step 3 — Inventory craft signatures

These are the fingerprints — formal and technical moves that recur enough to be characteristic. Not weaknesses, not generic strengths, but patterns that make this writing recognizable as this writer's.

For each signature:
- **Name it** (brief label)
- **Describe the move** (what actually happens in the text)
- **Cite 2–3 examples** with quotes
- **What it does** (why it works as a recurring strategy)

Common signature categories to check:
- Refrain behavior (does the chorus/refrain mutate on final pass? how?)
- Thesis delivery (how does the writer land the main claim — after pressure? plainly? as image? as question?)
- Speaker position (how does the "I" position itself relative to the condition?)
- Form-content mirroring (does structure enact subject?)
- Image types (abstract/concrete, domestic/cosmic, technical/vernacular)
- Endings (statement, image, question, trailing silence, irony)
- Register mixing (what vocabularies get combined?)
- Compression strategies (what gets omitted and why?)

---

### Step 4 — Assess formal range

Describe the full formal range of the collection:

- What types of pieces are present (song, poem, etc.)?
- What modes are represented (lyric, image inventory, dramatic monologue, satire, devotion, protest, etc.)?
- What's the range from most personal/interior to most outward/public?
- What formal experiments have been attempted? Which succeeded?
- What formal territory is *unexplored* — given this writer's strengths, what forms might they try next?

---

### Step 5 — Identify through-lines

A through-line is a pattern that cuts across many pieces and gives the collection coherence. Distinct from themes (which are subjects) — through-lines are structural or conceptual patterns.

Examples of through-lines (don't just use these — find the actual ones in this collection):
- The ghost turn: speaker questioning their own presence/reality
- Compulsive repetition as form enacting content
- Innocent/playful forms holding heavy content
- Withholding as subject: what is not said carries as much weight as what is
- A recurring image (particular object, setting, or gesture appearing in multiple pieces)

For each through-line:
- Name it
- Describe it precisely
- Cite which pieces it appears in
- Whether it deepens across the collection or remains consistent

---

### Step 6 — Describe the collection arc

Read the collection as a whole — not as a list but as a shape. What is the emotional journey?

- Where does it begin (the opening register, the first condition)?
- How does it move (what shifts, what deepens, what resolves)?
- Where does it land (the ending register, the final condition)?
- Is there a center of gravity — a piece or moment around which others orbit?
- Is the arc intentional or emergent?
- What would change the arc: what piece is missing that would complete or deepen the shape?

---

### Step 7 — Name the blind spots and unexplored territory

Honest assessment of what this body of work doesn't do (yet):

- Subjects conspicuously absent given the writer's apparent range and concerns
- Formal modes that match their strengths but haven't been attempted
- Registers that are thin or missing (they write interiority well — do they write the external world? They write doubt — do they write certainty? etc.)
- The thing the writer seems to be circling but hasn't written directly yet

This section is not a critique — it's a map of what's still possible.

---

### Step 8 — Deliver the synthesis

Structure the output:

```
## Voice Map: [Author / Collection Name if known]

**[N] pieces | [date range if visible] | [types: N songs, N poems, etc.]**

---

### Thematic Territory

[For each theme: condition description, pieces, development, distinctive angle]

---

### Craft Signatures

[For each signature: name, mechanism, examples with quotes, what it does]

---

### Formal Range

[Types, modes, range, experiments, unexplored territory]

---

### Through-Lines

[For each: name, description, pieces, development]

---

### Collection Arc

[Shape of the whole — beginning, movement, landing, center of gravity]

---

### Unexplored Territory

[Blind spots, missing subjects, possible next moves]

---

### Summary

[3–5 sentences: the writer's voice in its current state — what it does distinctively, what it's building toward, what makes it recognizable]
```

---

### Guidelines

- Quote liberally — this is a reading, and readings require evidence
- Don't produce a flattering profile. A map that only shows strengths is useless navigation
- The summary should be something the writer could hand to someone unfamiliar with the work and have them understand what they're about to read
- If the existing `voice.md` is wrong about something you've found — a theme it overclaims, a signature it misses — name the discrepancy directly and offer to update the file
