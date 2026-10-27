# Repository Inspection and Conditional Implementation

The planned stack is Next.js, TypeScript, Tailwind CSS, Payload CMS and PostgreSQL. **Inspect actual repository versions and architecture before implementing; do not invent paths.**

## Inspect and document
- Route tree, locale middleware, i18n plugin, language picker components, locale persistence.
- Payload collections/fields and any translation dictionaries; which pages have approved content.
- Metadata (`generateMetadata`, templates, canonical/alternate builders), sitemap and robots output.
- Forms (including multi-step quote), API submission and language-specific messages.
- URL origin variables and preview/production environment handling.
- Existing tests and previous P1 changes.

## Architecture boundary
Use a stable page/content ID linking language equivalents; define availability **per page**, not only per language. Build locale switcher links and SEO alternates from approved published equivalents. Reuse current data models where possible.

Suggested conceptual data:
```ts
type TranslationStatus = 'ready' | 'partial' | 'ui-only' | 'missing';
type LocalizedPage = {
  pageId: string;
  locale: string;
  pathname: string; // actual verified route
  translationStatus: TranslationStatus;
  indexable: boolean;
};
```
Do not create a new schema just because this example exists.

## If Next.js App Router
Use supported page/route metadata (static `metadata` or `generateMetadata`) and `alternates.languages` only for validated locale equivalents; `metadataBase` must resolve to approved production origin when generating production output. Ensure metadata is available to crawlers and not overwritten by shared templates. Reference: https://nextjs.org/docs/app/api-reference/functions/generate-metadata

## Minimum tests
- Unit: missing locale excluded from alternate cluster; canonical points correctly; x-default correct; no stage URLs.
- Integration: direct locale URL responds with correct body, HTML lang/dir and metadata.
- Browser: switcher, back/reload/deep links, mobile, keyboard, quote flow and Arabic.
- Data test: unpublishing a translation removes it from hreflang/sitemap.
- Regression: English URLs and previous P1 service edits unchanged.

**Do not deploy production by default.** If the repository is English-only, implement honest behavior and document the separate editorial task required before search-indexable localization.
