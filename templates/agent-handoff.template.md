# Universal Agent Handoff — Premium Frontend Art Direction

Use this handoff with any agentic AI frontend builder, including Antigravity, Claude Code, Gemini, Kiro, Cursor, Windsurf, OpenAI coding agents, or another tool.

## Instructions to the receiving agent

Use the attached `SKILL.md` as the governing art-direction workflow. Use the project brief as the source of project truth. Use the reference analysis as the boundary for what to study and what not to copy. Use the design-system template after a visual concept is selected. Use the QA checklist for final evidence. Use `docs/DESIRED_OUTCOME_VERIFICATION.md` to verify the owner actually received the intended frontend/UI/UX. Use `docs/MANUS_CONTINUITY_HANDOFF.md` when transferring the work to another Manus account.

The workflow is tool-agnostic. If your environment does not support a particular tool, perform the equivalent action available in your environment and document the limitation. Do not skip a phase merely because the tool name differs.

## Required order

1. Read `SKILL.md` completely before implementation.
2. Inspect the existing project, routes, data states, and technical boundaries.
3. Complete the project brief and clarify missing high-impact inputs.
4. Analyze three to seven references as principles, not templates.
5. Define the product’s emotional premise, visual world, voice, signature metaphor, material language, and anti-patterns.
6. Produce three materially different visual concepts with desktop and mobile proof.
7. Reject generic concepts and record the selected direction.
8. Create the project-specific `DESIGN.md`.
9. Build one landing/entry surface and one real product workflow.
10. Review screenshots and revise before full propagation.
11. Apply the approved system to the remaining routes by page responsibility.
12. Run visual, functional, responsive, accessibility, and persistence QA.
13. Verify the owner’s desired outcome and record the status as aligned, conditional, unverified, or rejected.
14. Return the preview URL, screenshots, evidence matrix, known limitations, desired-outcome status, and changed files.

## Project inputs

- **Project brief:** [attach or paste path]
- **Reference analysis:** [attach or paste path]
- **Existing repository:** [path or URL]
- **Routes/surfaces in scope:** [list]
- **Backend/API/database boundaries:** [describe]
- **Asset, icon, and font preferences:** [describe]
- **UI direction/morphism preference:** [describe or ask the agent to recommend]
- **Quality bar/competitor URLs:** [list]

## Cross-agent acceptance instruction

Do not begin full implementation from a feature list alone. Do not call a font/color swap “art direction.” Do not import a UI-library template wholesale. Do not copy reference websites. Do not claim completion when the concept gate, two-surface proof, route states, mobile checks, accessibility checks, persistence checks, or functional failure paths are unverified.

If you cannot perform a required check, report it as **unverified** rather than assuming it passed.

## Final response format

Return:

1. Selected visual world and one-sentence rationale.
2. Project-specific `DESIGN.md` path.
3. Concept screenshots and final screenshots.
4. Routes verified.
5. Functional workflows verified.
6. Responsive/accessibility checks performed.
7. Known limitations and unverified checks.
8. Preview URL.
9. Changed files or commit reference.
