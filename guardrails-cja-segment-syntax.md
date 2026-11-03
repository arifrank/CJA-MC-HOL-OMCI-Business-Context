---
filename: guardrails-cja-segment-syntax.md
title: OCMI Segment Validation and Evidence
summary: Current construction safeguards with dated, version-specific observations instead of blanket prohibitions.
layer: org
sandbox: end-to-end
category: guardrails
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI segment safeguards

## Applicability
Apply only to explicitly identified or conversation-confirmed OCMI versions in end-to-end. Do not activate for generic CJA, auto-select OCMI, or switch sandboxes. Stop when the user switches to a non-OCMI view. Resolve actual components and supported scopes for the selected version.

## Current capability review
The October 2026 segment guide reviewed November 3, 2026 documents metric occurrence conditions, numeric comparisons on metric totals, exclusions, and elapsed-time restrictions between sequence checkpoints. Original failures using different constructions do not establish that these business operations are unsupported.

Use current documented grammar; validate sequential definitions before reporting. Reuse a saved segment only after inspecting whether its business meaning, scope, purchase evidence and timing match the request. A validation pass does not prove successful execution or semantic correctness. Prefer request-local definitions for one-off analyses; save reusable components only when requested.

Multiple global report filters are combined with AND. They are not a generic OR/exclusion mechanism. Express union/exclusion inside the correctly scoped definition where supported, and validate it. Do not substitute channel equality for purchase occurrence when purchase is required.

Inspect report errors as well as returned values. A rejected inline segment can leave an unfiltered result; never present those values as a successful filtered answer. Fix and rerun within the current workflow's retry limits, or clearly report the limitation.

## Time and scope
The report period, sequence observation window, and maximum time between research and purchase are distinct. A report date range does not replace an explicit elapsed-time condition. Do not broaden scope or remove ordering/timing silently to make a construction succeed.

## Historical observations
The original July 2026 context reported failures for metric-as-dimension existence/comparison constructions, misplaced time modifiers, and generic negation constructions. Preserve these as historical syntax observations only; use the supported metric occurrence/total, sequence-restriction and exclusion mechanisms documented currently.

The original People-metric unauthorized observation did not retain evidence establishing an identity-stitching cause. Remove that diagnosis and the claim that another count is equivalent. The November 3, 2026 HOL catalog exposes a component labeled People; discovery alone does not demonstrate report execution or interchangeable identity semantics.

## Evidence standard
For each future test record exact version, date, definition and scope, component mappings, report period, validation result, execution errors/results, and business checks. No live segment execution tests were performed in this context revision.

## Related guidance
- [Canonical cohort definitions](org-other-ocmi-segments.md)
- [Query patterns](org-processes-cja-query-patterns.md)
