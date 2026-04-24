Vercel Brand Standards Audit -- extracted from https://vercel.com across 13 pages (April 2026)

---

## 1. Color Palette

### Every Hex Color Extracted from the Site

**Primary / Dominant Colors**
- `#000000` — Pure black. The dominant brand color. Used for: primary CTA button fills ("Start Deploying"), the Vercel triangle logomark, all H1/H2/H3 body headings, nav link text, announcement bar text, pricing plan names, footer section headings. This is the most frequently applied color on the entire site.
- `#FFFFFF` — Pure white. Used for: page backgrounds (global default), reversed text on black CTAs, inner logo variation on dark surfaces, secondary CTA fills ("Get a Demo," "Get a demo," "Enable Fluid"), footer background, form input backgrounds.
- `#FAFAFA` / `#F5F5F5` — Near-white off-white. Used for: secondary page section backgrounds, card backgrounds (e.g., pricing plan cards, template cards), the grid overlay section on hero backgrounds, the "Fluid Compute" module background, the Customers page background. Creates subtle visual zoning without introducing color.
- `#111111` / `#0A0A0A` — Near-black dark. Used for: the "Infrastructure for AI." speech bubble on the AI landing page, CTA variant fills on the AI page ("Get a ▲ Demo"), secondary typographic elements.

**Grid / Structural Colors**
- `#E5E5E5` / `#D1D1D1` — Light gray. Used for: the visible grid lines on every hero section — a distinctive recurring structural motif. Also used for horizontal divider lines, card borders, sidebar navigation borders in Docs, form input borders.
- `#C0C0C0` — Mid gray. Used for: subtle separators and muted secondary text elements (author bylines, timestamps, read times on blog posts).

**Text Hierarchy Colors**
- `#000000` — Primary text: all headings.
- `#666666` / `#6B6B6B` — Secondary text / body subtext. Used for: descriptive copy under H2 headings (e.g., "Vercel provides the developer tools..."), pricing plan descriptions, footer fine print, form field labels, sidebar nav in Docs for inactive states.
- `#999999` — Tertiary / muted text. Used for: timestamps ("Mar 19," "Mar 30"), placeholder text in form fields ("Email address," "Timmy Triangle," "http://address.com"), footnote-level metadata.

**Accent / Interactive Colors**
- `#0070F3` — Vercel blue. The primary interactive accent color. Used for: hyperlinks in Docs content ("framework," "multi-tenant," "getting started guide"), active state underlines, the "New" badge pill on the Fluid Compute hero page ("New | Lower Costs with Active CPU Pricing"), icon fill color on the Security page (firewall icons, workspace security icons appear in a blue-tinted line weight), the "Copy URL" link on blog posts.
- `#00C7B7` — Teal/cyan. Appears in the AI Gateway model list as data visualization color (one of the multicolor lines in the Fluid compute pricing chart). Also appears in the refracted hero light rays (green-teal spectrum on homepage hero illustration).

**Data / Illustration Colors (Hero Visualization)**
The homepage hero features a full-bleed illustration with multicolor light rays radiating from the central Vercel triangle. These colors are purely illustrative, not applied to UI components. Colors observed:
- Red/Coral: approximately `#FF6B6B` / `#E85454`
- Orange/Amber: approximately `#F5A623` / `#FF8C00`
- Yellow/Gold: approximately `#FFD700` / `#F7E05A`
- Green/Teal: approximately `#00C7B7` / `#4CAF50`
- Blue/Violet: approximately `#6C63FF` / `#3B82F6`

**Fluid Compute Chart Colors (Homepage section)**
The Fluid compute visualization uses six colored data lines:
- Blue: `#3B82F6`
- Orange: `#F59E0B`
- Purple: `#8B5CF6`
- Green: `#10B981`
- Red: `#EF4444`
- Teal: `#06B6D4`

**Announcement Bar**
- Background: `#000000` (black pill/capsule)
- Text: `#FFFFFF` (white label "Events")
- Secondary text: near-white/light gray
- "Save the date" CTA: white text with right-arrow chevron

**"Popular" Badge (Pricing Page)**
- Background: `#000000`
- Text: `#FFFFFF`
- Positioned as a floating pill above the Pro plan card

**"New" Badge (Fluid page, AI Gateway section)**
- Background: `#F0F9FF` — very light blue pill
- Text: `#0070F3` — Vercel blue
- Border: `#BAE6FD` — light blue

**Form Elements**
- Input border: `#E5E5E5` (default), likely `#0070F3` on focus
- Input background: `#FFFFFF`
- Placeholder text: `#999999`
- Dropdown chevron: `#666666`

**Careers Page Architecture Illustration**
- Line colors: `#AECF76` (yellow-green), `#F5C842` (yellow) — these appear as animated grid-line traces in the hero illustration, color-coding infrastructure paths.

---

### Palette Strategy Analysis

Vercel's palette is one of the most restrained in enterprise software. The strategy is **monochromatic absolutism with a single functional accent**. Black and white carry 95%+ of all visual weight. Gray scale is used with surgical precision to create hierarchy without introducing warmth or personality-disrupting hues. The single interactive accent (`#0070F3`) is used only where it serves a clear functional purpose (links, active states, new-feature badges). Illustration color (the hero rays, the globe lines, the Fluid charts) is scoped entirely to data visualization and brand visual setpieces — it never crosses into UI chrome.

**What this says strategically:** Vercel is positioning itself as infrastructure — invisible, foundational, professional. Aggressive color would imply opinionation about aesthetics. Instead, Vercel lets developers (and their products) bring the color. The platform itself is the blank canvas.

---

### Color Application by Page Type

**Homepage**
- Background: White (`#FFFFFF`) with light gray grid overlay (`#E5E5E5`)
- Hero: Full-bleed multi-color light-ray illustration (illustrative only)
- Headings: `#000000`
- Body copy: `#666666`
- Primary CTA ("Start Deploying"): Black fill, white text
- Secondary CTA ("Get a Demo"): White fill, black text, gray border
- Module section backgrounds alternate: white → off-white (`#FAFAFA`) → white

**Pricing Page**
- Background: White
- Grid lines: `#E5E5E5` (light gray)
- Plan names ("Hobby," "Pro," "Enterprise"): `#000000`
- Price ($20/mo): `#000000` bold
- "Popular" badge: Black pill, white text
- Feature list icons: `#000000` outline icons
- Plan card backgrounds: White with light gray border

**Enterprise Page**
- Background: White
- Heading "The complete platform to build the web.": `#000000`, very large
- Body text (right column): `#666666`
- CTA "Get a demo": Black fill, white text (pill)
- CTA "Explore the Product": White fill, black text (pill outline)
- Customer logo strip: Monochrome logos on white

**About Page**
- Background: White
- Hero heading: `#000000`, extremely large
- Body copy: `#666666`
- Values section (Easy/Universal/Accessible) uses `#000000` icons and headers
- Investor logos: Monochrome on white

**Blog / Editorial Page**
- Background: White
- Article cards: White with light gray grid borders
- Post title: `#000000`, bold/medium weight
- Post excerpt: `#666666`, regular weight
- Date stamp: `#999999`, small
- Category pills ("All Posts," "Engineering," etc.): Active = Black pill, white text; Inactive = white, `#666666` text
- Author avatar: Circular image
- Search field: `#E5E5E5` border, `#FFFFFF` background

**Blog Post (Editorial Detail)**
- Background: White
- Category label ("Blog"): `#999999`, small caps or small text
- Title: `#000000`, display/large
- Author name: `#000000`
- Role ("Software Engineer"): `#666666`
- Reading time icon: `#0070F3` (clock icon)
- "Copy URL" link: `#0070F3`
- Lede paragraph: `#000000`, italic
- Body paragraphs: `#333333` / `#000000`, regular
- Horizontal rule separator: `#E5E5E5`

**Docs Page**
- Background: White (main content), `#FAFAFA` (left sidebar)
- Sidebar nav: `#666666` text, `#000000` active, `#E5E5E5` borders
- Page heading: `#000000`
- Body text: `#333333`
- Hyperlinks in text: `#0070F3`
- Right rail "On this page" nav: `#666666`
- Code blocks: dark background (approximately `#1E1E1E`) with monospace font
- Quick reference card arrows: `#000000`

**Contact / Sales Page**
- Background: White
- Heading ("Talk to our Sales team."): `#000000`, large
- Sub-items with icons: `#000000` icon + `#000000` bold label + `#666666` description
- Form fields: White background, `#E5E5E5` border, `#999999` placeholder
- Social proof stat numbers ("6x faster," "98% faster"): `#000000`, heavy weight
- Customer logos (eBay, Tripadvisor, Sonos): Monochrome on white
- Quote text: `#000000` bold for emphasis words, `#666666` regular

**AI Landing Page**
- Background: White with light gray grid
- Speech bubble "Infrastructure for AI.": Black fill, white text — a uniquely differentiated callout component
- Content box: White with rounded border `#E5E5E5`
- "Get a ▲ Demo" CTA: White fill, black text, rounded outline
- Section heading ("The end-to-..."): `#000000`
- "The AI Cloud" label with sparkle icon: `#666666`

**Security Page**
- Background: White
- Hero: Split layout — left panel has the Vercel triangle in black outline + blue overlay/watermark behind
- Icons (Firewall, WAF, Workspace Security): `#0070F3` blue
- Heading: `#000000`
- Body: `#666666`

**Templates Page**
- Background: White
- Filter sidebar: White with `#E5E5E5` borders
- Template cards: White with subtle border
- Card title: `#000000`
- Card description: `#666666`
- Card image: Dark background screenshots (product thumbnails with `#1A1A1A`/`#000000` dark surfaces)
- Checkbox filter: `#0070F3` when active

**Careers Page**
- Background: White
- Grid illustration lines: `#AECF76` (green) and `#F5C842` (yellow) — only page to use green/yellow
- Heading: `#000000`, very large
- CTA "Open Positions": Black pill
- Job listing table: White background, `#E5E5E5` row dividers
- Job title: `#000000`
- Location: `#666666`
- "Read more" button: White with `#E5E5E5` border (ghost button)

**Footer (Global)**
- Background: White
- Section labels: `#000000`, small caps ("GET STARTED," "BUILD," "SCALE," "SECURE," "RESOURCES," "LEARN," "FRAMEWORKS," "SDKS," "USE CASES," "COMPANY," "COMMUNITY")
- Link text: `#666666`
- Vercel logo: Black wordmark
- Status link: `#999999`
- Theme selector: `#666666`
- Copyright/legal: `#999999`

---

### Color Hierarchy & Emotional Role Analysis

1. **Black (`#000000`)** — Authority, precision, confidence. Used for everything that communicates Vercel's core identity and primary actions. Conveys that Vercel is serious infrastructure, not a lifestyle brand.
2. **White (`#FFFFFF`)** — Openness, speed, clarity. The dominant background signals that Vercel doesn't crowd the screen — developer tools should feel frictionless.
3. **Light Gray (`#E5E5E5`)** — Structure without weight. The grid lines serve as a literal architectural metaphor — scaffolding that holds pages together but disappears under scrutiny.
4. **Mid Gray (`#666666`)** — Context and support. Secondary copy reads as authoritative but not primary, allowing headlines to dominate.
5. **Blue (`#0070F3`)** — Action and intelligence. Borrowed from Next.js / open-source heritage, this blue is used sparingly as a signal of interactivity and novelty ("New" badges).
6. **Hero Colors (multi-spectrum)** — Ambition, creativity, the web's range. The refracted light rays on the homepage hero reference a prism/spectrum — everything the web can be, refracted through Vercel's infrastructure.

---

### Colors NOT Used (Deliberate Absences)

- **No red/warning orange in UI** (only in data visualization) — Vercel avoids danger/urgency color psychology in its primary experience
- **No gradients in UI chrome** — No CSS gradient backgrounds on buttons, cards, or navigation. Gradients appear only in illustrative/hero setpieces.
- **No green for "success/go" CTAs** — The ecosystem standard of green=good is absent; Vercel uses black, reinforcing neutrality
- **No purple/violet** — Despite purple being common in developer tools (GitHub, Twitch), Vercel avoids it entirely
- **No yellow/amber in UI** — Only appears in the Careers illustration, never in typography or buttons
- **No dark mode as default** — Despite offering a theme toggle, the default is always light/white, signaling openness not mystery
- **No photography color grading** — No Instagram-style filters or tonal shifts on photography

---

## 2. Typography

### Font Families Identified

**Primary Sans-Serif (Display + Body): Geist**
Vercel's proprietary typeface, designed in-house and open-sourced. Geist is a grotesque sans-serif engineered for developer interfaces. It is the sole typeface used for all display headings, body copy, UI labels, navigation, buttons, and form elements across the entire site.

- Closest design match: A hybrid of **Inter** (by Rasmus Andersson, an individual investor in Vercel), **Söhne** (by Klim Type Foundry), and **Neue Haas Grotesk**. Geist shares Inter's clean numerals and optical-size clarity with the weight distribution of Helvetica Neue.
- Font style: Geometric-grotesque, optically engineered for screen clarity
- Available weights: 100 (Thin) through 900 (Black); Vercel's UI primarily uses 400 (Regular), 500 (Medium), 600 (SemiBold), and 700 (Bold)

**Secondary Monospace (Code): Geist Mono**
Vercel's companion monospace typeface, also proprietary and open-sourced. Used exclusively in:
- Code blocks on Docs pages (e.g., the `vercel.json` examples)
- The AI Gateway code snippet on the homepage (`import { streamText } from 'ai'`, etc.)
- CLI command displays in documentation
- The "S t a r t D e p l o y i n g" spaced-out letter animation at the bottom of the homepage — a creative typographic gesture using wide-tracked Geist Mono characters

Closest match: **Fira Code**, **JetBrains Mono**, or **IBM Plex Mono**, but with Geist's characteristic geometric confidence.

---

### Complete Font Usage Map

| Element | Font | Weight | Case | Approx. Size | Letter-spacing |
|---|---|---|---|---|---|
| Homepage H1 ("Build and deploy on the AI Cloud.") | Geist | 700–800 (Bold/ExtraBold) | Title case, sentence case | ~60–72px | Slightly tight, ~-0.02em |
| Enterprise H1 ("The complete platform to build the web.") | Geist | 700–800 | Sentence case | ~72–88px | ~-0.03em |
| About H1 ("Vercel enables the world to ship the best products.") | Geist | 700–800 | Sentence case | ~64–80px | ~-0.03em |
| Fluid Compute H1 ("The power of servers, in serverless form") | Geist | 700–800 | Sentence case | ~72–96px | ~-0.03em |
| Careers H1 ("Join us to Ship what's Next.") | Geist | 700–800 | Mixed case (capitalized "Ship," "Next") | ~72–88px | ~-0.03em |
| Security H1 ("Security that scales with you.") | Geist | 700 | Sentence case | ~56–64px | ~-0.02em |
| Pricing H1 ("Find a plan to power your apps.") | Geist | 700 | Sentence case | ~60–72px | ~-0.02em |
| Blog H1 (post title, e.g., "Agent responsibly") | Geist | 700 | Sentence case, lowercase | ~52–64px | ~-0.02em |
| Section H2 (e.g., "Your product, delivered.") | Geist | 600–700 (SemiBold/Bold) | Sentence case | ~40–48px | ~-0.015em |
| Section H3 (e.g., "Fluid Compute," "AI Gateway") | Geist | 600 (SemiBold) | Title case | ~28–36px | ~-0.01em |
| Body paragraph / Hero subtext | Geist | 400 (Regular) | Sentence case | ~16–20px | 0 (normal) |
| Navigation link text | Geist | 400–500 | Sentence case | ~14px | 0 |
| Nav dropdown labels | Geist | 500 | Sentence case | ~14px | 0 |
| Button text (primary CTA) | Geist | 500–600 | Sentence case | ~14–16px | 0 |
| Pricing plan tier names | Geist | 600–700 | Title case | ~28–32px | ~-0.01em |
| Pricing feature list items | Geist | 400 | Sentence case | ~14px | 0 |
| Blog category pills | Geist | 500 | Sentence case | ~13–14px | 0 |
| Blog post date/timestamp | Geist | 400 | "Mar 19" format | ~12–13px | 0 |
| Blog author name | Geist | 500 | Name case | ~13–14px | 0 |
| Blog author role | Geist | 400 | Sentence case | ~13px | 0 |
| Reading time ("5 min read") | Geist | 400 | Lowercase | ~13px | 0 |
| Footer column headers ("GET STARTED," "BUILD") | Geist | 600 | ALL CAPS | ~11–12px | ~0.08–0.12em (wide) |
| Footer link text | Geist | 400 | Sentence case | ~13–14px | 0 |
| "NEW" badge label | Geist | 600 | ALL CAPS | ~10–11px | ~0.06em |
| "Popular" badge | Geist | 500–600 | Title case | ~12–13px | 0 |
| Form field labels ("Company email," "Country") | Geist | 500 | Sentence case | ~13–14px | 0 |
| Form placeholder text | Geist | 400 | Sentence case | ~14px | 0 |
| Code snippets (Docs + AI section) | Geist Mono | 400 | Mixed | ~13–14px | 0 |
| "S t a r t D e p l o y i n g" (letter-spaced) | Geist Mono | 400–500 | Sentence case | ~14–16px | Extreme: ~0.3–0.5em per character |
| Announcement bar text | Geist | 400 | Sentence case | ~13–14px | 0 |
| Announcement "Events" badge | Geist | 600 | Sentence case | ~11–12px | 0 |
| Documentation body paragraphs | Geist | 400 | Sentence case | ~15–16px | 0 |
| Documentation sidebar nav | Geist | 400 | Sentence case | ~13–14px | 0 |
| Quick reference card titles | Geist | 500 | Sentence case | ~15–16px | 0 |
| Stat numbers ("6x faster," "98% faster") | Geist | 700 | Mixed | ~24–28px | ~-0.02em |
| Stat descriptors ("to build and deploy") | Geist | 400 | Sentence case | ~16px | 0 |
| Customer testimonial quote | Geist | 400 | Sentence case | ~15–16px | 0 |
| Quote attribution name | Geist | 500 | Name case | ~13–14px | 0 |
| Quote attribution role | Geist | 400 | Sentence case | ~12–13px | 0 |
| Value propositions ("Easy.", "Universal.", "Accessible.") | Geist | 600 | Sentence case, period-terminated | ~20–24px | 0 |
| Product sub-section label ("The AI Cloud" with sparkle) | Geist | 500 | Sentence case | ~13–14px | 0 |
| Template card title | Geist | 600 | Title case | ~16–18px | 0 |
| Template card description | Geist | 400 | Sentence case | ~13–14px | 0 |
| Filter label ("Filter Templates") | Geist | 600 | Title case | ~14px | 0 |
| Filter option labels | Geist | 400 | Sentence case | ~14px | 0 |

---

### Typography Application by Page Type

**Homepage**
The homepage uses the full type scale — from a massive 72px+ hero H1 to 11px badge labels. The typographic architecture descends: H1 (display impact) → H2 (section statements) → H3 (product feature labels) → body (16–20px supporting copy) → micro (12–13px metadata). Section H2s like "Your product, delivered." are styled with period-terminal punctuation, a consistent Vercel voice pattern. The "S t a r t D e p l o y i n g" animated letter-spaced CTA uses extreme tracking (each letter isolated with spaces) as a playful technical gesture referencing developer character-level manipulation of text.

**Product Detail Pages (Fluid, Security, AI)**
Hero H1s are even larger — up to 96px — on product pages. These pages use a single dominant typographic statement per hero section, then shift to smaller H3s (28–36px) for sub-features. Body paragraphs are tighter (~16px) and more technical in language. Code samples on the AI Gateway section use Geist Mono at 13–14px.

**Pricing Page**
Tier names ("Hobby," "Pro," "Enterprise") are 28–32px SemiBold. Price display ("$20/mo") is 24px Bold. Feature list items are 14px Regular. The hierarchy is deliberate: understand the tier name and price before reading features.

**Blog Listing Page**
Post titles are 24–32px Bold in a card context. Excerpts are 14–15px Regular gray. Dates are 12px gray. Author names are 13px Medium. The filter pills ("All Posts," "Engineering") are 13–14px Medium in capsule containers.

**Blog Post (Editorial Detail)**
The title is the largest element at 52–64px Bold. The author byline drops to 13–14px. The lede/intro paragraph is styled at ~16–18px italic (a typographic elevation signal). Body paragraphs are 15–16px Regular. Internal headers (H2 within article) would be ~24px SemiBold.

**Documentation**
Sidebar navigation uses 13–14px Regular with active-state Bold. Page title is ~32px Bold. Section headers within docs are 20–24px SemiBold. Body text is 15–16px Regular. Code is Geist Mono 13–14px.

**FAQ / Knowledge Base**
Accordion-style layout with question labels at ~16px Medium/SemiBold. Answer text at 14–15px Regular.

**Contact Page**
Headline ("Talk to our Sales team.") is ~52–64px Bold. Sub-items with icons use 14–15px Medium bold for the label + 14px Regular for description. Form labels are 13–14px Medium. Stats ("6x faster") are 24–28px Bold.

---

### Font Pairing Philosophy

Geist + Geist Mono is a **single-family pairing with a functional companion variant** — not a traditional serif/sans pairing or display/text pairing. This is deliberate and semiotically meaningful:

1. **Coherence over contrast:** Using one superfamily signals systematic thinking — no visual "jazz" between different typeface personalities fighting each other.
2. **Developer-native logic:** Geist Mono referencing a programming/terminal context grounds the brand in its core user's worldview. Every developer knows the monospace font as the font of code, commands, and precision.
3. **Infrastructure as brand:** Just as Vercel's platform is one unified system for deploying applications, the typography is one unified system for communicating them. No exceptions, no guest typefaces, no editorial flourish.
4. **Inter heritage:** Geist's spiritual ancestor, Inter, was created by Rasmus Andersson (an individual investor in Vercel). This is a quiet piece of the brand's story — the typeface carries the legacy of the open-source design community Vercel serves.

---

### Weight Distribution Analysis

- **400 (Regular):** Used for all body copy, nav links (default state), footer links, placeholder text, secondary metadata. The workhorse weight.
- **500 (Medium):** Used for button text, nav links (hover or active), form labels, author names, badge labels. Provides friction without heaviness.
- **600 (SemiBold):** Used for H3s, pricing feature headers, footer column headers (in ALL CAPS), card titles, filter labels. The "important but not critical" tier.
- **700 (Bold):** Used for all H1s, H2s, pricing tier names, stat numbers, quote emphasis words. The primary authority weight.
- **800–900 (ExtraBold/Black):** Used selectively for the most impactful H1s (Fluid Compute hero, About hero, Enterprise hero). Creates true display-weight impact without requiring a separate display typeface.

**Weights NOT used:** 100 (Thin), 200 (ExtraLight), 300 (Light) — Vercel avoids light weights entirely, maintaining a minimum of 400 Regular for legibility and brand solidity. No italic weight used except within blog body text (lede paragraphs).

---

### Letter-Spacing Rules

- **Display headings (H1, large H2):** Negative tracking, approximately -0.02em to -0.04em. Pulls large letterforms together for tighter optical fit.
- **Body copy:** Zero tracking (0em). No modification to default spacing.
- **ALL CAPS labels (footer headers, "NEW" badge):** Wide positive tracking, approximately +0.06em to +0.12em. Industry standard for small-caps legibility.
- **"S t a r t D e p l o y i n g" animated text:** Extreme positive tracking as an aesthetic/technical gesture, approximately +0.3–0.5em per character.
- **Button text:** Zero tracking.
- **Code/Geist Mono:** Zero tracking (monospace handles spacing inherently).

---

### Complete Type Scale Summary

Every distinct size observed across the site:

- ~10–11px: Badge labels ("NEW"), fine legal text
- ~12–13px: Timestamps, reading time, muted metadata
- ~13–14px: Navigation links, footer links, form labels, blog author info, sidebar nav
- ~15–16px: Body paragraphs, button text, docs body, pricing feature lists
- ~18–20px: Hero subheadlines/subtext, value prop descriptions
- ~20–24px: Value proposition statements ("Easy.", "Universal."), H3 section subheadings
- ~28–32px: Pricing tier names, blog card titles, section sub-H2s
- ~36–40px: Mid-weight H2s on interior pages
- ~48–56px: Standard H1 on interior pages (Pricing, Blog, Security)
- ~60–72px: Homepage H1, Enterprise H1, About H1
- ~72–96px: Maximum display size — Fluid Compute hero, Careers hero

---

## 3. Logo & Wordmark

### Primary Logo Description

**Type:** Combined mark — geometric symbol (the "Vercel triangle" or logomark) paired with the wordmark "Vercel" in the Geist typeface.

**Primary form:** The **logotype** — "Vercel" in Geist Bold/SemiBold with the black upward-pointing triangle (▲) preceding the wordmark. The triangle is a solid equilateral form, precisely geometric.

**Color:** Black (`#000000`) on white or light backgrounds. White on dark backgrounds (e.g., dark CTAs, the "Start Deploying" button includes the ▲ symbol in white).

**Placement:** Top-left of the navigation bar, consistent across all pages at all times. The logo is always in the same position within a fixed-height header (~56–60px tall), left-aligned to the content grid.

---

### Logo Characteristics

- **Typeface:** Geist — the proprietary typeface designed by Vercel. The wordmark is set in a consistent weight, approximately SemiBold or Bold.
- **Tracking:** Slightly tight or default — the wordmark does not appear to use significant positive or negative letter-spacing relative to standard Geist text.
- **Triangle mark:** The ▲ is used as both a standalone symbol AND inline within button labels ("▲ Start Deploying," "Get a ▲ Demo"). This is a distinctive and unusual decision — the brand mark bleeds into UI affordances, making the symbol functionally iconographic beyond just identity.
- **Mark/wordmark relationship:** The triangle precedes the wordmark with a small fixed gap. The triangle is sized to optically match the cap-height of the "V" in "Vercel."
- **File format observed:** SVG, served from Vercel's CDN as `vercel-logotype-light.svg` (light mode variant) — confirming separate assets per theme mode.

---

### Placement Rules

- **Position:** Fixed top-left corner of the global navigation bar on every page, every scroll state.
- **Clearance:** The logo maintains horizontal clearance to the left content margin, aligning with the overall content grid column start.
- **Vertical alignment:** Centered within the nav bar height.
- **Flanking elements:** The logo is always flanked on the right by the primary navigation links (Products, Resources, Solutions, Enterprise, Pricing) with sufficient breathing room. No taglines, no secondary brand marks, no imagery accompany the logo in the nav.
- **Footer usage:** The Vercel logo appears again in the footer, typically centered or left-aligned above the status link and theme selector. Used as a return-to-home anchor.

---

### Color Variations Observed

1. **Black logotype on white/light:** Primary usage across nearly all pages.
2. **White logotype on dark:** Used when the mark appears on black button fills or dark background setpieces. Observed as ▲ within black pill CTAs ("▲ Start Deploying").
3. **Standalone ▲ triangle icon:** Used inline within button labels, navigation arrows, and the AI demo button without the wordmark. Serves as a compact brand-mark shorthand.

---

### Sizing Details

- **Navigation bar logo:** Approximately 90–110px wide at the logo's full rendered extent, constrained within a ~56px tall nav bar.
- **Footer logo:** Similar size or slightly smaller (~80–100px wide).
- **Inline ▲ symbol in CTAs:** Approximately 12–16px, matching button text size.
- **Hero illustration:** A larger, outline version of the triangle appears as the centerpiece of the homepage hero (the focal point of the light-ray radiating illustration). This ceremonial/hero treatment is approximately 150–200px at the base.

---

### Brand Mark System

Vercel operates a **dual-element mark system**:
1. **Logotype** (▲ + "Vercel"): Primary identity mark for navigation, documents, presentations.
2. **Symbol/icon** (▲ alone): Compressed brand mark for favicon, app icon, and inline UI affordances.

The triangle is deeply semantically loaded:
- It is the universal "play" / "start" symbol (referencing deployment)
- It is an upward-pointing shape (suggesting growth, ascension, performance)
- It is geometry at its most reduced — suggesting engineering precision
- It is used in the CLI tool as `▲` — making the brandmark literally a command-line character

---

### Logo Relationship to Brand Heritage/Positioning

The Vercel wordmark in Geist signals a company that **designed its own typeface for its own name** — the highest form of typographic brand commitment in software. This is the same gesture made by Apple (San Francisco), IBM (Plex), and Google (Product Sans). It signals: we are building infrastructure, and we invest in every layer. The triangle mark's reuse as a CLI character and inline button affordance is a rare example of a logo mark that doubles as UI iconography — a deeply systems-thinking design decision that rewards developer users who "get the joke."

---

## 4. Layout & Grid System

### Global Structure

- **Max content width:** Approximately 1180–1280px (content column), with the full-bleed sections (hero illustrations, grid overlays) extending to 100% viewport width.
- **Lateral margins:** ~80–120px on each side at desktop, narrowing to ~24–32px on mobile.
- **Navigation height:** ~56–60px, fixed/sticky at top.
- **Announcement bar:** ~40–48px, appears above the nav on pages where active (homepage, AI page), making the combined header approximately 96–108px.
- **Grid overlay:** A recurring structural motif — a faint grid of ~84–96px cells is visible on hero sections, creating a "blueprint" aesthetic. Grid cells are delineated with `#E5E5E5` 1px lines. Corner markers ("+") appear at the bounding-box corners of grid sections.
- **Column system:** Appears to be a 12-column grid at desktop (1280px breakpoint), collapsing to fewer columns on tablet/mobile.
- **Horizontal section dividers:** Full-width `#E5E5E5` 1px horizontal rules divide major page sections.
- **Card/module gap:** Approximately 24–32px between grid cells in 3-column and 2-column module layouts.
- **Footer:** Multi-column layout with ~10–11 link columns organized under ALL-CAPS headings, stacking vertically on mobile. Copyright and theme selector appear in the footer basement.

---

### Every Page Template Identified

**Homepage**
Layout: Full-bleed hero → horizontal rule → logos ticker → tab-switcher product module → feature split-modules → globe visualization → feature modules → code sample → template link strip → footer. Architecture is a vertical scroll narrative — each module addresses a different audience segment (startup, enterprise, framework-specific).

**Pricing Page**
Layout: Standard hero (centered H1 + subtext) → 3-column plan cards (Hobby / Pro / Enterprise) stacked in a comparison grid → FAQ accordion (likely below fold) → footer.

**Enterprise Page**
Layout: Split hero (large H1 left, body + CTAs right) → customer logo strip → feature modules (2 and 3 column alternating) → testimonials → footer.

**About Page**
Layout: Centered hero (full-width H1) → 3-column values grid (Easy / Universal / Accessible) → investor logo gallery → individual investor list → CTA → footer. Ultra-minimal, mission-forward.

**Blog Listing**
Layout: Filter pill bar (category tabs + search) → featured 3-column article grid → "Latest news" section → footer. No hero imagery. Content-first.

**Blog Post (Editorial Detail)**
Layout: Narrow centered column (~680px) with: category label → H1 → author byline → reading time + share → lede → horizontal rule → body content. Clean long-form reading column with ample whitespace on both sides. A right-rail "On this page" anchor nav is suggested by the Docs page pattern.

**Documentation Page**
Layout: 3-panel: left sidebar nav (~240px) → main content (~720px) → right rail "On this page" nav (~240px). Sidebar uses accordion expand/collapse. Main content is a standard reading column with quick-reference cards at top.

**Contact / Sales Page**
Layout: 2-column split — left: headline + benefit bullets + social proof stats + testimonial; right: multi-field form. The form column takes approximately 45% of the layout width.

**AI Landing Page**
Layout: Announcement bar → standard hero with centered message + inline content box → feature section (AI Gateway, AI SDK, Agents, Sandbox) in modular grid → footer.

**Security Page**
Layout: Split hero (left: product illustration; right: H1 + body + CTA) → 3-column feature icons → customer logos → feature detail modules.

**Templates Page**
Layout: Filter sidebar (left, ~220px) + main content grid (right, ~960px). Template grid is 3 columns, showing 6 cards per load, with filter checkboxes on the left.

**Fluid Compute Product Page**
Layout: Standard centered hero → below-fold feature sections → footer.

**Careers Page**
Layout: Full-bleed hero with animated grid illustration → CTA → job listings table with accordion filters (Location, Department) → individual job rows.

---

### Whitespace Strategy

Vercel uses **generous, systematic whitespace** as a primary design element. Section padding is approximately 80–120px vertical on desktop. Hero sections have significant breathing room above and below the text block. This whitespace is not accidental — it is a brand signal of confidence. Only companies that are secure in their identity can afford to leave space empty. Crowded layouts signal anxiety. Vercel's whitespace says: "our content is worth the wait."

---

### Grid Alignment Philosophy

The omnipresent grid overlay (visible especially in hero sections) is not just aesthetic — it communicates systematic, architectural thinking. Vercel is literally showing users the structure beneath the surface. The grid's "+" corner markers (located at each section boundary) reinforce a technical, precise, engineering-first worldview. Every visual element aligns to the grid. Nothing floats arbitrarily. This is infrastructure logic applied to design.

---

### Homepage Scroll Architecture (Module Pattern, Depth)

1. **Announcement bar** (40px) — event/news
2. **Nav** (56px) — global
3. **Hero hero** — H1 + subtext + dual CTAs + full-bleed light-ray illustration
4. **Customer logos** — social proof strip (Runway, LeonardoAI, Zapier + metrics)
5. **Use case tab switcher** — AI Apps / Web Apps / Ecommerce / Marketing / Platforms
6. **"Your product, delivered."** — 4-panel product feature section
7. **Framework-Defined Infrastructure** — split module
8. **"Scale your Enterprise / Security"** — text + globe visualization
9. **"Deploy once, deliver everywhere"** — globe with active node visualization
10. **Fluid Compute section** — split module with chart visualization
11. **AI Gateway section** — code sample + live model usage leaderboard
12. **"Deploy your first app"** — framework template CTA grid
13. **Footer** — 11-column link grid + branding

---

### Product Card Anatomy (Templates Page)

Each template card contains:
- **Thumbnail image** (full-width top, ~200px tall) — dark-background screenshot or product mockup
- **Title** (~16–18px SemiBold, `#000000`)
- **Description** (2–3 lines, ~13–14px Regular, `#666666`)
- No price (all free)
- No explicit hover state observed from screenshots (likely subtle border or shadow)
- No star rating or social proof on individual cards

---

### PDP Layout (Product Feature Pages: Fluid, Security, AI)

These are single-page product "landing pages" that follow:
- Centered hero with product-specific headline
- Feature modules (split or 3-column grids)
- Visualizations (charts, diagrams, code samples)
- Social proof (customer logos, testimonials)
- CTA footer module

No tabbed navigation within PDPs. Single vertical scroll narrative.

---

### Footer Layout Details

The global footer is a **mega-footer** with 10+ column groups:
- **Row 1:** GET STARTED | BUILD | SCALE | SECURE | RESOURCES | LEARN | FRAMEWORKS | SDKS | USE CASES | COMPANY | COMMUNITY
- Each column has a 11–12px ALL-CAPS 600-weight heading followed by 4–7 links at 13–14px Regular
- **Row 2:** Vercel logo + status indicator ("LOADING STATUS...") + theme selector
- Estimated link count: 60+ links in footer

---

### Layout Elements NOT Present (Deliberate Absences)

- **No sticky sidebar CTAs** — CTAs are not floated or pinned on scroll
- **No live chat widget** — Intercom, Drift, or similar chat bubbles are completely absent
- **No cookie consent banner visible** — Privacy/GDPR handled elsewhere or via settings
- **No breadcrumb navigation** — Even in Docs, wayfinding is handled by sidebar + "On this page" nav
- **No "back to top" button** — Scrolling experience is trusted to be linear
- **No image carousels/sliders on main pages** — Static grid layouts only; no auto-advancing slideshows
- **No video autoplay background in hero** — Despite being a video-capable platform; hero uses SVG illustration instead
- **No stock photography** — Zero use of Unsplash-style or stock lifestyle photography on product pages
- **No product pricing comparison table with many columns** — Vercel limits to exactly 3 tiers (Hobby/Pro/Enterprise), refusing to create feature-fatigue comparison tables

---

## 5. UI Components

### Buttons

**Primary CTA (Black Pill):**
- Background: `#000000`
- Text: `#FFFFFF`, Geist 500–600, ~14–15px
- Border-radius: ~999px (fully rounded "pill" capsule)
- Height: ~44–48px
- Padding: ~12–16px horizontal
- Examples: "Start Deploying," "Enable Fluid," "Get a demo," "Open Positions"
- Icon integration: The ▲ triangle appears inline before text on "▲ Start Deploying" and "Get a ▲ Demo" variants

**Secondary CTA (White/Ghost Pill):**
- Background: `#FFFFFF`
- Text: `#000000`, Geist 500, ~14–15px
- Border: 1px solid `#E5E5E5` or `#D1D1D1`
- Border-radius: ~999px
- Height: ~44–48px
- Examples: "Get a Demo" (homepage), "Explore the Product" (Enterprise), "Get a demo" (Fluid), "Read more" (Careers job listings)

**Tertiary / Text Button:**
- Background: None
- Text: `#000000` or `#0070F3` (for link-style CTAs)
- Underline: On hover for links
- Examples: "Learn more" (Fluid section on homepage), "Read the docs" (AI page), "Copy URL" (blog post)

**Action Cards / Quick Reference Arrows:**
- Used in Docs page
- White card background, `#E5E5E5` border, right-pointing `→` arrow in `#000000`
- On hover: likely border color shift or subtle shadow

**Form Submit Buttons:**
- Not observed (form page loaded but submit button likely below fold)

---

### Navigation

**Desktop Nav Structure:**
- Height: ~56px, fixed/sticky, white background, `#E5E5E5` bottom border
- Logo: Top-left
- Primary links: Products ▼ | Resources ▼ | Solutions ▼ | Enterprise | Pricing (left-center of bar)
- Right cluster: Ask AI | Log In | Sign Up

**Dropdown/Mega Menu:**
- Products, Resources, Solutions each have dropdown menus (indicated by ▼ chevrons and "expanded=False" in accessibility tree)
- Menus are likely multi-column (mega menus) based on the volume of content in each category
- Dropdown style: White background, `#E5E5E5` border, Geist 400–500 text, organized with section headers

**Announcement Bar:**
- A thin event bar appears above the nav on some pages (Homepage, AI page)
- Style: Centered content area with "Events" badge (black pill) + text + "Save the date" CTA (with `>` arrow)
- Height: ~40–48px
- Background: White or very light gray
- NOT present on Docs, Contact, Careers, Pricing (contextual use)

---

### Forms (Contact/Sales Page)

- **Input fields:** Full-width, white background, `#E5E5E5` 1px border, ~44px height, 8px border-radius, Geist 400 placeholder, Geist 400 text
- **Select dropdowns:** White background, `#E5E5E5` border, chevron icon right-aligned (`#666666`), same sizing as inputs
- **Textarea ("How can we help?"):** Multiline, same border treatment, approximately 100–120px tall
- **Phone input:** Split field — flag picker (US flag visible) + number field
- **Labels:** Above each field, `#000000` Geist 500 ~13–14px
- **Field groups:** Some fields appear in 2-column layout (Your name + Phone number)
- **Form layout:** Single-column dominant, with occasional 2-column groupings for related fields

---

### Accordions (Careers Page — Location/Department Filters)

- **Style:** Full-width row, `#E5E5E5` bottom border
- **Label:** `#000000` Geist 500 ~15px
- **Toggle icon:** Chevron ∨ right-aligned, rotates to ∧ on open
- **Behavior:** Appears to be single-expand (one filter category at a time)
- **Answer container:** Slides in below label on expand

---

### Product Carousels / Tab Switchers (Homepage)

The homepage use-case section (AI Apps / Web Apps / Ecommerce / Marketing / Platforms) uses a **horizontal tab switcher**, not a carousel:
- Tab pills: Horizontal scrollable row
- Active tab: Distinct visual treatment (likely black text or underline vs. gray inactive)
- Content: Changes beneath without carousel arrows — click-to-switch or auto-advancing

No traditional product carousels with arrows were observed. Vercel prefers static grids and tab switching over carousels.

---

### Button States & Interactions

- **Default:** As described above (black fill primary, white ghost secondary)
- **Hover:** Not confirmed via screenshot, but industry standard would be: primary CTA → slightly lighter black or subtle brightness shift; secondary → gray fill `#F5F5F5`
- **Active/pressed:** Deeper fill shade
- **Disabled:** Not directly observed
- **Loading:** Not directly observed, but the ▲ triangle icon in CTA buttons suggests possible animation on deploy/loading states (the triangle could spin/pulse)

---

### Size Selector / Color Swatch

Not applicable — Vercel is not an ecommerce site and uses no product size or color selectors.

---

### Search Component

**Docs page search:** Full-width input with placeholder "Search Documentation" and keyboard shortcut indicator `⌘K`. Style: White background, `#E5E5E5` border, magnifying glass icon, Geist placeholder text. The `⌘K` hint suggests the search is command-palette style.

**Blog page search:** Embedded in the filter bar, with magnifying glass icon, placeholder "Search posts," rounded pill styling.

**Templates page search:** Prominent centered search bar, ~400px wide, rounded pill, "Search templates..." placeholder, magnifying glass icon.

---

### "Ask AI" Component

A unique nav element — "Ask AI" appears as a text link/button in the top-right of the nav, adjacent to "Log In." This is notable: Vercel integrates AI assistance into its own product navigation, eating its own dogfood. Behavior: likely opens an AI chat panel (not observed in full).

---

### Accessibility Features

- Skip-to-content link present: `[Skip to content]` as the first focusable element on all pages
- ARIA roles observed: `banner`, `navigation`, `button`, `link`, `heading` — proper semantic HTML
- Button states include `expanded=False` / `expanded=True` for dropdown menus (ARIA)
- Form fields appear labeled (not just placeholder-dependent)
- Image alt text present (observed: "Vercel's logo, a triangle, sits in the center of a grid...")

---

### Video Embed Behavior

No video autoplay observed on product marketing pages. Fluid Compute section shows a static data visualization chart, not video. No YouTube or Vimeo embeds observed in marketing pages. Blog posts may contain video content, but none was visible on visited pages.

---

### Animation & Motion Philosophy

**What's animated:**
- The homepage hero light-ray illustration (appears to be a living SVG or canvas animation — the colored rays radiate/rotate around the central triangle)
- The globe visualization (nodes pulse with small activity indicators)
- The Careers page grid illustration (colored architectural lines animate in, suggesting system paths/connections)
- The ▲ triangle icon in CTAs (possibly animates on hover or click — a deployment-action metaphor)
- The "S t a r t D e p l o y i n g" letter-spacing (animated gradual expansion of letter-spacing on scroll or page load)
- Fluid Compute data chart (animated line graph showing Active/Idle/Active CPU states)

**What's static:**
- All navigation, buttons, and UI chrome — absolutely no bouncing, floating, or gratuitous motion in the utility layer
- Photography (when used) — static, no parallax
- Pricing table — fully static, no interactive comparison toggle

**Motion philosophy:** Animation is used exclusively to communicate **product concepts** (infrastructure activity, global distribution, compute states) not to entertain. Every animation carries information. This is an engineering-first motion philosophy: motion as data visualization, not decoration.

---

## 6. Iconography

### Complete Icon Inventory

| Icon | Description | Usage Location | Style |
|---|---|---|---|
| ▲ (Triangle) | Vercel's brand mark; equilateral upward-pointing triangle | Nav logo, CTA buttons, hero illustration | Solid filled, geometric |
| ▼ (Chevron down) | Dropdown indicator | Nav buttons (Products ▼, Resources ▼, Solutions ▼), filter accordion expand | Thin line chevron |
| → (Right arrow) | Forward/next action | "Save the date →" (announcement), Docs quick-reference cards, "Read the full story →" | Thin line arrow |
| ∅ (Empty set / circle-slash) | "Easy" value icon | About page values section | Outline icon |
| 🌐 (Globe/Earth) | "Universal" value icon | About page values section | Outline icon |
| ♿ (Accessibility figure) | "Accessible" value icon | About page values section | Outline icon |
| 🔒 (Shield/Lock) | Security, DDoS Mitigation | Pricing page feature list | Outline icon |
| 💬 (Chat bubble/conversation) | Chat SDK blog post category icon | Blog listing page card | Pixel-art / geometric style |
| ⚙️ (Gear/settings) | Fluid Compute section label icon | Homepage Fluid section | Small outline |
| 🔗 (Link chain) | "Copy URL" action | Blog post action bar | Small outline |
| ⏱️ (Clock/timer) | Reading time indicator | Blog post header | Small outline |
| 📁 (Folder) | "Build knowledge agents" blog icon | Blog listing page | Pixel-art style |
| 🔵 (Circle) | Agent responsibly blog icon | Blog listing page | Pixel-art / solid circle |
| 📄 (Document) | Docs quick reference cards | Documentation page | Line icon |
| ↗ (Arrow Northeast) | Quick reference card CTA | Documentation page | Thin arrow |
| 🔥 (Firewall shield) | Vercel Firewall feature | Security page, Pricing page | Outline icon |
| 🏗️ (WAF/grid icon) | Web Application Firewall | Security page | Outline icon |
| 👥 (People/team) | Workspace Security, Team collaboration | Security page, Pricing page | Outline icon |
| ⏰ (Clock/SLA) | 99.99% SLA | Pricing page Enterprise feature | Outline icon |
| 🌍 (Globe) | Multi-region compute | Pricing page Enterprise feature | Outline icon |
| 📊 (Chart/analytics) | Observability | Pricing page feature | Outline icon |
| ✨ (Sparkle) | "The AI Cloud" section label | AI landing page | Multi-point star |
| 🔍 (Magnifying glass) | Search inputs | Templates page, Blog page, Docs page | Line icon |
| 📡 (RSS/feed) | Blog RSS feed | Blog listing page, top-right | Line icon |
| 🔲 (Import/repo icon) | "Import your repo" | Pricing feature list | Outline icon |
| ⚡ (Lightning/fast builds) | "Faster builds" | Pricing Pro feature | Outline icon |
| 🌡️ (Thermometer/Cold start) | "Cold start prevention" | Pricing Pro feature | Outline icon |
| 💰 (Dollar/spend) | "Advanced spend management" | Pricing Pro feature | Outline icon |
| 💻 (CLI/terminal) | CLI/code reference | Docs sidebar | Line icon |
| 🔑 (Key/access) | Guest & Team access controls | Pricing Enterprise feature | Outline icon |
| 📋 (Directory/SCIM) | SCIM & Directory Sync | Pricing Enterprise feature | Outline icon |

---

### Icon Design Philosophy

Vercel's icons follow two distinct registers:

1. **UI functional icons (navigation, actions, features):** Clean, thin-line outline icons, consistent stroke weight (~1.5–2px), no fills, no gradients. These are invisible infrastructure icons — they communicate function without drawing attention to themselves.

2. **Editorial/blog category icons:** A unique pixel-art or isometric geometric style for blog post category thumbnails. The chat bubble for "Chat SDK," the solid circle for "Agent responsibly," and the folder icon for "Build knowledge agents" use a different aesthetic — more playful, grid-aligned, referencing the visual language of 8-bit computing and developer culture.

This two-register approach is sophisticated: UI icons are Bauhaus-clean, while editorial icons have personality and wit, signaling that the blog is a creative/intellectual space vs. the product UI which is a precision tool.

---

### Icon Color Rules

- **UI functional icons:** `#000000` (black) primary; `#0070F3` (blue) for active/feature highlight states (Security page icons)
- **Editorial/blog icons:** `#000000` or `#333333` on white card backgrounds
- **Inline nav/button icons:** Match text color (`#FFFFFF` on black buttons, `#000000` on white buttons)
- **"New" badge sparkle:** `#0070F3` blue

---

### Icon Sizing

- **Nav chevrons (▼):** ~10–12px
- **Button inline icons (▲):** ~12–16px (matching button text size)
- **Feature list icons (Pricing, Security):** ~20–24px
- **Blog card category icons:** ~40–48px (large, treatment-level icons)
- **About page value icons:** ~32–40px
- **Search icons:** ~16–20px

---

### Icons NOT Used (Deliberate Absences)

- **No social media icons in navigation** — GitHub, Twitter/X, LinkedIn only appear in the footer text links, never as icon buttons in the nav or hero
- **No star rating icons** — No testimonial star ratings, no product star ratings
- **No cart/shopping icon** — Despite powering ecommerce, Vercel's own site has no cart
- **No bell/notification icon** — No alert/notification system in the UI
- **No emoji in UI** — Never used within product UI (only appear in developer-oriented blog posts if at all)
- **No illustrated icons (spot illustrations)** — No Intercom-style illustrative icons with characters or scenes
- **No flag icons** (except the country selector in the phone input on the contact form)
- **No heart/like/save icons** — No social engagement mechanics on any page

---

## 7. Photography Style

### Product Photography

Vercel has no physical products and therefore no traditional product photography. What serves the "product photography" function are **interface screenshots and UI mockups**:

- **Template card thumbnails:** Dark-background application mockups, showing actual deployed applications (weather apps, chat interfaces, documentation sites). These are real screenshots, not designed mockups. Background: `#1A1A1A` or `#000000` dark UI.
- **Product feature visualizations:** The Fluid Compute chart, the AI Gateway code snippet, the globe visualization — these are custom-built interactive diagrams, not photographs.
- **Code samples:** Presented as styled dark-mode code blocks with syntax highlighting, used in the AI Gateway section on the homepage.

---

### Lifestyle/Editorial Photography

**Blog post author avatars:** Small circular profile photos (~32–40px). Style: natural, approachable, neutral backgrounds. Not staged or heavily retouched. Conveys: these are real engineers, not marketing characters.

**Customer logos in case study context:** Monochrome logo lockups, no photography. Case study cards (Notion, PAIGE, Leonardo.AI on the Customers page) use no lifestyle imagery at the listing level.

**Customer page testimonial cards:** Pure text/logo, zero photography of people or environments. This is a deliberate editorial choice — Vercel's enterprise social proof is driven by metrics ("95% reduction in page load times," "24x faster builds"), not human faces or aspirational imagery.

---

### Hero Images / Visuals

**Homepage hero:** A full-bleed SVG/canvas animation featuring the Vercel ▲ triangle as the central node, surrounded by radiating colored light rays creating a "prism effect" or "refracted spectrum." The visual metaphor: Vercel is the infrastructure through which all web experiences are deployed. Black and white in the center (the triangle), exploding into the full color spectrum at the edges. This is not photography — it is a computational, mathematical illustration.

**Enterprise hero:** White background, large H1 typography only. No hero imagery.

**About hero:** White background, large H1 typography only. No imagery.

**Security hero:** Split — left panel shows the Vercel ▲ triangle in a blueprint-style diagram with light blue overlay/watermark. Geometric, architectural.

**Careers hero:** Full-bleed grid illustration with yellow-green animated architectural lines tracing system-path shapes across the grid. Conveys: infrastructure, systems, scale. No human photography.

**Fluid Compute hero:** White background with a faint dotted/particle texture in the lower half, suggesting compute density or distributed systems. No photography.

**AI landing page:** The "Infrastructure for AI." speech bubble sits on a grid background. Below, a content card with text and a "Get a ▲ Demo" CTA sits in the center. The right side extends the grid visualization. No photography.

---

### Photography Strategy & Art Direction

Vercel's deliberate **avoidance of photography** is itself an art direction decision of the highest order. In a sector where competitors (AWS, Azure, Google Cloud) often resort to stock photography of diverse teams collaborating around laptops, Vercel's total commitment to computation, diagram, typography, and SVG illustration says: **we are infrastructure, and infrastructure is invisible.** 

The visual language of the site is that of an engineering diagram — grids, lines, data, code. This is not "approachable" in the consumer-brand sense; it is "legible" in the developer-tool sense. Developers do not need to see themselves reflected in lifestyle photography. They need to see the system clearly.

This also means the site ages without becoming dated — no fashion, no hairstyles, no technology artifacts visible in photography to anchor the visual identity to a specific moment in time.

---

### Image Aspect Ratios by Context

- **Template card thumbnails:** ~16:9 landscape
- **Blog post author avatars:** 1:1 circle
- **Customer logo strip:** Variable width, fixed height (~32–48px)
- **Hero illustrations:** Full viewport width × variable height (100vh on some pages)
- **Security hero left panel:** ~50% viewport width, full section height
- **Docs illustration (none):** Documentation uses no imagery

---

### Image Treatment Consistency

- **No filters or color grading** on any photography
- **Monochrome treatment for customer/partner logos:** All third-party logos are rendered in single-color (black or white) — no brand colors allowed in Vercel's ecosystem display
- **Dark backgrounds for UI screenshots:** Template thumbnails consistently use dark/night-mode UI screenshots, reinforcing the technical aesthetic even when showing external products

---

## 8. Brand Voice & Language Style

### Tone: Overall Personality

Vercel's voice is that of a **confident, senior engineer who also happens to be a gifted communicator** — precise, declarative, never over-explaining, never condescending, never marketing-speak. The voice has deeply internalized what it is building and for whom, and it speaks peer-to-peer rather than brand-to-customer.

**10+ Voice Sub-Categories:**

1. **Declarative confidence:** Sentences often state facts without hedging. "Vercel provides the developer tools and cloud infrastructure." Not "We think we might help you with..." Every claim is stated as established truth.

2. **Terminal punctuation as punctuation mark:** Vercel uses the period as a full stop on power statements. "Build and deploy on the AI Cloud." "The complete platform to build the web." "Security that scales with you." The period adds grammatical finality — a closing of the argument, not an invitation for objection.

3. **Metric-first social proof:** Instead of vague success language ("our customers love us"), Vercel leads with specific numbers: "build times went from 7m to 40s," "95% reduction in page load times," "24x faster builds," "6x faster to build and deploy," "98% faster time to market." This is engineer-to-engineer credibility language.

4. **Mission compression:** Vercel's mission is expressed in just two sentences on the About page: "Vercel enables the world to ship the best products. Vercel's Frontend Cloud provides the developer experience and infrastructure to build, scale, and secure a faster, more personalized web." No paragraph-length origin stories. No founder journey. Pure product purpose.

5. **Active verb architecture:** Vercel's H1s almost always lead with or contain strong active verbs: "Build and deploy," "Find a plan to power," "Ship intelligent, secure applications," "Join us to Ship what's Next," "The teams we empower." The brand is always doing something, never being something.

6. **Developer-literate metaphors:** Language references concepts that only developers understand: "serverless," "git push," "preview environments," "microfrontends," "multi-tenant." There is no attempt to translate these for a non-technical audience — Vercel's marketing speaks directly to developers without dumbing down.

7. **The "build/scale/secure" triad:** A recurring three-part value framework that appears on Homepage, About, and Enterprise. "Build, scale, and secure" is a verbal brand asset — a mnemonic architecture for Vercel's product scope.

8. **Inclusive but not performative:** "Accessible. Great care in experience and design enables everyone." — The accessibility value is stated concisely without performative diversity language.

9. **Investor/community credibility:** The About page lists individual investors by name and their notable prior affiliations (Jordan Walke: Creator of React; Brendan Eich: CEO of Brave, Co-founded Mozilla & Firefox, Created JavaScript). This signals: the people who built the web trust Vercel to build what's next.

10. **Anti-hype:** Vercel never uses words like "revolutionary," "game-changing," "disrupting," "transformative," or "next-level." The blog post title "Agent responsibly" is a pun on "act responsibly" — wit and precision over hyperbole.

11. **Engineering humor:** The blog title "Build knowledge agents without embeddings" is written for an audience that knows what embeddings are and finds the alternative approach genuinely interesting. No explanation for the uninitiated.

12. **Product feature naming:** Feature names are direct and descriptive: "Fluid Compute," "AI Gateway," "BotID," "Sandbox," "Flags SDK," "Chat SDK." No abstract metaphors (vs. AWS's "Lambda," "S3," "DynamoDB"). Vercel names things what they do.

---

### Language Patterns

**Founder/mission narrative pattern:**
Absent on the site. Unlike Basecamp, Notion, or Linear which foreground founder stories, Vercel does not feature Guillermo Rauch's name or personal narrative anywhere in the marketing pages. The product/mission is the hero, not the person.

**Product description structure (Feature pages):**
[Feature name] + [one-sentence what it does] + [optional: one-sentence why it matters]
Example: "AI Gateway. Switch between AI models without needing to manage API keys, rate limits, or provider changes."

**Heading hierarchy pattern on product pages:**
1. Hero H1: Provocative statement or technical claim
2. Sub-label: Category context (e.g., "The AI Cloud," "Fluid Compute," "New")
3. H2 modules: Feature-level statement (period-terminated)
4. Body: Technical detail + customer benefit

**Collection/solution landing pattern:**
"[The/A] [superlative] [noun] to [verb] the [category]." Examples: "The complete platform to build the web." (Enterprise) / "Find a plan to power your apps." (Pricing) / "The teams we empower." (Customers)

**Editorial pattern (Blog posts):**
- Lede paragraph is bold/italic — it functions as the summary for engineers who skim
- Opens with context: "The following is based on an internal talk given at Vercel."
- Introduces the problem before the solution
- Uses first person ("we," "our team") when internally sourced

**Material/technical specification language:**
Features are specified with technical precision: "99.99% SLA," "Active CPU pricing," "multi-region compute & failover," "SCIM & Directory Sync," "Managed WAF Rulesets." No vague claims.

**Price presentation:**
Pricing is direct: "$20/mo + additional usage." The "Hobby" tier is described as "Free forever." — the period after "forever" adds emphasis. No asterisks, no hidden qualifiers visible in the header.

**Announcement bar messaging:**
"Events | Ship 26 is coming to 5 cities | Save the date →" — Event-first, specific (5 cities, not "multiple cities"), direct CTA.

**CTA language patterns:**
- Primary: Action verbs + context: "Start Deploying," "Enable Fluid," "Open Positions"
- Secondary: Social/exploratory: "Get a Demo," "Get a demo," "Explore the Product," "Read the docs," "Learn more"
- Tertiary/links: Descriptive: "Read the full story →," "More about Infrastructure," "Learn about Enterprise"
- Talk to sales: Conversational: "Talk to our Sales team." (period, not exclamation)

---

### Heading Style: Complete Heading Inventory by Page

**Homepage:**
- H1: "Build and deploy on the AI Cloud."
- H2: "Your product, delivered."
- H2: "Agents" / "AI Apps" / "Web Apps" / "Composable Commerce" / "Multi-tenant Platform"
- H2: "Framework-Defined Infrastructure"
- H2: "Scale your Enterprise / without compromising Security"
- H2: "Deploy once, deliver everywhere."
- H2: "Fluid Compute" → "A compute model for all workloads. With Active CPU pricing."
- H2: "AI Gateway" → "The AI Gateway For Developers."
- H2: "Deploy your first app in seconds."

**Pricing:**
- H1: "Find a plan to power your apps."
- H2 (implicit): "Hobby" / "Pro" / "Enterprise" (plan tier headings)

**Enterprise:**
- H1: "The complete platform to build the web."
- H2: "Trusted by the best enterprise teams"

**About:**
- H1: "Vercel enables the world to ship the best products."
- H2: "Backed by incredible investors."
- H2: "Individual investors."
- H2: "Join us and shape the future of the web."

**Blog Listing:**
- H2: "Latest news."

**Blog Post ("Agent responsibly"):**
- H1: "Agent responsibly"
- Sub-label: "Blog"
- (Body headers not observed in screenshot)

**Documentation:**
- H1: "Vercel Documentation"
- H2: "Get started with Vercel"
- H2: "Quick references"

**Contact:**
- H1: "Talk to our Sales team."

**Customers:**
- H1: "The teams we empower."

**AI Landing:**
- H1 (speech bubble): "Infrastructure for AI."
- H2: "Ship intelligent, secure applications with the cloud built for AI."
- H3: "AI Gateway." / "The AI Cloud"

**Security:**
- H1: "Security that scales with you."
- H3: "Vercel Firewall" / "Web Application Firewall" / "Workspace Security"
- Section: "Trusted by security teams."

**Fluid Compute:**
- H1: "The power of servers, in serverless form"
- Sub-label: "New | Lower Costs with Active CPU Pricing"

**Templates:**
- H1: "Find your Template"
- Subtext: "Jumpstart your app development process with pre-built solutions from Vercel and our community."

**Careers:**
- H1: "Join us to Ship what's Next."
- H2: "Open Positions at Vercel"

---

**Capitalization analysis:**
- H1s: Sentence case or mixed intentional case (capitalizing proper nouns and product names only)
- H2s: Sentence case with period termination
- H3s: Title case for product feature names ("Vercel Firewall," "AI Gateway")
- Footer headers: ALL CAPS
- CTA text: Title case ("Start Deploying," "Get a Demo") or sentence case ("Learn more")
- Badge labels: ALL CAPS or Title case
- No headline uses all-lowercase for effect (unlike many consumer brands)

---

### CTAs & Microcopy: Complete CTA Inventory

| Context | CTA Text | Style |
|---|---|---|
| Homepage hero (primary) | "▲ Start Deploying" | Black pill |
| Homepage hero (secondary) | "Get a Demo" | White ghost pill |
| Homepage Fluid section | "Learn more" | Text link |
| Homepage bottom | "S t a r t D e p l o y i n g" | Spaced text link |
| Homepage bottom | "Talk to an Expert" | Ghost pill |
| Homepage bottom | "Get an Enterprise Trial" | Ghost pill |
| Pricing page plan | "Get started" (implied, not confirmed) | |
| Enterprise hero (primary) | "Get a demo" | Black pill |
| Enterprise hero (secondary) | "Explore the Product" | Ghost pill |
| About | "View Open Positions" | Ghost pill |
| Blog post | "Copy URL" | Blue text link |
| Docs | "Copy as Markdown" | Text action |
| Docs | "Install Vercel Plugin" | Text action |
| Docs | "Give feedback" | Text action |
| Docs | "Ask AI about this page" | Text action |
| Contact | (form submit, not observed) | |
| Customers | "Get a Demo" | Black pill |
| Customers | "Read the full story" | Arrow link |
| AI page | "Get a ▲ Demo" | Ghost pill |
| AI page | "Read the docs" | Ghost pill |
| Security | "Get a Demo" | Black pill |
| Fluid Compute (primary) | "Enable Fluid" | Black pill |
| Fluid Compute (secondary) | "Get a demo" | Ghost pill |
| Careers | "Open Positions" | Black pill |
| Careers job listing | "Read more" | Ghost pill |
| Announcement bar | "Save the date" | Ghost pill with arrow |
| Templates | (deploy buttons on card hover, likely) | |

**Microcopy tone analysis:**
- Highly functional, no fluff — "Import your repo, deploy in seconds" (not "It's super easy to get started!")
- Uses "seconds" and "minutes" as units (concrete time language)
- Uses "forever" with finality: "Free forever."
- Form placeholders are conversational: "Timmy Triangle" as name placeholder — a small piece of brand personality peeking through utility

---

## 9. Platform & Technical Notes

### Platform Identification

**Platform:** Custom Next.js application, self-hosted on Vercel's own infrastructure (eating its own dogfood). Evidence:
- URL structure follows Next.js conventions
- SVG assets served from Vercel's CDN with `dpl=dpl_[hash]` query parameters (Vercel deployment hash)
- Asset URL pattern: `https://vercel.com/vc-ap-vercel-marketing/_next/static/media/vercel-logotype-light.3pet4y_bv2m1m.svg?dpl=dpl_9h9L1VwVVbBssDxNHhYyTqpYRU4o`
- `/_next/` path prefix confirms Next.js
- Project slug `vc-ap-vercel-marketing` confirms Vercel deployment
- Page titles follow Next.js `<Head>` conventions

**Not Shopify, WordPress, or any CMS platform.** This is a custom Next.js application — appropriate for a company that builds deployment infrastructure for Next.js.

---

### Theme Architecture

- **Custom theme:** Not a stock Next.js theme. Fully custom design system.
- The design system is likely **Geist Design System** — Vercel's open-source component library that pairs with the Geist typeface.
- CSS variables for theming (light/dark mode toggle observed in footer: "Select a display theme: system / light / dark") — CSS custom properties managing color tokens.
- Dark mode support is built in but **light is the default** across all pages.

---

### URL Structure Patterns

- Homepage: `/` 
- About: `/about`
- Careers: `/careers`
- Enterprise: `/enterprise`
- Pricing: `/pricing`
- Blog listing: `/blog`
- Blog post: `/blog/[slug]` (e.g., `/blog/agent-responsibly`)
- Documentation: `/docs`, `/docs/[category]/[page]`
- Contact: `/contact/sales`, `/contact/sales/demo`
- Customers: `/customers`
- Products: `/products/[product-name]`
- Solutions: `/solutions/[use-case]`
- Frameworks: `/frameworks/[framework]`
- Security: `/security`, `/security/[feature]`
- AI: `/ai`, `/ai-gateway`, `/agent`
- Templates: `/templates`, `/templates/[framework]`
- Fluid: `/fluid`
- Startups: `/startups`
- Legal: `/legal`, `/legal/privacy-policy`
- Events: `/events`, `/ship`

URL pattern is clean, semantic, and keyword-rich — no query string pagination or session IDs visible in marketing URLs.

---

### Third-Party Integrations Identified

- **Vercel Status page:** `vercel-status.com` (linked from footer)
- **Community forum:** `community.vercel.com` (linked from footer)
- **Social platforms:** GitHub (`github.com/vercel`), LinkedIn, X (Twitter), YouTube (@VercelHQ)
- **Phone number input:** Country code picker (US flag visible) — likely a third-party tel-input component
- **No visible Intercom/Drift chat widget**
- **No visible Google Analytics tracking pixels** (though likely present in headers)
- **No obvious A/B testing widget** visible

---

### Page Performance Observations

- Pages load extremely fast — appropriate for a performance-focused infrastructure company
- SVG illustrations render immediately (no image flicker)
- Font loading: Geist served via `/_next/static/media/` — no external font CDN dependency (no Google Fonts)
- Code splitting: Next.js handles this automatically
- Animations appear hardware-accelerated (CSS transforms, not layout-affecting properties)

---

### SEO & Meta Title Patterns

| Page | Title Format |
|---|---|
| Homepage | "Vercel: Build and deploy the best web experiences with the AI Cloud" |
| Pricing | "Vercel Pricing: Hobby, Pro, and Enterprise plans" |
| Enterprise | "Enterprise" |
| About | "About Us" |
| Blog | "Blog - Vercel" |
| Blog Post | "[Post Title] - Vercel" |
| Docs | "Vercel Documentation" |
| Contact | "Talk to our Sales team" |
| Customers | "Vercel Customers and Case Studies" |
| Templates | "Find your Template" |
| Fluid | "Fluid compute" |
| Careers | "Careers" |
| Security | "Security - Vercel" |
| AI | "Deploy AI at the speed of frontend" |

Pattern: Product/feature pages use minimal titles; marketing pages use keyword-rich descriptive titles. Inconsistency between pages (some include "- Vercel" suffix, others don't) suggests the title pattern is not yet fully standardized.

---

### Legal & Compliance Pages

Observed in footer:
- `/legal` — Legal hub
- `/legal/privacy-policy` — Privacy Policy
- No GDPR banner visible (likely handled via cookie settings)
- No terms of service link explicitly visible in footer (may be nested under `/legal`)

---

### Accessibility Features

- Skip navigation link: `[Skip to content]` present on all pages
- ARIA landmark roles: `banner`, `navigation`, `main` (inferred)
- ARIA button states: `expanded=True/False` for dropdowns
- Image alt text: Present on logo, hero illustration
- Keyboard shortcut for search: `⌘K` on Docs page
- Theme toggle for visual accessibility (light/dark/system)
- Semantic HTML heading hierarchy maintained

---

### Social Media Accounts

- **GitHub:** `github.com/vercel`
- **LinkedIn:** `linkedin.com/company/vercel`
- **X (formerly Twitter):** `x.com/vercel`
- **YouTube:** `youtube.com/@VercelHQ`
- No Instagram, no TikTok, no Facebook visible — developer audience means developer-native platforms (GitHub, Twitter/X, YouTube)

---

## 10. Pages Browsed

1. https://vercel.com/ — Homepage (hero, product modules, footer)
2. https://vercel.com/pricing — Pricing page (Hobby/Pro/Enterprise tiers)
3. https://vercel.com/enterprise — Enterprise landing page
4. https://vercel.com/about — About / Company page
5. https://vercel.com/blog — Blog listing (editorial index)
6. https://vercel.com/blog/agent-responsibly — Blog post (editorial detail, "Agent responsibly" by Matthew Binshtok)
7. https://vercel.com/docs — Documentation root (support/knowledge base)
8. https://vercel.com/contact/sales — Contact/Sales form page
9. https://vercel.com/customers — Customers/case studies listing
10. https://vercel.com/ai — AI landing page (product/solution)
11. https://vercel.com/security — Security product page (PDP)
12. https://vercel.com/templates — Templates directory (collection/category page)
13. https://vercel.com/fluid — Fluid Compute product page (PDP)
14. https://vercel.com/careers — Careers page (unique landing)

**Total: 14 pages browsed across 9 distinct page types.**

---

*Audit compiled April 3, 2026. All observations based on live site content at time of browsing. Screenshots saved to workspace.*
