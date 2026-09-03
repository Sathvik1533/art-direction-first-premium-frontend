# Cross-Agent Adapter Guide

Art Direction First is intentionally independent of a specific AI vendor, coding environment, frontend framework, or browser tool. The agent’s interface may change; the quality gates do not.

## Universal handoff

Give the agent these inputs:

1. `SKILL.md`.
2. `templates/agent-handoff.template.md`.
3. A completed `templates/project-brief.template.md`.
4. Reference URLs and reference analysis.
5. Existing repository path or URL.
6. Explicit backend/API/database boundaries.
7. Asset, icon, font, and motion preferences.

Then tell the agent to follow the phases in `SKILL.md` in order and to stop at the visual concept gate before full implementation.

## If the agent has browser access

Ask it to open every supplied reference and the current product. It should capture screenshots at the agreed viewport sizes, inspect desktop and mobile compositions, test interactions, and return URLs plus evidence. It must distinguish an initial blank/loading frame from a persistent rendering failure by waiting once and checking again.

## If the agent has no browser access

Provide screenshots, screen recordings, or static exports. Ask the agent to create local screenshot-ready prototypes and use the project’s available preview mechanism. It must mark live interaction checks as **unverified** rather than pretending they passed.

## If the agent has no image-generation tool

Use CSS, SVG, Canvas, or existing licensed assets to create the signature visual. Do not replace art direction with generic stock imagery. If a visual asset is essential and cannot be produced, record it as a blocked dependency and create a graceful fallback.

## If the agent has no repository write access

Ask it to produce a complete file-by-file implementation plan, a `DESIGN.md`, exact component specifications, and patches or code blocks. Do not accept a prose-only claim of completion.

## If the agent has no backend access

Keep the real backend contract untouched. Use representative fixtures only where the project owner authorizes them, and label them as fixtures. Do not invent persistence, audit, or API success.

## If the agent uses a different frontend stack

Translate the concepts, not the framework syntax. The required outcomes are the visual world, two-surface proof, responsive behavior, accessible states, and route evidence. React, Vue, Svelte, Angular, HTML/CSS, mobile frameworks, and other stacks may implement the same system.

## Tool-specific notes

### Antigravity

Attach the repository or give it the four core files. Ask it to inspect references with its browser, create the visual concept gate, and return screenshots before propagating.

### Claude Code

Place the repository in the working tree. Ask Claude to read `SKILL.md`, complete the project brief, inspect existing routes, save `DESIGN.md`, and work in staged commits: concept gate, two-surface proof, propagation, QA.

### Gemini or Google-based coding agents

Provide the repository and explicit screenshot/preview requirements. Ask the agent to compare its output against the reference principles and to report unsupported claims or missing tool access.

### Kiro, Cursor, Windsurf, and IDE agents

Add `SKILL.md` to the project context or rules directory. Keep the project brief and `DESIGN.md` in version control. Require the agent to update the design system before changing multiple routes.

### OpenAI coding agents or other agents

Use the universal handoff template. Provide exact commands for local preview, screenshot capture, tests, and build. Require the agent to return changed files and evidence rather than only a narrative summary.

## How to translate missing capabilities

| Required capability | Equivalent evidence |
|---|---|
| Browser inspection | Supplied screenshots or local preview captures |
| Browser interaction | Recorded test steps, test output, or manual verification instructions |
| Image generation | CSS/SVG/Canvas or licensed existing assets |
| Full-stack access | Explicit frontend-only limitation and fixture labels |
| Automated screenshots | Manual viewport captures or framework-specific screenshot tool |
| Built-in design preview | Local HTML/CSS prototype or static render |

## Failure handling

If a phase cannot be completed, stop and report the blocker, affected acceptance criterion, and the safest next action. Do not silently skip the visual gate, two-surface proof, or QA. An honest partial result is better than a false PASS.
