# Integrating Art Direction First with Any AI Coding Agent

This tutorial shows how to use the Art Direction First system with Antigravity, Claude Code, Gemini, Kiro, Cursor, Windsurf, OpenAI coding agents, or another agentic AI. The tool names may change; the workflow and acceptance gates stay the same.

## What you are installing

You are not installing a visual theme. You are giving an AI agent a repeatable decision process for creating an original frontend:

```text
Project truth
    → emotional premise
    → visual world
    → reference principles
    → three concepts
    → screenshot review
    → project DESIGN.md
    → two-surface proof
    → full implementation
    → QA + owner validation
```

The repository provides the reusable process. Your project supplies the identity.

## Before you start

Prepare these inputs:

| Input | What to provide |
|---|---|
| Product truth | What the product does, who uses it, and the core workflow |
| Constraints | Existing repository, routes, APIs, data, backend boundaries, and must-not-break behavior |
| References | Three to seven websites, screenshots, or products |
| UI direction | Preferred visual language, morphism, or a request for recommendation |
| Assets | Logo, fonts, icons, images, illustrations, chart preferences, and motion tolerance |
| Quality bar | Competitors, target devices, accessibility expectations, and rejection criteria |

Do not wait for perfect wording. A plain-language project brief is better than a long vague prompt.

## Method A — Give the agent the repository

This is the preferred method when the agent can read a local folder or GitHub repository.

### Step 1: Add the repository to the agent’s context

Clone or attach:

```bash
git clone https://github.com/Sathvik1533/art-direction-first-premium-frontend.git
```

Open the repository in the agent’s workspace. Ask the agent to read `SKILL.md` first, then `templates/agent-handoff.template.md`.

### Step 2: Create the project inputs

Copy the templates into your project or agent workspace:

```bash
cp templates/project-brief.template.md PROJECT_BRIEF.md
cp templates/asset-and-icon-brief.template.md ASSET_AND_ICON_BRIEF.md
```

Fill in both files. Keep these files project-specific; do not edit the reusable skill to store one project’s brand decisions.

### Step 3: Send the kickoff prompt

```text
Use the Art Direction First repository as the governing frontend workflow for this project. Read SKILL.md, templates/agent-handoff.template.md, PROJECT_BRIEF.md, and ASSET_AND_ICON_BRIEF.md before editing code. Follow the workflow in order. Diagnose the product, analyze the references as principles, define the emotional premise and original visual world, produce three materially different visual concepts, and stop for screenshot review. Do not implement every route yet. After one concept is selected, create DESIGN.md, prove the direction on one entry surface and one real workflow, then propagate it and perform functional, responsive, accessibility, and owner-outcome verification. Return verified and unverified checks separately.
```

## Method B — Paste the files into a chat agent

If the agent cannot clone a repository, paste or attach:

1. `SKILL.md`.
2. `templates/agent-handoff.template.md`.
3. Your completed project brief.
4. Your asset/icon brief.
5. The reference links.
6. The existing route or repository summary.

Use the same kickoff prompt. If the agent has a context limit, give it `SKILL.md` first, then load the reference and QA documents when those phases begin. Do not omit the concept gate just because the full repository was not attached.

## Method C — Add it to an IDE agent’s rules

For Kiro, Cursor, Windsurf, Claude Code, or similar tools, place `SKILL.md` in the project’s rules or instruction context. Keep the project brief, asset brief, reference analysis, and `DESIGN.md` in the project repository.

Add this rule:

```text
Before changing multiple frontend routes, read DESIGN.md and verify that the proposed change belongs to the locked visual world. If DESIGN.md does not exist, stop and run the Art Direction First concept gate.
```

## The correct staged conversation

Do not send one enormous prompt saying “build the whole website.” Use staged messages.

### Message 1 — Diagnose

```text
Do not edit the frontend yet. Inspect the project and return a diagnosis covering product truth, users, core workflow, existing data states, technical boundaries, placeholders, risks, and what must remain functional. Identify what the product should feel like and what it must never feel like.
```

### Message 2 — References and direction

```text
Analyze the supplied references as principles. For each, state what to study, where it applies, and what not to copy. Propose one visual world and two alternatives. Include emotional premise, typography roles, palette semantics, materials, signature metaphor, UI direction, motion, and anti-patterns.
```

### Message 3 — Concept gate

```text
Create three materially different screenshot-ready concepts. Each must show the entry surface and one real workflow at desktop and mobile widths. Do not submit color variations of one layout. Use the visual concept scorecard and stop for review.
```

### Message 4 — Select and prove

```text
Use the selected concept to create DESIGN.md. Implement only the entry surface and one real workflow first. Use real product content and states. Capture desktop and mobile screenshots. Do not propagate to the remaining routes until these two surfaces feel like one product.
```

### Message 5 — Propagate and verify

```text
Apply the locked design system to the remaining routes by page responsibility. Run the QA checklist. Verify happy paths, failure paths, direct routes, responsive widths, accessibility, and persistence where claimed. Then run the desired-outcome verification with the owner or designated reviewer. Return a status for every check.
```

## Working with browser-capable agents

Ask the agent to inspect reference websites and the current product, capture screenshots at agreed widths, test important controls, and wait once when a page initially appears blank. The agent should distinguish loading from a real rendering failure.

Require screenshot filenames and URLs in the final report. Screenshots are evidence of visual decisions, not decoration.

## Working without browser access

Provide screenshots or recordings. Ask the agent to create local prototypes and clearly mark live interaction checks as unverified. Do not let it claim browser-tested behavior from static source inspection.

## Working without image generation

Use CSS, SVG, Canvas, or approved existing assets for the signature visual. Do not replace art direction with random stock imagery. Record blocked assets and provide a graceful fallback.

## Working without backend access

Keep API and database behavior untouched. Use fixtures only when authorized and label them as fixtures. Do not claim persistence, audit history, or server success that was not tested.

## Adding component and animation libraries

Consider a component or animation library only after `DESIGN.md` exists. For each candidate, document:

- Product reason.
- Target page and interaction.
- Brand adaptation.
- Accessibility behavior.
- Reduced-motion behavior.
- Performance cost.
- License status.
- Fallback.

Use the smallest number of components that strengthen the product story. Do not import an entire visual language.

## Passing an existing review report

Give the agent the report and say:

```text
Read this report before editing. Treat it as [diagnostic / visual / functional / acceptance] evidence. Separate binding findings from optional recommendations. Preserve existing product behavior and data contracts. Apply required changes first to the entry surface and one real workflow. Show desktop and mobile screenshots before propagating. Return verified, unverified, conditional, and rejected items separately.
```

## Owner outcome verification

The implementing agent must not approve itself. Show the owner or designated reviewer the concepts, selected direction, two-surface proof, screenshots, and important states. Ask whether the result feels like the intended product, whether the story arrives before technical language, whether the palette and UI direction are right, and what still feels generic or wrong.

Use `docs/DESIRED_OUTCOME_VERIFICATION.md`. If the owner has not reviewed the result, the status is `UNVERIFIED — awaiting review`.

## Troubleshooting

| Problem | Correct response |
|---|---|
| The agent starts coding immediately | Stop it and send the Diagnose message |
| Three concepts look identical | Require a different composition and spatial architecture, not another palette |
| Landing page is polished but app is generic | Return to the two-surface proof and revise the system |
| Agent overuses library components | Require a product reason and remove anything decorative |
| Copy is full of technical terms | Rewrite the first narrative around the user’s problem and outcome |
| Palette looks attractive but feels wrong | Test semantic roles, contrast, emotional fit, and real content density |
| Agent says “complete” too early | Ask for route evidence, screenshots, and verified/unverified status |
| Tool is unavailable | Use the cross-agent adapter and document the limitation |

## Final delivery checklist

The agent should return:

- Selected visual world and rationale.
- Project-specific `DESIGN.md`.
- Concept comparison screenshots.
- Entry and core-workflow screenshots at desktop and mobile.
- Routes verified.
- Functional workflows verified.
- Responsive and accessibility checks.
- Owner desired-outcome status.
- Known limitations.
- Unverified checks.
- Preview URL.
- Changed files or commit reference.

That final response is the handoff artifact for the team—not a claim that the agent “made it premium.”
