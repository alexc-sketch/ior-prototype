# AUDIT & BUILD BRIEF: REGIONAL CONTACTS (v5.0)

**To:** UX Auditor & Development Team
**Page:** Regional Contacts
**Current GitHub URL:** `11b_Regional_Contacts.html`
**NEW Target GitHub URL:** `11b_Regional_Contactsv5.html`
**Global Components Reference:** [https://alexc-sketch.github.io/ior-prototype-v3-5/00_Global_Components.html](https://alexc-sketch.github.io/ior-prototype-v3-5/00_Global_Components.html)

---

## 💡 AUDITOR NOTES & BRAND RULES

*   **The "Utility Shell":** Build this on the `IOR_Utility_Template_Shell_v5.html`. Keep the Proto-bar, Header, Mobile Drawer, and Global Footer.
*   **🚨 STRICT BRAND RULE — NO "DEPOTS":** You must thoroughly scrub the word "Depot" from this page. Use "Regional Office", "Location", or "Service Area".
*   **No Phantom Addresses:** For regional sales/aviation reps who do not operate out of a public-facing corporate office, do not list a physical address. We do not want truck drivers navigating to a rep's home or corporate car park. Simply list their Name, Phone, Email, and "Service Area" (e.g., Service Area: Surat Basin).

---

## ⚙️ 1. GLOBAL NAV & SEO DIRECTIVES

*   **STAGING LINK:** `11b_Regional_Contactsv5.html`
*   **Meta Title:** IOR Regional Contacts — Local Support Across Australia | IOR
*   **Meta Description:** Find your local IOR contact. Regional offices and account managers across Queensland, NSW, WA, SA, NT, and Victoria. Locally-based support.
*   **Target Keywords:** IOR regional contacts, local fuel support, regional fuel account managers.

---

## 🏗️ 2. WIREFRAME COMPONENT FLOW & STRUCTURE

### 1. Minimal Utility Hero
*   **Style:** Solid brand color (`var(--ior-navy)`).
*   **Eyebrow:** LOCAL SUPPORT
*   **H1:** Regional Contacts.
*   **Subcopy:** Speak directly to the people on the ground. Find your local ground fuel or aviation representative for tailored support across Australia.

### 2. Quick Links Bar ("Explore:")
*   **Style:** The standard sticky horizontal link bar.
*   **Links Required:**
    1.  Contact Us
    2.  Help Centre & FAQs
    3.  Make a Payment
    4.  Find a Location

### 3. Interactive Map & Contact Directory (The Core Interaction)
*   **Layout:** A split-screen section.
*   **Left Column (Sticky):** Interactive Map of Australia.
    *   *Map Prompt (Left Column text above map):* Select your state or territory to view local IOR representatives.
*   **Right Column (Scrollable):** The contact cards for the selected state.

**🛠️ ELEMENTOR BUILD STRATEGY (How to build the map):**
The Developer has two ways to build this in Elementor:
*   **Option A (The Native Tabs Method - Recommended):** Use an Elementor Tabs Widget. Hide the default tab buttons using custom CSS. Embed a custom HTML SVG Map of Australia in the left column. Write a simple JavaScript snippet so that clicking an SVG path (e.g., `<path id="qld">`) triggers the click event on the corresponding hidden Elementor Tab, revealing the QLD contact cards in the right column.
*   **Option B (The Dynamic Loop Filter):** Use an Elementor Loop Grid for the contact cards (pulling from a Custom Post Type or ACF repeater). Use a plugin like JetSmartFilters or a custom AJAX script where clicking the SVG map applies a taxonomy filter (State) to the Loop Grid.

**Contact Card Design:**
Clean white cards with `border-top: 4px solid var(--ior-blue)`. Include:
*   Rep Name
*   Title/Division
*   Phone Icon
*   Email Icon
*   Service Area

*(Note for Builders: Populate the Contact Cards using the data from the provided Google Doc. Ensure the following format is strictly followed for each card):*

**[Card Template Format]**
*   **Name:** [First Last]
*   **Title:** [e.g., Regional Manager – Ground Fuels]
*   **Phone:** [Icon] [Phone Number]
*   **Email:** [Icon] [Email Address]
*   **Service Area:** [e.g., Surat Basin / South West QLD] *(Remember: DO NOT include physical street addresses unless it is an official, public-facing corporate office).*

### 4. 24/7 National Support CTA
*   **Style:** Full-width CTA strip (similar to the Pre-Footer, but distinct).
*   **H2:** Need immediate assistance?
*   **Copy:** For urgent after-hours supply emergencies or general national enquiries, our central support team is available 24/7.
*   **Button:** Call 1300 457 467

### 5. FAQ Accordion & "Still Have Questions?"
*   **Style:** Inject the standard Global FAQ accordion component here to deflect common support queries.
*   **Footer Box:** Ensure the standard "Still have questions? / Browse Help Centre" box is attached to the bottom of the FAQs.

### 6. Global Footer
*   **Style:** Append the standard v4.0 6-column global footer.

---

## 🎨 3. ASSET CHECKLIST FOR BUILDER

*   [x] Custom SVG Map of Australia (Paths divided by state for interactivity).
*   [x] List of Regional Contacts (via ACF / WordPress backend).
*   [x] Base Template to Duplicate: `IOR_Utility_Template_Shell_v5.html`
