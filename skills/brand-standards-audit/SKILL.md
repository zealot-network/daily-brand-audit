---
name: brand-standards-audit
description: Extracts complete brand standards from a website (colors, typography, UI/UX, voice, photography, iconography, layout, components, platform notes) by scraping 12+ pages, then writes the full audit into a Notion database. Designed for daily scheduled runs across multiple brands.
---

# Brand Standards Audit

## Overview
This skill performs an exhaustive brand-standards extraction for a given brand website and saves the results into a Notion database. It is designed to run as a scheduled daily task, processing one brand per execution. The output must match the depth and quality of a senior designer at a top-tier design firm. Strategic analysis with exact values, page-by-page breakdowns, and interpretation of design intent. Not surface-level observations.

## Parameters
When invoking this skill, provide:
- **BRAND_NAME**. The human-readable brand name (e.g., "Ebbets Field").
- **BRAND_URL**. The root URL of the brand's website (e.g., "https://www.ebbets.com").
- **BRAND_DOMAIN**. The bare domain for favicon retrieval (e.g., "ebbets.com").
- **NOTION_DATA_SOURCE_ID**. The Notion data source (collection) ID for "All Brand Standards DB". Default for Brett's workspace: `326ccc30-3aed-8083-8e84-000b9fec7590`.
- **WORKSPACE_FOLDER**. The local folder where the markdown copy and state file live. Default for Brett's workspace: `/Users/bretthenry/Desktop/Brands and their Standards`.

---

## Tool environment

This skill runs in any Claude runtime. The two supported execution paths are:

**Browser-based runtime** (Perplexity Computer, Claude in Chrome with full DOM tools, or any environment exposing `browser_task` / `read_page` / `get_page_text`):
- Use the browser tools directly to navigate and scrape each page.
- Take screenshots where layout, color, spacing, or visual hierarchy matters.

**WebFetch-based runtime** (Cowork, Claude Code, or any environment without DOM-aware browser tools):
- Use the available `web_fetch` tool to retrieve each page's HTML.
- Large pages exceed the inline output budget. The tool will save the response to a temp file path and return that path. Use `bash` plus `grep` or `python3` slicing to extract specifics. Do NOT try to read the entire raw HTML into the main conversation. Recommended grep patterns:
  - `grep -oiE '#[0-9a-f]{6}\b' FILE | sort -u` for hex colors
  - `grep -oiE 'rgba?\([^)]+\)' FILE | sort -u` for rgb/rgba
  - `grep -oiE 'font-family:[^;"}]+' FILE | sort -u` for font families
  - `grep -oiE 'font-weight:[^;"}]+' FILE | sort -u`
  - `grep -iE 'class="[^"]*btn|button|cta' FILE | head -50` for button class signatures
  - `grep -iE '<title>|<h1|<h2|<meta name="description"' FILE | head -40` for SEO/headings
  - `grep -oiE '"--[a-z-]+":[^,}]+' FILE | sort -u` for CSS custom-property design tokens
- Spawn a research subagent for the multi-page extraction so the bulk HTML stays out of the main context. The subagent should return only the synthesized 10-section markdown body.

If neither runtime is available, halt and report. Do not fall back to clicking pixels through `computer-use` for a 12-page scrape. That is not a viable execution path for this skill.

---

## Workflow

### Step 1: Site Exploration
Open BRAND_URL and scrape **at least 12 distinct pages**. Use whichever extraction path your runtime supports.

**Required page types to visit:**
- Homepage
- 2-3 collection/category listing pages (PLP). Pick different categories to see variation.
- 2 product detail pages (PDP). Pick products from different categories.
- About / story / brand history page
- Editorial, blog, or educational content page (if available)
- Collaboration or special collection landing pages (if available)
- Custom/bespoke service pages (if available)
- Regional, cultural, or themed collection pages (if available)
- FAQ page
- Shipping information page
- Returns & exchanges page
- Contact page

For brands without traditional commerce structure (e.g., manufacturers like Kubota with dealer-mediated sales, B2B platforms, or institutional sites), substitute equivalent pages: dealer locator, configurator entry, product line PLPs at multiple depths, financing or service pages, corporate/global properties.

If a target slug returns 404, document that as a finding (it's a brand-hygiene observation worth surfacing) and substitute another page. Do not stop at fewer than 12 successfully scraped pages.

**On each page, extract:**
- All visible colors (backgrounds, text, buttons, borders, accents, hover states)
- Font families, sizes, weights, letter-spacing from headings, body, nav, buttons, labels
- Layout structure: column counts, grid gaps, section padding, content width
- UI component inventory: what components appear and how they behave
- Copy/language: headings, CTAs, product descriptions, microcopy, error messages
- Photography: image types, aspect ratios, styling approach (infer from alt text, image filenames, srcset, and surrounding copy when full DOM rendering is unavailable)
- Navigation state: how does the nav differ on this page type?
- Platform fingerprints: CMS hints in markup (Sitefinity, Shopify, Webflow, Sitecore, ASP.NET viewstate, JS framework signatures)
- SEO patterns: title format, meta description format, JSON-LD schema presence

---

### Step 2: Synthesize the Audit
Produce a **senior-designer-level** brand standards document with the following 10 sections. Every section must be deeply detailed with specific examples, exact values, page-by-page breakdowns, and strategic interpretation of design choices. Do NOT summarize or abbreviate.

#### Section 1: Color Palette
Document EVERY hex code found across the site, organized into these categories:
- **Primary brand colors**. The dominant colors that define the brand identity.
- **Secondary/accent colors**. Supporting colors used for emphasis or variation.
- **Background colors**. Page backgrounds, section backgrounds, card backgrounds, modal overlays.
- **Text colors**. Body text, heading text, link text (default, hover, visited), muted/secondary text, placeholder text.
- **Button colors**. Primary button fill, primary button text, secondary/outline button border, hover states, disabled states.
- **UI state colors**. Error/validation red, success green, warning, info, focus ring color.
- **Border/divider colors**. Card borders, section dividers, input field borders.
- **Announcement bar / banner colors**. Background and text.
- **Footer colors**. Background, text, link colors if different from main site.
- **Notable absences**. Colors you would expect to find but that are missing (e.g., no red for sales, no green for success states).

For each color, note WHERE it appears (which pages, which components) and WHY the brand likely chose it (strategic interpretation).

#### Section 2: Typography
Document the complete typographic system:
- **Font families**. List every font family loaded (from CSS, Google Fonts, Adobe Fonts, or self-hosted). Note the foundry and whether it is serif, sans-serif, monospace, or display.
- **Heading hierarchy**. For H1 through H6 (or however many levels are used), document: font-family, font-weight, font-size (px or rem), line-height, letter-spacing, text-transform (uppercase, lowercase, none), color. Note which heading levels appear on which page types.
- **Body text**. Font-family, weight, size, line-height, color, max-width/measure if constrained.
- **Navigation text**. Font specs for main nav links, dropdown items, mobile menu items, breadcrumbs.
- **Button text**. Font-family, weight, size, letter-spacing, text-transform for each button variant.
- **Price text**. Font treatment for prices, sale prices, compare-at prices, currency symbols.
- **Label/badge text**. "New", "Sale", "Sold Out", collection tags, product tags.
- **Form text**. Input placeholder text, input value text, label text, validation message text.
- **Footer text**. If typography differs from main content area.
- **Uppercase/lowercase usage rules**. Where does the brand use all-caps vs. sentence case vs. title case? Is there a pattern by component type?
- **Letter-spacing distribution**. Where is tracking tight vs. loose? Why?
- **Font-weight distribution**. Which weights are used where? Is the brand heavy on bold or light on weight?
- **Type scale philosophy**. What is the ratio between sizes? Is it a modular scale, or custom? What does the type hierarchy communicate about the brand?
- **Application by page type**. How does typography shift between homepage, PLP, PDP, editorial, and support pages?

#### Section 3: Logo & Wordmark
- **Primary logo**. Describe the logo (wordmark, icon, combination mark), its visual style, and where it appears.
- **Header placement**. Position, size, alignment in desktop and mobile headers.
- **Footer treatment**. Does the logo appear in the footer? Same version or different?
- **Favicon**. Describe the favicon design.
- **Logo variations**. Are there alternate versions (reversed, monochrome, stacked, horizontal)? Where does each appear?
- **Clear space and sizing**. How much space surrounds the logo? Minimum size observed.
- **Co-branding / collaboration lockups**. How does the logo appear alongside partner brands on collaboration pages? What is the visual hierarchy?
- **Logo-to-navigation relationship**. Spacing, alignment, and visual weight balance.
- **Logo as brand signal**. Strategic interpretation: what does the logo design communicate about brand positioning?

#### Section 4: Layout & Grid System
Document the spatial architecture of the site:
- **Content max-width**. What is the maximum content width (in px)? Does it vary by page type?
- **Homepage section sequence**. List every section on the homepage in order (hero, featured collection, editorial block, etc.) with approximate heights and content types.
- **PLP grid structure**. Number of columns (desktop, tablet, mobile), grid gap, card aspect ratios, items per row, pagination vs. infinite scroll vs. load more.
- **PDP layout**. Image gallery position and behavior (carousel, sticky scroll, thumbnails), info panel width ratio, section order below the fold (description, reviews, related products, etc.).
- **Editorial/content page layouts**. Single column? Two column? Full-bleed images? Text measure/width.
- **Support page layouts**. FAQ accordion style, contact form layout, shipping info structure.
- **Section padding rhythm**. Vertical padding between major sections (consistent or variable?).
- **Element spacing patterns**. Margins between headings and body text, between cards, between form fields.
- **Responsive breakpoints**. Where do layouts shift? What changes at each breakpoint?
- **Whitespace philosophy**. Is the brand generous or dense with space? How does this reinforce brand positioning?
- **Scroll depth patterns**. How deep is each page type? What is the content-to-viewport ratio?
- **Full-bleed vs. contained**. Which sections break out of the content container? Why?

#### Section 5: UI Components
Build an exhaustive inventory of every UI component on the site. Buttons (primary, secondary, tertiary, icon, sizing variants), navigation (desktop nav, mobile nav, sub-navigation, breadcrumbs, announcement bar), product cards, PDP components (image gallery, size selector, color/variant selector, quantity, add to cart, description, size chart, related products), forms (inputs, labels, validation, submit, newsletter), accordions, footer, search, cart, modals, toasts, loading states, empty states, video players, scroll animations, accessibility observations.

#### Section 6: Iconography
- **Icon library**. What icon set is used (Font Awesome, custom SVG, Shopify built-in, none)?
- **Icon style**. Line icons, filled icons, duotone? Stroke weight? Rounded or sharp corners?
- **Where icons appear**. Navigation (cart, search, account, hamburger), social media footer, payment methods, product features, trust badges, accordion expand/collapse.
- **Icon sizing**. Consistent or variable? What sizes for nav vs. inline vs. decorative?
- **Icon color**. Do icons match text color or have their own color treatment?
- **Notable absences**. Does the brand intentionally avoid icons? Use text instead of icons anywhere you would expect icons?
- **Icon philosophy**. Strategic interpretation: what does the icon approach say about the brand (minimal, utilitarian, decorative, playful)?

#### Section 7: Photography Style
- **Product photography**. Flat lay, mannequin/ghost, or on-model? Background color/texture. Lighting. Shadow treatment. Consistent angle or varied?
- **Lifestyle/editorial photography**. Candid vs. posed, environment types, color palette of settings, model demographics and styling, mood/tone.
- **Hero/banner imagery**. Full-bleed or contained? Overlaid text treatment. Image subject matter. Aspect ratios.
- **Collection page imagery**. Header images, how they differ from product shots.
- **About/brand story imagery**. Historical photos, behind-the-scenes, founder imagery, archival material.
- **Image aspect ratios by context**. Product cards, PDP gallery, hero banners, editorial inline images.
- **Color grading/filtering**. Warm, cool, neutral, desaturated, high-contrast? Consistent across site or variable?
- **Image quality and resolution**. Sharp/crisp or intentionally grainy/vintage?
- **Notable patterns**. Recurring visual motifs, props, settings, textures.
- **What is NOT shown**. Types of imagery the brand avoids.

#### Section 8: Brand Voice & Language Style
This section must be the deepest and most detailed. It sets the quality bar for all other sections.

**Tone & emotional register:** Overall tone (authoritative, playful, aspirational, casual, scholarly, etc.). How does tone shift by page type? Emotional register: what feelings does the brand try to evoke? What the brand explicitly avoids (urgency language, discount-speak, hype, etc.).

**Narrative voice:** First person, second person, third person, or imperative? Active vs. passive voice preference. Sentence length and complexity. Use of storytelling, historical references, or cultural context.

**Heading patterns:** Heading writing style by page type (declarative, interrogative, imperative, poetic). Capitalization convention. Length patterns. Use of punctuation in headings.

**Complete CTA inventory by page context:** List every CTA (button text, link text) found on each page type. Homepage hero CTAs, homepage section CTAs, collection/PLP page CTAs, PDP CTAs (Add to Cart text, secondary CTAs), editorial CTAs, footer CTAs, support page CTAs, custom/B2B CTAs, announcement bar CTAs, cart/checkout CTAs.

**Product description formula:** How are product descriptions structured? Average length and depth. Use of technical vs. emotional language.

**Recurring language patterns:** Phrases or words that appear across multiple pages. Brand-specific vocabulary. How the brand refers to itself.

#### Section 9: Platform & Technical Notes
- **CMS/Platform** (Shopify, WordPress/WooCommerce, BigCommerce, Sitefinity, Sitecore, AEM, custom, etc.). Version if detectable.
- **Theme** (theme name, theme ID if visible in source or URL patterns).
- **Section/template IDs** (Shopify section types, template names visible in classes or data attributes).
- **URL patterns** (collection URL structure, product URL structure, page URL structure, blog URL structure).
- **Third-party integrations** (reviews, email, analytics, chat, loyalty, wishlist). When a service is identified by an API key embedded in client-side config, name the service and redact the key value (see "Secret redaction rule" below). Do not write live keys or tokens into the audit output.
- **Performance observations** (page load feel, lazy loading, image optimization, render-blocking resources).
- **SEO title patterns** (format of page titles).
- **Meta description patterns** (consistent template or unique per page?).
- **Legal/policy page URLs** (privacy, terms, accessibility, shipping, returns).
- **Accessibility notes** (ARIA labels, skip-to-content, focus management, screen reader considerations).
- **Structured data** (JSON-LD product schema, breadcrumb schema, organization schema if present).

#### Section 10: Pages Scraped
List every URL visited during the audit with a page-type label.
- Format: `URL. Page Type (e.g., Homepage, PLP, PDP, About, Editorial, Support)`
- Must contain at least 12 entries.
- Group by page type for easy scanning.
- Include attempted-but-404 URLs as a separate group when relevant.

#### Output format
The first line of the audit document must be:

```
# {BRAND_NAME} Brand Standards Audit: extracted from {BRAND_URL} across [X] pages ({Month Year})
```

Use H1 for the title line, H2 for each of the 10 sections, H3 for subsections within each section.

#### Punctuation rule (HARD)
**Do not use em dashes (—) anywhere in the audit output.** This is a non-negotiable user preference. Use periods, colons, or sentence restructuring instead. If a draft contains em dashes, scrub them before saving or pushing to Notion. En dashes (–) in numeric ranges like "13–14px" are acceptable.

#### Secret redaction rule (HARD)
**Never write live API keys, tokens, or secrets verbatim into the audit output.** This applies even when a key is publicly visible in the brand's client-side code (e.g., a Google Maps browser key in a React config). Reasons: (1) the audit markdown is committed to a public-ish repo and pushed to Notion, which trips GitHub secret scanning and re-publishes the value; (2) it is not our place to amplify another organization's exposed credentials, even if they are referrer-restricted.

When you identify a service by its key, document the service and redact the key value. Use a `prefix…[redacted]` form so it is still recognizable as a real key without being usable:

- Google API keys (`AIza...`): write as `AIza…[redacted]`
- Mapbox tokens (`pk....` / `sk....`): write as `pk…[redacted]` / `sk…[redacted]`
- TomTom keys: write as the first 4 chars + `…[redacted]`
- Anything matching `[A-Za-z0-9_\-]{20,}` that looks like a credential: same `prefix…[redacted]` form
- Bearer tokens, JWTs, signed URLs with tokens: redact the token portion, keep the host

Before saving the audit file or writing to Notion, grep the output for common key patterns and replace any survivors. Recommended scrub:

```
grep -nE 'AIza[A-Za-z0-9_-]{35}|sk_(live|test)_[A-Za-z0-9]{20,}|pk\.[A-Za-z0-9._-]{40,}|ghp_[A-Za-z0-9]{36}|xox[baprs]-[A-Za-z0-9-]{10,}' audit_output.md
```

If the grep returns matches, redact and re-run until clean. Do not save or push until clean.

---

### Step 3: Save the audit to disk

Before writing to Notion, save the full audit markdown to the workspace folder:

```
{WORKSPACE_FOLDER}/{BRAND_NAME}_Brand_Standards_Audit_{YYYY-MM-DD}.md
```

This gives the user a local copy independent of Notion, and lets later runs reference and diff prior outputs.

---

### Step 4: Write to Notion

Use the Notion MCP `notion-create-pages` tool. Required arguments:

```
parent: { "type": "data_source_id", "data_source_id": NOTION_DATA_SOURCE_ID }
pages: [{
  "properties": { "Name": BRAND_NAME },
  "icon": "https://www.google.com/s2/favicons?domain={BRAND_DOMAIN}&sz=128",
  "content": "<full audit markdown body, including the H1 title line>"
}]
```

Notes:
- Notion renders the page title from the `Name` property. The H1 line in the content is treated as descriptive metadata (it includes the URL and page count), so keep it. Notion will show it as a top-of-page heading.
- Do NOT put audit content into database properties. Everything goes in the page body.
- After creation, the tool returns the new page ID. Capture it for the state log.

If the Notion MCP is not available in the runtime, halt and report rather than fall back to a manual web flow.

---

### Step 5: Update state and log the run

Append a record to `{WORKSPACE_FOLDER}/brand_audit_state_{YYYY-MM-DD}.json` (creating the file by copying the prior day's state if needed) with:
- `current_index` incremented by 1
- An entry in `completed[]` with: `brand`, `date`, `notion_page_id`, `category`, `pages_browsed`, `sources[]`, `method`

Also write a short run log to `{WORKSPACE_FOLDER}/_audit_logs/{BRAND_NAME}_{YYYY-MM-DD}_run_log.md` summarizing: pages browsed, Notion page ID, notable findings, environmental caveats, next-run guidance.

If a step failed (page didn't load, Notion write rejected, etc.), still update the state file and log the failure in `failed[]` rather than `completed[]`.

---

### Step 6: Quality check

Before declaring the run complete, verify:
- Every section has deep, example-rich content with specific values (hex codes, font names, px sizes, exact CTA text).
- No section is shorter or less detailed than Section 8 (Brand Voice).
- At least 12 pages were scraped and listed in Section 10.
- All hex codes include the `#` prefix and are accompanied by usage context.
- All font names are specific (not "sans-serif" but the actual family name).
- The Notion page icon is set via favicon URL.
- Strategic interpretation (the "why") is included alongside observations (the "what").
- Notable absences are documented in every relevant section.
- Em dashes have been stripped from the final output.
- No live API keys, tokens, or secrets remain in the output (run the secret-pattern grep from the Secret redaction rule and confirm zero matches before saving or pushing).
- Local markdown copy saved to the workspace folder.
- Notion page exists and renders all 10 H2 sections (verify with a follow-up `notion-fetch` call).

---

## Rules
- Do NOT abbreviate or summarize. Every section must be exhaustive.
- Do NOT skip support pages (FAQ, Shipping, Returns, Contact) when the brand has them. For dealer-mediated brands, substitute analogous pages (dealer locator, finance, service).
- Always note what is **absent** as well as what is present.
- Include the strategic "why" behind design choices, not just the "what".
- Back every observation with references to specific pages.
- When in doubt, include more detail rather than less.
- Each section should read like a chapter from a professional brand guidelines document.
- If a section seems thin, go back to the site and scrape additional pages for more data.
- Never em dashes in output.
- Never write live API keys, tokens, or secrets verbatim. Always use the `prefix…[redacted]` form, even for client-side keys that are publicly visible in the brand's HTML.

---

## Example invocation
"Run the brand-standards-audit skill for Patagonia at https://www.patagonia.com and add the results to my Notion All Brand Standards DB."

The skill will then:
1. Detect the available runtime (browser tools vs. WebFetch).
2. Scrape 12+ pages.
3. Synthesize the 10-section audit.
4. Save the markdown locally.
5. Create the Notion page with favicon.
6. Update the state file and write a run log.
7. QA-verify and report.
