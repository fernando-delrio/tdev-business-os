# T·DEV Quality Gate — Cinematic Landing Intro

Apply this business-specific extension after the generic [`landing` gate](../../../quality-gates/landing.md) when the approved T·DEV cinematic intro is present.

## Interaction contract

- [ ] Scroll progress deterministically controls timeline/video progress.
- [ ] Stopping scroll stops the sequence.
- [ ] Reverse scroll reconstructs the same state exactly.
- [ ] Skip, deep-link, restored-scroll, load-failure, and reduced-motion paths expose the real landing safely.

## Visual hand-off

- [ ] The real landing DOM remains beneath the intro surface.
- [ ] The final intro state aligns with the landing reveal without a generic black fade.
- [ ] No pose crossfade, ghosting, visible media rectangle, or unintended crop appears.
- [ ] Motion and reveal preserve the approved T·DEV visual direction.

## Delivery evidence

- [ ] Desktop behavior has been inspected on a production-like build.
- [ ] Mobile containment and safe-area behavior are explicit and verified.
- [ ] Media weight, preload behavior, seeking performance, and fallbacks are measured or documented.
- [ ] Relevant automated tests and manual reverse-scroll checks pass.

## Boundary

This gate records readiness; it does not authorize deployment. Production publication requires explicit human approval.
