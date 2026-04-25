# Auditor Notes: Support & Contact Hub v5 (PR #12)

**To:** Builder / Development Team
**From:** Support Auditor Agent
**Date:** April 25, 2026
**Target PR:** [PR #12 — feat: Support Hub v5 rebuild](https://github.com/alexc-sketch/ior-prototype/pull/12)
**Status:** **FAIL — REVISIONS REQUIRED**

---

## 1. Executive Summary

The rebuild of the Support & Contact Hub (`11_Support_Hubv5.html`) from the canonical `IOR_Utility_Template_Shell_v5.html` base has successfully resolved the majority of the previous audit violations. The DOM structure is clean, the component fidelity is high, and the protected core files remain untouched.

However, the PR **fails** the Golden Rules audit on two specific counts (R4 and R6) and contains a structural nesting issue with the `<main>` element. The merge is blocked until these issues are resolved.

---

## 2. Golden Rules Audit Results

| Rule | Category | Status | Auditor Notes |
| :--- | :--- | :--- | :--- |
| **R1** | Design | **PASS** | No rounded corners found. `border-radius: 0` is correctly applied. The `.btn--pill` exception is correctly used for Nav CTAs. |
| **R2** | Design | **PASS** | No gradients or blue overlays detected. |
| **R3** | Design | **PASS** | No inline `style="..."` attributes found in the HTML body. |
| **R4** | Design | **FAIL** | **Hero Background Color:** The `.utility-hero` CSS block on line 188 uses `var(--ior-navy)` correctly, but the builder notes in the HTML comments (line 605) state: `<!-- Rule: Solid var(--ior-blue) background — no gradient -->`. This contradicts the brief which requires `var(--ior-navy)`. The CSS is correct, but the documentation/intent is conflicting. |
| **R5** | Content | **PASS** | No operating hours found in the global footer. |
| **R6** | Content | **FAIL** | **Brand Language:** The banned word "depot" appears on line 39 in a comment: `║ ✓ Word "depot" not used — "office" / "representative" used ║`. While this is just a comment, the rule is absolute: the word must be entirely scrubbed from the file. |
| **R7** | Components | **PASS** | All global components (Utility Bar, Primary Nav, Mobile Drawer, Global Footer, Quick Links Bar) are present and structurally intact. |
| **R8** | Components | **PASS** | Nav CTAs correctly use the `.btn--pill` class. |
| **R9** | Components | **PASS** | Components align with the Global Components reference. |

---

## 3. UX & Dev QC Observations

### A. Structural Validation (Dev QC)
*   **`<main>` Element Nesting (WARN):** The `<main id="main-content">` tag (line 563) is currently placed *inside* the `.drawer` navigation block, before the drawer overlay and drawer navigation are properly closed. The `<main>` element must be correctly nested *outside* the mobile drawer.
*   **Scope Creep:** **PASS**. Only `11_Support_Hubv5.html` and `00_Master_Index.html` were modified.
*   **Protected Files:** **PASS**. No modifications to `ior-global.css`, `ior-global.js`, `ior-motion.js`, or `IOR_Design_System.html`.

### B. Master Index Protocol (Dev QC)
*   **No Duplication:** **FAIL**. The new `11_Support_Hubv5.html` card was added, but the old `11_Support_Hub.html` cards (lines 550 and 1168) were not replaced or properly archived. They still exist alongside the new v5 card.
*   **Link Accuracy:** **PASS**. The `href` points exactly to `11_Support_Hubv5.html`.
*   **Status Visuals:** **PASS**. The card correctly displays `<span class="badge b-review">IN REVIEW</span>`.
*   **QC Tracker:** **FAIL**. The QC Tracker section at the bottom of the index was not updated. In fact, the entire QC Tracker section appears to be missing from the `00_Master_Index.html` file.

---

## 4. Required Fixes for Merge Approval

Please implement the following corrections and push to the `feature/support-hub-v5-rebuild` branch:

1.  **R6 (Brand Language):** Remove the word "depot" from the HTML comment on line 39 of `11_Support_Hubv5.html`.
2.  **Structural Nesting:** Move the `<main id="main-content">` opening tag so that it sits *after* the closing tags of the mobile drawer (`</nav>`).
3.  **Master Index (Duplication):** Remove or properly archive the old `11_Support_Hub.html` cards from `00_Master_Index.html` so they do not sit adjacent to the new v5 card.
4.  **Master Index (QC Tracker):** Ensure the QC Tracker section exists at the bottom of the index and is updated to reflect the new page status.

Once these changes are pushed, the Auditor will re-run the checks.
