---
filename: org-other-ocmi-revenue-model.md
title: OCMI Channel Revenue Architecture
summary: Historical channel architecture with verified coverage required for totals, AOV and margin.
layer: org
sandbox: end-to-end
category: org-other
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI revenue architecture

## Applicability
Apply only to an explicitly identified or conversation-confirmed OCMI version in end-to-end. Do not auto-select OCMI, activate for generic CJA, or switch sandboxes. Stop on non-OCMI views. Historical architecture is not proof of current complete coverage.

## Historical channel candidates
| Channel | Order candidate | Revenue candidate |
|---|---|---|
| Web/mobile web | purchase | purchase price |
| Mobile app | event94 | event115 |
| Call center | event126 | event128 |
| Point of sale | event121 | event92 |

Historical combined candidates: Total Revenue event138, Total Orders event140, Total Units event139, Total Product Cost event141, Total Discount event142. Resolve actual current component paths, aggregation and coverage. See [revenue selection](guardrails-cja-revenue-disambiguation.md) for canonical monetary selection safeguards.

## Unified versus channel measures
For an unspecified-channel revenue/order question, prefer a verified combined measure. For a specific channel, use the matching verified measure. A combined label does not guarantee all channels are populated, nor that a web-only result indicates a known benign limitation. Check the evidence and disclose actual coverage.

Do not automatically reconstruct a missing total. Any channel sum requires verified compatible measures, currency, period, aggregation, non-overlapping channels and complete coverage. Shared or overlapping events can double count.

## Derived measures
AOV = verified monetary revenue divided by compatible order count for the same eligible population. Gross Margin amount = verified revenue minus compatible product cost. This is an amount, not margin percentage, and may not include other operating costs. State actual cost coverage. A margin percentage, if requested, requires its explicitly defined denominator.

In-App Units is unverified for the checked HOL version: neither conflicting event116/event117 mapping was found in the complete standard-metric catalog including hidden metrics on November 3, 2026. This does not prove source data absence or identify a replacement. Do not reconstruct Total Units with an assumed app-unit component.

## Related guidance
- [Rate definitions](guardrails-cja-engagement-thresholds.md)
- [Historical component catalog](naming-conventions-ocmi-metrics.md)
