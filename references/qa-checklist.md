# Premium Frontend Visual and Functional QA Checklist

Use this checklist after the two-surface proof and again after full propagation. Record evidence, not assumptions.

## Art direction

- [ ] The product has a named visual world and one-sentence emotional premise.
- [ ] The result is recognizable without the logo.
- [ ] Typography has clear display, interface, and data roles.
- [ ] Scale and whitespace are intentional rather than empty or cramped.
- [ ] A signature metaphor expresses product truth and is not decorative noise.
- [ ] The marketing page and core workflow clearly belong to the same product.
- [ ] Reference sites informed principles but were not copied.
- [ ] The page does not default to generic AI SaaS patterns.

## Interface quality

- [ ] Navigation and active states are clear.
- [ ] Primary and secondary actions have consistent hierarchy.
- [ ] Tables, forms, charts, and evidence blocks use the design system.
- [ ] Icons have a coherent family and meaningful purpose.
- [ ] Status is not communicated by color alone.
- [ ] Copy is specific, readable, and free of unnecessary AI/implementation jargon.
- [ ] Loading, empty, error, success, disabled, and retry states are authored.

## Functional quality

- [ ] Core happy path works with real data or honest demo state.
- [ ] Core failure paths are visible and recoverable.
- [ ] Existing API/database/backend behavior remains intact.
- [ ] Direct routes load correctly.
- [ ] No blank root or unhandled runtime error appears.
- [ ] Persistence and refresh behavior are verified where claimed.
- [ ] Destructive or consequential actions are safe and clearly labeled.

## Responsive and accessible quality

- [ ] Desktop target viewport verified.
- [ ] Tablet target viewport verified.
- [ ] 375px mobile verified.
- [ ] 320px mobile verified.
- [ ] No horizontal overflow.
- [ ] Keyboard-only navigation verified.
- [ ] Visible focus verified.
- [ ] Screen-reader names/labels verified.
- [ ] Contrast verified against actual rendered surfaces.
- [ ] 200% zoom verified.
- [ ] Reduced-motion behavior verified.
- [ ] Touch targets are usable.

## Evidence to return

Return a preview URL, screenshots of the concept gate and final routes, a route-by-route matrix, known limitations, and a list of claims that are illustrative or unverified. Never mark PASS solely because a build or typecheck succeeded.
