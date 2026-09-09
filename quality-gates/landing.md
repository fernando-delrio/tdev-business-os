# Quality Gate — Landing / Commercial Website

A landing is ready to ship only when the relevant checks pass against production-like evidence.

## Inputs

- approved audience, offer, objective, and acceptance criteria;
- current implementation or preview;
- factual claims and proof sources;
- measurements/test results for applicable technical checks.

## Commercial

- [ ] A target customer can understand the offer quickly.
- [ ] Differentiation is specific and defensible.
- [ ] Proof supports important claims.
- [ ] The primary CTA has a clear next step.
- [ ] No section exists only because landing templates usually contain it.

## Experience

- [ ] Mobile is intentionally designed, not merely compressed desktop.
- [ ] Navigation, focus order, and interactive controls work with keyboard.
- [ ] Reduced-motion behavior exists for significant animation.
- [ ] Motion communicates hierarchy, state, or narrative rather than decoration.
- [ ] No unexpected layout shift, scroll jump, or interaction trap remains.

## Technical

- [ ] Performance has been measured on a production-like build.
- [ ] Heavy animation/assets have explicit budgets and fallbacks.
- [ ] Images/media are correctly sized and loaded.
- [ ] Metadata, canonical behavior, and crawl fundamentals are checked.
- [ ] Console/network errors are resolved or explicitly accepted.

## Content and trust

- [ ] Claims are factual and traceable.
- [ ] Contact and identity information are coherent.
- [ ] Privacy/cookie/legal treatment has been reviewed for the actual data flows and jurisdiction.
- [ ] Legal review is escalated where checklist-level risk identification is insufficient.

## Failure conditions

Return `BLOCKED` for a critical accessibility barrier, broken primary journey, unsupported material claim, unresolved sensitive-data risk, or missing required professional/human approval. Return `PARTIAL` when non-critical checks remain unmeasured or intentionally deferred.

## Output

Record `PASS`, `PARTIAL`, or `BLOCKED`, evidence for each applicable check, accepted exceptions, owner, and next action. Business-specific extensions belong in `implementations/<business>/quality-gates/`.
