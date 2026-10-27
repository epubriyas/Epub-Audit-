# Page spec — `/contact-us`

## Why this needs editing

The current H1 `Find your way to us.` and section labels such as `Your next chapter starts here.` conceal this page's immediate purpose. The page already contains concrete contact methods, a general enquiry form, a link to the structured quote form and Chennai office information. Make those actions explicit.

## Search/user intent
- **Primary:** branded contact/navigational + project enquiry.
- **Audience:** both publishing organizations and LSPs/translation agencies, as well as potential partners.
- **Primary action:** contact EPUBTRANS. Detailed quotes use `/get-a-quote`.
- **Keyword theme:** contact EPUBTRANS / publishing and localization enquiries. Do not force keywords or create a second service landing page.

## Exact required edits
1. Replace the H1 and hero text exactly as in `03_PROPOSED_COPY.md`.
2. Re-label the project quote H2 `Request a Detailed Project Quote`. Keep the existing body text, list of helpful project details and `Get a Quote` link.
3. Re-label the form H2 `Send a General Enquiry`. Keep the distinction between a general message and a more structured quotation.
4. Re-label location H2 `Our Offices in Chennai`. Keep each address exactly as currently shown unless a business owner has approved corrected address data.
5. Preserve contact methods (email, phone, partnership CTA), form fields and privacy link.
6. Check line wraps and hero legibility across breakpoints; remove any forced line breaks written specifically for the old poetic heading.

## Semantic implementation notes
- Exactly one visible `<h1>` in `<main>`.
- The three labels above remain section headings (typically `<h2>`), with their children in logical hierarchy.
- Preserve accessible name and focus behavior of contact action buttons.
- Do not repurpose `aria-label` content from the old heading or leave stale decorative text in screen reader output.
- If the old heading is split into multiple elements for animation, update or remove animation-specific split strings.

## Acceptance
- H1 clearly says how/why to contact EPUBTRANS.
- General enquiry and detailed quote journeys are distinguishable.
- Email, phone, maps, privacy notice, form and quote links are unchanged and work as before.
- No accidental phone/address edits, invented response time or claims of global office presence.
