# Repeatable Multilingual Test Matrix

Record date, tested URL, browser, environment, screenshot/log evidence, tester and `PASS / FAIL / BLOCKED / N/A` for every case. Use actual valid locale URLs from repo inventory, not the example routes below.

## Functional
| ID | Scenario | Expected |
|---|---|---|
| F01 | Homepage picker | 11 visible options, accessible labels/current state |
| F02 | Switch on typesetting page | Equivalent translated page **if actually published** |
| F03 | Switch without equivalent page | Transparent fallback, not unrelated or fictional route |
| F04 | Direct-load locale URL without cookie | Correct URL, body, language attributes |
| F05 | Reload, back/forward and new tab | Predictable language and history |
| F06 | Move via services audience pathways | Relevant service/anchor retained where possible |
| F07 | Mobile language picker | Works at narrow widths, no focus trap |
| F08 | Keyboard-only picker | Accessible focus and selected state |
| F09 | Quote form in alternate locale | Accurate labels, validates and submits; service context preserved |
| F10 | Contact form in alternate locale | Valid submission/confirmation and delivery test |
| F11 | Arabic route | `dir=rtl`, no layout/form corruption |
| F12 | Return to English | Existing English canonical path; no unwanted forced redirect |

## Technical SEO
| ID | Scenario | Expected |
|---|---|---|
| S01 | GET declared localized routes | 200 substantive correct language, not just translated header |
| S02 | Inspect source `<html>` | Correct `lang`; `dir` for RTL |
| S03 | Inspect server-rendered `<head>` | Correct localized title, meta description, one canonical |
| S04 | Inspect all alternate links | Real, equivalent, published and indexable URLs |
| S05 | Reciprocity | Each declared version links back and includes itself |
| S06 | Canonical | Self/same-language policy; not all to English |
| S07 | Inspect sitemap | Only published canonical URLs; no preview |
| S08 | Inspect robots and response headers | Preview protected; intended production pages indexable |
| S09 | Test missing locale counterpart | No bogus alternate, no thin body |
| S10 | Crawl English routes | No lost CTA/link/metadata/heading from earlier P1 work |

## Coverage set
`/`, `/services`, `/typesetting-services`, `/desktop-publishing-services`, `/ebook-creation-services`, `/xml-conversion-services`, `/scielo-xml-markup-services`, `/accessibility-services`, `/contact-us`, `/get-a-quote`, actual Industries route and an actual published resource article if localized.

## Optional HTTP checks
```bash
curl -sS -D /tmp/epub_headers.txt -o /tmp/epub_home.html https://epub-audit.vercel.app/
grep -Ei 'canonical|hreflang|description|<html' /tmp/epub_home.html
# Test verified locale URLs only:
# curl -sS -L -D /tmp/locale_headers.txt -o /tmp/locale_body.html "$VERIFIED_LOCALE_URL"
```
HTTP status alone never proves a page is fully translated. Use repo's existing automated tests plus real-browser inspection. If network/browser access unavailable: `BLOCKED`, not `PASS`.
