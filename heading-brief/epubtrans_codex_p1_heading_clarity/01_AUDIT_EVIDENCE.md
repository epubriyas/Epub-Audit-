# Staging audit evidence — abstract headings

**Observed:** 2026-10-26, publicly crawlable rendered text on https://epub-audit.vercel.app  
**Evidence limitation:** This is a content/heading review of publicly retrieved pages, not a complete DOM, mobile screenshot, CMS, page-source or functional test. Codex must inspect actual repo and preview after editing.

| URL | Observed page title (tab/search) | Current visible H1 | Why revision is justified |
|---|---|---|---|
| `/contact-us` | `Contact EPUBTRANS \| Publishing & Content Services` | `Find your way to us.` | Does not name the company or tell visitors the page is for contacting the team. |
| `/get-a-quote` | `Request a Project Quote \| EPUBTRANS` | `A clear brief. A considered next step.` | Attractive as brand copy, but a visitor should immediately see that this is a quote-request form. |
| `/industries` | `Industries \| EPUBTRANS` | `Content support shaped around your industry.` | Describes a concept rather than the types of services and audiences covered by the six industry cards. |
| `/technology` | `Technology \| EPUBTRANS` | `Technology, grounded in production.` | Optional: general phrase; stronger descriptive H1 is possible. |
| `/work` | `Portfolio & Selected Work \| EPUBTRANS` | `Selected publishing and content samples.` | Optional: partly descriptive already, but can identify work-sample categories more clearly. |

## Exact content signals supporting the proposal

### Contact
- Intro currently: `Publishing, localization or a new collaboration. Let’s find the right next step.`
- Content includes email, phone, business partnership contact, a general enquiry form, a project quote CTA and two Chennai office locations.
- Other vague headings include `Your next chapter starts here.`, `Tell us what you have in mind.` and `At home in Chennai. Connected to your team.`
- **Appropriate primary action:** ask a question, contact the team or request a detailed project quote.

### Get a Quote
- Current intro: `Tell us what you need. Share the details you have, and we can clarify the rest.`
- Four visible stages: Service → Project Requirements → Contact Details → Review.
- Existing SEO title is already intent-led: **retain it**.
- Abstract subordinate headings: `Built around your requirements.`, `What do you have in mind?`, `From brief to next steps.`
- **Appropriate primary action:** complete the service enquiry form; allow the visitor to provide partial project information.

### Industries
- Current intro: `Publishing, localization and accessible digital content for specialized industries. Explore the areas we support and the services that may fit your project.`
- Six visible cards/sections:
  1. Publishing & Scholarly Communications
  2. Education & eLearning
  3. Technology & Digital Content
  4. Corporate & Business Communications
  5. Media & Entertainment
  6. Accessibility & Inclusive Content
- Each card includes materials and related service links; preserve those.
- Additional broad H2s include `A clear process for connected content.` and `Practical answers before you begin.`
- **Appropriate primary action:** browse the relevant industry section, then its service destinations, or request a quote.

## Pages deliberately excluded from the mandatory change

- `/` already has `Digital Publishing, Content Transformation & Localization`.
- `/services` already has `Publishing, Content Conversion & Localization Services`.
- `/about-us` already has `About EPUBTRANS`.
- `/resources` already has `Publishing and localization resources`.
- Existing service-specific H1s should be handled by their own service-page content tickets, not overwritten by this ticket.

## Finding classification

Observed strings and page structures above are direct staging observations. The proposed wording and priority decisions in this package are **editorial recommendations**, not measured search-volume/ranking results.
