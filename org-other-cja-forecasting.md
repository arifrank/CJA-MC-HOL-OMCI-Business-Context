---
filename: org-other-cja-forecasting.md
title: OCMI Native Forecasting and Data-Gap Review
summary: Native CJA forecasts, returned ranges and supported granularity; no separately fitted fallback.
layer: org
sandbox: end-to-end
category: org-other
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI native forecasting

## Applicability
Use only for an explicitly identified or conversation-confirmed OCMI version in end-to-end. Generic CJA does not activate this page. Do not auto-select OCMI or switch sandboxes. Stop on non-OCMI views. Verify the selected metric and current forecasting support.

## Forecast source and interpretation
Use forecasts and forecast ranges returned by CJA only. Do not fit, extrapolate or invent a replacement forecast if native forecasting fails or returns no usable forecast. Explain the established limitation and distinguish historical actuals from unavailable projections.

The current connected capability reviewed November 3, 2026 documents hourly, daily, weekly and monthly forecasts for a single time dimension. Do not assume quarterly forecasting is reachable merely because quarterly reporting exists. Request the supported granularity matching the user's question; do not roll daily bounds into monthly ranges.

Preserve calendar/timezone alignment and state the history and horizon used. Separate complete actual periods, in-progress actuals and forecasts. Do not plot partial actuals as complete periods. A zero in the actual-value field for a future date does not establish a zero forecast or model failure; inspect the forecast fields and missing-data indicators.

Show the returned range without manufacturing a confidence label, fitted-model score, or summed-interval formula. Bounds cannot be summed as a horizon range. Only aggregate native forecast point values where the current workflow permits and the metric is additive; distinct-person counts, rates and averages are not additive. If presenting an additive current-period actual-plus-forecast total, do not invent a range for it.

## Data-quality review
A zero primary metric between nonzero days, corroborated by a secondary metric also being zero, is a possible gap signal—not proof of a collection outage. Inspect evidence before assigning a cause. Flag possible gaps and limits visibly; never silently delete or interpolate observations. Warn when substantial missing periods limit interpretation without claiming the native forecast's internal handling was changed.

## Evidence
The old claim that native forecasts often return zeros and the automatic statistical fallback have been removed. Native forecasting support was reviewed, but no live forecast test was run against an OCMI version during this revision. Adobe documents a forecasting service modeling trend and seasonality; do not replace it with persona-specific fitted models.

## Source
- [Forecasting statistical techniques](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/forecasting/statistics-forecasting)

## Related guidance
- [Optional personas](org-processes-cja-personas.md)
- [Measurement checks](guardrails-cja-engagement-thresholds.md)
