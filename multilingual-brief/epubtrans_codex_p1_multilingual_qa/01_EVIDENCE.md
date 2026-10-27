# Evidence and Risk Register

## Observed, 27 October 2026
On https://epub-audit.vercel.app/ the language modal lists:
- Original: EN English
- Indian: HI हिन्दी, TA தமிழ், TE తెలుగు, BN বাংলা
- Global: FR Français, ES Español, DE Deutsch, AR العربية, ZH 简体中文, JA 日本語
Visible wording: “Your choice follows you as you explore.”

The web-readable homepage output includes language picker markup in more than one layout location. This is **not evidence** that users see duplicate dialogs; check desktop/mobile DOM. The tool could not independently fetch `/services`, `/robots.txt` or `/sitemap.xml`; these are **tool access errors**, not verified endpoint failures.

## Not tested and risks to investigate
| Risk hypothesis | Severity if real | Evidence to collect |
|---|---|---|
| Only navigation translated; body English | High | Per-locale rendered main content |
| Locale choice lost on navigation/reload | Medium | Browser flows |
| No distinct persistent locale URLs | High for multilingual SEO | Actual route inventory |
| English title/meta on translated pages | High | Server head/source |
| Invalid/absent reciprocal hreflang | High where indexed variants exist | Alternate URL graph |
| All locale canonicals point to English | High where translated pages exist | Canonical inspection |
| RTL Arabic form/layout breaks | High | Mobile/desktop Arabic test |
| Quote form fails or service context resets | High | Real test submission |
| Staging indexed / production noindexed | Release blocker | Response headers, GSC |
| Bad language-based automatic redirects | High | Direct cold-session requests |

**Important:** Search-engine guidance supports stable URLs for truly localized pages, but the observed selector alone does not establish that these pages exist.
