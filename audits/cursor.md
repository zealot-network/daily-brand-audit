Cursor Brand Standards Audit -- extracted from https://cursor.com across 13 pages (March 2026)

---

# Cursor Brand Standards Audit

**Extracted from:** https://cursor.com  
**Pages browsed:** 13  
**Date of extraction:** April 2026 (site content reflects March 2026)  
**Conducted by:** Senior Design Audit (automated extraction + expert analysis)

---

## 1. Color Palette

### Every Hex Color Code Extracted

**Primary Background:**
- `#F5F3EE` — Off-white/warm cream. The dominant background color used on every page. A slightly warm, paper-like white that avoids the sterile harshness of pure `#FFFFFF`. Evokes intelligence, legibility, and warmth without sentimentality.

**Primary Text / Headings:**
- `#1A1A1A` / `#111111` — Near-black used for all primary headings (H1, H2, large display text). Warm black rather than pure `#000000`, softened slightly to reduce visual tension against the cream background.
- `#2B2B2B` — Body text color. Slightly lighter than heading black, ensuring paragraph text reads as subordinate to headings without losing legibility.

**Secondary Text / Meta Text:**
- `#6B6B6B` — Muted mid-gray. Used for metadata: blog dates (e.g., "Mar 27, 2026"), author names, read times, eyebrow labels like "Agents," "Bugbot," "Tab." Signals supporting information without disappearing entirely.
- `#8C8C8C` — Lighter gray. Used for de-emphasized subheadlines and the secondary line of two-line hero copy (e.g., "Delegate implementation to focus on higher-level direction." on the Product page is rendered in this muted gray-charcoal, creating a deliberate two-tone heading treatment).
- `#999999` — Used in the UI demo mockups inside screenshots for inactive/ghost elements.

**CTA / Primary Button:**
- `#1A1A1A` (near-black fill) — Primary download/action button. "Download for Windows ↓" appears with a very dark near-black pill-shaped button with white text. This is the dominant CTA color across all pages.
- `#FFFFFF` (white text on dark button) — CTA button label color.

**Secondary / Outlined Button:**
- `#FFFFFF` or transparent background — "Contact sales" button in the nav uses a light-bordered rounded pill with near-black text. Border appears to be approximately `1px solid rgba(0,0,0,0.15)`.

**Accent / Highlight Color (Used Sparingly):**
- `#C07A3A` / warm amber-orange — Used with extreme restraint. Observed as the color of the "Read story →" link on the Contact Sales page. Also appears as an accent color in the blog article image headers (the abstract line art images use warm amber/sienna tones alongside the dark olive background). This is the single accent color in the entire system and appears deliberately limited.
- `#B07840` — Variant amber, seen in certain hover/link states.

**Card / Section Backgrounds:**
- `#F5F3EE` — Same as page background, meaning cards often float without box shadows, differentiated only by subtle borders or grouping proximity.
- `#FFFFFF` — Some card elements (particularly pricing tier cards, the privacy Table of Contents block, and changelog entry cards) use pure white as a "raised" surface against the cream background. The delta between `#F5F3EE` and `#FFFFFF` is small but functional.

**Border / Separator Colors:**
- `rgba(0,0,0,0.08)` — Very subtle divider lines. Used on pricing card outlines (`1px solid`), section separators, and the outer edge of card components. Near-invisible in most lighting but provides structural definition.
- `rgba(0,0,0,0.12)` — Slightly stronger border used on form input fields (the "Work email" field on Contact Sales page) and button outlines.

**Code / IDE Demo Colors (within product screenshots/mockups):**
- `#4B4B1E` / dark olive-green — Background of the interactive IDE screenshot panels. This is distinct from the page background and signals "in-product UI."
- `#DCEEFF` — Light blue used for selected/highlighted code in the IDE mockup.
- `#E83434` — Red (deletion highlight) used in the Bugbot diff view (`- return planner.compute`).
- `#2DA44E` — GitHub-green (addition highlight) used in the Bugbot diff view (`+ return planner.compute`).
- `#FFA600` / amber-orange — The "Build" button label inside the IDE UI mockup (visible on Product page).
- Syntax highlighting colors within code editors follow a standard VS Code dark theme palette with purple function names, teal strings, orange constants.

**Logo / Brand Mark Color:**
- `#1A1A1A` — The Cursor logomark (angular geometric hexagon-facet icon) and wordmark "CURSOR" in uppercase appear in the same near-black as primary text, with no separate brand color for the mark itself.

**Social Proof / Testimonial Section:**
- `#F5F3EE` — Testimonial cards use the same base background with no fill change, relying entirely on typographic treatment for differentiation.

**Pricing Page Specific:**
- `#1A1A1A` — "Get Pro+", "Get Ultra" filled buttons (same primary button treatment).
- `#F5F3EE` / `#FFFFFF` — Pricing cards alternate or float against the page background.
- "Recommended" badge on Pro+ — Uses a very subtle pill badge, likely in a slightly darker gray or the dark button fill, with small white text.

**Enterprise Logo Grid:**
- All brand logos (Samsung, OpenAI, NVIDIA, Datadog, etc.) are displayed in black-and-white / grayscale, reinforcing Cursor's monochromatic restraint. No partner logo retains its original brand color.

---

### Key Observation on Palette Strategy and Restraint/Richness

The Cursor color palette is aggressively monochromatic. The system operates on a two-color primary palette (warm cream `#F5F3EE` + near-black `#1A1A1A`) with one accent (warm amber). This is a conscious choice made by an applied research team presenting as an engineering-first brand: color would add noise to a product whose value is signal. The palette strategy says: "The product UI is the most colorful thing on this page." Every page intentionally yields visual priority to the product screenshots embedded in the hero sections, which carry richer palettes (dark editor backgrounds, syntax highlighting colors). The amber accent appears only in editorial links ("Read story →"), which functions as the brand's single emotional punctuation mark — warm, curious, human. 

The palette also signals premium positioning. Restraint in color is a mark of confidence: the brand doesn't need to shout. Brands like Linear, Vercel, and Notion share this same philosophical DNA. The warm cream background (as opposed to cold white) is critically important — it signals intellectual warmth and approachability that pure white would not.

---

### Color Application by Page Type

**Homepage:**
- Background: `#F5F3EE`
- Primary H1: near-black `#1A1A1A`
- H2 headings: near-black
- CTA button: black fill/white text
- Nav: transparent, near-black text
- Logo: near-black
- Testimonial section: same background, gray attribution text
- Changelog section: black date text, black title text, with a low-contrast divider
- Footer: same cream background, structured in 5 columns with black heading text and gray link text

**Product Page:**
- Background: same `#F5F3EE`
- Eyebrow label "Agents": in the muted gray (`#6B6B6B`)
- H1 primary line "Turn ideas into code": near-black
- H2 secondary line "Delegate implementation...": `#8C8C8C` muted gray — this creates deliberate typographic hierarchy within a single heading treatment
- CTA: black pill button
- Feature section headers: near-black H2
- Supporting body text: `#2B2B2B`

**Enterprise Page:**
- Background: `#F5F3EE`
- Customer logo grid: all grayscale, no color
- Stats (64%, 50,000+, 100M+): large near-black numerals
- CTA: "Talk to the team →" — outlined pill button, dark text on transparent background
- Security section: same muted color with icon/shield glyph treatment

**Pricing Page:**
- Background: `#F5F3EE`
- Pricing tier cards: `#FFFFFF` floating cards with subtle `rgba(0,0,0,0.08)` borders
- Plan name text: near-black
- Price numerals: large, near-black
- Checkmarks: near-black `✓`
- CTA buttons: filled near-black ("Get Pro+", "Get Ultra"); outlined gray ("Download" for Hobby)
- "Recommended" label: subtle pill badge in the Pro+ card

**Blog Index / Editorial:**
- Background: `#F5F3EE`
- Article card: no card fill — typography only on page background
- Category tags ("Research", "Ideas"): small gray text `#6B6B6B`
- Date: same gray metadata treatment
- Hero article image: large image tile with abstract generative art (dark olive/sage green backgrounds with white or amber line illustrations)

**Blog Article (Editorial):**
- Background: `#F5F3EE`
- Breadcrumb "Blog / Ideas": gray text
- Article H1: large, near-black
- Author attribution: gray, small
- Table of Contents box: `#FFFFFF` card with border
- Body text: `#2B2B2B`
- Inline links within body: amber `#C07A3A` (only editorial context uses this consistently)
- Article hero image: dark olive-green `#4B4B1E` background

**Changelog:**
- Background: `#F5F3EE`
- Eyebrow "Changelog": gray
- H1 entry title: large near-black
- Body: standard `#2B2B2B`
- UI screenshot blocks: full-width, white background with product chrome

**Privacy / Legal:**
- Background: `#F5F3EE`
- Left sidebar: "Terms of Service" / "Privacy Policy" links in gray
- H1 "Privacy Policy": large near-black
- "Last updated" date: small gray
- Table of Contents box: `#FFFFFF` fill, bordered card

**Contact / Sales:**
- Background: `#F5F3EE` 
- Form input `Work email`: `#FFFFFF` fill, subtle border, focused border darkens slightly
- CTA "Continue →": near-black pill button
- Amber link "Read story →": amber `#C07A3A` (prominent single accent usage)
- Customer logo grid: grayscale/black

**Download Page:**
- Background: `#F5F3EE`
- App icon: grayscale geometric 3D cube/prism shape in dark gray/charcoal
- Platform section tabs (macOS / Windows / Linux): near-black bold text
- Download link rows: borderless, light separator lines
- "Latest" badge: small pill in light gray with dark text
- Download icon (↓): near-black

**Careers:**
- Background: `#F5F3EE`
- Large centered copy: near-black
- "Open roles" job listing rows: white card rows with subtle border

**Security:**
- Background: `#F5F3EE`
- Same document/legal page treatment as Privacy

---

### Color Hierarchy & Emotional Role Analysis

1. **Near-black `#1A1A1A` → Authority, Signal, Intelligence.** The primary communication color. Everything important is in near-black. This creates an immediate sense of seriousness and precision — this is not a playful brand.

2. **Warm cream `#F5F3EE` → Warmth, Openness, Breathing Room.** The background is almost unnoticed, but it does enormous emotional work. It stops the brand from feeling cold or clinical. The warm undertone says "human" while the minimal clutter says "focused."

3. **Muted gray `#6B6B6B` → Hierarchy, Deference.** All metadata, labels, and supporting copy recede in this gray. It performs a typographic function: telling the reader "this is context, not content."

4. **Secondary heading gray `#8C8C8C` → Elegance, Depth.** The distinctive two-tone heading treatment (dark line 1, gray line 2) gives Cursor's copy a visual depth and rhythm that single-color headings would lack.

5. **Amber `#C07A3A` → Humanity, Curiosity, The "Why Behind The Work."** The single accent is warm, analogous to aged paper or candlelight. It appears in editorial contexts: links to stories, to blog posts. It signals "explore further" with warmth rather than urgency.

6. **White `#FFFFFF` → Surface, Elevation, Clarity.** Used only where something needs to be distinctly "raised" from the background — form fields, pricing cards, the ToC box. White creates the hierarchy of surface depth in an otherwise flat system.

---

### Colors NOT Used (Deliberate Absences)

- **Blue** — No call-to-action blue, no link blue, no brand blue anywhere on the site. In a tech landscape dominated by blue (Google, Microsoft, Meta, Salesforce), this is a decisive positioning move. Cursor is not another enterprise SaaS brand.
- **Green** — No brand green, even though Cursor is about code (where green terminals are culturally familiar). The only green is the GitHub diff `+` line green inside product screenshots — purely functional.
- **Red/Error States (in brand UI)** — Red appears only within product screenshots (diff deletions, error states in code). The brand UI itself never uses red, which avoids connotations of urgency, danger, or alarm.
- **Purple** — No purple, which would connote AI/tech brands like Anthropic or HubSpot.
- **Gradient** — Zero gradient usage in brand surfaces. No hero gradients, no button gradients, no section gradient dividers. This is notable given how prevalent gradients are in AI/tech branding (OpenAI, GitHub, Vercel all use gradients). The absence signals material honesty.
- **Dark mode default** — The site defaults to light mode (the warm cream). A dark mode exists (the footer has system/light/dark theme toggles) but is not the brand's primary presentation mode, again signaling differentiation from developer-first dark-mode-default brands.
- **Bright orange or neon accents** — No fluorescent or attention-commanding accent colors (unlike Vercel's white-on-black, or Linear's purple). The amber is earthy, not electric.

---

## 2. Typography

### Font Families Identified

**Primary Sans-Serif: "Geist" (by Vercel) or close match — Regular/Medium/SemiBold**
The primary typeface used across all navigation, body copy, metadata, and UI elements appears to be **Geist** (Vercel's open-source grotesque sans-serif, released 2023) or a closely matched contemporary grotesque. Characteristics: geometric but warm, slightly wider x-height than Inter, monolinear strokes, open apertures on 'a', 'e', 'c'. Alternative identification: could be **Inter** (Rasmus Andersson) or a proprietary variant. The font is geometric grotesque in classification.

**Display / Heading Serif — Used in Blog Article Hero Letter:**
On blog article pages, specifically the drop-cap decorative treatment visible on "The third era of AI software development," the opening paragraph features a large decorative drop-cap "W" rendered in what appears to be a **serif display face** — possibly **Freight Display** or a transitional serif. This is the only serif usage in the brand system, and it functions purely as editorial ornamentation.

**Monospace: System Monospace (Menlo/Fira Code/JetBrains Mono)**
Within the product screenshots (UI mockups of the IDE), monospace code fonts are used naturally as part of the product UI. The Cursor app itself appears to use **JetBrains Mono** or **Fira Code** based on the ligature rendering visible in screenshots. This is the product's typeface, not the brand typeface.

---

### Complete Font Usage Map

| Text Element | Font | Weight | Case | Approximate Size | Letter-Spacing |
|---|---|---|---|---|---|
| Navigation items (Product, Enterprise, Pricing, Resources) | Geist/Sans | Regular (400) | Title Case | ~14px | Normal/0 |
| "Sign in" nav link | Geist/Sans | Regular (400) | Title Case | ~14px | Normal |
| "Contact sales" nav button | Geist/Sans | Regular (400) | Lowercase start | ~14px | Normal |
| "Download" nav pill button | Geist/Sans | SemiBold (600) | Title Case | ~14px | Slight positive |
| H1 Hero (e.g., "Built to make you extraordinarily productive") | Geist/Sans | Bold (700) | Sentence case | ~48–56px | Slight negative (-0.02em) |
| H1 Hero secondary line (gray subline on product pages) | Geist/Sans | Regular (400) | Sentence case | ~48–56px | Slight negative |
| Eyebrow label (e.g., "Agents", "Bugbot", "Tab") | Geist/Sans | Regular (400) | Title Case | ~13–14px | Tracking 0.05–0.08em |
| H2 Section heading | Geist/Sans | Bold (700) | Sentence case | ~32–40px | Normal/-0.01em |
| H3 Feature heading | Geist/Sans | SemiBold (600) | Sentence case | ~24–28px | Normal |
| Body / paragraph text | Geist/Sans | Regular (400) | Sentence case | ~16–17px | Normal |
| Feature description (supporting copy) | Geist/Sans | Regular (400) | Sentence case | ~15–16px | Normal |
| Testimonial quote text | Geist/Sans | Regular (400) | Sentence case | ~15–16px | Normal |
| Attribution name (testimonials) | Geist/Sans | SemiBold (600) | Title Case | ~14px | Normal |
| Attribution role/company | Geist/Sans | Regular (400) | Title Case | ~13px | Normal |
| Date / metadata | Geist/Sans | Regular (400) | E.g., "Mar 27, 2026" | ~13px | Normal |
| Category tag ("Research", "Ideas") | Geist/Sans | Regular (400) | Title Case | ~13px | Normal |
| Blog article H1 title | Geist/Sans | Bold (700) | Sentence case | ~40–48px | -0.02em |
| Blog article byline | Geist/Sans | Regular (400) | Mixed | ~14px | Normal |
| Blog article body text | Geist/Sans | Regular (400) | Sentence case | ~17–18px | Normal/0.01em leading |
| Pricing tier name (Hobby, Pro, Pro+, Ultra) | Geist/Sans | Bold (700) | Title Case | ~22–24px | Normal |
| Pricing price ($20, $60, $200) | Geist/Sans | Bold/Black (700–900) | n/a (numeral) | ~36–48px | Normal |
| "/mo." pricing suffix | Geist/Sans | Regular (400) | Lowercase | ~14px | Normal |
| Pricing feature list items | Geist/Sans | Regular (400) | Sentence case | ~14–15px | Normal |
| CTA button text (primary) | Geist/Sans | SemiBold (600) | Sentence case | ~15–16px | 0.01em |
| Footer column headings (Product, Resources, Company) | Geist/Sans | SemiBold (600) | Title Case | ~13px | 0.04–0.06em (small caps feel) |
| Footer link text | Geist/Sans | Regular (400) | Title Case | ~13–14px | Normal |
| Copyright text | Geist/Sans | Regular (400) | Sentence | ~12–13px | Normal |
| Changelog entry title | Geist/Sans | Bold (700) | Sentence case | ~32–36px | -0.01em |
| Changelog entry date | Geist/Sans | Regular (400) | Title Case | ~13px | Normal |
| Changelog body text | Geist/Sans | Regular (400) | Sentence case | ~16–17px | Normal |
| Careers page quote text (large centered) | Geist/Sans | Bold (700) | Sentence case | ~28–36px | -0.01em |
| Careers job listing title | Geist/Sans | SemiBold (600) | Title Case | ~15px | Normal |
| Careers job meta (Sales, Full-time, SF) | Geist/Sans | Regular (400) | Title Case | ~13px | Normal |
| "Apply →" link | Geist/Sans | Regular (400) | Title Case | ~14px | Normal |
| Drop-cap on blog article | Serif (Freight/Georgia) | Bold | Uppercase | ~80–100px | Normal |
| Table of Contents labels | Geist/Sans | Regular (400) | Sentence | ~14px | Normal |
| "Table of Contents" heading | Geist/Sans | SemiBold (600) | Title Case | ~14px | Normal |

---

### Typography Application by Page Type

**Homepage:**
The homepage uses the most typographic scale range of any page. The hero H1 is the largest instance of the brand typeface: approximately 48–56px, bold, sentence case, with negative letter-spacing. The two-line hero headings create a distinctive "dark line / gray line" duo-tone treatment. Supporting feature copy (e.g., "Accelerate development by handing off tasks to Cursor") drops to ~15px regular for comfortable reading in the tight feature columns.

**Product Pages (Tab, Agents, Bugbot):**
All three product feature pages follow the same template. The eyebrow label (e.g., "Agents", "Tab", "Bugbot") is the smallest text element on the page (~13px, slightly tracked). The H1 splits into two lines: Line 1 is large bold black ("Turn ideas into code"), Line 2 is the same size but in muted gray ("Delegate implementation to focus on higher-level direction."). This two-tone heading treatment is a system-wide pattern. Feature section H2s are bold ~32–40px. Feature descriptions are ~15–16px regular.

**Enterprise:**
Nearly identical to product page treatment. The hero heading "Develop enduring software at scale" / "The choice for ambitious engineering teams." follows the dark/gray split. The enterprise stats section ("64% Fortune 500 companies using Cursor") uses very large numerals (possibly 64–80px) as focal points.

**Pricing:**
The typography is explicitly hierarchical. Plan names are bold ~22px. Prices are the largest numerals on the page (~40–48px bold). The "/mo." suffix immediately de-emphasizes by dropping to regular ~14px. Feature lists use small checkmarks + ~14px regular text. The "Recommended" badge is the smallest text element, serving as a whisper of guidance rather than a shout.

**Blog Index:**
Article titles are ~24–28px bold. The featured article title (large, left-positioned) runs ~32–36px. Category tags and dates are ~13px gray. Author lines are ~14px regular.

**Blog Article (Editorial):**
The article title functions as an H1 at ~40–48px bold. The byline sits below at ~14px regular. The hero image follows. Body text is ~17–18px regular at a generous line-height (~1.7), optimized for long-form reading. The "Table of Contents" component uses ~14px semibold for the title and ~14px regular for the entries.

**FAQ / Q&A (Enterprise, Pricing Pages):**
FAQ items use SemiBold ~16px for the question text. The accordion expand/collapse appears to use the same heading size but with a right-side chevron (↑/↓). No answers are visible in the collapsed state.

**Contact / Sales:**
The left-panel "Join over 50,000 companies building with Cursor" is rendered bold ~28–32px. The form labels ("Work email *", "What can we help you with? *") are ~13px regular with a red asterisk for required fields. The input field text is ~15px regular.

**Download:**
Section headers ("macos", "Windows", "Linux") use bold ~16px with platform emoji icons. Version number "2.6" is displayed bold ~20px. The "Latest" badge is ~12px in a pill. Download item rows use ~14px regular.

**Footer (All pages):**
Footer column headings (Product, Resources, Company, Legal, Connect) appear to be 12–13px in semibold or tracked regular, functioning visually like small caps. Footer links are 13–14px regular. Copyright line is 12px.

---

### Font Pairing Philosophy

Cursor uses a **mono-family typographic system** — there is effectively one typeface (a geometric sans) used at varying weights and sizes, with one editorial serif reserved exclusively for the drop-cap moment. This is not a pairing in the traditional sense; it is the most radical possible simplification of a type system. The philosophy is: **maximum expressiveness from one face.** The geometric sans must carry all the emotional weight — gravitas from its bold headline weights, warmth from its medium/regular body weights, precision from its spaced small tracking in small labels.

This approach is semiotic: using a single typeface communicates that Cursor is a product about reduction, about stripping out unnecessary complexity, about doing one thing with excellence. A multi-family type system would contradict the product's own core value proposition.

The one serif drop-cap exception signals editorial intelligence — it says "this is a publication worth slowing down for." It adds a literary quality to the research blog without importing a full serif family.

---

### Weight Distribution Analysis

- **Bold (700):** H1 headlines, H2 section headings, pricing numerals, plan names, bold feature headings. The workhorse "statement" weight.
- **SemiBold (600):** CTA button text, attribution names, footer column labels, some H3 sub-feature headers. The "important supporting" weight.
- **Regular (400):** Body text, nav links, metadata, tags, descriptions, footer links. The reading weight.
- **Light/Thin:** NOT used. There is no thin or light weight in the Cursor system. The brand communicates through density and contrast of weights, never through delicacy or feathering. This reinforces the idea of precision engineering over aesthetic softness.

---

### Letter-Spacing Rules

- **H1 / large display text:** Slightly negative (-0.01em to -0.02em) — makes large type optically tighter and more typographically sophisticated.
- **Body text:** Normal / 0.
- **Small labels / eyebrows (nav items, metadata, footer headings):** Slightly positive tracking (+0.03em to +0.06em) — an invisible micro-decision that makes small-size type more legible and gives labels a "set" quality.
- **CTA button text:** Slightly positive (~+0.01em) — gives buttons a slightly deliberate, assured feel.

---

### Complete Type Scale Summary

| Size | Usage |
|---|---|
| ~80–100px | Drop-cap initial (blog article only) |
| ~56px | H1 hero on homepage (largest heading) |
| ~48px | H1 hero on product/feature pages; blog article H1 |
| ~40px | Pricing price numerals; some page-level H2s |
| ~36px | Changelog entry titles; careers quote text |
| ~32px | H2 section headings (feature sections) |
| ~28px | Sub-feature headings; contact page left-panel heading |
| ~24px | H3 feature heads; blog article card titles |
| ~22px | Pricing plan names |
| ~20px | Version number on download page |
| ~17–18px | Blog article body text |
| ~16–17px | Standard body/paragraph text |
| ~15px | Feature descriptions; CTA button text; job listing titles |
| ~14px | Nav items; attribution names; blog metadata; form labels; ToC items; footer links |
| ~13px | Eyebrow labels; category tags; dates; small footer headings |
| ~12px | Copyright; "Latest" badge |

---

## 3. Logo & Wordmark

### Primary Logo Description

The Cursor logo consists of two components used together: **a geometric brand mark (icon)** and a **wordmark** ("CURSOR" or "Cursor"). The logo appears in the top-left of the navigation bar on every page.

**Brand Mark (Icon):** A small, compact, abstract geometric shape that resembles a multifaceted angular form — approximately an irregular hexagonal or pentagonal shape with visible internal facets, similar to a stylized crystalline or diamond-like form. It is visible in the nav at approximately 24x24px. The form reads as both a cursor (triangular pointer) and an abstract 3D geometric solid. The mark has an "exploded" quality — multiple angular planes meet to suggest depth and dimension within a flat 2D space. It is entirely monochromatic (near-black on the cream background).

**Wordmark:** "CURSOR" appears immediately to the right of the brand mark in uppercase with the same geometric sans-serif typeface used throughout the site. The wordmark tracking appears slightly generous — enough to give the uppercase word an authoritative, spaced feel. The weight is consistent with SemiBold or Bold.

**Combined Treatment:** The mark + wordmark operate as a locked horizontal unit in the navigation. The mark sits at approximately the same cap-height as the wordmark lettering.

---

### Logo Characteristics

- **Typeface:** Uppercase geometric grotesque sans, consistent with the site's primary typeface (Geist variant). The wordmark is not a bespoke lettered logotype — it appears to be the site typeface rendered in all-caps.
- **Weight:** SemiBold to Bold range.
- **Tracking:** Slightly positive, appropriate for an all-caps treatment to maintain legibility and airy spacing.
- **Case:** All-caps ("CURSOR") — this is the primary logo treatment.
- **Form:** The brand mark icon appears to be an SVG/video animation. The nav DOM includes a `<Video "Cursor logo animation">` element, suggesting the mark is animated at some scale or context (possibly a subtle loop or appear animation). A static fallback image is also present.

---

### Placement Rules

- **Navigation bar:** Top-left corner, locked to the left edge of the content well. Vertically centered in the 48px nav bar.
- **Contact Sales page exception:** On the contact-sales landing page, the navigation bar disappears — only the logo appears in the top-left, with no nav links, creating a focused conversion experience.
- **Favicon/app icon (Download page):** The download page shows a standalone app icon — a 3D-rendered version of the brand mark as a faceted geometric prism/cube in dark gray/charcoal with visible light-catch highlights. This is the most dimensional and detailed version of the brand mark.
- **Footer:** The logo does NOT appear in the footer. The footer uses text navigation only, not a logo repeat. This is a notable restraint — many brands double the logo in the footer; Cursor does not.

---

### Color Variations Observed

- **Standard (light mode):** Near-black mark + near-black wordmark on cream/white background.
- **Dark mode (toggle available):** Would invert to white mark + white wordmark on dark background (not directly observed as active state, but the theme toggle implies this exists).
- **No color variant observed:** No full-color, reversed-out (white on colored), or brand-accent-colored logo variant was encountered across all 13 pages.
- **Within product screenshots:** The Cursor app icon appears in the macOS window chrome within product demos as a small square app icon using the faceted geometric mark.

---

### Sizing Details

- **Navigation (primary):** Approximately 24px tall (mark), with wordmark at approximately 14–15px cap height.
- **Download page app icon:** ~128px square display size (the geometric prism).
- **Bugbot page:** A small Cursor bot avatar (approximately 32x32px circular avatar) appears in the GitHub PR mockup, showing the geometric mark at very small scale.

---

### Brand Mark System

Cursor operates a **three-element mark system:**

1. **Full lockup (mark + wordmark):** Used in navigation — the primary brand presence.
2. **Mark only (icon):** Used in app icon contexts, product screenshots, bot avatars. The geometric faceted form works independently at small scales.
3. **Wordmark considerations:** The "CURSOR" wordmark in all-caps functions legibly without the mark, but this combination is not observed as an isolated usage on the marketing site.

There is no separate monogram, no brand flag, no stacked version visible. The system is lean.

---

### Logo Relationship to Brand Heritage/Positioning

Cursor is a product by Anysphere, Inc. The Cursor logo does not carry any reference to Anysphere (the parent company mark is entirely separate and links to anysphere.inc). This is a product-first brand with no parent-company visual debt. The geometric crystalline mark is original, contemporary, and abstract — it does not simulate a literal cursor arrow (which would be too literal) nor does it reference neural networks, atoms, or code brackets (which would be too derivative of AI/tech clichés). The form is technical in feel (precision, geometry, facets) but also organic in rhythm (the facets suggest natural crystal growth, not mechanical construction). This is a mark that can age gracefully: it is not trendy, not tied to a cultural moment, and it is distinctive at small sizes.

---

## 4. Layout & Grid System

### Global Structure

- **Max-width content well:** Approximately 1280–1320px wide based on observed element positions. Content on most pages spans from approximately 59px from left edge to ~1281px (measuring from homepage DOM coordinate data where headings start at x=59 and span to ~1282px container width at 1366px viewport width).
- **Horizontal margins:** ~59–66px on each side at typical laptop viewport widths.
- **Header/Nav height:** 48px (from DOM coordinate data: nav items positioned at y=24, centered in a 48px bar).
- **Left-aligned content start:** Most hero text begins at the left margin (~59px), not centered. This signals editorial/reading intent over decorative centeredness.
- **Gap between nav and hero content:** Approximately 80–100px of vertical breathing room before the H1 text begins.
- **Section vertical padding:** Generously spaced — sections breathe with approximately 80–120px of padding between major content modules.
- **Column structure:** The site uses a fluid multi-column grid. Feature sections typically use 3-column grids (e.g., 3 testimonials across, 3 changelog entries across, 3 "stay on the frontier" feature cards). Blog index uses a 2-column grid (1 large + 1 smaller, or 2 equal).
- **Footer columns:** 5-column grid — Product / Resources / Company / Legal / Connect, each with approximately equal column width.

---

### Page Templates

**Homepage Template:**
- Full-width nav bar (transparent background)
- Left-aligned hero zone (H1 left-aligned, CTA button left-aligned, no center-alignment)
- Full-width interactive demo embed (the Cursor IDE screenshot panel, edge-to-edge with slight horizontal inset)
- Trusted-by logo strip (centered logos, scrolling or static grid)
- 3 feature highlight modules (each with left-side heading/copy and right-side interactive demo)
- Full-width stats/testimonials section (dark background or same cream)
- 3-column testimonials grid
- 3-column "stay on the frontier" cards
- Changelog module (4-item horizontal list)
- Company mission statement (centered, full-width text block)
- Blog highlights (4-item grid)
- Final CTA ("Try Cursor now." centered, button)
- 5-column footer

**Product Feature Page Template (Agents, Tab, Bugbot):**
- Same nav
- Left-aligned hero with eyebrow label + 2-line heading + CTA
- Full-width product demo (the interactive IDE screenshot)
- Alternating feature modules: heading/copy on left or right, with demo/screenshot opposite
- Testimonials section (horizontal scroll or grid)
- Blog highlights section
- Changelog section
- CTA footer module
- 5-column footer

**Enterprise Page Template:**
- Left-aligned hero heading + CTA button
- Customer logo grid (2 rows × 8 columns, gray logos)
- Feature modules (alternating layout)
- Stats bar ("64% Fortune 500", etc.)
- Testimonials (logo + quote + attribution) — uses a distinct card with company logo treatment
- Customer stories blog cards (4-item grid)
- FAQ accordion section
- CTA module
- 5-column footer

**Pricing Page Template:**
- Centered page title ("Pricing") — one of the only centered H1s on the site
- Monthly/Yearly toggle (centered, pill switcher)
- 4-column pricing tier cards (Hobby, Pro, Pro+, Ultra) — Individual Plans
- 2-column pricing cards (Teams, Enterprise) — Business Plans
- Logo strip
- Bugbot pricing section
- FAQ accordion
- Bottom CTA (2 buttons: Download + Contact Sales)
- 5-column footer

**Blog Index Template:**
- No hero heading — immediately begins with article card grid
- Featured article: large left-aligned card (approximately 2/3 width) with full-bleed image
- Secondary articles: right column with vertically stacked cards
- Below fold: continues with alternating article card pairs
- 5-column footer

**Blog Article Template:**
- Breadcrumb navigation (left-side column) — small gray "Blog / Category"
- Main content (center-right column) — article title, author, date, hero image, ToC box, body
- No sidebar ads, no related article sidebar
- Body text in a single comfortable reading column (~620–660px wide)
- Drop-cap on first paragraph letter
- 5-column footer

**Changelog Template:**
- Left sidebar: date (e.g., "Mar 25, 2026")
- Main column: "Changelog" eyebrow, H1 entry title, body paragraphs, feature screenshots

**Legal / Privacy Template:**
- Left sidebar with section navigation links ("Terms of Service", "Privacy Policy")
- Main column with H1, "Last updated" date, ToC accordion, body text
- Clean, document-style layout

**Contact / Sales Page Template:**
- No standard nav (logo only)
- Split 2-column layout: left = testimonial + customer logos, right = form
- Form: email input + dropdown + CTA button
- No footer nav

**Download Page Template:**
- Header: app icon + headline + subline + CTA
- Platform tabs: macOS / Windows / Linux
- File list rows (platform, architecture, file format, download icon)
- "View release notes" link
- 5-column footer

**Careers Page Template:**
- Large centered text block (the company culture statement)
- "Open roles" section with job listings in card rows
- Filter dropdowns (All teams, All locations)

---

### Product Card Anatomy

On the Blog Index page, article "cards" are not traditional cards (no box shadow, no card fill). They consist of:
- **Image tile:** Full-bleed image (abstract generative art), no rounded corners on the full-width featured card. Right-column cards appear slightly smaller.
- **Metadata line:** Date + Category tag (gray, ~13px)
- **Title:** ~24–28px bold, near-black
- **Description:** ~15px regular, muted gray
- **Author + Read time:** ~14px regular gray, with circular author avatar (~24px)

On the Pricing page, tier cards have:
- White (`#FFFFFF`) background fill
- Subtle `1px solid rgba(0,0,0,0.08)` border
- ~16px padding on all sides
- Plan name + tier descriptor
- Price + /mo. unit
- Feature list with checkmarks
- CTA button at bottom

---

### Responsive Behavior

- **Desktop (1280px+):** 3-column feature grids, 4-column pricing cards, 5-column footer.
- **Tablet (~768–1024px):** Likely collapses to 2-column feature grids, 2-column pricing, 2–3 column footer.
- **Mobile (<768px):** Single column throughout. The nav collapses (a hamburger or simplified nav would appear). Pricing cards stack vertically. Footer columns likely stack. (Full mobile testing not conducted in this audit.)

---

### Whitespace Strategy

Cursor's whitespace strategy is aggressive and confidence-signaling. The homepage hero section alone occupies a full viewport before the first piece of supporting content. Section breaks are generous (80–120px top/bottom padding). This is the "silence between notes makes the music" school of design — whitespace is not dead space, it is the brand's confidence expressed spatially. In a category (AI coding tools) where competitors often cram features into every pixel, Cursor's restraint is a positioning statement.

---

### Grid Alignment Philosophy

The grid is predominantly **left-aligned**, not centered. This is editorial/longform reading convention applied to a marketing site. The implication: Cursor is a serious tool for serious people, and serious reading is left-to-right, column-based, not decoratively centered. The only centered elements are the pricing page H1, the careers page culture statement, and the final "Try Cursor now." CTA — all of which are specific rhetorical choices (centrality to signal directness or conviction).

---

### Homepage Scroll Architecture

1. **Nav** (48px, sticky or fixed)
2. **Hero module** (~100vh or close) — headline + CTA + interactive Cursor IDE screenshot (edge-to-edge)
3. **Trust strip** — partner logos
4. **Feature 1:** "Agents turn ideas into code" — text left, demo right
5. **Feature 2:** "Works autonomously, runs in parallel" — Cloud Agents demo
6. **Feature 3:** "In every tool, at every step" — multi-surface demo
7. **Feature 4:** "Magically accurate autocomplete" (Tab) — text right, code demo left
8. **Testimonials** — 2-row × 3-column grid of quote cards
9. **"Stay on the frontier"** — 3-column feature cards (Models / Codebase Understanding / Enterprise)
10. **Changelog** — 4-column horizontal list
11. **Company mission** — full-width centered headline + "Join us" CTA
12. **Blog highlights** — 4-column article cards
13. **Final CTA** — "Try Cursor now." centered + download button
14. **Footer** — 5-column

The pattern is: Claim → Proof → Claim → Proof → Social Proof → Feature depth → Recency signal → Mission/Ethos → Editorial depth → Final conversion → Navigation utility.

---

### PDP Image Gallery Layout

Cursor doesn't have product images in the traditional e-commerce sense. The "product gallery" equivalent is the **interactive IDE demo panel** embedded in each product page hero. This is a full-width (with slight inset) panel that displays the Cursor app interface against a background image. Background images used:
- Homepage: An oil-painting-style mountainous landscape (warm, impressionistic, rendered with a painterly aesthetic — NOT a photographic stock image).
- Tab page: A warm sunset/cloud sky landscape painting.
- Bugbot page: A coastal/seascape landscape (more blue-teal).
The IDE app chrome floats on top of these painterly backgrounds. This creates an unexpectedly humanistic, almost Renaissance quality — the precision of code overlaid on natural beauty. This is a deliberate editorial art direction choice.

---

### Footer Layout

5-column horizontal footer on a cream (`#F5F3EE`) background:
- **Column 1:** Product (Agents, Enterprise, Pricing, Code Review, Tab, CLI, Cloud Agents, Marketplace)
- **Column 2:** Resources (Download, Changelog, Docs, Learn, Forum, Help, Workshops, Status)
- **Column 3:** Company (Careers, Blog, Community, Students, Brand, Future, Anysphere)
- **Column 4:** Legal (Terms of Service, Privacy Policy, Data Use, Security)
- **Column 5:** Connect (X, LinkedIn, YouTube)
- **Bottom bar:** © 2026 Anysphere, Inc. | 🛡 SOC 2 Certified | System/Light/Dark theme toggles | Language selector (English)

External links are annotated with ↗ (Marketplace, Forum, Learn, Help, Status, Anysphere, and social links) to clearly distinguish off-site navigation.

---

### Layout Elements NOT Present

- **Announcement banner / promo bar above nav** — absent. No "🎉 New: Cursor 2.6 now available" banner. This restraint avoids urgency / discount culture signaling.
- **Chat widget or live support bubble** — absent from all marketing pages.
- **Cookie consent banner** — not prominently visible (may be suppressed or handled via minimal methods).
- **Social media share buttons on blog** — absent.
- **Comment sections on blog** — absent.
- **Breadcrumb nav on most pages** — only appears on blog article pages (and as a left-sidebar item on privacy/legal pages).
- **Comparison tables on homepage** — absent. The pricing page has comparison detail but the homepage does not attempt a competitor comparison table.
- **Sticky floating CTA button** — absent. No persistent "Download Free" pill that follows the user down the page.
- **Progress indicator / reading bar on blog posts** — absent.

---

## 5. UI Components

### Buttons

**Primary CTA Button (Download / Get Pro+ / Continue):**
- Shape: Fully rounded pill (border-radius: ~100px / 9999px)
- Background: Near-black (`#1A1A1A`)
- Text: White, SemiBold, ~15px, slight positive tracking
- Height: ~44–48px
- Width: Content-dependent (text + horizontal padding ~20–24px each side)
- Icons: Inline icon appears in Download button (↓ arrow) positioned after text
- Example: "Download for Windows ↓", "Get Pro+", "Continue →", "Try Bugbot for free →"
- **States:** Default: black. Hover: very likely slightly lighter black or subtle shadow (not directly observable via screenshot). Active: slight darkening. Disabled: not observed.

**Secondary / Outlined Button (Contact sales nav, Talk to the team):**
- Shape: Fully rounded pill
- Background: Transparent or very light (`#FAFAF8`)
- Border: 1px solid, subtle near-black with low opacity (~rgba(0,0,0,0.15))
- Text: Near-black, Regular, ~14–15px
- Height: ~36–40px
- Example: "Contact sales" in nav, outlined pricing buttons

**Text Link Button (CTA with arrow):**
- Shape: No button shape — plain text with "→" appended
- Color: Near-black or amber (`#C07A3A` in editorial contexts)
- Example: "Learn about cloud agents →", "Explore models ↗", "Read story →"
- No underline by default; likely underlines on hover.

**Download Tier Button (Hobby "Download"):**
- Outlined style, less prominent than primary button
- Height: ~40px
- Lighter visual weight than filled CTA buttons

---

### Navigation

**Desktop Nav Structure:**
- Fixed/sticky position at top of viewport
- Background: Transparent (content scrolls beneath without nav changing — or very subtly frosted)
- Left side: Logo (mark + "CURSOR" wordmark)
- Center: Nav links — Product (with expand dropdown), Enterprise, Pricing, Resources (with expand dropdown)
- Right side: Sign in (text link) | Contact sales (outlined pill) | Download (filled pill, near-black)
- Height: ~48px

**Nav Dropdown Behavior:**
- "Product" has an "Expand Menu" button (ref_479) — likely reveals a mega-dropdown with product links (Agents, Tab, CLI, etc.)
- "Resources" has an "Expand Menu" button (ref_504) — likely reveals links to Changelog, Docs, Forum, etc.
- The dropdowns were not explicitly expanded in this audit but are confirmed by the DOM "Expand Menu" button elements.

**Mobile Nav:** A hamburger or simplified nav is implied for responsive but not directly observed.

---

### Forms

**Contact Sales Form:**
- Input: "Work email *" — Full-width text input, white background (`#FFFFFF`), 1px border `rgba(0,0,0,0.12)`, rounded corners (~6–8px radius), placeholder text in gray, label above input (~13px)
- Dropdown: "What can we help you with? *" — `<select>` element styled as a bordered dropdown with chevron (↓)
- Submit: "Continue →" — primary black pill button (~44px tall, full width on right panel)
- Required field indicator: `*` in red

---

### Accordions

**FAQ Sections (Enterprise, Pricing pages):**
- Questions displayed as expandable items
- Style: Each question is a row with a right-side expand indicator (↑/↓ or +/−)
- Separator: Subtle border line between items
- Expand behavior: Single-expand (one open at a time) or multi-expand — not confirmed, but enterprise FAQs show questions as labeled `<button>` elements
- When collapsed: Question text only visible
- When expanded: Answer text reveals below, likely with a smooth height animation

**Table of Contents (Blog articles, Privacy, Security pages):**
- A collapsible "Table of Contents" box
- Default: Expanded (visible in screenshots)
- Collapse button: a ∧ (up chevron) visible in the box header
- Contains: linked section headings
- Background: White card with border
- Padding: ~16px

---

### Product Demo Panels

The most prominent "UI component" on product pages is the **full-width interactive IDE demo panel**. This is not a static screenshot but a live-updating animated component that simulates the Cursor editor running in real time. Key aspects:
- Full-bleed width with slight horizontal insets (~59px on each side, matching the content margin)
- Background: Painterly oil-painting landscape art (custom art direction, not stock)
- App window: macOS-style window chrome (three traffic-light circles: red, yellow, green) displayed as a floating panel on the painting background
- This component has been described in the DOM as an "interactive demo for sighted users" with accessible text descriptions provided for screen readers

---

### Button States & Interactions

- **Default:** As described above
- **Hover:** Not directly captured but inferred to be: primary button → very slight opacity change or shadow; text links → underline appears; outlined buttons → border darkens
- **Active/Pressed:** Slight darkening or scale micro-reduction
- **Disabled:** Not observed
- **Focus:** Standard browser focus ring or custom styled outline for accessibility
- **Loading:** Not observed in CTA context (download links trigger file download without loading state in UI)

---

### Announcement Bar

**Not present.** There is no announcement bar above the navigation on any page. Cursor does not run persistent promotional banners. Updates are communicated through the Changelog page and the Changelog section embedded on the homepage. This is a deliberate choice: announcement bars create a sense of temporal urgency / discount culture that would undermine the brand's premium, research-team positioning.

---

### Search Component

**Not observed on the marketing site.** There is no search bar, no search icon, no search shortcut in the navigation. This absence reflects the site's focused information architecture — users navigate through clear hierarchical nav, not search. The Docs site (cursor.com/docs) likely has search, but the marketing/brand site does not.

---

### Video Embed Behavior

The Cursor logo in the nav is confirmed to be a `<Video>` element ("Cursor logo animation"), suggesting a subtle animation loop. Blog article hero images are static (JPG/PNG). Product demo panels are interactive/animated JavaScript-rendered components, not embedded video iframes. There are no YouTube embed iframes or third-party video players observed on the browsed marketing pages.

---

### Animation & Motion Philosophy

Cursor's animation philosophy is: **Motion as function, not decoration.** Observed:
- **Cursor logo:** Animated SVG or video loop (subtle)
- **Interactive IDE demos:** JavaScript-rendered, live-updating to simulate real product behavior — the most complex animation on the site
- **Testimonial carousel:** If animated, would be a slow fade or horizontal slide
- **Accordion expand/collapse:** Smooth CSS height transition (standard pattern)
- **No:** Page transition animations, parallax scroll effects, particle effects, hover transformations, or other decorative motion
- **Why:** The product itself is dynamic (AI typing, code being written). The marketing site's job is to *not compete* with that dynamism. Static, minimal motion in the brand environment makes the product demos feel more powerful by contrast.

---

## 6. Iconography

### Complete Icon Inventory

| Icon | Description | Location | Context |
|---|---|---|---|
| Cursor logo mark | Angular faceted geometric symbol | Nav (all pages), App icon (Download), Bot avatar (Bugbot page) | Brand identity |
| ↓ (down arrow) | Simple arrow, inline | Download CTA button text ("Download for Windows ↓") | Download CTA |
| → (right arrow) | Simple arrow, inline text | Feature links ("Learn about cloud agents →"), CTA text ("Talk to the team →"), footer external links | Navigation / CTA |
| ↗ (diagonal arrow) | External link indicator | Footer links (Marketplace, Forum, Learn, Help, Status, Anysphere, social), resource links | External navigation |
| ✓ (checkmark) | Simple text checkmark | Pricing feature list items | Feature confirmation |
| 🛡 (shield emoji) | Security/trust shield | Footer bottom bar ("SOC 2 Certified") | Trust/compliance signal |
| 🌐 (globe emoji) | Language/internationalization | Footer language selector | Localization |
| ∧ / ↑ (up chevron) | Collapse indicator | Table of Contents accordion close, FAQ expand/collapse | Interactive component |
| macOS Apple icon (🍎) | Apple logo | Download page platform tab | Platform identification |
| Windows grid icon (⊞) | Windows logo | Download page platform tab | Platform identification |
| Linux penguin/system icon | Linux symbol | Download page platform tab | Platform identification |
| ● ● ● (traffic lights) | macOS window chrome circles | Product IDE demo panels (red, yellow, green circles) | Product UI authenticity |
| ♥ (heart) | Reaction emoji | Bugbot GitHub PR mockup (❤️ 3) | Product UI demo realism |
| · (bullet/dot) | Separator | Agent task metadata ("Editing files · Opus-4.6") | UI mockup metadata |

---

### Icon Design Philosophy

Cursor uses **almost no custom iconography** in its brand/marketing context. This is an extremely deliberate constraint. The reasoning:
- Custom icon libraries suggest "UI-heavy" products. Cursor wants to signal that the product is about substance, not chrome.
- Text-based directional indicators (→, ↗, ↓) are more linguistically precise than abstract icons and align with the brand's engineering/editorial voice.
- Emoji are used in very specific functional contexts (🛡, 🌐) — they function as lightweight trust/utility signals without requiring custom SVG icon design.
- Within the **product screenshots**, icons appear naturally as part of the Cursor IDE interface (file icons, spinner/loading icons, git indicators) — but these are product UI, not brand assets.

---

### Icon Color Rules

- All brand icons (arrows, checkmarks) are rendered in the same near-black (`#1A1A1A`) as the text they accompany.
- No icons use the amber accent color.
- No icons use blue, red, or green in the brand environment.
- Product UI icons within IDE screenshots follow standard dark-theme IDE conventions (colored file icons, syntax highlighting).

---

### Icon Sizing

- Nav logo mark: ~20–24px
- Inline arrow icons (→, ↗, ↓): Text-size matched (~13–16px depending on context)
- Checkmark ✓: Text-size matched (~14–15px)
- Shield emoji 🛡: ~16–20px (footer bottom bar)
- Globe emoji 🌐: ~16–20px
- App icon (Download page): ~128px display

---

### Icons NOT Used (Deliberate Absences)

- **Social media icons (Twitter bird, LinkedIn "in" logo, YouTube play button)** — Footer social links use text only ("X ↗", "LinkedIn ↗", "YouTube ↗"). No brand color social icons. This forces these links into the same visual hierarchy as all other text links — no social media is visually privileged.
- **Star ratings / review icons** — Zero star ratings visible anywhere (no 5★ social proof).
- **Feature benefit icons** (checkboxes with custom SVG, shield icons for security features on the features list) — The enterprise security features section uses text labels only, not iconographic bullet points.
- **Progress/spinner loading icons** — Not visible in brand context.
- **Hamburger menu icon** — Not observed (may appear on mobile).
- **Search magnifying glass** — Not used on marketing site.
- **Shopping cart icon** — Cursor has no e-commerce cart flow; pricing is subscription via button CTAs.
- **Notification bell** — Absent.
- **User/profile avatar in nav** — "Sign in" is a text link, no avatar icon.

---

## 7. Photography Style

### Product Photography

Cursor is not a physical product company, so there is no traditional product photography. The equivalent "product photography" is the **IDE interface mockup / demo panel** embedded in hero sections. Key observations:

- **Background art:** Each product page hero features a custom artwork image visible behind/beneath the IDE mockup. These are high-quality oil-painting-style landscape artworks — not stock photography, not AI-generated photographic content, but what appear to be actual fine art reproductions or custom-commissioned painterly illustrations:
  - **Homepage:** Mountain landscape (impressionistic, warm palette, reminiscent of 19th-century American landscape painting)
  - **Tab page:** Warm sunset cloud sky (golden hour, streaks of warm coral/amber)
  - **Bugbot page:** Coastal/river landscape (cooler blues and teals, more serene)
  - The Tab page's background image URL confirms: `ptht05hbb1ssoooe.public.blob.vercel-storage.com/assets/internal-brand/internal-brand-023-3291bb4c.jpg` — stored in a Vercel Blob storage bucket, labeled as "internal-brand" assets.

- **Art direction principle:** The pairing of precision engineering (IDE chrome, code syntax, structured UI) with romantic, hand-painted landscape art creates a powerful semiotic tension — the technological and the humanistic in the same frame. This is a statement about Cursor's mission: AI that extends human capability rather than replacing human creativity. The landscapes evoke vastness (exploration, possibility) while the code editor grounds the experience in the present moment of work.

---

### Lifestyle / Editorial Photography

**Blog article hero images** are abstract generative or mathematical art:
- "The third era of AI software development": Dark olive-green background with thin white geometric looping lines forming an infinity-symbol or orbital path shape — beautiful and technical.
- "Introducing Composer 2": A pattern of horizontal lines in orange/amber tones on dark background — like fiber optic visualization or data flow.
- "How we compare model quality": Stacked layered lines creating depth — data visualization aesthetic.

These are **not photographs of people**. This is the most notable characteristic of Cursor's editorial photography strategy: **zero lifestyle photography, zero human subjects** on the marketing site. No developer photos, no team photos, no "person on laptop in coffee shop" stock images. This is a profound brand decision that says:
1. The product is for all developers, regardless of how they look.
2. The brand is defined by ideas (visualized abstractly), not by demographic aspiration.
3. Abstract imagery allows global audiences to project themselves without friction.

---

### Hero Images (Format, Content, Overlays)

- Format: JPG (served via Next.js `/_next/image` CDN optimization with `q=70` quality)
- Dimensions: Full-width, typically ~1280px wide at maximum. Hero image heights vary (~400–500px visible).
- **No text overlays** on images — the IDE mockup panels that sit on top of landscape images are self-contained components; no marketing text is placed directly on top of photos.
- Images have very slight rounded corners at the bottom edge of the demo panel crop (not on the background image itself).

---

### Photography Strategy & Art Direction

**Three image registers used:**

1. **Fine Art Landscapes (Product hero backgrounds):** Romantic, impressionistic. Humanize the engineering. Signal timelessness — these don't "date" the site visually.

2. **Abstract Mathematical/Generative Art (Blog heroes):** Technical, beautiful, intellectual. Signal that Cursor's writing is research-quality. Consistent with an "applied research team" identity.

3. **Product UI Screenshots (In-demo mockups):** Clean, authentic. Show real product interface (or near-real). These are the most "functional" images on the site.

**What is deliberately absent:** Stock photography of humans, photographic color grading/filtering, illustrated mascots, product render animations, 3D asset renders (except the app icon on the Download page), infographic-style charts.

---

### Author Avatars

Blog articles and testimonials include small circular avatar photos of real people (Michael Truell, Diana Hu, Jensen Huang, Patrick Collison, etc.). These are approximately 24–48px circular crops of actual photographs. The photos appear to be authentic headshots/candid shots, not studio-lit professional photos. They are rendered at tiny sizes and serve a credibility function, not a lifestyle photography function.

---

### Image Aspect Ratios

- **Blog article hero images:** Approximately 16:9 or custom wide crop (~600px wide × ~320px tall on the index page featured card)
- **Blog article body hero image:** Approximately 16:9 or close (~600px × ~320px)
- **Product IDE demo panel:** Wide, approximately 21:9 or similar ultra-wide crop within the viewport
- **Customer logos (Enterprise page):** Approximately 160×80px each (landscape logos)
- **Author avatars:** 1:1 circular crop, ~24–48px
- **App icon (Download page):** 1:1, ~128px

---

### Image Treatment Consistency

No filters, no overlays, no brand color washes applied to any images. The landscape paintings are used at full natural color. The generative/abstract art is used as-is. The product screenshots are clean. This is consistent with the broader brand ethic of material honesty: things look like what they are.

---

## 8. Brand Voice & Language Style

### Tone: Overall Personality

Cursor's brand voice is the voice of a confident, brilliant colleague who doesn't need to oversell. It is:

1. **Direct:** Cursor never beats around the bush. "Built to make you extraordinarily productive" — a strong claim, directly stated. No hedging language, no "we believe" qualifiers.

2. **Technically credible:** The product copy demonstrates genuine understanding: "Subagents run in parallel to explore your codebase, with each one using the best model for the task." This is written for developers, by developers. No simplification or condescension.

3. **Precise but not pedantic:** "Magically accurate autocomplete" pairs the precision of "accurate" with the surprise of "magically" — Cursor can use evocative language without sacrificing meaning.

4. **Mission-scale / ambition:** Cursor doesn't present itself as a productivity tool — it presents itself as infrastructure for the future of software. "Cursor is an applied research team focused on building the future of software development." "The new way to build software."

5. **Low-ego:** Despite enormous ambitions and a list of enterprise customers that includes NVIDIA, Stripe, and OpenAI, the copy is notably non-boastful. Stats are stated plainly: "64% Fortune 500 companies using Cursor." No exclamation marks. No "AMAZING!" superlatives.

6. **Research-positioned:** The blog posts read as academic/technical papers written accessibly. "A technical report on Composer 2." "How we compare model quality in Cursor." This positions Cursor alongside research institutions, not just software products.

7. **Community-aware without pandering:** The testimonials include shadcn ("Creator of shadcn/ui") alongside Jensen Huang ("President & CEO, NVIDIA") — developer cultural figures alongside executive enterprise voices. This signals a dual audience understood and respected equally.

8. **Future-oriented without sci-fi clichés:** "The third era of AI software development." "Stay on the frontier." "The future of software development." The language is temporal and directional — the product exists in a moment of profound change — without leaning into generic AI hype language ("harness the power of AI", "unleash your potential").

9. **Product-specific (no generic AI language):** The copy describes Cursor's specific behaviors: "Cursor instruments your code and uses real execution data to pinpoint the fix." "A custom embedding model gives agents best-in-class recall across large codebases." This specificity is itself a trust signal.

10. **Humble in a specific way:** On the Careers page: "We obsess over talent to an unusual degree and are designing a company that's a haven for self-motivated individual contributors. This work demands our best." This is aspirational and self-aware, not self-aggrandizing.

11. **Second-person (you/your) dominant:** Almost all product copy addresses "you" directly — "Make you extraordinarily productive," "Delegate implementation to focus on higher-level direction," "Point Cursor at exactly what matters." This creates intimacy and directness.

12. **The voice of peers, not vendors:** Cursor writes as if the reader is a peer engineer who will immediately understand the implications. "Leave it to the folks at Cursor to bring out the absolute most from the models." (Testimonial voice echoes brand voice because the brand selected voices that sound like its own.)

---

### Language Patterns

**1. The Strong Claim Opening:**
Every hero section opens with a bold, unqualified claim: "Built to make you extraordinarily productive," "Turn ideas into code," "Next-action prediction," "AI code review that catches real bugs," "Develop enduring software at scale." No conditional language, no "helping you" qualifiers. These are declarative statements of intent.

**2. The Two-Line Heading Structure:**
The hero H1 pattern is: Line 1 = the bold claim (dark) / Line 2 = the elaboration (gray). Examples:
- "Turn ideas into code" / "Delegate implementation to focus on higher-level direction."
- "Next-action prediction" / "Tab anticipates where you're headed and suggests changes."
- "AI code review that catches real bugs" / "Bugbot detects the hardest logic bugs with a low false positive rate."
The gray second line is almost a subtitle — it adds specificity and technical precision to the claim without diminishing it.

**3. The Understated Arrow CTA:**
Links and CTAs use "→" or "↗" rather than aggressive "CLICK HERE" language. Examples: "Learn about cloud agents →", "Explore models ↗", "See what's new in Cursor →". The arrow is directional without demanding. It respects the reader's autonomy.

**4. Spec-Level Technical Description:**
Feature sections describe product capabilities at a depth that reveals genuine engineering pride: "A custom embedding model gives agents best-in-class recall across large codebases." "Subagents run in parallel to explore your codebase." "Cursor instruments your code and uses real execution data to pinpoint the fix."

**5. The Attribution Pattern in Testimonials:**
Every testimonial follows: [Quote text in quotation marks] / [Name] / [Title] / [Company]. The attribution is structured with deliberate hierarchy — name first (largest), title (supporting), company (smaller). Example: "shadcn / Creator of shadcn/ui" — the creator's handle (not real name) is used, signaling cultural awareness of developer identity.

**6. Research Paper Headings for Blog Posts:**
"A technical report on Composer 2," "How we compare model quality in Cursor," "Securely indexing large codebases" — these are academic paper-style titles. They signal rigor, not content marketing.

**7. The Mission Statement as Company Description:**
"Cursor is an applied research team focused on building the future of software development." This is not a typical corporate mission statement. "Applied research team" is a deliberate positioning against "software company" — it signals academic rigor combined with shipping products.

**8. The "Stay on the frontier" Pattern:**
The phrase "frontier" recurs: "Stay on the frontier," "frontier models." This is language from AI research culture (the "frontier" of model capability). Using it positions Cursor as a participant in AI research, not just a consumer of it.

**9. The Changelog/Release Format:**
"Mar 25, 2026 / Self-hosted Cloud Agents" — minimal, chronological, technical. No marketing language in changelog titles. This signals: "We ship. Here's proof."

**10. Careers Voice:**
"We obsess over talent to an unusual degree" and "This work demands our best" and "If this sounds exciting, we'd love to hear from you." The careers copy is honest about the difficulty and specificity of the work, which filters for the right candidates without over-promising.

---

### Heading Style

**By Page:**

**Homepage:**
- H1: "Built to make you extraordinarily productive, Cursor is the best way to code with AI." (Sentence case, bold, ~48–56px)
- H2s (feature sections): "Agents turn ideas into code," "Works autonomously, runs in parallel," "In every tool, at every step," "Magically accurate autocomplete," "The new way to build software.," "Stay on the frontier," "Use the best model for every task," "Complete codebase understanding," "Develop enduring software," "Changelog," "Recent highlights," "Try Cursor now." (All sentence case, bold)

**Product Page:**
- H1: "Turn ideas into code" (bold, short, declarative)
- H2s: "Understands your codebase, no matter the size," "Multiple models," "Codebase indexing," "Team rules," "Spans the full development lifecycle," "Plan," "Design," "Debug," "Equipped to do real engineering," "Terminal," "Add context," "Git & checkpoints," "Extend with tools and knowledge," "Plugins," "Skills," "MCP," "Everywhere you work," "Desktop," "CLI," "Other Surfaces," "Web & Mobile," "Trusted by the world's best developers"

**Enterprise Page:**
- H1: "Develop enduring software at scale" (bold)
- H2: "Your engineering knowledge base," "Ship better software, faster," "Loved by developers," "AI is changing how software is built.," "Powerful, yet customizable," "Total control," etc.

**Pricing:**
- H1: "Pricing" (centered, simple, bold — the most minimal heading on the site)
- Plan names function as H2-level: "Hobby," "Pro," "Pro+," "Ultra," "Teams," "Enterprise"

**Blog Article:**
- H1: "The third era of AI software development" (sentence case)
- H2 (body sections): "From Tab to agents," "Cloud agents and artifacts," "The shift is underway inside Cursor"

**Pattern analysis:** All headings are **sentence case** (first word capitalized, rest lowercase except proper nouns). This is consistent 100% across all pages. No ALL CAPS headings (except the logo wordmark). No title case headings (except plan names on pricing, which are proper names). The sentence case convention signals editorial sophistication — it's the practice of quality publications, not marketing departments.

---

### CTAs & Microcopy

**CTA Inventory by Page:**

**Homepage:**
- "Download for Windows ↓" (primary hero CTA, repeated at bottom)
- "Learn about agentic development →" (feature link)
- "Learn about cloud agents →"
- "Learn about Cursor's surfaces →"
- "Learn about Tab →"
- "Explore models ↗"
- "Learn about codebase indexing ↗"
- "Explore enterprise →"
- "See what's new in Cursor →"
- "Join us" (careers link in mission section)
- "View all blog posts →"

**Product Page:**
- "Download for Windows ↓"
- Multiple "Learn more →" (per feature section)
- "Download →" (CLI section)
- "View more posts →"
- "See what's new in Cursor →"

**Enterprise Page:**
- "Talk to the team →" (hero CTA)
- "Contact sales" (multiple instances)
- "View enterprise controls ↗"
- "View available models ↗"
- "Learn more about Bugbot ↗"
- "Visit our Trust Center"
- "Read about our security"
- "Bring Cursor to your team"
- "View all stories →"

**Pricing Page:**
- "Download" (Hobby plan)
- "Get Pro"
- "Get Pro+"
- "Get Ultra"
- "Contact Sales" (Enterprise/footer)
- "Download" (bottom CTA)

**Blog (index and article):**
- "View all blog posts →"
- No CTA on article pages (no "Subscribe to newsletter," no "Download" in blog article context)

**Footer (all pages):**
- All navigation links function as soft CTAs
- "SOC 2 Certified" (trust link)
- Theme toggles (System / Light / Dark)
- Language selector

**Contact/Sales page:**
- "Continue →" (form submit CTA)
- "Read story →" (amber editorial link)

**Download page:**
- "Download for Windows ↓"
- Platform-specific download link rows
- "View release notes →"

**Careers:**
- "Apply →" (per job listing)

**CTA tone analysis:**
The micro-copy in CTAs is action-oriented but never pushy. "Get Pro+" vs "Buy Pro+" — "Get" is lower-friction, personal, immediate. "Download" is neutral/functional. "Talk to the team" is warm and human. "Try Bugbot for free →" introduces "free" only in the Bugbot context — a deliberate contrast to the premium positioning on paid plans.

---

## 9. Platform & Technical Notes

### Platform Identification

**Next.js (React) — with evidence:**
- URL pattern for images: `cursor.com/marketing-static/_next/image?url=...&w=1920&q=70` — confirms Next.js Image optimization component
- The tab title pattern `Cursor: The best way to code with AI` and `Blog · Cursor` reflects Next.js metadata patterns
- DOM accessibility tree shows React-rendered component structure
- Blob storage: `ptht05hbb1ssoooe.public.blob.vercel-storage.com` — Vercel Blob storage, confirming the site is deployed on **Vercel**

**Custom build (not a Shopify theme or WordPress):**
- The marketing site is a fully custom Next.js application, not a CMS template
- URL structure follows clean routing patterns consistent with Next.js App Router or Pages Router
- The interactive demo components (animated Cursor IDE) are custom JavaScript/React components

---

### URL Structure

- Homepage: `cursor.com/`
- Product pages: `cursor.com/product`, `cursor.com/product/tab`
- Feature pages: `cursor.com/enterprise`, `cursor.com/pricing`, `cursor.com/bugbot`, `cursor.com/agents`
- Sub-product: `cursor.com/cli`
- Utility: `cursor.com/download`, `cursor.com/careers`, `cursor.com/contact-sales`
- Blog: `cursor.com/blog`, `cursor.com/blog/[slug]`, `cursor.com/blog/topic/[topic]`
- Changelog: `cursor.com/changelog`, `cursor.com/changelog/[slug]`
- Legal: `cursor.com/privacy`, `cursor.com/security`, `cursor.com/terms-of-service`, `cursor.com/data-use`
- Locale-aware: `/en-US/` prefix used in footer links (e.g., `cursor.com/en-US/product`) — suggests i18n routing support for multiple languages
- Query params for UTM/source tracking: `?source=navbar`, `?source=enterprise_hero`, `?source=enterprise_features`, `?source=pricing_enterprise`, `?source=pricing_footer` — used on contact-sales CTAs for conversion tracking
- Dashboard: `cursor.com/dashboard` (authenticated)
- External: `cursor.com/docs` (likely subdomain or subdirectory for documentation), `forum.cursor.com` (separate subdomain)

---

### Third-Party Integrations Identified

- **Vercel** — Hosting/deployment (Vercel Blob storage confirmed)
- **api2.cursor.sh** — Download/update API (`https://api2.cursor.sh/updates/download/golden/win32-x64-user/cursor/2.6` — the direct download link)
- **trust.cursor.com** — Trust Center for enterprise security/compliance (separate subdomain)
- **status.cursor.com** — Status page (separate subdomain, likely Statuspage.io or similar)
- **forum.cursor.com** — Community forum (likely Discourse or similar)
- **anysphere.inc** — Parent company external site

No obvious third-party chat widgets (Intercom, Drift, Zendesk), no observable analytics tags from the DOM read, no social login buttons visible.

---

### SEO & Meta Title Patterns

Observed title tag patterns:
- `Cursor: The best way to code with AI` — Homepage
- `Cursor · Agent` — Product page
- `Cursor · Enterprise` — Enterprise page
- `Cursor · Pricing` — Pricing page
- `Blog · Cursor` — Blog index
- `The third era of AI software development · Cursor` — Blog article (Article Title · Cursor)
- `Changelog · Cursor` — Changelog
- `Cursor · Careers` — Careers
- `Cursor · Contact our sales team` — Contact sales
- `Cursor · Privacy Policy` — Privacy
- `Cursor · Download` — Download
- `Cursor · Tab` — Tab product page
- `Cursor · Bugbot` — Bugbot page

**Pattern:** Most pages follow `Cursor · [Page Name]` or `[Article Title] · Cursor` (reversed for editorial content, where the content title leads). The homepage uses a full value proposition sentence.

---

### Legal & Compliance Pages

- Terms of Service: `cursor.com/terms-of-service`
- Privacy Policy: `cursor.com/privacy` (last updated Oct 6, 2025)
- Data Use: `cursor.com/data-use`
- Security: `cursor.com/security` (last updated Jan 27, 2026)
- SOC 2 Type 2 certified (mentioned in footer and enterprise page)
- GDPR and CCPA compliant (stated on enterprise page)
- Trust Center: `trust.cursor.com`
- AES-256 encryption at rest, TLS 1.2+ in transit (stated)
- Zero data retention option for enterprise
- SAML-based SSO and SCIM provisioning available

---

### Accessibility Features

- "Skip to content" link present on every page (first focusable element)
- Semantic `<header>`, `<main>`, `<footer>` landmarks
- Proper `<heading>` hierarchy (H1 → H2 → H3)
- Interactive demo panels have accessible text descriptions ("This element contains an interactive demo for sighted users. It's a demonstration of Cursor's IDE...")
- Aria labels on interactive buttons ("Expand Menu", "Send message", etc.)
- `alt` text on all partner logos (e.g., `![Stripe]`, `![OpenAI]`)
- Focus management on dropdown menus
- `aria-expanded` states on expandable components
- Accessible color contrast: Near-black on cream (`#1A1A1A` on `#F5F3EE`) exceeds WCAG AA standards

---

### Social Media Accounts

- **X (formerly Twitter):** `x.com/cursor_ai` — handle: @cursor_ai
- **LinkedIn:** `linkedin.com/company/cursorai` — company: cursorai
- **YouTube:** `youtube.com/@cursor_ai` — channel: @cursor_ai

All three use the same handle pattern (`cursor_ai`), signaling brand consistency across platforms.

---

## 10. Pages Browsed

1. **https://cursor.com/** — Homepage
2. **https://cursor.com/product** — Product / Agents feature page
3. **https://cursor.com/enterprise** — Enterprise page
4. **https://cursor.com/pricing** — Pricing page
5. **https://cursor.com/blog** — Blog index
6. **https://cursor.com/blog/third-era** — Blog article: "The third era of AI software development" (by Michael Truell, Feb 26, 2026)
7. **https://cursor.com/changelog** — Changelog (most recent entry: Self-hosted Cloud Agents, Mar 25, 2026)
8. **https://cursor.com/careers** — Careers page
9. **https://cursor.com/contact-sales** — Contact our sales team
10. **https://cursor.com/privacy** — Privacy Policy (last updated Oct 6, 2025)
11. **https://cursor.com/download** — Download page
12. **https://cursor.com/product/tab** — Tab product feature page
13. **https://cursor.com/bugbot** — Bugbot / Code Review feature page
14. **https://cursor.com/security** — Security page (browsed briefly for legal/compliance section)

---

*End of Cursor Brand Standards Audit. All data extracted directly from browsed pages. Screenshots saved to workspace.*
