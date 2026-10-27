# Vercel repository layout repair — 2026-10-27

## Confirmed failure

Project: green-9edc/epub-audit. Connected repository: epubriyas/Epub-Audit-.
Failed deployment: 6rsnmsLaoo9GJALmkqVdcEBMTjmi, commit 91716d3.
Vercel failed in 3 seconds during npm ci: EUSAGE, no package-lock.json.
The commit contains an epubtrans-v2 entry with Git mode 160000 pointing to b36f8f2; it does not contain the application source or package files at the root. No .gitmodules supplies a usable submodule checkout.

## Repair

Restored the application files at the repository root from D:/co/epubtrans-v2, including the completed heading clarity, keyword ownership and multilingual P1 changes and their reports/tests. Removed the broken Git pointer from the index. Preserved existing repository screenshots and brief documents. Kept npm ci / npm run build configuration and matching package-lock.json. No application logic was changed specifically for this repair.

Ignored private environment files, local dependencies, generated build outputs, database backups and private uploads were not copied. No Vercel environment variables, project settings or CMS records were changed. The original application workspace is preserved.

## Validation

- PASS: npm ci --dry-run --ignore-scripts --no-audit --no-fund in the corrected checkout (857 packages resolved). This validates installation planning; it does not execute dependency lifecycle scripts.
- PASS: package.json dependency and devDependency maps match package-lock.json root entries.
- PASS: no Git mode 160000 entries remain in the corrected index.
- PASS: no private .env, .vercel, node_modules or private upload paths staged.
- Previously completed P1 checks: production build, lint, typecheck, 124 integration tests and 8 browser tests passed. See docs/p1-multilingual-implementation.md for evidence and limitations.
- Default git diff --check flags historical whitespace in restored files, including generated migrations; no broad formatting rewrite was performed.

- PASS: fresh npm run build in the source workspace, including TypeScript, static page generation and next-sitemap (exit 0). Build used local environment configuration; production environment remains unverified.
- PASS: SHA-256 comparison confirms all 637 copied application files match that tested workspace.

## Release boundary

No push, redeploy or production setting change has been performed. Pushing this corrected checkout to main will trigger the configured automatic Vercel deployment. Await user approval under the earlier instruction not to deploy automatically. Live Vercel installation/build verification remains pending until that deployment runs. The previous Ready deployment remains available.

