# Implementation Plan — From Zero to OM-5.5-Aligned

A prioritised roadmap for an organisation starting with **no formal cyber practices** and needing to reach alignment with CBB OM-5.5 (and, by construction, most of ISO 27001:2022 and NIST CSF 2.0). This is the part a plain crosswalk doesn't give you: sequencing, ownership, and evidence.

Three design rules, learned from why crosswalk projects usually fail:

1. **Every control gets an owner and an evidence artefact** — a mapping without an owner and proof is a spreadsheet, not a programme.
2. **Rules before Guidance** — binding "must" paragraphs are sequenced first; "should" items slot in where dependencies allow.
3. **The plan is maintained, not finished** — a named Framework Owner tracks CBB Rulebook quarterly updates and re-baselines this plan when paragraphs change (OM-5.5.9 was amended as recently as May 2026).

## Phase 0 — Mandate & visibility (weeks 1–4)

Nothing else works without governance and an inventory.

| Action | OM-5.5 | Owner | Evidence |
|---|---|---|---|
| Board resolution: cyber risk ownership, accountability, standing agenda item | .1 | Board | Board minutes |
| Appoint accountable security lead (CISO or equivalent), independent of IT where feasible | .6, .8 | Board | Appointment letter, org chart |
| Asset inventory — hardware, software, data, external systems | .11 | Security lead | Living inventory register |
| Data classification scheme with named data owners | .11, .12 | Security lead + business | Classification policy v1 |

*Small-organisation note: OM-5.5's full governance set (committee, independent function) assumes bank scale. A startup satisfies the intent with one accountable owner and documented Board-level oversight — scale the structure, keep the accountability.*

## Phase 1 — Strategy, policy, risk baseline (months 1–3)

| Action | OM-5.5 | Owner | Evidence |
|---|---|---|---|
| Cyber security strategy (threats, approach, scope incl. third parties) | .13, .14 | Security lead | Approved strategy doc |
| Written policy covering the eleven domains (see rationale doc) with risk tolerance statement | .15 | Security lead | Board/SM-approved policy |
| First threat assessment + risk register with treatment plan | .22–.24 | Security lead | Risk register v1 |
| Vulnerability assessment baseline; patch management process with risk-based SLAs | .25–.27 | IT | VA report, patch SLA doc |

## Phase 2 — Preventive stack (months 3–6)

Sequenced by cost-to-impact for a greenfield environment, not by paragraph order:

1. **Email authentication (SPF, DKIM, DMARC)** — near-zero cost, immediate anti-spoofing value (.19, .21)
2. **IAM foundations + MFA everywhere** (.18k)
3. **EPP/EDR on every endpoint** (.18a)
4. **Network segmentation + firewall baseline** (.18c, .18j)
5. **PAM for admin accounts** (.18e)
6. **Secure email & web gateways** (.18f, .18g)
7. **MDM/BYOD policy and enforcement** (.18i)
8. **DLP, application whitelisting** (.18b, .18h)
9. **Security testing gate in the development pipeline** (.18d)

Evidence per item: deployment record + configuration baseline + coverage metric (e.g. % endpoints under EDR).

## Phase 3 — Detection (months 6–9)

| Action | OM-5.5 | Owner | Evidence |
|---|---|---|---|
| Centralised logging → SIEM; retention target 5 years | .31–.33 | Security lead | SIEM coverage matrix |
| SOC capability — in-house or **outsourced MSSP for small orgs** | .35 | Security lead | SOC/MSSP contract, runbooks |
| Incident scenarios + SIEM use cases; taxonomy and severity model | .36, .37, .42 | SOC | Use-case register |

## Phase 4 — Response, recovery, assurance (months 9–12)

| Action | OM-5.5 | Owner | Evidence |
|---|---|---|---|
| IR playbooks, roles (Incident Owner / Spokesperson / Record Keeper), incident log | .17, .38–.41 | Security lead | Approved playbooks |
| BCP incl. cyber recovery; RTO/RPO defined and tested | .45–.49, .52 | Security lead + business | Test reports |
| Exercise programme: tabletop → simulation → war game | .50 | Security lead | Exercise reports |
| First penetration test cycle (certified external party) | .28 | Security lead | Pentest report + remediation plan |
| Cyber insurance assessment and cover | .53 | CFO/Risk | Policy document |
| Regulator-reporting readiness: 1-hour contact drill, report templates pre-filled | .57–.61 | Security lead | Drill record, template pack |

## Continuous (from Phase 1 onward)

- Training & awareness with effectiveness measurement (.54–.56) — quarterly cadence, annual programme refresh
- Threat intelligence feed (.20); metrics & dwell-time reporting (.44)
- Board reporting pack every meeting (.4); framework re-approval every 3 years (.5)
- **Framework Owner reviews CBB Rulebook quarterly updates and re-baselines this plan**

## What "done" means

Alignment is not a phase gate — it's all Rules operating with owners and current evidence, plus the recurring obligations (twice-yearly pentests, board packs, training cycles) running on schedule. This plan is analysis, not legal or audit advice; validate scope with the regulator or a qualified assessor before relying on it.
