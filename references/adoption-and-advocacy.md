# Adoption and Advocacy

Explaining a technology and getting it used are different jobs. This file covers
the second one. Load it whenever the goal is uptake — launching a feature,
promoting an internal platform, encouraging migration, growing a community.

The rule that governs everything below: **adoption is a cost the other person
pays, not a favour they do you.** Every artifact must reduce their cost.

## The adoption ladder

Diagnose where the audience actually stands. Do not write step-4 content for a
step-1 audience.

| Step | State | They need | Wrong content |
|---|---|---|---|
| 1 · Awareness | Do not know it exists | A reason to care, in their terms | Architecture deep-dive |
| 2 · Understanding | Know it exists, unclear what it does | One clear mental model and a concrete use case | Feature list |
| 3 · Evaluation | Interested, assessing fit | Honest trade-offs, boundaries, comparison against the incumbent | Marketing claims |
| 4 · First use | Convinced, hitting friction | Shortest path to a working result | Background and history |
| 5 · Regular use | Using it, not yet fluent | Patterns, pitfalls, best practice | Introduction material |
| 6 · Advocacy | Fluent and happy | Material they can reuse to convince others | Anything aimed at them |

Most disappointing "evangelism" fails because it delivers step-2 content to step-3
audiences. Match the rung.

## Positioning statement

Fill this before writing anything adoption-oriented:

```
For <specific audience>
who <have this problem, and this workaround today>
<the thing> is <category>
that <the single most important benefit>
unlike <the incumbent>
it <the specific mechanism that produces the benefit>
```

Two rules:
- The benefit must be measured in the audience's currency — latency, cost, review
  time, incidents, headcount — not in the technology's own vocabulary.
- "Unlike the incumbent" is a mechanism, not a slur. Say what is different, not
  that the other thing is bad.

## Time to first value

The single strongest adoption lever is the length of the path from "interested"
to "it worked".

- State the first useful result up front: "You will have a working X in about
  ten minutes."
- Remove every prerequisite that is not strictly required for that first result.
- Reach the first success before explaining the design.
- Show the expected output at each step. Uncertainty is the main reason people
  abandon a tutorial.

## Handling objections

Write objections down in their strongest form, then handle them honestly.

| Objection type | Real question | How to answer |
|---|---|---|
| "It's immature" | Will it break under me? | Version status, production users you can cite, release cadence |
| "Too much migration cost" | What does switching cost me? | Concrete migration path, incremental adoption option, exit path |
| "Extra operational burden" | Who runs it at 3am? | Ops surface, failure modes, existing skills it reuses |
| "We already do this" | Is the delta worth it? | Name what the incumbent does well; show the specific gap |
| "Security / compliance" | Can I get it approved? | Data flow, permissions model, self-host option, audit trail |
| "Unproven at our scale" | Has anyone like us done it? | Closest comparable case; if none, say so |

Three rules:
- Concede what is true. Every objection contains something correct.
- Do not answer an objection with a feature list. Answer the question asked.
- If an objection has no answer for this audience, say so and describe who should
  not adopt it. This increases adoption among those who should.

## Differentiation without FUD

Legitimate: compare on named, verifiable dimensions; state the scenario where the
alternative wins; cite public documentation.

Not legitimate: fear, uncertainty, doubt; implied competitor failures; invented
weaknesses; uncited performance claims; "industry-leading" as a property.

If the honest comparison says the alternative is better for some readers, write
that. It is the fastest route to trust, and the readers it costs you were going
to churn anyway.

## Proof

Ranked by strength:

1. Reproducible benchmark with method and environment published.
2. Named production case study with numbers.
3. Migration write-up from a real team, including what went wrong.
4. Runnable demo the reader can execute themselves.
5. Reference architecture.
6. Vendor claim.

Prefer a runnable demo over any claim. It moves the reader from step 2 to step 4
in one action.

## Measuring

Useful signals, roughly in order of honesty: repeat usage, time to first success,
tutorial completion, issue quality (not volume), organic mentions from
non-employees, contribution rate.

Be sceptical of: page views, download counts, conference applause, internal
sign-offs without deployments.

## What never to do

- Manufacture urgency. "You'll be left behind" is not an argument.
- Claim universal suitability. A tool that fits everyone fits no one.
- Hide the cost. Hidden costs surface later as churn.
- Replace reasoning with enthusiasm.
- Write for the approving manager instead of the adopting engineer.
- Use AI-sounding filler: "seamless", "game-changing", "unlock", "supercharge".
