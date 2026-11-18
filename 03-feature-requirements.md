# Proposed Feature Requirements

> All requirements describe **planned capabilities**. None has been implemented or empirically validated as of this Round 1 documentation release.

## F1 — Multilingual voice and text assistant

- Select English, Kannada or Kannada–English mixed mode.
- Switch languages without losing validated product fields.
- Support speech transcription **only if testing demonstrates acceptable accuracy**; text fallback remains available.
- Separately identify ingredient names, amounts and units, normalize quantities and read back uncertain data before recording.
- Never silently turn low-confidence speech into approved product declarations.

## F2 — FSSAI registration guidance

- Ask about business type, activity, scale and other relevant criteria.
- Use a curated, current and source-linked decision tree; avoid a simplistic turnover-only test.
- Display provisional pathways and information/document gaps; link to official FoSCoS.
- Never claim to register, license or officially verify a business without a real authorized integration.

## F3 — Smart label studio

- Create a fixed-template PDF for a supported food/product/packaging scenario.
- Identify missing, inconsistent or unsupported fields using a small **deterministic** legal rulebook.
- Store legal source, version, scope, effective date and reviewer for every rule.
- Show label states: draft, pending review, approved for a particular product version, superseded/blocked.
- Preserve historical labels on batches even after the current recipe changes.

## F4 — Shelf-life and claims evidence tracking

- Store proposed shelf life, test/evidence references, packaging conditions and review status.
- Flag missing nutrition, claims or shelf-life evidence as unresolved; never generate fictitious laboratory values or scientific support.
- Keep draft copy separate from approved declarations.

## F5 — Pricing and profitability calculator

- Input ingredients, packaging, labour, logistics, fees and expected returns; distinguish variable contribution from full profit.
- Compare local sales with **one illustrative** marketplace scenario.
- Clearly mark estimates and assumptions as editable, not real-time marketplace pricing.
- Require producer confirmation for finalized sale prices.

## F6 — Batch traceability and recall assistance

- Store batch ID, production dates, product version, label version, quantity, stock and recorded orders.
- Locate batches and related orders during a simulated incident.
- Draft internal actions and notifications subject to human sign-off.
- Escalate promptly to the official authority/food-safety experts when required; do not present in-app assistance as an official recall submission.

## F7 — Buyer Readiness Report

- Collate producer and product information, registration status, label check results, evidence gaps, costs, batch completeness and next steps.
- Tag each requirement LAW, BUYER POLICY or BEST PRACTICE.
- Include provenance, dates, uncertainty and approvals; do not display an invented compliance certification score.

## F8 — Agentic task orchestration

- Coordinate tasks through explicit states and tool permissions.
- Track every meaningful action, source and approval status.
- Invalidate *future* dependent label approvals and readiness reports after relevant product changes; keep historic batch records intact.
- Apply rule changes only when their in-force date and applicability scope justify it.
- Do not permit language models to bypass deterministic checks or human approvals.
