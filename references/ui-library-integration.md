# UI Library Integration Policy

Use component libraries as implementation resources, not as sources of identity. A library can accelerate a well-defined direction; it cannot supply the art direction.

## The three named libraries

- **AnimasterLib / Animmaster-style animated component collections:** use only for a small number of purposeful landing-page effects, scroll transitions, or pointer responses after the signature visual metaphor is defined. Verify the exact package, license, browser support, bundle cost, and reduced-motion behavior before adoption.
- **Skiper UI:** use as a source for uncommon shadcn-style structures, hero compositions, pricing/form patterns, or interaction scaffolds. Restyle and simplify them to the project design system. Never import a whole template because it looks premium in isolation.
- **Vengeance UI:** use selectively for distinctive interaction patterns such as displacement hover, animated tooltips, or scroll-linked moments. Apply only when the interaction explains product behavior and remains accessible.

## Additional React and motion resources

- **React Bits** — use for a small expressive moment such as a text reveal, a restrained entrance wrapper, or a custom pointer/hover treatment. It is an open collection, not a complete design system. Prefer copying the smallest component and adapting its DOM, type, color, and motion to the project rather than importing a visual package wholesale. For LedgerLens, a subtle staged reveal of the Reconciliation Line may be appropriate; animated headline gimmicks are not.
- **Aceternity UI** — use as a source of advanced React/Tailwind/Motion implementation patterns for one hero composition, background treatment, or carefully bounded interactive block. Its defaults often lean toward dramatic gradients and effects, so strip away anything that conflicts with the project’s material language. For LedgerLens, it may inform a restrained hero transition or evidence reveal, never a neon background or generic animated card wall.
- **Framer Motion / Motion** — use as the low-level motion engine when state transitions, layout choreography, presence, or gesture behavior genuinely improve comprehension. Define the project’s easing, duration, reduced-motion fallback, and interaction rules first. For LedgerLens, use it for source-line drawing, evidence-slip arrival, accordion/panel transitions, and a quiet decision-receipt confirmation. Do not use it to animate every card.
- **Motion Primitives** — use for small, composable motion primitives such as text, spotlight, scroll, accordion, or presence behavior when they reduce implementation time without imposing a second visual identity. Copy or adapt only the primitive that fits the locked system. For LedgerLens, use it for progressive disclosure and sequential methodology transitions, not for ornamental background effects.
- **OpenDesign** — use as an optional agent-agnostic design workspace and DESIGN.md workflow reference. Its useful lesson is that visual direction, reusable systems, real artifacts, and iterative preview should be explicit and portable across agents. For LedgerLens, use it to preserve DESIGN.md, screenshot review, and handoff evidence across Antigravity, Claude, Gemini, Kiro, Cursor, or another agent. Do not import OpenDesign’s visual identity, templates, or “vibe design” language into the product.

## Acquisition map: what to use for what

| Product need | Preferred resource | LedgerLens example | Do not use it for |
|---|---|---|---|
| Base components and accessible controls | Existing project UI kit / Radix / shadcn-style primitives | Buttons, tabs, fields, dialogs, accordion | Replacing the brand system |
| Signature visual metaphor | Build in-house first; optionally use Framer Motion or Motion | Reconciliation Line and redline | Importing a pre-made hero |
| Hero composition reference | Skiper UI or Aceternity UI, heavily adapted | Layout inspiration for landing hero | Copying a complete template |
| Small expressive animation | React Bits | One restrained trace reveal | Repeated animated text everywhere |
| State and layout animation | Framer Motion / Motion | Evidence panel, decision receipt, panel transitions | Decorative motion on every element |
| Composable scroll/presence primitive | Motion Primitives | Methodology stage reveal, progressive disclosure | A second visual language |
| Portable design-system workflow | OpenDesign | Keep DESIGN.md, references, previews, and evidence portable | Treating an agent workspace as the product’s brand |
| Advanced hover or pointer moment | Vengeance UI or React Bits | A subtle source-line inspection cue | Essential navigation or keyboard-only actions |
| Uncommon landing block | Skiper UI | Adapted section structure | Full template import |
| Heavy cinematic / background effects | None by default | Only if it clarifies the trace | Neon, noise, or 3D for its own sake |

The exact resources are references and implementation accelerators. They are not automatically dependencies. Before acquiring any component, inspect its license, bundle cost, browser support, accessibility behavior, reduced-motion behavior, and maintenance status. Prefer copying a small, understandable component over adding a large package.

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

> Explore the named libraries and React/motion resources only after art direction is locked. Use them as implementation references, not as the project’s brand. Build the project signature first, then borrow the smallest number of accessible, performant components that reinforce it. For every borrowed component, state the product reason, route, visual adaptation, accessibility behavior, performance cost, licensing, and fallback. If a library component conflicts with the design system, reject it.
