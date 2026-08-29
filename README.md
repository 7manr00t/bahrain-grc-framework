# Bahrain GRC Framework

Mapping the CBB Rulebook (Volume 1, Module OM-5.5 — Cyber Security Risk Management) to **ISO/IEC 27001:2022** and **NIST CSF 2.0**, with a prioritised implementation plan for organisations starting from zero.

Bilingual: English and [العربية](README.ar.md).

---

## Why this exists

Three frameworks, three different jobs:

| Framework | Role | Status |
|---|---|---|
| **CBB OM-5.5** | Tells Bahraini licensees what they **must** do | Mandatory |
| **ISO/IEC 27001:2022** | How you **prove** you do it systematically | Certifiable standard |
| **NIST CSF 2.0** | The map you use to **organise and measure** | Voluntary framework |

Commercial GRC platforms already publish crosswalks between international standards. What this repository adds is the Bahrain-specific anchor — CBB as the starting point rather than an afterthought — and a sequencing opinion: what to build first when you have nothing.

## Status

**Early scaffold.** The structure is in place. Control content is being populated directly from the official CBB Rulebook.

No control text in this repository is written from memory or generated. Every mapped requirement is transcribed from the source and cited with its rulebook reference.

## Repository structure

```
mappings/              Control-by-control crosswalk register
implementation-plan/   Phased roadmap for zero-to-baseline
docs/                  Methodology, scope decisions, sources
```

## Scope

In scope:

- CBB Rulebook Volume 1, Module OM-5.5 (Cyber Security Risk Management)
- Crosswalk to ISO/IEC 27001:2022 clauses and Annex A controls
- Crosswalk to NIST CSF 2.0 Functions, Categories, and Subcategories
- A prioritised implementation sequence for an organisation with no existing cyber practice
- Evidence artefacts expected for each control

Out of scope for now:

- Volumes 2–6 of the Rulebook
- Outsourcing (OM-2) beyond points where it intersects OM-5.5
- Sector-specific guidance outside CBB-licensed entities

## Related work

- [`cbb-rulebook-gap-assessment`](https://github.com/7manr00t) — earlier gap assessment against OM-5.5 using a fictional entity (Al Manara Bank)

## Disclaimer

Independent project by a cybersecurity student. Not affiliated with or endorsed by the Central Bank of Bahrain. Nothing here is regulatory, legal, or compliance advice. Always work from the current official Rulebook.

## Licence

MIT — see [LICENSE](LICENSE).
