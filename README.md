# Art Direction First

## Build a frontend that feels like a real product—not an AI template.

Art Direction First is a free, open-source workflow for building polished websites, dashboards, and product interfaces with any agentic AI.

Use it with **Antigravity, Claude Code, Gemini, Kiro, Cursor, Windsurf, OpenAI coding agents, or any other AI builder**.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## The simple idea

Do not ask an AI agent to build the whole frontend immediately.

First help it understand the product. Then make it choose a visual direction. Then test that direction on a small part of the product. Only after the direction feels right should it build the rest.

```text
Understand the product
        ↓
Choose the visual world
        ↓
Compare three concepts
        ↓
Prove one landing page + one real workflow
        ↓
Review screenshots
        ↓
Build the remaining pages
        ↓
Test everything honestly
```

## Start here

### Step 1 — Give the agent the skill

Give the agent [`SKILL.md`](SKILL.md). This is the rulebook.

Also give it [`templates/agent-handoff.template.md`](templates/agent-handoff.template.md), which explains exactly how to use the process in any AI environment.

### Step 2 — Fill in the project brief

Copy [`templates/project-brief.template.md`](templates/project-brief.template.md) and answer the questions:

- What are you building?
- Who is it for?
- What problem does it solve?
- What is the most important user workflow?
- What should the product feel like?
- What should it never feel like?
- What must stay functional?
- What references, fonts, icons, assets, and UI direction do you prefer?

You do not need to know design vocabulary. Plain language is enough.

### Step 3 — Add references carefully

Give the agent three to seven websites, screenshots, or products that inspire you.

For every reference, write:

| Tell the agent | Example |
|---|---|
| Study this | Editorial spacing, product visualization, calm financial trust |
| Do not copy this | Exact layout, colors, wording, illustrations, or branded metaphor |

Use [`references/reference-analysis.md`](references/reference-analysis.md) to keep references from becoming a copy-paste collage.

### Step 4 — Choose the UI direction

Tell the agent what kind of interface you want, or ask it to recommend one:

- Editorial.
- Tactile.
- Cinematic.
- Utilitarian.
- Spatial.
- Neo-brutalist.
- Soft.
- Dark.
- Light.
- Another direction that fits the product.

The agent must explain why the direction fits the users and the product. Glassmorphism, neumorphism, and heavy animation are not automatically premium.

### Step 5 — Compare three concepts

Before building every page, require three genuinely different visual concepts.

Each concept must show:

- The landing or entry surface.
- One real product workflow.
- Desktop and mobile versions.
- Typography.
- Palette.
- Materials.
- Signature visual metaphor.
- Interaction direction.

Use [`docs/VISUAL_CONCEPT_SCORECARD.md`](docs/VISUAL_CONCEPT_SCORECARD.md) to compare them. Reject anything that is only a font change, color change, card change, or copy of a reference website.

### Step 6 — Prove the direction

Build two things first:

1. The landing or entry surface.
2. One complete real workflow.

This is the most important time-saving step. If these two surfaces feel like different products, fix the direction now—not after building twelve pages.

### Step 7 — Lock the design system

After choosing a concept, create the project’s `DESIGN.md` using [`templates/design-system.template.md`](templates/design-system.template.md).

This records the project-specific:

- Visual world.
- Emotional premise.
- Voice.
- Typography.
- Palette.
- Spacing.
- Materials.
- Icons.
- Motion.
- Signature metaphor.
- Page expressions.
- Anti-patterns.

### Step 8 — Build the rest

Apply the locked system to the remaining pages. Keep one visual identity, but let each page behave according to its job:

| Page | What it should prioritize |
|---|---|
| Landing | Story and memorable first impression |
| Dashboard | Summary and orientation |
| Queue | Fast scanning and prioritization |
| Case/workspace | Evidence and decisions |
| Forms/ingestion | Clear steps and useful feedback |
| Audit/history | Trust and chronology |
| Settings | Precision and control |
| Documentation | Reading and finding information |

Do not turn every route into the same card grid.

### Step 9 — Test the result

Use [`references/qa-checklist.md`](references/qa-checklist.md). Check:

- Desktop.
- Tablet.
- 375px mobile.
- 320px mobile.
- Keyboard navigation.
- Focus states.
- Contrast.
- Reduced motion.
- Loading states.
- Empty states.
- Error states.
- Success states.
- Real workflow success and failure paths.
- Direct route loading.
- Persistence where claimed.

Use [`docs/DESIRED_OUTCOME_VERIFICATION.md`](docs/DESIRED_OUTCOME_VERIFICATION.md) to ask the owner or reviewer whether the result actually feels like the intended product.

If something was not tested, write **unverified**. Never claim PASS because the code compiles.

## Hackathon mode

For a 4–8 hour hackathon, use [`docs/HACKATHON_QUICKSTART.md`](docs/HACKATHON_QUICKSTART.md).

The short version is:

| Time | Focus |
|---:|---|
| 15 min | Product truth and constraints |
| 20 min | Visual direction and concept decision |
| 60–90 min | Landing page and one real workflow |
| 90–180 min | Remaining high-value routes |
| 30–45 min | Screenshot, responsive, accessibility, and function checks |

Do not remove the concept gate to save time. Time-box it instead.

## What this prevents

This workflow exists because AI agents often produce interfaces that are technically complete but visually generic. It protects against:

- Default SaaS dashboards.
- Repeated rounded cards.
- Excessive pills.
- Neon gradients.
- Random glass panels.
- Unnecessary monospace text.
- Decorative terminal language.
- Unrelated 3D objects.
- Generic stock imagery.
- Fake testimonials.
- Unsupported metrics.
- Technical copy before the user story.
- Beautiful landing pages disconnected from the real product.

## UI libraries and animation

You may inspect libraries such as Animaster-style animated collections, Skiper UI, and Vengeance UI. Use [`references/ui-library-integration.md`](references/ui-library-integration.md).

Use a library only when a component has a product reason, fits the visual system, is accessible, performs well, and has a valid license. Libraries are ingredients. They are not the brand.

## How to hand a report to an AI agent

Give the agent:

1. The report file.
2. The project brief.
3. `SKILL.md`.
4. The universal handoff template.
5. A clear instruction describing whether the report is diagnostic, visual, functional, or acceptance evidence.

Use this wording:

> Read this report as a binding input for the next frontend pass. Summarize the findings first. Separate required changes from optional suggestions. Preserve the existing product behavior and data contracts. Do not modify every route until the revised landing surface and one real workflow are shown in desktop and mobile screenshots. Return verified and unverified checks separately.

## Files

| File | Use it for |
|---|---|
| [`SKILL.md`](SKILL.md) | Core workflow and quality gates |
| [`templates/agent-handoff.template.md`](templates/agent-handoff.template.md) | Handoff to any AI agent |
| [`templates/project-brief.template.md`](templates/project-brief.template.md) | Project truth and constraints |
| [`templates/asset-and-icon-brief.template.md`](templates/asset-and-icon-brief.template.md) | Assets, fonts, icons, images, and motion |
| [`templates/design-system.template.md`](templates/design-system.template.md) | Project-specific `DESIGN.md` |
| [`references/reference-analysis.md`](references/reference-analysis.md) | Reference research without copying |
| [`references/ui-library-integration.md`](references/ui-library-integration.md) | Safe library and animation use |
| [`references/qa-checklist.md`](references/qa-checklist.md) | QA evidence |
| [`docs/CROSS_AGENT_ADAPTER.md`](docs/CROSS_AGENT_ADAPTER.md) | What to do when an agent lacks a tool |
| [`docs/VISUAL_CONCEPT_SCORECARD.md`](docs/VISUAL_CONCEPT_SCORECARD.md) | Choosing between concepts |
| [`docs/HACKATHON_QUICKSTART.md`](docs/HACKATHON_QUICKSTART.md) | Rapid sprint workflow |
| [`docs/HACKATHON_PRESENTATION_SCRIPT.md`](docs/HACKATHON_PRESENTATION_SCRIPT.md) | Explaining the system to others |
| [`docs/DESIRED_OUTCOME_VERIFICATION.md`](docs/DESIRED_OUTCOME_VERIFICATION.md) | Confirming the owner got the intended UI/UX |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contributing to the open-source project |
| [`LICENSE`](LICENSE) | MIT License |

## Why this project exists

This started as a practical response to a frustrating pattern: a working product could lose its momentum when an AI-generated frontend looked generic, disconnected, or unlike the product the owner imagined.

Art Direction First turns that personal solution into a reusable open-source workflow. It helps people make the difficult visual decisions earlier, test them sooner, reduce rework, and hand the same process to different AI agents without losing the product’s identity.

## License

This project is released under the [MIT License](LICENSE). The license covers this repository’s original workflow, documentation, and templates. External websites, assets, fonts, icons, and UI libraries mentioned here remain subject to their own terms.
