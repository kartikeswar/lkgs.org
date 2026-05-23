# LKGS Support Resource — Content & Inclusivity Guide

This file guides Claude when editing or generating content for this website.

## Site Identity

- **Name**: LKGS Support Resource — Smile with Cleft
- **Domain**: www.lkgs.org
- **Purpose**: An open, inclusive support resource for families of children with cleft lip and palate (LKGS / Lippen-Kiefer-Gaumenspalte), hosted in Germany and serving a global audience.
- **Languages**: English (primary), German (secondary)
- **Operator**: Kartikeswar Koppula, Berlin, Germany

## Inclusivity Principles

All content on this site must be welcoming to every family, without exception.

### Family structures
- Welcome all caregivers equally: mothers, fathers, grandparents, foster parents, same-sex parents, single parents, non-binary parents, adoptive families.
- Never assume a two-parent heterosexual household. Use neutral language: "caregivers", "parents and guardians", "your family".
- Do not use gendered defaults. Avoid "the mother" when "the parent" or "the caregiver" works.

### Cultural and ethnic inclusivity
- Do not center any single culture, nationality, or ethnicity.
- Acknowledge that families come from diverse backgrounds; medical experiences, access to care, and emotional contexts vary widely.
- When referencing German-specific resources, also acknowledge international alternatives.

### Language and tone
- Use **person-first language**: "a child with a cleft" — not "a cleft child" or "cleft baby".
- Avoid medicalising or pathologising language that frames cleft as a defect or abnormality beyond what is clinically accurate.
- Never use outdated, stigmatising, or offensive historical terms for cleft conditions.
- Avoid language that implies parents are to blame for the condition.
- Use "cleft lip and palate" or "LKGS" (Lippen-Kiefer-Gaumenspalte) as primary descriptors.
- Keep medical terminology accurate but accessible — explain clinical terms in plain language.

### Emotional tone
- Calm, warm, and non-alarmist. Parents reading this may be in acute distress.
- Hopeful without being unrealistically positive or dismissive of difficulty.
- Avoid toxic positivity ("everything will be perfect!"). Acknowledge real challenges while providing reassurance.
- Never imply a child's life quality will be diminished. Many people with LKGS live full, typical lives.

### Disability and ableism
- Do not frame cleft conditions as inherently limiting or as something to be "fixed" beyond necessary medical care.
- Respect the autonomy and dignity of children and adults with cleft conditions.
- Avoid inspiration-porn framing ("despite their cleft, they achieved…").

## Content Red Lines — Never Include

- Content that discriminates on the basis of race, ethnicity, religion, gender, sexual orientation, disability, socioeconomic status, or family structure.
- Stereotypes about any group of people.
- Suggestions that certain types of families are less capable of caring for a child with LKGS.
- Medical misinformation or unverified health claims.
- Promotion of unproven, pseudoscientific, or potentially harmful treatments.
- Content that shames parents for their child's diagnosis.
- Language that equates a cleft with ugliness or deformity in a stigmatising way.

## Privacy and Legal

- This site must remain GDPR-compliant (see `datenschutz.html`).
- Do not add third-party scripts, analytics, or font CDNs without updating the Content Security Policy and Datenschutzerklärung.
- All fonts must remain self-hosted under `fonts/`.
- The `impressum.html` and `datenschutz.html` pages must remain reachable from every page footer.
- The contact form has been removed. If a form is added in future, update `form-action` and `connect-src` in the CSP meta tag on all three HTML pages, and update section 3.3 of `datenschutz.html`.

## Technical Notes

- Single-file static HTML — no build tooling, no bundler.
- Fonts: Satoshi (body) and Source Serif 4 (headings), both self-hosted in `fonts/`.
- Logo: `images/logo.png` — the "LKGS — Smile with Cleft" illustration.
- Three HTML pages: `index.html`, `impressum.html`, `datenschutz.html`.
- Deployed via GitHub Actions to GitHub Pages at www.lkgs.org.
- CSS and JS are inline in each HTML file (no external stylesheet or script files).
- Dark mode is handled via `[data-theme="dark"]` on `<html>` set by inline JS.
- If you add a new page, copy the `<head>` CSS block (including fonts and CSP meta) and the header/footer from an existing page.
