# Contextual links and directory-label matrix

Use **actual verified repository routes**, not proposed File 03 examples. Preserve the current site route conventions.

## Services directory

| Surface | Preferred label | Destination | Relationship |
| --- | --- | --- | --- |
| Data conversion card (default) | `Data Conversion Services` or clearer `PDF-to-Word Conversion & OCR` | `/data-conversion-services#pdf-to-word-ocr` | One page, OCR/extraction section |
| PDF recreation card (default) | `PDF Recreation & Document Preparation` | `/data-conversion-services#pdf-recreation` | Same page, recreation section |
| EPUB card | `EPUB Conversion & eBook Creation` | `/ebook-creation-services` | Owner of EPUB production |
| XML card | `JATS XML Conversion` | `/xml-conversion-services` | Owner of general JATS XML |
| SciELO card | `SciELO XML Markup` | `/scielo-xml-markup-services` | Owner of SciELO-specific workflows |
| DTP card | `Multilingual Desktop Publishing` | `/desktop-publishing-services` | Owner of post-translation layout |
| Typesetting card | `Book & Journal Typesetting` | `/typesetting-services` | Owner of publisher layout |
| Accessibility card | `Digital Accessibility & Remediation` | `/accessibility-services` | Owner of accessibility remediation |

Avoid making directory-card descriptions long enough to compete with service page introductions.

## Service-to-service contextual linking

| Source | Destination | Suggested natural anchor / context |
| --- | --- | --- |
| JATS XML | SciELO XML | `SciELO XML markup` when specific collection requirements apply |
| SciELO XML | JATS XML | `JATS XML conversion` for non-SciELO scholarly workflows |
| Document conversion | DTP | `post-translation desktop publishing` when formatting translated content |
| DTP | Document conversion | `PDF-to-Word conversion and document recreation` when source is uneditable |
| Typesetting | DTP | `multilingual DTP` for translation-related page adaptation |
| DTP | Typesetting | `book and journal typesetting` for original publisher composition |
| EPUB | Accessibility | `digital accessibility remediation` for distinct standards-focused work |
| Accessibility | EPUB | `EPUB conversion and eBook creation` for creating an eBook |
| Graphic design/image | Cover design | `cover page design` for book covers |
| Cover design | Graphic design/image | `publication artwork and image services` for figures |
| Copyediting | Proofreading | `proofreading services` for final checks |
| Proofreading | Copyediting | `copyediting services` for earlier substantive language/style work |
| eLearning | Subtitling / Voiceover | Only if media services are an approved component and the cross-link is useful |
| Subtitling | Transcription | `transcription services` when a text transcript rather than timed display is needed |
| Voiceover | Subtitling | `subtitling services` when on-screen captions rather than spoken tracks are needed |

## Audience pathway package compatibility

- Keep `/services#for-publishers` and `/services#for-localization-providers` (if implemented) as navigation anchors on the single Services page.
- The previously proposed LSP entry `PDF Recreation & Editable File Preparation` can link directly to `/data-conversion-services#pdf-recreation` after the anchor has been implemented and tested.
- The previous publisher link to general conversion can remain `/data-conversion-services` unless there is a useful subtask to highlight.
- Do not remove publisher/LSP pathway cards, CTAs, or six-category search/filter logic.

## Rules

- Do not make user-facing links to non-existent, draft or future URLs.
- Update service-directory, cards, footer, audience sections, related-services blocks and CMS references consistently.
- If localized routes differ, use the site's i18n/linking conventions rather than hardcoding English paths.
- No generic "click here" anchors and no mass exact-match keyword anchors.
- Every destination must be accessible through crawlable `<a href>` links where appropriate.
- Link targets should not pass through accidental redirects or point to staging from live content.
