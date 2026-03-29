# Changelog — Babson AI Risk Quiz

All changes to this project are documented here in reverse chronological order.

---

## [1.16.0] — 2026-03-29 UTC
### Added
- **"60-Second Assessment Quiz" section header** — bold Babson Green (#1B4332) centered heading added above the "Your Progress / 0% Complete" progress bar to clearly label the quiz section for visitors

### Infrastructure
- **GitHub Actions auto-deploy workflow** — added `.github/workflows/deploy.yml` so every `git push` to `main` automatically zips and deploys to Netlify via API — no more manual deploys needed
- **GitHub Secrets configured** — `NETLIFY_AUTH_TOKEN` and `NETLIFY_SITE_ID` added to repo secrets for use by the workflow
- **GitHub PAT updated** — new token (`ghp_mkn...`) with `repo + workflow` scopes stored in project memory; old token retired
- **Netlify token saved to memory** — API token and Site ID now persisted for future sessions

### Technical
- Deployment method clarified: site uses **Netlify API zip upload** (not GitHub auto-deploy via Netlify UI link); GitHub Actions now bridges this gap automatically
- First GitHub Actions run: ✅ completed successfully

### Deployed
- GitHub commits: `8c3b685` (header), `bcd5b9b` (GitHub Actions workflow)
- Netlify deploy ID: `69c91b96e174be9f3ee7a4b0` — state: **ready** ✅
- Live at: https://babson-ai-risk-quiz.netlify.app

---

## [1.15.1] — 2026-03-28 UTC
### Fixed
- **"Send the Assessment" blank white tab bug** — removed `window.open('mailto:...')` call that opened a blank browser tab on submit; replaced with fully in-page "Thank you" confirmation message
- **Friend invitation** — now sends invitation email directly via FormSubmit instead of relying on the visitor's local email client
- **Success message** — now shows inline: "✓ Thank you, [Name]! Scott & Peter have been notified, and an invitation has been sent to [friend email]"

### Technical
- Removed `window.open()` call from `sendReferral()` function
- Added second FormSubmit AJAX call to deliver quiz invite link to the referred friend's email
- Success message now uses `innerHTML` and explicit `display: block` toggle for reliable rendering

---

## [1.15.0] — 2026-03-28 UTC
### Changed
- **"Book a 15-Minute Call" button** — mailto link now automatically pre-fills subject as "Requested a 15 minute conversation", adds BCC to smagnacca@babson.edu, and includes the prospect's full name, email, company, and AI Risk Score in the email body

### Technical
- Updated `href` on `.btn-cta` anchor in `buildResults()` template to include `bcc=smagnacca%40babson.edu`, updated `subject` parameter, and restructured `body` to present prospect details clearly

---

## [1.14.0] — 2026-03-24 UTC
### Added
- **Hero subtitle typewriter animation** — "The capability gap between AI-enabled and non-enabled organizations widens every week. Find out exactly where you stand." types out character-by-character at reading speed (~42ms/char) in white on page load
- **Gold pulse on typewriter completion** — when text finishes typing, it pulses bright gold (#E8C96A with glow) then settles back to original white/65% opacity
- **Sequential pill glow animation** — each hero pill button ("4 Questions", "Under 60 Seconds", "Personalized Results", "No Cost") glows and pulses gold in sequence with a 3-second pause between each; sequence loops continuously

### Technical
- Added `@keyframes heroSubGoldPulse` CSS animation for text pulse effect
- Added `@keyframes pillGlowAnim` CSS animation for pill glow/pulse effect
- Added `.hero-sub-pulse` and `.pill-glow` CSS utility classes
- Added IDs `pill-1` through `pill-4` to pill elements
- Added two IIFE JavaScript blocks for typewriter and sequential pill orchestration
- Commit: `bd9f572`

### Deployed
- GitHub push: ✅ ae17396 → bd9f572 (main)
- Netlify deploy ID: `69c33325c9ece6045be35c3e` — state: **ready** ✅
- Live at: https://babson-ai-risk-quiz.netlify.app

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
