# Language Selector, Locale URLs and Fallback Behavior

## Required user experience
- The language control must have an accessible name and convey the current selection.
- When a true equivalent exists, switch to that exact page in the selected language (typesetting remains typesetting, not homepage).
- When missing, show a clear fallback to the available English page or clearly identified alternative. Do **not** silently pretend a translated page exists.
- Switching back to English retains established production English URLs.
- Direct locale deep links, browser history, refresh and new tabs should not depend on a prior cookie.
- Respect explicit selection without forcing IP or Accept-Language redirects.
- If preference persists, ensure it never overrides a directly requested locale URL.
- Preserve service-to-quote context, audience anchors and existing CTA destinations.
- Inspect separate mobile/desktop selector markup to avoid duplicate accessible interactive elements.

## URL structure — illustrative only
English: `https://www.epubtrans.com/typesetting-services`
French **if approved and implemented**: `https://www.epubtrans.com/fr/typesetting-services`
Arabic **if approved and implemented**: `https://www.epubtrans.com/ar/typesetting-services`

These are **proposed**, not verified live destinations. Prefer stable English slugs within a locale prefix initially; translated slugs require a separate approved mapping. Do not add `/en` and redirects just for consistency.

## Acceptance scenarios
| ID | Action | Expected |
|---|---|---|
| SW-01 | Switch typesetting to French (if published) | Equivalent French page and route, full French body |
| SW-02 | Load French URL directly in new private session | French remains visible |
| SW-03 | Reload selected locale | Correct locale and current page persist |
| SW-04 | Back/forward across switch | URLs and selection match |
| SW-05 | Missing locale counterpart | Honest accessible fallback; no false route |
| SW-06 | Switch back to EN | Existing English canonical path |
| SW-07 | Arabic switch and navigation | RTL coherent, Arabic remains |
| SW-08 | Mobile and keyboard picker | Operable, focus handled |
| SW-09 | User arrives at English deep link with stored French preference | No unexpected redirect away from requested page |
| SW-10 | `/services#for-publishers` in another locale | Correct actual counterpart/anchor if available |

Do not introduce a language toggle that changes visible body language on the same canonical URL and then claim independent search-indexable translations.
