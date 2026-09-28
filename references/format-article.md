# Format — Technical Article

The default long-form deliverable. Return a complete, publish-ready draft unless
the user asks for an outline.

## Length budgets

| Length | Sections | Words | Use for |
|---|---|---|---|
| Note | 2–3 | 400–800 | One insight, one mechanism |
| Standard article | 4–7 | 1,500–3,000 | The default |
| Deep dive | 7–10 | 3,000–6,000 | Architecture, internals, a full case study |

More sections is not more value. Beyond roughly seven, most articles are two
articles sharing a title.

## Structure

```
Title
Opening (problem, concrete — 1–2 paragraphs)
Thesis (stated plainly, once)
Background / context
Mechanism (the core of the piece; most of the words live here)
Practice (how it is used, with a real example)
Trade-offs and boundaries
Takeaway + next action
```

Deviate when the thesis demands it — see `narrative-patterns.md` — but keep the
opening and the closing doing their jobs.

## Openings

Pick one. Two paragraphs maximum.

- **The failure.** Show the breakage. "At 40 tools, the descriptions alone were
  eating a fifth of the window before the user typed."
- **The reframe.** A claim the reader disagrees with, immediately earned.
- **The question.** Something the reader cannot answer but should be able to.
- **The number.** Only if sourced and genuinely surprising.

Never: "In today's fast-moving landscape", a definition, an agenda, a paragraph
about how important the topic is, or an apology for writing.

## Titles

Deliver three, ranked, whenever the article is for publication.

- Make a claim or name the tension. "Why your agent forgets: context as working
  memory" outperforms "An introduction to context management".
- Avoid colons stacking two topics, avoid "A Deep Dive into", avoid
  "Everything you need to know".
- No clickbait the article cannot pay off.

## Body

- **One idea per paragraph.** First sentence carries it.
- **Headings as an outline.** A reader skimming only the headings should still
  get the argument.
- **Alternate abstraction and concrete.** After every conceptual paragraph,
  land it with something specific: a function name, a log line, a diagram, a
  number.
- **Front-load.** Put the most useful material as early as the narrative allows.
  Readers leave; do not save the good part.
- **State the boundary explicitly.** "Use this when …; do not use it when …".
  This is the section most writers omit and most readers need.

## Code samples

- Minimal and runnable. Every sample should be executable by the reader with the
  stated prerequisites.
- Show the surrounding context needed to run it — imports, the function
  signature, the call site — but nothing else.
- Show real output, or clearly mark it illustrative.
- Use the language's idiomatic style. Non-idiomatic samples imply the author does
  not use the technology.
- One idea per sample. Comments explain *why*, not what the next line does.
- Pin the version the sample targets.

## Diagrams

One to three per article, at the points where prose is failing. Follow the
diagram discipline in `narrative-patterns.md`: one question per diagram, labelled
edges, and a sentence telling the reader what to notice.

## Closing

End with one of: the thesis, restated harder; a boundary statement; or a concrete
next action. No "In conclusion", no summary of the summary, no inspirational
close.

## Self-edit pass

Before returning the draft:

1. Delete the first paragraph. Did the article improve? Then it was throat-
   clearing — keep it deleted.
2. Read only the headings. Is that a coherent argument? If not, restructure.
3. Find every adjective describing the technology. Can it be replaced with a
   mechanism or a number? Replace or delete.
4. Find every claim. Tagged or sourced? If neither, cut it.
5. Find the thesis. Is it in the first fifth of the piece? If not, move it.
6. Search for banned phrases from `SKILL.md`. Remove.
