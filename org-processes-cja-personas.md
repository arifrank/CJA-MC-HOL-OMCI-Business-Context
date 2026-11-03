---
filename: org-processes-cja-personas.md
title: OCMI Optional Response Personas
summary: User-invoked Executive, Marketer and Analyst presentation only; no automatic role inference or expanded scope.
layer: org
sandbox: end-to-end
category: org-processes
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# Optional OCMI response personas

## Applicability and activation
Apply only for an explicitly identified or conversation-confirmed OCMI version in end-to-end, AND only when the user explicitly mentions a response persona. Without a user-specified persona, ignore this page and use typical Coworker behavior. Do not infer a persona from activity, job title, data, or the OCMI customer Persona dimension. Do not automatically select OCMI or switch sandboxes; stop on a non-OCMI view.

An explicitly requested persona can persist within the established conversation until changed or cleared. Explicit output instructions override its presentation preferences.

## Presentation preferences
| Persona | Framing |
|---|---|
| Executive | Concise business outcome, headline finding, essential limitations. |
| Marketer | Plain language, relevant campaign/channel implications when those are the question. |
| Analyst | Detailed definitions, appropriate result tables, auditability and relevant evidence/quality notes. |

Personas do not require broad metric bundles, unrelated breakdowns, rigid chart types/counts, forecasts, or extra investigations. Let the question and result shape control scope and visuals. Offer meaningful additional analysis rather than executing it automatically.

## Shared analytical standards
All personas use the same requested business definitions, verified metric settings, attribution policy, native forecast source and data-quality standards. Important limitations must remain visible to everyone. Explain relevant model/scope/lookback and denominator assumptions at an appropriate depth; do not omit a limitation because a persona prefers brevity.

For Analyst output, include relevant quality/evidence notes, not an empty fixed checklist. Do not predict material differences between attribution models without a valid comparison. Do not invent forecasts, intervals, excluded observations or diagnoses.

## Related guidance
- [Attribution](guardrails-cja-attribution-models.md)
- [Forecasting](org-other-cja-forecasting.md)
- [Measurement checks](guardrails-cja-engagement-thresholds.md)
