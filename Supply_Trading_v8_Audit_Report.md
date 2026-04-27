# Content Audit Report: Supply & Trading Hub (v8)

**STAGING LINK:** [https://alexc-sketch.github.io/ior-prototype/06_Supply_Trading_v8.html](https://alexc-sketch.github.io/ior-prototype/06_Supply_Trading_v8.html)
**FOCUS KEYWORD:** bulk diesel supply Australia
**SECONDARY KEYWORDS:** diesel import terminal, sovereign fuel supply, fuel supply chain Australia
**META TITLE:** Supply & Trading | Bulk Diesel Import & Storage | IOR®
**META DESCRIPTION:** IOR operates two of Australia's largest diesel import terminals with 191ML combined capacity. Sovereign supply partner to the Federal Government. Enquire about terminal access.

---

## 1. Executive Summary

This document serves as the formal content and technical audit report for the newly rebuilt **Supply & Trading Hub (v8)** page. The page has been successfully developed, merged into the `main` branch, and pushed to the live GitHub Pages environment.

The build strictly adheres to the provided brief and the canonical IOR design system (`IOR_Global_Template_Shell_v4.html`). It acts as the primary silo hub for the Supply & Trading division, routing users to specific terminal and refinery pages while capturing high-value wholesale leads.

---

## 2. Technical & UX Audit

The page has been audited against the IOR global development standards to ensure zero issues in the build.

| Component | Status | Auditor Notes |
| :--- | :--- | :--- |
| **Global Navigation** | Passed | Canonical utility bar, primary nav, mega menus, and mobile drawer implemented verbatim from the shell template. No structural alterations made. |
| **Global Footer** | Passed | Canonical 6-column footer and pre-footer implemented verbatim. |
| **Silo Accent Color** | Passed | **IOR Green (`#00B140`)** applied correctly to buttons, eyebrows, active states, and pillar accents. No gold (`#D98300`) used on this page. |
| **Hero Section** | Passed | Solid dark navy (`#0A1628`) background with video placeholder. No gradient overlays used, adhering to strict design rules. |
| **Quick Links Bar** | Passed | "Supply & Trading" marked as the active state. Bar is static (not sticky), adhering to quicklink behavior rules. |
| **Responsive Design** | Passed | Fluid typography (`clamp()`) and CSS Grid used throughout. Fully responsive down to 320px mobile viewports. |
| **Accessibility (a11y)** | Passed | ARIA labels, roles, `aria-expanded` attributes, and semantic HTML5 tags (`<nav>`, `<main>`, `<section>`, `<article>`) implemented correctly. |

---

## 3. Content Audit & H-Tag Structure

The content has been audited for factual accuracy, brand tone of voice (professional, innovative, reliable, grounded), and correct hierarchical structure.

### H1: Hero Section
*   **Tag:** `<h1>Securing Australia's <span class="highlight">fuel supply chain.</span></h1>`
*   **Copy:** IOR operates two of Australia's most strategic diesel import and storage terminals, providing 191 million litres of combined capacity. As a sovereign supply partner to the Federal Government, we deliver absolute fuel security for Australian industry — wherever it operates.
*   **CTAs:** "Enquire About Terminal Access" (Primary, links to `#lead-capture`), "View Terminal Gate Pricing" (Ghost, links to external pricing page).

### H2: The Challenge (Section 4)
*   **Tag:** `<h2 id="problem-heading">Australia's fuel supply chain is more fragile than most operators realise.</h2>`
*   **Structure:** 3-card grid detailing Global Supply Disruption, Insufficient Local Storage, and Sovereign Risk.

### H2: Our Supply & Trading Operations (Section 5)
*   **Tag:** `<h2 id="routing-heading">From refinery to terminal to your site.</h2>`
*   **Structure:** 3-card routing grid linking to Lytton & Port Bonython Terminals, Eromanga Refinery, and Condensates.

### H2: Why IOR Supply & Trading (Section 6)
*   **Tag:** `<h2 id="why-ior-heading">The only independent fuel company with a sovereign supply mandate.</h2>`
*   **Structure:** 3 pillars detailing Sovereign Mandate, Strategic Infrastructure, and 40 Years of Reliability.

### H2: Lead Capture (Section 7)
*   **Tag:** `<h2 class="lead-capture__h2" id="lc-h2">Enquire about terminal access or term supply.</h2>`
*   **Notes:** HubSpot form placeholder included. Fields required: First Name, Last Name, Company, Email, Phone, Message. Primary button: "Submit Enquiry".

### H2: Resources & Insights (Related Content)
*   **Tag:** `<h2 id="rc-heading">Resources &amp; <span class="highlight">insights</span></h2>`
*   **Structure:** Tabbed grid for Case Studies and Blog Posts.

### H2: FAQs
*   **Tag:** `<h2 id="faq-heading">Supply &amp; Trading — <span class="highlight">common questions</span></h2>`
*   **Structure:** 5 accordion items addressing common Supply & Trading queries.

---

## 4. Pending Items for Production Handoff

The following items require input from the broader team before the page is considered 100% production-ready:

1.  **Video Asset:** The hero section requires the final aerial drone shot of the Lytton terminal (currently using a placeholder).
2.  **HubSpot Embed:** The marketing team needs to provide the Portal ID and Form ID to replace the placeholder in the Lead Capture section.
3.  **Logo Carousel:** Real client logos need to be inserted into the "Trusted by" carousel.
4.  **Related Content Links:** The placeholder case studies and blog posts need to be wired up to actual CMS content.
5.  **Condensates Page:** The routing card for Condensates currently links to `#lead-capture` as the `06c_Condensates_v8.html` page has not yet been built (as per the brief).

---

*Report generated by Manus AI.*
*Reference Briefing URL:* [https://alexc-sketch.github.io/ior-prototype-v3-5/00_Global_Components.html](https://alexc-sketch.github.io/ior-prototype-v3-5/00_Global_Components.html)
