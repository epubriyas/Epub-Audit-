# SEO, accessibility, content and regression acceptance checklist

Use PASS / FAIL / BLOCKED / NOT TESTED. A textual instruction or a code diff alone is not evidence of a passed browser/form test.

## A. Heading copy and page intent

- [ ] `/contact-us` rendered H1 is `Contact EPUBTRANS About Publishing & Localization Projects`.
- [ ] `/get-a-quote` rendered H1 is `Request a Quote for Publishing & Content Production Services`.
- [ ] `/industries` rendered H1 is `Digital Publishing & Localization Services by Industry`.
- [ ] Supporting hero paragraphs match `03_PROPOSED_COPY.md`.
- [ ] Required secondary section heading changes are present on all three pages.
- [ ] No other routes' copy changed accidentally.
- [ ] Home, Services, About and service page H1s remain intact.

## B. HTML accessibility / visual

- [ ] One meaningful main H1 on each page as rendered.
- [ ] Logical H2/H3 structure maintained.
- [ ] Headings are selectable text and not visually or accessibly duplicated by animation.
- [ ] Heading layout works at 320px, 375px, 768px and desktop sizes.
- [ ] No overflow, clipped H1, overlapping CTA, screen-reader-only duplicate or broken reduced-motion animation.
- [ ] Non-English locale handling is identified, and actual translations are reviewed before enabling translated variants.

## C. SEO

- [ ] URL paths unchanged.
- [ ] No redirect changes caused by this ticket.
- [ ] Canonicals still point to the final approved production URLs (on production).
- [ ] Staging indexability restrictions remain in place; no accidental production `noindex`.
- [ ] `/get-a-quote` title remains `Request a Project Quote | EPUBTRANS`.
- [ ] `/industries` page metadata is updated if its current generic title is confirmed, and no duplicate title introduced.
- [ ] H1 and title describe the same primary user intent but need not be exact matches.
- [ ] No new inaccurate schema or fabricated company claims.
- [ ] Existing internal links to pages remain valid.

## D. Functional regression

- [ ] `/contact-us`: email, telephone, general form, quote CTA, maps and privacy link still behave as before.
- [ ] `/get-a-quote`: service selector, all four steps, back/forward state, validations, successful submission/confirmation tested where environment permits.
- [ ] `/industries`: all six industry sections, quick navigation links, related service links, FAQ and quote CTA intact.
- [ ] Site navigation and language picker still work.
- [ ] No production deployment asserted unless separately authorized and verified.

## E. Human approval gates

- [ ] Content owner approves final English hero/H2 wording.
- [ ] Service owner approves any material change in claimed scope (this ticket is designed to avoid such changes).
- [ ] Localization owner reviews affected translation keys.
- [ ] Developer signs off responsive and functional tests.

## Suggested implementation result table

| Check | Status | Evidence (URL, screenshot, command/log) | Owner | Date |
|---|---|---|---|---|
| Contact heading and form | NOT TESTED | | | |
| Quote heading and four-step form | NOT TESTED | | | |
| Industries heading and six sections | NOT TESTED | | | |
| Mobile heading layouts | NOT TESTED | | | |
| SEO/canonical/meta | NOT TESTED | | | |
| Locale QA | NOT TESTED | | | |

## Definition of done

All mandatory edits are implemented in the **actual repository**, English copy is approved, rendering is checked, functional workflows still work, and no outstanding critical/major regressions are present. Staging-only completion is not production launch approval.
