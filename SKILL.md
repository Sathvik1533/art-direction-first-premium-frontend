---
name: art-direction-first-premium-frontend
description: Agent-agnostic art direction and premium frontend workflow. Use when any AI builder must create or redesign a website, web app, dashboard, landing page, or product UI and the user wants an original, polished, non-generic visual identity.
---

# Art Direction First — Premium Frontend System

Use this skill to prevent generic AI frontend output. It is designed to be handed to any capable agentic AI—Antigravity, Claude Code, Gemini, Kiro, Cursor, Windsurf, OpenAI coding agents, or another builder—alongside a project brief and reference links. The workflow is tool-agnostic: when one agent lacks a tool, perform the equivalent action available in that environment and document the limitation. It does not prescribe one aesthetic. It makes the process reusable while keeping every project’s identity original.

## Non-negotiable inputs

Require the project owner or agent to provide these before implementation:

1. **Project truth:** product, users, job-to-be-done, primary workflow, domain constraints, existing code/data/API boundaries, and what must remain functional.
2. **Reference set:** three to seven carefully selected URLs or assets. For each, specify what to study and what not to copy.
3. **UI direction:** preferred interface mode or morphism, such as editorial, tactile, cinematic, utilitarian, spatial, neo-brutalist, soft, or not yet decided.
4. **Asset preferences:** logo/brand assets, imagery, illustration, icon family, chart style, motion tolerance, font constraints, and licensing constraints.
5. **Quality bar:** competitor or benchmark level, target devices, accessibility expectations, and what would make the result feel generic or unacceptable.

If inputs are missing, infer only low-risk details and explicitly record assumptions. Do not invent product claims, testimonials, benchmarks, assets, or brand history.

Use `templates/project-brief.template.md` to collect inputs. Read `templates/agent-handoff.template.md` for the universal handoff, `templates/asset-and-icon-brief.template.md` for project assets and motion, `references/reference-analysis.md` when evaluating references, `references/ui-library-integration.md` when considering animation/component libraries, and `templates/design-system.template.md` when locking the selected direction. Use `docs/CROSS_AGENT_ADAPTER.md` when the chosen agent lacks a particular tool and `docs/VISUAL_CONCEPT_SCORECARD.md` when comparing concepts.

## Core principle

Never begin a full frontend implementation from a feature list alone. First convert product truth into an emotional premise, a visual-world name, a distinct voice, a signature visual metaphor, a material and interaction language, a page-expression map, and an anti-pattern list.

The goal is not “make it modern.” The goal is a product world that is recognizable without the logo and remains coherent from marketing pages to real product workflows.

## Mandatory workflow

### Phase 0 — Diagnose before designing

Inspect the existing project, routes, data states, and constraints. Identify what is real, what is placeholder, and what must not be changed. Separate frontend art direction from backend/API/database work. Define the primary user anxiety or desire and the product’s emotional premise.

Write a short diagnosis covering what the product is, who it is for, what it must feel like, what it must never feel like, which workflow proves the product, and which constraints are binding.

### Phase 1 — Analyze references as principles

Study three to seven references. For each, record the visual strength to borrow, the page behavior it informs, and the elements explicitly not to copy. Do not create a collage of websites. References provide principles, not templates.

Choose a reference role for each page type only when useful. Keep one project identity across all pages; vary the expression by page purpose.

### Phase 2 — Create the art direction

Define and name one visual world. Specify the brand thesis and emotional premise, distinct voice and copy rules, locked typography roles, palette with semantic meaning, scale/grid/spacing/whitespace logic, surface/material language, signature metaphor or visual object, button/navigation/icon/status/data-display language, motion and reduced-motion principles, state language, marketing-to-product relationship, and explicit anti-patterns.

Do not let a preferred “morphism” become a blanket effect. Select a restrained material language that supports trust, readability, and interaction. Glassmorphism and neumorphism are not defaults and must be rejected when they reduce contrast, clarity, or brand distinctiveness.

### Phase 3 — Visual concept gate

Before redesigning every route, create three materially different, screenshot-ready visual concepts. Each concept must include a desktop and mobile landing/entry surface, one complete real product workflow or core screen, typography, palette, material, signature visual, CTA, evidence/content treatment, motion cue, rationale, and risks.

Do not submit three color variations of one layout. Score concepts for distinctiveness, emotional premise, typography, scale, whitespace, metaphor, product relationship, usability, originality, and mobile integrity. Reject anything that is merely a safe SaaS dashboard, a font/color swap, or a copied reference.

Do not proceed until one concept is selected and recorded in the project’s `DESIGN.md` using `templates/design-system.template.md`.

### Phase 4 — Two-surface proof

Implement only two surfaces first: the landing or entry experience and one complete real product workflow. Use real project content and actual data states. Prove that the marketing world and product world share the same visual DNA. Capture desktop and mobile screenshots. Revise the art direction if the two surfaces feel like separate products.

### Phase 5 — Propagate by page responsibility

Apply the locked system to all remaining routes, reusing primitives. Keep identity consistent but vary behavior:

| Page responsibility | Typical expression |
|---|---|
| Marketing landing | Editorial, atmospheric, memorable |
| How it works | Narrative, explanatory, sequential |
| Evidence/details | Documentary, transparent, source-led |
| Dashboard | Summary-focused, calm, scannable |
| Queue | Dense, operational, fast to scan |
| Detail/workspace | Evidence-led, contextual, decision-focused |
| Ingestion/forms | Procedural, reassuring, state-rich |
| Audit/history | Chronological, archival, trustworthy |
| Settings | Contractual, precise, explicit |
| Docs | Structured, searchable, readable |

Do not force a hero layout onto an operational route or make every page a card grid.

### Phase 6 — Independent visual and functional QA

Test the live result, not only the source code. Use `references/qa-checklist.md` and report evidence for each route. Verify first impression and recognizability without the logo, generic AI patterns and reference copying, typography hierarchy, scale, whitespace, contrast, focus, content density, marketing/product continuity, desktop/tablet/375px/320px layouts, keyboard navigation, visible focus, screen-reader names, 200% zoom, reduced motion, loading/empty/error/success/disabled/retry states, core workflow success and failure paths, and preservation of backend/API/database behavior.

Do not claim complete or PASS when a route is blank, a state is unverified, or a claim is unsupported. Return a stable preview URL, screenshots, known limitations, and a route-by-route evidence matrix.

## Rapid hackathon mode

For a 4–8 hour sprint, time-box rather than remove the workflow. Spend approximately 15 minutes on diagnosis and inputs, 20 minutes on the visual concept decision, 60–90 minutes on the landing/entry surface and one real workflow, 90–180 minutes on propagation, and 30–45 minutes on evidence-based QA. If time runs out, ship the two-surface proof and clearly mark lower-priority routes unverified; do not pretend that unfinished routes passed.

Use `docs/HACKATHON_QUICKSTART.md` for the sprint sequence. The rapid path is optimized for fewer wrong turns, not for skipping product truth, concept comparison, screenshot review, accessibility, or functional honesty.

## Anti-AI-slope guardrails

Reject or revise output that relies on repeated rounded cards, excessive pills, default dark SaaS styling, neon gradients, generic dashboard tiles, tiny uppercase labels, monospace texture, decorative terminal logs, meaningless charts, stock imagery, AI/LLM language as personality, fake testimonials, unsupported metrics, or empty screens.

A project may use any of these intentionally, but only with a documented product reason. Decoration must express product truth or improve usability.

## Handoff format to another AI agent

Give the receiving agent this skill, `templates/agent-handoff.template.md`, a completed project brief using `templates/project-brief.template.md`, reference analysis using `references/reference-analysis.md` or equivalent, existing project constraints and routes, asset/icon/font preferences, and the required visual concept gate and QA checklist.

Tell the agent: **Do not skip the concept gate, do not redesign every route before the two-surface proof, and do not treat a font/color change as art direction.**

When passing a review report, identify its path, classify it as diagnostic, visual, functional, or acceptance evidence, state which findings are binding, define the allowed change scope, require preservation of backend/data behavior, and require screenshots plus verified and unverified checks in the response.
