# IOR Website Prototype — QA & Review Brief

**To the Reviewing Agent:**
You are a senior UX and brand QA reviewer. Your job is to audit every HTML page in this repository against the criteria below and produce a structured, page-by-page correction report.

---

## 1. Core References

| Input | What It Is | How to Provide |
|---|---|---|
| **Repository URL** | The GitHub repo containing all HTML/CSS/JS files | `https://github.com/alexc-sketch/ior-prototype` |
| **Brand Guidelines** | Colour tokens, typography, logo rules, tone of voice | See Section 2 below |
| **Design System file** | `IOR_Design_System.html` — the canonical component reference | In repository |
| **UX Journey Map** | The intended user flows | See Section 4 below |
| **UX Principles** | Agreed principles (e.g. "no long paragraphs", "zero harm first") | See Section 3 below |
| **Feedback Log** | Previous client/stakeholder feedback to check against | See Section 5 below |
| **Homepage reference** | `01_Homepage_and_Global.html` — the approved global standard | In repository |

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

## 6. Required Output Format: Page-by-Page Correction Report

For every page reviewed, you must provide a specific, actionable list of corrections needed to meet the criteria above.

**Format your output exactly like this:**

### [Filename.html]
**Status:** [PASS / NEEDS WORK / FAIL]
**Corrections Needed:**
- **Brand:** [List any wrong colours, rounded corners, or forbidden words. If none, write "Pass"]
- **UX/Copy:** [List any paragraphs that are too long, missing CTAs, or tone issues. If none, write "Pass"]
- **Global Elements:** [List any footer column mismatches, missing nav elements, or missing animation JS. If none, write "Pass"]
- **SEO:** [List missing or duplicate title/meta tags. If none, write "Pass"]
- **Journey Alignment:** [Does this page serve its intended persona? Yes/No + brief reason]

*(Repeat for every page in the repository)*

**Summary:**
At the end of the report, provide the **Top 5 Priority Fixes** across the entire site.
