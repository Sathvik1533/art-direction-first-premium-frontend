# Art Direction First — Premium Frontend System

A reusable, agent-agnostic workflow for creating original, premium websites and product interfaces without falling into generic AI-generated frontend patterns.

This repository is designed to be handed to Antigravity, Claude Code, Gemini, Cursor, or another AI builder alongside a project brief and reference links. It does not force every project to share one visual style. It makes the **art-direction process** reusable while keeping each project’s visual identity original.

## What problem it solves

AI frontend agents often jump from a feature list directly to familiar cards, pills, gradients, dashboards, and default typography. The result may work technically but feel generic, visually disconnected, or obviously AI-generated.

This system forces a better sequence: diagnose the product, define its emotional premise and visual world, analyze references as principles, produce multiple visual concepts, reject generic output, lock a project-specific design system, prove it on one marketing surface and one real workflow, then propagate and verify.

## Quick start

1. Give the AI agent `SKILL.md`.
2. Fill `templates/project-brief.template.md` with the project truth, references, UI direction, assets, icons, fonts, and quality bar.
3. Ask the agent to analyze the references using `references/reference-analysis.md`.
4. Require three screenshot-ready visual concepts before full implementation.
5. Select one concept and ask the agent to create the project-specific `DESIGN.md` from `templates/design-system.template.md`.
6. Build one landing or entry surface and one real product workflow.
7. Review desktop and mobile screenshots.
8. Propagate the approved system across the remaining routes.
9. Run `references/qa-checklist.md` and return evidence, limitations, and a stable preview URL.

## Three mandatory protections

### Avoid the AI slope

The agent must define a visual world, emotional premise, signature metaphor, typography, spacing, materials, voice, and anti-patterns before full implementation. It must reject font/color swaps that do not create a distinctive visual identity.

### Use references as principles

The project owner provides three to seven references. The agent records what to borrow, where it applies, and what not to copy. References are not templates and must never produce a collage of copied websites.

### Let the project choose its UI language

The project owner may specify editorial, tactile, cinematic, utilitarian, spatial, neo-brutalist, soft, glass, or another direction. The agent must justify the choice against the product’s trust, readability, audience, and workflow. Morphism is not a default effect.

## UI libraries

`references/ui-library-integration.md` explains how to evaluate libraries such as AnimasterLib/Animmaster-style animated collections, Skiper UI, and Vengeance UI. Use them as implementation resources only, after art direction is locked. Do not import component libraries wholesale or let default components override the project identity.

## Repository files

| File | Purpose |
|---|---|
| `SKILL.md` | Core agent instructions and mandatory workflow |
| `templates/project-brief.template.md` | Project-specific inputs supplied by the user or team |
| `templates/design-system.template.md` | Project-specific design system created after concept selection |
| `references/reference-analysis.md` | Reference research and anti-copy method |
| `references/ui-library-integration.md` | Safe use of animation/component libraries |
| `references/qa-checklist.md` | Visual, functional, responsive, and accessibility QA |

## Non-negotiable principle

> Never begin a full frontend implementation from a feature list alone. First create a product world. Then prove it on one entry surface and one real workflow before scaling it.

## License

Add the license chosen by the maintainers before public distribution. Review third-party component and asset licenses separately; this repository does not grant rights to external references or libraries.
