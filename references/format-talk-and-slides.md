# Format — Technical Talk and Slide Deck

A talk is not an article read aloud, and a deck is not a talk. Design the talk
first; the slides serve it.

## Talk design

### Timing arithmetic

| Slot | Share | 30-min talk | 45-min talk |
|---|---|---|---|
| Opening — why care, what problem, what they will learn | ~8% | 2–3 min | 3–4 min |
| Problem and context | ~15% | 4–5 min | 6–7 min |
| Insight / thesis | ~10% | 3 min | 4–5 min |
| Technical explanation | ~30% | 9 min | 13 min |
| Demo | ~20% | 6 min | 9 min |
| Lessons and trade-offs | ~12% | 3–4 min | 5 min |
| Close and takeaway | ~5% | 1–2 min | 2 min |

Plan to run 85% of the slot. Overruns come from the demo, which always takes
longer than rehearsal.

### The first five minutes

The audience decides in five minutes whether to keep listening. Those minutes
must deliver, in order:

1. **Why this matters to them** — in their terms, not the technology's.
2. **What problem will be solved** — specific, demonstrable.
3. **What they will be able to do afterwards** — a concrete capability.

No agenda slide. No self-introduction longer than one sentence. No company
history.

### Storyline

```
Opening question / concrete failure
→ Problem
→ Insight (the thesis, said out loud)
→ Technical explanation
→ Demonstration
→ Engineering lessons, including what went wrong
→ Takeaway + call to action
```

### One idea

A talk carries **one** idea. Not three. If there are three, the talk is three
talks and will be remembered as none. Everything that does not serve the one
idea is cut, however good.

### Demo design

- Rehearse the demo three times, including one run offline.
- Have a recorded fallback. Live demos fail in front of audiences.
- Narrate what the audience should watch *before* it happens; they cannot read
  output and listen at once.
- Keep output on screen large enough for the back row.
- Bound the demo to the single behaviour the talk is about. Do not show the
  whole product.
- Have a pre-staged state. Never debug on stage.

### Speaker notes

For each section, write: what to say, what to show, the transition out. The
transition is what most speakers lose — the audience notices the gap between
sections more than the sections.

### Q&A preparation

Prepare for: the strongest technical objection, the "how is this different
from X" question, the scaling question, the cost question, and the one question
the speaker hopes nobody asks — prepare that one hardest.

Concede what is true. "That's a real limitation; here's where it bites" earns
more credibility than a defence.

## Deck design

### Slide budget

Roughly one slide per 60–90 seconds of talk: 20–30 slides for 30 minutes. Fewer
if the slides carry a lot each.

### One message per slide

Every slide has one primary message, expressed as the title. If the title is a
noun phrase ("Architecture"), the slide has no message yet — rewrite it as a
claim ("The router and the worker never share state").

```
Slide title (the claim)
Key message (one line, only if the title is not enough)
Evidence: diagram / code / number / example
```

### What to avoid on slides

- Paragraphs. If the audience is reading, they are not listening.
- Multiple unrelated ideas on one slide.
- More than about six bullets, and bullets longer than a line.
- Decorative architecture diagrams with unlabelled arrows.
- Full code files. Show the four relevant lines with context elided.
- Logo slides, thank-you slides, and "Questions?" as a final slide — end on the
  takeaway instead.

### Architecture slides

Show, in this order of usefulness: responsibility boundaries, data flow, runtime
behaviour, then deployment topology. Most architecture decks invert this and show
topology only, which tells the audience nothing about how the thing behaves.

### Deck output

When the deliverable is a deck, return:

1. Deck objective and target audience
2. Slide-by-slide: title, key message, content type, diagram/demo note
3. Speaker notes for the sections that need them
4. Demo plan with the fallback
5. Anticipated questions

Use `assets/talk-outline-template.md`.
