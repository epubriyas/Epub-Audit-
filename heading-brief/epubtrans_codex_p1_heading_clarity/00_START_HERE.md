# EPUBTRANS — P1 Codex task: Replace abstract headings with intent-led headings

**Priority:** P1 — High  
**Task type:** Small, controlled copy and semantic-heading change  
**Audit date:** 2026-10-26  
**Website checked:** https://epub-audit.vercel.app/  
**Status:** Instructions only. No repository changes have been made.

## Objective

Make the main heading and a few important section headings immediately explain what a visitor can do or find on the page. Prioritize **Contact**, **Get a Quote** and **Industries**. Preserve the site's restrained design personality by retaining creative language in secondary copy only when useful.

Do not turn all pages into keyword-heavy templates. The homepage, `/services`, `/about-us`, `/resources` and existing service pages already have generally descriptive H1s and are **out of scope** for mandatory H1 changes.

## Mandatory URLs and H1 updates

1. `/contact-us`: `Find your way to us.` → **`Contact EPUBTRANS About Publishing & Localization Projects`**
2. `/get-a-quote`: `A clear brief. A considered next step.` → **`Request a Quote for Publishing & Content Production Services`**
3. `/industries`: `Content support shaped around your industry.` → **`Digital Publishing & Localization Services by Industry`**

The exact hero introductions and H2 replacements are in `03_PROPOSED_COPY.md` and page briefs `04_`–`06_`.

## Deferred, optional follow-up suggestions (do not change without explicit approval)

- `/technology`: `Technology, grounded in production.` → `Production Technology for Publishing & Localization`
- `/work`: `Selected publishing and content samples.` → `Publishing & Content Transformation Work Samples`

See `07_OPTIONAL_PAGES.md`. These are outside mandatory P1 acceptance.

## Implementation order

1. `01_AUDIT_EVIDENCE.md` — live staging observations, as of audit date.
2. `02_HEADING_DECISION_MATRIX.md` — page priority, exact before/after text, SEO and intent.
3. `03_PROPOSED_COPY.md` — proposed replacement strings; **proposed, not yet approved by management**.
4. `04_CONTACT_PAGE.md`, `05_QUOTE_PAGE.md`, `06_INDUSTRIES_PAGE.md` — page-level specifications.
5. `07_OPTIONAL_PAGES.md` — non-blocking suggestions only.
6. `08_IMPLEMENTATION_GUIDE.md` — repository/CMS, i18n, heading semantics, layout rules.
7. `09_SEO_AND_QA_ACCEPTANCE.md` — tests and acceptance criteria.
8. `10_SOURCES_AND_ASSUMPTIONS.md` — URLs and internal knowledge-base references.
9. `11_PASTE_INTO_CODEX.md` — execution prompt.
10. `12_CHANGE_LOG_TEMPLATE.md` — document actual implementation and results.

## Boundaries

- **No URL/slug changes, new pages, redirects, H1 duplication or broad component redesign.**
- Preserve all contact information, forms, CTA destinations, service relationships and six industry cards.
- Do not inadvertently alter shared hero components across the site.
- Keep the previous `epubtrans_codex_p1_service_dedup` and `epubtrans_codex_p1_audience_pathways` tasks intact.
- Avoid asserting live service support, certifications, standards, country coverage or response-time guarantees beyond approved facts.
- The listed copies are editorial proposals requiring the normal EPUBTRANS review/approval process.
- Do not mark work PASS until tested in the actual repository and preview.
