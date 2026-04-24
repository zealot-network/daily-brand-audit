---
name: brand-standards-audit
description: Extracts complete brand standards from a website (colors, typography, UI/UX, voice, photography, iconography, layout, components, platform notes) by scraping 12+ pages, then writes the full audit into a Notion database. Designed for daily scheduled runs across multiple brands.
---

# Brand Standards Audit — Perplexity Computer Skill

## Overview
This skill performs an exhaustive brand-standards extraction for a given brand website and saves the results into a Notion database. It is designed to run as a scheduled daily task, processing one brand per execution. The output must match the depth and quality of a senior designer at a top-tier design firm — not surface-level observations, but strategic analysis with exact values, page-by-page breakdowns, and interpretation of design intent.

## Parameters
When invoking this skill, provide:
- **BRAND_NAME** — The human-readable brand name (e.g., "Ebbets Field")
- **BRAND_URL** — The root URL of the brand's website (e.g., "https://www.ebbets.com")
- **BRAND_DOMAIN** — The bare domain for favicon retrieval (e.g., "ebbets.com")

---

## Workflow

### Step 1: Site Exploration
Open BRAND_URL and scrape **at least 12 distinct pages**. For each page, use `read_page` and `get_page_text` to extract full DOM content. Take screenshots where layout, color, spacing, or visual hierarchy matters.

**Required page types to visit:**
- Homepage
- 2-3 collection/category listing pages (PLP) — pick different categories to see variation
- 2 product detail pages (PDP) — pick products from different categories
- About / story / brand history page
- Editorial, blog, or educational content page (if available)
- Collaboration or special collection landing pages (if available)
- Custom/bespoke service pages (if available)
- Regional, cultural, or themed collection pages (if available)
- FAQ page
- Shipping information page
- Returns & exchanges page
- Contact page

**On each page, extract:**
- All visible colors (backgrounds, text, buttons, borders, accents, hover states)
- Font families, sizes, weights, letter-spacing from headings, body, nav, buttons, labels
- Layout structure: column counts, grid gaps, section padding, content width
- UI component inventory: what components appear and how they behave
- Copy/language: headings, CTAs, product descriptions, microcopy, error messages
- Photography: image types, aspect ratios, styling approach
- Navigation state: how does the nav differ on this page type?

---

### Step 2: Synthesize the Audit
Produce a **senior-designer-level** brand standards document with the following 10 sections. Every section must be deeply detailed with specific examples, exact values, page-by-page breakdowns, and strategic interpretation of design choices. Do NOT summarize or abbreviate.

#### Section 1: Color Palette
Document EVERY hex code found across the site, organized into these categories:
- **Primary brand colors** — the dominant colors that define the brand identity
- **Secondary/accent colors** — supporting colors used for emphasis or variation
- **Background colors** — page backgrounds, section backgrounds, card backgrounds, modal overlays
- **Text colors** — body text, heading text, link text (default, hover, visited), muted/secondary text, placeholder text
- **Button colors** — primary button fill, primary button text, secondary/outline button border, hover states, disabled states
- **UI state colors** — error/validation red, success green, warning, info, focus ring color
- **Border/divider colors** — card borders, section dividers, input field borders
- **Announcement bar / banner colors** — background and text
- **Footer colors** — background, text, link colors if different from main site
- **Notable absences** — colors you would expect to find but that are missing (e.g., no red for sales, no green for success states)

For each color, note WHERE it appears (which pages, which components) and WHY the brand likely chose it (strategic interpretation).

#### Section 2: Typography
Document the complete typographic system:
- **Font families** — list every font family loaded (from CSS, Google Fonts, Adobe Fonts, or self-hosted). Note the foundry and whether it is serif, sans-serif, monospace, or display.
- **Heading hierarchy** — for H1 through H6 (or however many levels are used), document: font-family, font-weight, font-size (px or rem), line-height, letter-spacing, text-transform (uppercase, lowercase, none), color. Note which heading levels appear on which page types.
- **Body text** — font-family, weight, size, line-height, color, max-width/measure if constrained.
- **Navigation text** — font specs for main nav links, dropdown items, mobile menu items, breadcrumbs.
- **Button text** — font-family, weight, size, letter-spacing, text-transform for each button variant.
- **Price text** — font treatment for prices, sale prices, compare-at prices, currency symbols.
- **Label/badge text** — "New", "Sale", "Sold Out", collection tags, product tags.
- **Form text** — input placeholder text, input value text, label text, validation message text.
- **Footer text** — if typography differs from main content area.
- **Uppercase/lowercase usage rules** — where does the brand use all-caps vs. sentence case vs. title case? Is there a pattern by component type?
- **Letter-spacing distribution** — where is tracking tight vs. loose? Why?
- **Font-weight distribution** — which weights are used where? Is the brand heavy on bold or light on weight?
- **Type scale philosophy** — what is the ratio between sizes? Is it a modular scale, or custom? What does the type hierarchy communicate about the brand?
- **Application by page type** — how does typography shift between homepage, PLP, PDP, editorial, and support pages?

#### Section 3: Logo & Wordmark
- **Primary logo** — describe the logo (wordmark, icon, combination mark), its visual style, and where it appears.
- **Header placement** — position, size, alignment in desktop and mobile headers.
- **Footer treatment** — does the logo appear in the footer? Same version or different?
- **Favicon** — describe the favicon design.
- **Logo variations** — are there alternate versions (reversed, monochrome, stacked, horizontal)? Where does each appear?
- **Clear space and sizing** — how much space surrounds the logo? Minimum size observed.
- **Co-branding / collaboration lockups** — how does the logo appear alongside partner brands on collaboration pages? What is the visual hierarchy?
- **Logo-to-navigation relationship** — spacing, alignment, and visual weight balance.
- **Logo as brand signal** — strategic interpretation: what does the logo design communicate about brand positioning?

#### Section 4: Layout & Grid System
Document the spatial architecture of the site:
- **Content max-width** — what is the maximum content width (in px)? Does it vary by page type?
- **Homepage section sequence** — list every section on the homepage in order (hero, featured collection, editorial block, etc.) with approximate heights and content types.
- **PLP grid structure** — number of columns (desktop, tablet, mobile), grid gap, card aspect ratios, items per row, pagination vs. infinite scroll vs. load more.
- **PDP layout** — image gallery position and behavior (carousel, sticky scroll, thumbnails), info panel width ratio, section order below the fold (description, reviews, related products, etc.).
- **Editorial/content page layouts** — single column? Two column? Full-bleed images? Text measure/width.
- **Support page layouts** — FAQ accordion style, contact form layout, shipping info structure.
- **Section padding rhythm** — vertical padding between major sections (consistent or variable?).
- **Element spacing patterns** — margins between headings and body text, between cards, between form fields.
- **Responsive breakpoints** — where do layouts shift? What changes at each breakpoint?
- **Whitespace philosophy** — is the brand generous or dense with space? How does this reinforce brand positioning?
- **Scroll depth patterns** — how deep is each page type? What is the content-to-viewport ratio?
- **Full-bleed vs. contained** — which sections break out of the content container? Why?

#### Section 5: UI Components
Build an exhaustive inventory of every UI component on the site:

**Buttons:**
- Primary button: fill color, text color, font specs, padding, border-radius, hover state, active state, disabled state
- Secondary/outline button: border color, text color, background, hover behavior
- Text-link buttons: underline style, color, hover behavior
- Icon buttons (if any): size, padding, icon style
- Button sizing: are there small/medium/large variants? Where is each used?
- CTA placement patterns: where do buttons appear relative to content?

**Navigation:**
- Desktop nav: structure (horizontal links, mega-menu, dropdowns), font specs, spacing between items, active/current state, hover state
- Mobile nav: hamburger icon style, slide-out drawer or full-screen overlay, menu item hierarchy, close behavior
- Sub-navigation or category filters (on PLP pages)
- Breadcrumbs: separator style, font specs, truncation behavior
- Announcement/utility bar: position, content type, dismiss behavior, link style

**Product Cards (PLP):**
- Card anatomy: image container (aspect ratio, hover behavior like quick-view or image swap), product title, price, color swatches (if shown), badge/label position
- Card spacing: gap between cards, internal padding
- Hover behavior: image change, overlay, button reveal, shadow, border
- Card click target: entire card or just image/title?

**Product Detail Page Components:**
- Image gallery: layout (side thumbnails, bottom thumbnails, carousel dots), zoom behavior, image count indicator
- Size selector: button group, dropdown, or segmented control? Selected state styling, out-of-stock state
- Color/variant selector: swatches (circle, square, image-based), selected indicator, swatch size
- Quantity selector: +/- buttons or input field? Styling
- Add to cart button: size, prominence, position (sticky on mobile?), loading state
- Product description: accordion or open? Tab structure?
- Size chart/guide: modal, inline, or link?
- Related/recommended products: carousel or grid?

**Forms:**
- Input fields: border style, border-radius, padding, focus ring color, placeholder text style
- Labels: position (above, floating, inline), font specs
- Validation: error message style, success state, inline vs. below-field
- Submit buttons: styled differently from other buttons?
- Newsletter signup: placement, input+button layout, confirmation behavior

**Accordions:**
- Where used (FAQ, PDP details, mobile nav)
- Expand/collapse icon: plus/minus, chevron, caret
- Animation: smooth expand or instant?
- Border/divider between items

**Footer:**
- Column count and structure
- Content: nav links, social icons, newsletter signup, payment icons, legal links
- Social icon style: brand-colored or monochrome?
- Payment method icons: which ones, what style?

**Other Components:**
- Search: icon-triggered or persistent input? Predictive/autocomplete?
- Cart drawer vs. cart page: which pattern? Styling.
- Modal/popup: overlay color, animation, close button style, content types (newsletter, size chart, quick view)
- Toast/notification: style, position, auto-dismiss?
- Loading states: skeleton screens, spinners, progress bars?
- Empty states: empty cart, no search results — messaging and illustration style
- Video players: custom controls or native? Autoplay behavior.
- Scroll animations: parallax, fade-in, slide-up? Subtle or prominent?

**Accessibility observations:**
- Focus indicators: visible or suppressed?
- Alt text patterns on images
- Keyboard navigation support
- Color contrast compliance (approximate)

#### Section 6: Iconography
- **Icon library** — what icon set is used (Font Awesome, custom SVG, Shopify built-in, none)?
- **Icon style** — line icons, filled icons, duotone? Stroke weight? Rounded or sharp corners?
- **Where icons appear** — navigation (cart, search, account, hamburger), social media footer, payment methods, product features, trust badges, accordion expand/collapse
- **Icon sizing** — consistent or variable? What sizes for nav vs. inline vs. decorative?
- **Icon color** — do icons match text color or have their own color treatment?
- **Notable absences** — does the brand intentionally avoid icons? Use text instead of icons anywhere you would expect icons?
- **Icon philosophy** — strategic interpretation: what does the icon approach say about the brand (minimal, utilitarian, decorative, playful)?

#### Section 7: Photography Style
- **Product photography** — flat lay, mannequin/ghost, or on-model? Background color/texture. Lighting (soft/diffused, hard/directional, studio, natural). Shadow treatment. Consistent angle or varied?
- **Lifestyle/editorial photography** — candid vs. posed, environment types, color palette of settings, model demographics and styling, mood/tone
- **Hero/banner imagery** — full-bleed or contained? Overlaid text treatment. Image subject matter. Aspect ratios.
- **Collection page imagery** — header images, how they differ from product shots
- **About/brand story imagery** — historical photos, behind-the-scenes, founder imagery, archival material
- **Image aspect ratios by context** — product cards, PDP gallery, hero banners, editorial inline images
- **Color grading/filtering** — warm, cool, neutral, desaturated, high-contrast? Consistent across site or variable?
- **Image quality and resolution** — sharp/crisp or intentionally grainy/vintage?
- **Notable patterns** — recurring visual motifs, props, settings, textures
- **What is NOT shown** — types of imagery the brand avoids (e.g., no lifestyle shots, no models, no close-ups)

#### Section 8: Brand Voice & Language Style
This section must be the deepest and most detailed. It sets the quality bar for all other sections.

**Tone & Emotional Register:**
- Overall tone (authoritative, playful, aspirational, casual, scholarly, etc.)
- How does tone shift by page type (homepage vs. PDP vs. editorial vs. support)?
- Emotional register: what feelings does the brand try to evoke?
- What the brand explicitly avoids (urgency language, discount-speak, hype, etc.)

**Narrative Voice:**
- First person, second person, third person, or imperative?
- Active vs. passive voice preference
- Sentence length and complexity (short punchy vs. long literary)
- Use of storytelling, historical references, or cultural context

**Heading Patterns:**
- Heading writing style by page type (declarative, interrogative, imperative, poetic)
- Capitalization convention (title case, sentence case, all-caps)
- Length patterns (short 2-3 word vs. full phrases)
- Use of punctuation in headings (periods, colons, em-dashes)

**Complete CTA Inventory by Page Context:**
List every CTA (button text, link text) found on each page type:
- Homepage hero CTAs
- Homepage section CTAs
- Collection/PLP page CTAs
- PDP: Add to Cart text, secondary CTAs (size chart, wishlist, share)
- Editorial/content page CTAs
- Footer CTAs (newsletter, social, nav)
- Support page CTAs (contact form submit, return initiation)
- Custom/B2B page CTAs (inquiry, quote request)
- Announcement bar CTAs
- Cart/checkout CTAs

**Product Description Formula:**
- How are product descriptions structured? (opening hook, feature list, heritage/story, materials, care)
- Average length and depth
- Use of technical vs. emotional language

**Recurring Language Patterns:**
- Phrases or words that appear across multiple pages
- Brand-specific vocabulary or terminology
- How the brand refers to itself (we, the brand name, passive)

#### Section 9: Platform & Technical Notes
- **CMS/Platform** — Shopify, WordPress/WooCommerce, BigCommerce, custom, etc. Version if detectable.
- **Theme** — theme name, theme ID if visible in source or URL patterns
- **Section/template IDs** — Shopify section types, template names visible in classes or data attributes
- **URL patterns** — collection URL structure, product URL structure, page URL structure, blog URL structure
- **Third-party integrations** — reviews (Yotpo, Judge.me, Stamped), email (Klaviyo, Mailchimp), analytics (GA4, Meta Pixel), chat, loyalty programs, wishlist apps
- **Performance observations** — page load feel (fast, moderate, slow), lazy loading, image optimization, render-blocking resources
- **SEO title patterns** — format of page titles (e.g., "Product Name – Brand Name", "Collection | Brand")
- **Meta description patterns** — consistent template or unique per page?
- **Legal/policy page URLs** — list URLs for privacy policy, terms of service, accessibility statement, shipping policy, returns policy
- **Accessibility notes** — ARIA labels, skip-to-content links, focus management, screen reader considerations
- **Structured data** — JSON-LD product schema, breadcrumb schema, organization schema if present

#### Section 10: Pages Scraped
List every URL visited during the audit with a page-type label:
- Format: `URL — Page Type (e.g., Homepage, PLP, PDP, About, Editorial, Support)`
- Must contain at least 12 entries
- Group by page type for easy scanning

#### Output Format
The first line of the audit document must be:
> **{BRAND_NAME} Brand Standards Audit** — extracted from {BRAND_URL} across [X] pages ([Month Year])

Use H1 for the title line, H2 for each of the 10 sections, H3 for subsections within each section.

---

### Step 3: Write to Notion
1. Open the Notion workspace: **Zealot → Brands and their Standards → All Brand Standards DB**.
2. Create a new row with Name = BRAND_NAME.
3. Open the new page.
4. Set the page icon using the Link option with this URL:
   `https://www.google.com/s2/favicons?domain={BRAND_DOMAIN}&sz=128`
5. Write the entire audit into the page body using proper heading hierarchy (H1 for the title line, H2 for each of the 10 sections, H3 for subsections).
6. Do NOT put content into database properties — write everything into the page body.

### Step 4: Quality Check
Before considering the task complete, verify:
- Every section has deep, example-rich content with specific values (hex codes, font names, px sizes, exact CTA text)
- No section is shorter or less detailed than the Brand Voice section
- At least 12 pages were scraped and listed in Section 10
- All hex codes include the # prefix and are accompanied by usage context
- All font names are specific (not "sans-serif" but the actual family name)
- The Notion page icon is set via favicon URL
- Strategic interpretation (the "why") is included alongside observations (the "what")
- Notable absences are documented in every relevant section

---

## Rules
- Do NOT abbreviate or summarize. Every section must be exhaustive.
- Do NOT skip support pages (FAQ, Shipping, Returns, Contact).
- Always note what is **absent** as well as what is present.
- Include the strategic "why" behind design choices, not just the "what".
- Back every observation with references to specific pages.
- When in doubt, include more detail rather than less.
- Each section should read like a chapter from a professional brand guidelines document.
- If a section seems thin, go back to the site and scrape additional pages for more data.

---

## Example Invocation
"Run the brand-standards-audit skill for Patagonia at https://www.patagonia.com and add the results to my Notion All Brand Standards DB."