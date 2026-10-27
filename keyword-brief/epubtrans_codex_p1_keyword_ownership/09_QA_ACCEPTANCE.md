# P1 — keyword ownership and shared destination QA

**Testing labels:** PASS (with evidence), FAIL, BLOCKED, NOT RUN, NOT APPLICABLE. Instructions are not proof.

## A. Route and card checks
- [ ] Actual repo/CMS service inventory recorded with all current paths and service options.
- [ ] Both historical conversion-card labels located, or changes since previous snapshot recorded.
- [ ] One owner URL for general PDF-to-Word/OCR/recreation (`/data-conversion-services`).
- [ ] If two conversion cards remain, both have specific, meaningful labels and point to distinct **working fragments**.
- [ ] Fragment IDs exist only once in rendered DOM, are semantic, and work on direct load, refresh and client-side navigation.
- [ ] Sticky header does not obscure targeted heading; keyboard users can reach it.
- [ ] Service directory search/filter still works and every card has a valid link.
- [ ] Publisher/LSP pathway anchors and service links from previous P1 package still work.

## B. Keyword and content boundaries
- [ ] All current service URLs have one recorded primary keyword theme and one dominant buyer task.
- [ ] `/xml-conversion-services` primarily addresses JATS XML; SciELO-specific instructions remain on `/scielo-xml-markup-services`.
- [ ] `/data-conversion-services` remains about editable conversion/recreation; `/desktop-publishing-services` about post-translation layout.
- [ ] `/typesetting-services` owns publisher book/journal composition distinct from LSP DTP.
- [ ] `/ebook-creation-services` owns EPUB creation/conversion distinct from `/accessibility-services` remediation.
- [ ] Copyediting vs proofreading, graphic design vs cover design, eLearning vs media, and media subservices have differentiated use cases.
- [ ] Useful inputs, outputs, technical QA, scope boundaries and FAQs remain intact.
- [ ] No invented service, certification, standard, language, software-version, turnaround or outcome claims.

## C. On-page and technical SEO
- [ ] One unique visible H1 per service URL; metadata titles/descriptions reviewed for duplicates.
- [ ] Existing service URL paths unchanged; no newly invented indexable pages.
- [ ] Canonicals point to each page's approved production URL; none points to staging/fragment/another distinct service.
- [ ] No erroneous 301/noindex/robots/sitemap changes.
- [ ] Internal links use verified paths and do not lead through avoidable redirects.
- [ ] Structured data, breadcrumb labels, Open Graph titles and metadata still match page purpose where applicable.
- [ ] Pages and link destinations remain available in meaningful server-rendered HTML.
- [ ] Locale/i18n variants handled or explicitly flagged for translation/approval.

## D. Functional regression
- [ ] Contact/quote CTAs and forms unchanged and functional (test actual submit only in authorized test environment).
- [ ] Desktop/mobile visual layouts, category cards, navigation and accessible focus verified.
- [ ] Previous service-deduplication and intent-led-heading P1 updates preserved.
- [ ] Project lint/typecheck/build/tests run and outcomes documented.
- [ ] Any blocked test is marked BLOCKED or NOT RUN, not PASS.

## Definition of done

A complete **before/after ownership table**, edited file list, actual test results, and open approvals are documented. Exactly one primary owner per service intent; conversion cards route to meaningful parts of one established page without a new URL; adjacent services remain clearly different in their H1, intro, scope and cross-links.
