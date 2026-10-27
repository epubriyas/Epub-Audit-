# Acceptance and Release Gates

## Gate A: Inventory and business truth
- [ ] Actual router/CMS locale options and full translated-page availability inventoried.
- [ ] Language picker label accurately reflects available behavior.
- [ ] Any locale route additions and international targeting are explicitly approved.
- [ ] Each indexable locale-page pair has an assigned reviewer/owner.

## Gate B: Language UX
- [ ] Eleven selector options inspected; all relevant options function as intended.
- [ ] Existing English paths intact; deep link/refresh/history/fallback work.
- [ ] Desktop, mobile, keyboard and screen reader flow works.
- [ ] Contact/quote forms preserve context, submission and success/error handling.

## Gate C: Translation
- [ ] All indexable localized pages have substantive reviewed translations.
- [ ] B2B and publishing terminology correct; no unapproved company claims.
- [ ] H1/body/CTA/forms/metadata are consistent and localized.
- [ ] Arabic RTL and remaining scripts tested; no clipping or misplaced direction.

## Gate D: Search-engine signals
- [ ] Each published locale has an accurate canonical and own-language metadata.
- [ ] `hreflang` only to actual equivalent published indexable pages, reciprocal/self references.
- [ ] No broken, redirected, staging, noindex or unrelated alternate target.
- [ ] Sitemap contains canonical, approved URLs only.
- [ ] Production indexation and staging protection actually tested.

## Gate E: Regression and release
- [ ] Prior P1 content and navigation edits untouched unless an approved dependency required changes.
- [ ] English service-page keyword ownership and intent remain clear.
- [ ] Build/test results captured; browser network evidence for forms.
- [ ] Known gaps have severity, owner and block/ship decision.
- [ ] Rollback instructions documented; no auto deployment.

**Required output:** actual page×locale inventory, changes by file, test results with artifacts, blocked translation reviews, requested management decisions and verdict.

Verdict: `PASS_FOR_APPROVED_LOCALES` / `PARTIAL_PASS_WITH_BLOCKERS` / `BLOCKED` / `FAIL`. An English-only site may pass an accurate language-UX release while **not** passing multilingual SEO/indexation readiness.
