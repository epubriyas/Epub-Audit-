# Provisional service-page keyword ownership matrix

**Type:** Qualitative candidate mapping, **not verified keyword metrics**.  
**Owner:** SEO/content owner, subject to approval of company facts and current search evidence.  
**URL convention:** Preserve observed existing paths; Codex must confirm each in the current code/CMS.

Every row has **one primary intent**; secondary phrases belong to that owner unless a clearly distinct, evidenced buyer task justifies a later page.

| Current URL | Audience / primary intent | Primary keyword theme (candidate) | Secondary cluster / questions | Commercial priority* | Overlap boundary | Research confidence / unresolved question |
| --- | --- | --- | --- | --- | --- | --- |
| `/typesetting-services` | Publishers; typeset books/journals | book and journal typesetting services | book typesetting, academic journal typesetting, page composition, print/digital proofs | High | Not post-translation LSP layout; link DTP when language adaptation is the job | Medium; compare Search Console queries to DTP |
| `/copyediting-services` | Publishers; editorial revision before composition | copyediting services for publishers | academic copyediting, style consistency, manuscript editing scope | Medium | Not last-stage proof correction; link proofreading | Medium; verify editorial scope and distinct demand |
| `/proofreading-services` | Publishers; correction of proofs / final text | proofreading services for publishers | journal proofreading, typeset proof review, final proof corrections | Medium | Not full copyediting/substantive editing | Medium; confirm whether proofreading is independently sold |
| `/graphic-design-image-services` | Publishers; publication artwork/figure services | graphic design and image services for publishing | figure recreation, image editing, chart graphics, illustration preparation | Medium | Cover design has its own page; do not make this page a competing cover-design landing page | Medium-low; verify coverage and enquiries |
| `/cover-page-design-services` | Publishers; publication cover-specific deliverables | book cover design services | book cover layout, print cover artwork, spine/back cover preparation | Medium | Not general image editing/figure recreation | Low-medium; current offer, portfolio proof and audience fit need confirmation |
| `/ebook-creation-services` | Publishers; create/convert EPUB | EPUB conversion services | EPUB3 creation, fixed-layout EPUB, reflowable eBook conversion, accessible EPUB as a scoped variation | High | Not broad document accessibility remediation; link accessibility for specialist compliance work | Medium; validate whether creation vs conversion terminology wins |
| `/xml-conversion-services` | Academic/journal publishers; JATS or general article XML | JATS XML conversion services | scholarly XML tagging, JATS tag sets, journal XML, schema validation where scoped | High | Not SciELO-specific program/schema work | Medium; confirm target tag sets, versions, scope |
| `/scielo-xml-markup-services` | Scholarly publishers; SciELO schema deliverables | SciELO XML markup services | SciELO Publishing Schema, SciELO journal XML, SPS metadata | High (specialist fit) | Not the default page for all JATS XML services | Medium; validate active capability/status wording |
| `/data-conversion-services` | Publishers/LSPs; PDF-to-editable document / reconstruction | PDF to Word and document conversion services | OCR text extraction, scanned PDF to Word, PDF recreation, translation-ready source preparation | High | Not multilingual post-translation DTP, JATS XML production or EPUB publishing | Medium; one page has TWO directory entry intentions |
| `/desktop-publishing-services` | LSPs; multilingual/post-translation layout | multilingual DTP services | post-translation DTP, localized InDesign layout, text expansion, multilingual desktop publishing | High | Not general PDF OCR or publisher book typesetting | Medium; may require audience-focused snippet |
| `/translation-services` | Buyers needing translation text/linguistic work | translation services (capability to confirm) | translation/localization of content, language-pair questions | Review / Medium | Translation itself distinct from multilingual DTP; do not make homepage translation-led | Low; confirm active scope and target B2B customers |
| `/elearning-localization-services` | LSPs / learning teams; localize course assets/projects | eLearning localization services | course localization, Storyline/Rise/Lectora where currently supported, localized course QA | High | Not general subtitling or narration; those may be scoped subservices | Medium; confirm live tool support |
| `/subtitling-services` | LSPs/media producers; timed captions/subtitles | subtitling services | subtitle timing, multilingual subtitling, SRT/VTT where offered | Medium | Not transcription-only or voiceover production | Medium-low; format/language scope approval |
| `/voiceover-services` | LSPs/media producers; recorded speech/narration | voiceover production services | multilingual voiceover, training narration, audio synchronization | Medium | Not subtitling or full dubbing unless verified | Medium-low; delivery mode and claims to confirm |
| `/transcription-services` | LSPs/media producers; speech-to-text | transcription services | audio/video transcription, speaker labeling, timecodes where agreed | Medium | Not translated subtitles or voiceover audio | Medium-low; validate service status and outputs |
| `/accessibility-services` | Publishers/institutions; remediate digital documents | document accessibility remediation services | accessible PDF, EPUB, Word, PowerPoint, tagging, alt-text/reading-order projects | High | Not general EPUB creation or conversion; do not imply formal compliance guarantees | Medium; standards/testing claims must be specific |

\*Priority reflects *provisional business/intent fit*, not search volume, keyword difficulty or rankings.

## Core decisions

- **Exactly one owner** for generic `EPUB conversion`: `/ebook-creation-services`; `accessible EPUB` may be a related scope there while `/accessibility-services` owns remediation/conformance-assessment intent.
- **Exactly one owner** for generic `JATS XML conversion`: `/xml-conversion-services`; `/scielo-xml-markup-services` owns SciELO-specific work only.
- **Exactly one owner** for `PDF-to-Word`, `OCR`, and `PDF recreation`: `/data-conversion-services`, with clearly distinguished sections and optional deep links; no new route.
- **Exactly one owner** for `multilingual DTP` and `post-translation layout`: `/desktop-publishing-services`; typesetting owns publisher page composition.
- `copyediting` and `proofreading` stay separate only while each offers a distinct scoped service and useful unique buyer answers.
- `cover design` vs `graphic/image` remains distinct unless production and performance evidence supports a formally approved consolidation; no automatic redirect.
- The broad `/services` directory is a **service-discovery hub**. It should summarize and link, not repeat full commercial copy or try to outrank each specialist landing page for its primary keyword.
- The `/industries` and `/services#for-publishers` or `#for-localization-providers` pathways are **navigation contexts**, not competitors for the same exact service terms.

## Data needed to finalize ownership

Export GSC page+query data by URL; where available, add country/device, landing-page organic conversions, enquiry quality and representative SERPs for the actual international target markets. Until then label mapping **provisional**.
