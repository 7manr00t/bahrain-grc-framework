# Sources & Mapping Conventions

## Primary regulatory source

- **CBB Rulebook, Volume 1 (Conventional Banks), Module OM (Operational Risk Management), Section OM-5.5 — Cyber Security Risk Management.**
  - Official text: https://cbben.thomsonreuters.com/rulebook/om-55-cyber-security-risk-management
  - Section introduced January 2020, substantially expanded July 2021; individual paragraphs amended through May 2026 (amendment dates are recorded per paragraph in the Rulebook and noted in the register where they affect interpretation).
  - Coverage: OM-5.5.1 – OM-5.5.61 plus OM-5.5.21A (62 paragraphs), and Appendix C (Cyber Security Control Guidelines).
- The near-identical section for Islamic banks lives in **Volume 2, Module OM**. This register cites Volume 1 paragraph numbers; Volume 2 deltas are out of scope for v1.

## Reference frameworks

- **ISO/IEC 27001:2022** — cited by management-system clause ("Cl. 4–10") and Annex A control ID ("A.x.y"). Control IDs and short titles only; the standard's text is copyrighted and is not reproduced anywhere in this repository.
- **NIST Cybersecurity Framework 2.0** — cited at Function.Category level (e.g. `GV.PO`, `DE.CM`). Mapping at category level is deliberate: it stays accurate across CSF 2.0 subcategory revisions and avoids false precision.
- OM-5.5.3 mandates that the licensee's framework be developed *in accordance with the NIST Cybersecurity Framework* — which is the regulatory basis for this crosswalk's existence.

## Register conventions (`mappings/om-5-5-crosswalk.csv`)

| Column | Meaning |
|---|---|
| `Type` | `Rule` = binding requirement (bold text in the Rulebook, "must"). `Guidance` = expectation ("should"/"may"). |
| `Requirement_Summary_EN/AR` | Paraphrased summaries for navigation — **not** substitutes for the legal text. Arabic is Modern Standard Arabic. Always verify against the Rulebook before relying on a row. |
| `ISO_27001_2022` | Closest ISO clause(s)/control(s). Semicolon-separated. A range (e.g. `A.5.15–A.5.18`) means the CBB paragraph spans the whole control set. |
| `NIST_CSF_2_0` | CSF 2.0 categories the paragraph exercises. |
| `Mapping_Notes` | Rationale, composite-rule flags, and **CBB-specific deltas** — places where the CBB requirement is stricter or broader than ISO/NIST (fixed frequencies, retention periods, reporting SLAs, mandatory insurance). |

## Mapping philosophy

1. **Regulator → standard → framework.** CBB OM-5.5 tells Bahraini banks *what they must do*; ISO 27001 is *how they prove they do it systematically*; NIST CSF is *the map used to organise and measure it*.
2. **Best-fit, not exhaustive.** Each row cites the controls a practitioner would test first, not every control with a tangential connection.
3. **Deltas are the product.** Commercial GRC platforms already sell generic crosswalks. The value here is the Bahrain-specific layer: which CBB requirements exceed the international baselines, and by how much.
4. **No reproduction of standards.** ISO text never appears in this repo; CBB Rulebook text is publicly published by the regulator and is referenced by paragraph number with paraphrased summaries.

## Known limitations (v1)

- Mappings are the author's analysis, produced with AI assistance and under review — not legal or audit advice.
- Appendix C (Cyber Security Control Guidelines) is not yet decomposed into the register.
- Per-domain expansion of the composite rules (OM-5.5.15's eleven policy domains, OM-5.5.18's preventive stack) is planned under `mappings/rationale/`.
