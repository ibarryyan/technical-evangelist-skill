# Research and Accuracy

Correctness is the precondition for everything else. A memorable article that is
wrong is a liability with reach.

## Source hierarchy

Prefer, in order:

1. **Official documentation** for the exact version in question.
2. **Official engineering blogs / changelogs / release notes.**
3. **Source code and repository history** — the tiebreaker when docs and
   behaviour disagree.
4. **Specifications and RFCs.**
5. **Peer-reviewed or preprint papers.**
6. **Maintainer talks and conference sessions.**
7. **High-quality technical publications** with named authors.
8. **Aggregators, listicles, AI-generated summaries** — leads only, never
   citations.

## When to research

Research when any of these hold:

- The user asks for current information, or says "latest", "now", "2026".
- The topic changes faster than a training cycle: model versions, framework
  APIs, pricing, limits, feature availability.
- A version number, a benchmark, or a market-share figure would appear in the
  output.
- You are about to write a claim you could not point to a source for.

Do not research to confirm general concepts you can reason about correctly. Do
research before writing down any number.

## Verification checklist

For each technical claim entering the output:

- [ ] Version and date are pinned. "As of <tool> <version>, <date>" — not
      "currently".
- [ ] Official terminology is used, exactly as the vendor writes it.
- [ ] The claim is about behaviour, not intentions. "The docs describe X" is not
      "X ships".
- [ ] Deprecation and preview status are stated. Anything experimental is
      labelled.
- [ ] Conflicting sources are surfaced rather than averaged.
- [ ] Quotes are verbatim and attributed.

## Claim tagging

Tag substantive claims so the reader knows what stands on evidence.

| Tag | Meaning | Requirement |
|---|---|---|
| `[FACT]` | Verifiable; sourced | Cite the source |
| `[INFERENCE]` | Derived from cited facts | Show the reasoning chain |
| `[OPINION]` | Judgement or recommendation | Own it as the author's |
| `[UNVERIFIED]` | Plausible, not checked | Say so plainly |

Rules:
- Never let an inference read as a fact. The gap between "this design implies X"
  and "the team says X" is where credibility dies.
- Never turn a hypothesis into a prediction.
- If a claim cannot be tagged confidently, cut it or mark it `[UNVERIFIED]`.
- Do not tag trivia — tag anything a reader might repeat to someone else.

## Citation format

Cite inline at the point of the claim, not in a bibliography at the end.

- Add a link to the official page for the specific version where possible.
- For behaviour that differs between versions, cite each version.
- For numbers, cite the source *and* its measurement date.
- Say what the source is when the link is not self-evident: "per the v2.3
  migration guide".
- Do not cite an aggregator when the primary source exists. Find it.

## The gap test

In the workflow's "build the model" step, some slots will not fill. For each
empty slot:

1. **Is it knowable?** → research it.
2. **Is it knowable but out of scope?** → state the assumption and move on.
3. **Is it genuinely unknown or contested?** → say so in the text. An honest
   "the vendor has not published this" is worth more than a confident guess.

Never fill a slot with fluent-sounding placeholder prose. That is the single
most common failure mode of AI-assisted technical writing.

## Boundaries of what to produce

- Do not write benchmarks you did not run or cite.
- Do not attribute adoption or market share without a source.
- Do not describe a competitor's internals beyond what is publicly documented.
- Do not reproduce proprietary code or non-public material.
- When the user's own claim appears wrong, say so in the review output — with
  the evidence — rather than softening it.
