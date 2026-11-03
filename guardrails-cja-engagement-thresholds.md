---
filename: guardrails-cja-engagement-thresholds.md
title: OCMI Rate Definitions and Measurement Checks
summary: Matched populations, counting units and historical baselines; no unsourced fixed benchmarks.
layer: org
sandbox: end-to-end
category: guardrails
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI measurement checks

## Applicability
Use only for an explicitly identified or conversation-confirmed OCMI version in end-to-end. Do not activate for generic CJA, auto-select OCMI, or switch sandboxes. Stop on a non-OCMI view. Verify every component against the selected version.

## Canonical rate rules
Before calculating, define the eligible population, channel coverage, reporting period, counting unit, numerator and denominator. Verify matching coverage and comparable counting methods. Name the denominator in the output. Handle a zero denominator as unavailable, not zero conversion.

- Cart conversion: share of qualifying carts or cart sessions with a verified purchase under the stated definition. Do not divide all-channel orders by digital cart opens without establishing comparability.
- Cart abandonment: complement of cart conversion only when it represents non-converting eligible carts under that definition. State observation window; late conversions can change interpretation.
- Product-to-cart and checkout completion: match eligible product/checkout cohorts and outcomes. Raw event ratios may represent activity intensity rather than person/session conversion; label accordingly.
- Overall conversion: identify the business conversion and explicitly name whether the denominator is eligible people, sessions, carts, or another population.
- Email rates: distinguish unique recipients from total opens/clicks. Define sent versus delivered populations explicitly. Click-to-open requires a comparable opener population.
- Advertising CTR: match the click and impression populations, channels and counting method.

If compatible signals are unavailable, explain the limitation and offer a labeled alternative. Never silently change populations, counting units, or channels to produce a rate.

## Baselines, not unsupported thresholds
The original numeric 'typical industry' ranges and fixed suspicion thresholds were unsourced and have been removed. Use comparable OCMI historical baselines when available, respecting the same metric definition, period alignment, channel, and population. External benchmarks require source, date, industry, population and counting-method documentation.

An unusual rate is a review signal, not proof of bad data or a statistical anomaly. Investigate duplicate/total events, denominator mismatches, population coverage and available contamination evidence. Do not assert a cause without evidence or change a calculation silently.

## Related guidance
- [Query patterns](org-processes-cja-query-patterns.md)
- [Revenue architecture](org-other-ocmi-revenue-model.md)
