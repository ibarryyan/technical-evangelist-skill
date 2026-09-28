# Audience Calibration

Depth is a dial, not a default. Fix the audience before drafting, then set
vocabulary, example choice, diagram type, and code presence from this table.

## The calibration table

| Audience | Already knows | Needs | Vocabulary | Code | Diagrams | Examples from |
|---|---|---|---|---|---|---|
| **Beginner** | Nothing of the domain | What it is, why it exists, a usable mental model | Plain language; define every term on first use | Little to none; tiny annotated snippets only | One simple conceptual picture | Everyday life, familiar tools |
| **Developer** | Programming, common tooling | How it works, the API surface, how to try it today | Standard domain terms, no definitions | Real, runnable, minimal | Component + flow | Their own stack |
| **Senior developer** | One stack deeply | Internals, limits, failure behaviour, what breaks at scale | Precise, no hedging | Real code with edge cases | Runtime behaviour, state transitions | Production incidents |
| **AI engineer** | Models, prompting, evals | Mechanism, cost/latency envelope, evaluation method | Canonical AI terminology | Real prompts, schemas, harness snippets | Data + control flow through the model | Eval results, token budgets |
| **Architect** | Multiple systems | Boundaries, runtime behaviour, scalability, reliability, security, trade-offs | Dense and precise | Interface signatures, config shape | Deployment and responsibility boundaries | Reference architectures |
| **Tech lead** | Delivery pressure | Effort, risk, migration path, effect on the team | Pragmatic | Migration or integration snippet | Before/after architecture | Team-scale rollouts |
| **CTO / EM** | Business and org context | Value, cost, risk, adoption difficulty, engineering impact | No implementation detail unless asked | None | Value chain or maturity curve | Cost, headcount, time-to-value |
| **General tech audience** | Varies widely | One idea that survives the ride home | Plain, vivid, non-condescending | None | One hero diagram | Widely known products |

## Choosing a depth level

Ask, in order:

1. **What will they do after reading?** Evaluate → architect depth. Implement →
   developer depth. Decide → manager depth. Understand → beginner depth.
2. **What is the cost of a wrong assumption?** High cost → under-assume and
   gloss. Low cost → go deeper and skip basics.
3. **What is their patience budget?** A conference talk permits one deep idea. A
   design doc permits twenty.

## Vocabulary policy

- **Gloss on first mention, never after.** `context window (the maximum number of
  tokens a model can consider at once)` — then use the bare term.
- **Prefer the canonical term.** Do not invent friendly synonyms for things the
  audience will meet under their real name; they need to search for it later.
- **Define by function, not by category.** "A tool call is how the model reaches
  outside itself" beats "a tool call is an abstraction primitive".
- **One term, one meaning, throughout.** Pick `agent` or `assistant` and stay
  with it.

## Common failure modes

| Failure | Symptom | Fix |
|---|---|---|
| Wrong depth | Explaining HTTP to an architect; assuming a reader knows what a token is | Re-run the three questions above |
| Fake beginner | Childish analogies for a senior audience | Keep the analogy, drop the tone |
| Manager deck with implementation | Config blocks in a CTO briefing | Move to an appendix or cut |
| Jargon as proof | Terms used to signal expertise rather than to carry meaning | Replace each with a functional definition or delete |
| Uniform treatment of mixed audiences | Everyone bored in different places | Split into a short "if you only read one paragraph" lead plus tiered sections |

## Mixed audiences

When one artifact must serve several audiences:

1. Lead with a **universal section** — problem and thesis, no prerequisites.
2. Add clearly labelled tiers: "For implementers", "For architects",
   "For decision-makers".
3. Keep the universal section self-sufficient. A CTO who stops after it should
   not feel cheated.

Never average two audiences. Averaging produces content that serves neither.
