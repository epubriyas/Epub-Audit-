# Cross-page content boundaries and anti-cannibalization rules

**Purpose:** Make each service page useful for its own buyer task. Overlap in terminology is natural; harmful duplication is when multiple URLs give substantially the same answer to the same service search.

| Pair / group | Owner A: page and unique scope | Owner B: page and unique scope | Remove or downgrade from neighboring page | Helpful cross-link |
| --- | --- | --- | --- | --- |
| JATS vs SciELO XML | `/xml-conversion-services`: JATS tag sets, XML preparation, general journal XML schemas, conversion inputs/outputs | `/scielo-xml-markup-services`: SciELO Publishing Schema, collection/journal instructions, specialized validation requirements | Remove long general JATS explainer from SciELO; remove full SciELO procedure from generic JATS; keep 2–3 sentence distinction | "Need SciELO-specific markup?" and "For general JATS XML projects" |
| PDF-to-Word vs DTP | `/data-conversion-services`: OCR, source extraction, editable target format, PDF reconstruction | `/desktop-publishing-services`: multilingual/post-translation layout adaptation, fonts, text expansion, target-language composition | Do not make DTP page a full OCR service; do not make conversion page a multilingual layout service | "Post-translation DTP" ↔ "Prepare an editable source from PDF" |
| Publisher typesetting vs multilingual DTP | `/typesetting-services`: book/journal composition, publication proofs, tables, equations, house styles | `/desktop-publishing-services`: localization production, target-script/RTL and text expansion within existing layouts | Remove general book/journal typesetting keyword focus from DTP intro and general localization language as core focus of typesetting | "Typesetting for publishers" ↔ "Multilingual DTP for localization teams" |
| EPUB creation vs accessibility | `/ebook-creation-services`: reflowable/fixed-layout EPUB creation/conversion, EPUB packaging | `/accessibility-services`: format-specific remediation, reading order, tagging, accessibility QA scopes | Do not put full accessibility remediation workflow on EPUB conversion page; do not turn accessibility page into generic EPUB creation | "EPUB conversion" ↔ "Accessible EPUB and document remediation" |
| Copyediting vs proofreading | `/copyediting-services`: style, language consistency and editing before layout according to brief | `/proofreading-services`: errors in text or proofs at the agreed final stage | Do not describe both pages as the same editorial review; distinguish file/state at intake and what is NOT included | "Copyediting before typesetting" ↔ "Proofreading of final text/proofs" |
| Graphics/image vs cover design | `/graphic-design-image-services`: figures, illustrations, artwork recreation, image production | `/cover-page-design-services`: book/publication cover concept/layout, spine/back/front file preparation if currently offered | Graphic design page should mention covers only as related service; cover page should not list all figure-cleanup services as its main offer | "Cover design" ↔ "Figure & image preparation" |
| Translation vs DTP | `/translation-services`: text-language translation work only if actively sold | `/desktop-publishing-services`: layout of translated content supplied by a client/LSP | DTP must not imply translation included; translation must not market post-translation layout as the core translation product | "Need post-translation layout?" ↔ "Translation needs" |
| eLearning vs subtitle/voiceover | `/elearning-localization-services`: localized course assets, authoring project files, interactions and functional delivery | `/subtitling-services` and `/voiceover-services`: timed text or recorded media when separately scoped | Avoid repeating end-to-end course localization content on media pages | "Course localization" ↔ "Subtitles/narration as part of a course project" |
| Subtitling vs transcription | `/subtitling-services`: timed on-screen text for media | `/transcription-services`: audio/video speech converted to text, optional timestamps/speakers | Do not promise translated captions from transcription alone; do not make subtitling page a broad transcription sales page | "Transcription" ↔ "Timed subtitles" |
| Voiceover vs subtitling | `/voiceover-services`: narration/recorded speech tracks | `/subtitling-services`: text timing/caption files | Do not use generic "video localization" H1 on either page; explain each deliverable | "Voiceover" ↔ "Subtitling" |
| Directory vs service pages | `/services`: concise service discovery by buyer/category | 16 individual service URLs: deeper commercial/technical answers | Remove directory blocks that reproduce full service pages; avoid a competing "all conversion services" sales essay | Short, descriptive service cards linking directly to owner page |

## Implementation method

For each overlap:
1. Inspect the current H1, SEO title, introduction, first H2, FAQ and related-service block on **both** pages.
2. Record 1) the unique user problem 2) deliverables 3) inputs/dependencies 4) when to use the other service.
3. Keep full technical detail **only** where it supports the owner page's service intent.
4. Replace long off-topic paragraphs with a single useful 1–3 sentence contextual explanation and a link.
5. Do not remove legitimate shared terms (e.g., PDF, metadata, QA, language) merely because they appear elsewhere.
6. Do not invent service availability, certification or validation status.
7. Keep headings natural; one differentiated H1 per page, unique SEO title and metadata, no keyword stuffing.

## Suggested boundary copy (proposed; not blanket replacements)

**JATS page:** "For article markup that must follow the SciELO Publishing Schema, see our SciELO XML markup services. Schema version and collection instructions determine the required workflow."

**SciELO page:** "For broader scholarly XML conversion that does not require SciELO-specific rules, see our JATS XML conversion services."

**Document conversion page:** "If the document has already been translated and now needs target-language layout adjustment, see our multilingual DTP services."

**Multilingual DTP page:** "If the only source is a non-editable or scanned PDF, document conversion or manual recreation may be needed before localization DTP."

**EPUB page:** "Where the brief requires accessibility remediation or testing against specified criteria, discuss our digital accessibility services as a separate or combined scope."

**Accessibility page:** "Need a new reflowable or fixed-layout eBook rather than remediation? See EPUB conversion and eBook creation."

**Typesetting page:** "For layout adaptation of translated files, explore multilingual DTP."

**Graphics page:** "For front, back and spine cover artwork, see our cover page design service where currently offered."

## Decision rule: avoid automatic merging

Two pages can use similar formats but have **different clients, inputs, outputs and acceptance criteria**. Keep them distinct unless both search-intent evidence and page performance show true duplication, and an owner approves a separate migration plan.
