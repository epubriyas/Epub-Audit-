# EPUBTRANS — P1 Multilingual Website Verification and Remediation
Codex handoff | 27 October 2026 | **Proposed, not implemented**

## Objective
Verify, then fix where evidence supports changes: translations, locale URLs, language selector, persistence, metadata, canonical URLs, `hreflang`, mobile/RTL behavior, accessibility and enquiry flows. Preserve existing English URLs, previous P1 edits and accurate company claims.

Staging: https://epub-audit.vercel.app
Preferred production host (confirm): https://www.epubtrans.com

## Observed scope
The homepage visibly offers English plus 10 choices: Hindi, Tamil, Telugu, Bengali, French, Spanish, German, Arabic, Simplified Chinese and Japanese. Its selector says “Your choice follows you as you explore.” **We did not test switching, persistence, translation coverage, individual locale routes or metadata.** Do not treat language buttons as proof of translated/indexable URLs.

## Mandatory decision gate
1. Inspect actual route structure, localization library, CMS, selector, API, metadata and sitemap; record verified page×locale availability.
2. Classify every locale/page: `READY_FULL_TRANSLATION`, `PARTIAL_TRANSLATION`, `UI_ONLY`, `MISSING`, `NOT_TESTED`.
3. Choose implementation:
   - **A, UI-only / English body:** No new indexable locales or fake `hreflang`; make language-picker behavior honest and functional.
   - **B, verified full translations and stable locale URLs:** Localized body + title/meta/H1; correct URL, canonical, reciprocal `hreflang` and sitemap.
   - **C, mixed coverage:** Only fully translated and approved page/locale pairs may be indexed; other combinations use a disclosed fallback.
4. Do not launch broad locale routes or change indexing policy without content-owner approval. Flag blocked reviews.

## Read in order
`01_EVIDENCE.md`, `02_LOCALE_MATRIX.md`, `03_SWITCHER_ROUTING.md`, `04_TRANSLATION_REVIEW.md`, `05_HREFLANG_CANONICAL.md`, `06_REPOSITORY_IMPLEMENTATION.md`, `07_RTL_ACCESSIBILITY.md`, `08_SITEMAP_DEPLOYMENT.md`, `09_TEST_MATRIX.md`, `10_ACCEPTANCE.md`, `11_CODEX_PROMPT.md`, `12_CHANGE_LOG.md`, `13_SOURCES.md`, `14_LOCALE_QA_TEMPLATE.md`.

## Constraints
- Do not create fictional URLs, add `/en` redirects, force country-specific targeting or auto-publish machine-translated services.
- Do not canonicalize genuinely distinct fully translated pages indiscriminately to English.
- No staging URLs in production canonical/hreflang/sitemap.
- Preserve P1 service deduplication, audience pathways, heading clarity and keyword-ownership changes.
- Preserve forms and quote-service context; no automatic production deployment.
- Label tests `PASS`/`FAIL`/`BLOCKED`; never assume success.

## Codex deliverables
Verified locale-page inventory, file-by-file diff summary, functional and SEO test evidence, language-review blockers, approved implementation branch and rollback note.
