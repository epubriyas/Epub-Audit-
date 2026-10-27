# Evidence, observations, and limitations

## Observed in previous staging audit, 2026-10-26

- `/services` displayed **17 service cards/options** and **16 unique service destinations**.
- Two cards targeted `/data-conversion-services`: `Data Conversion Services` and `PDF Recreation & Document Preparation`.
- Other observed service routes include:
  - `/typesetting-services`
  - `/copyediting-services`
  - `/proofreading-services`
  - `/graphic-design-image-services`
  - `/cover-page-design-services`
  - `/ebook-creation-services`
  - `/scielo-xml-markup-services`
  - `/xml-conversion-services`
  - `/data-conversion-services`
  - `/desktop-publishing-services`
  - `/translation-services`
  - `/elearning-localization-services`
  - `/subtitling-services`
  - `/voiceover-services`
  - `/transcription-services`
  - `/accessibility-services`
- The previous content-deduplication package identified repeated service-scope text within many individual pages. In **this** ticket, focus on *cross-page topic ownership and navigation*, not a second broad deduplication pass.
- The previous audience-pathway package explicitly preserves both cards pending a distinct decision, and routes LSP `PDF Recreation & Editable File Preparation` to `/data-conversion-services`.

## Sources of truth, in order

1. The **repository and connected CMS records** for actual current paths, components, copy and field relationships.
2. Current server-rendered **staging HTML** and local route tests (when accessible from Codex).
3. EPUBTRANS approved company and service scope. Relevant uploads:
   - `EPUBTRANS_02_Service_Catalog_v1.0.docx`
   - `EPUBTRANS_03_SEO_Keyword_Page_Map_v1.0.docx`
   - `EPUBTRANS_05_Website_URL_Inventory_v1.0.docx`
   - `EPUBTRANS_07_Internal_Linking_Map_v1.0.docx`
   - `EPUBTRANS_08_SEO_Research_Validation_Workflow_v1.0.docx`
   - `EPUBTRANS_04_Brand_Voice_Content_Standards_v1.0.docx`
4. Previously generated P1 packages as implementation context, not proof they were actually deployed.

## Status on 2026-10-27

Direct public opens of the Vercel staging pages were unavailable through the available browsing tool. These pages may still be accessible from Codex or from the developer's network; do NOT call the site offline or broken based on this limitation alone. Verify current route mappings from repository/CMS first.

External qualitative examples examined:
- https://www.jatstech.org/services/jats-xml-conversion-services/ — specialist JATS XML vendor landing-page pattern.
- https://www.scielo.org/en/about-scielo/partnerships/companies-certified-for-xml-article-tagging-services/ — authoritative SciELO service-provider terminology.
- https://www.prepress-projects.co.uk/services/digital/ — XML/eBook services grouped but technically distinguished.

These examples **do not validate** EPUBTRANS market share, ranking, conversion rate, supported standards, or certifications.

## Evidence conditions

| Status | Meaning | Codex action |
| --- | --- | --- |
| Observed previous snapshot | Previously checked staging text/link | Confirm against current repo |
| Documented in knowledge base | Approved positioning or working strategic candidate | Follow scope; verify active capabilities |
| Proposed | Copy, anchors, keyword owner, metadata | Implement only if compatible and approved |
| Unknown | Rankings, traffic, GSC, backlink value, actual current form behavior | Do not infer; record for follow-up |

## Do not infer

Do not present the File 03 suggested `/pdf-to-word-ocr/`, `/xml-jats-services/`, `/epub-conversion/`, `/scielo-xml-markup/`, `/multilingual-dtp/` as actual staging or production URLs. Those are examples; the 16 current observed paths are the implementation baseline.
