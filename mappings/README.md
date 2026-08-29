# Mapping register

The crosswalk lives in [`om-5-5-crosswalk.csv`](om-5-5-crosswalk.csv). CSV rather than a Markdown table so it stays diffable, sortable, and importable into a spreadsheet or GRC tool. All 62 paragraphs of OM-5.5 (OM-5.5.1–61 plus 21A) are populated.

## Columns

| Column | Meaning |
|---|---|
| `CBB_Ref` | Rulebook paragraph reference, e.g. `OM-5.5.28` |
| `Type` | `Rule` (binding — bold "must" text in the Rulebook) / `Guidance` ("should" / "may") |
| `Section` | The OM-5.5 sub-section the paragraph belongs to |
| `Requirement_Summary_EN` / `Requirement_Summary_AR` | One-sentence paraphrase in English and Modern Standard Arabic — for navigation, never a substitute for the legal text |
| `ISO_27001_2022` | Management-system clause(s) (`Cl. x`) and/or Annex A control(s) (`A.x.y`), semicolon-separated. A range (`A.5.15–A.5.18`) means the paragraph spans the whole control set |
| `NIST_CSF_2_0` | CSF 2.0 Function.Category codes (e.g. `GV.PO`, `DE.CM`) — category level deliberately, to stay accurate across subcategory revisions |
| `Mapping_Strength` | `direct` / `partial` / `none` — honesty grade. `partial` usually means the CBB requirement is *stricter or more prescriptive* than the standard; `none` means no ISO/CSF counterpart exists |
| `Phase` | Which [implementation-plan](../implementation-plan/) phase the requirement lands in (`0`–`4`, or `Cont.` for continuous obligations) |
| `Mapping_Notes` | Rationale, composite-rule flags, and CBB-specific deltas (frequencies, retention periods, reporting SLAs) |

Detailed reasoning lives in [`rationale/`](rationale/) for the two composite Rules, and in [`appendix-c-decomposition.md`](appendix-c-decomposition.md) for Appendix C. Per-control evidence artefacts live with their actions in the [implementation plan](../implementation-plan/).

## Rules for maintaining this register

1. **Transcribe from the source.** Every change starts from the current Rulebook text, never from memory or a secondary summary.
2. **Record the version.** The Rulebook state consulted is recorded in [`docs/methodology.md`](../docs/methodology.md). Regulations change; an undated mapping is worthless.
3. **Summarise, do not copy.** Summaries stay short and in our own words; `CBB_Ref` lets the reader reach the source.
4. **Mark weak mappings honestly.** `partial` and `none` are legitimate answers. A crosswalk with no gaps is a crosswalk nobody checked.
5. **Re-baseline on Rulebook quarterly updates.** When a paragraph is amended (most recently OM-5.5.9, May 2026), its row is re-verified and the change noted.

## Reading the register — three threads worth pulling

- **Filter `Mapping_Strength = partial`** to see everywhere CBB is stricter than ISO/NIST: fixed pentest frequency (.28), 5-year log retention (.33), 1-hour/2-hour incident reporting (.57), named technologies (.18, .31, .35), named certifications (.11).
- **Filter `Mapping_Strength = none`** for the requirements with no international counterpart at all: mandatory cyber insurance (.53) and the CBB email-domain approval process (.21A).
- **Sort by `Phase`** to turn the register into a build order for an organisation starting from zero.
