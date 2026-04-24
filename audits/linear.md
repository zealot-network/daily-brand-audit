# Linear Brand Standards Audit -- extracted from https://linear.app across 14 pages (April 2026)

---

## 1. Color Palette

### Official Brand Colors (from linear.app/brand)

Linear's brand guidelines name only two official primary brand colors:

| Name | Hex | RGB | Role |
|---|---|---|---|
| **Mercury White** | `#F4F5F8` | RGB 244, 245, 248 | Primary light/background, wordmark on dark |
| **Nordic Gray** | `#222326` | RGB 35, 35, 38 | Primary dark/background, wordmark on light |

The brand page states verbatim: *"Comfortable against light and dark backgrounds, Linear's primary brand color is a subtle desaturated blue. The following light and dark accents are preferred for monochrome wordmark usage, while the brand color is typically reserved for backgrounds."*

### Extended Site Color Palette (observed across all pages)

From visual inspection of the rendered site and DOM:

| Usage Context | Approximate Hex | Description |
|---|---|---|
| Page background (all marketing pages) | `#0a0a0b` – `#0d0d0f` | Near-black, slightly warm. The darkest UI surface, the dominant background color across the entire site. Appears as a true dark charcoal with minimal warmth |
| Navigation bar background | `#0a0a0b` / transparent | Matches page background; no distinct nav bar color |
| Body text (primary) | `#ffffff` / `#F4F5F8` | Pure white to off-white for main headings and body copy on dark backgrounds |
| Body text (secondary/muted) | `#8a8a9a` – `#999aab` | Muted mid-gray used for subtitles, metadata (bylines, dates), captions |
| CTA button background — primary ("Sign up") | `#ffffff` | White button with dark text on dark background — inverse of the page |
| CTA button text (primary) | `#0a0a0b` | Near-black text on white CTA |
| CTA button background — secondary ("Contact sales", "Get started") | `rgba(255,255,255,0.08)` – `rgba(255,255,255,0.12)` | Ghost/outline button with subtle white tint |
| CTA button border (secondary) | `rgba(255,255,255,0.15)` | Very subtle white border on ghost buttons |
| Card/module background | `#13131a` – `#161618` | Slightly lighter than page background, used for feature cards, customer story cards, pricing cards |
| Card border | `rgba(255,255,255,0.06)` – `rgba(255,255,255,0.1)` | Hairline white-alpha borders on cards |
| Accent / AI era indicator dot | `#5E6AD2` | A muted indigo/periwinkle blue — used sparingly for status dots (e.g., the live "Issue tracking is dead" indicator on homepage), active toggles, and priority/progress indicators in UI mockups |
| Toggle switch active state | `#5E6AD2` | Same indigo accent as above — the "Billed yearly" toggles on pricing page |
| Green (In Progress / Done status) | `#26b05e` | Seen in issue status badges within UI mockups |
| Orange/amber (priority label) | `#f0a030` | Seen on "High" priority label in mockups |
| Red (urgent/bug) | `#e5484d` | Seen on bug labels and blocking states in UI mockups |
| Border/separator (subtle) | `rgba(255,255,255,0.05)` | Used for horizontal rules, dividers |
| Footer background | matches page background `#0a0a0b` | No distinct footer background — continuous dark field |
| Link color (in-body) | `#5E6AD2` – `#6872d9` | Same indigo family for hyperlinks within body prose |
| Hover state (nav links) | `#ffffff` from `#aaaabb` | Nav links lighten to white on hover |
| Breadcrumb/label text | `#6a6a7a` | Used for small label tags like "THE LINEAR METHOD", "Brand", "Security" above headings |
| Code / monospace background | `#1a1b1f` | Subtle elevated surface for inline code tags (like `vehicle_state`) |

### Palette Strategy Analysis

Linear's color palette is one of the most restrained in contemporary SaaS design. The philosophy is **chromatic minimalism in service of product clarity**. The near-black backgrounds (`#0a0a0b`) are marginally warmer than pure black (`#000000`), creating a velvet-like quality that feels premium without the coldness of OLED black. The only true chromatic color in the entire UI — the indigo accent `#5E6AD2` — is used with extreme parsimony, appearing only where state communication is essential.

This is a deliberate anti-exuberance stance: no gradients, no color washes, no colorful CTAs. The "color" of the brand *is* the darkness — with Mercury White as its counterpart. The single-accent approach communicates technical precision and confidence; the product's power comes from its capabilities, not visual persuasion through color.

The muted indigo was chosen carefully: it reads as neither purple nor blue, referencing the coolness of engineering software without the aggression of primary blue. It registers as an active state, not a brand color — a crucial distinction.

### Color Application by Page Type

**Homepage:** Near-black background `#0a0a0b` with white type. Product UI mockup sections introduce the broader extended palette (blues, greens, ambers from within the app). CTA section at bottom uses white "Get started" button and ghost "Contact sales" button. The hero section is the only place true white type exists at headline scale.

**Customers Page:** Identical dark background. Customer story cards use the `#13131a` elevated surface. Customer logo marks (Coinbase, OpenAI, etc.) appear in white/light monochrome against the dark cards, maintaining strict palette discipline.

**Pricing Page:** The four pricing tiers (Free, Basic, Business, Enterprise) all appear on the same dark background. Toggle switches for "Billed yearly" use the indigo `#5E6AD2`. Checkmark icons for feature lists are white. No color differentiation between tiers — all treated equally in the visual hierarchy, with typography doing the heavy lifting of distinction.

**Editorial/Blog (Now page):** Dark background continues. Article card thumbnails carry the only significant color variation — editorial images (like the Coinbase "C" logo card) bring external brand colors into the palette. Typography is entirely white/off-white.

**Method page:** The hero shows a large serif display typeface against the near-black background. The only color deviation is the brand-page-specific deep dark charcoal, warmer still than homepage — perhaps `#0d0c0b`.

**Security page:** Dark background. Certification badges (SOC2, GDPR, HIPAA) rendered in a very dark gray/charcoal color, almost camouflaged — a deliberate choice to show security as inherent, not marketed.

**Contact page:** Same dark background. Two card components use elevated dark surfaces. The email link `hello@linear.app` appears with the indigo underline.

**Footer (all pages):** Five-column grid on the same dark background. Footer link text is muted gray (`#666674`), lightening to white on hover. Footer logo uses the Mercury White mark.

### Color Hierarchy & Emotional Role

1. **Near-black background** — establishes seriousness, focus, premium positioning. Signals "this is a tool, not a toy."
2. **Mercury White** — purity, precision, the "result" of good software. White text on black connotes a terminal/code aesthetic.
3. **Nordic Gray** — the inverse world (light mode app UI, brand assets on white). Warm charcoal rather than cold black.
4. **Indigo `#5E6AD2`** — the only "alive" color. Signals state, action, progress. Feels technical without being corporate blue.
5. **Status greens/reds/ambers** — exist only within UI mockups to show the product, not to brand the site. Deliberately quarantined.

### Colors Deliberately Absent

- **Warm brand colors** (orange, yellow, teal, coral): Absent. No emotional warmth, no consumer-software friendliness.
- **Gradient backgrounds**: Completely absent from all marketing pages. Many SaaS brands use purple-to-blue gradients; Linear uses none.
- **Photography color-grading overlays**: Not present — images are used as-is with no tinting.
- **Brand blue (primary)**: Classic corporate navy/blue avoided — indigo occupies a subtler, more sophisticated position.
- **Green as brand color**: Green exists only as a status indicator in the product UI — never as a brand or CTA color.
- **White backgrounds**: No marketing page uses a light/white background. The entire marketing site is dark-first.
- **Colored section dividers or background banding**: Absent. No alternating white/gray sections as seen in traditional SaaS sites.

---

## 2. Typography

### Font Families Identified

**1. Inter (or custom "Linear" variant of Inter)**
- The primary sans-serif typeface used throughout all marketing pages
- Closest match: Inter by Rasmus Andersson (widely used in SaaS, but Linear's use is exemplary of best practice)
- Used for: navigation, body copy, pricing tables, card text, footer, form labels, CTAs, metadata
- Weights observed: Regular (400), Medium (500), Semibold (600)

**2. A Custom or Licensed Serif Display Typeface**
- Observed exclusively on the **Method page** for the massive hero heading "Practices for building"
- Characteristics: High-contrast thick/thin strokes, classical proportions, high x-height, strong serifs
- Closest match: Appears to be **Freight Display Pro**, **Canela**, **Chronicle Display**, or a similar editorial serif. The letterforms suggest it could be **Noe Display** or a custom commissioned serif.
- Used exclusively at display size — this is a design statement, not a body serif
- Creates a deliberate tension: the discipline page uses the most expressive typography on the site

**3. Monospace / Code Font**
- Used within UI mockups showing code (HomeScreen.tsx, bash commands on changelog pages)
- Closest match: **JetBrains Mono** or **Fira Code** — standard developer monospace
- Also used for inline code tags like `vehicle_state` in editorial content

### Complete Font Usage Map

| Element | Font Family | Weight | Case | Approx Size | Letter-spacing |
|---|---|---|---|---|---|
| Main hero H1 (homepage) | Inter | 500–600 | Sentence case | ~72–96px / clamp fluid | Tight, ~-0.02em |
| Section H2 headings | Inter | 500–600 | Sentence case | ~48–64px | Tight, ~-0.02em |
| Section H3 sub-headings | Inter | 500 | Sentence case | ~28–36px | -0.01em |
| Method page hero display | Serif display | 400 (regular) | Sentence case | ~120–160px fluid | -0.03em or tighter |
| Navigation links | Inter | 400–500 | Sentence case | 15–16px | Normal (0) |
| Body/paragraph text | Inter | 400 | Sentence case | 17–18px | 0 |
| Subheadline/lead paragraphs | Inter | 400 | Sentence case | 19–22px | -0.01em |
| Card title text | Inter | 500–600 | Sentence case | 18–22px | -0.01em |
| Card body text | Inter | 400 | Sentence case | 14–15px | 0 |
| Pricing tier name ("Free", "Basic") | Inter | 600 | Sentence case | 22–24px | 0 |
| Pricing price ($0, $10) | Inter | 600–700 | — | 40–48px | -0.02em |
| Pricing feature list items | Inter | 400 | Sentence case | 14–15px | 0 |
| CTA button text ("Get started", "Sign up") | Inter | 500–600 | Sentence case | 14–16px | 0 to +0.01em |
| Footer category headers | Inter | 600 | Sentence case | 12–13px | +0.03em to +0.05em (tracked out) |
| Footer link text | Inter | 400 | Sentence case | 13–14px | 0 |
| Label/eyebrow text ("THE LINEAR METHOD", "Brand") | Inter | 500–600 | ALL CAPS | 11–13px | +0.08em to +0.12em (wide tracking) |
| Blog post date/metadata | Inter | 400 | Sentence case | 12–14px | 0 |
| Blog post author | Inter | 500 | Sentence case | 13–14px | 0 |
| Inline code (`vehicle_state`) | JetBrains Mono / monospace | 400 | lowercase | 13–14px | 0 |
| Quote attribution ("Gabriel Peal · OpenAI") | Inter | 400–500 | Sentence case | 14–15px | 0 |
| Section number labels ("FIG 0.2") | Inter | 600 | ALL CAPS | 11px | +0.1em |

### Typography Application by Page Type

**Homepage:** The H1 "The product development system for teams and agents" is the largest typographic moment on the site (~72–96px fluid, Inter Medium-Semibold, tight tracking). Section headings ("Make product operations self-driving", "Define the product direction") step down to ~48–56px. Feature section labels ("FIG 0.2") are 11px ALL CAPS Inter with very wide tracking — functioning as chapter markers. Customer quotes appear at ~18px italic-weight (though Inter is not italic here — weight signals the quote). The quotation marks themselves are typographically generous.

**Customers page:** H1 at display scale, "Meet the teams who build the future" spanning two lines, creating a visual mass. Sub-heading paragraph in Inter 400 at ~18–20px. "Make the switch →" is a text-link CTA in Inter with an arrow glyph.

**Pricing page:** "Pricing" H1 at ~56px Inter Semibold. Tier names at ~24px. Pricing numbers at ~44px with "per user/month" at 15px reducing the price to its functional information. Feature list items are tightest type on the page at 14px.

**Method page:** This page is typographically the most bold on the site. The serif display headline ("Practices for building") takes up nearly the full viewport — approximately 120–160px at desktop. Below, the body text is Inter 400 at ~18px in a centered, relatively narrow column. The contrast between the monumental serif display and the quiet Inter body creates maximum tension and authority. This is the page that signals "we take ideas about software craft seriously."

**Blog/Now/Editorial:** Article titles at ~40–56px Inter Medium. Breadcrumb navigation ("Now / Craft") in 13px with separator. Body prose in Inter 400 at ~17–18px with generous line height (~1.6–1.7). Author + date metadata at 13px muted gray. Image captions in ~13px italic-ish weight. Section H2s within articles at ~28–32px Inter Semibold.

**Contact page:** H1 "How can we help?" at ~64–80px — one of the more expressive typographic moments on utility pages. Section headers ("Sales", "Help & support", "Join the community") at ~20–22px Inter Medium.

**Security page:** "Safe, secure, and private." styled as a multi-line display statement at ~72–96px — continues the pattern of security/trust pages getting powerful typographic treatment to communicate confidence.

**Careers page:** "Help us craft high-quality tools" at ~72px, two lines, left-aligned.

**Brand page:** "Linear Brand Guidelines" at ~48px Inter Medium. Section labels ("Naming", "Usage", "Colors") at ~24px Semibold. Body prose in Inter 400 at ~16–18px.

### Font Pairing Philosophy

The pairing of **Inter** (the world's most refined UI sans-serif) with a **classical editorial serif display** (Method page) is a semiotic statement about Linear's duality: it is both a precision engineering tool and a company with philosophical depth about craft. The serif appears only on the Method page — the most ideological page on the site — signaling that this is not a decorative choice but a contextual one. The rest of the site uses Inter exclusively, which itself is not a "generic" choice: Inter was specifically designed for screen legibility at small sizes, making every character in every UI component function at its best. Using the same font for marketing as for product UI creates seamless continuity — you're reading the brand in the same voice as the app.

The monospace font for code elements isn't decorative; it's functional proof. When Linear shows code on its marketing pages, it uses real monospace — treating code as evidence, not decoration.

### Weight Distribution Analysis

- **400 (Regular):** Body text, paragraph prose, navigation links, footer links, metadata, pricing feature lists
- **500 (Medium):** Lead paragraphs, navigation (semi-active state), card titles, CTA text, some headings
- **600 (Semibold):** Major section headings, pricing tier names, footer category headers, eyebrow labels
- **700 (Bold):** Rarely observed on marketing pages — when pricing numbers appear very large they may be 700, but the system generally avoids heavy bold in favor of size + weight combinations

The **absence of 700/800/900 weights** across the marketing site is notable. Linear achieves visual hierarchy through scale and spacing rather than weight extremes. This creates a more sophisticated, less shouty aesthetic than competitors who rely on heavy bold headings.

### Letter-spacing Rules

- **Display headings (>60px):** Tight tracking, approximately -0.02em to -0.03em
- **Mid-scale headings (28–60px):** -0.01em to -0.02em
- **Body text (16–22px):** 0 (normal)
- **Small/label text (<14px):** 0 to +0.01em
- **ALL CAPS eyebrow labels:** Wide tracking +0.06em to +0.12em — standard technique to improve readability of small caps

### Complete Type Scale

Approximate distinct sizes observed across all pages:
- 11px — figure labels, metadata minimal
- 12px — smallest legal/footer text
- 13–14px — card body, feature lists, nav secondary
- 15–16px — nav primary, form labels
- 17–18px — body prose (standard)
- 19–22px — lead paragraphs, sub-headings
- 24px — pricing tier names, smaller H3s
- 28–32px — editorial article sub-headings
- 36–40px — blog post titles, pricing prices
- 48–56px — section H1s (Pricing, Contact, Brand pages)
- 64–80px — homepage H2 section starts, Contact H1
- 72–96px — homepage hero H1, hero headings
- 120–160px — Method page serif display (the largest typographic element on the site)

---

## 3. Logo & Wordmark

### Primary Logo Description

Linear uses a **combined lockup** of logomark + wordmark reading "Linear" in white on the dark background. The logo appears at the top-left of the navigation bar across every page.

**Logomark (Symbol):** An abstract, stylized multi-layered triangular/circular form that suggests the letter "L" abstracted through a 3D geometric lens. It appears as a faceted shape — somewhat like a sliced sphere or geodesic form with internal geometric subdivisions. The mark has a distinctly technical, architectural quality: it suggests precision, dimensionality, and motion (the "linear" quality of directed movement). At small sizes it reads as a sophisticated monogram. The mark is rendered in white or Mercury White (`#F4F5F8`).

**Wordmark:** The word "Linear" in a clean, geometric sans-serif — closely matching Inter but with potential custom optical adjustments. The letterforms are open, confident, and unpretentious. No special effects, no gradient fill. Set in approximately 15–17px at nav size, white on dark.

### Logo Characteristics

- **Typeface style:** Geometric sans-serif, optically balanced for web/screen contexts
- **Weight:** Medium (500) — neither light nor bold, reflecting the brand's neutral confidence
- **Tracking:** Slightly looser than default Inter tracking, perhaps +0.01em to +0.02em to give the wordmark breathing room at nav scale
- **Case:** Title case — "Linear" with capital L, lowercase remainder. The brand guidelines are explicit: always capitalize "L" and never abbreviate to "Linear app"

### Placement Rules

- **Position:** Top-left, aligned to the left margin of the navigation container across all pages
- **Flanking elements:** On the right side of the nav, five main navigation links (Product, Resources, Customers, Pricing, Now, Contact), a separator pipe character, then "Log in" (ghost text link) and "Sign up" (white button)
- **Alignment:** The logomark and wordmark are vertically centered in the nav bar
- **Spacing:** Generous padding around the lockup; the logo is not crowded by nav elements
- **Footer:** Only the logomark (symbol alone, no wordmark) appears in the footer, centered in the leftmost column — a confident statement that the mark alone is sufficient for recognition

### Color Variations Observed

- **White (Mercury White `#F4F5F8`):** Primary usage across entire dark-background site — all pages use white mark on dark nav
- **Dark (Nordic Gray `#222326`):** For use on light backgrounds — not seen in the marketing site itself (all pages dark) but documented in brand guidelines as the preferred inverse version
- **Monochrome only:** The brand guidelines explicitly state light and dark accents are "preferred for monochrome wordmark usage" — no color logo variant is shown

### Sizing Details

- **Navigation bar:** Logomark approximately 20–24px tall, wordmark approximately 15–17px text size (total lockup width ~90–100px)
- **Footer:** Logomark symbol only, approximately 28–32px — slightly larger than nav to assert brand identity as a standalone mark
- **Brand guidelines page:** Shows the wordmark in a generous "breathing space" format demonstrating correct whitespace proportions

### Brand Mark System

Linear operates a **three-tier mark system** as documented on linear.app/brand:
1. **Wordmark** — "Linear" typeset in full, for primary communications and contexts with sufficient space
2. **Logo (Logomark + Wordmark lockup)** — for tight layouts, logo grids, co-branding
3. **Icon** — the symbol alone, "for social media or where a 'chip' design is required" — the rounded-square app icon format

This three-tier approach reflects mature brand architecture thinking: context-appropriate representation at every scale.

### Logo Relationship to Brand Heritage/Positioning

The logomark's geometric complexity (multi-faceted 3D form) references the sophistication of the product itself — a tool built for complex systems. The name "Linear" evokes directed, purposeful movement from point A to point B — cutting through the noise of chaotic software development. The mark, paradoxically, is non-linear (complex, faceted) which creates an interesting tension: the brand name is an aspiration (linear workflows), while the mark represents the reality (complex systems made navigable). This is a sophisticated brand positioning move. The visual language of the mark connects Linear to the tradition of precision instrument brands and aerospace design — Vitra, Apple, IDEO — rather than to consumer SaaS playfulness.

---

## 4. Layout & Grid System

### Global Structure

- **Max content width:** Approximately 1280–1440px, with generous inner padding. Navigation likely constrained to 1280px max.
- **Outer page margins:** ~80–120px at desktop, scaling down to ~24–32px on mobile
- **Navigation bar height:** ~56–64px, fixed/sticky at top
- **Section vertical padding:** Varies by content type — hero sections use ~120–160px top padding, standard content sections use ~80–100px vertical spacing
- **Column gap (cards):** ~24px between cards in two-up and four-up grids
- **Footer structure:** Five columns — Product, Features, Company, Resources, Connect — with horizontal rule above and privacy/terms links below

### Page Template Inventory

**Homepage:** Full-bleed dark background. Hero = 100vh with centered large text + floating UI mockup screenshot below fold. Subsequent sections alternate between: left-aligned heading + right/below interactive mockup. Feature "chapters" numbered 1.0–5.0 (Intake, Plan, Build, Diffs, Monitor) with expandable sub-feature labels. Changelog strip (horizontal card scroll). Customer quote strip. Final CTA section. Total scroll depth: ~15–20 viewport heights of content. The homepage is structured as a **narrative scroll architecture** — chapter by chapter telling the product story.

**Customers page:** Hero with large centered heading. Two-column grid of customer story cards below. Cards include: customer logo, illustrative graphic background, headline, "Read story" link. Cards have equal height and consistent padding.

**Pricing page:** Single-column hero ("Pricing"). Four-column pricing table (Free / Basic / Business / Enterprise) with feature toggle above. Each column has: tier name, price, billing toggle, feature list with checkmarks. Below the table (implied from scroll): FAQ section.

**Blog/Now page:** Two-column card grid for featured articles. Cards contain: thumbnail image (16:9 approximate ratio), category label + date, headline, excerpt. Sub-section for Changelog (with date + title + description, horizontal list). Below: Press section.

**Editorial (Article) page:** Narrow single-column content column (~680–720px wide), centered. Breadcrumb navigation top. Large hero image full-width. Author + date below image. Body prose follows. In-article images are full-width of the content column. Author attribution repeated at bottom.

**Contact page:** Centered hero text. Two-column card layout (Sales | Help & Support). Below: two-column info layout (Join community | General communication). Very sparse, functional.

**Security page:** Centered hero text. Certification badge strip (SOC2, GDPR, HIPAA). Feature list below in a grid.

**Brand page:** Centered single-column content layout. Sections for Naming, Usage, Wordmark, Logo, Icon, Colors — each with heading and description. Color swatches shown as large rectangular cards side-by-side.

**Careers page:** Left-aligned hero text with full-bleed photography below. Team values and open roles sections below.

**Method page:** Full-viewport hero with massive serif display type, centered. The visual graphic (abstract circular/line art) fills the viewport. Below: longform text sections.

**Enterprise page:** Centered hero, product screenshot mockup, feature grid.

**Integrations page:** Left sidebar filter (category list), right content grid of integration cards.

### Product Card Anatomy (Customer Story Cards, Integration Cards)

- **Container:** Dark elevated surface (~`#13131a`), subtle border, 8–12px border radius
- **Image area:** Top ~50% of card, fills full width, no border radius on image itself within rounded card
- **Customer logo:** Small icon/symbol, top-left overlay on image, in a slightly darker rounded square chip
- **Headline:** Inter Semibold, 2–3 lines, ~20–24px, white
- **CTA:** "Read story" text link in muted gray with no underline — understated but functional
- **Hover behavior:** Subtle border brightening or card lift — not a heavy shadow, consistent with the minimal aesthetic
- **No price information** on card-type components (this is B2B SaaS, not e-commerce)

### Responsive Behavior

- Desktop (1280px+): Five-column footer, two–four column card grids, wide nav with all items visible
- Tablet (~768–1024px): Two-column card grids, footer collapses to 2–3 columns
- Mobile (<768px): Single-column stacking, hamburger menu (implied), cards stack vertically, footer collapses to single column accordion
- Hero headlines use fluid type (`clamp()` is standard for this design system)
- Navigation: full desktop nav condensed to menu toggle on mobile

### Whitespace Strategy

Linear's whitespace is **architecturally generous**. The near-black background allows whitespace to be expressed through the darkness itself — empty dark space is not "empty" but rather a compositional element. Sections breathe with ~80–120px vertical gaps. Within cards, padding is ~24–32px. This generosity signals premium SaaS — the contrast with Jira or Asana's information-dense interfaces is the point.

The deliberate use of whitespace around the logo (documented in brand guidelines: "give them room to breathe") extends to the entire site. Nothing competes for attention that hasn't earned it — a phrase from their own design refresh blog post.

### Grid Alignment Philosophy

Left-aligned body content, center-aligned hero sections. The navigation is left/right split (logo left, nav links centered-right). Feature sections alternate between centered intro text and offset/asymmetric mockup positioning — creating visual rhythm that prevents the scroll from becoming monotonous. The numbered chapter system (1.0, 2.0, etc.) creates a visual spine running through the homepage scroll.

### Homepage Scroll Architecture (Module Pattern)

1. Hero (full-viewport, dark): Large H1 + descriptor + floating live-updating annotation ("Issue tracking is dead")
2. UI mockup (full-bleed product screenshot)
3. "A new species of product tool" — three-column value propositions (FIG 0.2, 0.3, 0.4)
4. Feature section 1.0 (Intake) — left text, right product UI
5. Feature section 2.0 (Plan) — text + roadmap product UI
6. Feature section 3.0 (Build) — text + agents UI
7. Feature section 4.0 (Diffs — "Coming soon") — text + code diff UI
8. Feature section 5.0 (Monitor) — text + analytics UI
9. Changelog horizontal strip
10. Customer quotes + social proof
11. CTA section ("Built for the future. Available today.")
12. Footer

### Footer Layout Details

Five-column grid: Product | Features | Company | Resources | Connect. Each column has a bold 12px tracked label and then a list of text links at 13–14px. Below the columns: a horizontal rule, then a row with the Linear logomark (left), Privacy / Terms / DPA (right). Social links (X, GitHub, YouTube) appear in the Connect column as text.

### Layout Elements Deliberately Absent

- **No sticky announcement bar** (many SaaS sites have a promo/announcement strip above nav — Linear omits this entirely, consistent with the "don't compete for attention you haven't earned" philosophy)
- **No floating chat widget** (no Intercom bubble or similar — contact is accessed via the Contact nav item)
- **No cookie consent banner** (at time of access — or handled at a lower visual prominence than most EU-facing SaaS)
- **No mega menu** (Product and Resources links in the nav may expand, but there's no multi-column mega menu in the Shopify/enterprise SaaS style)
- **No sidebar on marketing pages** (no sticky sidebar for in-page navigation, even on long Method page)
- **No "breadcrumb" trail** on most pages (only appears in editorial/blog posts)
- **No infinite scroll carousels** for homepage content — content is stacked sections, not horizontally scrolling carousels (except implied for changelog strip)

---

## 5. UI Components

### Buttons

**Primary CTA ("Sign up"):**
- Background: `#ffffff` (Mercury White)
- Text: near-black `#0a0a0b`
- Height: ~36–40px
- Border radius: ~6–8px (slightly rounded, not pill-shaped)
- Font: Inter Medium/Semibold, 14–15px
- Padding: ~12–16px horizontal
- Border: none (solid fill)
- Hover state: slight opacity reduction or background dims to `#e8e8ec`

**Secondary CTA ("Contact sales", "Get started" secondary):**
- Background: `rgba(255,255,255,0.08)` — ghost/glass button
- Text: `#ffffff`
- Border: 1px `rgba(255,255,255,0.15)`
- Border radius: same ~6–8px
- Hover state: background brightens to `rgba(255,255,255,0.12)`

**Text link CTA ("Make the switch →", "Customer stories →", "See all releases →"):**
- No background, no border
- Text: `#ffffff` with arrow character
- Underline: none by default
- Hover: color shifts to `#F4F5F8` or underline appears
- Font size: matches context (14–16px)

**"Talk to sales" / "Contact support" (small outline):**
- Observed on Contact page as rounded rectangle buttons
- Background: transparent or very subtle dark fill
- Border: ~1px white-alpha border
- Border radius: ~6px
- Contains a `›` or `→` arrow icon inline
- These are smaller, more contained than homepage CTAs — appropriate for functional contexts

**Toggle switches (Pricing — "Billed yearly"):**
- Active state background: `#5E6AD2` (indigo accent)
- Inactive state: dark gray
- Width: ~36px, height: ~20px, pill-shaped
- Thumb: white circle

### Navigation

**Desktop nav structure:**
- Fixed horizontal bar at top, full viewport width
- Left: Linear logomark + wordmark
- Center-right: Product | Resources | Customers | Pricing | Now | Contact (text links, ~15px, Inter Regular/Medium)
- Far right: pipe separator | "Log in" (text link) | "Sign up" (white button)
- Background: matches page background (transparent to dark)
- No visible border/shadow below nav — the darkness provides implicit separation

**No mega menu observed.** Hovering "Product" and "Resources" may trigger a dropdown, but based on the DOM read the nav appears to be a simple link structure, not a mega menu system.

### Forms

Contact page has no inline form — it directs to external sales/support flows. The "Sign up" button leads to `linear.app/signup`. Forms are not native to the marketing site.

### Accordions

Not prominently observed in the pages browsed — pricing FAQ section may use accordions (below the fold on pricing page) but could not be confirmed in the scroll depth accessed.

### Product Carousels

The homepage changelog strip appears as a horizontal list of changelog items — likely scrollable or simply overflowing with visible items. No custom carousel arrow buttons were observed on the pages accessed. The feature sections (1.0–5.0) are vertical scroll sections, not carousels.

### Button States & Interactions

- **Hover:** Background lightens or gains transparency shift; text links gain underline or lighten to white
- **Active/Pressed:** Brief darker state (implied, standard web behavior)
- **Disabled:** Not prominently observed in marketing context
- **Focus:** Standard browser focus ring, potentially styled with the indigo accent color
- **Loading:** Sign up / login flows would have loading states, but these exist within the app (not visible in marketing pages)

### Toggle/Switch Behavior (Pricing)

The "Billed yearly" toggle on pricing cards uses the indigo `#5E6AD2` active state. Switching between monthly/yearly presumably animates the price values — the toggles are pre-set to "Billed yearly" state, suggesting this is the encouraged default.

### Search Component

No visible search bar on marketing pages. The nav does not include a search icon or input. The documentation site (linear.app/docs) likely has search, but not observed in this audit.

### Accessibility Widget

No visible third-party accessibility widget (UserWay, AccessiBe, etc.) was observed — consistent with the clean UI philosophy. Accessibility is handled natively (skip-to-content links were observed in the page source: `[Skip to content →](https://linear.app/#skip-nav)`).

### Link & Hover States

- **Nav links:** Mouse-over lightens text from ~`#aaaabc` to `#ffffff`
- **Footer links:** Similar behavior, muted gray to white
- **In-body text links:** Indigo `#5E6AD2`, likely with underline on hover
- **CTA buttons:** Described above
- **Card containers:** Subtle border brightening or background shift on hover

### Video Embed Behavior

Multiple pages feature embedded HTML5 video players:
- About page: founder video (3:18 duration)
- Blog posts: feature demonstration videos
- Changelog entries: product announcement videos

The video player is minimal — custom styled with play/pause, mute, seek bar, and full-screen button. No third-party player branding (no YouTube chrome). The player background matches the page dark background. Autoplay with muted audio is likely used for showcase videos.

### Animation & Motion Philosophy

Linear's motion is **surgical and purposeful**. What's animated:
- **Page transitions:** Smooth fade or slide (implied by SPA architecture)
- **UI mockup components on homepage:** Live-updating content within the product screenshots — simulated real-time activity (issues being created, agents running) — this is the most complex animation on the site
- **CTA button hover states:** Subtle opacity/color transitions (~150–200ms ease)
- **Toggle switches:** Smooth thumb slide on state change

What's static:
- **Section titles:** No entrance animations observed (no GSAP scroll-triggered text reveals)
- **Card grids:** No staggered reveal animations
- **Navigation:** No animated hamburger or mega menu transitions visible

The philosophy is: **animate what the product does, not the marketing page itself.** The animated UI mockups demonstrate product value through motion; the marketing page wrapper is static. This is the inverse of many SaaS sites that use heavy Lottie animations for features but show static product screenshots. Linear chose to make the product mockups themselves the animation canvas.

---

## 6. Iconography

### Complete Icon Inventory

**Navigation & Global UI:**
- Linear logomark symbol — top-left nav and footer; geometric faceted shape
- RSS/bell icon — top-right of Now/Blog page header (feed subscription)
- External link arrow (↗) — used inline with investor names on About page, indicating off-site destinations
- Arrow right (→ and ›) — used in text-link CTAs throughout ("Make the switch →", "Talk to sales ›")

**Contact Page:**
- Document/form icon — next to "Sales" heading
- Chat bubble icon — next to "Help & support" heading
- Mail/envelope icon — next to `hello@linear.app` email address

**Pricing Page:**
- Checkmark circles — feature list items for each pricing tier, white filled circles with checkmark
- Toggle/switch UI component — described above

**Security Page:**
- Lock icon — next to "Enterprise-grade security" feature
- Chart/bar icon — next to "SOC 2 compliance"
- Medical caduceus icon (badge) — HIPAA compliance badge

**Integrations Page:**
- Star icon — "Essentials" category in sidebar filter
- Robot/agent face icon — "Agents" category
- Wrench/tool icon — various categories
- Monitor/screen icon — "Engineering", "Customer Experience" categories
- Lock icon — "Security & Compliance"
- Analytics gear — "Analytics" category
- Chat bubble — "Collaboration"
- Paintbrush/palette — "Media & Design"
- Bug icon — "Bug Reporting"
- Refresh/cycle icon — "Automations"
- Verified badge (checkmark in circle) — "By Linear" verification on integration cards (GitHub, Slack, GitLab, Figma, Intercom, Google Sheets)

**App UI Mockups (shown in product screenshots on homepage/feature pages):**
- Inbox icon (tray)
- Issue/document icon
- Reviews icon (star or similar)
- Pulse icon (waveform)
- Search icon (magnifying glass)
- Compose/new icon (pen/edit)
- More options (ellipsis)
- Priority level icons (four-bar chart for High priority)
- Status icons (circle for In Progress, filled circle variants for Done/Todo/Canceled)
- Avatar circles (user profile images)
- Copy icon, link icon, pin icon (in issue header)
- GitHub Copilot logo

### Icon Design Philosophy

Linear's icons are **custom-drawn, minimal, and highly geometric** — consistent with the Inter typeface family in their clean, unpretentious construction. They use a consistent stroke weight (~1.5–2px at 16px display size), round end caps, and geometric construction. No skeuomorphic detail, no gradients, no drop shadows.

Icons are used **very selectively** — they appear only where categorization or navigation demands them (integrations filter, contact page), never decoratively. The homepage hero has no icons. Major section headings have no icons. This restraint is intentional: icons can reduce perceived intelligence of content when overused.

### Icon Color Rules

- Marketing page icons: **white** (`#ffffff`) or very light gray (`#F4F5F8`) on dark backgrounds
- UI mockup icons: context-appropriate (muted gray for inactive, white for active, indigo for selected)
- "By Linear" verification badges: white checkmark on a slightly elevated circular background
- Status icons in mockups: colored (green, orange, gray) to convey state

### Icon Sizing

- Nav/global: 16–20px
- Integrations sidebar: 16px
- Contact page section icons: 20–24px
- In-content CTA arrows (text inline): 12–14px, treated as characters not separate images
- App UI mockup icons: 12–16px (matching app specifications)

### Icons Deliberately Absent

- **No social media share icons** on article pages (contrary to typical blog convention — no Facebook/Twitter share buttons)
- **No star ratings** or review icons (no social proof gamification)
- **No emoji usage** in official UI (emojis appear only within the product mockup data as customer-generated content — e.g., the Kinetic Corp demo uses emoji in their workspace)
- **No feature illustration icons** (many SaaS companies use colorful icon sets — Notion, Loom — for feature grids; Linear uses UI screenshots instead)
- **No trust badge icons** except the certification seals on the Security page (no "256-bit encrypted" padlock badges on pricing, etc.)

---

## 7. Photography Style

### Product Photography

Linear does not sell physical products, so traditional "product photography" is replaced by **software UI photography/mockups**. These are pixel-perfect, high-fidelity renders of the Linear application interface, styled as:
- Dark mode interface (consistent with site aesthetic)
- Floating/floating-perspective views (slight isometric tilt on some mockups)
- Fully-populated with realistic fictitious data (the "Kinetic Corp" autonomous vehicle startup)
- Rendered with subtle depth of field effects implied by layer shadows
- The content within mockups is carefully art-directed — the fictional company (Kinetic Corp / ENG-xxxx issue IDs) tells a coherent story

### Lifestyle/Editorial Photography

**Careers page:** The single editorial photograph is a **real photography** image of what appears to be a team member or employee — a person at an outdoor workspace (garden/patio setting, European roofline visible). The image is:
- Natural, candid framing
- Shot in daylight with warm, soft natural light
- No studio setup — authentically casual
- Desaturated slightly in post — not vibrant, consistent with the brand's restrained palette
- Full-bleed layout taking up most of the viewport

**About page:** A video (3:18) features founder Karri Saarinen. The video still shows him in what appears to be a home office/workspace setting. Casual, authentic, no studio backdrop. This is the "face" of the brand — deliberate warmth and humanity in contrast to the cold precision of the UI.

**Blog/Now thumbnails:** Article card thumbnails include:
- Product UI screenshots (most common)
- Customer brand logos (Coinbase "C", Cursor logo) on abstract dark backgrounds — creating a visual consistency by treating third-party logos as art objects
- Abstract geometric/design imagery (the UI refresh post features a blueprint-like technical diagram)

### Hero Images

The site uses **no hero photography** in the traditional sense. Hero sections are:
- Pure dark background + typography (Homepage, Method, Security, Careers hero)
- Typography + embedded video (About page)
- Typography + product screenshot (Enterprise, features pages)

The deliberate avoidance of stock photography in heroes is significant. No smiling teams, no abstract blue gradients, no "technology hands on keyboard" clichés. This positions Linear as a brand above the visual language of enterprise software.

### Photography Strategy & Art Direction

The photography strategy can be summarized as: **Real humans, real environments, real work — never stock, never staged.** Where photography appears, it is documenting actual Linear culture. The product mockup "photography" (UI screenshots) is meticulously designed to communicate product value better than any photo could.

The art direction of the product mockups is particularly sophisticated: the fictional "Kinetic Corp" is a self-driving vehicle company — a maximally complex, high-stakes engineering context — demonstrating that Linear can handle the most demanding product teams. This is strategic storytelling through example data.

### Lifestyle Casting Notes

The limited human imagery shows:
- The founding team (About page video, team member photos): diverse, international backgrounds (Finnish founders, team spanning North America and Europe per About page text)
- Casual, professional attire — no suits, no hoodies (the default Silicon Valley look) — the careers photo shows neutral casual wear
- Settings: home offices, outdoor workspaces — communicating the remote-first culture
- Age range: appears 30s–40s for leadership; broader range implied in full team listing

### Image Aspect Ratios

- **Blog/Now card thumbnails:** ~16:9 (landscape)
- **Customer story cards:** approximately 3:2 landscape
- **Full-bleed page heroes:** 16:9 to 21:9 (ultra-wide hero images span viewport width)
- **Founder video (About page):** 16:9
- **Product UI mockup screenshots:** variable, often approximately 4:3 or 16:10 (matching laptop screen proportions)

### Hover Behavior on Cards

Cards on Customers and Now pages show subtle border brightening or slight scale transform (~1.02) on hover — no dramatic zoom or overlay text behavior. Consistent with the restrained interaction philosophy.

### Image Treatment Consistency

- **No filters or color overlays** on photographic images
- **No tinting to match brand palette** (images retain their own color temperature)
- **Dark mode context** means all images are "floating" against the dark background — they're not edge-to-edge color-matched but rather panel-contained
- **UI screenshots:** These are shown "clean" — no device frames (no MacBook bezels, phone frames) except occasionally slight shadow to suggest floating depth

---

## 8. Brand Voice & Language Style

### Tone: Overall Personality

Linear's brand voice is **the voice of a thoughtful senior engineer who has also read philosophy and cares deeply about craft**. It is not a marketing voice. It is not friendly in the customer-service sense. It is confident without arrogance, intelligent without condescension, and principled without preachiness.

Ten sub-categories:

1. **Declarative authority:** Statements are made without hedging. "Issue tracking is dead." Not "Issue tracking may be becoming less relevant." This is a brand that makes bold claims and backs them with reasoning. The voice claims territory.

2. **Systems thinking:** Language consistently frames software development as a *system* — "the product development system," "product operations self-driving," "a new species of product tool." This positions Linear at the meta-level above individual features, claiming to solve the architecture of work itself.

3. **Technical precision:** Exact language. "Purpose-built for planning and building products. Designed for the AI era." No waste words. The copy mirrors the product philosophy: nothing unnecessary.

4. **Craft reverence:** The Method page opens: "There is a lost art of building true quality software." This is not marketing language — it's cultural positioning. Linear speaks to engineers who believe software can be a form of craftsmanship.

5. **Anti-hype sincerity:** Despite the bold claims, the voice avoids hyperbole superlatives. No "world-class," "revolutionary," or "game-changing" (the about page says "world-class product teams" as a descriptor of customers, not Linear itself). This is strategic: engineers distrust marketing language.

6. **Founder authenticity:** CEO Karri Saarinen's byline appears on major essays ("Issue tracking is dead," design philosophy posts). The brand speaks through its founders' genuine perspectives, not through brand committee copy.

7. **Future-orientation without futurism clichés:** "Built for the future. Available today." positions Linear as already ahead, without invoking sci-fi language or AI hype tropes. The phrase is simple and confident.

8. **Community as mission:** "More than 25,000 companies" and "ambitious startups to major enterprises" — the community is described in terms of ambition and quality, not just size. The customer is cast as the hero of a larger story.

9. **Self-aware meta-commentary:** The design refresh blog post explicitly discusses the trade-offs and thinking behind design decisions. The brand documents its own process publicly — this is transparency as brand strategy.

10. **Question-free headlines:** Nearly all headlines are statements, not questions. "How can we help?" (Contact page) is a rare exception. This creates a sense that Linear knows exactly what it's doing and doesn't need to invite your input — it presents.

### Language Patterns

**Founder narrative:** Karri Saarinen writes in a measured, essayistic voice. "Issue tracking is dead. It was built for a handoff model of software development." These are short declarative sentences. The rhythm is deliberate. The essay builds an argument. This mirrors the Linear Method — written communication should be clear and direct.

**Product description structure:** Feature descriptions follow a consistent pattern: [verb] + [object] + [outcome]. "Turn conversations and customer feedback into actionable issues that are routed, labeled, and prioritized." Active voice, specific mechanism, clear outcome.

**Collection/feature page pattern:** Each product area (Intake, Plan, Build, Diffs, Monitor) follows: numbered label → benefit statement → brief description → "N.0 Feature name →" link. The numbered system creates a sense of a comprehensive methodology, not a feature list.

**Material/capability specificity:** Rather than vague "powerful" language, Linear uses specific capabilities: "Triage Intelligence," "SAML and SCIM," "Granular admin controls." Technical specificity is trust-building with their audience.

**Pricing copy:** Stark and functional. "Free for everyone." "$10 per user/month." No discounting drama, no "Save 20%!" banners. Even the pricing page CTA ("Get started") is neutral rather than urgent.

**Social proof language:** "Linear powers over 25,000 product teams. From ambitious startups to major enterprises." The specific number (25,000) is precise — not "tens of thousands." The qualifier "ambitious" is evaluative — Linear is for companies with aspirations.

**Announcement/alert:** "Issue tracking is dead · linear.app/next →" — this nav-adjacent annotation is conversational, pointed, and deliberately provocative as a cultural statement.

### Heading Style (Complete Inventory)

| Page | Heading | Pattern |
|---|---|---|
| Homepage H1 | "The product development system for teams and agents" | Descriptor noun phrase, lowercase except "The" |
| Homepage H2s | "Make product operations self-driving", "Define the product direction", "Move work forward across teams and agents", "Review PRs and agent output", "Understand progress at scale" | Action verb + object, sentence case |
| Customers | "Meet the teams who build the future" | Imperative verb ("Meet") + descriptor |
| Pricing | "Pricing" | Single word, bare |
| About | "Building tools for the next era of product development" | Gerund phrase |
| About sub | "A new species of product tool" | Declarative descriptor |
| About sub | "Meet the team behind Linear" | Imperative, mirrors Customers page pattern |
| About sub | "Backed by the best" | Short, confident |
| Method | "Practices for building" | Noun + gerund — unusually spare |
| Blog/Now | "Now" | Single word |
| Security | "Safe, secure, and private." | Adjective series with terminal period (stylistic) |
| Careers | "Help us craft high-quality tools" | Imperative, collaborative |
| Contact | "How can we help?" | The only question mark in all headlines — appropriate softening for a service context |
| Brand | "Linear Brand Guidelines" | Functional descriptor |
| Enterprise | "Product development for modern enterprises" | Noun phrase |

**Capitalization pattern:** Sentence case throughout — only first word and proper nouns capitalized. No title case. This is a direct reflection of the technical writing standard (GitHub, Stripe, Linear all use sentence case) — it signals engineering culture over marketing culture.

**Period use in headlines:** Used sparingly but deliberately. "Safe, secure, and private." has a terminal period — as do some Method page passages. The period as stylistic device signals that the statement is complete, definitive, non-negotiable.

### CTAs & Microcopy

**Homepage:**
- "Get started" — primary, white button. Neutral, imperative, low-anxiety
- "Contact sales" — secondary, ghost button. Professional, not salesy

**Pricing:**
- "Get started" — repeated on Free/Basic/Business tiers
- "Contact sales" — for Enterprise tier (appropriate escalation)

**Contact page:**
- "Talk to sales ›" — specific action verb matching the context
- "Contact support ›" — specific action verb

**Footer CTA section:**
- "Built for the future. Available today." — the most rhetorically complete CTA copy on the site. Two sentences. First establishes aspiration, second eliminates the excuse for waiting.
- "Get started" — white button
- "Contact sales" — ghost button

**Careers:**
- "Open roles ↓" — text with directional arrow, scrolls to jobs list
- "We're hiring →" (About page link to careers) — casual, human

**Blog/Now:**
- "Read story" — minimal, no ornamentation
- "See all releases →" — functional, honest

**Brand guidelines:**
- "Download Brand Assets" — direct, functional, no "Download now!" enthusiasm
- "Get in touch" — human register for the IP usage question CTA

**Microcopy tone:** Consistently **minimal and precise**. No exclamation marks. No FOMO language. No countdown timers or "limited time" pressure. The brand trusts its audience to make good decisions without being manipulated. This is consistent with the anti-hustle culture stance documented in the Entrepreneur press mention ("Why the CEO of a $1 Billion Startup Rejects Silicon Valley's Hustle Culture").

---

## 9. Platform & Technical Notes

### Platform Identification

Linear.app is a **fully custom-built React/Next.js single-page application (SPA)**, not a CMS like Shopify, WordPress, or Webflow.

**Evidence:**
- URL structure is clean and app-like (no `.html` extensions, no `?page=`)
- Page navigation behaves as client-side routing (no full page reloads)
- The blog/Now section uses a custom CMS or flat-file approach
- Page titles follow: "[Page Name] – Linear" or "Linear – [Description]" (standard Next.js pattern)
- No Shopify cart indicators, no WordPress admin bar
- The site loads assets from `static.linear.app` (brand assets ZIP: `https://static.linear.app/design-assets/Linear-Brand-Assets.zip?v=3`)

### Theme Architecture

Custom design system, not a stock theme. The UI consistency across all pages (spacing, typography scale, color tokens) indicates a mature internal design system — consistent with the blog post revealing they use design tokens (JSON import capability for theme values). The "integrated color picker" and "dev toolbar" described in the design refresh post confirm a custom token-based theming system.

### URL Structure Patterns

- `linear.app/` — homepage
- `linear.app/[product-feature]` — product landing pages (intake, plan, build, diffs, monitor)
- `linear.app/[feature]` — feature pages (agents, asks, insights, mobile, integrations)
- `linear.app/customers` — customer index
- `linear.app/customers/[company-slug]` — individual customer stories
- `linear.app/pricing` — pricing
- `linear.app/now` — blog/content hub
- `linear.app/now/[article-slug]` — individual blog posts
- `linear.app/changelog` — changelog (redirects to linear.app/now with changelog filter)
- `linear.app/changelog/[date-slug]` — individual changelog entries
- `linear.app/about`, `linear.app/careers`, `linear.app/brand`, `linear.app/method`, `linear.app/quality`
- `linear.app/security`, `linear.app/enterprise`, `linear.app/startups`
- `linear.app/docs` — documentation (separate app)
- `linear.app/developers` — developer documentation
- `linear.app/contact`, `linear.app/contact/sales`
- `linear.app/signup`, `linear.app/login`

**Pattern:** Flat URL structure with no deep nesting beyond two levels. Clean, memorable, functional.

### Third-Party Integrations Identified

- **Intercom** — implied (Linear Asks feature references Zendesk and Intercom integrations; likely used for their own support)
- **Slack** — deep integration (community is Slack-based)
- **GitHub** — deep integration (code-level features)
- **Figma** — integration partner
- **Google Sheets** — integration
- **GitLab** — integration
- **Zendesk** — integration partner (mentioned in Business plan features)
- **Stripe** — likely for payment processing (standard for SaaS billing)
- No visible Segment, Mixpanel, or analytics pixel banners detected
- No visible A/B testing tool overlays (Optimizely, etc.)
- No third-party chat widget visible on marketing pages

### Page Performance Observations

The site loads extremely fast — consistent with their stated emphasis on performance as a brand value. The dark background loads nearly instantly (few large images in the initial viewport). JavaScript is the main bundle but the SPA architecture handles routing efficiently. The heavy content (UI mockup animations, videos) is below the fold and lazy-loaded.

### SEO & Meta Title Patterns

- Homepage: "Linear – The system for product development"
- Pricing: "Pricing – Linear"
- Customers: "Linear Customers"
- About: "About – Linear"
- Method: "Linear Method – Practices for building"
- Security: "Security – Linear"
- Careers: "We're hiring – Linear"
- Brand: "Brand Guidelines – Linear"
- Blog posts: "[Article Title]" (no site name appended on articles — they're confident about traffic)
- Contact: "Contact us – Linear"

**Pattern:** "[Page] – Linear" or "Linear – [Descriptor]." Consistent, functional, no keyword stuffing.

### Legal & Compliance Pages

- `linear.app/privacy` — Privacy Policy
- `linear.app/terms` — Terms of Service
- `linear.app/dpa` — Data Processing Agreement (notably present in footer — signals enterprise readiness)
- `linear.app/security` — Security page (SOC 2, GDPR, HIPAA compliance documented)

### Accessibility Features

- Skip-to-content link in source: `[Skip to content →](url#skip-nav)` — present on every page
- No third-party accessibility overlay widget
- Semantic HTML structure implied by the accessibility tree
- Alt text on images: partially observed ("Linear logo", "Avatar of Karri", etc.)
- Keyboard navigation expected given Linear's user base (developers and power users)
- Focus management within SPA routing: critical for accessibility compliance

### Social Media Accounts

As listed in the footer "Connect" section:
- **X (Twitter):** https://x.com/linear
- **GitHub:** https://github.com/linear
- **YouTube:** https://www.youtube.com/@linear
- **Slack community:** `linear.app/join-slack`

Notable **absence**: No LinkedIn, no Instagram, no Facebook. The social channel selection (X/Twitter, GitHub, YouTube) precisely maps to the developer/product/engineering community that is Linear's audience. This is not an accident.

---

## 10. Pages Browsed

1. **https://linear.app** — Homepage: "The system for product development"
2. **https://linear.app/pricing** — Pricing page: Free / Basic / Business / Enterprise tiers
3. **https://linear.app/customers** — Customers index: "Meet the teams who build the future"
4. **https://linear.app/about** — About page: Company story, team, investors
5. **https://linear.app/method** — Linear Method: "Practices for building"
6. **https://linear.app/blog** (redirects to https://linear.app/now) — Blog/Now content hub
7. **https://linear.app/now** — Now page: editorial index with Changelog, Community, News, Craft, AI, Practices, Press
8. **https://linear.app/contact** — Contact page: Sales, Help & Support, Community, General communication
9. **https://linear.app/brand** — Brand Guidelines: naming, usage, wordmark, logo, icon, colors
10. **https://linear.app/security** — Security page: SOC2, GDPR, HIPAA compliance
11. **https://linear.app/careers** — Careers page: "Help us craft high-quality tools"
12. **https://linear.app/changelog** — Changelog: "Introducing Linear Agent" (latest release)
13. **https://linear.app/now/behind-the-latest-design-refresh** — Editorial post: "A calmer interface for a product in motion" (March 12, 2026)
14. **https://linear.app/enterprise** — Enterprise landing page: "Product development for modern enterprises"
15. **https://linear.app/next** — Long-form essay: "Issue tracking is dead" by Karri Saarinen (March 24, 2026)
16. **https://linear.app/integrations** — Integrations directory: GitHub, Slack, GitLab, Figma, Intercom, Google Sheets + categories

---

*Audit compiled by AI analysis of linear.app across 16 pages, April 2026. All observations based on rendered page content, DOM inspection, and visual analysis. Color values are observed approximations unless explicitly confirmed by the brand guidelines page (Mercury White `#F4F5F8`, Nordic Gray `#222326`).*
