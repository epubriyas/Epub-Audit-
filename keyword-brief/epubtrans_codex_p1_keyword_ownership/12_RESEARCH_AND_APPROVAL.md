# Research log, approval questions, and next decisions

## Qualitative research only

**Date:** 2026-10-27  
**Market:** International, English-speaking B2B audiences (specific country/locale search personalization not established).  
**Method:** Review EPUBTRANS working keyword/page maps, past staging audit, and illustrative recent service-page web results.

Examples:
- JATS commercial service page: https://www.jatstech.org/services/jats-xml-conversion-services/
- SciELO official program/service-provider terminology: https://www.scielo.org/en/about-scielo/partnerships/companies-certified-for-xml-article-tagging-services/
- Publisher's XML and EPUB services coexisting under different scopes: https://www.prepress-projects.co.uk/services/digital/

**Observations:** JATS XML and SciELO-specific markup are distinguishable service needs; a single provider may support more than one production format while still explaining each. This does not prove any target phrase's volume, difficulty, CTR, or ranking for EPUBTRANS.

**Not available:** GSC/GA4/CRM, commercial keyword tool metrics, current link graph/backlink data, full current staging crawl. All ownership decisions remain editorially provisional pending these.

## Management/service-owner approvals

1. Does the current `/data-conversion-services` page substantively cover **both** editable PDF-to-Word/OCR and layout recreation, and are both independently marketable offerings?
2. Should the directory retain **two differentiated cards** with anchor links (recommended) or consolidate into one? Card merger would require explicit approval.
3. Is `/translation-services` an active standalone sales priority, or should it stay secondary to LSP production partner positioning? Do not delete/redirect based on priority alone.
4. Are cover design, media services, current tool versions and supported languages all active/current? Confirm before detailed copy changes.
5. Are SciELO service scope and public certification wording approved for current use?
6. Do GSC enquiries or rankings support additional or different primary search terms for any page?

## Developer decisions

- Where are card records stored, and how does updating them affect published/localized site content?
- Are anchor links compatible with client-side routing, scroll restoration, sticky header and site search/filter?
- What is the canonical trailing-slash/domain policy?
- Have the other P1 Codex packages already been implemented? If so, preserve their changes.

## Future page creation — separate proposal only

If evidence later reveals genuinely distinct **commercial search intent**, draft a new-page case with unique buyer job, proof of delivery capability, useful substantial content, live/legacy URL inventory, GSC performance review, and redirect/internal-link implications. Do not create pages automatically from keyword synonyms or every service card.

## Approval workflow

Codex implementation → SEO/content owner checks keyword and intent ownership → service owner verifies technical scope → developer runs QA → management approves material claims/URL changes → controlled deployment.
