# Implementation plan: zero to baseline

A gap assessment tells an organisation what is missing. It does not tell them what to do on Monday. This section is the sequencing opinion — the part a crosswalk alone cannot give you.

The ordering assumes an organisation with no formal cyber practice and finite budget. Each phase produces artefacts that the next phase depends on.

---

## Phase 0 — Mandate

Without this, everything below stalls at the first budget conversation.

- Board-approved information security policy
- Named accountable owner for cyber risk at senior-management level
- Defined scope: which entities, systems, and locations
- Reporting line and escalation path to the board

**Exit criterion:** someone senior is accountable in writing, and there is a policy they signed.

---

## Phase 1 — Know what you have

You cannot protect, or risk-assess, an estate you have not enumerated.

- Asset inventory: systems, data stores, third parties
- Data classification scheme, applied to the inventory
- Risk assessment methodology, documented before the first assessment is run
- Initial risk register with owners and treatment decisions

**Exit criterion:** a risk register a regulator could read.

---

## Phase 2 — Baseline controls

The controls that reduce the most risk per unit of effort. Deliberately unglamorous.

- Identity: MFA, joiner/mover/leaver process, privileged access separation, access reviews
- Patch and vulnerability management with defined remediation SLAs
- Backup and tested restore
- Logging and centralised log retention
- Security awareness training with completion tracking

**Exit criterion:** each control has a named owner and evidence it is running, not just a policy saying it should.

---

## Phase 3 — Detect and respond

- Incident response plan with defined severity levels
- CBB notification triggers and timelines built into the plan — verify current requirements
- Contact tree and out-of-hours arrangements
- At least one tabletop exercise, documented

**Exit criterion:** the plan has been rehearsed, not only written.

---

## Phase 4 — Assurance

This is where regulatory testing obligations land. Doing it earlier tests controls that do not exist yet.

- Penetration testing at the frequency the Rulebook requires — confirm the current paragraph and cadence before committing to a schedule
- Independent review or internal audit of the control set
- Management review, with findings feeding back into the risk register
- Metrics: what gets reported to the board, and how often

**Exit criterion:** the cycle closes — findings change the register, and the register changes the plan.

---

## A note on ordering

Organisations under regulatory pressure often start at Phase 4, because testing is the visible obligation. Commissioning a penetration test against an estate with no asset inventory and no patching process produces a long report and no improvement. The sequence above exists to avoid that.
