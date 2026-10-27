# Codex implementation guide — content, components, CMS and i18n

## 1. Inspect the actual repository first

Locate the route sources for:
- `/contact-us`
- `/get-a-quote`
- `/industries`

Search for the exact **old H1 strings** listed in `02_HEADING_DECISION_MATRIX.md`. Inspect the rendering layer (e.g. CMS content, local configuration, TSX or JSON locale resources). Do not assume the route lives at a particular filesystem path.

Write down:
- Source file(s)/CMS fields for each page H1 and intro.
- Whether a shared `<Hero>` / split-text component is used.
- Metadata ownership (route module, layout, CMS schema or SEO helper).
- Whether localization keys exist and whether translated headings would need a separate human localization task.

## 2. Apply only mandatory text changes

Treat `03_PROPOSED_COPY.md` as the single copy source for this ticket; **do not rewrite whole pages**. Keep all nested sections, form logic, CTA destinations and industry links.

Use the text as plain content. If code must split the H1 for visual animation, ensure the concatenated DOM text has natural spaces and punctuation.

## 3. Semantic heading and accessibility rules

- Exactly one meaningful main-content H1 per route (check actual rendered DOM, not just source strings).
- A shared header, language selector, modal or assistant must not introduce additional H1s.
- Keep H2/H3 hierarchy logical. Changing a heading's wording does not authorize changing element depth.
- Heading must remain real selectable text, not image-only text or pseudo-elements.
- If the heading is split across spans, ensure screen readers receive one coherent name.
- Do not use hidden keyword-stuffed headings.
- Preserve `id` anchors referenced by navigation or TOCs; changing visible text must not break fragment targets.

## 4. CSS/responsiveness

Longer, descriptive H1s can wrap to 2–3 lines. Inspect:
- 320px and 375px mobile
- 768px tablet
- a desktop viewport (e.g. 1280px)

Check typography, clipping, overflow, line-height, decorative overlays, animations, reduced-motion behavior, CTA overlap and first-screen legibility. Use fluid text/clamp/responsive layout within existing design system; do not shrink all headings globally or redesign shared components.

## 5. SEO and metadata

- Canonicals: retain `/contact-us`, `/get-a-quote`, `/industries` on the production origin after launch.
- Do not canonicalize any production page to the temporary `epub-audit.vercel.app`.
- `/get-a-quote` SEO title already describes the intent; keep it.
- Improve the `/industries` SEO title and description if the current metadata is still generic.
- Check Open Graph social text as a non-blocking review.
- Preserve redirects, robots, sitemap behavior and route slugs.
- No need to add FAQ structured data or Service schema simply because headings change.

## 6. Language support

The staging site exposes a language picker. Do not substitute English headings into other locales silently or invent machine translations. Use the existing localization system to:
1. update English source strings;
2. enumerate affected translation keys/locales;
3. leave a translation/localization approval TODO for untranslated locales;
4. check language-specific rendering and RTL layout where supported.

## 7. Existing P1 package coordination

The previous `epubtrans_codex_p1_service_dedup` package concerns service-page repetition. The previous `epubtrans_codex_p1_audience_pathways` package concerns audience links and `/services` anchor sections. This ticket is limited to wording and metadata on three different primary pages. If any shared component is affected, inspect and report the overlap before changing it.

## 8. Output requirements for Codex

On completion supply:
- files changed with short summaries;
- old → new heading map;
- metadata changes, if any;
- test commands run and results (not merely proposed);
- screenshot/preview links if produced;
- outstanding translation/approval issues;
- rollback instructions or safe commit reference;
- no claim of successful production deployment unless actually deployed and checked.
