# Narrative Patterns

Choose the structure *after* the thesis. Never reuse one structure by reflex —
the structure that carried the last article usually flattens the next one.

## Selecting a structure

| Thesis looks like | Audience goal | Structure |
|---|---|---|
| "The current approach breaks at scale, so X exists" | Understand a new solution | A — Problem driven |
| "X is unfamiliar and widely misunderstood" | Build a mental model | B — Concept explanation |
| "X is the latest step in a long trend" | Place it in context | C — Evolution |
| "We shipped X and learned Y" | Transfer experience | D — Case study |
| "A or B, depending on your constraints" | Make a decision | E — Comparison |
| "The common objection to X is wrong because Y" | Change a held position | F — Objection led |
| "You can get value from X in ten minutes" | Reach first success | G — Build along |

---

## A — Problem driven

Use for most technical articles and talks.

```
Problem → Existing approach → Limitation → New approach
→ Mechanism → Practice → Trade-offs → Conclusion
```

Discipline: the limitation must be *specific and demonstrated*, not asserted.
"Doing this manually doesn't scale" is weak. "At 40 tools, the tool
descriptions alone consume ~12% of the context window before the user has typed
anything" is a limitation.

## B — Concept explanation

Use for unfamiliar technology.

```
What → Why → Mental model → Architecture → Example → Limitations
```

The mental model does the heavy lifting. Pick one, state it once, then reuse it
consistently for the rest of the piece. Two competing metaphors in one document
is a defect.

## C — Technology evolution

Use for emerging technology, and for explaining *why now*.

```
Past → Problem → Evolution → Current architecture → New challenges → Direction
```

Rules: no unsupported predictions. Mark forward-looking statements as
`[OPINION]` or `[UNVERIFIED]`. Distinguish "this exists today" from "this is
expected to arrive".

## D — Case study

Use for real engineering experience.

```
Background → Problem → Constraints → Decision → Implementation
→ Result → Lessons
```

Rules: separate `[FACT]` (what happened, with numbers where you have them) from
`[OPINION]` (what you concluded). Constraints are the interesting part — a
decision made without constraints is not a decision, it is an accident. Include
at least one thing that went wrong.

## E — Comparison

Use when the user must choose. Full playbook in `format-comparison.md`.

```
Decision framing → Dimensions → Evidence per dimension
→ Scenario-based verdict → Migration and exit costs
```

Do not declare a universal winner unless the user supplied the evaluation
framework.

## F — Objection led

Use to shift an existing position, and throughout adoption-oriented work.

```
Name the objection fairly → Show why it exists → Evidence against it
→ What is actually true → Revised decision rule
```

Rules: state the objection in its strongest form. A straw man is detected
instantly and costs all credibility. Concede the part of the objection that is
correct before addressing the rest.

---

## G — Build along

Use when the goal is time-to-first-success, not comprehension.

```
Outcome promised → Prerequisites → Smallest working step
→ Verify → Extend → Explain what just happened → Where to go next
```

The first working result should arrive within the first fifth of the document.
See `format-tutorial.md`.

---

## Storytelling technique

### Mental models

When a concept resists explanation, build a model the audience already owns.

Weak:

> Context management controls the information available to the model.

Strong:

> Think of context as the agent's working memory. The problem is not that the
> model cannot hold more, but that everything in there competes for the same
> limited attention.

Rules for a model:
- It must map onto the real mechanism, not merely resemble it.
- It must break in the same places the real thing breaks. If it survives a
  scenario the technology fails, it is misleading.
- Introduce it once and reuse it. Do not replace it mid-piece.

### Analogy test

Before using an analogy, ask: **where does this analogy stop being true?**
If you cannot answer, do not use it. If you can answer, consider stating it —
"this breaks down once you have more than one writer" — which turns a weakness
into credibility.

### Concrete beats abstract

| Abstract | Concrete |
|---|---|
| Skills improve capability reuse | User task → discovery → load SKILL.md → context built → agent executes |
| Latency improved | p99 dropped from 1.8s to 420ms after batching the embedding call |
| Better developer experience | The config went from 40 lines to 3 |

Concrete does not mean numeric. It means *specific*. A named function, an actual
error message, a real sequence of steps.

### Openings

Open with one of:
- **A concrete failure.** Show the thing breaking.
- **A sharp counterintuitive claim.** Then earn it.
- **A question the audience cannot answer but should be able to.**
- **A number that reframes the problem.**

Never open with: "In today's fast-moving landscape", "As we all know", "X has
become increasingly important", a definition, or an agenda slide.

### Closings

Close with one of:
- The thesis restated in a way that lands harder than the first time.
- A concrete next action the reader can take today.
- The boundary: "use this when …, not when …".

Never close with "In conclusion", a summary of the summary, or an invitation to
"embrace the future".

---

## Diagram discipline

Propose a diagram when structure, flow, or boundaries matter more than prose.
Skip it when a sentence suffices.

| Medium | Use when |
|---|---|
| Inline SVG / rendered widget | Teaching, presenting, or when visual hierarchy matters; anything the user will screenshot |
| Mermaid | Repository docs, PRs, anything that must live as text and stay editable |
| ASCII | Terminal context, commit messages, comments in code |

Every diagram must answer one question: *components, data flow, control flow,
runtime lifecycle, or responsibility boundary.* A diagram that answers none is
decoration.

Rules:
- Label the edges, not just the boxes. Unlabelled arrows are noise.
- Do not draw a box per buzzword.
- Keep it to one idea. Two ideas → two diagrams.
- Diagram the *runtime*, not just the boxes — most architecture diagrams fail by
  showing deployment topology when the reader wanted to know what happens during
  a request.
- Accompany every diagram with one sentence stating what the reader should
  notice in it.
- Follow the region's conventions for anything involving maps or geographic
  data.
