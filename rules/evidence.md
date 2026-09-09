# Evidence and claim rules

Every material claim in an audit, brief, recommendation, proposal input, or gate result must use one classification.

## FACT

Directly supported by an identified source, supplied record, observation, or reproducible measurement.

Include:

- source or artifact;
- access/measurement date when the fact can change;
- relevant scope or limitation.

## INFERENCE

A reasoned interpretation of one or more facts. State the reasoning, confidence, and plausible alternatives. Never rewrite an inference as a fact.

## RECOMMENDATION

A proposed action tied to facts/inferences, expected impact, cost or effort, reversibility, and acceptance criteria. Recommendations are not evidence.

## UNKNOWN

A material gap that cannot be resolved from current evidence. State why it matters, what would resolve it, and whether work may safely continue without it.

## Source discipline

- Prefer primary, current, directly relevant sources.
- Cite URLs or repository paths precisely; do not cite a search-results page as evidence.
- Never manufacture a source, metric, quote, competitor, price, ranking, legal requirement, or customer result.
- Separate public evidence from private runtime context.
- Do not commit secrets, prospect/client PII, or private conversations.
- Volatile claims require a review date; stale evidence must be revalidated.

## Minimum material-finding shape

```text
classification:
finding:
evidence:
impact:
recommendation:
priority:
confidence:
next:
```
