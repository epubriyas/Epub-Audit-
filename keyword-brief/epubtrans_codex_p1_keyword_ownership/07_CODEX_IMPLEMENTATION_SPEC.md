# Codex implementation specification — repository-first

## 1. Inspect before changing

The expected stack is Next.js + TypeScript + Tailwind CSS + Payload CMS + PostgreSQL, but repository reality wins. **Do not assume a source-file path, CMS model, route module, or translation system**.

Locate:
- service directory data, actual source of each card (code constants / Payload records / MDX / page blocks);
- page route definitions and trailing-slash policy;
- SEO title/description/canonical/H1 sources;
- service-page component templates and related-link modules;
- localized language variants and link handling;
- prior P1 modifications already applied or pending.

Suggested discovery commands (adjust to repo tools):
```bash
rg -n 'PDF Recreation & Document Preparation|Data Conversion Services|JATS XML|SciELO XML|Multilingual Desktop Publishing' .
rg -n 'data-conversion-services|xml-conversion-services|scielo-xml-markup-services' .
rg -n 'generateMetadata|canonical|alternates|og:title|robots|hreflang' app src pages
```
Do not run commands on a production environment without authorization.

## 2. Build a baseline audit table

For every one of the 16 paths: repo/CMS source, actual H1, title, meta description, first-paragraph service focus, primary CTA, overlap/conflict and suggested edit. Save this table in the Codex report.

If a path or content model differs from the prior staging snapshot, follow the actual implemented source and report the discrepancy. Do not silently substitute a proposed URL.

## 3. Fix shared destination

Implement the default choice in `03_SHARED_DESTINATION_DECISION.md` unless it conflicts with current page structure. Use semantic headings and stable, unique fragment IDs:

```tsx
<section aria-labelledby="pdf-to-word-ocr">
  <h2 id="pdf-to-word-ocr">PDF-to-Word Conversion &amp; OCR</h2>
  {/* existing useful OCR/extraction content */}
</section>
<section aria-labelledby="pdf-recreation">
  <h2 id="pdf-recreation">PDF Recreation &amp; Editable Document Preparation</h2>
  {/* existing useful reconstruction content */}
</section>
```

This is illustrative only: reuse existing components, check for existing IDs and do not assign the same `id` twice in the DOM. `aria-labelledby` correctly refers to the heading ID in this example.

Add `scroll-margin-top` (CSS/Tailwind) where needed for sticky-header offsets. Direct links must work on initial load and client navigation.

**This instruction prohibits adding duplicate `id` values.** The final implementation can put each fragment ID on its heading or enclosing section, not both.

## 4. Resolve cross-page ownership

For each pair in `04_CROSS_PAGE_BOUNDARIES.md`:
- retain page's primary buyer task and unique deliverables;
- remove only lengthy, duplicated *neighboring-service* explanations;
- add one concise related-service context and one meaningful link;
- preserve technical requirements, inputs, outputs, QA and boundaries;
- protect all user-approved content from previous P1 packages.

Avoid indiscriminately applying metadata candidates from `05_PROPOSED_COPY_AND_METADATA.md`. Only replace actual weak/duplicative metas following comparison with current values and SEO review.

## 5. Content source of truth and i18n

If content is stored in Payload CMS, update the appropriate content records/migration/seed files through supported workflows; changing a generated file alone may have no production effect. Log the record identifiers or affected fields (but do not expose credentials or personal data).

Where translations are managed, note whether non-English variants require approved translations. Do not silently translate complex service claims, repurpose English-only slugs for all locales or overwrite curated text.

## 6. Tests

- Use the project-defined lint, typecheck, unit tests, build and route tests.
- If feasible, inspect rendered HTML for H1/title/description/links and page-specific headings.
- Test all fragment routes after hard refresh and client navigation, including on mobile/sticky-header layout.
- Check image/CTA/form preservation, same-domain internal links and no content regression.
- Check indexable service pages have distinct canonicals and are not set to each other automatically.
- Reconcile localized URLs, sitemap and internal navigation behavior.
- Do not mark unavailable tests as passed.

## 7. Expected final response from Codex

Provide:
1. What was modified (file paths and CMS records).
2. Before/after for directory cards and cross-page boundaries.
3. Final keyword owner mapping and any unresolved conflicts.
4. Actual test commands, pass/fail/skipped results, and proof.
5. Outstanding approvals and risks.
6. No implied deployment unless explicitly performed and verified.
