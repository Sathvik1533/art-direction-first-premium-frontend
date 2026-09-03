# UI Library Integration Policy

Use component libraries as implementation resources, not as sources of identity. A library can accelerate a well-defined direction; it cannot supply the art direction.

## The three named libraries

- **AnimasterLib / Animmaster-style animated component collections:** use only for a small number of purposeful landing-page effects, scroll transitions, or pointer responses after the signature visual metaphor is defined. Verify the exact package, license, browser support, bundle cost, and reduced-motion behavior before adoption.
- **Skiper UI:** use as a source for uncommon shadcn-style structures, hero compositions, pricing/form patterns, or interaction scaffolds. Restyle and simplify them to the project design system. Never import a whole template because it looks premium in isolation.
- **Vengeance UI:** use selectively for distinctive interaction patterns such as displacement hover, animated tooltips, or scroll-linked moments. Apply only when the interaction explains product behavior and remains accessible.

## Selection rule

Do not use all three libraries by default. First identify the page job and the product truth the interaction should communicate. Then select zero, one, or a small number of components that fit the locked project design system.

For every proposed library component, record:

| Question | Required answer |
|---|---|
| Product reason | What does this interaction help the user understand or do? |
| Page fit | Which route and moment needs it? |
| Brand fit | How will it express this project’s visual world rather than the library’s default style? |
| Accessibility | What happens with keyboard, reduced motion, touch, and screen readers? |
| Performance | What is the bundle/rendering cost and fallback? |
| Licensing | Is use and redistribution permitted? |
| Removal test | Does the product still feel authored if the effect is removed? |

## Anti-component-soup rules

Reject a library component when it is only decorative, when it introduces a second visual language, when it requires generic gradients or glass panels, when it delays the primary action, when it harms content density, or when the same effect appears on multiple routes without a product reason.

Use one or two signature interactions more than ten unrelated animations. The project’s own metaphor, materials, typography, spacing, and status language must remain dominant.

## Agent instruction

Tell the receiving AI agent:

> Explore the named libraries after art direction is locked. Use them as implementation references only. Do not treat their defaults as the project’s brand. Build the project signature first, then borrow the smallest number of accessible, performant components that reinforce it. If a library component conflicts with the design system, reject it.
