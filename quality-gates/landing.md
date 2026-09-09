# Quality Gate — Landing / Commercial Website

A landing is not ready to ship until the relevant checks pass.

## Commercial
- [ ] A target customer can understand the offer quickly.
- [ ] Differentiation is specific and defensible.
- [ ] Proof supports important claims.
- [ ] Primary CTA has a clear next step.
- [ ] No section exists only because landing-page templates usually have it.

## Experience
- [ ] Mobile is intentionally designed, not merely compressed desktop.
- [ ] Navigation and focus behavior work with keyboard.
- [ ] Reduced-motion behavior exists for significant animation.
- [ ] Motion communicates hierarchy/narrative rather than decoration.
- [ ] No unexpected layout shifts or scroll jumps.

## Technical
- [ ] Performance has been measured on a production-like build.
- [ ] Heavy animation/assets have explicit budgets/fallbacks.
- [ ] Images/media are correctly sized and loaded.
- [ ] Metadata, canonical behavior and crawl fundamentals are checked.
- [ ] Console/network errors are resolved.

## Content / trust
- [ ] Claims are factual.
- [ ] Contact/identity information is coherent.
- [ ] Required privacy/cookie/legal treatment has been reviewed for the actual implementation.

## T·DEV cinematic intro extension
When the intro is present:
- [ ] scroll progress deterministically controls timeline progress;
- [ ] reverse scroll reconstructs the sequence correctly;
- [ ] stopping scroll stops the sequence;
- [ ] transition reveals the real landing without a generic black fade;
- [ ] final intro frame aligns with the landing handoff;
- [ ] no obvious pose crossfade/ghosting;
- [ ] desktop remains fluid;
- [ ] mobile strategy is explicit;
- [ ] reduced-motion fallback is explicit.