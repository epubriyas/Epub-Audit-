# Sources, Date and Limits of Verification

**Research date:** 27 October 2026.

## EPUBTRANS staging evidence
Homepage: https://epub-audit.vercel.app/
The readable homepage clearly exposes an English selector and ten additional language options, grouped as four Indian and six global languages. It says “Your choice follows you as you explore.” This establishes UI labels, **not** active language URL coverage, accurate translations, persistence or SEO correctness. Attempts to inspect `/services`, `/robots.txt`, `/sitemap.xml` via the available public retrieval tool returned tool access errors. They are not reported as website defects.

## EPUBTRANS knowledge sources
Company Profile & SEO Positioning (01), Service Catalog (02), SEO Keyword & Page Map (03), Brand Voice & Content Standards (04), Website URL Inventory (05), Internal Linking Map (07), SEO Research & Validation Workflow (08), Technical SEO & Website QA Checklist (11), and Lead Conversion & Enquiry Optimization Playbook (19). These govern B2B audience, service scope, claims, URL preservation, internal links and release gates; they do **not** verify deployed multilingual functionality.

## Official external references
- Google Search Central, Managing multi-regional and multilingual sites:
  https://developers.google.com/search/docs/specialty/international/managing-multi-regional-sites
- Google Search Central, Tell Google about localized versions:
  https://developers.google.com/search/docs/specialty/international/localized-versions
- Google Search Central, Canonical URL guidance:
  https://developers.google.com/search/docs/crawling-indexing/consolidate-duplicate-urls
- Next.js, `generateMetadata`, `alternates.languages` and `metadataBase`:
  https://nextjs.org/docs/app/api-reference/functions/generate-metadata
- W3C, Structural markup and right-to-left text:
  https://www.w3.org/International/questions/qa-html-dir.en.html
- W3C, Internationalization checker:
  https://www.w3.org/International/quicktips/doc/checker

## Interpretation
Google recommends separate URLs for language versions and appropriate reciprocal hreflang annotations. It does not use `lang` alone to detect indexed language; still set `lang` for accessibility and correct document semantics. Do not present unverified page variants, translated content coverage, metrics, test passes or rankings as facts.
