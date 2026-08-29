# Rationale — OM-5.5.18: The Preventive Technology Stack

OM-5.5.18 is the second **composite Rule** in OM-5.5: a single paragraph mandating a *minimum* preventive technology stack of eleven items. The register shows it as one row with a control range; this doc maps each mandated technology to its closest ISO 27001:2022 control(s) and NIST CSF 2.0 category, with the reasoning — including where no clean ISO equivalent exists.

| # | CBB-mandated technology | ISO 27001:2022 | NIST CSF 2.0 | Rationale / deltas |
|---|---|---|---|---|
| a | EPP / EDR incl. anti-virus & anti-malware | A.8.7; A.8.1 | PR.PS; DE.CM | A.8.7 is the malware-protection control; EDR's telemetry side also serves Detect — a control that spans two CSF functions |
| b | Data leakage prevention (DLP) | A.8.12 | PR.DS | Exact match — A.8.12 is new in the 2022 revision |
| c | Firewalls, network segmentation, WAF, ACLs | A.8.20–A.8.22 | PR.IR | Networks security, security of network services, segregation of networks |
| d | Security testing in development and post-deployment | A.8.29 | ID.RA; PR.PS | Testing in dev/acceptance; post-deploy testing feeds vulnerability identification |
| e | Privileged Access Management (PAM) | A.8.2; A.8.18 | PR.AA | Privileged access rights + privileged utility programs |
| f | Secure email gateway | A.8.7; A.5.14 | PR.PS | **No dedicated ISO control for email security exists** — nearest fit is malware protection + information transfer. A real gap worth naming in any gap assessment |
| g | Secure web gateway | A.8.23 | PR.PS | A.8.23 (web filtering) is effectively this control — one of the tightest matches in the module |
| h | Application whitelisting | A.8.19 | PR.PS | Governs what software may be installed/active. *Not* A.8.18, which covers privileged utilities, not the allow-list itself |
| i | MDM / BYOD security policies | A.8.1; A.6.7 | PR.AA; PR.PS | User endpoint devices + remote working; BYOD sits at the seam of the two |
| j | Network Access Control (NAC) | A.8.20; A.8.21 | PR.AA; PR.IR | Port-level admission control — ISO treats it inside network security rather than as a standalone control |
| k | Identity & Access Management (IAM) | A.5.15; A.5.16; A.5.18; A.8.5 | PR.AA | Access control, identity management, access rights, secure authentication |

## Observations that matter for gap work

1. **CBB regulates at product-category level; ISO regulates at objective level.** ISO never says "deploy a WAF"; it says protect networks. CBB names the technology class. Practical consequence: an ISO-certified bank can still be non-compliant with OM-5.5.18 if a named category (e.g. NAC) is absent — certification is not a safe harbour.
2. **Two items lack clean ISO homes** — secure email gateway (f) and NAC (j) are composites of broader controls. These are the rows where an assessor must test the technology directly rather than inherit assurance from an ISO audit.
3. **OM-5.5.19 (SPF/DKIM/DMARC) and OM-5.5.21 (unified email domain)** extend item (f) into requirements with no ISO or CSF equivalent at all — they exist to fight regional phishing/spoofing fraud. Treat them as a Bahrain-specific email-integrity control set.
4. **The word "minimum" is load-bearing.** The stack is a floor, not a target architecture; OM-5.5.16 still requires the overall approach to be risk-based and proportionate.
