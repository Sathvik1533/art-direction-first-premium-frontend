# Art Direction First — Premium Frontend System

A reusable, agent-agnostic workflow for creating original, premium websites and product interfaces without falling into generic AI-generated frontend patterns.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

This repository can be handed to Antigravity, Claude Code, Gemini, Cursor, or another AI builder alongside a project brief, reference links, and the existing project constraints. It does not force every project to share one visual style. It makes the **art-direction process** reusable while keeping each project’s visual identity original.

## Why this exists

AI frontend agents often jump from a feature list directly to familiar cards, pills, gradients, dashboards, and default typography. The result may work technically but feel generic, visually disconnected, or obviously AI-generated.

This system changes the order of operations. It starts with product truth, emotional premise, and brand point of view. It treats reference websites as principles rather than templates. It requires multiple visual concepts, screenshot-based rejection of generic output, a project-specific design system, a two-surface proof, and independent visual and functional QA before full propagation.

## The workflow

1. Give the agent `SKILL.md`.
2. Fill `templates/project-brief.template.md` with product truth, users, workflow, constraints, references, UI direction, assets, icons, fonts, and quality bar.
3. Analyze three to seven references using `references/reference-analysis.md`.
4. Define a project-specific emotional premise, visual world, distinct voice, signature metaphor, material language, and anti-pattern list.
5. Produce three materially different, screenshot-ready visual concepts at desktop and mobile widths.
6. Reject generic concepts and select one direction.
7. Create the project-specific `DESIGN.md` using `templates/design-system.template.md`.
8. Build one landing or entry surface and one real product workflow as a two-surface proof.
9. Review screenshots and revise before full propagation.
10. Apply the locked system to the remaining routes by page responsibility.
11. Run `references/qa-checklist.md` and return evidence, limitations, screenshots, and a stable preview URL.

## Three mandatory protections

### Avoid the AI slope

The agent must define a visual world, emotional premise, signature metaphor, typography, spacing, materials, voice, and anti-patterns before full implementation. A font or color change is not art direction. The result must be recognizable without the logo and must not default to generic SaaS patterns.

### Use references as principles

The project owner provides three to seven references. The agent records what to borrow, where it applies, and what not to copy. References are not templates. The result must not become a collage of copied layouts, colors, wording, illustrations, or animations.

### Let the project choose its UI language

The project owner may specify editorial, tactile, cinematic, utilitarian, spatial, neo-brutalist, soft, glass, or another direction. The agent must justify the choice against the product’s trust, readability, audience, and workflow. Morphism is never a default effect.

## UI libraries and animation

`references/ui-library-integration.md` explains how to evaluate animated and component libraries such as AnimasterLib/Animmaster-style collections, Skiper UI, and Vengeance UI. Use them only after the project art direction is locked. Select the smallest number of accessible and performant components that reinforce the project’s identity. Never import a full template or let a library’s default styles define the brand.

## Repository map

| Path | Purpose |
|---|---|
| `SKILL.md` | Core agent instructions and mandatory workflow |
| `templates/project-brief.template.md` | Project-specific inputs supplied by the user or team |
| `templates/design-system.template.md` | Project-specific system created after concept selection |
| `references/reference-analysis.md` | Reference research and anti-copy method |
| `references/ui-library-integration.md` | Safe use of animation/component libraries |
| `references/qa-checklist.md` | Visual, functional, responsive, and accessibility QA |
| `CONTRIBUTING.md` | Contribution and maintenance guidelines |
| `NOTICE.md` | Scope, responsibility, and third-party reference notice |
| `LICENSE` | MIT License |

## How to use it with an AI agent

Give the agent the repository or the contents of `SKILL.md`, then provide a completed project brief. Say:

> Use this repository as the art-direction and premium frontend workflow for this project. Follow the phases in order. Do not skip product diagnosis, reference analysis, the three-concept visual gate, or the two-surface proof. Do not treat a font/color change as art direction. Do not copy reference websites. Create one original visual world for this project, document it in `DESIGN.md`, prove it on one entry surface and one real workflow, then propagate it and perform independent visual, functional, responsive, and accessibility QA.

## What this repository does not promise

This repository is a process, not a guarantee of visual quality or production readiness. Project owners and implementing agents remain responsible for validating product claims, accessibility, performance, security, backend behavior, data integrity, deployment, and third-party licenses.

## Open-source status

This repository is released under the **MIT License**. You may use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the materials, subject to the terms in `LICENSE`.

The MIT License applies to this repository’s original documentation, templates, and workflow. Reference websites, external assets, fonts, icons, and third-party UI libraries mentioned in the documentation remain subject to their own licenses and terms.

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md) for contribution guidance. Improvements should make the process more useful, more agent-agnostic, more accessible, more honest, or more resistant to generic AI output.
