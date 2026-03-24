# Changelog — Babson AI Risk Quiz

All changes to this project are documented here in reverse chronological order.

---

## [1.3.0] — 2026-03-24 17:26 UTC
### Changed
- Full visual redesign using official Babson brand colors (forest green + gold)
- Replaced dark/black hero background with Babson green (#1B4332) — brand compliant
- Replaced magenta accents with gold (#C9A84C / #E8C96A) throughout
- Switched display font to Merriweather serif for academic, institutional feel
- Switched body font to Inter for clean professional readability
- Added warm cream (#FAFAF7) page background replacing stark white
- Simplified overall design — removed excessive decorative elements
- Gold gradient progress bar (green → gold)
- Gold "B" logo mark in nav and footer
- Stats bar updated to forest-mid green (#2D6A4F)
- Card borders updated to subtle warm tone (#E4E0D8)

### Deployed
- Live at: https://babson-ai-risk-quiz.netlify.app
- Netlify deploy state: uploaded ✓

---

## [1.2.0] — 2026-03-24 17:10 UTC
### Changed
- Attempted premium redesign with Cormorant Garamond font and elaborate decorative elements
- Reverted per feedback — too complex, not aligned with professional simplicity goal

---

## [1.1.0] — 2026-03-24 17:02 UTC
### Added
- Initial Netlify deployment — site created and pushed live
- Netlify site name: babson-ai-risk-quiz
- Netlify site ID: c316d57c-5c06-433e-873a-5252b2a85840

### Changed
- Converted from downloadable HTML file to live hosted website

---

## [1.0.0] — 2026-03-24 16:45 UTC
### Added
- Initial website build matching Babson College flyer CTA
- 4-question AI readiness quiz with scored answer options
- Progress bar with percentage display
- Back/forward navigation between questions
- Email capture gate (Name, Work Email, Company) before results
- 4 personalized result tiers: Critical / Elevated / Moderate / Low Risk
- Score circle with color-coded risk level badge
- 3 tailored insight bullets per score tier
- CTA block linking to pdennis@babson.edu with pre-filled email
- Responsive mobile layout
- Babson College branding (green + magenta — later revised)
- Hero stats bar: 77%, 56%, 3–5× data points from flyer
- Footer with Babson branding and contact email
- EmailJS placeholder wired in (not yet activated)

---

## Pending / In Progress
- [ ] **Formspree integration** — awaiting endpoint URL from smagnacca@babson.edu
  - Recipients: smagnacca@babson.edu + pdennis@babson.edu
  - Will auto-deploy once endpoint provided
