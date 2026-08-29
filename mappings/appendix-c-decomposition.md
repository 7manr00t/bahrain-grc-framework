# Appendix C Decomposed — CBB's Control Guidelines vs NIST CSF 1.1 and 2.0

OM-5.5.3 mandates that the cyber security risk management framework be developed *in accordance with the NIST Cybersecurity Framework, summarised in Appendix C*. That makes Appendix C the load-bearing reference of the whole module — and it carries a structural fact every assessor should know:

> **Appendix C (added July 2021) is built on NIST CSF 1.1** — five Functions (Identify, Protect, Detect, Respond, Recover), 22 categories, ~90 guideline statements. **CSF 2.0 (2024) restructured this**: a sixth Govern (GV) function was created, supply-chain risk moved into it, and several 1.1 categories (PR.IP, PR.MA, PR.PT, DE.DP) were dissolved and redistributed. A licensee following Appendix C literally is following the 1.1 topology.

This file indexes each Appendix C category to its CSF 2.0 home and nearest ISO 27001:2022 territory, so the register (which is CSF 2.0-native) and the Appendix stay reconciled.

## IDENTIFY

| Appendix C category | CSF 2.0 home | ISO 27001:2022 territory | Notes |
|---|---|---|---|
| Asset Management | ID.AM | A.5.9; A.5.12; A.8.1 | Inventories of devices, software, data flows, external systems; criticality-based prioritisation |
| Business Environment | GV.OC | Cl. 4.1–4.2 | Moved to Govern in 2.0 — mission, dependencies, resilience requirements |
| Governance | GV.PO; GV.RR | A.5.1; A.5.31 | Policy, roles, legal/regulatory obligations |
| Risk Assessment | ID.RA | Cl. 6.1; A.5.7 | Vulnerabilities, threat intel, likelihood/impact, prioritised responses |
| Risk Management Strategy | GV.RM | Cl. 6.1 | Risk tolerance expression moved to Govern in 2.0 |
| Third Party Risk Management | GV.SC | A.5.19–A.5.23 | Supply-chain: identify, assess, contract, audit, joint response testing |

## PROTECT

| Appendix C category | CSF 2.0 home | ISO 27001:2022 territory | Notes |
|---|---|---|---|
| Identity Mgmt, Authentication & Access Control | PR.AA | A.5.15–A.5.18; A.8.2; A.8.5; A.7.1–A.7.4 | Includes physical access and MFA commensurate with risk |
| Awareness & Training | PR.AT | A.6.3 | **CBB delta: awareness programme updated at least annually**; secure-coding training for developers |
| Data Security | PR.DS | A.8.24; A.8.12; A.8.6; A.8.31 | **CBB delta: strong encryption explicitly required for critical/confidential data at rest and in transit** |
| Information Protection Processes & Procedures | PR.PS; PR.IR (dissolved PR.IP) | A.8.9; A.8.25; A.8.32; A.8.13; A.5.24; A.5.29; A.8.8; A.6.1 | Baseline config, SDLC, change control, tested backups, tested response/recovery plans, HR security, vuln mgmt plan |
| Maintenance | PR.PS (dissolved PR.MA) | A.7.13 | Logged, tool-controlled, secured remote maintenance |
| Protective Technology | PR.PS; PR.IR (dissolved PR.PT) | A.8.15; A.7.10; A.8.19; A.8.20; A.8.14 | Audit logs, removable media, least functionality, resilience mechanisms |

## DETECT

| Appendix C category | CSF 2.0 home | ISO 27001:2022 territory | Notes |
|---|---|---|---|
| Anomalies & Events | DE.AE | A.8.16 | Baselines, correlation from multiple sensors, alert thresholds |
| Security Continuous Monitoring | DE.CM | A.8.16; A.8.7 | Network, physical, personnel, provider monitoring. **CBB delta: vulnerability scans at least quarterly** (OM-5.5.25 tightens further: monthly internal / weekly external preferred) |
| Detection Processes | dissolved → DE + ID.IM | A.5.2 | Roles, testing and continuous improvement of detection |

## RESPOND

| Appendix C category | CSF 2.0 home | ISO 27001:2022 territory | Notes |
|---|---|---|---|
| Response Planning | RS.MA | A.5.24; A.5.26 | Plan executed during/after incident |
| Communications | RS.CO | A.5.5; A.6.8 | **CBB delta: cross-department incident response exercises at least annually** |
| Analysis | RS.AN | A.5.25–A.5.28 | Investigation, forensics, categorisation, vulnerability disclosure intake |
| Mitigation | RS.MI | A.5.26; A.8.8 | Contain, mitigate, document accepted risks |
| Improvements | → ID.IM in 2.0 | A.5.27 | Lessons learned |

## RECOVER

| Appendix C category | CSF 2.0 home | ISO 27001:2022 territory | Notes |
|---|---|---|---|
| Recovery Planning | RC.RP | A.5.29; A.5.30 | |
| Improvements | → ID.IM in 2.0 | A.5.27 | |
| Communications | RC.CO | A.5.24 | PR management and reputation repair are explicit guideline items |

## Why this matters

1. **Assessment scoping:** a bank saying "we follow Appendix C" is making a CSF 1.1 claim. Mapping its programme to CSF 2.0 (as this register does) surfaces the governance items 1.1 buried inside Identify.
2. **Quantified deltas live here too:** annual awareness refresh, quarterly scans, annual IR exercises, and mandatory strong encryption are Appendix C guideline statements that turn soft ISO objectives into checkable numbers.
3. **A likely future Rulebook change:** if CBB refreshes Appendix C against CSF 2.0, this file is the migration map — track the Rulebook's quarterly updates.

*Summaries are paraphrased from the Rulebook's Appendix C for analysis; the official text is authoritative: https://cbben.thomsonreuters.com/rulebook/appendix-c-cyber-security-control-guidelines*
