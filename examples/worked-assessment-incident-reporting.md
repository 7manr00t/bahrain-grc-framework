# Worked Example — Al Manara Bank, Incident Reporting Readiness

The register says *what* to map and the implementation plan says *what order to build in*. Neither shows an assessment actually performed. This is one, end to end, against a fictional entity.

**Scope of this example:** OM-5.5.57–.61 (Reporting to CBB) and its dependencies in .31, .35, .38 and .41.
**Entity:** Al Manara Bank — fictional Bahraini retail bank licensee, ~300 staff, core banking outsourced, in-house IT of nine, no SOC. The same fictional entity used in [`cbb-rulebook-gap-assessment`](https://github.com/7manr00t/cbb-rulebook-gap-assessment).
**Why this section:** it carries the strictest deadline in OM-5.5 — one hour — and it fails quietly. A bank can hold ISO 27001 certification and still miss it.

## 1. Requirements in scope

| Ref | Type | Obligation | Strength | Phase |
|---|---|---|---|---|
| .57 | Rule | Call CBB within **1 hour**; Incident Report Section A within **2 hours** | partial | 4 |
| .58 | Rule | Section B within **10 calendar days** incl. full RCA; **weekly** updates until closed | partial | 4 |
| .59 | Guidance | Submit even if incomplete | direct | 4 |
| .60 | Guidance | Report contents: timeline, discoverer, type, impact, affected systems, IoCs/TTPs, RCA, actions | direct | 4 |
| .61 | Rule | Pentest report retained **5 years**; submitted within **2 months** of test month-end | partial | 4 |

Dependencies: .31 (SIEM), .35 (SOC), .38 (escalation to IR team/management/Board), .41 (incident log).

## 2. Findings

| # | Finding | Refs | Severity | Evidence sought |
|---|---|---|---|---|
| F-01 | No documented trigger definition for "compromises customer information or disrupts critical services" — staff cannot tell which incidents start the 1-hour clock | .57 | **High** | IR plan; incident classification policy |
| F-02 | CBB hotline and incident mailbox not recorded in the IR plan; no out-of-hours contact procedure | .57 | **High** | IR plan contact annex |
| F-03 | No pre-filled Appendix OM-1 templates — Sections A and B would be drafted from scratch under pressure | .57, .58 | **Medium** | Template pack |
| F-04 | Incident log exists as an email thread, not a structured, tamper-evident record | .41, .58 | **Medium** | Incident log sample |
| F-05 | Outsourced core banking contract contains no notification SLA to the bank — the provider could detect an incident and inform Al Manara after its own 1-hour window has expired | .57 + OM-2 | **High** | Outsourcing agreement |
| F-06 | No RCA methodology; nobody named as accountable for the 10-day submission | .58 | **Medium** | RCA procedure; RACI |
| F-07 | Pentest reports held in a shared drive with no retention control against the 5-year rule | .61 | **Low** | Retention schedule |

## 3. Why ISO certification would not have caught most of this

Al Manara could pass an ISO 27001 audit with all seven findings open. A.5.5 requires contact with authorities; it does not know that the authority is the CBB, that the number is a hotline, or that the window is sixty minutes. **This is the practical argument for the whole repository:** certification demonstrates a working management system, not conformance with a specific regulator's clock.

F-05 is the finding that matters most and the one a control-by-control review misses entirely — it lives in the seam between OM-5.5 and OM-2 outsourcing. Regulatory obligations do not stop at the licensee's perimeter.

## 4. Remediation, ordered by risk reduced per unit of effort

| Order | Action | Fixes | Effort | Owner |
|---|---|---|---|---|
| 1 | Add CBB contact block + trigger definition to the IR plan; brief the on-call rota | F-01, F-02 | Hours | Security lead |
| 2 | Pre-fill Appendix OM-1 Sections A and B; store beside the IR plan | F-03 | Days | Security lead |
| 3 | Run a notification drill — stopwatch from detection to simulated call | F-01–F-03 | Days | Security lead |
| 4 | Amend the outsourcing agreement: provider notification within 30 minutes | F-05 | Months | Legal + procurement |
| 5 | Move the incident log to a structured, access-controlled system | F-04 | Weeks | IT |
| 6 | Document RCA methodology; name the accountable owner | F-06 | Weeks | Security lead |
| 7 | Apply a 5-year retention rule to pentest reports | F-07 | Hours | IT |

Items 1–3 cost almost nothing and close both High findings the bank controls directly. Item 4 is slow because it is contractual — which is exactly why it should start on day one rather than after the drill.

## 5. Residual risk statement

After items 1–7, the residual risk is *detection latency*: with no SOC (.35) and no SIEM (.31), Al Manara's one-hour clock starts whenever a human happens to notice. Reporting readiness is necessary but not sufficient — it is Phase 4 work resting on Phase 3 capability the bank has not yet built. **Sequencing matters more than completeness.**

---

*Fictional entity; illustrative findings. Not an assessment of any real licensee, and not regulatory, legal or audit advice.*
