# Quality Rubric

Use for content reviews, and as a self-check whenever a draft feels weak but the
cause is unclear. Score each dimension 1–5, then act on the lowest score first —
raising a 2 fixes more than polishing a 4.

## Scoring anchors

### 1. Technical accuracy

| 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|
| Every claim tagged and sourced; versions pinned; assumptions explicit; limits stated | Claims correct, minor sourcing gaps | Correct overall; some claims unsourced or unversioned | Contains at least one factual error or invented detail | Multiple errors, or confident claims about unverifiable behaviour |

### 2. Logical structure

| 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|
| Single causal chain from problem to conclusion; every section load-bearing | Clear structure, one or two loose sections | Recognisable structure but sections drift from the thesis | Assertions without support; reader cannot reconstruct the argument | Sections contradict each other |

### 3. Audience fit

| 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|
| Vocabulary, examples, and depth exactly match the declared audience; terminology glossed on first use | Well targeted, occasional over- or under-explanation | Broadly aimed, mixed depth | Written for the wrong audience | Written for the author |

### 4. Memorability

| 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|
| One thesis, stated once, quotable in one line; reader could repeat it tomorrow | Clear thesis, slightly buried | Thesis present but generic | No identifiable thesis | Several competing theses |

### 5. Engineering value

| 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|
| Reader knows when to use it, when not to, what it costs, and the next action | Trade-offs and takeaway present | Takeaway vague; boundaries missing | Informational only; no decision support | Actively misleading about fit |

### 6. Register and style

| 5 | 4 | 3 | 2 | 1 |
|---|---|---|---|---|
| Precise, human rhythm; no filler, no marketing, no AI tics | Clean with a few weak sentences | Noticeable filler, padding, or hedging | Marketing language or heavy AI cadence | Unreadable, or reads as generated |

## Interpreting the total

| Total (max 30) | Verdict |
|---|---|
| 26–30 | Publish as is. |
| 20–25 | Publish after fixing the lowest dimension. |
| 14–19 | Substantial revision; usually the thesis or the audience is wrong. |
| Below 14 | Rewrite. Do not patch. |

Never average away a 1. A single score of 1 in accuracy or logic blocks
publication regardless of the total.

## Defect catalogue

Fast diagnosis for the most common problems.

| Defect | Tell | Fix |
|---|---|---|
| Orphan thesis | Sections do not support the opening claim | Rewrite the thesis to match what the piece actually says, or cut the sections |
| Definition opener | Starts with "X is a …" | Move the problem first; the definition goes second |
| Listicle drift | Section count grows; each adds a new topic | Cut until each section serves the thesis |
| Adjectival vagueness | "powerful", "robust", "flexible" | Replace with the mechanism or a number |
| Asserted limitation | "doesn't scale" with no evidence | Add the specific number or scenario |
| Borrowed authority | "experts agree", "widely adopted" | Cite a source or delete |
| Dead analogy | Analogy that breaks where the technology works | Discard or state the boundary |
| Decorative diagram | Boxes are nouns, arrows unlabelled | Redraw around one runtime question, or delete |
| Buried lede | Best insight is in section 6 | Move it to section 1 |
| Hedge stack | "may potentially help in some cases" | Commit, or state the condition |
| Circular close | Conclusion restates the intro | Close with a boundary or a next action |
| Tone mismatch | Playful language in an incident post-mortem | Rewrite for the audience's register |

## Review output format

Return the dimensions scored, then the prioritised findings, then the corrected
passages. Do not rewrite the whole piece unless asked — the author needs to see
*what* was wrong as much as the fix.

Use `assets/review-checklist.md` for the structure.
