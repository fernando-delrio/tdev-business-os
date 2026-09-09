# Quality Gate — Evidence-backed Recommendation

A recommendation is ready for human decision only when all relevant checks pass.

## Evidence

- [ ] Material claims are labelled FACT, INFERENCE, RECOMMENDATION, or UNKNOWN.
- [ ] Facts have traceable sources or reproducible observations.
- [ ] Volatile evidence includes an access or measurement date.
- [ ] Unknowns and alternative explanations are visible.

## Decision quality

- [ ] The business/user outcome is explicit.
- [ ] The recommendation follows from cited facts and stated inferences.
- [ ] A smaller intervention and a no-action option were considered.
- [ ] Expected impact, effort, risk, reversibility, and confidence are stated proportionately.
- [ ] Acceptance criteria and the next decision owner are named.

## Boundaries

- [ ] No market, competitor, SEO, pricing, legal, or performance information is fabricated.
- [ ] Sensitive/private data is absent from committed artifacts.
- [ ] Business-specific assumptions are outside the reusable core.
- [ ] Required human or professional approval is explicit.

## Result

Return `PASS`, `PARTIAL`, or `BLOCKED`, followed by failed checks and the smallest action required to resolve them.
