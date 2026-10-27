# EPUBTRANS — P1 Codex task: Shared destinations and keyword ownership

**Priority:** P1 — High  
**Ticket:** `P1-SERVICE-INTENT-OWNERSHIP`  
**Date:** 2026-10-27  
**Status:** Implementation instructions; NOT applied to the website.

## Goal

Make every active service URL the clear owner of one commercially meaningful search intent, prevent overlapping service descriptions from obscuring page purpose, and fix ambiguous service-directory cards where different service options share a destination.

This is an *editing and link-routing* task, **not** authorization to create, delete, merge, redirect, or canonicalize entire pages.

## Evidence / limitations

- Prior staging review on **2026-10-26** documented 17 options in the `/services` directory leading to **16 distinct service paths**. `Data Conversion Services` and `PDF Recreation & Document Preparation` both target `/data-conversion-services`.
- In the 2026-10-27 review, public browsing could not directly retrieve the current Vercel staging pages. **Treat the prior snapshot as provisional; validate against the actual repository/CMS before edits.**
- EPUBTRANS knowledge-base Files 02, 03, 05, 07 and 08 supply scope, keyword candidates, URL policy and internal-link policy. Their proposed slugs are **not proof of published routes**.
- Keyword mappings are **qualitative hypotheses**, not measured search demand or ranking data. No Search Console, GA4, commercial keyword metrics, or complete HTTP crawl was available for this task.
- Current generic search results show specialist JATS publishing service intent and SciELO-specific services, supporting the *conceptual distinction* between these page types, not EPUBTRANS rankings or search volume.

## Required work

1. Read `01_EVIDENCE_AND_LIMITATIONS.md` and inventory *actual* routes, services cards, CMS content records, metadata and localized variants.
2. Apply `02_KEYWORD_OWNERSHIP_MATRIX.md` as a **provisional map**. Before implementation, compare against current Search Console / analytics data if available. Note conflicts explicitly.
3. Resolve the shared document-conversion destination following `03_SHARED_DESTINATION_DECISION.md`.
4. Differentiate overlapping service pairs per `04_CROSS_PAGE_BOUNDARIES.md`; make **targeted** edits with `05_PROPOSED_COPY_AND_METADATA.md`, not mass page rewrites.
5. Audit all relevant internal links using `06_INTERNAL_LINK_MATRIX.md`.
6. Follow technical and content restrictions in `07_CODEX_IMPLEMENTATION_SPEC.md` and `08_SEO_GUARDRAILS.md`.
7. Run tests and hand off evidence using `09_QA_ACCEPTANCE.md` and `11_CHANGE_LOG_TEMPLATE.md`.
8. Resolve approval needs listed in `12_RESEARCH_AND_APPROVAL.md`.

## Protected decisions

- **Do not create** `/pdf-recreation-services`, `/pdf-to-word-ocr`, `/xml-jats-services`, `/epub-conversion`, `/multilingual-dtp`, or any other keyword-variant route merely because File 03 suggests it.
- Preserve all **16 observed service URLs**, including `/data-conversion-services`, unless a separate documented migration decision has been approved using real URL, performance, backlink and conversion data.
- Do not set cross-canonicals between *different legitimate services*, e.g., JATS and SciELO, solely because they have XML terminology in common.
- Do not create two near-duplicate landing pages from the two conversion cards.
- Keep distinct publisher and LSP pathways from `epubtrans_codex_p1_audience_pathways`. Keep previous heading and deduplication work.
- No unverified standards, certifications, validation guarantees, current tool versions, media languages, client evidence or results.
- Avoid changes to website design, quote form logic, tracking or global navigation outside the narrow scope unless necessary for functional links.

## Deliverable from Codex

- Inventory: actual page path, CMS source / code source, existing H1/title, primary intent, overlapping pages and final proposed action.
- Changes: full file list, before/after snippets and reason for each.
- QA: test commands and results, links verified, translations handled, regression outcomes, blocked items.
- Approval list: undecided ownerships or capabilities.
- **Never claim deployment, indexing or passing QA without test evidence.**

## Files

1. `01_EVIDENCE_AND_LIMITATIONS.md`
2. `02_KEYWORD_OWNERSHIP_MATRIX.md`
3. `03_SHARED_DESTINATION_DECISION.md`
4. `04_CROSS_PAGE_BOUNDARIES.md`
5. `05_PROPOSED_COPY_AND_METADATA.md`
6. `06_INTERNAL_LINK_MATRIX.md`
7. `07_CODEX_IMPLEMENTATION_SPEC.md`
8. `08_SEO_GUARDRAILS.md`
9. `09_QA_ACCEPTANCE.md`
10. `10_PASTE_INTO_CODEX.md`
11. `11_CHANGE_LOG_TEMPLATE.md`
12. `12_RESEARCH_AND_APPROVAL.md`
