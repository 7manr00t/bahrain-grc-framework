# Rationale — OM-5.5.15: The Eleven Policy Domains

OM-5.5.15 is a **composite Rule**: one paragraph obliges licensees to maintain a Board/senior-management-approved, annually reviewed cyber security policy covering eleven named domains. In the register it appears as a single row (`A.5.1; A.5.37 / GV.PO`), which is correct for the *policy obligation itself* but hides the fact that each domain lands on its own ISO control family. This doc is the expansion.

## Policy-level obligations

| CBB element | ISO 27001:2022 | NIST CSF 2.0 | Rationale |
|---|---|---|---|
| Written policy, approved, reviewed ≥ annually | A.5.1; Cl. 5.2 | GV.PO | A.5.1 requires policy defined, approved and reviewed at planned intervals — CBB fixes the interval at one year |
| Roles, responsibilities, delegated powers | A.5.2; A.5.4 | GV.RR | |
| Cyber risk tolerance statement aligned to business strategy | Cl. 6.1 | GV.RM | ISO expresses this as risk acceptance criteria; CBB requires an explicit written tolerance statement weighing customer impact, downtime, media, penalties and financial loss |

## The eleven domains (OM-5.5.15(d))

| # | Domain | ISO 27001:2022 | NIST CSF 2.0 | Notes |
|---|---|---|---|---|
| a | Asset management (hardware & software) | A.5.9; A.5.10; A.8.1 | ID.AM | Inventory + acceptable use + endpoint devices |
| b | Incident management (detection & response) | A.5.24–A.5.28 | DE.AE; RS.MA | The full ISO incident cluster: planning, assessment, response, learning, evidence |
| c | Vulnerability management | A.8.8 | ID.RA | Operationalised further by OM-5.5.25–.27 |
| d | Configuration management | A.8.9 | PR.PS | |
| e | Access management | A.5.15–A.5.18; A.8.2; A.8.3; A.8.5 | PR.AA | Policy-to-control set: access control policy, identity, authentication info, rights, privileged access |
| f | Third party management | A.5.19–A.5.23 | GV.SC | CSF 2.0 moved supply-chain risk into the Govern function — one of the clearest 1.1→2.0 shifts |
| g | Secure application development | A.8.25–A.8.28; A.8.31 | PR.PS | SDLC, requirements, architecture, secure coding, environment separation |
| h | Secure change management | A.8.32 | PR.PS | |
| i | Cyber training and awareness | A.6.3 | PR.AT | Expanded by OM-5.5.54–.56 |
| j | Cyber resilience (business continuity & disaster planning) | A.5.29; A.5.30 | PR.IR; RC.RP | Expanded by OM-5.5.45–.52 |
| k | Secure network architecture | A.8.20–A.8.22; A.8.27 | PR.IR; PR.PS | Network controls + secure engineering principles |

## Considered and rejected

- **A.8.4 (source code access) under domain (g):** rejected — CBB's wording targets the development *process*, not repository access control; A.8.4 belongs under access management if the licensee scopes it there.
- **Mapping domain (b) to A.6.8 (event reporting):** rejected as primary — A.6.8 is the *employee reporting duty*; the domain is the management process (A.5.24–.28). A.6.8 supports it.
- **Placing domain (f) under ID.RA:** rejected — CSF 1.1 housed supply chain under Identify; CSF 2.0 explicitly relocated it to GV.SC. Mapping to the current home keeps the register 2.0-native.

## How to use this in a gap assessment

Each domain row doubles as an audit question: *does a written, approved policy section exist for this domain, and does a control owner operate it with evidence?* A licensee can be fully "mapped" and still fail OM-5.5.15 if the policy text exists but the annual Board review is missing — the approval cadence is itself the Rule.
