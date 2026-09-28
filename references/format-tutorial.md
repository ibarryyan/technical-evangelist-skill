# Format — Tutorial and Developer Education

A tutorial succeeds when the reader has a working result and understands why it
works. Confusion is a defect — the reader cannot debug your prose.

## Structure

```
Outcome promised (what they will have, and roughly how long it takes)
Prerequisites (exact versions, exact commands to verify them)
Step 1 → … → Step N   (each: action, expected result, what to do if it differs)
Mini-explanation (what just happened, now that it works)
Extend (one variation they can try alone)
Common mistakes and failure modes
Where to go next
```

## The rules

**Promise a result, then give it early.** State the outcome in the first two
lines: "You will have a working retrieval index over your own files in about
fifteen minutes." The first meaningful success should land within the first fifth
of the document.

**Prerequisites are exact.** Versions, not ranges. Include a command the reader
can run to check. "You will need Python 3.11+ and Node 20" plus
`python --version` and `node --version` with the expected output.

**Progressive complexity.** Mental model → minimal example → mechanism →
realistic example → advanced. Never open with the production-grade version.

**Every step shows its output.** If the reader cannot tell whether the step
succeeded, the tutorial is broken. Show the expected output — trimmed, with
elisions marked `…`.

**Every step says what happens if it goes wrong.** The two or three most likely
errors, with the fix. This is what distinguishes a tutorial that works from one
that merely reads well.

**One path through.** Do not offer alternatives mid-step. A single correct route
with notes for variation, not a decision tree. Choices belong in a section at the
end.

**Checkpoints.** Every few steps, a verification: "At this point you should see
X. If not, check Y." This bounds the reader's search space when a failure
happens later.

**No unexplained copy-paste.** Never ask the reader to run something opaque.
Either explain the line, or say "this is a standard X; we will come back to it".

## Code in tutorials

- Complete and runnable at each step. The reader must be able to run the code as
  shown, not assemble it from fragments.
- Show file paths and names explicitly. The reader's directory structure must be
  unambiguous at every point.
- Mark elisions clearly (`…`) and say what was elided.
- Explain *why* in comments, never *what*. The code says what.
- Avoid clever. Prefer obvious.

## Explanation blocks

After a step produces a result, explain what just happened — briefly, and in the
mental model established at the start. Two or three sentences. This is where
learning happens; skipping it produces readers who can copy but not adapt.

## Common mistakes section

List the errors readers actually hit, phrased as symptoms not causes:

> **`ModuleNotFoundError: no module named 'x'`** — you are in the wrong virtual
> environment. Run `which python` and confirm it points inside `.venv`.

Symptom-first, because that is what the reader has in front of them.

## Length

Tutorials are allowed to be long; they are not allowed to be padded. Cut
history, background, and vendor context unless it prevents a mistake. A tutorial
is a path, not a survey.

## Anti-patterns

| Anti-pattern | Why it fails |
|---|---|
| "Simply run …" | Nothing is simple to someone who has not done it |
| Skipped setup for "brevity" | The reader hits an error you never answered |
| Unversioned instructions | Breaks silently on the next release |
| Screenshots instead of text | Uncopyable, unsearchable, stale |
| Teaching three ways to do it | Reader stalls on the choice |
| Ending without a next step | Reader does not know what they now can build |
