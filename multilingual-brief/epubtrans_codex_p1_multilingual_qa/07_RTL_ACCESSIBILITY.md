# RTL, Script Typography and Accessibility QA

## Arabic
For an approved full Arabic route use `<html lang="ar" dir="rtl">`; prefer semantic `dir` and CSS logical properties over arbitrary flipping. Check headers, nav, breadcrumbs, accordions, cards, numbers, dialogs, quote-stepper, success/error states and mobile. Isolate embedded emails, file names and terms like `JATS XML` with appropriate bidirectional semantics (`bdi`, `dir="auto"` as needed).

## Other language scripts
- Hindi/Tamil/Telugu/Bengali: glyph shaping, font fallback, vowel/combining marks, narrow-screen clipping.
- Japanese/Simplified Chinese: punctuation and natural line wrapping.
- German/French/Spanish: longer strings, accent marks, button widths.
- All: no horizontal overflow, labels readable at 200% zoom, meaningful tab order.

## Switcher
Accessible label, clear current selection, keyboard access, focus management, Escape if dialog, and native language options labeled correctly. If desktop/mobile controls coexist in the DOM, avoid duplicate active accessibility nodes.

## Test evidence
| ID | Test |
|---|---|
| R-01 | Arabic route: proper RTL on desktop and 375px |
| R-02 | Arabic quote form: mixed LTR email/URLs, input/errors and submission |
| R-03 | Screen reader announces current language, picker and error messages |
| R-04 | Keyboard-only selection and focus return |
| R-05 | Each locale's `html lang` and `dir` reflect actual page content |
| R-06 | All scripts render without boxes, clipped marks or collisions |
| R-07 | Layout and reading order remain usable at 200% zoom |

Reference: W3C internationalization guidance in `13_SOURCES.md`.
