# Page spec — `/get-a-quote`

## Why this needs editing

Current visible H1 `A clear brief. A considered next step.` describes an attitude, not the page task. The existing SEO title is clearer. Use a visible H1 that says the page lets visitors request a production-project quote.

## Search/user intent
- **Primary:** transactional enquiry.
- **Audience:** publishers, academic publishers, LSPs and translation agencies.
- **Primary action:** complete the four-step project enquiry.
- **Keyword theme:** project quote / publishing production quote (not a broad informational resource).

## Exact required edits
1. Replace hero H1 and intro exactly as in `03_PROPOSED_COPY.md`.
2. Rename `Built around your requirements.` → `Share Your Project Requirements`.
3. Rename first-step `What do you have in mind?` → `Choose the Service You Need`.
4. Rename post-form `From brief to next steps.` → `What Happens After You Submit an Enquiry`.
5. Keep metadata title `Request a Project Quote | EPUBTRANS`.
6. Keep the current note that estimates and delivery commitments depend on review.

## Must preserve
- Four steps: `Service`, `Project Requirements`, `Contact Details`, `Review`.
- All service-category options, including `Multiple Services / Not Sure` and `Other`.
- Conditional form state and validation; prevent losing step progress.
- `Continue`, previous-step navigation where implemented, submit, error/success feedback and bot protection.
- Accessible field labels and form heading association.
- Current internal links to Contact and Services.
- No promise of immediate quote turnaround, fixed pricing or a guaranteed schedule.

## Tests
- Keyboard navigation through steps, clear error messages and screen-reader labels.
- Mobile line breaks for the longer H1.
- A complete, authorized test enquiry: record actual result before marking PASS.
- Ensure updates do not leak into unrelated route templates via a shared hero.
