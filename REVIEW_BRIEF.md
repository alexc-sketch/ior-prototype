# IOR Website Prototype — QA & Review Brief

**To the Reviewing Agent:**
You are a senior UX and brand QA reviewer. Your job is to audit every HTML page in this repository against the criteria below and produce a structured report.

---

## 1. Core References

- **Repository:** `https://github.com/alexc-sketch/ior-prototype`
- **Design System (Canonical):** `IOR_Design_System.html`
- **Homepage/Global Standard:** `01_Homepage_and_Global.html`

---

## 2. Brand Guidelines & Rules

### Colours
- **Primary Blue:** `#0355A3` (`--ior-blue`)
- **Navy:** `#0A4066` (`--ior-navy`)
- **Deep Navy:** `#0B1929` (`--ior-deep`)
- **Sky Blue:** `#4DA8DA` (`--ior-sky`)
- **Aviation Gold:** `#C9A227` (`--av-gold`)

### Hard Rules
1. **No rounded corners.** `border-radius` must be `0` on all cards, buttons, and images. (Note: The CSS tokens `--radius-sm/md/lg` exist but should not be applied to UI elements).
2. **No use of the word "depot".** It must be replaced with "site", "office", or "location".
3. **Logo placeholder.** Must read `[IOR LOGO]` until the SVG is provided.
4. **Tone of Voice.** Direct, confident, regional Australian. No corporate jargon. "Zero Harm. No compromise."

---

## 3. UX & Structural Principles

1. **No long paragraphs.** Maximum 2–3 sentences per block. Break up text with lists, grids, or accordions.
2. **Primary CTA.** Every page must have a clear primary Call to Action above the fold (usually in the hero section).
3. **Global Navigation.** Must be identical across all pages (sticky nav + hamburger drawer).
4. **Global Footer.** Must be identical across all pages. Exactly 5 columns:
   - Fuel Solutions
   - Digital Platforms
   - Industries
   - Corporate
   - Quick Actions
5. **Scroll Animations.** Elements must use `data-animate="fade-up"` or `class="fade-up"` and be triggered by `ior-global.js`.
6. **SEO.** Every page must have a unique `<title>` and `<meta name="description">`.

---

## 4. User Journey Flows to Validate

When reviewing a page, consider if it successfully serves its primary persona:

- **Utility User (Driver/Operator):** Needs fast access to locations, Fuelcharge app download, and account application.
  *Flow:* Homepage → Ground Fuels → Diesel Network → Fuelcharge → Apply for Account
- **Revenue Engine (Procurement/B2B):** Needs assurance of supply chain reliability, bulk delivery specs, and contact info.
  *Flow:* Homepage → Industries → Mining / Transport → Contact Us
- **Talent (Job Seeker):** Needs to see culture, regional benefits, and clear application pathways.
  *Flow:* Careers Hub → Entry Pathways / Regional → Apply

---

## 5. Previous Feedback Log (Must Verify Fixed)

- [x] Footer was dropping off or inconsistent on Careers and About pages.
- [x] "Depot" must not appear anywhere on the site.
- [x] EVP YouTube videos must be embedded on all Careers sub-pages (Tahlia, Risky, Dylan, Luke, Drew, Darren).
- [x] ISO 45001 and ISO 14001 certifications must be explicitly called out on the Sustainability page.
- [x] RACQ LifeFlight, Heart of Australia, and Outback Futures must be highlighted on the Community page.
- [x] The "IOR is fuelling Australia" brand video must be embedded on the About IOR page.
- [x] Fuelcharge 3-step section must have the hover-image effect and App Store / Google Play badges.

---

## 6. Required Output Format

For each page reviewed, produce a markdown table row with the following columns:

1. **Page** (Filename)
2. **Brand** (Pass/Fail - colours, radius, forbidden words)
3. **UX** (Pass/Fail - CTA, paragraph length)
4. **Global** (Pass/Fail - nav, footer, JS)
5. **SEO** (Pass/Fail - title, meta)
6. **Notes** (Specific issues found)

Follow the table with a **Top 5 Priority Fixes** summary section.
