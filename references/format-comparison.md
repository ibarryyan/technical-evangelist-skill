# Format — Technology Comparison

A comparison is decision support, not a feature checklist. The question is never
"which is better" but "which is better *for this reader, under these
constraints*".

## Step 1 — Name the decision

Before comparing anything, write one sentence:

> The reader needs to decide whether to ______, given constraints ______.

If the user has not supplied the decision or the constraints, state the
constraints you are assuming and ask for correction. A comparison without a
decision context is a table nobody can act on.

## Step 2 — Choose dimensions from the decision

Do not use a fixed list. Select dimensions that can change the answer.

| Candidate dimension | Use when |
|---|---|
| Architecture / runtime model | The decision turns on how it behaves |
| Capability fit | One side genuinely cannot do the job |
| Complexity to adopt | Effort is a constraint |
| Performance envelope | Load or latency is the driver |
| Cost model | Shape matters more than magnitude — per-request vs per-seat |
| Operational burden | Who runs it, and what they must learn |
| Security / compliance | Data residency, permissions, audit |
| Ecosystem and maturity | Longevity risk |
| Developer experience | Time-to-first-success, iteration speed |
| Migration and exit cost | Switching in either direction |
| Scaling limits | Known ceilings |

Prune aggressively. Three dimensions that change the decision beat twelve that
do not.

## Step 3 — Evidence per cell

Every cell needs one of: a cited fact, a measured number, or a clearly marked
`[OPINION]`/`[UNVERIFIED]`.

- Do not put marketing copy in a cell.
- Where information is unavailable, write "not published" — do not leave it
  blank and do not guess.
- Version-pin anything behavioural. Comparisons go stale faster than anything
  else in technical writing.

Table shape:

| Dimension | A | B | What decides it |
|---|---|---|---|
| <dimension> | <evidence> | <evidence> | <the condition under which this dimension matters> |

The third column is what makes a comparison usable. A table without it is a
checklist.

## Step 4 — Scenario-based verdict

Never declare a universal winner. Instead:

```
If your constraint is <X>, choose A, because <mechanism>.
If your constraint is <Y>, choose B, because <mechanism>.
If <Z> holds, neither is a good fit; consider <alternative or the incumbent>.
```

This is the section readers quote. It also protects the author's credibility —
there is almost never a universal winner.

Include at least one scenario where the option you prefer loses. Readers trust
comparisons that have a losing condition stated.

## Step 5 — Total cost of adoption

The line item everyone forgets. State, in the reader's currency:

- Migration work, including the parts nobody scopes (data, tests, docs, CI)
- New operational responsibilities
- Training and ramp
- Ongoing maintenance of the integration
- Exit cost, if the choice proves wrong

A tool that is better on capability and worse on total cost may still be the
wrong choice. Say which one wins under which budget.

## Fair-comparison rules

- Compare like with like: same workload, same constraints, same configuration
  class. Do not compare a tuned instance of one against a default of the other.
- Cite each side's own documentation for its claims.
- Use the terminology each project uses for itself.
- When the user clearly prefers one option, still state the case against it. A
  comparison that always lands where the reader wanted is not a comparison.
- Distinguish "cannot" from "not supported in this version".

## Testing the comparison

Before returning it, ask:

1. Does a reader with a different constraint reach a different conclusion?
   If every reader reaches the same one, the comparison was unnecessary.
2. Could the losing side's maintainer object on factual grounds? If so, fix the
   cell or cite it.
3. Does the reader know what to do next, including how to reverse the decision?
