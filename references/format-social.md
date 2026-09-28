# Format — Social, Short-Form, and Release Notes

Short formats are not simplified long formats. They are their own discipline: one
idea, a hook that earns the next line, and no room to recover from a vague
opening.

## Threads and post series

```
Post 1  — Hook: the claim, the failure, or the number. Must stand alone.
Post 2  — Why it matters / what is broken today
Post 3–6 — The mechanism, one idea per post
Last    — Takeaway + link or next action
```

Rules:
- **One idea per post.** If a post has two, split it.
- **Each post must survive being read alone.** People arrive mid-thread and
  quote single posts out of context.
- **Front-load the value.** No "let me explain", no "a thread 🧵" before any
  substance.
- **No manufactured hooks.** "Nobody talks about this" is a claim; only use it if
  you can show it is true.
- **Length follows the idea.** Do not pad to hit a target count.

## Short technical posts

Useful shapes:

- **The bug and the cause.** Symptom → wrong hypothesis → actual cause → fix.
  High value; readers recognise themselves.
- **The mental model.** One analogy that maps cleanly onto a real mechanism.
- **The number.** A measurement, with method and conditions stated.
- **The correction.** "I used to believe X; here is what changed my mind."

Every one of these needs a specific detail — a line of code, an error message, a
measurement. Abstract short posts read as noise.

## Release notes and changelogs

Structure each entry as four lines, in this order:

```
What changed   — in the user's terms, not the implementation's
Why it matters — what it now makes possible, or what it fixes
Who is affected — which versions, which configurations
What to do     — the upgrade action, or "no action required"
```

Rules:
- Lead with the user-visible change, not the internal refactor.
- Breaking changes go first and are labelled explicitly.
- Include the migration snippet where one exists.
- Distinguish "deprecated" (still works, will not later) from "removed" (does not
  work now).
- Do not pad with "we're excited to announce". The reader wants the four lines.
- Link to the full documentation for the version.

## Announcement posts

```
The problem, in the reader's terms
→ What we built (one paragraph, concrete)
→ What it changes for them (the mechanism, not the adjective)
→ How to try it (a command, a link, a time budget)
→ Honest limitations
```

Include the limitations. An announcement with no stated limits reads as
advertising and gets discounted accordingly.

## Payload discipline

Whatever the format:

- Every claim still carries the tag discipline from
  `research-and-accuracy.md`. Short form is not exempt from accuracy.
- No claim in a hook that the body does not pay off.
- Numbers require a source and a date.
- If the piece needs a disclaimer to be honest, the piece is wrong — rewrite it.

## What to cut

- Emoji used as punctuation rather than structure.
- "Let that sink in", "Read that again", "This changes everything".
- Emoji-numbered lists that bury a real sequence.
- Claims of novelty without a comparison point.
- Engagement bait that asks a question the piece does not answer.
