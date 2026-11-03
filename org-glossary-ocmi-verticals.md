---
filename: org-glossary-ocmi-verticals.md
title: OCMI Industries and Conversion Candidates
summary: Historical industry mappings requiring version-specific validation; revenue always retains monetary meaning.
layer: org
sandbox: end-to-end
category: org-glossary
source: /workspace/cja-b2c-context.md
original_extracted_at: '2026-07-22T15:36:48+00:00'
revised_at: '2026-11-03'
status: draft-not-published
---

# OCMI industry interpretation

## Applicability
Only for explicitly identified or conversation-confirmed OCMI versions in end-to-end. Do not activate for generic CJA, auto-select OCMI or switch sandboxes. Stop on non-OCMI views. Industry context helps discovery; it does not prove a mapping or require an industry picker for every question.

## Historical candidates, not verified defaults
| Industry | Intended outcome | Historical candidate |
|---|---|---|
| Retail | Purchase | Total Orders, event140 |
| Financial Services | Application completion/account opening | event36, labeled Accounts Created in original source; equivalence needs validation |
| Media & Entertainment | Subscription | event101, Premium Enrollments |
| Telecommunications | Plan activation | event36; intended semantics unverified |
| Travel & Hospitality | Booking | Total Orders, event140; verify booking meaning |
| Education | Enrollment/course completion | event41, Event Registrations; equivalence unverified |
| Government | Service/form completion | event52, Form Completes |
| Healthcare | Appointment/registration | event41 in original mapping; verify instead of assuming this is the appointment metric |

These mappings originate in July 2026 context, not current live validation. An event number or label alone does not prove the intended conversion. Discover the correct component for the selected version and requested outcome.

## Revenue has monetary meaning
Preserve revenue as monetary revenue across every industry. Verify business meaning, currency and coverage using [revenue selection](guardrails-cja-revenue-disambiguation.md). If no appropriate monetary metric is available, state the limitation. Offer non-monetary conversions as clearly labeled alternatives only with user agreement; never silently replace revenue with applications, appointments, enrollments or completions.
