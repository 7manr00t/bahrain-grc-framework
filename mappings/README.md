# Mapping register

The crosswalk lives in [`om-5-5-crosswalk.csv`](om-5-5-crosswalk.csv). CSV rather than a Markdown table so it stays diffable, sortable, and importable into a spreadsheet or GRC tool.

## Columns

| Column | Meaning |
|---|---|
| `cbb_ref` | Rulebook paragraph reference, e.g. `OM-5.5.28` |
| `cbb_requirement` | The requirement, summarised in one sentence. Not a verbatim reproduction of the Rulebook. |
| `obligation` | `mandatory` / `guidance` — whether the paragraph uses binding language |
| `iso_27001_clause` | Management-system clause, e.g. `6.1.2` |
| `iso_27001_annex_a` | Annex A control, e.g. `A.8.8` |
| `nist_csf_subcategory` | e.g. `ID.RA-01` |
| `mapping_strength` | `direct` / `partial` / `none` — be honest; forced mappings are worse than gaps |
| `evidence_artifact` | What an auditor would ask to see |
| `phase` | Which implementation phase this belongs to (0–4) |
| `notes` | Ambiguities, overlaps, judgement calls |

## Rules for populating this register

1. **Transcribe from the source.** Open the current Rulebook and work paragraph by paragraph. Never fill a row from memory or from a secondary summary.
2. **Record the version.** Note the Rulebook version and date consulted in `docs/methodology.md`. Regulations change; an undated mapping is worthless.
3. **Summarise, do not copy.** Keep `cbb_requirement` short and in your own words. Cite `cbb_ref` so the reader can go to the source.
4. **Mark weak mappings honestly.** `partial` and `none` are legitimate answers. A crosswalk with no gaps is a crosswalk nobody checked.
5. **One row per requirement**, not one row per paragraph — some paragraphs carry several distinct obligations.

## Known anchor points

These are starting threads to pull on, not verified content. Confirm each against the current Rulebook before entering it:

- Penetration testing frequency (believed `OM-5.5.28`, twice yearly) — verify the paragraph number and the exact wording, including who must perform the test and what must be reported.
- Incident notification timelines to the CBB.
- Board and senior-management accountability for cyber risk.
- Third-party and outsourcing intersections with OM-2.
