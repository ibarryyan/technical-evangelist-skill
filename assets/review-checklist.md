# Content Review Checklist

## Verdict

```
Artifact reviewed:
Declared audience:
Publish / revise / rewrite:

Accuracy        /5
Logic           /5
Audience fit    /5
Memorability    /5
Engineering value /5
Register        /5
Total           /30
```

A single 1 in **Accuracy** or **Logic** blocks publication regardless of total.

## Findings, prioritised

```
1. [BLOCKER]    <finding>  →  <fix>
2. [MAJOR]      <finding>  →  <fix>
3. [MINOR]      <finding>  →  <fix>
```

Order by effect on the reader, not by ease of fixing.

## By dimension

### Accuracy
- [ ] Every substantive claim is tagged or sourced
- [ ] Versions pinned for behavioural claims
- [ ] No invented implementation details, benchmarks, or adoption figures
- [ ] Assumptions stated
- [ ] Conflicting sources surfaced, not averaged
- [ ] Quotes verbatim and attributed

### Logic
- [ ] Causal chain from problem to conclusion is intact
- [ ] Every major section serves the thesis
- [ ] No unsupported jumps
- [ ] Limitations demonstrated, not asserted
- [ ] No internal contradictions

### Audience fit
- [ ] Depth matches the declared audience
- [ ] Vocabulary appropriate; terms glossed on first mention only
- [ ] Examples drawn from the audience's world
- [ ] No jargon used as a signal of expertise
- [ ] Mixed-audience pieces labelled and each tier self-sufficient

### Memorability
- [ ] One thesis, stated once, in the first fifth
- [ ] Quotable in one line
- [ ] Opening earns the next paragraph
- [ ] Closing is not a restatement of the introduction

### Engineering value
- [ ] Reader knows when to use it
- [ ] Reader knows when **not** to use it
- [ ] Trade-offs named, including the inconvenient one
- [ ] Next action is concrete
- [ ] Total cost of adoption addressed, where relevant

### Register
- [ ] No banned phrases (see `SKILL.md`)
- [ ] No empty introduction or generic conclusion
- [ ] No marketing language, invented urgency, or manufactured scarcity
- [ ] No AI filler or hedge stacking
- [ ] Human rhythm; varied sentence length

### Format compliance
- [ ] Matches the requested format exactly
- [ ] Length within the declared budget
- [ ] Code samples runnable and idiomatic
- [ ] Diagrams: labelled edges, one question each, accompanied by a sentence
      telling the reader what to notice
- [ ] Output language matches the request

## Corrected passages

Quote the original, then the fix. Do not rewrite the whole artifact unless asked
— the author needs to see *what* was wrong.

```
Original:  "<passage>"
Issue:     <which dimension, which defect>
Fixed:     "<passage>"
```

## What was done well

Name two or three things the draft does right. Reviews that only list problems
get discarded, and knowing what to keep matters as much as what to change.
