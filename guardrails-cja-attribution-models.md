---
filename: guardrails-cja-attribution-models.md
title: OCMI Attribution Models and Evidence
summary: Correct model definitions, OCMI attribution defaults, and version-specific capability verification.
layer: org
sandbox: end-to-end
category: guardrails
origin: revised
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI attribution models

## Applicability
Apply only when the user explicitly identifies an OCMI data view version or that version has already been confirmed in the conversation. Generic CJA questions do not activate this guidance. Do not automatically select OCMI or switch sandboxes. Stop applying it when the user switches to a non-OCMI view. This page is restricted to end-to-end; verify configuration for the exact version.

## Business defaults
Honor explicit user instructions and established analysis settings first. Routine reporting preserves the selected metric's verified attribution configuration; do not assume an unmodified metric means Last Touch or Same Touch. For explicit journey-credit attribution questions with no established model, the OCMI business default is Algorithmic, Person scope, and a 30-day lookback. This is an agreed organizational convention, not a universal product default. Confirm that the settings can actually be applied. Report period and lookback are separate.

## Canonical model definitions
| Model | Allocation |
|---|---|
| Last Touch | 100% to the most recent eligible touch before conversion. |
| First Touch | 100% to the first eligible touch within the lookback window. |
| Linear | Equal credit across eligible touches. |
| Participation | 100% to each unique touchpoint; sums can exceed the conversion total. |
| Same Touch | Credit to the touchpoint on the conversion event; otherwise None. |
| U-Shaped | 40% first, 20% shared among middle touches, 40% last. |
| J-Curve | 20% first, 20% shared among middle touches, 60% last. |
| Inverse J | 60% first, 20% shared among middle touches, 20% last. |
| Time Decay | Exponential weighting favoring recent touches, using a configurable half-life; documented default 7 days. |
| Custom | User-defined first/middle/last weights normalized to 100%; not necessarily U-Shaped. |
| Algorithmic | Dynamic statistical allocation based on the Harsanyi Dividend, a generalization of Shapley value. |

For U-Shaped and the J models, a single touch receives 100%. For two touches, U-Shaped splits 50/50; J-Curve splits 25% first/75% last; Inverse J splits 75% first/25% last. Do not interpret fixed three-part weights as separate middle credit when there are no middle touches.

## Current capability and evidence
The connected reporting capability reviewed on November 3, 2026 documents report-time attribution for standard metrics, including First Touch, Last Touch, Time Decay, Custom, and Algorithmic. Do not create saved components solely to apply report-time attribution. Calculated metrics have different override constraints: inspect their definitions and current supported behavior rather than assuming standard-metric overrides apply.

Documented construction does not prove execution on an OCMI version or entitlement. Algorithmic/custom lookback settings can depend on entitlements. Inspect the actual response. If a requested model cannot be applied, explain the limitation and obtain agreement before substituting. Algorithmic is not equivalent to First Touch; Inverse J is early-weighted and is not a back-weighted Time Decay proxy.

July 2026 failures in the original context are historical observations about particular constructions, not permanent model prohibitions. Exact test payloads/report periods are not fully preserved here; do not label those observations current verified tests.

## Evidence records
For future tests record date, exact view/version, metric and dimension, model, scope, lookback, report period, construction, execution result, and uncertainty. Separate documented support, validation success, successful execution, and business-meaning verification.

## Sources
- [Attribution components](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/attribution/models)
- [Attribution component settings](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution)

## Related guidance
- [Revenue selection](guardrails-cja-revenue-disambiguation.md)
- [Cross-event attribution](org-other-cja-cross-event-attribution.md)
