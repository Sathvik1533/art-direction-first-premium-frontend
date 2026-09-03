# Art Direction First

### A practical design workflow for building frontends that feel like products—not templates.

[![MIT License](https://img.shields.io/badge/license-MIT-0f766e.svg)](LICENSE)
[![Agent agnostic](https://img.shields.io/badge/works%20with-any%20agentic%20AI-1f2937.svg)](docs/CROSS_AGENT_ADAPTER.md)
[![Skill validated](https://img.shields.io/badge/Skill%20Creator-validated-7c3aed.svg)](SKILL.md)
[![Live preview](https://img.shields.io/badge/live%20preview-open-0f766e.svg)](https://ist-established-takes-elliott.trycloudflare.com/concepts)

<p align="center">
  <a href="https://ist-established-takes-elliott.trycloudflare.com/concepts"><img src="docs/assets/concept-gate.webp" alt="LedgerLens visual concept review gate" width="31%" /></a>
  <a href="https://ist-established-takes-elliott.trycloudflare.com/concept/a"><img src="docs/assets/cinematic-ledger-landing.webp" alt="Cinematic Ledger landing concept" width="31%" /></a>
  <a href="https://ist-established-takes-elliott.trycloudflare.com/concept/a/case"><img src="docs/assets/cinematic-ledger-case.webp" alt="Cinematic Ledger case workspace concept" width="31%" /></a>
</p>

<p align="center"><sub>Example concept gate · entry surface · real workflow proof — <a href="https://ist-established-takes-elliott.trycloudflare.com/concepts">open the live preview</a></sub></p>

Art Direction First is an open-source workflow for creating original, premium websites, dashboards, and product interfaces with **Antigravity, Claude Code, Gemini, Kiro, Cursor, Windsurf, OpenAI coding agents, or any other agentic AI**.

It keeps the process reusable while allowing every project to choose its own product story, references, UI direction, visual world, typography, assets, icons, and motion language.

New to the workflow? Read the [integration tutorial](docs/INTEGRATION_TUTORIAL.md) for copy-ready prompts and setup instructions for different AI coding agents.

---

## The workflow at a glance

This is intentionally vertical so it remains readable on GitHub, mobile screens, and zoomed views.

```mermaid
%%{init: {"theme": "base", "themeVariables": {"fontFamily": "ui-sans-serif, -apple-system, BlinkMacSystemFont, Segoe UI, sans-serif", "fontSize": "17px", "lineColor": "#64748b", "primaryTextColor": "#111827"}}}%%
flowchart TD
    A[01 · UNDERSTAND<br/>Product truth + user + workflow] --> B[02 · DEFINE<br/>Emotional premise + point of view]
    B --> C[03 · DIRECT<br/>Original visual world + UI direction]
    C --> D[04 · EXPLORE<br/>Three distinct visual concepts]
    D --> E{05 · REVIEW<br/>Does it feel original?}
    E -->|No · reject generic| D
    E -->|Yes · select one| F[06 · LOCK<br/>Project-specific DESIGN.md]
    F --> G[07 · PROVE<br/>Landing or entry surface]
    G --> H[08 · PROVE<br/>One real product workflow]
    H --> I{09 · OWNER CHECK<br/>Did we achieve the intended UI/UX?}
    I -->|Changes requested| F
    I -->|Aligned| J[10 · PROPAGATE<br/>Build the remaining routes]
    J --> K[11 · VERIFY<br/>Functional + responsive + accessibility QA]
    K --> L[12 · HAND OFF<br/>Verified, honest, reusable result]

    classDef understand fill:#e0f2fe,stroke:#0284c7,color:#082f49,stroke-width:2px
    classDef define fill:#fef3c7,stroke:#d97706,color:#451a03,stroke-width:2px
    classDef direct fill:#ede9fe,stroke:#7c3aed,color:#2e1065,stroke-width:2px
    classDef explore fill:#fce7f3,stroke:#db2777,color:#500724,stroke-width:2px
    classDef review fill:#fff7ed,stroke:#ea580c,color:#431407,stroke-width:2px
    classDef prove fill:#dcfce7,stroke:#16a34a,color:#052e16,stroke-width:2px
    classDef verify fill:#ccfbf1,stroke:#0f766e,color:#042f2e,stroke-width:2px
    classDef handoff fill:#f3f4f6,stroke:#374151,color:#111827,stroke-width:2px

    class A understand
    class B define
    class C direct
    class D explore
    class E review
    class F direct
    class G,H prove
    class I review
    class J direct
    class K verify
    class L handoff
```

### What the colors mean

| Color | Stage | Meaning |
|---|---|---|
| Blue | Understand | Start with product truth |
| Amber | Define | Decide what the product should feel like |
| Violet | Direct | Create the visual world and system |
| Pink | Explore | Generate genuinely different concepts |
| Orange | Review | Reject generic or weak directions |
| Green | Prove | Test the entry surface and real workflow |
| Teal | Verify | Check quality, behavior, and accessibility |
| Gray | Hand off | Return evidence and honest status |

> **The fastest way to a better frontend is to catch the wrong visual direction before building the entire product.**

## Start in three steps

### 1. Give the agent the workflow

Give the agent [`SKILL.md`](SKILL.md) and [`templates/agent-handoff.template.md`](templates/agent-handoff.template.md).

The workflow is tool-agnostic. If the agent does not have browser access, image generation, repository access, or backend access, it must use an equivalent method and report the limitation instead of silently skipping a stage. See [`docs/CROSS_AGENT_ADAPTER.md`](docs/CROSS_AGENT_ADAPTER.md).

### 2. Add the project’s inputs

Copy [`templates/project-brief.template.md`](templates/project-brief.template.md) and [`templates/asset-and-icon-brief.template.md`](templates/asset-and-icon-brief.template.md). Fill them in with plain language:

- What are you building?
- Who is it for?
- What problem does it solve?
- What is the core user workflow?
- What should it feel like?
- What should it never feel like?
- Which references should inspire it?
- Which fonts, icons, assets, and UI direction do you prefer?
- What existing behavior must remain functional?

You do not need to know design vocabulary. The agent can recommend a UI direction when you are unsure.

### 3. Run the gates in order

| Gate | What must be true before moving on |
|---|---|
| **Understand** | Product truth, users, workflow, constraints, and quality bar are clear |
| **Define** | Emotional premise, visual world, voice, metaphor, materials, and anti-patterns exist |
| **Explore** | Three materially different concepts are shown at desktop and mobile sizes |
| **Choose** | One concept is selected using the [scorecard](docs/VISUAL_CONCEPT_SCORECARD.md) |
| **Prove** | The landing/entry surface and one real workflow feel like the same product |
| **Propagate** | The project-specific [`DESIGN.md`](templates/design-system.template.md) is locked |
| **Verify** | Functional, responsive, accessibility, screenshot, and owner-outcome checks are evidenced |

Do not build every route before the **Prove** gate.

---

## What this prevents

AI agents are excellent at producing familiar UI quickly. Familiar UI is not the same as product identity.

This workflow is designed to prevent:

- Generic SaaS dashboards.
- Repeated rounded cards and pills.
- Random gradients and glass panels.
- Decorative terminal or AI language.
- Unrelated 3D objects and stock imagery.
- A landing page disconnected from the real product.
- A font or color change being mistaken for art direction.
- Technical terminology arriving before the human product story.
- Unverified claims about performance, persistence, or completion.

## The quality bar

A successful project has:

| Requirement | Evidence |
|---|---|
| Product diagnosis | A short explanation of the user, problem, workflow, and constraints |
| Product truth | Real behavior and truthful content are distinguished from fixtures or placeholders |
| Reference analysis | Each reference has a principle to study and a boundary not to copy |
| Emotional premise | The intended feeling is explicit |
| Original visual world | A named, ownable identity exists before full implementation |
| UI direction | The chosen interface language is justified by the product |
| Three concepts | Distinct compositions, not three color variations |
| Two-surface proof | Entry surface plus one complete real workflow |
| Screenshot review | Desktop and mobile screenshots are compared before propagation |
| Full propagation | Remaining routes share one system but express their different jobs |
| Functional QA | Happy paths, failure paths, direct routes, and persistence are tested |
| Responsive QA | Desktop, tablet, 375px, and 320px behavior is checked |
| Accessibility QA | Focus, labels, contrast, zoom, touch, and reduced motion are checked |
| Honest status | Verified, conditional, unverified, and rejected items are separated |
| Owner alignment | The owner or designated reviewer confirms the intended UI/UX was actually achieved |

Use [`references/qa-checklist.md`](references/qa-checklist.md) and [`docs/DESIRED_OUTCOME_VERIFICATION.md`](docs/DESIRED_OUTCOME_VERIFICATION.md) for the final review.

## How to hand it to any AI agent

Give the agent this repository and say:

> Use this repository as the governing art-direction workflow for the project. Read `SKILL.md` and `templates/agent-handoff.template.md` first. Follow the gates in order. Use the project brief as the source of truth. Analyze references as principles, not templates. Create three materially different visual concepts and show desktop/mobile proof before full implementation. Reject generic output. Lock the selected direction in `DESIGN.md`. Prove it on one landing or entry surface and one real workflow. Then propagate it and return screenshots, verified checks, unverified checks, limitations, and the preview URL. Do not call a font/color swap art direction, do not copy references, and do not claim completion without owner or reviewer alignment.

For a written review report, also state whether it is diagnostic, visual, functional, or acceptance evidence; which findings are binding; what may change; what must remain functional; and what screenshots are required. The detailed method is in the README’s [report handoff section](#passing-a-review-report).

## Hackathon mode

Use [`docs/HACKATHON_QUICKSTART.md`](docs/HACKATHON_QUICKSTART.md) when the sprint is time-boxed.

```text
15 min   Product truth + constraints
20 min   Visual direction + concept decision
60–90    Landing/entry surface + real workflow
90–180   High-value route propagation
30–45    Screenshots + functional/responsive/accessibility QA
```

Time-box the gates; do not remove them. If time runs out, ship the two-surface proof and label the rest unverified.

## Passing a review report

Give the AI agent:

1. The report file.
2. The project brief.
3. [`SKILL.md`](SKILL.md).
4. [`templates/agent-handoff.template.md`](templates/agent-handoff.template.md).
5. The expected scope of change.

Use this instruction:

> Read this report before editing. Classify its findings as required, recommended, or informational. Summarize the binding findings first. Preserve existing product behavior and data contracts. Apply the required changes to the entry surface and one real workflow first. Show desktop and mobile screenshots before propagating. Return verified and unverified checks separately.

## Repository map

| Path | Purpose |
|---|---|
| [`SKILL.md`](SKILL.md) | Core workflow and mandatory quality gates |
| [`templates/agent-handoff.template.md`](templates/agent-handoff.template.md) | Universal handoff for any agentic AI |
| [`templates/project-brief.template.md`](templates/project-brief.template.md) | Project truth, users, workflow, and constraints |
| [`templates/asset-and-icon-brief.template.md`](templates/asset-and-icon-brief.template.md) | Assets, fonts, icons, imagery, and motion |
| [`templates/design-system.template.md`](templates/design-system.template.md) | Project-specific `DESIGN.md` scaffold |
| [`references/reference-analysis.md`](references/reference-analysis.md) | Reference research without copying |
| [`references/ui-library-integration.md`](references/ui-library-integration.md) | Safe use of component and animation libraries |
| [`references/qa-checklist.md`](references/qa-checklist.md) | Visual, functional, responsive, and accessibility QA |
| [`docs/CROSS_AGENT_ADAPTER.md`](docs/CROSS_AGENT_ADAPTER.md) | Equivalent methods when an agent lacks a tool |
| [`docs/VISUAL_CONCEPT_SCORECARD.md`](docs/VISUAL_CONCEPT_SCORECARD.md) | Evidence-based concept comparison |
| [`docs/DESIRED_OUTCOME_VERIFICATION.md`](docs/DESIRED_OUTCOME_VERIFICATION.md) | Owner/reviewer confirmation gate |
| [`docs/HACKATHON_QUICKSTART.md`](docs/HACKATHON_QUICKSTART.md) | Rapid 4–8 hour execution plan |
| [`docs/HACKATHON_PRESENTATION_SCRIPT.md`](docs/HACKATHON_PRESENTATION_SCRIPT.md) | Script for teammates, mentors, or judges |
| [`docs/INTEGRATION_TUTORIAL.md`](docs/INTEGRATION_TUTORIAL.md) | Detailed setup guide for any AI coding agent |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | Contribution guidelines |
| [`NOTICE.md`](NOTICE.md) | Scope and third-party reference notice |
| [`LICENSE`](LICENSE) | MIT License |

## Why this exists

This project began with a recurring problem: a working product could lose momentum when an AI-generated frontend looked generic, disconnected, or unlike what the owner imagined.

Art Direction First turns that personal solution into a reusable open-source method. It moves difficult decisions earlier, tests them sooner, reduces redesign stress, and gives people a dependable way to work with different AI agents without losing the product’s identity.

## Contributing and license

Read [`CONTRIBUTING.md`](CONTRIBUTING.md) before opening a pull request. The project is released under the [`MIT License`](LICENSE). This license covers the original workflow, documentation, and templates in this repository. External websites, assets, fonts, icons, and UI libraries mentioned here retain their own terms.
