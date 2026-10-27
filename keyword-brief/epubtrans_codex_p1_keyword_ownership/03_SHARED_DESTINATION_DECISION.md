# Shared destination resolution — document conversion

## Confirmed in 2026-10-26 staging snapshot

| Directory label | Destination | User expectation |
| --- | --- | --- |
| Data Conversion Services | `/data-conversion-services` | Convert PDFs or other documents into specified usable formats |
| PDF Recreation & Document Preparation | `/data-conversion-services` | Recreate PDF layout and prepare editable files for further production/translation |

This is **one landing page with two valid entry intents**, not two competing URLs. Codex must confirm labels and links in the current repository before editing.

## Default decision (recommended)

**Keep one indexed `/data-conversion-services` page.** On that page, organize **two distinct, visible, server-rendered sections**:

1. ID `pdf-to-word-ocr`, heading `PDF-to-Word Conversion & OCR`  
   - Source PDFs/scanned documents to editable DOCX, text extraction and assessed cleanup.
   - Buyer decision: editing/reuse vs extraction quality; input scan quality and table complexity.
2. ID `pdf-recreation`, heading `PDF Recreation & Editable Document Preparation`  
   - Reconstruct pages/layout elements for editing, translation or downstream production where feasible.
   - Buyer decision: editability vs visual fidelity; need for source fonts/linked assets and manual recreation.

Proposed card targets:
- `Data Conversion Services` → `/data-conversion-services#pdf-to-word-ocr`
- `PDF Recreation & Document Preparation` → `/data-conversion-services#pdf-recreation`

**Both sections must have substantive content specific to the respective card.** If existing pages already use suitable IDs, prefer the existing stable IDs and document them. Do not add anchors that point to an arbitrary hero or generic paragraph.

### Alternative if both cards are indistinguishable in repository copy

Use **one directory card** labeled `PDF-to-Word, OCR & Document Recreation` targeting `/data-conversion-services`, and adjust category/count/layout accordingly; do this only after SEO/content owner approval and review of earlier audience-pathway requirements. Do not hide a service capability merely to reduce card count.

## Proposed minimal section content

### PDF-to-Word Conversion & OCR

> Convert eligible PDFs and scanned pages into editable Word files or extracted text for publishing, translation and content reuse. Source quality, tables, columns, equations and recognition needs determine how much cleanup or manual reconstruction is required.

### PDF Recreation & Editable Document Preparation

> Recreate document layouts in an agreed editable format when the original source file is unavailable or unsuitable. Tell us whether you need working content for translation, close visual similarity to a reference PDF, or a combination of both; those are distinct production requirements.

## On-page boundaries

- H1 stays a single main service statement, such as `PDF-to-Word & Document Conversion Services`. It **must not** repeat for each card/section.
- Keep one canonical URL for the page itself **without `#fragment`**.
- Neither card should have its own canonical, `<title>`, standalone XML sitemap entry, or duplicate content page.
- Do not create `/pdf-recreation-services` or `/pdf-to-word-services` for this ticket.
- Do not imply OCR guarantees perfect text accuracy, that all PDFs can be recreated exactly, or that every layout is directly CAT-tool-compatible.
- Related LSP use case: link to `/desktop-publishing-services` for post-translation layout adaptation. Related publisher use case: link to `/xml-conversion-services` only when target is XML.

## Codex implementation checkpoints

1. Find both directory records by their **visible label**, not assumed data-file names.
2. Confirm whether the route's content presently has separate OCR and recreation sections.
3. Implement stable `id` attributes on semantic headings/sections; adjust scroll offset for sticky navigation if needed.
4. Update the links, preserving accessible labels and keyboard focus.
5. Recheck search/filter behavior, audience link contexts and locale handling. If filtering hides cards, the deep links must still work independently.
6. Test direct URL entry, hard refresh and client-side navigation with fragments.
7. If the two pages/labels have changed since snapshot, record the actual current state and seek editorial approval before making a materially different restructuring.
