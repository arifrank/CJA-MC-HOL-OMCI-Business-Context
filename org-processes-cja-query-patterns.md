---
filename: org-processes-cja-query-patterns.md
title: OCMI Query Patterns and Component Verification
summary: Focused OCMI analysis recipes linked to canonical definitions and current component discovery.
layer: org
sandbox: end-to-end
category: org-processes
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI query patterns

## Applicability
Apply only when an OCMI version is explicitly identified or confirmed in the conversation, in end-to-end. Generic CJA does not activate these recipes. Do not auto-select OCMI or switch sandboxes. Stop on a non-OCMI view. Establish the exact version before applying any mapping.

## Common workflow
1. Preserve the user's question, established view, period, metrics, scope and filters unless changed explicitly. Clarify only meaningful ambiguity; industry selection is not a mandatory step for every question.
2. Discover current standard and calculated metrics, dimensions, and saved segments. The [catalog](naming-conventions-ocmi-metrics.md) is a historical snapshot, not the complete current inventory.
3. Verify business meaning, aggregation, coverage and relevant settings. Inspect saved definitions before reuse. Apply [segment safeguards](guardrails-cja-segment-syntax.md).
4. Use [attribution defaults](guardrails-cja-attribution-models.md) only when appropriate. Preserve configured settings for routine reports; explicit journey-credit questions default to Algorithmic/Person/30 days unless overridden.
5. Report only successful, correctly scoped results. Include relevant assumptions and limitations; use current Coworker presentation, not fixed historical layouts/buttons. Offer focused follow-ups rather than running unrelated cuts.

## Campaign performance
Determine whether the user wants combined performance, channel ranking, campaign detail or a person/session cohort. Discover the relevant delivery, engagement and verified conversion metrics without retrieving every channel's metrics by default. Campaign lookup names and tracking codes may differ. Use verified monetary revenue when requested; do not mix incompatible channel or recipient populations. Apply [rate definitions](guardrails-cja-engagement-thresholds.md).

## Revenue and purchases
Use [revenue selection](guardrails-cja-revenue-disambiguation.md) and [channel architecture](org-other-ocmi-revenue-model.md). Supporting orders, units, AOV, cost or margin are relevant only when requested or necessary to answer the question. Do not assert complete omni-channel coverage from a metric label. Verify any reconstruction before using it.

## Cart, checkout and conversion
Historical candidate flow: Product Views → Cart Additions → Cart Views → Checkout Step 1 → Checkout Step 2 → qualifying purchase. Verify each signal, population and scope. Do not count all-channel orders as digital checkout completion without establishing the relationship. Use ordered eventual progression when it matches the question; do not imply a raw event-count ratio is a person/session funnel. Canonical rates are in [measurement checks](guardrails-cja-engagement-thresholds.md).

## Customer profile, loyalty and propensity
Resolve the requested attribute in the selected version and inspect configuration/coverage. Profile Loyalty Tier and event-level Customer Tier can represent different values or timing; combined demographic groups are not interchangeable with separate age/gender attributes. Do not automatically introduce Participation or substitute attributes to eliminate missing values. A No value result alone does not prove a broken relationship. Offer any meaning-changing alternative explicitly and obtain agreement.

## Ordinary engagement and media
Content Views, shares, downloads, searches, media starts/completes/time spent are ordinary engagement candidates, distinct from Content Analytics creative attributes. Verify metrics and units. Completion rates require matched populations and counting methods. [Content Analytics-specific guidance](org-other-ocmi-content-analytics.md) requires both confirmed OCMI and a specific Content Analytics question.

## Satisfaction and voice of customer
Distinguish profile-level scores/status from event-level survey values; verify scale, aggregation and population. Do not automatically change attribution or substitute a hit-level score for a profile measure. Missing results do not establish a profile defect.

## Cross-channel research and purchases
Use [canonical ROPO definitions](org-other-ocmi-segments.md). Distinguish same-person cohort membership from the purchase events actually counted. Validate ordering, purchase evidence, exclusions and elapsed-time requirements. Category/product matching is optional unless explicitly requested.

## Forecasts and presentation
Use [native forecasting guidance](org-other-cja-forecasting.md). [Response personas](org-processes-cja-personas.md) apply only when explicitly mentioned by the user; otherwise typical behavior applies.
