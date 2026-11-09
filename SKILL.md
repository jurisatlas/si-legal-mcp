---
name: si-legal-mcp-skill
description: Official Slovenia (SI) legislation, multi-tier court precedent research, and citation verification skill.
version: 2.0.0
author: JurisAtlas
license: MIT
---

# Slovenia Legal Research & Multi-Tier Case Law Skill (`si-legal-mcp`)

Use this skill whenever the user asks a legal question, drafts a pleading or contract, or researches case law across any judicial instance in **Slovenia (SI)**.

## Verification & Research Rules

1. **Citation Verification:** Never fabricate a statutory provision or case citation. Query `search_legislation`, `search_case_law`, `search_tiered_court_decisions`, or `verify_citation` before citing any authority (e.g., `ECLI:SI:VSRS:2024:II.IPS.10.2024 or PISRS`).
2. **Multi-Tier Judicial Coverage:**
   - **First Instance (Trial / Municipal / District):** Okrajna sodišča (44 Local Courts), Okrožna sodišča (11 District Courts), Delovna sodišča & Upravno sodišče RS
   - **Second Instance (Cantonal / Regional / Appellate):** 4 Višja sodišča (Ljubljana, Maribor, Celje, Koper) & Višje delovno in socialno sodišče
   - **Supreme & Constitutional Instance:** Vrhovno sodišče Republike Slovenije (VSRS) & Ustavno sodišče Republike Slovenije (USRS)
   - **Primary Tiered Database:** Sodna praksa RS (sodnapraksa.si — Višja sodišča, Upravno sodišče & Vrhovno sodišče) (`https://www.sodnapraksa.si`)
