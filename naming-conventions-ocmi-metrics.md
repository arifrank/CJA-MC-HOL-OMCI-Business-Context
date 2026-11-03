---
filename: naming-conventions-ocmi-metrics.md
title: OCMI Version-Specific Component Reference
summary: Historical component candidates and limited HOL catalog evidence; current discovery is required.
layer: org
sandbox: end-to-end
category: naming-conventions
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI component reference

## Applicability
Use only when the user explicitly identifies an OCMI version or that version is confirmed in the conversation. Generic CJA questions do not activate this reference. Do not auto-select OCMI or switch sandboxes. Restricted to end-to-end; stop on non-OCMI views. Verify every mapping for the exact version.

## Snapshot scope and verification
Historical reference view: Omni-Channel - Multi-Industry (HOL), dv_681b875cd7b56a2b266fb9ba; event dataset described as Demo Data CJA midValues. This is not an exhaustive current catalog or a family-wide default.

This compact reference preserves the main historical component categories and candidates; the untouched original source remains the provenance for its longer catalog. All mappings below are historical/unverified unless explicitly described in the limited evidence section. Missing entries do not prove absence. Discover current standard and calculated metrics, dimensions, lookup paths and saved definitions before reporting. Names, event numbers, prefixes and suffixes alone do not verify meaning, aggregation, attribution or coverage.

## Traffic and navigation candidates
| Dimension | Historical variable |
|---|---|
| Page Name; Site Section | pageName; channel |
| Site Subsection; Page Title; Page Type; Page Path | prop1; prop2; prop4; prop9 |
| Country Site; Language Site; Site | eVar13; eVar12; eVar14 |
| Internal Search Term; No. Search Results; Search Results Page | eVar17; eVar18; eVar19 |
| Search Facet ID; Search Facet Value; Navigation Method | eVar20; eVar21; eVar86 |
| Digital Content ID/Type; Blog ID; Download ID; Article ID | eVar25/eVar26; eVar22; eVar27; eVar88 |
| Content ID/Type (traffic); App Search Term; App Versions | prop7/prop8; prop10; prop11 |

Time-dimension candidates include hour, day, week, month, quarter, year, day of week and day of month. Discover support rather than asserting all are always available. Reporting granularity and forecast granularity are separate capabilities.

## Customer, campaign and channel candidates
| Dimension | Historical variable |
|---|---|
| Marketing Channel | eVar1; historically described as 30-day last touch; verify persistence/settings |
| Campaign Vendor; Delivery Method; Landing Page; Tracking Code | eVar2; eVar3; eVar4; campaign |
| Email Message/Recipient ID | eVar5/eVar6 |
| Customer Relationship; Customer Tier; CRM ID | eVar7; eVar8; eVar9 |
| DMA Region; Demographic Group | eVar10; eVar11 |
| Account Type/ID; Registration/Sign-In Method | eVar33/eVar32; eVar34/eVar35 |
| Payment/Fulfillment Method; Order ID | eVar36/eVar37; eVar124 |
| Product ID; Brand ID; Discount Code; Service ID | product; eVar123; eVar84; eVar87 |
| Location ID/City/State/Country | eVar39/eVar41/eVar43/eVar44 |
| Location Size/Type; Representative ID | eVar144/eVar145; eVar146 |
| Interaction Channel | eVar142; historical values Website, Mobile Web, Mobile App, Point Of Sale, Call Center |
| Caller/Call Center/Call ID; Call Duration/Reason/Agent | eVar69/eVar72/eVar105; eVar70/eVar148/eVar165 |
| Form ID/Field/Error | eVar57/eVar58/eVar59 |
| Journey ID; Message Channel | eVar98; eVar169 |
| ECID; Stitched ID | eVar162; eVar163; labels do not establish identity equivalence |
| Customer Persona | eVar60; customer data, NOT activation of a response persona |

Customer Tier and Demographic Group are event-level candidates, not automatic substitutes for profile loyalty, age or gender.

## Purchase and channel candidates
| Channel | Orders | Revenue | Units | Discount | Product cost |
|---|---|---|---|---|---|
| Web/mobile web | purchase | purchase price | purchase quantity | event10 | event9 |
| App | event94 | event115 | Unverified; do not assume event116/event117 | event120 | event119 |
| Call center | event126 | event128 | event127 | event160 | event161 |
| POS | event121 | event92 | event122 | event158 | event159 |
| Historical combined | event140 | event138 | event139 | event142 | event141 |

[Revenue selection](guardrails-cja-revenue-disambiguation.md) owns monetary candidate disambiguation; [revenue architecture](org-other-ocmi-revenue-model.md) owns coverage and derived measures. Do not reconstruct totals automatically. Historical channel-sum recipes for orders, revenue, discount and cost require verified complete, non-overlapping coverage and compatible aggregation/currency. The old Total Units reconstruction formula has been removed because its app-unit input is unverified.

## Checkout and engagement candidates
| Measure | Historical variable |
|---|---|
| Cart Opens/Additions/Removals/Views | scOpen/scAdd/scRemove/scView |
| Checkout Steps 1/2; Product Views | scCheckout/event14; prodView |
| Product Detail/Quick Views; Collection Views | event78/event79; event1 |
| Emails Sent/Delivered/Bounced/Clicked/Unsubscribed | event16/event17/event18/event19/event20 |
| Email Opened; Unique Opens; Unique Clicks | event109; event113; event112 |
| SMS Sent/Delivered/Clicked/Opened | event21/event201/event202/event208 |
| Display Impressions; Campaign Cost | event23; event24 |
| Content Views/Shares/Ratings; Downloads | event25/event26/event27; event29 |
| Internal Searches/No Results/Refinements | event74/event75/event76 |
| Sign-Ins; Lead Form Steps 1/2/Completed | event37; event30/event31/event32 |
| Location Searches; Check-Ins; Self-Service Tool Usage | event43; event42; event50 |
| Chat Requests/Offers/Accepted/Declined/Initiated | event59/event60/event61/event62/event63 |
| Account Creation Steps 1/2/3/Complete | event33/event34/event35/event36 |
| Event Detail/Registration Steps 1/2/Complete | event38/event39/event40/event41 |
| Form Starts/Completes/Errors | event51/event52/event53 |
| In-App Purchase Steps 1/2; Premium Enrollments | event81/event82; event101 |
| BOPIS; Online Return; Return in Store | event199; event198; event195 |
| Calls; Agent Calls; IVR Calls; Call Length/Cost | event193; event85; event88; event166/event167 |
| Offline Orders/Revenue/Units/Discount/Cost | event13/event11/event106/event108/event107 |

All cart conversion, abandonment, product-to-cart, checkout completion, email and overall conversion rates follow [matched-rate definitions](guardrails-cja-engagement-thresholds.md); no unmatched blanket event ratios are prescribed here. Additional messaging channels and AJO metric variants require current discovery.

## Media candidates
Historical media metrics include starts, completes, time spent, resumes, segment/chapter views and completions, progress milestones, pauses, bitrate/buffering/errors/dropped-frame measures. Historical dimensions include media asset/ad/chapter, channel, content type, length and name. Multiple legacy and current schema variants may coexist; discover actual components, units and populations rather than choosing by a historical variable alone. These are ordinary media analysis, not Content Analytics creative attributes.

## Profile and lookup candidates
Profile families preserved from the original catalog: Person ID, Loyalty ID/Tier/Member; CRM age/gender/name/address/contact/occupation/household groups; CLTV score/group; NPS score/status; survey score/sentiment; next-best-offer fields; category affinities; purchase/churn/abandonment/account/loyalty propensity fields; consent flags; partner attributes.

Verify selected-version profile configuration and coverage. No universal Person-plus-Participation requirement applies from this snapshot. A No value result alone does not establish a broken relationship. Do not automatically change attribution or replace a profile value with a potentially different event-level value. See [profile query safeguards](org-processes-cja-query-patterns.md).

Lookup families: Retail Product Name/Subcategory/Browse Category, Campaign Name, and Call Reason. Historical lookup datasets include product, campaign-tracking-code and call-reason lookup datasets. Their schema-path-based component IDs vary; discover current IDs and joins for the exact version.

[Content Analytics catalog and recipe](org-other-ocmi-content-analytics.md) are preserved separately, including the original Experience ID and asset/experience attributes and metric candidates.

## Limited current evidence: November 3, 2026
For the named HOL version in end-to-end, the complete standard-metric catalog including hidden entries was retrieved (401 entries). Neither event116 nor event117 nor a named In-App Units metric appeared. Units, Total Units, POS Units, Offline Units, In-App Orders and In App Revenue were discoverable. This establishes catalog availability only, not source-data presence, metric aggregation, live values or a verified replacement mapping. The calculated-metric lookup returned unrelated entries rather than a reliably filtered match; it did not establish absence of a calculated alternative. Do not generalize these results to other OCMI versions.
