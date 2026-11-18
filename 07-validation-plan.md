# Technology Validation Plan

> **Status: 0 / 6 hands-on validation areas completed.** Desk research and candidate selection are not equivalent to an empirical benchmark or a passing test.

## Checklist

| ID | Test | Current state | Evidence required to mark complete |
|---|---|---|---|
| V1 | Benchmark Kannada and Kannada-English speech on real recordings | **Not run** | Consent-based representative recordings, reference transcripts, provider/version, WER/CER, costs/latency, error analysis |
| V2 | Verify ingredient, quantity and unit extraction separately | **Not run** | Ground-truth labelled utterances, exact-match metrics by field, ambiguity and correction logs |
| V3 | Map official rules for one retail pickle jar | **Research incomplete** | Primary rule text, reviewer-checked requirement table, scope/exceptions, dates, citation per check |
| V4 | Effective-date and product-applicability filtering | **Not run** | Passing tests for in-force, future, superseded, in-abeyance and unrelated-product cases |
| V5 | Recipe-change approvals and traceability dependencies | **Not run** | Regression tests preserving historical batches while invalidating applicable future outputs |
| V6 | Human sign-off and FoSCoS recall escalation | **Not run** | Attempts to bypass approval fail; simulated verification clearly marked; official escalation links and response steps checked |

## V1 — Speech benchmark protocol

Collect diverse (consented) Kannada, English and code-switched recordings containing Kannada ingredient names, English units, numeric quantities, prices and recipe corrections. Include background noise, regional pronunciation and varied speaking rates. Compare candidate providers with the same audio and reference transcripts. Track:

- Word error rate (WER) and character error rate (CER), where suitable for script differences.
- **Ingredient name**, **number** and **unit** extraction separately; a transcription can be linguistically close while the amount is dangerous.
- Code-switched quantity accuracy, latency and measured cost.
- Clarification frequency, read-back success and failure modes.

**Speech-provider choices are not finalized.** Google Chirp 3 Kannada availability has been described as Preview in provider documentation; this is not proof of performance. BHASHINI access and specific model suitability remain unverified. Sarvam Saaras v4/v3 are candidates, not winners.

## V2 — Extraction protocol

For each spoken/text recipe, use a reviewed ground truth containing `ingredient_name`, `raw_amount`, `normalized_amount`, `unit`, `certainty`, and `user_confirmation` fields. Test ambiguous phrases such as “one packet,” “half cup,” number code-switching and similar-sounding ingredient names. Do not infer grams from a cup or packet without the necessary product-specific conversion evidence.

## V3 & V4 — Legal checks

Create a narrow, date-aware rulebook for the supported mango-pickle retail jar. For each rule: cite the source, law vs channel policy, exact applicability, exceptions, in-force status, effective date and reviewer. Evaluate only relevant rules. A future milk-logo requirement or unrelated product rule must not be treated as applicable to mango pickle.

## V5 — Versioning invariants

1. Historical batch `MP-001` retains the label version used at its production.
2. Change of ingredient/recipe creates a **new** product version.
3. Future dependent label approval and readiness reports become stale, never silently stay approved.
4. Cost assumptions are recomputed or marked pending after an input change.
5. An unrelated rule change does not invalidate an unaffected product.
6. Failed workflow transitions leave records internally consistent and auditable.

## V6 — Human approval and escalation

- Block label finalization, price finalization, sharing and external messages without the correct human approval.
- Never invent shelf life, nutrition evidence, claim substantiation or government verification.
- Distinguish a *simulated incident workflow* from a legally required recall/withdrawal notification.
- Show official FoSCoS links and clearly state when live official connectivity is absent.

## Suggested testing priority

**First:** speech/quantity safety + official rule scoping; **second:** approvals/versioning; **third:** recall practice and full journey. If time is short, keep input as **text** rather than claiming voice support that has not passed tests.

## Acceptance reporting

Every item should end with a dated test record: sample set, environment, provider/rule version, expected behavior, actual behavior, pass/fail, known defects and responsible reviewer. Never convert “planned” to “passed” based only on documentation.
