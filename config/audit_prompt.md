# Brand Standards Audit Prompt Template

Variables: {{BRAND_NAME}}, {{BRAND_URL}}, {{BRAND_DOMAIN}}

---

Go to {{BRAND_URL}} and extract the total and complete brand standards for {{BRAND_NAME}}. Think like a senior designer at the top design firm in the world. Browse at least 12 pages across the site -- homepage, collection/category pages, at least 2 product detail pages, about/story page, any editorial/blog content, FAQ/support pages, contact page, and any unique landing pages. Read the DOM and take screenshots of every page you visit.

Produce a comprehensive brand standards audit. The first line should read: "{{BRAND_NAME}} Brand Standards Audit -- extracted from {{BRAND_URL}} across [X] pages (March 2026)"

The audit MUST contain ALL of the following 10 sections with FULL depth -- no abbreviations, no summaries. Every section should be exhaustively detailed:

## 1. Color Palette
- Extract every hex color code used on the site (primary, secondary, background, text, CTA, borders, hover states, sale/promo colors)
- Key observation on palette strategy and restraint/richness
- Color application broken down by EVERY page type (Homepage, PLP, PDP, Editorial, FAQ, Footer)
- Color hierarchy & emotional role analysis
- Colors NOT used (what's deliberately absent from the UI)

## 2. Typography
- Identify all font families (serif, sans-serif, display, monospace) with closest match names
- Complete font usage map: every text element mapped to font family, weight, case, size, letter-spacing
- Typography application by EVERY page type (Homepage, PDP, PLP, Collection Landing, Editorial, FAQ, Brand Film/Video)
- Font pairing philosophy (why the combination works semiotically)
- Weight distribution analysis (which weights are used and where)
- Letter-spacing rules
- Complete type scale summary (every distinct size used)

## 3. Logo & Wordmark
- Primary logo description (type, color, placement)
- Logo characteristics (typeface style, weight, tracking)
- Placement rules (positioning, flanking elements, alignment)
- Color variations observed
- Sizing details
- Brand mark system (icon, monogram, symbol, or wordmark-only)
- Logo relationship to brand heritage/positioning

## 4. Layout & Grid System
- Global structure (max width, margins, header height, padding, gaps, footer columns)
- Every page template identified with layout description (Homepage, PLP, PDP, Editorial, FAQ, Contact)
- Product card anatomy (image, text, price, hover behavior, social proof elements)
- Responsive behavior (breakpoints, column shifts, stacking behavior)
- Whitespace strategy
- Grid alignment philosophy
- Homepage scroll architecture (module pattern, depth)
- PDP image gallery layout
- Footer layout details
- Layout elements NOT present (what's deliberately missing)

## 5. UI Components
- Buttons: every button style (primary CTA, text link CTA, size selector, color swatch) with colors, radius, height
- Navigation: desktop nav structure, mega menu behavior, announcement bar
- Forms: input styles, placeholders, submit buttons
- Accordions: style, separator, expand/collapse behavior
- Product carousels: scroll behavior, arrow placement, visible count
- Button states & interactions (hover, active, disabled, loading)
- Size selector behavior
- Color swatch behavior
- Mega menu details
- Announcement bar component specs
- Accordion component details (single vs multi expand)
- Search component
- Accessibility widget
- Link & hover states across all element types
- Video embed behavior
- Animation & motion philosophy (what's animated, what's static, and why)

## 6. Iconography
- Complete icon inventory (every icon on the site with description, usage location, and context)
- Icon design philosophy (why icons are/aren't used)
- Icon color rules
- Icon sizing
- What icons are NOT used (deliberate absences)

## 7. Photography Style
- Product photography (background, style, angles, props)
- Lifestyle/editorial photography (lighting, environments, casting, posing, color grading)
- Hero images (format, content, overlays)
- Photography strategy & art direction (image-to-product relationship)
- Historical/archival imagery usage and sourcing
- Lifestyle casting notes (age, styling, settings)
- Image aspect ratios by context
- Hover behavior on product cards
- Image treatment consistency (filters, overlays, post-processing)

## 8. Brand Voice & Language Style
- Tone: overall personality description with 10+ sub-categories (storytelling approach, educational voice, craftsman voice, community voice, anti-trend positioning, cultural respect, customer service tone, collection intro voice variations, etc.)
- Language patterns: every recurring pattern with specific examples from the browsed pages (founder narrative, product description structure, collection landing pattern, editorial pattern, material specification language, geographic/cultural specificity, price presentation, announcement bar messaging)
- Heading style: complete heading inventory by page with analysis of hierarchy pattern and capitalization rules
- CTAs & Microcopy: complete CTA inventory by page context (Homepage, PDP, Footer, Returns, B2B), plus microcopy tone analysis

## 9. Platform & Technical Notes
- Platform identification (Shopify, WordPress, custom, etc.) with evidence
- Theme architecture (section IDs, custom vs stock)
- URL structure patterns
- Third-party integrations identified
- Page performance observations
- SEO & meta title patterns
- Legal & compliance pages
- Accessibility features
- Social media accounts

## 10. Pages Browsed
- Numbered list of every page URL visited

CRITICAL INSTRUCTIONS:
- Do NOT abbreviate any section. Every section must have the same depth and thoroughness.
- Include specific examples, verbatim phrases, and exact measurements from the actual site content.
- Analyze what is NOT present (absent design choices) as thoroughly as what IS present.
- Include senior-level design analysis (the "why" behind choices, not just the "what").
- Write all content as markdown text that will be placed into a Notion page body.
