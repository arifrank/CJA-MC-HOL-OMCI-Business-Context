---
filename: org-other-ocmi-segments.md
title: OCMI Canonical Cohort Definitions
summary: Verified-purchase ROPO, channel, loyalty and purchase cohorts with explicit scope and time rules.
layer: org
sandbox: end-to-end
category: org-other
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI cohort definitions

## Applicability
Apply only when an OCMI version is explicitly identified or confirmed in the conversation, in end-to-end. Do not activate for generic CJA, auto-select OCMI or switch sandboxes. Stop on non-OCMI views. These are business definitions, not proof that saved components implement them. Inspect actual saved definitions and verify version-specific signals.

## Canonical ROPO definitions
ROPO means Research Online, Purchase Offline.

| Cohort | Definition |
|---|---|
| Strict ROPO | Same person performs qualifying online product/category research, THEN a verified in-store purchase. Website, mobile web and app research qualify where verified. Same-product/category matching is not required unless requested. |
| Loose research-and-purchase | Same person has qualifying online research AND a verified in-store purchase, without enforcing order. Directional cohort, not proof research preceded purchase. |
| Exclusive ROPO | Strict ROPO plus no verified online purchase in the stated exclusion period. Define web, mobile-web and app purchase coverage explicitly. |
| Cross-channel interaction | Online and store activity without verified purchase evidence. Do not label these people ROPO purchasers. |

An Interaction Channel value of Point Of Sale alone is not proof of an order. Research criteria, purchase occurrence, identity scope, ordering, analysis period, exclusion period and maximum elapsed time must be explicit. A report date range is not a replacement for a requested research-to-purchase delay. Validate definitions using [segment safeguards](guardrails-cja-segment-syntax.md).

Cohort membership and reported purchase events are distinct. A person-level segment can include events outside the particular qualifying purchase; ensure reported purchase counts match the question. Do not assert matched categories, exclusivity or timing unless actually enforced.

## Other business cohorts
- Web Only / App Only: people with qualifying activity in the stated channel and no qualifying activity in other covered channels during the period. Define activity and coverage; do not infer absence from partial data.
- Call Center / In-Store: define whether the scope is events, sessions or people and whether activity or actual purchase is intended.
- Multi-Channel: people with qualifying activity in at least two distinct covered channels during the stated period.
- Loyalty tiers: resolve the requested profile or event-level tier and timing; these are not automatically equivalent. Explicit non-membership and missing tier values are separate unless the user agrees otherwise.
- Cart Abandoners: eligible cart/cart-session population without a verified qualifying purchase under the agreed period/scope. See [rate rules](guardrails-cja-engagement-thresholds.md).
- Repeat / One-Time Buyers: people with at least two / exactly one verified qualifying purchases in the stated period; deduplicate as required by the business definition.
- High-Value Customers: define eligible population, monetary measure and threshold; if using a percentile specify its population and period, rather than assuming a universal 75th percentile.
- Lapsed Customers: prior verified purchasers with no qualifying purchase during an explicitly defined recent period. No activity is a different inactivity cohort; do not interchange them. A 90-day window is not implicit unless requested or established.

## Evidence
Definitions were revised by user agreement November 3, 2026; no live segment execution was performed. Historical channel-only recipes were removed because they did not necessarily establish purchase or research evidence.
