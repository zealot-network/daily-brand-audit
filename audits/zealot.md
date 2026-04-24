# Zealot Brand Standards Audit -- extracted from https://www.zealot.company across 14 pages (March 2026)

---

## 1. Color Palette

### Complete Color Token Inventory (from CSS `:root`)

The site uses an HSL-based design token system defined in the CSS `:root`. All colors are expressed as HSL values and consumed via CSS custom properties using `hsl(var(--token))`. This is a modern, systematic approach that enables programmatic theme toggling (light/dark modes are supported).

**Light Mode Color Tokens:**

| Token Name | HSL Value | Computed Hex Approx. | Role |
|---|---|---|---|
| `--background` | 0 0% 100% | `#FFFFFF` | Page background — pure white |
| `--foreground` | 196 100% 13% | `#002B33` (deep teal-black) | Primary body text color |
| `--primary` | 196 100% 13% | `#002B33` | Primary brand color — deep dark teal |
| `--primary-foreground` | 0 0% 98% | `#FAFAFA` | Text on primary backgrounds |
| `--secondary` | 44 58% 50% | `#C9A227` (warm gold) | Gold/amber accent — secondary brand color |
| `--secondary-foreground` | 196 100% 13% | `#002B33` | Text on gold/amber |
| `--accent` | 182 26% 31% | `#3D6B68` (muted teal) | Tertiary accent — muted teal-green |
| `--accent-foreground` | 0 0% 98% | `#FAFAFA` | Text on accent backgrounds |
| `--muted` | 51 24% 89% | `#EAE5D4` (warm cream) | Muted backgrounds — sections, cards |
| `--muted-foreground` | 196 100% 13% | `#002B33` | Text on muted/cream backgrounds |
| `--border` | 51 24% 89% | `#EAE5D4` | Border color — same as muted |
| `--input` | 51 24% 89% | `#EAE5D4` | Form input border/background |
| `--ring` | 44 58% 50% | `#C9A227` | Focus ring — gold, same as secondary |
| `--success` | 75 32% 29% | `#4A5922` (olive green) | Success states |
| `--destructive` | 0 84.2% 60.2% | `#EF4444` | Error/destructive states |
| `--card` | 0 0% 100% | `#FFFFFF` | Card backgrounds |

**Dark Mode Color Tokens (`.dark` class):**

| Token Name | HSL Value | Computed Hex Approx. | Role |
|---|---|---|---|
| `--background` | 196 100% 8% | `#001A1F` (very deep teal-black) | Dark page background |
| `--foreground` | 0 0% 98% | `#FAFAFA` | Light text on dark |
| `--primary` | 44 58% 50% | `#C9A227` (gold flips to primary in dark mode) | Gold becomes the primary in dark mode |
| `--primary-foreground` | 196 100% 13% | `#002B33` | Text on gold buttons |
| `--secondary` | 196 100% 13% | `#002B33` | Deep teal becomes secondary in dark |
| `--muted` | 196 100% 15% | `#004D5E` | Dark muted backgrounds |
| `--muted-foreground` | 51 24% 75% | `#C4B88A` | Warm cream-tan text on dark muted |
| `--accent` | 182 26% 35% | `#456F6C` | Muted teal in dark mode |
| `--border` | 196 100% 15% | `#004D5E` | Dark borders |

**Gradient Definitions:**
- `--gradient-primary`: `linear-gradient(135deg, hsl(196 100% 13%), hsl(182 26% 31%))` — Deep teal → muted teal
- `--gradient-gold`: `linear-gradient(135deg, hsl(44 58% 50%), hsl(44 58% 60%))` — Gold → lighter gold
- `--gradient-hero`: `linear-gradient(135deg, hsl(196 100% 13% / .95), hsl(182 26% 31% / .9))` — Hero overlay with 95/90% opacity

**Additional Inline Colors Found in CSS:**
- `#9CA3AF` — gray-400, used for placeholder text
- `#E5E7EB` — gray-200, used for default border color in TailwindCSS base
- `#EF4444` — red-500, destructive/error
- `#22C55E` — green-500, success indicator
- `#EAB308` — yellow-500, warning states
- `#DC2626` — red-600, destructive hover
- `#FFFFFF` — white, various
- `#CCCCCC` — light gray, fallback
- Various RGBA black overlays: `rgba(0,0,0,0.8)`, `rgba(0,0,0,0.75)`, `rgba(0,0,0,0.5)` — used for hero image darkening overlays

### Key Observation on Palette Strategy and Restraint/Richness

The Zealot palette is one of studied **aristocratic restraint** — just three foundational colors do all the heavy lifting: a nearly-black deep teal (`#002B33`), a rich warm gold (`#C9A227`), and an off-white/cream (`#FAFAFA`, `#EAE5D4`). This palette communicates **institutional authority, heritage, and faith-adjacent gravitas** without veering into religious kitsch. The gold specifically signals premium positioning, legacy, and treasure — consistent with the firm's identity around building "ventures that last."

The palette is deliberately **non-tech**: it avoids the blues/grays/purples associated with SaaS or venture capital, instead choosing warmth and depth. This is a firm that wants to feel more like a trusted advisor or law firm than a startup accelerator.

The **color inversion strategy in dark mode** is sophisticated: gold (`--secondary`) and deep teal (`--primary`) swap their `primary/secondary` roles, so in dark mode the gold becomes the primary interactive color against a near-black teal canvas. This is not a simple `#000000` dark mode — it's a considered dual-theme system.

### Color Application by Page Type

**Homepage:**
- Hero section: Full-bleed photographic background (street scene of Franklin, TN at dusk with golden-hour light), nav bar uses `background/95` (translucent white), text in white/cream over the photo
- "WHO WE ARE" section: White/cream background (`#FFFFFF`), section label in `--secondary` gold (`#C9A227`), h2 in `--foreground` deep teal-black
- "HOW WE HELP" services carousel: `--muted` warm cream background (`#EAE5D4`), service cards with white backgrounds and `--border` edges
- "OUR PORTFOLIO" section: White background, venture logos/images in their native colors
- "OUR CLIENTS" section: Warm cream muted background, category labels in gold
- "LEADERSHIP" (Brett Henry): White background with large photographic portrait
- Contact form: White background, input fields with `--input` border (`#EAE5D4`), primary CTA in deep teal `--primary`

**Team page:**
- Hero area: Very light background (nearly white, slight cream gradient)
- Team cards: Clean white cards with circular profile photos, accordion items with `--border` dividers

**Auth/Login page:**
- Pure white background (`#FFFFFF`), centered layout, deep teal form inputs, primary CTA button in deep teal with white text

**404 page:**
- Pure white background, minimal — deep teal text, single link in teal

**Dark Mode (across all pages):**
- Background shifts to near-black deep teal (`#001A1F`)
- Text becomes `#FAFAFA`
- Gold accent (`#C9A227`) becomes primary interactive/highlight color
- Section labels and headings render in gold tone
- A distinctly cinematic, editorial dark look — like a premium membership club

### Color Hierarchy & Emotional Role Analysis

1. **Deep Teal-Black (`#002B33` / `hsl(196 100% 13%)`)** — The foundational "Authority Color." This is the color of depth, certainty, and wisdom. It functions like a navy or charcoal but with a unique personality — slightly tropical, alive. Used for: primary text, nav bar backgrounds, CTA buttons, footer.

2. **Warm Gold (`#C9A227` / `hsl(44 58% 50%)`)** — The "Value Signal Color." Not a flashy pop gold but a muted, aged gold that reads as earned rather than borrowed. Used for: section labels (e.g., "STRATEGIC CONSULTANCY," "WHO WE ARE"), focus rings, hover states, heading text accents. In dark mode it becomes the dominant interactive color.

3. **Off-White / Warm Cream (`#EAE5D4` / `hsl(51 24% 89%)`)** — The "Breathing Space Color." A slightly warm, parchment-adjacent white that prevents the site from feeling cold or clinical. Used for: section backgrounds, borders, form inputs, service card backgrounds.

4. **White (`#FFFFFF`)** — Pure white used for maximum contrast sections, card backgrounds, and primary layout canvas. Alternates with cream to create rhythm.

5. **Muted Teal (`#3D6B68` / `hsl(182 26% 31%)`)** — Supporting role, used in gradients and as a middle tone between the deep primary and lighter backgrounds.

### Colors Deliberately NOT Used

- **Bright/neon blues, purples, or electric greens** — no tech-brand colors whatsoever. This is a firm distinguishing itself from Silicon Valley aesthetics.
- **Flat grays** — while gray-400 (`#9CA3AF`) appears in placeholder text, no neutral gray dominates the UI. The palette is warm-spectrum only.
- **Red as a brand color** — red only appears in purely functional destructive states (error messages), never in branding.
- **Black (#000000)** — the darkest color is actually deep teal-black, not pure black. This preserves warmth even in dark contexts.
- **Orange, pink, or purple** — entirely absent from the brand palette. These colors would undermine the conservative, trustworthy positioning.
- **Gradient rainbow or multi-color fills** — no RGB iridescent gradients or trendy prismatic treatments. Gradients are monochromatic (teal-to-teal, gold-to-gold).

---

## 2. Typography

### Font Families Identified

The CSS `--font-sans` and `--font-serif` variables reveal a deliberate two-font system:

1. **Inter** — `"Inter", ui-sans-serif, system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, "Noto Sans", sans-serif`
   - A geometric humanist sans-serif designed by Rasmus Andersson, optimized for screen readability
   - Used for all body copy, navigation labels, form labels, metadata, section labels, utility text
   - Closest comparables: Helvetica Neue, SF Pro Text

2. **Cormorant Garamond** — `"Cormorant Garamond", Georgia, serif`
   - A high-fashion, ultra-refined display serif with extreme contrast between thick and thin strokes
   - Inspired by the Renaissance Garamond typeface, revived for digital by Christian Thalmann
   - Used for primary headings, hero text, names, and decorative italic/serif emphasis elements
   - The specific italic weight of Cormorant is used for the *italicized* parts of split headings (e.g., "Foster *Friendship*", "Our *expertise*", "Ventures we *believe in*")

**No monospace or display-only fonts are used.** The two-font system is absolute and disciplined.

### Complete Font Usage Map

| Element | Font Family | Weight | Case | Approx. Size | Letter-Spacing | Notes |
|---|---|---|---|---|---|---|
| Hero H1 "Foster / Friendship" | Cormorant Garamond | 400 (regular + italic) | Sentence case | ~120–140px (viewport-relative) | Normal | Two-line split; "Foster" in roman, "Friendship" in italic |
| Section label (e.g., "STRATEGIC CONSULTANCY", "WHO WE ARE") | Inter | 500–600 (medium/semibold) | ALL CAPS | ~11–12px | Wide (0.15–0.2em) | Gold color (`--secondary`), small but commanding |
| H2 section headings (e.g., "Building ventures that last") | Cormorant Garamond | 400 (roman + italic split) | Mixed sentence case | ~48–72px | Normal | Italic applied to second/emphasis word only |
| H3 service/venture headings (e.g., "Consulting & Strategy") | Cormorant Garamond | 500–600 | Sentence case | ~24–32px | Normal | Used within cards and list items |
| H4 sub-section labels (e.g., "NOTABLE WORK", "AREAS OF EXPERTISE") | Inter | 700 (bold) | ALL CAPS | ~11–12px | Wide (0.12–0.18em) | Text color: `--foreground` deep teal-black |
| Body paragraph text | Inter | 400 (regular) | Sentence case | ~16–18px | Normal | Leading ~1.6–1.75 for readability |
| Navigation links (About, Services, Portfolio…) | Inter | 400–500 | Sentence case | ~14–15px | Normal | Subtle, refined — not bold nav |
| "Book Consultation" CTA button | Inter | 500–600 | Sentence case | ~14px | Slight positive | Contained button with border |
| Form labels ("YOUR NAME", "EMAIL ADDRESS") | Inter | 500–600 | ALL CAPS | ~11–12px | Wide | Gold color (`--secondary`) |
| Form placeholder text | Inter | 400 | Sentence case | ~16px | Normal | Color: `#9CA3AF` (gray-400) |
| Footer navigation links | Inter | 400 | Sentence case | ~14px | Normal | |
| Footer copyright | Inter | 400 | Sentence case | ~13px | Normal | Muted foreground |
| Team page partner names (e.g., "Joel Allen") | Cormorant Garamond + Inter | 400/600 | Mixed | ~22–28px / ~13px | Normal/Wide | Name in serif, title in Inter small-caps-style |
| Auth page logo wordmark "ZEALOT" | Inter | 300–400 (light/regular) | ALL CAPS | ~32–36px | Wide (~0.2em+) | Centered, architectural |
| Auth page heading "Welcome Back" | Cormorant Garamond | 400 | Title case | ~28–32px | Normal | Italic-inflected serif heading |
| Auth form labels | Inter | 500 | ALL CAPS | ~11–12px | Wide | |
| Blockquote (footer of contact section) | Cormorant Garamond | 400 italic | Sentence case | ~22–26px | Normal | `"We believe the best work happens…"` |
| Number labels "01", "02", "03" | Inter or Cormorant | 400–500 | Numeric | ~14–16px | Normal | Muted teal/foreground color |
| Expertise tag pills (e.g., "Systems Building", "Blockchain") | Inter | 400–500 | Title case | ~13–14px | Normal | Rounded border containers |
| Scroll indicator "SCROLL" | Inter | 500 | ALL CAPS | ~11–12px | Wide | With chevron icon below |
| Service card icon description | Inter | 500 | Sentence case | ~13px | Normal | Below icon in card |

### Typography Application by Page Type

**Homepage:**
- The typographic architecture moves from display-scale (120px+ serif) at hero → medium scale (48–72px) at section headings → body text (16–18px) at content → small caps labels (11–12px) at section identifiers.
- The italic serif split-heading technique is used 4 times on the homepage: "Foster *Friendship*", "Building ventures that *last*", "Our *expertise*", "Ventures we *believe in*", "Champions of *purpose*", "Stories of *transformation*", "Let's start a *conversation*"
- This creates a recurring typographic "signature" — the plain/italic serif split is the most distinctive typographic move on the site.

**Team page:**
- Hero heading "Our *Team*" follows the same italic-serif split pattern
- Subheading "Founder & *Principal*" follows the same pattern
- Bio text in Inter body copy ~16–18px
- Partner accordion names in Cormorant Garamond ~22–24px, role titles in Inter small-caps style ~12–13px

**Auth/Login page:**
- Wordmark "ZEALOT" rendered in ALL CAPS Inter with wide tracking — functions as a logotype substitute
- "Welcome Back" / "Create Account" in Cormorant Garamond italic heading style
- All form elements in Inter

**404 page:**
- "404" in Inter bold, very large (~80px)
- "Oops! Page not found" in Inter body

### Font Pairing Philosophy (Semiotic Analysis)

The Inter + Cormorant Garamond pairing is a **tension-based harmony**: Inter brings modernity, precision, and systemic clarity (a typeface literally designed for the digital grid); Cormorant Garamond brings history, craft, and emotional weight (a typeface with 500 years of heritage). Together, they communicate Zealot's core positioning: **a modern operating system for timeless values**.

The choice of Cormorant specifically (over, say, Playfair Display or Canela) is notable: Cormorant has extreme thin strokes that push it toward fashion/luxury territory, giving Zealot headings a sophistication that exceeds its business category. This is a deliberate aspirational signal — the firm positions itself at the intersection of strategy consulting and cultural taste-making.

### Weight Distribution Analysis

- **Light (300):** Rarely used — only potentially in the auth wordmark logo
- **Regular (400):** Dominant weight — all body copy, most serif headings, nav links
- **Medium (500):** Section labels, form labels, some nav items
- **Semibold (600):** Stronger labels, some headings in smaller contexts
- **Bold (700):** Sub-section ALL CAPS labels (NOTABLE WORK, AREAS OF EXPERTISE), the strongest emphasis text
- **ExtraBold/Black:** Not observed

The weight distribution skews toward **restraint** — no bludgeoning the reader with heavy weights. The hierarchy is created through size, case, and serif-vs-sans contrast rather than weight brutalism.

### Letter-Spacing Rules

- **ALL CAPS Inter labels (section identifiers, form labels):** Wide positive tracking (~0.12–0.2em / ~1.5–3px at 12px size). This transforms Inter into a refined small-caps equivalent.
- **Body Inter text:** Default/normal tracking (0)
- **Cormorant Garamond headings:** Minimal/default tracking — the serif's own character spacing is refined enough; adding tracking would over-loosen it
- **"ZEALOT" auth wordmark:** Very wide tracking (~0.3em+) — letters breathe apart, creating a monogram-like feeling

### Complete Type Scale Summary

| Level | Font | Size (approx.) | Usage |
|---|---|---|---|
| Display | Cormorant Garamond | 120–140px | Hero H1 |
| H1 Section | Cormorant Garamond | 64–80px | Primary section headings |
| H2 | Cormorant Garamond | 42–56px | Sub-section headings |
| H3 | Cormorant Garamond | 24–32px | Card/item headings |
| Label XL | Inter | 14–16px | Nav links, button text |
| Body | Inter | 16–18px | Paragraph text |
| Label SM | Inter | 11–13px | Section identifiers, form labels (ALL CAPS) |
| Micro | Inter | 11–12px | Footer links, copyright, tags |

---

## 3. Logo & Wordmark

### Primary Logo Description

The Zealot logo is a **horizontal wordmark** — the word "ZEALOT" rendered in all-caps, in what appears to be a refined geometric sans-serif typeface (visually consistent with Inter or a custom/similar sans), with wide letter-spacing. The wordmark appears in:

1. **Navigation bar (top-left):** Small, approximately 80px wide × 30px tall, in dark teal-black (`--foreground` / `#002B33`) on white/transparent background. The logo image file is: `https://www.zealot.company/assets/zealot-logo-BRuBDO0X.png`
2. **Footer (bottom-left):** Same wordmark image, approximately 80–100px wide, rendered in the footer column on the left.
3. **Auth page (centered):** A centered wordmark version, slightly larger at ~100px width, with notably wide letter-spacing — functioning as a centered brand stamp.
4. **AI Chatbot header:** A tiny version of the Zealot "leaf/flame" icon (from the chatbot favicon asset `zealot-chat-logo-CYzW2Ulh.png`) appears in the chat widget header and the floating chatbot button.

### Logo Characteristics

- **Typeface style:** All-caps geometric sans-serif, refined and architectural. The letterforms are clean, without decorative serifs or humanist variations.
- **Weight:** Light to regular — the logo maintains delicacy rather than heavy bolding
- **Tracking:** Wide — letters are spaced generously, giving the wordmark an expansive, unhurried quality
- **No icon/mark accompanying the wordmark in the nav or footer** — pure wordmark system

### Brand Mark / Icon System

Alongside the wordmark, Zealot has a secondary mark: a stylized **olive branch or flame-leaf icon** that appears exclusively in the AI chatbot floating button and chat header. This icon is rendered in a warm gold-green tone. It appears to be an abstracted botanical/flame symbol. This mark is NOT used in the main navigation, header, or footer — it is isolated to the AI advisor product, suggesting it functions as a sub-brand mark for that tool rather than the primary brand.

### Placement Rules (Observed)

- **Navigation:** Top-left, vertically centered within the 60px-tall sticky header. Left-aligned to the page's left margin (~32px from edge).
- **Footer:** Bottom-left of the footer row, aligned to the content grid's left edge.
- **Auth page:** Perfectly centered, with extra vertical space above and below.
- **No reversed (white-on-dark) version** was observed in the primary navigation; the logo appears to be a single dark/teal color that works on both white and translucent-over-photo backgrounds due to its dark tone.

### Color Variations Observed

- **Dark teal-black version** — primary usage, on white/light backgrounds
- The auth page login form shows the same logo coloring. No white version observed in primary UI, though the dark mode may render it differently.

### Logo Sizing

- Nav bar: ~80–110px wide
- Footer: ~80px wide
- Auth page centered: ~100–120px wide

### Logo Relationship to Brand Heritage/Positioning

The all-caps wordmark-only approach is a strategic choice that communicates **confidence without embellishment** — comparable to how legacy consulting firms (McKinsey, Bain) or luxury fashion houses (CELINE, BOTTEGA VENETA) rely on the name itself as the mark. The firm is saying: "Our name is our proof." The word "Zealot" itself carries theological and emotional charge — a person of extreme devotion — which the clean, measured wordmark holds in productive tension. The logo doesn't shout; it commands.

---

## 4. Layout & Grid System

### Global Structure

- **Max-width container:** `max-width: 1400px` at breakpoint `≥1400px`, with `padding-right: 2rem; padding-left: 2rem` (32px each side). Below 1400px the container is full-width with 32px gutters.
- **Body font family:** Inter (sans-serif)
- **Default border-radius:** `--radius: 0.75rem` (12px) — used on cards and buttons
- **Section vertical spacing:** `--spacing-section: 12rem` (192px) desktop; `--spacing-section-mobile: 6rem` (96px) mobile
- **Header height:** ~60px (sticky, fixed to top, uses `bg-background/95` translucent white with `backdrop-blur`)
- **Scroll behavior:** `scroll-behavior: smooth` global

### Page Templates Identified

**Homepage (SPA single-page scroll architecture):**
The entire site is architected as a long-scroll, single-page application with anchor navigation. The homepage is the primary content canvas containing: Hero → About/Who We Are → How We Help (Services) → Portfolio → Clients → Client Impact Stories → Leadership → Contact/Form → Footer. Each section is a full-width module with alternating cream/white backgrounds.

**Team page (`/team`):**
- Separate route, only standalone page beyond auth
- Hero section (nearly full-viewport height, centered text, gradient background)
- Founder featured section (two-column: large portrait left, bio right)
- Key Achievements list
- Key Partners accordion list (three partners with circular photos, expandable bios)
- Footer
- Background: near-white with subtle gradient, not the full-bleed photo approach of homepage

**Auth page (`/auth`):**
- Minimal centered single-column layout
- No nav bar (clean, distraction-free)
- Logo centered top, form centered middle, navigation links bottom
- Pure white background, maximum whitespace

**404 page:**
- Centered single-column, just number, message, and return link
- Teal-on-white, minimal

### Product Card Anatomy (Portfolio/Venture Cards)

Each portfolio venture card on the homepage uses:
- **Logo image** (square/rounded-square logo mark) in the upper area, ~75px × 75px
- **Venture name** in Cormorant Garamond H3 (~24–28px)
- **Short description paragraph** in Inter body (~14–16px, muted foreground)
- **Grid layout:** A 2-column grid with varying row heights — some ventures span full width (DECO DAO, Apostle, Zealot Media, Liberty Cigar), some are in side-by-side pairs (Triumph Roofing / Swift Property Solutions, and Ten Boom Coffee / [partner])
- **No price, no CTA button on venture cards** — informational only, no explicit "learn more" button per card
- **Hover behavior:** Not explicitly confirmed from screenshots; likely cursor: pointer based on the interactive nature

### Client Cards (Our Clients section)

- Three-column grid layout
- Each card has: category label in gold ALL CAPS Inter (e.g., "AI-POWERED ACCOUNTING"), venture name in Cormorant Garamond H3, logo image (tall-format, approximately 300px height), short description in Inter body
- Background: warm cream `--muted`

### Service/Expertise Cards (How We Help carousel)

- Horizontally scrollable carousel with visible arrow control
- Each card: icon (custom SVG illustration), service heading in Cormorant Garamond H3, description body in Inter
- Card background: white on cream section background
- Card minimum height: ~350px (from CSS `min-h-[350px]`)
- A "Scroll right" arrow button positioned at the right edge

### Responsive Behavior (Breakpoints)

From TailwindCSS utilities observed in the CSS:
- **Mobile:** Single column, `gap-4` or `gap-6`, stacked layouts
- **Small (`sm:`):** Begins allowing 2-column grids for some components
- **Medium (`md:`):** Two-column primary layouts (like the Brett Henry bio section with portrait left, text right)
- **Large (`lg:`):** Three or more column grids, full carousel behavior
- **XL (`xl:`):** Wider grid gaps, larger typography
- Section spacing: desktop `12rem` (192px), mobile `6rem` (96px) — a 2:1 ratio

### Whitespace Strategy

Zealot uses whitespace as a **primary design element** — not as empty space but as breathing room that communicates premium quality. Each section is generously padded (192px top/bottom on desktop). Text blocks are never crowded. The page has a slow, meditative scroll rhythm that demands the reader slow down. This is anti-efficiency design — you cannot skim through this site quickly, and that is intentional.

### Grid Alignment Philosophy

Left-aligned for body copy and section labels, but section headings frequently break the left-align pattern with **centered or right-weighted layouts** in specific sections (particularly the Brett Henry leadership section where text is right-column and image is left-column). The homepage uses a two-column layout for most prominent content blocks.

### Homepage Scroll Architecture (Module Pattern)

1. **Hero** — Full-bleed photographic, 100vh, dual CTA
2. **WHO WE ARE** — Two-column: image left (office exterior), numbered pillars right
3. **HOW WE HELP** — Left header column, right horizontal scrolling service carousel
4. **OUR PORTFOLIO** — Left heading column, right portfolio grid (7 ventures)
5. **OUR CLIENTS** — Left heading column, three-column client cards grid
6. **CLIENT IMPACT** — Full-width featured client story carousel (Ten Boom Coffee first)
7. **LEADERSHIP** — Two-column: portrait left, bio/achievements right
8. **GET IN TOUCH** — Two-column: form left, contact info + quote right
9. **FOOTER** — Four-column: logo + nav links + email/location

### Footer Layout Details

- **Full-width**, no max-width container visible — spans full bleed
- **Top row:** Logo (left) | Nav links (center: About, Services, Portfolio, Contact) | Email + Location (right)
- **Bottom row:** Copyright text centered: "© 2026 Zealot. Building systems, scaling ventures, fostering friendship."
- **Background:** White (`--background`)
- **Divider:** None visible — footer flows from the page
- **Social links:** NOT present in footer
- **Columns:** ~3 columns on desktop, stacked on mobile

### Layout Elements Deliberately NOT Present

- **Announcement bar / banner** — none (not an e-commerce context)
- **Sidebar navigation** — none; full top-nav only
- **Breadcrumbs** — not applicable given single-page structure
- **Sticky sidebar** — none on any page
- **Full-screen menu overlay** — not observed (mobile behavior unknown from screenshots)
- **Scroll progress indicators** — not observed
- **Back-to-top button** — not observed (though the floating AI button occupies that corner position)

---

## 5. UI Components

### Buttons

**Primary CTA Button ("Book a Consultation")**
- Background: `--primary` (`#002B33` deep teal-black)
- Text: `--primary-foreground` (near-white `#FAFAFA`), Inter, ~14px, medium weight
- Border: None (solid fill)
- Border-radius: `--radius` (0.75rem / 12px)
- Height: ~48px (from `min-h-[48px]` CSS class)
- Padding: ~16px horizontal
- Shadow: `--shadow-elegant` (`0 10px 30px -10px hsl(196 100% 13% / .3)`)
- Hover: Likely darkens or adds gold border — not captured in screenshots but transition-smooth is defined (`all .3s cubic-bezier(.4, 0, .2, 1)`)

**Secondary CTA Button ("Explore Our Work")**
- Background: Transparent
- Border: 1px solid, likely `--border` or `--primary` tone
- Text: White/light (on hero photo background)
- Border-radius: Same 12px
- Height: ~48px
- This is a ghost/outline button variant

**Form Submit Button ("Send Message")**
- Background: `--primary` deep teal
- Text: White, Inter medium
- Full-width or left-aligned
- Height: ~48px
- Border-radius: 12px

**Auth Form Button ("Sign In" / "Sign Up")**
- Background: `--primary` deep teal-black (`#002B33`)
- Text: White, Inter, ~14–15px medium/semibold
- Border-radius: 12px
- Full-width within the form container (~420px)
- Height: ~48px

**Scroll Arrow Button ("Scroll right")**
- Small circular or rectangular button
- Background: likely white/card with border
- Icon-only (chevron right)
- Position: absolute right edge of carousel

**Team Partner Accordion Expand Button**
- Down chevron icon on right side of partner row
- On row background (`--card` white), `--border` bottom
- No visual button container — the entire row is the clickable target

### Navigation

**Desktop Navigation:**
- Sticky, top-fixed, full-width header bar
- Height: ~60px
- Background: `--background/95` (95% opacity white with backdrop-blur) in light mode; dark teal in dark mode
- Logo: Left-aligned
- Nav links: Center-right cluster — About | Services | Portfolio | Clients | Team | Contact | [divider] Book Consultation | Sign In | Theme Toggle
- "Book Consultation" is styled as a bordered button/pill, distinctly separate from plain text links
- "Sign In" has a user-icon before the text
- "Theme toggle" is a sun/moon icon button
- **No mega-menu** — all primary nav links are anchor-scroll links (except Team and Sign In which navigate to separate pages)
- **No dropdown submenus**
- Nav link hover state: likely underline or color shift based on the CSS transition-smooth definition

**Mobile Navigation:**
- Not captured in screenshots; likely a hamburger menu based on the hidden/visible responsive classes in CSS

### Forms (Contact Form & Auth Forms)

**Contact Form:**
- Three fields: YOUR NAME (text input), EMAIL ADDRESS (email input), YOUR MESSAGE (textarea, multi-line)
- Label style: Inter, ALL CAPS, ~11–12px, wide tracking, `--secondary` gold color
- Input style: Full-width, `--input` background (`#EAE5D4` cream), `--border` border (same cream color, 1px), border-radius 12px, Inter body text, placeholder in gray-400 (`#9CA3AF`)
- Textarea: `resize: vertical`, min-height ~120–150px
- Submit button: "Send Message" — full-width deep teal CTA
- Form width: Left column of two-column layout, approximately 50% page width

**Auth Form:**
- EMAIL ADDRESS input + PASSWORD input
- Eye icon for password visibility toggle
- Labels: Inter ALL CAPS small with tracking
- Input fields: Bordered, rounded, full-width within ~420px centered container
- "Forgot your password?" link — underlined, small Inter text
- "Don't have an account? Sign up" — small text link inline
- "← Back to Home" — arrow link, centered below

### Accordions (Team Partner List)

- Three expandable team partner items
- Each item: Circular profile photo (left, ~52px diameter) + Name in Cormorant/Inter + Role title in Inter small + Chevron down icon (right)
- Separator: 1px `--border` line between items
- Background: White card container with subtle border/shadow
- Expand/collapse: Chevron rotates 180° on expand (standard accordion behavior)
- Single-expand vs multi-expand: Not confirmed but appears to be standard accordion allowing one open at a time
- Container: Centered, max-width ~840px, on white section background

### Horizontal Service Carousel

- Scroll behavior: `overflow-x: auto`, `scroll-snap-type: x mandatory`, each card `scroll-snap-align: center`
- Scrollbar hidden via `.scrollbar-hide` class
- Visible count: ~2–2.5 cards visible at once on desktop (based on card width ~560px and viewport ~1366px)
- Navigation: "Scroll right" arrow button at right edge
- No dots/indicators below carousel
- Card height: `min-h-[350px]` minimum

### Client Impact Story Carousel

- Pagination dots below: up to 7 client stories (7 dot buttons observed)
- Previous/Next arrow buttons in a small cluster (left of dots)
- Featured stories display one at a time with full content block

### Button States & Interactions

**Hover (inferred from CSS `--transition-smooth: all .3s cubic-bezier(.4, 0, .2, 1)`):**
- Smooth 300ms transition on all interactive elements
- Primary button likely lightens or adds shadow on hover
- Ghost/outline button likely fills with primary color on hover
- Nav links likely show underline or color shift

**Focus:**
- `--ring: 44 58% 50%` (gold) — focus rings render in gold, consistent with the gold accent color

**Loading:**
- CSS has `.animate-pulse` and `.animate-spin` defined — likely used for form submission states
- Typewriter cursor animation defined for AI chat

**Disabled:**
- `cursor: default` for disabled elements

### Size/Color Selector Behavior
- Not applicable — this is a consultancy, not a product retailer

### Mega Menu
- Not present — no dropdown or mega menu structure observed

### Announcement Bar
- Not present — not an e-commerce site

### Search Component
- Not observed anywhere in navigation or UI

### Accessibility Widget
- An AI chatbot button (`ZealotAI`) floats in the bottom-right corner — this doubles as a support/FAQ channel. It is NOT a traditional WCAG accessibility widget (like UserWay or AudioEye).
- No separate WCAG accessibility overlay/widget observed.
- `sr-only` class present in CSS, indicating some screen reader text is used.

### AI Chat Widget Specs

- **Floating button:** Bottom-right, approximately 52px diameter circle
- **Icon:** Zealot leaf/flame icon + "AI" text badge
- **On click:** Expands to a modal overlay card (~360px × ~560px) with:
  - Header: ZealotAI title + Zealot icon + "How can we help you today?" + refresh icon + close icon
  - Message area: White background, bot messages centered
  - Input bar: Full-width text input + send button (deep teal background, arrow icon)
  - Welcome message: "Welcome! I'm here to help you learn about Zealot's services."
  - Sub-prompt: "How can Zealot help you build something that lasts?"
- The chat widget has its own brand: "ZealotAI"

### Video Embed Behavior
- No video embeds observed on the site during this audit

### Animation & Motion Philosophy

Zealot uses **purposeful, restrained animation** — motion that guides rather than entertains:

1. **Entrance animations (`animate-fade-in`):** `opacity: 0 → 1, translateY(10px → 0)` over 300ms — content fades and rises gently into view. Applied to sections as they scroll into viewport (intersection observer likely).
2. **Typewriter animation** in the AI chat widget — sophisticated character-by-character text reveal with blinking cursor.
3. **Accordion expand/collapse:** Chevron rotation, content height transition.
4. **Carousel scroll:** Native scroll-snap, no JS animation.
5. **Message enter animation** for chat messages: `opacity → 1, translateY(8px → 0), scale(.98 → 1)` in 250ms.

**What is NOT animated:**
- Navigation links — static, no animated underlines or sliding effects
- Logo — static
- Background patterns — no parallax effects despite the hero photo background
- Hero text — not animated in (despite the large display type that would typically warrant reveal animation)
- Page transitions — none (SPA anchoring is instant scroll, not animated transitions)

The restraint in animation is intentional: it would be dissonant to have aggressive motion on a firm that communicates steadiness and gravitas.

---

## 6. Iconography

### Complete Icon Inventory

| Icon | Description | Usage Location | Context |
|---|---|---|---|
| User icon | Simplified person silhouette | Nav bar "Sign In" button | Left of "Sign In" text, ~16px |
| Sun icon | Solar/sun symbol | Nav bar theme toggle (light mode) | Toggle between light/dark |
| Moon icon | Crescent moon | Nav bar theme toggle (dark mode) | Indicates current dark mode |
| Chevron down | Simple downward-pointing chevron | Team page accordion items | Right edge of each partner row |
| Arrow down | Thin downward arrow/chevron | "SCROLL" indicator on hero | Below "SCROLL" text in hero section |
| Scroll right arrow | Right-pointing arrow/chevron | Service carousel | Right edge control for horizontal scroll |
| Previous/Next arrows | Left/right arrows | Client Impact story carousel | Navigation within testimonial carousel |
| External link arrow | Diagonal arrow | "Visit Ten Boom Coffee" link | After external link text, small icon |
| Eye icon | Show/hide password toggle | Auth page password field | Right side of password input |
| Service icons | Custom illustrated icons (each unique per service) | Services carousel cards | One icon per service type, ~48–64px square |
| Refresh/reset icon | Circular refresh arrow | AI chat widget header | Resets conversation |
| Close (×) icon | Standard × | AI chat widget header | Closes the chat window |
| Send icon | Arrow/paper-plane | AI chat widget input send button | Right side of chat input |
| Zealot leaf/flame icon | Abstracted botanical/flame mark | AI chat widget button + header | Sub-brand mark for ZealotAI product |
| Dot/circle bullets | Filled circles | Client story carousel dots | Pagination indicators (up to 7) |
| Bullet list dots | Standard list-disc | Leadership notable work list | Unordered list items |

### Icon Design Philosophy

Icons on zealot.company are deliberately **minimal and functional** — they serve navigation and interaction affordance purposes, not decorative ones. The service carousel uses what appear to be custom illustrated icons (distinct icons per service area — a chart/system icon for "Consulting & Strategy," a network icon for "Partnerships"), but these are small and subdued rather than illustrated focal points.

**Why icons are used sparingly:** The brand identity is built on typographic and photographic hierarchy. Icons would compete with the authority of the Cormorant Garamond display type and the editorial photography. By keeping icons small and peripheral, the design ensures type and image remain dominant.

### Icon Color Rules

- UI/functional icons (nav, chevrons, arrows): `--foreground` deep teal or `--muted-foreground`
- No icons appear in the brand's gold color except potentially on hover states
- Service card icons: appear to use the primary teal or a related tone
- AI advisor icon: warm gold-green (the botanical mark is the exception — color-branded)

### Icon Sizing

- Navigation icons (user, sun/moon): ~16–20px
- Chevron/arrow icons: ~12–16px
- Service card icons: ~48px (contained within icon wrapper)
- Chat widget icon: ~28–32px in the floating button

### Icons Deliberately NOT Used

- **Social media icons** — notably absent from both navigation and footer; LinkedIn, Instagram, X/Twitter, Facebook — none present. This is a striking absence that signals the firm is deliberately not building a public social media presence or driving social engagement. Peer-to-peer relationship is prioritized over broadcast.
- **Star/rating icons** — no testimonial rating stars; the firm uses prose stories rather than star ratings
- **Shopping/cart icons** — n/a
- **Hamburger menu icon** — not confirmed in screenshots (mobile not captured)
- **Map/location pin icons** — despite "Tennessee • Israel • Beyond" geographic anchoring, no location pin icons

---

## 7. Photography Style

### Product Photography
Not applicable — Zealot is a consultancy, not a product company. There are no "product" photographs in the traditional e-commerce sense.

### Hero Photography (Homepage Hero)

**Subject:** An aerial/street-level perspective of a main street in Franklin, Tennessee — specifically what appears to be Main Street in Franklin, shot at golden hour dusk. Warm amber sky, tree-lined streetscape, storefronts, American flags, traffic. A distinctly small-town-American, Southern heritage scene.

**Technical style:**
- **Angle:** Near-ground street-level perspective looking down the main street corridor
- **Lighting:** Golden hour/dusk — warm amber, orange, and deep teal sky tones that perfectly complement the brand's gold-and-teal palette. The photograph was either selected or retouched to match the brand colors.
- **Color temperature:** Very warm (3000–4000K equivalent)
- **Overlay:** The hero section uses a subtle dark overlay (likely `from-black/70` gradient) to ensure text legibility while preserving the photo's visual richness
- **Aspect ratio:** 16:9 or full-viewport-height crop, full-bleed

**Strategic intent:** This image immediately establishes geographic and cultural identity — Zealot is rooted in the American South, specifically Tennessee. It communicates: community, permanence, Main Street economics (local businesses, real places), and the warm human scale of the firm's values. It's a *place* photo, not an *abstract* photo — grounding an otherwise intangible consulting service in physical geography.

### Portrait Photography (Brett Henry)

**Subject:** Brett Henry, founder, photographed in an informal outdoor setting (appears to be a natural-light outdoor portrait)
**Style:**
- **Background:** Deep forest green/dark green foliage background, creating strong contrast with the subject
- **Lighting:** Soft natural light, slightly overcast or window-diffused, creating even skin tones without harsh shadows
- **Posing:** Relaxed, direct-to-camera gaze, slight smile — approachable authority, not corporate formality
- **Wardrobe:** Casual-professional (brown vest/jacket over casual shirt) — signals he's a builder/operator, not a boardroom executive
- **Crop:** Bust/three-quarter crop (shows from approximately waist up)
- **Aspect ratio:** Approximately 2:3 portrait orientation, displayed in a left-column layout

**Team partner photos (Joel Allen, Ryan Rogers, Peyton Henry):**
- Small circular headshots (~52px diameter in accordion)
- Black and white or desaturated treatment observed — creates visual consistency across different photographers/sources
- Professional but casual — same non-corporate register as Brett's portrait

### Office/Exterior Photography

**Subject:** Zealot office exterior — a building exterior shot, warm-toned, suggests a historic/heritage building in Tennessee
**Style:**
- Warm golden-hour-adjacent lighting
- Architecture with heritage/character (brick or traditional Southern commercial building)
- Used in the "WHO WE ARE" section alongside the three pillars content

### Photography Strategy & Art Direction

The photography direction follows a **terroir principle** — like a winery communicating its sense of place through every bottle, every photograph communicates Zealot's specific geographic and cultural rootedness. Tennessee, heritage architecture, golden-hour light, natural environments. No photography uses studio setups, abstract backgrounds, or generic stock photo aesthetics.

**Color harmony with brand:** The photography selection is coordinated with the brand palette — the golden-hour light in the hero photo mirrors the `--secondary` gold color. The deep green foliage in the Brett Henry portrait mirrors the `--accent` muted teal-green. This is not accidental. Either the photos were selected for chromatic harmony with the brand, or the brand palette was derived from the photography.

### Image Aspect Ratios by Context

| Context | Aspect Ratio |
|---|---|
| Hero full-bleed | 16:9 or viewport-height fill |
| Brett Henry portrait | ~2:3 (portrait) |
| Office exterior | ~4:3 or 3:2 (landscape) |
| Client/venture logos | ~1:1 (square) |
| Partner headshots | 1:1 (circular crop) |
| Client featured story image | ~1:1 or 4:5 (portrait) |

### Image Treatment Consistency

- No heavy filters applied (no Instagram-style color grading)
- Warm-tone preference throughout — cool blues and cold temperatures are avoided
- Subtle overlay gradients on hero image for text legibility (gradient from black/dark to transparent)
- No watermarks or attribution text visible
- Images hosted on the Zealot domain (`/assets/` path), not external CDNs

---

## 8. Brand Voice & Language Style

### Tone: Overall Personality

Zealot's voice occupies a distinctive and deliberate space: **the language of a faith-driven, conservative Southern gentleman who has also read Nassim Taleb and studied blockchain.** It is simultaneously rooted (in place, tradition, and values) and forward-looking (AI, systems architecture, decentralized finance). The voice is never ironic, never casual-tech-bro, never jargon-heavy for its own sake.

**10+ Sub-category Tone Analysis:**

1. **Foundational / Creedal Voice:** The language of deeply held conviction. Phrases like "Faith-Driven Leadership," "Conservative, Christian values guide every partnership," and "ventures that last" signal permanence and moral authority. This is not hedged corporate-speak — it's declarative.

2. **Builder's Voice:** Concrete, operational, systemic. "Building systems," "scalable frameworks," "transform chaos into clarity," "repeatable, scalable processes." The language of someone who actually builds things, not just advises.

3. **Relational / Friendship Voice:** "Foster Friendship," "meaningful partnerships," "cultivating meaningful relationships," "lasting impact," "connectors." The firm frames its value proposition around relationship quality, not transactional efficiency.

4. **Geographical Specificity Voice:** "Tennessee, Israel, and beyond" appears at least five times across the site. This geographic anchoring is unusual in consulting — it's a market-category-defining move that tells you exactly who Zealot is for and not for.

5. **Heritage / Legacy Voice:** "ventures that last," "courage and faith" (Ten Boom Coffee reference), "rooted in tradition" (Liberty Cigar), "world-class... blending heritage and innovation." The firm celebrates age, endurance, and things built to outlast their makers.

6. **Aspirational Clarity Voice:** "clarity, systems, and meaningful relationships," "execute with confidence," "clarity and strategic vision." Clarity is a recurring theme — it's positioned as the primary deliverable.

7. **Humble Authority Voice:** The firm doesn't boast of scale, revenue, or deal counts. It presents Brett Henry's accomplishments factually ("Co-founded Honest Coffee Roasters," "50+ owners, 100+ members") without superlatives. The confidence is quiet.

8. **Mission-Driven Business Voice:** Every venture and client is described through a mission or values lens first, then capabilities. Ten Boom Coffee is introduced as "inspired by the Ten Boom family's legacy of courage and faith" before discussing coffee quality. This mission-first framing is consistent and total.

9. **Educational/Systems Voice:** "Training teams and leaders to build repeatable, scalable processes," "strategic planning and seamless integration of AI tools." Positions the firm as a teacher and architect, not just an advisor.

10. **Anti-Excess Voice:** Liberty Cigar's description — "No hype. No shortcuts. Just cigars worthy of the name Liberty." — is the most concise expression of the brand's broader anti-hype stance. This three-sentence kicker could serve as brand manifesto for the whole firm.

11. **Theological / Purposive Voice:** "Jesus-centered marketplace network" (DECO DAO), "faith, innovation, and lasting community," "mission-driven," "integrity and purpose in all we do." Faith is not hidden or implicit — it's explicit and central.

### Language Patterns

**Recurring Structural Patterns with Examples:**

1. **The "Building / Scaling / Fostering" Triple:** The tagline and footer close with a three-part gerund structure: "Building systems, scaling ventures, fostering friendship." This pattern echoes throughout: "Building systems, scaling ventures, and cultivating meaningful partnerships." The gerund form (-ing) creates a sense of ongoing, active process — the work is never done.

2. **The "Mission + Method + Geography" Formula:** Almost every partner/client description follows: [cultural/spiritual mission] + [operational method] + [geographic/community impact]. Example: "A specialty coffee company inspired by the Ten Boom family's legacy of courage and faith [mission], focused on sourcing exceptional coffees [method] and sharing meaningful stories [community impact]."

3. **The "Rooted in / Built Around" Opening:** Several venture descriptions begin this way: "Rooted in tradition and respect for craftsmanship" (Liberty Cigar), "Built around a simple idea" (Liberty Cigar). This suggests a brief writing template for venture descriptions.

4. **The Italic Serif Emphasis Split:** In headings, the second or operative phrase receives italic Cormorant Garamond while the first is roman. "Foster *Friendship*", "Building ventures that *last*", "Our *expertise*", "Ventures we *believe in*" — the italicized word is always the emotionally loaded one, the word doing the most philosophical work.

5. **The Three-Bullet Credential Pattern:** Brett Henry's "Areas of Expertise" and "Notable Work" are presented as plain, unpretentious bullet lists. No puffery, no percentage claims, no "drove $X million in revenue." Just: "Co-Founder of DECO DAO (50+ owners, 100+ members)."

6. **The "Beyond" Escape Hatch:** "Tennessee, Israel, and beyond" uses "beyond" as a deliberate open-ended qualifier — it names two specific places (creating authenticity) and adds "beyond" (allowing global scope without overpromising).

### Heading Style Inventory by Page

**Homepage:**
- "STRATEGIC CONSULTANCY" — Inter ALL CAPS, label style, gold
- "Foster / Friendship" — Cormorant serif, ~120px, roman/italic split
- "WHO WE ARE" — Inter ALL CAPS label
- "Building ventures that last" — Cormorant, split italic on "last"
- "01 / 02 / 03" numbered subheadings with "Systems Building," "Faith-Driven Leadership," "Community Focus"
- "HOW WE HELP" — ALL CAPS Inter label
- "Our expertise" — Cormorant, italic on "expertise"
- "OUR PORTFOLIO" — ALL CAPS label
- "Ventures we believe in" — Cormorant, italic on "believe in"
- "OUR CLIENTS" — ALL CAPS label
- "Champions of purpose" — Cormorant, italic on "purpose"
- Section labels for clients: "AI-POWERED ACCOUNTING", "MUSIC & ENTERTAINMENT", "SUSTAINABLE AGRICULTURE"
- "CLIENT IMPACT" — ALL CAPS label
- "Stories of transformation" — Cormorant, italic on "transformation"
- "LEADERSHIP" — ALL CAPS label
- "Brett Henry" — split: "Brett" roman, "Henry" italic
- "FOUNDER & PRINCIPAL" — Inter ALL CAPS
- "NOTABLE WORK" / "AREAS OF EXPERTISE" — Inter ALL CAPS bold labels
- "GET IN TOUCH" — ALL CAPS label
- "Let's start a conversation" — Cormorant, italic on "conversation"

**Team page:**
- "Our Team" — Cormorant serif, italic on "Team"
- "Founder & Principal" — Cormorant, italic on "Principal"
- "Brett Henry" — serif display
- "Key Achievements" / "Areas of Expertise" — ALL CAPS style
- "Key Partners" — heading
- "Joel Allen, Creative Partner" / "Ryan Rogers, Strategic Partner" / "Peyton Henry, Operations & Sales Partner"

**Capitalization Rules:**
- Section identifier labels: ALWAYS ALL CAPS
- H2/H3 headings: Sentence case (only first word capitalized), with italic emphasis applied to second phrase
- Navigation links: Title case (first letter of each word)
- Body copy: Standard sentence case
- CTA buttons: Title case

### CTAs & Microcopy: Complete Inventory

**Homepage CTAs:**
- "Book a Consultation" — primary hero CTA, deep teal filled button
- "Explore Our Work" — secondary hero CTA, ghost/outline button
- "SCROLL" + chevron — scroll invitation, not clickable button, ALL CAPS Inter label

**Navigation CTAs:**
- "Book Consultation" — bordered pill button in nav, differentiated from plain nav links
- "Sign In" — nav item with user icon

**Footer CTA (implicit):**
- "hello@zealot.company" — email as CTA, no explicit button

**Contact Form CTAs:**
- "Send Message" — form submit button, primary teal
- No explicit "Cancel" or secondary form action

**Auth Page CTAs:**
- "Sign In" — primary full-width button
- "Forgot your password?" — text link, underlined
- "Don't have an account? Sign up" — inline text link
- "← Back to Home" — arrow text link, centered

**Sign Up Page CTAs:**
- "Sign Up" — primary full-width button
- "Didn't receive verification email?" — text link
- "Already have an account? Sign in" — text link
- "← Back to Home" — arrow text link

**Client Impact Section:**
- "Visit Ten Boom Coffee" — external link with arrow icon, not a button

**AI Chat Widget Microcopy:**
- "ZealotAI — How can we help you today?" — header prompt
- "Welcome! I'm here to help you learn about Zealot's services." — first bot message
- "How can Zealot help you build something that lasts?" — secondary prompt (echoes the brand tagline language)
- "Type your message..." — input placeholder

**Microcopy Tone Analysis:**
The microcopy maintains the brand voice with notable consistency. "How can Zealot help you build something that lasts?" in the AI chatbot mirrors the homepage's "Building ventures that last" — deliberate copy-harmony. Form placeholders ("Tell us about your project or inquiry...", "your@email.com") are functional and friendly without being informal. No exclamation points outside the chatbot.

---

## 9. Platform & Technical Notes

### Platform Identification

**Platform: Custom React/Vite SPA (Single Page Application)**

Evidence:
- The main JavaScript bundle is `https://www.zealot.company/assets/index-CIbfF3Fl.js` — a Vite-bundled production JavaScript file
- The CSS file is `https://www.zealot.company/assets/index-OnKuFvI2.css` — content-hashed Vite output
- TailwindCSS is the styling framework (evident from utility class patterns in CSS: `bg-primary`, `text-foreground`, `rounded-lg`, grid utilities)
- **ShadCN/UI** component library is likely in use — the CSS variable naming convention (`--background`, `--foreground`, `--primary`, `--radius`) matches exactly the ShadCN/UI design system, which is a React component library built on Radix UI primitives
- **Radix UI** component primitives are confirmed by CSS variable names: `--radix-navigation-menu-viewport-height`, `--radix-select-trigger-height` — these are Radix UI-specific variables
- React framework confirmed by the SPA routing behavior (`/team`, `/auth` routes without page reload)
- **Flock.js**: `https://www.zealot.company/~flock.js` appears in the source — this is the Flock platform/hosting script, suggesting the site may be built on or deployed via the **Flock** platform (a startup that offers website/SPA hosting)

**NOT Shopify, NOT WordPress, NOT Webflow, NOT Squarespace.** This is a fully custom-coded application.

### Theme Architecture

- Custom CSS variable system built on ShadCN/UI conventions
- TailwindCSS v3+ for utility classes
- Dual light/dark theme toggleable via `.dark` class on `<html>` element
- `--radius: 0.75rem` global border-radius token
- `--spacing-section: 12rem` and `--spacing-section-mobile: 6rem` custom spacing tokens
- `--font-sans` and `--font-serif` CSS variables explicitly defined
- `--gradient-primary`, `--gradient-gold`, `--gradient-hero` named gradient tokens
- `--shadow-elegant` and `--shadow-gold` named shadow tokens

### URL Structure Patterns

- `https://www.zealot.company/` — Homepage (full single-page app with anchor nav)
- `https://www.zealot.company/team` — Team page (only dedicated sub-route)
- `https://www.zealot.company/auth` — Authentication page (sign in / sign up)
- `https://www.zealot.company/#about` — Homepage About section anchor
- `https://www.zealot.company/#services` — Homepage Services anchor
- `https://www.zealot.company/#portfolio` — Homepage Portfolio anchor
- `https://www.zealot.company/#contact` — Homepage Contact anchor
- `/portfolio`, `/login`, and other common routes return 404 (no-match handling)

### Third-Party Integrations Identified

1. **Flock.js** (`https://www.zealot.company/~flock.js`) — Hosting/deployment platform integration
2. **Google Fonts or similar** — Inter and Cormorant Garamond are web fonts, likely loaded via Google Fonts CDN or self-hosted via the /assets/ folder
3. **AI Chat (ZealotAI)** — A custom AI chatbot integration; the branding suggests it's built internally or via a custom LLM integration rather than a third-party chat widget (no Intercom, Drift, or Zendesk signatures visible)
4. **Supabase or similar auth backend** — The sign-in/sign-up/forgot password flow suggests a backend auth service; the form's `/auth` routing and verification email flow is consistent with Supabase Auth patterns

### Page Performance Observations

- Single JS bundle (`index-CIbfF3Fl.js`) and single CSS bundle (`index-OnKuFvI2.css`) with content-hashed filenames indicate production Vite builds with long-term browser caching strategy
- Image assets are served from `/assets/` with content-hashed filenames (e.g., `brett-henry-CfmGsKPd.jpg`, `office-exterior-CujGWTBs.jpg`) — optimal for CDN caching
- `scroll-behavior: smooth` for anchor navigation
- Intersection Observer likely used for scroll-triggered fade-in animations

### SEO & Meta Title Pattern

Observed page title: `"Zealot | Consultancy | Foster Friendship"` — follows the format `[Brand] | [Category] | [Tagline]`. This is a clean, keyword-rich format that communicates brand, function, and positioning in one title.

### Legal & Compliance Pages

- **No Privacy Policy page observed** — not linked in footer
- **No Terms of Service page observed** — not linked in footer
- **No Cookie Notice/Banner** — none observed (unusual for a site with potential EU visitors)
- Copyright notice present: `© 2026 Zealot. Building systems, scaling ventures, fostering friendship.`

### Accessibility Features

- `sr-only` CSS class present — some elements have screen-reader-only text
- Semantic HTML likely used (landmark regions, heading hierarchy confirmed in DOM: `banner`, `heading` roles properly assigned)
- ARIA labels on navigation buttons (confirmed: "Scroll right", "Previous client", "Next client", "Go to client 1–7")
- `role="button"` present in CSS for interactive elements
- **No WCAG accessibility overlay widget** (no UserWay, AccessiBe, etc.)
- Form `required` attributes confirmed on all contact form fields
- `type="email"` on email inputs
- No explicit `alt` text failure observed — images have descriptive alt text (e.g., `"Brett Henry, Founder & Principal of Zealot"`, `"Zealot Office Exterior"`)

### Social Media Accounts

**None identified.** No social media links appear anywhere on the site — not in the navigation, footer, or contact section. This is a remarkably deliberate absence for a consulting firm in 2026. The business card-equivalent social signals (LinkedIn especially) that virtually all professional services firms display are completely absent. This either represents: (a) a deliberate brand statement that client relationships are built person-to-person, not via platforms, or (b) an early-stage site where social infrastructure hasn't been added yet.

The email `hello@zealot.company` on a custom `.company` TLD is the only direct communication channel listed.

---

## 10. Pages Browsed

1. **https://www.zealot.company/** — Homepage (full scroll through all 9 sections)
2. **https://www.zealot.company/** (scrolled: Section 1 — Hero) — Hero screenshot captured
3. **https://www.zealot.company/** (scrolled: Section 2 — WHO WE ARE + HOW WE HELP) — Services carousel captured
4. **https://www.zealot.company/** (scrolled: Section 3 — OUR PORTFOLIO) — Portfolio grid header captured
5. **https://www.zealot.company/** (scrolled: Section 5 — LEADERSHIP) — Brett Henry portrait and bio captured
6. **https://www.zealot.company/** (scrolled: Section 6 — GET IN TOUCH / Contact Form) — Form and footer captured
7. **https://www.zealot.company/team** — Team page (full scroll: hero, Brett Henry bio, Key Partners accordion)
8. **https://www.zealot.company/portfolio** — 404 Not Found (confirmed Portfolio is anchor-only, not a separate route)
9. **https://www.zealot.company/login** — 404 Not Found (confirmed /login is not a route)
10. **https://www.zealot.company/auth** — Auth / Sign In page (sign-in form, ZEALOT wordmark, form fields)
11. **https://www.zealot.company/auth** (Sign Up toggle) — Create Account page (sign-up form variant)
12. **https://www.zealot.company/** (dark mode) — Homepage in dark mode (theme toggle captured)
13. **https://www.zealot.company/** (dark mode, scrolled) — HOW WE HELP section in dark mode captured
14. **https://www.zealot.company/** (AI chat widget open) — ZealotAI chatbot interface captured and documented
15. **https://www.zealot.company/assets/index-OnKuFvI2.css** — Full CSS stylesheet extracted and analyzed for design tokens, color variables, typography variables, spacing, animations, and component styles

---

*Zealot Brand Standards Audit — Senior Design Analysis*
*Extracted and compiled: March 23, 2026*
*Method: Live browser traversal, DOM accessibility tree extraction, CSS file direct analysis, and visual screenshot documentation across 14 page states*
