# Desired Outcome Verification Gate

A frontend is not successful merely because it builds, looks polished in one screenshot, or satisfies the implementing agent. The final reviewer must verify that it delivers the user’s intended experience.

## Required questions

Before declaring completion, ask the project owner or designated reviewer:

1. Does this feel like the product you intended to build, rather than a generic AI interpretation?
2. Does the first viewport communicate the product story in user language before technical terminology?
3. Does the visual world feel original and recognizable without the logo?
4. Does the chosen UI direction or morphism fit the product’s users, trust needs, and workflow?
5. Does the landing or entry surface feel connected to the real product workflow?
6. Are the typography, palette, spacing, materials, icons, imagery, and motion aligned with the intended quality bar?
7. Do the core interactions feel clear, useful, and calm rather than decorative or noisy?
8. Does the interface still feel right on mobile and at the actual target viewport?
9. Are loading, empty, error, success, and disabled states part of the same visual world?
10. Is anything visually or verbally misleading, unsupported, copied, or technically overemphasized?
11. What is the strongest part of the experience?
12. What still feels wrong, generic, confusing, or unlike the intended product?

## Evidence requirement

Do not ask only “Do you like it?” Show the reviewer the concept screenshots, final desktop and mobile screenshots, and the core workflow. Record the reviewer’s answers, requested changes, approved direction, and remaining concerns in the project’s review report.

## Agent self-check

The implementing agent must answer separately:

- What did the user explicitly ask for?
- Which parts are demonstrably satisfied?
- Which parts are interpreted rather than explicit?
- Which parts remain unverified?
- What would most likely make the user reject this result?

The agent must not mark a project PASS when the owner’s desired outcome has not been reviewed. If the owner cannot review immediately, mark the outcome as **awaiting owner validation**, not approved.

## Final status vocabulary

Use one of these statuses:

| Status | Meaning |
|---|---|
| `PASS — owner aligned` | Owner reviewed the proof surfaces and confirmed the intended experience is present |
| `PASS — reviewer aligned` | Designated reviewer confirmed it when the owner is unavailable |
| `CONDITIONAL — changes requested` | Core direction is viable but owner identified material changes |
| `UNVERIFIED — awaiting review` | Evidence exists but the intended outcome has not been confirmed |
| `FAIL — direction rejected` | The result is generic, disconnected, misleading, or materially unlike the intended product |
