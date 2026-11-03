---
filename: guardrails-cja-revenue-disambiguation.md
title: OCMI Revenue Metric Selection
summary: Verify monetary meaning, aggregation, currency, coverage and attribution for each OCMI version.
layer: org
sandbox: end-to-end
category: guardrails
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI revenue selection

## Applicability
Only for an explicitly identified or conversation-confirmed OCMI version in end-to-end. Generic CJA questions do not activate this page. Do not automatically select OCMI or switch sandboxes. Stop on non-OCMI views. Mappings below are historical candidates, not universal version-independent rules.

## Selection safeguards
Revenue means monetary revenue in every industry. Discover standard and calculated candidates in the selected version; verify source field, aggregation level, business meaning, currency, channel coverage, and existing attribution. Similar names do not establish equivalent measures. Prefixes/suffixes are discovery clues, not proof of semantics.

Prefer verified omni-channel monetary revenue for an unspecified-channel revenue question. For explicit channel questions use verified matching channel coverage. If only partial coverage is available, name it prominently. Do not invent missing channels or silently substitute orders, applications, appointments, enrollments, or form completions.

## Historical HOL candidates
| Historical label | Candidate component path | Historical observation |
|---|---|---|
| Total Revenue | metrics/productListItems._experience.analytics.event101to200.event138.value | Original context identifies this product-line-item variant as the monetary candidate. Verify current configuration and coverage. |
| Total Revenue (Linear) | metrics/_experience.analytics.event101to200.event138.value | Original June 2026 observation reported order-scale values despite the label. Do not choose it as a monetary/Linear shortcut from its name. |
| Total Revenue (Last Touch 30 Days) | metrics/productListItems._experience.analytics.event101to200.event138.value_1 | Original context describes a pre-attributed variant; verify actual settings rather than inferring from the suffix. |

The historical June 2026 source reported that the unprefixed variant and Total Orders both returned 770,722 over an unspecified 90-day window. Exact dates and execution evidence are not retained here; this is historical caution, not a current result or universal equality claim.

The November 3, 2026 review inspected the standard-metric catalog for Omni-Channel - Multi-Industry (HOL), not live revenue results or all component configuration. Do not label these candidates fully verified from that check.

## Attribution and derived measures
Use [canonical attribution guidance](guardrails-cja-attribution-models.md). Report-time model changes need not create saved components. Do not confuse a label containing Linear with verified attribution. AOV requires compatible monetary revenue and order coverage. Margin follows the [revenue architecture](org-other-ocmi-revenue-model.md).
