# Skill — landing-quality

## Responsibility

Evaluate a landing page as a commercial product and engineered experience, not merely as a visual composition.

## Inputs

- landing URL, build, screenshots, or source repository;
- target audience, offer, and primary conversion objective;
- approved brand/experience constraints;
- available analytics, user evidence, test output, and performance measurements.

## Dimensions

1. Positioning and message clarity.
2. Narrative and information architecture.
3. Trust and verified proof.
4. Conversion path and CTA friction.
5. UX and responsive behavior.
6. Visual differentiation and brand coherence.
7. Accessibility.
8. Performance and Core Web Vitals risk.
9. SEO fundamentals.
10. Technical maintainability.

Animation must have an interaction contract. For scroll-driven work, evaluate progress mapping, reversibility, pause behavior, mobile fallback, reduced motion, and layout-shift constraints. Reject decorative effects that weaken clarity or performance; do not impose any particular brand aesthetic in this reusable skill.

## Output

For every material issue, use the shape in `rules/evidence.md`. Then provide:

- top five changes by leverage;
- explicit keep list;
- change and do-not-build lists;
- implementation acceptance criteria;
- pre/post measurement plan;
- applicable `quality-gates/landing.md` result when delivery readiness is requested.

## Boundaries

- Do not infer user behavior from visual inspection alone.
- Do not claim measured performance, rankings, or conversion without evidence.
- Do not redesign a working brand direction without authorization.
- Do not treat aesthetic novelty as business value.
- Apply business-specific quality overlays only when explicitly loaded from `implementations/<business>/`.

## Failure conditions

Return a constrained heuristic review when audience, offer, objective, analytics, or production-like measurements are unavailable. Label the missing context and do not present hypotheses as validated behavior.

## Evidence requirements

Cite inspected artifacts, viewport/environment, measurement method, and date. Separate observed defects from conversion hypotheses and recommendations.

## Quality criteria

Findings are reproducible, prioritized by user/business impact, protective of successful design, implementable without guessing, and honest about unmeasured outcomes.
