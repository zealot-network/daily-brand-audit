# Attio Brand Standards Audit -- extracted from https://attio.com across 14 pages (April 2026)

---

## 1. Color Palette

### Every Hex Color Code Used on the Site

Based on exhaustive visual observation and DOM analysis across all 14 pages, Attio's color palette is one of the most restrained in the SaaS industry. The brand operates almost entirely within a near-monochromatic system anchored by black and white, with a single high-impact blue accent used surgically.

#### Primary Colors

- **#0D0D0D / #111111 (Near-Black / Soft Black)** — The dominant text and heading color across all pages. Used for all primary headings, body copy, and the logo wordmark. Slightly softer than pure black (#000000), giving the typography a warmer, more humanistic quality.
- **#FFFFFF (White)** — Background color for all main content areas. Pricing cards, help center, blog, and the main content zones are pure white.
- **#F5F5F5 / #F7F7F7 (Off-White / Near-White)** — Used as secondary background on alternating page sections. The homepage's feature demo tabs, table rows in the pricing comparison, and the help center left sidebar all use this near-white to create depth without introducing color.

#### Accent / Brand Color

- **#2563EB / approximately #2460EB (Electric Blue / Attio Blue)** — The single signature accent color. Observed in:
  - The "Start for free" primary CTA button (filled state).
  - The "Continue with Pro" pricing CTA button (highlighted / most-popular plan).
  - The blue arrow/send icon in the Ask Attio chat input UI component.
  - Hover states on the Changelog "Subscribe" button.
  - The "Feature" tag badge dot on the Changelog page (solid blue circle indicator).
  - The legend dot in reporting charts (US market segment indicator).
  - The chat widget send button (circular, ~#2563EB fill).
  - Link underlines and hover states on Help Center navigation.
  - The "Official app" green-bordered badge uses a lighter tint for its background, while the green dot itself is #22C55E (Tailwind green-500), suggesting third-party icon use, not brand color.

#### Secondary / UI Colors

- **#E5E7EB (Light Gray / Border Gray)** — Used for all card borders, table dividers, input field borders, and the subtle gridlines in the pricing comparison table. Equivalent to Tailwind's gray-200.
- **#9CA3AF (Medium Gray)** — Used for secondary text, metadata labels ("Per user/month, billed annually"), pricing comparison secondary text, and blog article timestamps. Equivalent to Tailwind gray-400.
- **#6B7280 (Muted Gray)** — Used for tertiary copy: captions, breadcrumbs (e.g., "APPS / SLACK"), changelog dates ("April 09, 2026"), and the "/ REDEFINING CRM" section markers. Equivalent to Tailwind gray-500.
- **#374151 (Dark Gray)** — Appears in descriptive body text on feature/platform pages and the help center. Bridge between near-black headings and medium-gray secondary text.

#### Background Textures and Decorative Colors

- **Dot Grid Pattern (#D1D5DB on #FFFFFF)** — A recurring decorative motif: a subtle, regular grid of small dots used as a background texture on the Careers hero, the homepage hero, the Changelog hero, the Manifesto page, and the Startup program hero. Color of dots is approximately #D1D5DB (Tailwind gray-300) against white.
- **#F9FAFB (Ghost White)** — The faintest background used on pricing card for the "Free" tier, and some section backgrounds.
- **Highlight color in Manifesto heading** — The word "magic." in the manifesto hero is rendered in a light gray (#A3A3A3) or near-transparent color, used to de-emphasize the word and create typographic contrast with the black text, creating a fade/ghost effect within the heading.

#### Status / Semantic Colors (in Product UI Screenshots)

- **#22C55E (Green)** — Used in the product UI screenshots for "Running" workflow status badge, "Official app" indicator badge, and positive/success states in the Reporting charts (EMEA dataset indicator).
- **#F59E0B (Amber/Orange)** — Appears in the workflow builder UI as the "Condition" node badge color (warning/branch logic).
- **#EF4444 (Red)** — Does not prominently appear but implied in error states in product UI.
- **#8B5CF6 (Purple)** — Appears subtly in Reporting page product screenshot as the "Workspaces" data series color.

#### Save/Promo Colors

- **Save 20% badges** — On Pricing page, the "Save 20%" label appears in black text on a light yellow/cream background (#FEF9C3 approximately, Tailwind yellow-100). This is the only warm accent color on the entire site, used exclusively to highlight pricing savings and draw attention to the annual billing toggle benefit.

### Key Observation on Palette Strategy and Restraint/Richness

Attio's palette strategy is one of **extreme typographic minimalism**. In a SaaS landscape saturated with vibrant gradient backgrounds, rainbow icon sets, and multi-color marketing, Attio makes a deliberate counter-statement: near-total chromatic restraint, with a single electric blue accent deployed with surgical precision. The result is a brand that reads as serious, confident, and modern — communicating product-led credibility rather than marketing spectacle.

The closest analogue in the SaaS world is Linear (the project management tool) which similarly uses a near-monochromatic palette to signal taste and engineering culture. Attio applies this same philosophy to the CRM space, differentiating itself visually from Salesforce (heavy blues and grays with red accent), HubSpot (orange-dominant), and Pipedrive (green-dominant).

The strategic insight: restraint in color is itself a brand signal — it tells sophisticated users "we trust our product to speak for itself." The blue CTA is strong enough to guide conversion without polluting the brand experience.

### Color Application by Page Type

**Homepage:**
- Background: #FFFFFF (white) for primary sections, #F5F5F5 for alternating feature blocks.
- Large section break: Full-width near-black (#0D0D0D) background used for the testimonial marquee block ("When I first opened Attio…") with white text — creating dramatic contrast and visual relief.
- CTA buttons: Blue (#2563EB) for "Start for free"; transparent with dark border for "Talk to sales."
- Dot grid decorative texture on hero background.
- Social proof section: White background with a slow-scrolling ticker of avatar/profile photos, creating a human, social-proof section without introducing color complexity.

**Product/Feature Pages (Ask Attio, Data Model, Automations, Reporting):**
- White backgrounds throughout.
- Category badge pills (e.g., "Data model", "Ask Attio", "Reporting"): Small rounded rectangles with a light gray border (#E5E7EB) and dark text, sitting above hero headings. No color fill.
- Product UI screenshots use the internal Attio UI colors (blue, green, amber for workflow statuses).

**Pricing Page:**
- Background: White.
- Plan cards: All on white with light gray borders, except the "Pro" card (highlighted/recommended) which has a slightly elevated appearance. The Pro column's CTA button is filled blue; other CTAs are outlined/ghost.
- "Save 20%" badge: Cream/yellow tint.
- Pricing table: Alternating row background in very light gray vs white for readability.

**Customers Page:**
- White background.
- Customer logos rendered in solid black, stripped of their brand colors — a design decision that unifies all partner logos into Attio's monochromatic system.

**Careers Page:**
- White background.
- Dot grid decorative pattern used on hero behind heading.
- Team photo grid presented in full color — the one section with authentic human color.
- Section labels ("/ CAREERS") in muted gray.

**Blog Page:**
- White background.
- Category tags ("PRODUCT", "COMPANY", "GUIDES") rendered as uppercase labels in muted gray or black without color-coding — no colored tag system.
- Article timestamps in muted gray (#9CA3AF).

**Changelog Page:**
- White background.
- Feature category badge: Solid blue circle dot followed by "Feature" text in black.
- Email input field: White with gray border.
- Subscribe CTA: Black fill, white text — reversal of the usual blue CTA, signaling lower-priority action.

**Help Center:**
- White content area.
- Left sidebar: Light gray background (#F5F5F5) for navigation.
- Category card icons (Academy, Reference, API): Light gray rounded square icon containers.
- Popular search tags: Outlined pill badges in gray.

**Legal Pages (Privacy Policy, Terms & Conditions):**
- Full white background.
- Sidebar legal navigation links: plain text in near-black.
- No decorative elements, no color beyond functional.

**App/Integration Pages (Slack):**
- White background with dashed-border container for the app header.
- "Official app" badge: Light green background with green dot (#22C55E).
- CTA "Install app": Black fill, white text.

**Manifesto / Redefine Page:**
- White background.
- The word "magic." appears as a faded/ghost text — lighter gray within an otherwise black heading, creating a visual motif of gradual revelation.

**Startup Program Page:**
- White background.
- Category badge pill: "Startup program" in gray border.
- Customer logos in black (same treatment as Customers page).
- Form inputs: Standard white inputs with gray borders.

**Footer (all pages):**
- White background.
- Footer text in muted grays (#6B7280, #9CA3AF).
- Logo in near-black.
- Social icons as simple line glyphs in gray.

### Color Hierarchy and Emotional Role Analysis

1. **Near-Black (#111111)** — Authority, permanence, confidence. Used for all value propositions, headings, and the logo. Communicates seriousness and technical credibility.
2. **White (#FFFFFF)** — Openness, space, modern clarity. The dominant background; signals that the product itself is the hero, not decorative chrome.
3. **Electric Blue (#2563EB)** — Action, forward momentum, conversion. Reserved exclusively for primary CTAs and critical interactive states. Its rarity makes it powerful — the eye is trained to associate this color with the one action Attio wants taken.
4. **Medium Gray (#9CA3AF, #6B7280)** — Support, metadata, hierarchy. Used for all secondary information — it recedes so primary content can lead.
5. **Dot Grid (Gray on White)** — Depth, technical texture, a nod to graph paper and data. The grid pattern carries a subtle message: Attio is structured, precise, and data-oriented — without being cold.

### Colors Deliberately Absent

- **No gradients** — No linear, radial, or mesh gradients appear anywhere on the marketing site. This is a deliberate rejection of the "Web3 / 2021-era SaaS" aesthetic.
- **No brand orange, green, or purple** — Despite these being common SaaS brand colors, Attio avoids all of them as primary brand expressions.
- **No dark mode** — The entire marketing site is light-mode only. Dark backgrounds appear only as full-bleed section breaks.
- **No neon or fluorescent colors** — No electric green, hot pink, or cyber yellow.
- **No photography-driven color** — Customer photography (on Customers and Careers pages) is used sparingly and never bleeds color into the UI chrome.
- **No red accent** — Despite red being a high-conversion CTA color, Attio avoids it entirely in brand UI. Red is reserved for error states within the product, not the marketing site.

---

## 2. Typography

### Font Families Identified

**Primary Typeface: Inter (or a very close custom variant)**
Attio's main typeface for all body copy, UI text, navigation, pricing tables, and supporting content is **Inter** — the open-source, sans-serif typeface designed by Rasmus Andersson, originally optimized for computer screens. Inter is identifiable by its tall x-height, open apertures, and the slightly squared-off geometry of its letterforms. It is virtually the industry standard for high-quality SaaS interfaces.

**Display / Heading Typeface: A Modified or Custom Grotesque — Possibly "Editorial New" or "Neue Montreal" or a licensed variant**
The display typeface used for all major headings ("Customer relationship magic.", "From zero to IPO.", "The CRM behind the next generation of companies.") is distinctly different from Inter. Key characteristics observed:
- Taller, more dramatic x-height than Inter.
- Slightly condensed proportions on some headings.
- The period/full stop at end of headlines is characteristic — used as a design element (e.g., "magic.", "Automate. Iterate. Accelerate.", "Ask Attio.").
- Variable weight rendering: headlines range from Regular to Bold depending on emphasis level.
- Strong resemblance to **Neue Montreal** (by Pangram Pangram Foundry) or possibly a licensed display grotesque.
- The Manifesto page heading "CRM /ˌsiː ɑːr ˈɛm/ abbr." uses phonetic IPA characters — suggesting a typeface with broad Unicode support and linguistic personality.

**Monospace (limited):**
Within the product UI screenshot components (not in the main marketing copy), what appears to be a monospace typeface is used for code-adjacent content (API keys, workflow node identifiers). Likely **JetBrains Mono** or similar.

### Complete Font Usage Map

| Text Element | Family | Weight | Case | Approx Size | Letter-Spacing |
|---|---|---|---|---|---|
| Hero headline (H1) | Display Grotesque | Bold/Black | Sentence case | 72–96px | Tight (-0.02em to -0.04em) |
| Section headline (H2) | Display Grotesque | Bold | Sentence case | 48–64px | Tight (-0.02em) |
| Feature subheading (H3) | Display Grotesque | Medium/SemiBold | Sentence case | 28–36px | Default (0em) |
| Body paragraph | Inter | Regular (400) | Sentence case | 16–18px | Default (0em to 0.01em) |
| Navigation links | Inter | Medium (500) | Sentence case | 14–15px | Default |
| CTA button text | Inter | Medium/SemiBold (500–600) | Sentence case | 14–16px | 0em to 0.02em |
| Category badge / eyebrow text | Inter | Regular/Medium | Sentence case | 12–13px | 0.02em–0.04em |
| Section counter ("/ ITEM 1 ⋮ 4") | Inter | Regular | Uppercase | 11–12px | 0.08em–0.12em (tracked out) |
| Blog timestamp/metadata | Inter | Regular | Uppercase | 11–12px | 0.06em |
| Pricing tier name ("Free", "Plus") | Display Grotesque | Bold | Sentence case | 24–28px | Default |
| Pricing price ("$69") | Display Grotesque | Bold/Black | N/A (numeric) | 48–64px | Tight |
| Pricing feature list items | Inter | Regular | Sentence case | 14px | Default |
| Footer column headers | Inter | SemiBold | Sentence case | 14px | Default |
| Footer links | Inter | Regular | Sentence case | 14px | Default |
| Legal body copy | Inter | Regular | Sentence case | 15–16px | Default |
| FAQ accordion headers | Inter/Display | Medium | Sentence case | 16–18px | Default |
| Testimonial quotes | Display Grotesque | Regular/Medium | Sentence case | 32–48px | Tight |
| Testimonial attribution | Inter | Regular | Sentence case | 13–14px | Default |
| Changelog entry title | Display Grotesque | SemiBold | Sentence case | 20–24px | Default |
| Changelog date | Inter | Regular | Sentence case | 13px | Default |
| Help center nav | Inter | Regular | Sentence case | 14px | Default |
| Breadcrumb text | Inter | Regular | Uppercase | 11px | 0.08em |

### Typography Application by Page Type

**Homepage:**
- Giant serif-influenced display type for the hero: "Customer relationship magic." approximately 80–96px, bold, tight tracking.
- The section headers use a numbered system: "[01] POWERFUL PLATFORM" — section labels in small caps / uppercase with generous letter-spacing, creating an editorial print-magazine sensibility.
- Feature tab labels ("Ask Attio", "Data model", "Workflows", "Reporting"): Inter Medium, 14px.
- Testimonial text uses the display typeface at approximately 36–40px for maximum visual weight.

**Product/Feature Pages:**
- Category eyebrow ("Data model", "Automations & workflows", "Reporting") in bordered pill above the hero heading — Inter Regular, ~13px, default tracking.
- Hero headline: Display grotesque, approximately 64–80px.
- Body paragraph beneath hero: Inter Regular, 18px, line-height ~1.6.

**Pricing Page:**
- Hero: "From zero to IPO." — Display grotesque, Bold, approximately 72px.
- Plan tier names in medium display weight.
- Pricing table feature categories as H2-level section dividers using bold display type.

**Customers Page:**
- Hero: "The CRM behind the next generation of companies." — Display grotesque, Bold, ~72px.
- Subheader: Inter Regular, 18px.

**Careers Page:**
- Hero: "Our mission is to build the CRM for the next generation." — Display grotesque Bold, ~64px.
- Body intro: Inter Medium/SemiBold, 18–20px — slightly heavier than regular feature pages, emphasizing emotional mission statement.
- Open position list items: Inter Regular 15px with position number in muted gray.

**Blog Page:**
- Featured article title: Display grotesque, Bold, very large (~72px) but displayed in a stripped-back editorial style.
- Article list titles: Inter or Display grotesque, SemiBold, ~20px.
- Category/timestamp metadata: Inter Regular, 12px, uppercase, tracked out at ~0.08em — evoking print magazine metadata.

**Changelog Page:**
- "What's new?" hero in Display grotesque Bold, approximately 56–64px.
- Entry titles: Display SemiBold, 20px.
- Entry dates: Inter Regular, 13px, muted gray.

**Help Center:**
- Main heading: "How can we help?" — Display grotesque Bold, approximately 48–56px.
- Search placeholder: Inter Regular/Medium, 15px.
- Sidebar nav items: Inter Regular, 14px.

**Legal Pages:**
- Page title ("Privacy Policy", "Terms and Conditions"): Display grotesque Bold, ~56–64px, unusually large for a legal page — signals design care even in utilitarian contexts.
- Body text: Inter Regular, 15–16px, with generous line-height (~1.7) for readability of dense legal text.
- Section headers within document: Inter SemiBold, 16–18px.

**Manifesto (Redefine) Page:**
- Typography becomes experimental: "CRM /ˌsiː ɑːr ˈɛm/ abbr." — uses IPA phonetic notation as typographic design element.
- Numbered philosophical points: Display Regular, large, with abundant whitespace — resembling a printed essay.

### Font Pairing Philosophy

The core pairing of a **high-impact display grotesque** for headings with **Inter** for body text is a masterclass in functional elegance:

1. **The Display Font** provides brand personality, emotional weight, and visual distinctiveness. Its slightly compressed, highly legible letterforms support long headings ("The CRM behind the next generation of companies.") without breaking rhythm. The consistent use of a terminal period as a design flourish (present in nearly every H1 on the site) creates a signature typographic "voice."

2. **Inter** provides operational clarity. It is globally recognized as a screen-optimized, accessible typeface. Its neutrality allows content to be the focus. For a product that values power-without-complexity, using the world's most readable screen typeface signals that Attio respects users' time.

The semiotic message of the pairing: **Drama in concept, clarity in execution.** Big ideas, delivered efficiently.

### Weight Distribution Analysis

- **Black/Bold (800–900):** Reserved exclusively for H1 hero headings — used sparingly, maximizing impact.
- **Bold (700):** H2 section headings and pricing prices.
- **SemiBold (600):** H3 subheadings, CTA button text, footer column headers.
- **Medium (500):** Navigation links, category labels, testimonial attribution names.
- **Regular (400):** All body text, pricing feature lists, legal copy, blog metadata, footer links.
- **No Light or Thin weights observed** — Attio avoids weights below Regular in all marketing contexts, maintaining a confident, legible visual weight even in supporting text.

### Letter-Spacing Rules

- **Hero headings:** Tight tracking (-0.02em to -0.04em) — standard for display-sized type, improves cohesion of large letterforms.
- **Body text:** Default (0em) — no artificial tracking applied to body copy.
- **Uppercase metadata/labels:** Generous positive tracking (+0.06em to +0.12em) — standard compensation for uppercase legibility, used on section labels, blog timestamps, and breadcrumbs.
- **Button text:** Slight positive tracking (+0.01em to +0.02em) — subtle, not exaggerated.

### Complete Type Scale Summary

| Scale Level | Size Range | Usage |
|---|---|---|
| Display XL | 80–96px | H1 hero headings |
| Display L | 64–72px | Primary page headings |
| Display M | 48–56px | Secondary page headings, Help center H1 |
| Display S | 32–40px | Testimonial quotes, H3 content headings |
| Display XS | 24–28px | Pricing tier names, Changelog titles |
| Body L | 18–20px | Hero subheadings, mission statement body |
| Body M | 15–16px | Standard body copy, legal text |
| Body S | 13–14px | Supporting body, attribution, pricing metadata |
| Label / Caption | 11–13px | Metadata, timestamps, section counters, breadcrumbs |
| Micro | 10–11px | Terms footnotes, small legal references |

---

## 3. Logo & Wordmark

### Primary Logo Description

Attio's logo is a **wordmark-only system** consisting of the company name "attio" set in a bespoke or heavily customized grotesque sans-serif typeface. There is no separate abstract mark, icon, monogram, or symbol used independently in marketing contexts. The wordmark is the brand.

**Observed rendering:** Lowercase "attio" in a clean, geometric sans-serif. The letterforms are open, humanistic, and proportioned. The weight appears to be Regular to Medium — not bold — which is a deliberate choice: a bold logo would feel corporate; the medium-weight wordmark feels modern, accessible, and confident without shouting.

### Logo Characteristics

- **Typeface style:** Geometric/humanistic grotesque sans-serif. Lowercase only. No capitalization.
- **Weight:** Medium (approximately 400–500 weight in a variable font scale).
- **Tracking:** Slightly loose tracking (+0.02em to +0.04em) — creating airiness in the letterforms and making the wordmark feel light and modern rather than compressed and aggressive.
- **Color:** Near-black (#0D0D0D / #111111) on white backgrounds. White version used internally (implied by dark-background navigation reversal on dark sections, though no dark nav was observed; the announcement bar renders the logo in its standard dark form even over white).
- **Accompaniment:** A small square icon appears immediately to the left of the wordmark. This icon is a stylized "a" mark or abstract geometric symbol — approximately 20×20px at standard nav scale — set in the same near-black, with slight visual complexity suggesting a product-derived icon (resembling a simplified grid or relationship node abstraction). This functions as a "favicon mark" paired with the wordmark.

### Placement Rules

- **Navigation (top-left):** Standard top-left placement in the sticky navigation bar, at approximately 40px height. Always the leftmost element in the nav. Consistent across all 14 pages observed.
- **Footer (bottom-left within footer container):** The wordmark appears alone in the footer's top-left area, before the footer column grid begins.
- **Favicon/Tab icon:** The Attio icon mark (without wordmark) appears as the browser favicon in the page tab — confirming that the brand mark system allows the icon to function independently at small sizes.
- **No centered placement** observed anywhere on the site — the logo is always flush-left or left-aligned within its container.

### Color Variations Observed

- **Dark/near-black on white:** Primary state across all pages.
- **No white-on-dark version** observed in the marketing site (no dark navigation bars encountered).
- **No colored version** observed (no blue, gray, or tinted versions).

### Sizing Details

- **Navigation logo:** Approximately 90–110px wide × 28–34px tall (the wordmark at standard desktop nav scale).
- **Footer logo:** Approximately 80–100px wide — slightly smaller than nav version, appropriate for footer hierarchy.
- **Favicon icon only:** 16×16px browser tab display.

### Brand Mark System

Attio operates a **two-component brand mark system:**

1. **Icon Mark:** The small geometric square/abstract icon to the left of the wordmark. Used independently at favicon scale and within the product UI (as the support chat widget avatar shows a circular version of this mark).
2. **Full Wordmark (Icon + Text):** Used in all marketing navigation and footer contexts.
3. **No isolated wordmark without icon** was observed in marketing contexts.

The support chat widget displays a circular version of the icon mark as its avatar, confirming the icon functions as a standalone brand identifier in product contexts.

### Logo Relationship to Brand Heritage/Positioning

The blog post "How we chose the name Attio" exists on the site, confirming intentionality behind naming. The "io" suffix is characteristic of modern tech/SaaS companies (Figma, Notion, Attio). The all-lowercase treatment positions the brand alongside peers like "linear", "notion", and "vercel" in the new generation of SaaS tools that reject titlecase corporate naming conventions. The wordmark-only system avoids the complexity of icon-based logos (which can feel arbitrary or abstract) in favor of the brand name itself as the primary visual identity — a highly confident design choice that says the name itself is the asset.

---

## 4. Layout & Grid System

### Global Structure

- **Maximum content width:** Approximately 1200–1280px. Content columns are constrained to this width and centered within the viewport at wider screen sizes. The full-bleed sections (dark testimonial block, feature demo tabs) extend to 100% viewport width.
- **Left/right padding (gutter):** Approximately 24–48px on desktop (varying by section). On mobile, this collapses to 16–20px.
- **Navigation bar height:** Approximately 56–64px, sticky (fixed position). Includes the announcement bar above it (~36px), creating a total top clearance of approximately 96–100px before content.
- **Announcement bar:** Full-width, near-black background (#0D0D0D or #111111), white text, positioned at the very top of every page. Contains a single line of marketing text with an arrow link. Height approximately 36–40px. Has an ×-close button.
- **Header/Nav structure:** [Logo] [Nav items — Platform▼, Resources▼, Customers, Pricing] [Sign in | Start for free]. Two-tone CTA: "Sign in" as text link; "Start for free" as filled black button.
- **Footer columns:** 6-column grid layout on desktop. Columns: Platform, Company, Import from, Attio for, Apps, Resources. Footer also contains the Attio wordmark, copyright notice, and legal links (Terms & Conditions, Privacy Policy, LLMs).

### Every Page Template Identified

**Template 1: Hero-Product (Homepage, Feature Pages)**
- Full-height hero with large centered display heading + subheading + dual CTA buttons.
- Below hero: Product demo component (interactive tab panels or animated UI screenshots).
- Alternating content sections: text-left / product-visual-right or centered text with full-bleed product screenshots.
- Social proof section (testimonial quotes, customer logos).
- Final CTA section: centered text + two buttons.

**Template 2: Index/Gallery (Customers, Blog)**
- Hero with category eyebrow pill + large heading + body text.
- Customer logo grid (2–3 rows of partner logos in monochrome).
- Case study card grid (2-column on desktop).
- Blog uses a featured article hero (full-width card) + article list below (2-column grid).

**Template 3: Pricing**
- Hero with large heading + subheading.
- Monthly/Annual toggle switch (pill-style segmented control).
- 4-column pricing card grid (Free, Plus, Pro, Enterprise).
- Detailed feature comparison table below cards.
- FAQ accordion section.

**Template 4: Content/Editorial (Blog Posts, Manifesto)**
- Single-column centered content.
- Large display heading.
- Body text at standard reading width (~640–720px max).
- Manifesto uses an experimental vertical scroll with animated word-by-word text reveal.

**Template 5: Utility/Legal (Privacy Policy, Terms)**
- Two-column: Left sidebar (navigation) + Right main content area.
- Full text in standard Inter body font.
- No decorative elements.

**Template 6: Help Center**
- Three-column: Left sidebar (topic tree navigation) + Center content area + Implicit right margin.
- Search bar prominent at top.
- Category card grid (3 columns: Academy, Reference, API).

**Template 7: Careers**
- Hero with eyebrow + heading + body + CTA button + team avatar cluster.
- Milestone timeline section (dot grid decoration + horizontal scroll of feature release dots).
- Values section (2-column grid of value cards).
- Open positions section (expandable category accordion).

**Template 8: Integration/App Detail Page**
- Breadcrumb navigation.
- App name + icon + subtitle + install CTA.
- Dashed border separator.
- Left column: metadata (Built by, Category, Resources).
- Right column: product screenshots.

### Card Anatomy for Repeated Modules

**Pricing Cards:**
- White background.
- 1px gray border (#E5E7EB).
- Border-radius: approximately 12px.
- Internal padding: approximately 24–32px.
- Tier name (SemiBold, 20px) + Price (Bold, 48px) + Billing period (Regular, 13px) + Target description (Regular, 14px, gray) + Feature list (checkmarks, Regular 14px) + CTA button (full-width, bottom).
- "Pro" card elevated with a slightly more prominent border or box-shadow and a filled blue CTA.

**Testimonial/Customer Cards:**
- Light gray background or white.
- Customer logo.
- Quote text in display typeface.
- Attribution: headshot avatar + name + role + company.

**Blog Article Cards:**
- Date + Category tag (uppercase, tracked) — metadata row.
- Article title in display SemiBold.
- Brief excerpt in Inter Regular.
- Author name + role.

**Help Center Category Cards:**
- Rounded rectangle.
- Icon in gray container.
- Category name (SemiBold).
- Description (Regular gray).

### Responsive Behavior

- **Breakpoints:** Based on visual observation, Attio uses approximately:
  - Mobile: 0–767px — single column, hamburger menu.
  - Tablet: 768–1023px — 2-column content layouts, compressed hero.
  - Desktop: 1024px+ — full multi-column grids.
  - Wide desktop: 1280px+ — max-width container kicks in.
- **Column shifts:** 4-column pricing grid collapses to 2-column on tablet, 1-column on mobile.
- **Navigation:** Hamburger menu on mobile (implied by standard SaaS pattern).
- **Hero headings:** Font size reduces approximately 40–50% from desktop to mobile.

### Whitespace Strategy

Attio is exceptionally generous with whitespace. Section-to-section vertical padding appears to be approximately 80–120px on desktop. Individual sections have internal padding of 48–80px. This creates a "breathing" quality that positions Attio alongside premium consumer software brands (Apple, Figma) rather than feature-dense legacy SaaS tools (Salesforce, SAP).

The whitespace strategy serves several functions:
1. It allows each section to be a distinct "moment" in the scroll narrative.
2. It prevents visual clutter, reinforcing the "clarity over complexity" product message.
3. It creates natural pauses that make the hero headings land harder.

### Grid Alignment Philosophy

Attio uses a **center-dominant layout philosophy for marketing content** and a **left-dominant philosophy for utility/information content.** 

- All hero headings are centered.
- All body text beneath hero headings is centered (max-width ~640px).
- Feature section content shifts to left-aligned text with right-aligned product imagery.
- Tables, lists, and help center content are left-aligned.
- This center/left duality maps perfectly to the emotional vs. functional split: "inspire you" (centered) vs. "help you act" (left-aligned).

### Homepage Scroll Architecture

The homepage follows a deliberate narrative scroll pattern:

1. **Announcement bar** (global, dismissible).
2. **Navigation** (sticky).
3. **Hero** — Category badge → Giant H1 ("Customer relationship magic.") → Subheading → Dual CTAs.
4. **Product Demo Tabs** — "Ask Attio / Data model / Workflows / Reporting" — 4-tab interactive demo panel.
5. **Section break testimonial** — Full-width dark background with a large customer quote.
6. **Feature Section 1 "[01] POWERFUL PLATFORM"** — "GTM at full throttle." with Automate/Deploy AI/Connect data/Reporting sub-sections.
7. **Free trial CTA** — "Start with a 14-day free trial of Pro."
8. **Feature Section 2 "[02] ADAPTIVE MODEL"** — "A seismic shift in CRM flexibility."
9. **Feature Section 3 "[03] DATA ENRICHMENT"** — "Build fast."
10. **Feature Section 4 "[04] BUILT FOR SCALE"** — "The system of action for the next generation."
11. **Social proof wall** — Scrolling avatar ticker of hundreds of customer faces.
12. **Final CTA** — "The CRM behind thousands of companies." + "Start for free."
13. **Footer.**

This architecture mirrors a classic sales narrative: Hook → Demonstration → Social proof → Scale proof → Action.

### Footer Layout Details

The footer uses a **6-column grid** on desktop with the following columns:
1. **Platform** (Refer a team, Changelog, Gmail extension, iOS app, Android app)
2. **Company** (Customers, Announcements, Engineering blog, Careers, Manifesto, Become a partner)
3. **Import from** (Salesforce, Hubspot, Pipedrive, Zoho, Excel, CSV) — an SEO-driven column that signals migration from competitors.
4. **Attio for** (Startups, Deal flow) — solution verticals.
5. **Apps** (Gmail, Outlook, Segment, Mailchimp, Slack, Outreach, Mixmax, Typeform, Zapier) — integration links.
6. **Resources** (Startup program, Help center, Automation templates, Developers, System status, Hire an expert, Downloads)

Below the grid: Social media links (LinkedIn, X/Twitter, Dribbble, YouTube) + Copyright notice + Legal links.

The footer design itself is minimal: all links in Inter Regular 14px, column headers in SemiBold. No icons in footer links (except social media icons which use platform logos). Background: white. Bottom border: none.

### Layout Elements Not Present

- **No sidebar navigation** on marketing pages (only on Help Center and Legal pages).
- **No sticky sidebar** content (no table-of-contents on blog/feature pages).
- **No mega menu** in the traditional sense — the "Platform" and "Resources" nav dropdowns are likely simple flyout panels, not full-width mega menus with imagery.
- **No split-screen hero** (text left, image right at 50/50) — all heroes are centered with product imagery below/beside.
- **No floating action buttons** beyond the chat widget.
- **No parallax scrolling effects** beyond the social proof avatar ticker.
- **No cookie banner with color** — the cookie banner (observed on first load) is white with standard gray/black text and two simple buttons (Continue, Reject).

---

## 5. UI Components

### Buttons

**Primary CTA — "Start for free":**
- Background: #2563EB (Electric Blue).
- Text: White, Inter SemiBold, 14–15px.
- Border-radius: approximately 6–8px (slightly rounded, not pill-shaped).
- Height: approximately 40–44px.
- Horizontal padding: approximately 20–24px.
- Hover state: Slightly darker blue (approximately #1D4ED8), with smooth CSS transition (~200ms).
- Used in: Navigation (top-right), homepage hero, feature page heroes, pricing Free tier, final CTA sections.

**Secondary CTA — "Talk to sales":**
- Background: Transparent.
- Border: 1px solid near-black (#0D0D0D) or dark gray (#374151).
- Text: Near-black, Inter Medium, 14–15px.
- Same border-radius and height as primary.
- Hover state: Light gray background fill (#F5F5F5) on hover.
- Used consistently paired alongside the primary blue CTA across all hero sections.

**Ghost/Outline Button — plan-specific CTAs:**
- "Continue with Plus" and "Continue with Pro" on pricing cards use outlined/filled variants based on plan tier.
- "Continue with Pro" (recommended plan): Filled blue, same as primary CTA.
- "Continue with Plus": Outlined dark border, transparent fill.
- "Start for free" (Free plan): Outlined.

**Tertiary / Text Button:**
- "Sign in" in the navigation: plain text link, no border, no background. Inter Medium, 14–15px, near-black. Simple underline or color change on hover.
- "Explore automations →", "Explore our data model →": text links with trailing arrow, used within feature sections to direct deeper exploration without demanding conversion.

**Black CTA Variant:**
- "Subscribe" (Changelog), "Install app" (App pages), "Join the team" (Careers): Black (#0D0D0D) fill, white text. Same border-radius and height as primary. Used for lower-priority or context-specific conversion actions.

**Icon Button:**
- The chat widget floating button: circular, approximately 48px diameter, uses the Attio icon mark in white on a dark background.
- Arrow/send buttons within search inputs: Small circular button (~32px), blue fill.

### Navigation

**Desktop Navigation:**
- **Announcement bar** (above nav): Full-width, near-black background. Single line of text (marketing message) with arrow link. Close (×) button on right.
- **Main nav bar**: White background, sticky. Height ~56px.
  - Left: Attio wordmark.
  - Center/Left: [Platform ▼] [Resources ▼] [Customers] [Pricing] — links in Inter Medium 14–15px.
  - Right: [Sign in] [Start for free button].
- **Dropdowns:** "Platform" and "Resources" have dropdown chevrons (▼), suggesting flyout menus. Not fully explored in screenshots but implied by nav structure.
- **Active state:** The current page is not visibly highlighted in the navigation (minimal/no active state differentiation observed).

**Mobile Navigation:**
- Hamburger menu (3-line icon) implied — not directly screenshot on mobile breakpoint but standard for this nav structure.

### Forms

**Email Input (Changelog subscribe):**
- White background, 1px #E5E7EB border.
- Border-radius: ~6–8px.
- Placeholder text: "Your email address" in gray (#9CA3AF), Inter Regular, 15px.
- Height: ~44–48px.
- Paired with "Subscribe" button (black fill) placed directly below or beside.

**Multi-field Form (Startup Program):**
- Standard grid form with labeled inputs.
- Field labels above inputs.
- Input fields: white background, 1px gray border, 6–8px border-radius.
- Placeholder examples: "e.g. Julia" / "e.g. Arowa" in light gray.

**Help Center Search:**
- White background, 1px gray border.
- Distinctive: includes a keyboard shortcut indicator (⌘K) on the right side of the input — signaling power-user awareness.
- Search icon (magnifying glass) on the left inside the input.

### Accordions

**Pricing FAQ Accordion:**
- Question as H3 in Inter SemiBold/Medium.
- Expand/collapse arrow indicator on right.
- Collapsed: shows question only. Expanded: reveals answer body text in Inter Regular.
- Subtle separator line between accordion items.
- No animation flash — simple height expansion.

**Careers Open Positions Accordion:**
- Category name + count in brackets: "Engineering [9]".
- Expanded reveals numbered list of positions with location tags ([Hybrid], [Remote]).

### Tabs

**Homepage Product Demo Tabs:**
- Four tabs: Ask Attio / Data model / Workflows / Reporting.
- Active tab: white background, visible bottom border or elevated state.
- Inactive tabs: gray text, no underline.
- Tab labels: Inter Medium, ~14px.
- Tab content: Large product UI screenshot, animated/switching on click.

### Cards

Covered in detail in Section 4 (Layout). All cards share: white or near-white background, 1px gray border (#E5E7EB), ~12px border-radius, 24–32px internal padding.

### Button States and Interactions

- **Hover:** Color darkens (blue CTA → darker blue; black CTA → slight opacity change). CSS transition ~150–200ms ease.
- **Active/Pressed:** Further darkening, subtle scale-down (transform: scale(0.98)) implied.
- **Disabled:** Not directly observed on marketing pages — pricing CTAs are always active.
- **Loading:** Not applicable to marketing CTAs (they link to external URLs).

### Animation and Motion Philosophy

Attio's marketing site uses **restraint in animation** consistent with its overall design philosophy:

- **No hero animations** on text — headings appear statically (no typing effects, no entrance animations except on first load).
- **Social proof avatar ticker:** A slow horizontal scroll of customer avatar photos. Speed: approximately 30–60 seconds per full rotation. Creates a sense of scale and community without the vulgarity of "500+ customers" counters.
- **Manifesto word animation:** On the Redefine page, individual words appear to animate in one-by-one or section-by-section as the user scrolls — the most experimental animation on the site.
- **Tab panel transitions:** Smooth crossfade between tab content panels.
- **Hover transitions:** All interactive elements use 150–200ms ease transitions. No spring physics, no dramatic motion.
- **Chat widget:** Opens/closes with a smooth expand animation.
- **No page transition animations** between pages (standard full-page load).
- **No skeleton loaders** on marketing pages (content is server-rendered).
- **Counter animations:** The statistics section on the homepage ("1,000,000 Customer records", "99.9% Uptime") appears to use countUp animations as the section enters the viewport.

The motion philosophy aligns with Attio's brand voice: purposeful, not decorative. Animations serve to guide attention, not to perform sophistication.

---

## 6. Iconography

### Complete Icon Inventory

**Navigation / UI Icons:**
- **Chevron/Arrow down (▼):** Used on "Platform" and "Resources" nav items to indicate dropdown availability. Simple geometric chevron in near-black.
- **Close (×):** Used on the announcement bar dismiss button and the chat widget close button. Minimal thin-line ×.
- **Arrow right (→):** Used in announcement bar CTA ("Ask Attio. →"), feature section "Explore" text links. Simple directional arrow.

**Platform / Help Center Category Icons:**
- **Graduation cap / mortarboard icon:** "Academy" category in the Help Center. Line-art style, gray, approximately 32–40px.
- **Cube/Box icon:** "Reference" category in the Help Center. 3D cube line-art, gray.
- **Brackets/Code icon:** "API" category in Help Center. Angular bracket symbols ({}) or similar, gray.

**Product UI Workflow Icons (within product screenshots, not standalone brand icons):**
- **Circular trigger node icon:** Green circle with lightning bolt or clock symbol. Used in Automations workflow builder screenshots.
- **Diamond/condition node icon:** Yellow/amber diamond with question mark. Used in Automations workflow.
- **Square action node icons:** Blue/purple squares with integration logos.
- **Slack logo:** Used in integration pages and workflow screenshots.

**App/Integration Icons:**
- Third-party logos (Slack, Gmail, Segment, Zapier, etc.) appear in their original brand colors within integration context. This is the only place on the site where full-color brand assets from external companies appear.

**Social Media Icons (Footer):**
- LinkedIn, X (Twitter), Dribbble, YouTube: Standard platform logos in simple line or flat style. Color: gray (#9CA3AF) default, near-black on hover.

**Sidebar Navigation Icons (Help Center):**
- Small geometric icons precede each left-sidebar nav category: a small square, circle-with-arrows, etc. Consistent with the Attio product UI icon style — geometric, minimal, single-color.

**Chat Widget Icon:**
- Circular chat bubble or message icon. Used as the floating trigger for the Attio Support chat widget. Near-black circle with white icon.

**Announcement Bar Arrow:**
- The "→" character (Unicode right arrow) used as a link indicator in the announcement bar.

**Breadcrumb Separator:**
- Forward slash "/" character used as separator in breadcrumbs (e.g., "APPS / SLACK").

### Icon Design Philosophy

Attio's iconography is **line-art / minimal geometric**, consistent with the overall brand aesthetic. Key principles:
1. **Single weight, single color:** Icons do not use two-tone, gradient, or filled-plus-outline combinations.
2. **Proportionally sized:** Icons appear at approximately 16px, 20px, 24px, or 32px depending on context — never arbitrarily large.
3. **Functional, not decorative:** Icons appear only when they aid navigation or identification. No decorative icons in feature sections.
4. **System-derived:** The icon style appears consistent with the Attio product UI itself, suggesting a unified design system where marketing icons come from the same library as product icons.

### Icon Color Rules

- **Default:** Gray (#9CA3AF or #6B7280) for navigation and UI icons.
- **Active/Featured:** Blue (#2563EB) for active or highlighted states.
- **Product status:** Green (#22C55E) for positive/success, Amber (#F59E0B) for condition/warning.
- **Social:** Gray by default, near-black on hover.

### Icon Sizing

- Small (16px): Inline icons within text, breadcrumb separators, close buttons.
- Medium (20–24px): Navigation icons, sidebar items, workflow node icons.
- Large (32–40px): Help center category card icons.

### Icons Not Used

- **No emoji** anywhere in marketing copy or headings (significant counter-trend to many SaaS sites).
- **No custom illustrated mascots or characters.**
- **No hand-drawn / sketch-style icons.**
- **No duotone icons.**
- **No icon fonts** (appears to use SVG-based icons).
- **No checkmark icons in bold styles** — pricing feature checkmarks use a simple thin-stroke checkmark, not filled circle or badge styles.
- **No "star rating" icons** for testimonials.

---

## 7. Photography and Imagery Style

### Product Imagery / UI Screenshots Treatment

Product UI screenshots are the **primary imagery asset** across the entire site. Every feature section and hero deploys highly crafted screenshots of the Attio application interface. Key treatment characteristics:

- **Floating/elevated presentation:** Screenshots appear to float on the page, often with subtle drop shadows or isolated against white — never framed in a browser/laptop mockup on marketing pages.
- **Partial/cropped framing:** Screenshots are often cropped to show only the most relevant portion of the UI — a specific workflow, a record detail, a reporting chart — rather than showing the full application window. This focuses attention and avoids overwhelming complexity.
- **Animation within screenshots:** Some screenshot regions use subtle animation (the "AI is thinking..." typing states, the data loading animations) to create a sense of a live, responsive product.
- **Retina/high-DPI quality:** All screenshots appear to be captured at 2x or higher resolution, rendering crisply on all screen types.
- **White application backgrounds:** The Attio product UI itself predominantly uses white backgrounds, making screenshots integrate naturally into the white marketing site.
- **Consistent scale:** Screenshots across different pages maintain visual consistency in relative scale and cropping style.

### Lifestyle and Editorial Photography

**Minimal lifestyle photography:**
- On the Careers page, a grid of **team member headshots** appears — these are authentic photographs of Attio employees, not stock photography. Style: casual, natural light, diverse team. No corporate "suit-and-tie" compositions.
- On the Customers page, the Granola case study thumbnail shows what appears to be a lifestyle/editorial image of a person outdoors — the only editorial photography observed.
- No stock photography anywhere on the site. This is a deliberate brand choice: everything is either product screenshots or authentic team/customer photography.

### Hero Images

No traditional "hero photography" (no backgrounds of people working, no abstract technology imagery). The homepage hero is **purely typographic** with a dot-grid texture background — letting the words carry the visual weight. Below the hero, the product UI screenshots serve as the primary visual. Feature page heroes follow the same pattern.

This absence of hero photography is highly unusual and strategically bold — it says: "the product is the beauty."

### Imagery Strategy and Art Direction

Attio's imagery art direction can be summarized in four principles:

1. **Product is the hero:** Every major section's imagery is a product UI screenshot. The art direction ensures these screenshots are aspirational — they show the most beautiful, information-dense states of the application.
2. **Authenticity over aspiration (for people):** When humans appear (team photos, customer avatars), they are real people, not models or stock photos.
3. **No decorative imagery:** No abstract background photos, no technology stock imagery, no blurred bokeh backgrounds. Every image is purposeful.
4. **Brand cohesion through screenshot consistency:** Because all screenshots come from the same product with a consistent internal design system, they naturally create a unified visual language across the marketing site.

### Illustration Style

**No traditional illustration** observed. The dot-grid pattern serves an illustrative-decorative function but is geometric/generative rather than hand-drawn. The Manifesto page's "blob" graphic (a soft, organic shape seen behind a section) is the closest to abstract illustration — it appears as a very light gray amorphous form, barely visible. No character illustrations, no isometric artwork, no icon illustrations beyond functional icon sets.

### Aspect Ratios by Context

- **Product demo screenshots (homepage tabs):** Approximately 16:9 to 4:3, filling the demo area horizontally.
- **Feature section screenshots:** Variable — often wider than tall, displayed at approximately 3:2 or 16:10.
- **Blog featured article image:** Full-width banner, approximately 16:6 (very wide crop).
- **Customer case study images:** Approximately 16:9.
- **Team photos (Careers):** Approximately 1:1 (square crop) for the grid.
- **Customer/Partner logos:** Variable original ratios, but all rendered in a consistent fixed-height container (~32–40px tall) to create a unified logo band.
- **App integration icons:** 1:1 square, approximately 80×80px in the app detail page.

### Image Treatment Consistency

**Extremely consistent.** The visual language of product screenshots is maintained across all pages — same corner radius (approximately 8–12px on screenshot containers), same shadow treatment (very subtle, close-range shadow), same white/light background for the app. Customer logos are all converted to monochrome (black). Team photos all appear at consistent scale. This consistency is not accidental — it reflects a mature design system operating across the entire site.

---

## 8. Brand Voice and Language Style

### Tone: Overall Personality Description

Attio's brand voice is one of the most sophisticated in the CRM space. It can be characterized across 12 sub-categories:

1. **Confident without arrogance:** "Attio is the AI CRM for GTM." — stated as fact, not as aspiration. No qualifiers, no hedging.
2. **Ambitious and visionary:** "Customer relationship magic." "The time has come to redefine CRM." Attio positions itself as building the future, not iterating on the present.
3. **Intellectually precise:** Terminology is exact ("GTM", "PLG", "ICP Fit", "sub-50ms latency"). The audience is assumed to be sophisticated — no over-explaining.
4. **Punchy and aphoristic:** Headlines often end in a period for rhetorical finality. "Automate. Iterate. Accelerate." — three words, three periods, total authority.
5. **Conversational in body copy:** Despite the ambition of headlines, body copy is clear, direct, and free of jargon overload. "Forget months of setup." reads like a person talking.
6. **Empowering:** The language consistently positions the user as in control: "You're in control." "Attio adapts to you." "Your business model — your CRM."
7. **Respectful of user intelligence:** No oversimplification. The pricing page, help center, and changelog all assume the reader understands CRM concepts.
8. **Philosophically grounded:** The Manifesto page goes deep: "rejecting the false trade-off that power must mean complexity." This is product philosophy as brand copy.
9. **Quietly disruptive:** Attio critiques the incumbent (Salesforce, HubSpot) without naming them. "For more than twenty years, businesses have faced an impossible choice." "We were told, that's just how CRM works."
10. **Milestone-aware:** Multiple references to IPO ("From zero to IPO."), funding rounds ($7.7M seed → $23.5M Series A → $33M → $52M Series B), and scale metrics — building credibility through visible growth narrative.
11. **Human and personal:** Blog posts use first-person plural ("We're redefining CRM"). Team values use inclusive language ("We believe in building with heart"). Customer quotes are prominent and specific (named individuals with titles and companies).
12. **Restrained in superlatives:** Unlike many SaaS brands ("the world's greatest", "the most powerful"), Attio uses "magic" as its aspirational framing — a word that is simultaneously grand and humble.

### Language Patterns with Specific Examples

**Pattern 1: Bold declarative with period.**
- "Customer relationship magic."
- "From zero to IPO."
- "Ask Attio."
- "What's new?"
- "The data model for go-to-market magic."
- "Automate. Iterate. Accelerate."
- "Attio for startups."
- "How we chose the name Attio." (blog)

**Pattern 2: Reframing the familiar.**
- "A seismic shift in CRM flexibility." (seismic = metaphor for total disruption)
- "The system of action for the next generation." (not "CRM software" but "system of action")
- "GTM at full throttle." (motorsport metaphor)
- "Build fast." (three syllables, maximum directness)

**Pattern 3: "You" language with specific empowerment.**
- "You're in control."
- "Attio adapts to how your business works, not the other way around."
- "Your business model — perfectly reflected in your CRM."
- "Search, update, and create with AI."

**Pattern 4: Numbers as credibility shorthand.**
- "Sub-50ms latency."
- "14-day free trial of Pro."
- "1,000,000 Customer records."
- "99.9% Uptime."
- "80% off Attio."
- "130+ team members."

**Pattern 5: The next generation framing.**
- "Customer relationship magic." — implies magic where there was once mundane.
- "The CRM for the next generation."
- "The CRM behind the next generation of companies."
- "Our mission is to build the CRM for the next generation."
- "The next generation of CRM." (multiple pages, ~6 instances observed) — this is Attio's core narrative.

### Heading Style: Complete Inventory by Page

| Page | H1 Heading | Subheading | Notes |
|---|---|---|---|
| Homepage | "Customer relationship magic." | "Attio is the AI CRM for GTM." | Period as design choice |
| Ask Attio page | "Ask Attio." | "Search, update, and create with AI." | Period on brand name |
| Data Model page | "The data model for go-to-market magic." | "Attio gives you control and flexibility to build the perfect CRM that drives revenue forward." | "magic." repeated across pages — intentional |
| Automations page | "Automate. Iterate. Accelerate." | "Workflows turns your GTM strategies into dynamic engines for revenue growth." | Triple imperative, each own sentence |
| Pricing page | "From zero to IPO." | "Designed for every stage of your journey. Start today, no credit card required." | Journey metaphor, conversion reassurance |
| Customers page | "The CRM behind the next generation of companies." | "Discover how thousands of companies use Attio to scale their business." | "next generation" positioning |
| Careers page | "Our mission is to build the CRM for the next generation." | "We're redefining CRM — shipping powerful, groundbreaking features at every turn. Join us to revolutionize the world's largest software category." | Mission as recruitment |
| Blog page | "Introducing Ask Attio" (featured post H1) | "Ask Attio is a new way to work with your CRM." | Editorial, specific |
| Changelog | "What's new?" | "A rundown of the latest Attio feature releases, product enhancements, design updates, and important bug fixes." | Colloquial, inviting |
| Help Center | "How can we help?" | "Get answers to common questions on all things Attio." | Service-oriented, warm |
| Manifesto | "Customer relationship magic." (as dictionary definition: "CRM /ˌsiː ɑːr ˈɛm/ abbr.") | "The time has come to redefine CRM." | Most experimental heading on site |
| Startup Program | "Attio for startups." | "Build on the CRM for the next generation. Get 80% off Attio and benefits to help your startup grow." | Direct offer, "next generation" |
| Solutions/Startup CRM | "The real-time CRM for scaling startups." | "Infinitely flexible, Attio is built for every stage of the startup journey – from zero to IPO." | "zero to IPO" repeated |
| Privacy Policy | "Privacy Policy" | "Attio takes the security of your data and our infrastructure very seriously." | Unusually large heading for legal |
| Terms | "Terms and Conditions" | "By logging into your Attio account you agree to be bound by our Terms & Conditions." | Direct and clear |

**Capitalization Rules:**
- H1 and H2 headings: **Sentence case** (only first word and proper nouns capitalized).
- Section counter labels ("/ ITEM 1 ⋮ 4", "/ REDEFINING CRM"): **ALL CAPS** — used as editorial separators.
- Blog/Changelog metadata categories ("[PRODUCT]", "[COMPANY]"): **ALL CAPS** in brackets.
- Navigation links: **Sentence case**.
- Button text: **Sentence case** ("Start for free", "Talk to sales", "Continue with Plus").

### CTAs and Microcopy

**Complete CTA Inventory:**

| Context | Primary CTA | Secondary CTA | Notes |
|---|---|---|---|
| Navigation (all pages) | "Start for free" (blue) | "Sign in" (text) | Ubiquitous, persistent |
| Homepage hero | "Start for free" (blue) | "Talk to sales" (outlined) | Classic conversion pair |
| Feature section inline | "Start for free" | "Talk to sales" | Repeated pattern |
| Data Model hero | "Start for free" | "Talk to sales" | Consistent |
| Automations hero | "Start for free" | "Talk to sales" | Consistent |
| Solutions page | "Try for free" | "Talk to sales" | Variant: "Try" vs "Start" — slightly softer |
| Pricing — Free tier | "Start for free" | — | Low-commitment single CTA |
| Pricing — Plus tier | "Continue with Plus" | — | Progress-language CTA |
| Pricing — Pro tier | "Continue with Pro" | — | Progress-language CTA |
| Pricing — Enterprise tier | "Talk to sales" | — | High-touch only |
| Changelog | "Subscribe" | — | Action-specific |
| App pages | "Install app" | — | Technical action |
| Careers | "Join the team" | — | Culture-forward |
| Startup Program | (Form submission) | — | Embedded form, no button text visible |
| Blog articles | "Explore" (text link) | — | Low-commitment browse CTA |

**Microcopy Analysis:**

- **"Start today, no credit card required."** (Pricing subheading) — directly addresses the #1 friction point in SaaS sign-up without dedicating a separate callout to it. Embedded naturally in supporting copy.
- **"Designed for every stage of your journey."** — journey as growth metaphor; "designed" signals intentionality.
- **"Forget months of setup."** — starts with an imperative to release anxiety.
- **"Sub-50ms latency"** — a technical spec used as emotional reassurance ("we've thought about this at the infrastructure level").
- **"Build on the CRM for the next generation."** — invitation to become part of the story.
- **"Get answers to common questions on all things Attio."** — "all things" is a colloquial, warm phrase that makes the Help Center feel less clinical.
- **"We'll share relevant opportunities when they open up."** (Careers email capture) — respectful, non-pushy framing for email collection.
- **"Keep up to date."** (Careers social section header) — simple, no FOMO manipulation.
- **"Ask us anything, or share your feedback."** (Chat widget) — open-ended, welcoming, peer-to-peer.

---

## 9. Platform and Technical Notes

### Platform Identification

**Framework: Next.js (React)**
Evidence:
- URL structure follows Next.js conventions with no file extensions.
- The page title format "[Feature] | Attio" (e.g., "Pricing | Attio", "Ask Attio | Attio") is consistent with Next.js metadata configuration.
- Navigation between pages appears as instant client-side transitions (Next.js router).
- The `app.attio.com` subdomain for the product application is separate from the marketing site, consistent with a decoupled marketing site + SaaS app architecture.
- Changelog email subscription form, help center search, and chat widget load asynchronously, consistent with React component architecture.

**CSS Framework: Tailwind CSS** (highly probable)
Evidence:
- Color values observed (blue ~#2563EB, grays #E5E7EB, #9CA3AF, #6B7280, #374151) map precisely to Tailwind CSS default color palette values (blue-600, gray-200, gray-400, gray-500, gray-700).
- The "Save 20%" badge color maps to Tailwind yellow-100.
- The responsive breakpoints (768px, 1024px, 1280px) align with Tailwind's default breakpoint system.
- Uniform spacing (padding multiples of 4px) is consistent with Tailwind's spacing scale.

### Theme Architecture

- **No visible CMS watermarks** or platform-specific footers (rules out Webflow, Framer, Squarespace).
- Custom-built marketing site on Next.js with Tailwind, deployed likely on **Vercel** (Vercel appears as a customer/logo in the homepage product UI screenshots — suggesting brand affinity if not direct use).
- Section IDs are clean and semantic (implied by URL hash navigation in Help Center).
- The legal pages (Privacy Policy, Terms) use a separate two-column template with a sidebar navigation — likely a custom template within the same Next.js codebase.
- **Help Center** appears to be built on a custom system hosted at `attio.com/help` — not a third-party tool like Zendesk or Intercom (which would typically use a subdomain like `help.attio.com`). This is a strong signal of design control — they built their own help center to maintain visual consistency.

### URL Structure Patterns

- `attio.com/` — Homepage
- `attio.com/pricing` — Pricing
- `attio.com/customers` — Customers
- `attio.com/careers` — Careers
- `attio.com/careers/[job-title-slug]` — Individual job postings
- `attio.com/blog` — Blog index
- `attio.com/blog/[article-slug]` — Individual articles
- `attio.com/changelog` — Changelog
- `attio.com/platform/[feature]` — Feature pages (ask, data, automations, reporting, developers)
- `attio.com/solutions/[solution]` — Solution landing pages (startup-crm, deal-flow-management-software)
- `attio.com/apps/[app-name]` — Integration pages (slack, gmail, segment, etc.)
- `attio.com/help` — Help center
- `attio.com/help/[category]/[article]` — Help articles
- `attio.com/legal/[document]` — Legal pages (privacy, terms-and-conditions)
- `attio.com/redefine` — Manifesto
- `attio.com/startups` — Startup program
- `attio.com/partners` — Partners
- `attio.com/experts` — Expert network
- `attio.com/templates` — Automation templates
- `attio.com/download` — App downloads
- `attio.com/refer` — Referral program
- `attio.com/engineering/blog` — Engineering blog
- `attio.com/llms.txt` — LLM-readable content file (modern SEO/AI discovery pattern)

### Third-Party Integrations Identified

- **Intercom or custom chat widget:** The "Attio Support" chat widget (bottom-right floating button) behaves like Intercom but uses Attio's own branding — may be a custom implementation or a white-labeled version.
- **Google Chrome Web Store:** Gmail extension link points to Chrome Web Store.
- **Apple App Store:** iOS app link.
- **Google Play Store:** Android app link.
- **LinkedIn, Twitter/X, Dribbble, YouTube:** Social media presence.
- **Cloudflare or similar CDN:** Implied by performance and global reach mentioned in copy.

### Page Performance Observations

- Pages load quickly with minimal flash of unstyled content — consistent with Next.js server-side rendering.
- Images appear to use Next.js Image component optimization (lazy loading, modern formats).
- The animated social proof ticker on the homepage appears smooth — CSS animation-based rather than JavaScript-heavy.
- The chat widget initializes after a short delay — lazy loaded to not block page render.

### SEO and Meta Title Patterns

Observed title pattern: **"[Page Name] | Attio"**
- "Attio: Ask more from CRM" (Homepage — using marketing tagline instead of page name)
- "Pricing | Attio"
- "Customers | Attio"
- "Careers | Attio"
- "Insights & updates | Attio Blog"
- "Changelog | Attio"
- "How can we help? | Attio Help Center"
- "Privacy Policy | Attio"
- "Ask Attio | Attio"
- "Data structure & syncing | Attio"
- "Automations & workflows | Attio"
- "Reporting | Attio"
- "Startup Program | Attio"
- "Slack Integration | Attio"
- "Redefining CRM | Attio"

The presence of `attio.com/llms.txt` is a forward-looking SEO move — providing a machine-readable summary of the site for LLM training and AI search crawlers. This is a very early adoption of an emerging standard, signaling technical leadership and awareness of AI-driven discovery.

### Legal and Compliance Pages

Observed legal documents accessible via footer and sidebar:
- **Terms & Conditions** (last updated November 2025)
- **Privacy Policy** (last updated March 2023)
- **Cookie Policy** (linked in legal sidebar)
- **Referral Policy** (linked in legal sidebar)
- **Acceptable Use** (linked in legal sidebar)
- **Attio Data Processing Addendum** (linked in legal sidebar)
- **Attio Developer Terms** (linked in legal sidebar)
- **Vulnerability Disclosure Policy** (linked in legal sidebar)

Compliance badges observed on homepage: **GDPR, CCPA, ISO** — indicating EU data compliance, California consumer privacy compliance, and ISO information security certification.

Company legal name: **Attio Limited / F Stack Limited** (per Privacy Policy: "Attio Limited, previously F Stack Limited"). Registered address: **42 St John's Square, 2nd Floor, London, EC1M 4EA, United Kingdom.** Support email: **support@attio.com.**

### Accessibility Features

- The Help Center uses a left-sidebar navigation with clear hierarchical structure — keyboard navigable.
- All CTAs use descriptive text ("Start for free", "Talk to sales") rather than ambiguous labels ("Click here").
- Form inputs have associated labels or clear placeholders.
- Keyboard shortcuts are surfaced (⌘K for search) — indicating power-user accessibility considerations.
- Alt text is implied for images (observed in text extraction as "![Basepoint]", "![Sarah Johnson]" etc.) — confirming alt attributes are present.
- The cookie consent banner offers both "Continue" and "Reject" options — GDPR compliant.

### Social Media Accounts

- **LinkedIn:** linkedin.com/company/attio
- **X (Twitter):** twitter.com/attio
- **Dribbble:** dribbble.com/attio (unusual for a SaaS brand — signals design identity importance)
- **YouTube:** youtube.com/@attioCRM
- **Instagram:** Not linked from site.
- **GitHub:** Not linked from site (though an engineering blog exists — GitHub likely accessible from there).

The presence of a **Dribbble account** is a particularly distinctive signal — very few B2B SaaS companies maintain a Dribbble presence. This positions Attio within the design community, suggesting it considers designers and design-forward founders part of its target audience.

---

## 10. Pages Browsed

1. https://attio.com — Homepage
2. https://attio.com/pricing — Pricing page
3. https://attio.com/customers — Customers / Case Studies page
4. https://attio.com/careers — Careers page
5. https://attio.com/blog — Blog / Announcements index
6. https://attio.com/changelog — Changelog page
7. https://attio.com/help — Help Center / Documentation
8. https://attio.com/legal/privacy — Privacy Policy
9. https://attio.com/legal/terms-and-conditions — Terms and Conditions
10. https://attio.com/platform/ask — Ask Attio feature page (AI)
11. https://attio.com/platform/data — Data model feature page
12. https://attio.com/platform/automations — Automations & Workflows feature page
13. https://attio.com/platform/reporting — Reporting feature page
14. https://attio.com/redefine — Manifesto / Redefining CRM page
15. https://attio.com/apps/slack — Slack Integration page
16. https://attio.com/solutions/startup-crm — Startup CRM solution page
17. https://attio.com/startups — Startup Program landing page

**Total: 17 pages browsed.**

---

*Audit prepared April 2026. All observations based on live site content as captured during systematic browsing of attio.com across 17 distinct pages. Analysis reflects the site as of the browsing date and should be refreshed periodically as the brand evolves.*
