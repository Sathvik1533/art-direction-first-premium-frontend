# LedgerLens Phase 1 — Exact Antigravity Prompt

Copy everything inside the block below into Antigravity.

```text
Act as the lead product designer, senior frontend engineer, and QA owner for LedgerLens. This is Phase 1 of an art-direction implementation, not a generic restyling task.

Read these files before editing:

- SKILL.md
- examples/ledgerlens/DESIGN.md
- examples/ledgerlens/WIREFRAMES.md
- templates/agent-handoff.template.md
- references/qa-checklist.md
- docs/DESIRED_OUTCOME_VERIFICATION.md
- docs/VISUAL_CONCEPT_SCORECARD.md

Read the current repository and inspect the existing routes, data states, backend/API boundaries, and real functionality. Do not modify backend code, API endpoints, database schemas, or server logic.

## Product truth

LedgerLens helps finance operators find why money captured by a business does not match the money reported by a payment gateway or credited by a bank. It compares four financial records, isolates the exact difference, surfaces the relevant operating rule, and records the human decision.

The product story is:

A payment was captured. Less money arrived. LedgerLens follows the trail, shows exactly where the amount changed, explains the rule, and records what the reviewer decided.

Do not lead the interface with throughput, database, retrieval, or implementation terminology. Technical proof remains available, but the user story comes first.

## Reference principles

Use these references only to understand quality principles. Do not copy their layout, wording, brand, colors, assets, metaphors, or typography:

- Apptains: https://apptains.com/
  Study its emotional premise, memorable voice, narrative pacing, editorial spacing, and consistency between marketing and product promise.

- Modern website gallery: https://dribbble.com/tags/modern-website
  Study composition, scale, visual confidence, whitespace, and product presentation across high-quality work. Do not copy individual shots.

- Awwwards websites: https://www.awwwards.com/websites/
  Study art direction, interaction restraint, typography, motion, and the relationship between a visual idea and a product story. Do not copy individual sites.

- Ledger website reference: https://dribbble.com/shots/25075102-Ledger-Website-Design
  Study editorial composition, product-centered storytelling, and visual hierarchy. Do not copy the design.

## Selected LedgerLens direction

Use the “Editorial Evidence System” direction and the working visual world “The Reconciliation Room.”

The signature metaphor is the “Reconciliation Line”: four source records travel as distinct, restrained colored lines. The line diverges, terminates, or doubles where the discrepancy occurs. A physical oxide-red redline marks the exact break. The line then resolves into a human decision and an audit receipt.

Use:

- Deep ink for investigative/narrative space.
- Warm mineral paper surfaces for evidence and reading.
- Muted source colors with semantic roles.
- Oxide red only for the exact discrepancy.
- Green only for verified/reconciled states.
- Amber only for attention/pending review.
- Blue only when it represents a defined source or system meaning.

Do not use random gradients, heavy glassmorphism, unrelated 3D, terminal decoration, excessive pills, or tiny uppercase labels as a substitute for art direction.

## Phase 1 scope

Implement and prove exactly two surfaces first:

1. Landing page.
2. Case workspace.

Do not propagate to every route until these two surfaces pass screenshot review.

## Landing requirements

The first viewport must narrate:

1. The payment was captured.
2. The numbers did not agree.
3. LedgerLens follows the trail.
4. The operator can review the discrepancy.

Keep the Reconciliation Line as the primary visual object. Keep the hero copy in human financial language. Move RPS, parity, PostgreSQL numeric, Python Decimal, retrieval metadata, and contract invariant terms below the narrative or into technical disclosure.

Use the wireframe in `examples/ledgerlens/WIREFRAMES.md` as the structural starting point, not as a final visual design.

## Case workspace requirements

The reviewer must understand quickly:

- Expected amount.
- Actual amount.
- Difference.
- Source of the difference.
- Relevant policy.
- Recommended action.
- Available decision.
- What will be recorded.

Use evidence slips, the Reconciliation Line, a plain-language decision brief, a policy note, and a clear decision area. Technical IDs and retrieval details must remain available but secondary.

## Typography and spacing

Use a display role for narrative moments, a highly readable body role, and a restrained utility role only for IDs, timestamps, and technical values. Do not make the entire product look like a terminal. Do not use tiny type to create sophistication.

Use generous editorial spacing on the landing page. Use denser but highly scannable composition in the case workspace. Preserve readability at 375px and 320px.

## Loading and state behavior

Replace blank white loading frames with intentional LedgerLens loading states. Preserve or improve real behavior. Add or verify loading, empty, error, retry, success, and disabled states where relevant. Do not fake persistence or server behavior.

## Required process

1. Diagnose the current implementation and return the diagnosis before editing.
2. State the visual decisions you will implement and how they derive from `DESIGN.md`.
3. Implement the landing and case workspace only.
4. Capture desktop and mobile screenshots for both.
5. Compare the two surfaces for shared visual DNA.
6. Fix any marketing/product disconnect.
7. Run functional, responsive, accessibility, and state checks.
8. Stop and return evidence. Do not build the remaining routes in this Phase 1 task.

## Required acceptance table

Return a table with:

- Surface.
- Desktop screenshot.
- 375px screenshot.
- 320px result.
- Story clarity.
- Typography result.
- Palette semantics.
- Reconciliation Line continuity.
- Loading/error/empty/success state.
- Keyboard/focus/contrast result.
- Verified or unverified status.

## Owner-outcome gate

Before calling Phase 1 complete, show the owner or designated reviewer the landing page and case workspace screenshots and ask:

1. Does this feel like LedgerLens rather than a generic AI finance dashboard?
2. Does the financial story arrive before technical language?
3. Does the palette feel intentional and trustworthy?
4. Do the landing page and case workspace feel like one product?
5. What still feels generic, confusing, or unlike the intended product?

Use the status `PASS — owner aligned`, `CONDITIONAL — changes requested`, `UNVERIFIED — awaiting review`, or `FAIL — direction rejected`. Do not self-approve.

## Completion rule

Do not claim “fully complete” after only a successful build or HTTP 200 response. Return the screenshots, route evidence, functional checks, accessibility checks, known limitations, and owner-outcome status. Do not change backend code.
```
