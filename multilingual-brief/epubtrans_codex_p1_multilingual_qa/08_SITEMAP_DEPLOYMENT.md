# Sitemap, Staging Protection and Release QA

## Staging / production
- Use HTTP response and deployment checks to verify staging is protected from unwanted indexing; web research fetch errors are **not proof of endpoint failure**.
- Production indexable pages must not inherit staging `noindex`/robots restrictions.
- Production canonical, hreflang, OG URLs and sitemap must never point to `epub-audit.vercel.app`.
- Test both the staging and production environment and record the differences explicitly.

## Sitemap
- Include only existing, published, approved, indexable canonical page URLs returning 200.
- Include locales only where page translations are actually ready. Do not list JS-only language states or query toggles as pages.
- Use one maintained hreflang source of truth; HTML-head annotations are sufficient for standard HTML pages, sitemap alternate annotations are an alternative.
- Validate www/non-www, HTTPS, case and trailing-slash consistency.

## Migration / release
- Keep established English service routes; don't invent `/en` moves or mass redirects.
- New locale route architecture must be approved and documented with migration impacts.
- If any genuinely existing URL changes, use relevant approved permanent redirects and update every internal link, sitemap, canonical and alternate.
- Verify production Search Console property, submit sitemap, inspect sample locale pages after rollout.
- Don't imply traffic results, rankings or indexing approval without Search Console evidence.

## Blocking conditions
- Indexable locale page with untranslated core body.
- Missing/unreciprocated hreflang on actual intended locale clusters.
- Hreflang to a 404, 3xx, noindex, staging or unrelated page.
- Distinct translated pages all canonicalized to English.
- Broken language selector or quote/contact conversions.
- Broken RTL user journey.
- Staging indexable unexpectedly or production blocked.
- Unapproved translation/certification/claim published in any language.

If blocked, limit release scope to ready approved locales rather than generating placeholder pages.
