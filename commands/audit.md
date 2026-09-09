# Command — `/audit`

Run an evidence-first commercial audit of a business, URL, or current business asset.

This file specifies an operator command; v0.2 does not include a command parser.

## Required inputs

- audit subject: business name, URL, or artifact;
- desired business outcome;
- market/location when relevant;
- available evidence and its provenance;
- current business configuration or explicit statement that it is unavailable.

Optional: known pain, analytics, discovery notes, constraints, and desired depth.

## Routing

The orchestrator selects only the necessary path:

1. `opportunity` establishes the business/customer context and evidence quality.
2. `business-audit` diagnoses the opportunity.
3. `growth-experience` joins when a site, funnel, discoverability, or content question exists.
4. `delivery-risk` joins only for feasibility or delivery-readiness questions.

Use `landing-quality` and `quality-gates/landing.md` when the audited artifact is a commercial landing. Business-specific overlays may add checks but must not alter the generic gate.

## Output

- scoped executive diagnosis;
- evidence ledger using FACT / INFERENCE / RECOMMENDATION / UNKNOWN;
- customer journey and opportunity map when supported;
- prioritized findings;
- keep / change / do-not-build;
- discovery questions and material unknowns;
- recommended next action;
- acceptance criteria if implementation follows.

Use `templates/evidence-brief.md` when a durable artifact is requested.

## Failure conditions

- No identifiable subject or outcome: request clarification.
- Insufficient evidence: return unknowns and an evidence-gathering plan, not a confident diagnosis.
- Private/sensitive input cannot be stored safely: keep it in runtime context and sanitize the artifact.
- Request crosses pricing, legal, external communication, destructive, or deployment approval boundaries: stop before action.

## Done when

The result passes `quality-gates/recommendation.md`, sources are traceable, uncertainty is visible, and the next decision belongs to a named human or workflow step.
