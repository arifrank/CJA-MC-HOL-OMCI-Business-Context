---
filename: org-other-ocmi-content-analytics.md
title: OCMI Content Analytics Reference
summary: Separately scoped historical creative-attribute catalog; requires a confirmed OCMI version and Content Analytics-specific request.
layer: org
sandbox: end-to-end
category: org-other
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI Content Analytics reference

## Applicability
Apply only when BOTH the OCMI version has been explicitly identified or confirmed in the conversation AND the user asks a Content Analytics-specific question about assets, experiences or creative attributes. Restricted to end-to-end. Generic CJA or generic content performance does not activate this page. Do not auto-select OCMI or switch sandboxes. Stop on a non-OCMI view.

Ordinary content views/shares/downloads/search and media engagement remain in [standard query patterns](org-processes-cja-query-patterns.md). This page preserves material separated from the original catalog and recipe, not a verified current implementation.

## Historical attribute catalog
| Attribute | Historical mapping |
|---|---|
| Experience ID | eVar152; described as campaign image filename |
| Asset ID | list1 |
| Asset Tags, Asset Type, Asset Image Type | No fixed mapping retained |
| Asset Orientation, Overall Tone | No fixed mapping retained |
| Asset Background Colors, Foreground Colors | No fixed mapping retained |
| Asset Scenes, Objects, People Categories | No fixed mapping retained |
| Asset Camera Position, Photography Styles, Lighting Conditions | No fixed mapping retained |
| Experience Attributes, Keywords, Tones | No fixed mapping retained |
| Experience Narratives, Persuasion Strategies, Marketing Emotions | No fixed mapping retained |

Historical metric candidates: Asset Views event169, Asset Clicks event171, Experience Views event168, Experience Clicks event170. These original mappings are unvalidated snapshots; discover current components for the exact version. Do not assume they match current Content Analytics-native fields or exist in every OCMI version.

## Preserved analysis intent
The original recipe asked which assets/experiences or creative attributes perform, using asset/experience views and clicks with campaign or demographic breakdowns. Resolve the user's actual outcome and whether the question concerns engagement or downstream conversions. Do not impose all creative dimensions or a fixed chart layout by default.

For downstream conversions and separate-event dimensions, use [cross-event attribution safeguards](org-other-cja-cross-event-attribution.md) and [canonical attribution policy](guardrails-cja-attribution-models.md). No automatic saved component creation or unverified attribution-label shortcut. Missing values and model association do not prove a cause.

## Evidence
Preserved from the July 2026 source, separated November 3, 2026. No live Content Analytics mapping/report test was performed during this revision. Verify metric and attribute availability and business meaning before use.
