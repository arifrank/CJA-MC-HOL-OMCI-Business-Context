---
filename: org-other-cja-cross-event-attribution.md
title: OCMI Cross-Event Attribution
summary: Attribute outcomes to separate-event touchpoints without changing scope or creating unnecessary saved components.
layer: org
sandbox: end-to-end
category: org-other
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI cross-event attribution

## Applicability
Only when an OCMI version is explicitly identified or conversation-confirmed, in end-to-end. Do not activate for generic CJA, auto-select OCMI or switch sandboxes. Stop on a non-OCMI view. This standard-CJA recipe includes cases such as calls credited to earlier page interactions; it is not limited to Content Analytics.

## Workflow
1. Resolve the outcome metric, eligible outcome conditions and touchpoint dimension for the exact version. Inspect existing component settings and saved filters. Different-event collection can explain missing dimension values but does not guarantee that every unmodified report will return only No value.
2. Specify outcome selection separately from touchpoint eligibility and person/session scope. Verify the requested business meaning.
3. Apply [canonical attribution settings](guardrails-cja-attribution-models.md), using report-time settings for standard metrics when supported. Use request-local definitions for one-off filters/calculations where appropriate; create persistent components only when requested.
4. Preserve eligible journey context. A global event-only filter can remove relevant outcomes or touches; validate its effect rather than assuming it preserves attribution.
5. Inspect validation and execution errors before presenting results. Do not hide, drop, relabel or reinterpret returned rows to make the analysis appear scoped correctly. Prefer correct request scoping or a clearly labeled limitation.
6. Check coverage, missing dimension credit and model-appropriate reconciliation. For conserved-credit models compare attributed outcomes to a compatible outcome total, respecting deduplication and rounding. Participation can exceed the total and requires a different interpretation. Do not impose a universal fixed tolerance or manufacture reconciliation from incompatible populations.

## Historical example
The original source describes Returns & Refunds calls attributed to web pages using a person-scoped Algorithmic calculation, and reports 185,457 attributed calls versus 185,353 filtered calls. Exact reporting dates and the full current component configuration are not retained here. Preserve this as historical illustration, not a verified current result or a fixed reconciliation standard.

## Presentation
Use current Coworker result presentation with relevant settings, coverage and caveats. Remove historical fixed layout/button requirements. Clearly distinguish attributed association from a causal explanation.

## Related guidance
- [Segment validation](guardrails-cja-segment-syntax.md)
- [Query patterns](org-processes-cja-query-patterns.md)
- [Separate Content Analytics reference](org-other-ocmi-content-analytics.md)
