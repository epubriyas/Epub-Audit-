# Locale Inventory and Release Decisions

## Selector options, proposed normalized language tags
| Option | Tag to verify | Direction | Note |
|---|---|---|---|
| English | `en` | LTR | Keep existing English root URLs |
| Hindi | `hi` | LTR | Reviewer required |
| Tamil | `ta` | LTR | Reviewer required |
| Telugu | `te` | LTR | Reviewer required |
| Bengali | `bn` | LTR | Reviewer required |
| French | `fr` | LTR | Reviewer required |
| Spanish | `es` | LTR | Reviewer required |
| German | `de` | LTR | Reviewer required |
| Arabic | `ar` | RTL | Full directionality QA |
| Simplified Chinese | `zh-Hans` | LTR | Proposed script tag; confirm actual app convention |
| Japanese | `ja` | LTR | Reviewer required |

No country/region targeting is inferred. Choose region tags only when content really targets a specific region. `zh-Hans` is a recommendation for Simplified Chinese, not proof of the deployed code.

## Status
- `READY_FULL_TRANSLATION`: Full substantive body, navigation, relevant forms, title/meta and accessibility strings translated and approved.
- `PARTIAL_TRANSLATION`: Some core copy not translated.
- `UI_ONLY`: Menu/template translated, body English.
- `MISSING`: No localized version.
- `NOT_TESTED`: No verifiable evidence.

Only `READY_FULL_TRANSLATION` is eligible for locale SEO publication.

## Data required per page×locale
`contentId | English path | locale | verified locale URL | status | body language | localized H1/title/description | canonical | hreflang equivalents | indexability | reviewed by | evidence link | decision`.

Audit `/`, `/services`, `/typesetting-services`, `/desktop-publishing-services`, `/ebook-creation-services`, `/xml-conversion-services`, `/scielo-xml-markup-services`, `/accessibility-services`, `/contact-us`, `/get-a-quote`, actual Industries path, and one resource article if localized.

**Never assume every service has a counterpart in all eleven languages.** No locale-page URL may be emitted solely from the global menu list.
