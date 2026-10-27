# Metadata, Canonical and hreflang Rules

## Primary rule
Publish `hreflang` **only** for verified, equivalent, approved, crawlable localized URLs. A language selector alone is insufficient.

## For each truly translated and indexable page
1. Localize H1, HTML `<title>`, description, Open Graph text as relevant, and primary body.
2. Set HTML `lang` appropriately and `dir=rtl` for actual Arabic pages.
3. Use one accurate canonical URL for the preferred version **in its own language**, normally self.
4. List only actual page-equivalent alternate URLs in `hreflang`, with full HTTPS URLs.
5. The list must include self and be reciprocal across all variants claimed.
6. Use `x-default` only if it resolves to a genuine suitable fallback (e.g. English or selector page).
7. All alternates must return meaningful 200 content, be canonical and intended for indexing; exclude 404, redirect, noindex, missing and non-equivalent routes.
8. Never output preview/Vercel hostnames in production metadata/sitemap.

## Example (only if these routes are real and translated)
A published French typesetting page's head could include:
```html
<link rel="canonical" href="https://www.epubtrans.com/fr/typesetting-services">
<link rel="alternate" hreflang="en" href="https://www.epubtrans.com/typesetting-services">
<link rel="alternate" hreflang="fr" href="https://www.epubtrans.com/fr/typesetting-services">
<link rel="alternate" hreflang="x-default" href="https://www.epubtrans.com/typesetting-services">
```
On the English page, **its own** canonical must be the English URL. The alternate cluster matches across the two. **Example paths are not confirmed live.**

## Partial coverage
If French homepage exists but French typesetting does not, do **not** point English typesetting hreflang to the French homepage. The group is per equivalent content identity, not per global list.

## When switching is only client-side/UI-only
Keep English canonical and metadata; do not synthesize alternate tags or sitemap pages. Google advises unique URLs for crawlable language versions; a cookie or JS-only switch may not be independently discoverable.

## QA
Check server-rendered HTML and post-hydration DOM for:
- correct, unique title, meta, canonical and hreflang;
- correct content language and no English-only body duplication;
- canonical target and hreflang URLs matching final host, path and indexation;
- no head conflicts across layout/page metadata;
- no canonical to English solely because English is the default.

Use the official Google references in `13_SOURCES.md`.
