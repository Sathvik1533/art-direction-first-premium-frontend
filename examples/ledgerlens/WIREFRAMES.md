# LedgerLens Phase 1 Wireframes

These are structural wireframes, not final visual mockups. They define hierarchy, content order, and relationships before styling.

## Landing page — desktop

```text
┌──────────────────────────────────────────────────────────────────────────────┐
│ LEDGERLENS                         How it works  Evidence  Docs   OPEN LEDGER │
├──────────────────────────────────────────────────────────────────────────────┤
│                                                                              │
│  THE MOMENT OF DOUBT                                                        │
│                                                                              │
│  The payment arrived.                                                       │
│  The numbers did not.                                                       │
│                                                                              │
│  LedgerLens follows the amount across the records, shows where it changed, │
│  and gives your team a decision they can stand behind.                     │
│                                                                              │
│  [Review a live discrepancy]     [See how the trace works]                   │
│                                                                              │
│                       ┌──────────────────────────────────────────────┐      │
│                       │  RECONCILIATION LINE                          │      │
│                       │  capture ────────┐                            │      │
│                       │  settlement ─────┼─── redline: −₹150           │      │
│                       │  refund ─────────┘        WHERE IT CHANGED     │      │
│                       │  bank credit ────────────────┐                 │      │
│                       │                                └─ REVIEW        │      │
│                       └──────────────────────────────────────────────┘      │
│                                                                              │
├──────────────────────────────────────────────────────────────────────────────┤
│  ONE TRACE. FOUR SOURCES. ONE EXPLAINABLE DECISION.                          │
│                                                                              │
│  Captured payment     Gateway settlement     Customer refund     Bank credit │
│  ₹10,000.00            ₹9,614.00              ₹0.00                ₹9,614.00  │
│                                                                              │
├──────────────────────────────────────────────────────────────────────────────┤
│  WHAT LEDGERLENS FINDS                                                       │
│                                                                              │
│  Expected             Reported              Difference                       │
│  ₹9,764.00            ₹9,614.00              −₹150.00                         │
│                                                                              │
│  The provider withheld more than the agreed fee. The evidence is assembled  │
│  in one case so a reviewer can resolve it without reconstructing the trail.  │
│                                                                              │
│  [Open the case dossier]                                                     │
│                                                                              │
├──────────────────────────────────────────────────────────────────────────────┤
│  FROM DISCOVERY TO DECISION                                                  │
│  1. Find the break   2. Read the evidence   3. Check the rule   4. Sign off   │
├──────────────────────────────────────────────────────────────────────────────┤
│  Technical proof, policy sources, and methodology                             │
│  (progressive disclosure; secondary to the product story)                    │
└──────────────────────────────────────────────────────────────────────────────┘
```

### Landing page — mobile

```text
┌──────────────────────────────┐
│ LEDGERLENS              MENU │
├──────────────────────────────┤
│ THE MOMENT OF DOUBT          │
│                              │
│ The payment arrived.         │
│ The numbers did not.         │
│                              │
│ Follow the amount across the │
│ records. Find the break.     │
│ Record the decision.         │
│                              │
│ [Review discrepancy]         │
│ [How it works]               │
│                              │
│ ┌──────────────────────────┐ │
│ │ capture ────────┐        │ │
│ │ settlement ─────┼─ redline│ │
│ │ refund ─────────┘  −₹150 │ │
│ │ bank credit ─────────────│ │
│ └──────────────────────────┘ │
│                              │
│ FOUR SOURCES                 │
│ 01 Captured payment ₹10,000 │
│ 02 Settlement       ₹9,614  │
│ 03 Refund           ₹0      │
│ 04 Bank credit      ₹9,614  │
│                              │
│ WHERE IT CHANGED             │
│ Expected            ₹9,764  │
│ Reported            ₹9,614  │
│ Difference          −₹150   │
│                              │
│ [Open case dossier]          │
└──────────────────────────────┘
```

## Case workspace — desktop

```text
┌──────────────────────────────────────────────────────────────────────────────┐
│ LEDGERLENS  Overview  Queue  Ingestion  Audit  Policies  Settings            │
├──────────────────────────────────────────────────────────────────────────────┤
│ ← Review queue   CASE / pay_001057                         [Refresh records]  │
│                                                                              │
│ PAYMENT PAY_001057                         HIGH · DUPLICATE BANK CREDIT       │
│ What happened: two bank credits carry the same settlement reference.         │
│                                                                              │
├──────────────────────────────────────────────┬───────────────────────────────┤
│ THE RECONCILIATION LINE                      │ DECISION BRIEF                 │
│                                              │                               │
│ capture ──────────────────────────────┐      │ Expected       ₹9,616.56      │
│ settlement ───────────────────────────┼──────│ Actual         ₹9,616.56      │
│ refund ───────────────────────────────┘      │ Difference     duplicate       │
│ bank credit ────────────────┬─────────────── │                               │
│                             └ duplicate      │ What the evidence says        │
│                                              │ Two credits share the same    │
│ [source legend] [redline explanation]        │ UTR family. Review the extra  │
│                                              │ credit before closure.        │
├──────────────────────────────────────────────┼───────────────────────────────┤
│ SOURCE EVIDENCE                              │ POLICY NOTE                   │
│                                              │                               │
│ Merchant payment                            │ Plain-language rule           │
│ Captured gross       ₹9,849.00               │ A bank reference must be      │
│ Payment ID           pay_001057              │ globally unique.               │
│                                              │                               │
│ Gateway settlement                          │ Recommended action             │
│ Reported net         ₹9,616.56               │ Audit the nodal credit journal │
│ Batch ID             set_001057              │ and verify the double credit. │
│                                              │                               │
│ Customer refund         No refund            │ [View cited policy passages]  │
│                                              │                               │
│ Bank credit                                 │ Technical retrieval details   │
│ UTR 1                UTR00001057             │ (collapsed by default)        │
│ UTR 2                UTR00001057_DUP         │                               │
├──────────────────────────────────────────────┴───────────────────────────────┤
│ RECORD A REVIEW DECISION                                                     │
│ Reviewer [finance_ops_reviewer]   [Approve match] [Reject record] [Escalate] │
│ Rationale [Explain what you found and why this decision is defensible...]     │
│ [Record decision]                                                             │
│                                                                              │
│ AUDIT RECEIPT                                                                 │
│ No decision recorded yet · after submission, show signer, time, rationale,  │
│ case version, and a link to the audit ledger.                                │
└──────────────────────────────────────────────────────────────────────────────┘
```

### Case workspace — mobile

```text
┌──────────────────────────────┐
│ LEDGERLENS              MENU │
├──────────────────────────────┤
│ ← Queue                      │
│ PAYMENT PAY_001057           │
│ HIGH · DUPLICATE CREDIT      │
│                              │
│ WHAT HAPPENED                │
│ Two bank credits share the   │
│ same settlement reference.  │
│                              │
│ DECISION BRIEF               │
│ Expected       ₹9,616.56    │
│ Actual         ₹9,616.56    │
│ Difference     Duplicate    │
│                              │
│ ┌──────────────────────────┐ │
│ │ RECONCILIATION LINE      │ │
│ │ capture ────────┐        │ │
│ │ settlement ────┼─ redline│ │
│ │ bank credit ───┘ duplicate│ │
│ └──────────────────────────┘ │
│                              │
│ SOURCE EVIDENCE              │
│ [Payment] [Settlement]      │
│ [Refund] [Bank credit]       │
│                              │
│ POLICY NOTE                  │
│ A bank reference must be     │
│ globally unique.             │
│ [View cited passages]        │
│                              │
│ RECORD DECISION              │
│ [Approve] [Reject] [Escalate]│
│ [Rationale textarea]         │
│ [Record decision]            │
│                              │
│ AUDIT RECEIPT                │
│ No decision recorded yet     │
└──────────────────────────────┘
```

## Wireframe acceptance questions

Before styling, confirm:

1. Can a user understand the financial problem within five seconds?
2. Can a case reviewer find expected, actual, difference, evidence, policy, and next action without decoding technical labels?
3. Does the same Reconciliation Line appear in both surfaces without becoming repetitive decoration?
4. Does the mobile layout preserve the decision path rather than merely stacking desktop cards?
5. Are technical details available but subordinate to the user’s decision?
