# Methodology

## Source of truth

All CBB requirements are transcribed from the official Central Bank of Bahrain Rulebook.

| Field | Value |
| --- | --- |
| Rulebook volume | Volume 1 (Conventional Banks) |
| Module | OM-5.5 — Cyber Security Risk Management |
| Version consulted | *TODO — record version identifier* |
| Date consulted | *TODO — record date* |
| Source URL | *TODO — record URL* |

Re-check this before any release. If the module has been amended, the crosswalk is stale until reviewed.

## Standards referenced

- ISO/IEC 27001:2022 — clauses 4–10 and Annex A (93 controls, four themes)
- NIST CSF 2.0 — six Functions: Govern, Identify, Protect, Detect, Respond, Recover

ISO/IEC 27001 is copyright ISO. Control text is **not** reproduced in this repository. Annex A controls are referenced by identifier only (e.g. `A.8.8`). Anyone using this mapping needs their own licensed copy of the standard.

## Mapping approach

1. Read the CBB paragraph and isolate each distinct obligation within it.
2. Ask what the obligation is actually trying to achieve, not which keywords it contains. Keyword matching produces mappings that fall apart under questioning.
3. Identify the ISO clause or Annex A control that delivers that outcome.
4. Identify the NIST CSF subcategory that describes the same outcome.
5. Grade the mapping: `direct`, `partial`, or `none`.
6. Record the evidence an assessor would expect.

## On mapping strength

`partial` is the most common honest answer. CBB requirements are often more prescriptive than ISO controls — a specific frequency, a specific recipient, a specific timeline — where ISO states an outcome and leaves the method open. Recording these as `direct` overstates coverage and is the failure mode this register is designed to avoid.

`none` is also a legitimate result. Where a CBB requirement has no clean counterpart, that gap is a finding worth surfacing, not an error to paper over.

## Limitations

- Single-author work with no independent review.
- Mapping judgements are interpretive. Two competent practitioners will disagree on some rows.
- Nothing here has been validated against a live regulatory examination.
- The implementation plan reflects a defensible ordering, not the only valid one.
