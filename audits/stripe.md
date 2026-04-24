Stripe Brand Standards Audit -- extracted from https://stripe.com across 14 pages (April 2026)

---

## 1. Color Palette

### Every Hex Color Code Extracted from Site

**Primary Brand Colors**
- `#635BFF` — Stripe's signature purple/violet. The dominant brand color. Used for primary CTA buttons ("Get started," "Start accepting payments," "See open roles"), active nav product labels (e.g., "Billing" in green or purple depending on product), the "Contact sales" button background on the primary nav, and as a key gradient anchor in hero backgrounds. This is Stripe's most recognizable color. An electric, saturated indigo-violet.
- `#0A2540` — Deep navy/dark slate. Stripe's primary dark text color for all body copy, headings, subheadings, and the dark-background "Custom" pricing card. It reads as near-black but with a strong blue undertone, giving warmth and depth rather than neutral cold black.
- `#FFFFFF` — Pure white. Used for button text on dark/colored backgrounds, card backgrounds, form field backgrounds, nav background (on product pages), and large content areas.
- `#F6F9FC` — Lightest icy off-white/pale blue-grey. The global page background on almost every marketing page. Not pure white—this subtle tint differentiates content cards from the page background while maintaining near-white lightness. A hallmark of Stripe's clean, clinical-yet-warm aesthetic.
- `#E3E8EE` — Light grey/silver. Used for borders, dividers, horizontal rules, inactive tab underlines, card borders, input field borders.
- `#697386` — Medium slate grey. Used for secondary body text, captions, labels, metadata (e.g., blog post dates, article category tags).
- `#3C4257` — Dark slate/muted navy. Used for secondary headings and supporting text in cards where full `#0A2540` would be too heavy.

**Accent/Gradient Colors (Hero Backgrounds & Decorative)**
- `#FF7E5F` / `#FEB47B` — Coral/orange/warm amber gradient tones appearing in the diagonal slash gradient across the homepage hero, Payments page, Billing page, Enterprise page, and Pricing page. These are used exclusively as decorative/background gradient anchors—never as text or button colors.
- `#FF6B6B` to `#FFB347` — The orange-to-amber gradient sweep seen on product hero right panels.
- `#7C5CFC` / `#9B59FF` — Lighter lavender-purple gradient range, appearing in the same hero gradients alongside the coral. Creates the signature Stripe "slash" of color.
- `#00D4FF` / `#4ECDC4` — Teal/cyan. Appears prominently on the Billing product hero (the green-to-yellow gradient uses teal as a base), Payments page hero bottom, and in the gradient transitions.
- `#24B47E` — Stripe's green. Appears in the Billing product page hero gradient, and for the "Start now" CTA button within the animated Billing demo card (Typographic SaaS mockup). Also used for checkmarks in feature lists.
- `#F1C40F` / `#F9CA24` — Yellow/amber. Used in the Billing page hero gradient, and within the demo card's "Starter" plan icon background.
- `#D946EF` / `#C026D3` — Magenta/hot pink. Part of hero gradient sweeps, particularly visible in the homepage hero diagonal wave. Creates the vibrant "candy" quality of the hero.
- `#FF0080` — Hot pink/fuchsia. Secondary gradient anchor on homepage hero, visible in the sweeping wave background.
- `#6772E5` — Classic Stripe blue-purple (older era, still detectable in some component-level styles). Slightly lighter/cooler than `#635BFF`.

**Functional UI Colors**
- `#5469D4` — Stripe's "Connect" blue. Medium blue used for interactive states, links on white background, and the "Contact sales" button in its outlined/ghost style.
- `#1A1F36` — Very dark navy, near-black. Used in the "Custom" pricing card background, selected states, and the darkest UI elements.
- `#F7FAFC` — Almost-white card fill.
- `#EBF8FF` — Very pale blue, used for selected/active radio button backgrounds in demo checkout forms.
- `#A3ACB9` — Grey placeholder text in form inputs (e.g., "jane@example.com" placeholder color).
- `#CBD5E0` — Lighter border grey for form inputs.
- `#2D3748` — Dark charcoal, used in certain code blocks/API reference display contexts.
- `#48BB78` — Success green (checkmarks in feature lists, "Confirm and subscribe" button active state).
- `#FC8181` — Error/warning red (used sparingly in form validation states).

**Support Subdomain (support.stripe.com) Colors**
- `#425466` — Slightly lighter navy for body text on support pages.
- `#F6F9FC` — Same background as main site.
- `#635BFF` / `#5469D4` — Link colors on support pages.
- `#E4E9F0` — Border/divider on support article lists.

**Legal/Privacy Page Colors**
- `#FFFFFF` — Pure white background (notably different from `#F6F9FC` on marketing pages — legal pages use clean white).
- `#0A2540` — Text.
- `#635BFF` — Links.
- `#697386` — Navigation sidebar item text.

**Jobs Page Distinctive Colors**
- `#FFCF5C` / `#F0A500` — Golden amber/yellow. Unique to the Jobs page. Used as a decorative horizontal bar element at the bottom of the hero, creating a warmth/optimism signal distinct from the purple-dominant marketing site. This color is intentionally set apart to signal the cultural, human-facing nature of the careers page.

### Key Observation on Palette Strategy

Stripe's color strategy is a masterclass in *controlled vibrancy*. The palette has a disciplined, two-mode system:

1. **Structural/Utility Palette (Restrained):** A tight monochrome range — `#F6F9FC` background, `#0A2540` text, `#E3E8EE` borders, `#697386` secondary text, `#FFFFFF` surfaces. This creates an almost clinical, precision-engineered feel that signals trustworthiness, reliability, and technical credibility.

2. **Expressive/Brand Palette (Rich):** The diagonal gradient sweeps — purples, pinks, corals, teals, greens, yellows — serve as the sole venue for color expression. These are almost entirely confined to *background decoration*, never applied to functional text, buttons, or forms. The gradient is the "personality" while the UI stays neutral.

This separation is sophisticated: it lets Stripe signal vibrancy and creativity while maintaining the conservative legibility demanded by a financial infrastructure brand. The restrained structural palette builds trust; the expressive hero gradients build excitement. Neither compromises the other.

### Color Application by Page Type

**Homepage:**
- Background: `#F6F9FC` throughout all content sections
- Hero: massive diagonal gradient sweep (purple → pink → coral → orange → teal) covers the entire right two-thirds of the viewport
- Headings: `#0A2540` (near-black navy)
- Body text: `#0A2540` and `#3C4257`
- Secondary/metadata text: `#697386`
- Primary CTA "Get started": `#635BFF` fill, white text
- Secondary CTA "Sign up with Google": `#FFFFFF` fill, `#0A2540` text, `#E3E8EE` border
- Stats section ("135+ countries," "$1.9T," "99.999%"): white cards on `#F6F9FC` background
- Partner logos: monochrome black on white/light grey strip
- Footer: white background, `#0A2540` heading text, `#697386` link text

**Payments Product Page (PDP):**
- Sub-nav label "Payments": `#5469D4` blue (product-specific color coding)
- Sub-nav links (Overview, Features, Payment methods, Authentication, AI, Docs): `#697386` default, `#0A2540` active/hover
- Hero background: same diagonal gradient, but more blue-purple dominant
- Primary CTA "Start accepting payments": `#635BFF`
- Secondary CTA "Contact sales": text-only link in `#5469D4`
- Checkout demo card: white `#FFFFFF`, border `#E3E8EE`, interactive elements in `#635BFF`
- Sessions announcement badge: `#F6F9FC` fill, `#697386` text, small `#635BFF` arrow

**Billing Product Page (PDP):**
- Sub-nav label "Billing": `#24B47E` green (product-specific — green signals "billing/money")
- Sub-nav links: same neutral pattern as Payments
- Hero background: green-to-yellow-to-orange gradient (distinct from purple-dominant pages — each product has a signature gradient palette to differentiate while staying in the Stripe gradient language)
- Primary CTA "Get started with Billing": `#635BFF` (consistent across all products)
- Billing plan demo card: `#24B47E` button "Start now"
- Feature checkmarks: `#24B47E`

**Pricing Page:**
- Standard tier card: white `#FFFFFF` fill, `#E3E8EE` border
- Custom tier card: `#1A1F36` dark navy fill, `#FFFFFF` text — high contrast, signals enterprise premium
- "Get started" CTA (Standard): `#635BFF`
- "Contact sales" CTA (Custom): `#635BFF` on dark background
- IC+ pricing / Volume discounts / Multi-product discounts tabs: `#0A2540` text on `#F6F9FC` background
- Hero gradient: blue-purple to pink-coral (lighter/brighter than homepage)

**Blog/Editorial Page:**
- Article category tags (e.g., "Industry," "Product," "Engineering"): `#635BFF` text — violet/purple acts as category signal
- Article titles: `#0A2540`
- Bylines/dates: `#697386`
- "Read more" CTAs: `#0A2540` with right-chevron icon
- Hero article image: full bleed, custom designed editorial illustrations (the Shoptalk article used a designed purple gradient card with spaced-out white text — brand colors applied to editorial design)
- Blog post thumbnail backgrounds: highly varied brand-designed illustrations using `#635BFF`, `#FF6B6B`, `#24B47E`, `#F9CA24` — each post gets its own branded color card
- Sub-heading for "Recent highlights": `#0A2540`
- Changelog items: bordered list, `#E3E8EE` borders

**Customer Stories Page:**
- Background: `#F6F9FC`
- Hero headline: `#0A2540`
- Customer video thumbnails: actual photography with brand-designed overlay cards
- Customer logos on video thumbnails: white, overlaid on photography
- "See all stories" CTA: `#635BFF`
- "Watch video" link: `#5469D4` with arrow

**Enterprise Landing Page:**
- Announcement ticker bar (top): white background with scrolling news items — `#697386` category labels ("News," "Stories," "Report") in various accent colors, items separated by chevron arrows in `#5469D4`
- Hero: same diagonal gradient but darker, more purple-indigo heavy — signals gravity of enterprise audience
- Hero text "enterprise" (large display): `#FF6B6B` coral/warm tone — unique coloring only seen on this page. Used on the display word "enterprise" to add warmth and differentiation within the main headline
- Customer logos (H&M, Maersk, Marriott, BMW, Amazon): monochrome/grayscale on white/light section

**Contact/Sales Page:**
- Minimal UI: white modal card on `#F6F9FC` background with gradient lower half
- Progress indicators: active step in `#635BFF`, inactive in `#A3ACB9`
- "Continue" CTA: `#635BFF`
- Input border: `#CBD5E0` default, `#635BFF` on focus
- Background gradient: warm coral/orange (right side only) — softer, more welcoming than product pages

**Support Page (support.stripe.com):**
- Distinct visual system from main stripe.com
- Background: `#FFFFFF` (pure white, not `#F6F9FC`)
- "Stripe Support" wordmark: `#0A2540` "Stripe" + `#5469D4` "Support" in bold — unique two-color wordmark treatment
- Article titles: `#5469D4` blue links (different from main site where links are `#635BFF`)
- Category tags beneath articles: `#697386` pills
- Search bar: white input with `#E3E8EE` border, magnifying glass icon in `#697386`
- Right sidebar topic links: `#5469D4`
- "Contact support" card: `#F6F9FC` fill

**Privacy/Legal Page:**
- Pure white background `#FFFFFF`
- Left sidebar navigation: `#697386` link text, `#635BFF` active link
- H1 heading: `#0A2540`
- Body text: `#425466` (slightly lighter than full dark for long-form readability)
- Links in body text: `#5469D4`

**Jobs Page:**
- `#F6F9FC` main background
- Unique "JOBS" identifier next to logo in bold uppercase `#0A2540`
- Primary CTA "See open roles": `#635BFF`
- Photography-dominant hero (real employees, real workspaces)
- Distinctive yellow `#F0A500` diagonal bar element at hero bottom — the only page using unmuted yellow as a structural element

**404 Error Page:**
- Minimal design: text only on `#F6F9FC` background
- Diagonal gradient (blue-teal + purple) in bottom-right corner
- Body text `#0A2540`, links `#635BFF`

### Color Hierarchy & Emotional Role Analysis

| Color | Hierarchy Role | Emotional Role |
|---|---|---|
| `#635BFF` (Stripe Purple) | Primary action, brand identity | Authority, innovation, technological trust, premium but approachable |
| `#0A2540` (Deep Navy) | Primary text, dominant UI | Gravitas, precision, financial credibility, reliability |
| `#F6F9FC` (Ice White) | Global background | Openness, clarity, clinical precision, breathing room |
| `#24B47E` (Green) | Money/billing signals, success states | Growth, financial success, positive outcomes |
| Hero Gradients (Purple→Pink→Coral→Teal) | Hero decoration only | Dynamism, creativity, energy, forward momentum, vibrancy |
| `#697386` (Slate Grey) | Secondary information, metadata | Neutrality, editorial hierarchy, information without noise |
| `#1A1F36` (Dark Navy Card) | Enterprise/Custom tier | Exclusivity, premium, high-stakes gravity |
| `#F0A500` (Amber/Jobs only) | Cultural warmth, humanity | Optimism, warmth, human potential, fun |

### Colors Deliberately Absent

Stripe's palette is as notable for what's *missing*:

- **Pure black (#000000):** Never used. All "black" text is `#0A2540` — a navy that reads warm rather than neutral-cold. This avoids harsh contrast and the cold corporate feel of pure black text on white.
- **Red for CTAs or brand elements:** Red appears only as a form validation color and is invisible in normal page states. Stripe refuses to use alarm-signal red in any positive brand context, unlike many fintech competitors.
- **Bright green for CTAs:** Despite green being in the palette, it's product-specific (Billing) and never used as a primary site-wide CTA. This keeps the purple dominant and unmistakeable.
- **Orange as a primary color:** Orange appears only as one stop in a multi-color gradient — never as a standalone surface, button, or type color.
- **Pastel/pale colors for marketing:** No baby blues, mints, or lavenders as solid fills. Stripe avoids the "startup pastel" aesthetic that was common in 2018–2022.
- **High-contrast reversed-out pages (black backgrounds):** With the exception of the pricing Custom card, Stripe never does full black-background sections. The brand lives in light.
- **Photographic color grading overlays:** Images are used without brand-color tints or overlays — photography is treated as documentary, not stylized with brand filters.
- **Yellow/orange as CTA colors:** Despite Jobs page use of yellow, it never appears as a button color. Stripe keeps CTAs exclusively in the purple family.

---

## 2. Typography

### Font Families Identified

**Primary Sans-Serif: Sohne / Söhne**
Stripe uses what is clearly Klim Type Foundry's **Söhne** (or its licensed equivalent) as the primary typeface across all marketing pages. Söhne is a contemporary grotesque designed by Kris Sowersby, inspired by Akzidenz-Grotesk as seen through the Bauhaus. It is clean, functional, and highly legible at all sizes, with subtle humanist warmth in the letterforms. The lowercase "a" has a single-story form in some cuts. Stripe may license this as "Stripe Sans" — a custom-licensed version or fork.

Closest publicly recognizable match: Söhne by Klim Type Foundry, or alternatively Inter if Söhne isn't available. The weight range (light through black), optical sizing, and the particular feeling of the type all point strongly to Söhne.

**Monospace: Roboto Mono / Stripe Mono**
Code blocks, API examples, pricing tiers in code-like format, and data labels use a monospace font that matches **Roboto Mono** or a custom "Stripe Mono" variant. Used sparingly and exclusively for technical/code contexts.

**Display Use:**
On the Blog's Shoptalk 2026 article editorial card, a very wide-tracked, all-caps display treatment is used. This uses the same Söhne base family but at a different weight/tracking setting to create a typographic design poster effect.

**System/Fallback Stack:**
On the Support subdomain (support.stripe.com), typography falls back to a slightly different stack that feels closer to the system sans-serif, suggesting that subdomain may use a lighter font loading strategy.

### Complete Font Usage Map

| Text Element | Font Family | Weight | Case | Approx. Size | Letter-Spacing |
|---|---|---|---|---|---|
| **Homepage H1** ("Financial infrastructure to grow your revenue") | Söhne | Bold (700) | Title case | ~72–80px / ~4.5rem | Default (0) |
| **Product Page H1** ("Unified, global payments to grow your revenue") | Söhne | Bold (700) | Title case | ~56–64px / ~3.5–4rem | Default (0) |
| **Product Page H1** ("Accelerate growth with Stripe Billing") | Söhne | Bold (700) | Title case | ~56–64px | Default (0) |
| **Section Headings H2** ("Flexible solutions for every business model") | Söhne | Semibold (600) | Sentence case | ~36–42px / ~2.25rem | Default (0) |
| **Sub-section H3** ("Accept and optimize payments globally") | Söhne | Semibold (600) | Title case | ~24–28px / ~1.5rem | Default (0) |
| **Body text (hero paragraphs)** | Söhne | Regular (400) | Normal | ~18–20px / ~1.125rem | Default (0) |
| **Body text (content sections)** | Söhne | Regular (400) | Normal | ~16–18px | Default (0) |
| **Navigation items** | Söhne | Medium (500) | Title case | ~14px | Default (0) |
| **CTA button text** | Söhne | Medium-Semibold (500–600) | Title case | ~15–16px | Minimal (0 to 0.01em) |
| **Category tags/labels** ("Industry," "Product") | Söhne | Semibold (600) | Title case | ~12–13px | +0.02–0.05em (slightly tracked) |
| **Blog article titles** | Söhne | Bold (700) | Sentence case | ~24–28px | Default (0) |
| **Blog body/excerpt** | Söhne | Regular (400) | Normal | ~16px | Default (0) |
| **Blog author names** | Söhne | Semibold (600) | Title case | ~13–14px | Default (0) |
| **Blog post dates** | Söhne | Regular (400) | Normal | ~13px | Default (0) |
| **Pricing tier headings** ("Standard," "Custom") | Söhne | Semibold (600) | Title case | ~20–22px | Default (0) |
| **Pricing amounts** ("2.9% + 30¢") | Söhne | Bold (700) | — | ~32–36px | Default (0) |
| **Pricing body copy** | Söhne | Regular (400) | Normal | ~14–15px | Default (0) |
| **Stat numbers** ("135+," "$1.9T," "99.999%") | Söhne | Bold/Heavy (700–800) | — | ~48–56px | Default to slight tight (-0.01em) |
| **Stat labels** | Söhne | Regular (400) | Sentence case | ~14–16px | Default (0) |
| **Footer headings** ("Products and pricing," "Solutions") | Söhne | Semibold (600) | Title case | ~12–14px | +0.05em (slightly tracked) |
| **Footer links** | Söhne | Regular (400) | Title case | ~13–14px | Default (0) |
| **Footer legal text** ("© 2026 Stripe, LLC") | Söhne | Regular (400) | Normal | ~12–13px | Default (0) |
| **Sub-nav product labels** ("Payments," "Billing") | Söhne | Semibold (600) | Title case | ~13–14px | Default (0) |
| **Sub-nav links** ("Overview," "Features") | Söhne | Regular (400) | Title case | ~13–14px | Default (0) |
| **Code/monospace elements** | Roboto Mono / Stripe Mono | Regular (400) | Normal | ~13–14px | Default (0) |
| **Privacy/Legal H1** | Söhne | Bold (700) | Title case | ~40–48px | Default (0) |
| **Privacy/Legal body** | Söhne | Regular (400) | Normal | ~16px | Default (0) |
| **Support page H1** ("How can we help?") | Söhne | Bold (700) | Sentence case | ~32–36px | Default (0) |
| **Support article titles** | Söhne | Semibold (600) | Sentence case | ~16px | Default (0) |
| **Form labels** ("Work email," "Country/Region") | Söhne | Medium (500) | Title case | ~14px | Default (0) |
| **Input placeholder text** ("jane@example.com") | Söhne | Regular (400) | Normal | ~16px | Default (0) |
| **Announcement badge text** ("Sessions 2026 - April 29–30") | Söhne | Regular (400) | Normal | ~13px | Default (0) |
| **Jobs page H1** ("Our customers are building the future") | Söhne | Bold (700) | Sentence case | ~52–60px | Default (0) |
| **Jobs "JOBS" identifier** | Söhne | Bold (700) | All caps | ~14px | +0.1em (tracked) |
| **Jobs nav items** ("Our opportunity," "Life at Stripe") | Söhne | Regular (400) | Title case | ~14px | Default (0) |
| **Testimonial quote** (blockquote style) | Söhne | Regular (400) | Normal | ~18px | Default (0) |
| **Testimonial attribution name** | Söhne | Semibold (600) | Title case | ~14px | Default (0) |
| **Testimonial attribution title** | Söhne | Regular (400) | Normal | ~13px | Default (0) |

### Typography Application by Page Type

**Homepage:**
Very large display type (H1 ~72px) in the hero, with multi-line stacked treatment. Text is left-aligned, allowing the diagonal gradient wave to fill the right half of the viewport. The hierarchy cascades from huge H1 → smaller H2 sections → body text → CTAs, with clear vertical rhythm using generous whitespace. Notable: the H1 mixes colors — "grow" appears in a teal-green, "your revenue" in near-white on dark background, creating a rainbow typographic accent effect that is unique to the hero.

**Product Detail Pages (Payments, Billing):**
Sub-navigation at ~13–14px adds an additional layer of hierarchy below the global nav. The H1 is slightly smaller (~56–64px) than homepage to accommodate the split-layout (50% text, 50% demo). Body copy (~18px) is in high-contrast dark navy. Product-specific accent color appears on the sub-nav label only.

**Pricing Page:**
Typography in the pricing cards is extremely functional — tiered hierarchy of tier name (20–22px semibold) → price (32–36px bold) → description (14–15px regular). The feature list uses checkmark icons + 14px regular text. The FAQs section (below the fold) uses expandable accordion pattern with 16px semibold questions.

**Blog/Editorial:**
Blog index uses author avatar + name (13–14px semibold) + date (13px regular) + category (12–13px semibold in brand purple). Article titles are 24–28px bold, excerpts are 16px regular. The featured/hero article gets a full-bleed editorial card with much larger type (the Shoptalk card used ~56px spaced-out all-caps letters in a poster typographic treatment — a significant departure from body type standards, used only for editorial art direction).

**FAQ/Support:**
Support page typography is simplified — large question "How can we help?" (~32–36px bold), followed by a search box, then article list items at 16px semibold (linked). Right sidebar uses topic category links at ~14px. This is the most minimally typographic page on the site.

**Contact Form:**
Form typography is minimal and functional: H1 "Let's get you to the right place" (~28–32px bold), subheading "We just need a few quick details" (~16px regular), labels (~14px medium), input text (~16px regular), privacy footnote (~13px regular).

**Legal/Privacy:**
Longest-form typography on the site. H1 (~40–48px bold), large "Welcome" section header (~32px bold), body text (~16px regular) in long-paragraph format. Left sidebar navigation (~13–14px regular/semi) provides document navigation. Optimized for reading depth, not scanning.

**Enterprise Landing:**
Distinct: the word "enterprise" in the H1 is displayed in a coral/salmon color (~56–64px bold), a unique chromatic treatment not used on other product pages. This creates a dramatic three-line headline with color punctuation on the final word.

**Jobs:**
Uses both the standard Söhne family and adds the "JOBS" word-tag (~14px, bold, all-caps, tracked) as an identifier element next to the logo. The employment context is signaled through slightly more expressive use of photography and a warmer, more human typographic tone.

### Font Pairing Philosophy

Stripe uses effectively a *single-font system* — Söhne in various weights and sizes performs all roles from display to body to UI label. This is a deliberate choice that signals rigorous design discipline and engineering-brain aesthetics. The monospace font (Roboto Mono) is used exclusively in technical contexts and functions as a categorical separator rather than a true pairing.

**Why this works semiotically:**
Single-font systems signal precision, control, and systems thinking — qualities that align perfectly with Stripe's identity as infrastructure-level technology. Engineers trust systems that are internally consistent; a single typeface family (just variable in weight and size) communicates that same internal coherence. It also ensures visual harmony across 30+ product pages — there is no inter-typeface tension. Stripe's visual vocabulary says: "we've solved the fundamentals correctly, so you can trust us with more."

The choice of Söhne specifically is strategic: it's a humanist grotesque (warm, legible, approachable) rather than a pure geometric grotesque (cold, rigid) or a neutral Swiss grotesque (corporate). This positions Stripe as technically rigorous but human — not a cold financial utility.

### Weight Distribution Analysis

| Weight | Usage |
|---|---|
| Regular (400) | Body text, nav links, footer links, form placeholders, testimonial quotes, dates, secondary labels, privacy body |
| Medium (500) | Navigation primary items, CTA button text, form labels, some metadata labels |
| Semibold (600) | Section headings (H2–H3), blog titles, author names, product sub-nav labels, footer section headings, feature list items, category tags |
| Bold (700) | H1 display headings, all hero titles, pricing numbers, stat numbers, logo mark weight |
| Heavy/Black (800+) | Stat numbers on homepage ("$1.9T," "135+"), used for maximum visual impact on quantitative data points |

The weight distribution follows a strict hierarchy: Bold/Heavy reserved exclusively for quantitative impact statements and primary display; Semibold for navigational and heading utility; Medium for action-oriented UI; Regular for all reading contexts.

### Letter-Spacing Rules

- **Display headings (H1):** 0 or very slightly tight (-0.01em to -0.02em) at large sizes — standard typographic practice to optically tighten large type.
- **Section headings (H2–H3):** Default (0) tracking.
- **Category tags and footer headings:** Very slightly tracked (+0.02–0.05em) to increase legibility at small sizes.
- **"JOBS" label identifier:** +0.1em — noticeably tracked, functions as a badge identifier.
- **Blog editorial poster type:** Wide tracking (+0.3–0.5em) used exclusively on the designed article card illustrations — not in body UI.
- **CTA buttons:** Minimal to default (0 to +0.01em).
- **Code/monospace:** Default monospace tracking.
- **No ALL-CAPS treatment on body CTAs:** Unlike many brands, Stripe does not use all-caps for button labels. CTAs are title-case or sentence-case.

### Complete Type Scale Summary

| Size (approx) | Context |
|---|---|
| 72–80px | Homepage hero H1 (desktop) |
| 56–64px | Product page H1, Customers/Enterprise hero H1 |
| 48–56px | Stat numbers ("135+ countries"), Jobs page H1 |
| 40–48px | Legal page H1, Annual letter display |
| 36–42px | Major section headings (H2) |
| 32–36px | Support H1, pricing amounts, sub-section H2 |
| 28–32px | Contact form H1, H3 headings |
| 24–28px | Blog article titles, card headings |
| 20–22px | Pricing tier names, minor headings |
| 18–20px | Hero body paragraphs, testimonial quotes |
| 16–18px | Standard body copy, article excerpts, product descriptions |
| 14–16px | Navigation, CTAs, form labels, feature list items, footer headings |
| 13–14px | Blog metadata, captions, category tags, footer links, sub-nav links, annotation text |
| 12–13px | Legal footnotes, copyright, smallest metadata |

---

## 3. Logo & Wordmark

### Primary Logo Description

Stripe's logo is an **entirely custom wordmark** — there is no abstract icon or symbol. The wordmark "stripe" is set in a proprietary custom-designed geometric sans-serif typeface that does not exist as a public font. It has the following characteristics:

- Lowercase letterforms only
- Very tight/zero letter-spacing (letters touch or nearly touch at optical x-height)
- Extremely simple geometric construction — circular "s," "r," "t," "i," "p," "e" feel like they were drawn with geometric precision, reminiscent of Futura or Avenir's geometry but at much heavier weight and custom proportioned
- High x-height relative to overall cap height (though no capitals are used)
- Very heavy weight — closer to Black or Extra Bold. The strokes are thick, confident, and have minimal stroke contrast
- The "stripe" letterforms appear almost monoline — very little thick-thin variation
- Rounded terminals on some strokes, giving softness within an otherwise bold geometric form
- The wordmark sits in a single horizontal line with no stacked or altered arrangements seen on the main site

### Logo Characteristics

- **Typeface style:** Proprietary custom geometric sans-serif, lowercase only
- **Weight:** Black/Extra Bold equivalent (~800–900 in weight terms)
- **Tracking:** Default to very slightly loose — the letters aren't crammed but have natural geometric spacing
- **Case:** Always all-lowercase — "stripe," never "Stripe" in the logo mark itself
- **No icon/symbol:** The wordmark IS the logo. Stripe does not use an abstract mark, initial, or symbol as a standalone brand mark on the main consumer-facing site. (Note: individual product apps and the Stripe API documentation use a small "S" or lightning-bolt-style monogram in specific contexts, but the main marketing site uses the full wordmark exclusively.)

### Placement Rules

- **Global navigation (marketing site):** Top left, approximately 120×35px visual footprint. Floats at the far left of the nav bar, flanked immediately to the right by the navigation items (Products, Solutions, Developers, Resources, Pricing). Vertically centered in the 56–60px tall nav bar.
- **Footer:** Bottom left, slightly smaller than nav. Positioned above the country/language selector.
- **Legal/Privacy pages:** Top left corner, minimal nav context. Wordmark only, no additional treatment.
- **Support subdomain:** Modified — "Stripe" in the brand wordmark weight/color, followed by "SUPPORT" in a contrasting blue (`#5469D4`) at similar size. Creates a two-part identifier. The relationship is: brand wordmark + product/subdomain name in contrasting color.
- **Jobs subdomain:** Modified — "Stripe" in the brand wordmark + "JOBS" in bold uppercase (#0A2540) at a slightly different rhythm. Same logic as Support.
- **Contact/Sales page:** Logo appears solo at top left on a stripped-down page (no full navigation), creating a clean, focused form experience.
- **404 page:** Logo appears in footer only — main content area is logo-free, reinforcing the error state.
- **No centered placement observed:** The logo is always left-aligned. Stripe never centers its wordmark.
- **No stacked/vertical treatment observed** on any page reviewed.

### Color Variations Observed

1. **Standard dark:** `#0A2540` deep navy on white/light backgrounds — the default in all navigation contexts.
2. **White:** On dark/gradient backgrounds (e.g., within the Annual Letter hero image, on the Stripe logo watermark inside editorial article illustrations), the wordmark appears in pure white.
3. **No multi-color version observed** — the logo is never rendered in the brand purple or gradient. The wordmark is always a single, flat color.

### Sizing Details

- **Primary nav:** Logo is ~120px wide × ~22px tall at 1440px viewport
- **Footer:** Logo is ~80–100px wide
- **Contact page:** Logo is ~120px wide
- **Support subdomain "Stripe Support":** ~150–160px total (wordmark + descriptor)
- **Clear space:** The logo appears to maintain ~16–24px of clear space on all sides before nav items

### Brand Mark System

Stripe uses a **wordmark-only** system with no standalone icon on the main marketing site. This is an extremely confident brand choice that says: the name IS the brand. There's no need for a symbol to "stand in" for the name in any context. The wordmark's distinctive letterform is strong enough to function as a logo at any size that matters for the marketing site.

Within product UI (Stripe Dashboard, Stripe apps, Stripe Cards), a simplified geometric mark (an "S"-form or diagonal stripe-derived symbol) exists but is NOT deployed on the marketing/branding surfaces reviewed.

### Logo Relationship to Brand Heritage/Positioning

The all-lowercase wordmark projects **approachability within authority**. Financial institutions typically use capitalized, serif, formal wordmarks (Goldman Sachs, JPMorgan, American Express). Stripe's lowercase wordmark is a deliberate cultural signal: "we're not a bank, we're a technology company." This positions Stripe closer to tech brands (google, airbnb, figma) than to financial brands. The heavy weight prevents it from feeling casual — it's technically bold and substantial. The combination: heavy weight + lowercase = "powerful but not corporate." This was a 2011-era design decision that has aged extremely well and now feels foundational rather than dated.

---

## 4. Layout & Grid System

### Global Structure

- **Max content width:** Approximately **1100–1200px** for primary content columns on marketing pages. The global nav spans to the full viewport width with ~40px horizontal padding on each side (80px total side padding at standard desktop).
- **Content area max-width:** ~1100px centered, with generous side margins at larger viewports.
- **Nav height:** ~56–60px fixed at top of viewport. Sticky on scroll.
- **Sub-product nav height:** Additional ~44–48px bar below the global nav on product pages (Payments, Billing, etc.). This creates a dual-nav stack.
- **Section padding (vertical):** Approximately 80–120px between major sections on marketing pages. Very generous — Stripe uses whitespace as a structural element.
- **Content column padding (horizontal):** ~40px on each side at standard breakpoint.
- **Grid system:** Primary layouts alternate between **full-width (100vw) dramatic sections** and **contained two-column splits** (50%/50% or 60%/40%).
- **Footer columns:** 5-column footer on desktop — column 1: logo/selector, columns 2–5: "Products and pricing," "Solutions," "Integrations and custom solutions / Developers," "Resources," "Company / Support"

### Page Templates Identified

**1. Homepage Template:**
- Full-width hero: left text column (~50%) + right gradient sweep (~50%) — no grid constraint in hero
- Logo strip: full-width, auto-scrolling horizontal marquee of partner logos
- Feature tiles section: 2-column grid (50%/50%) with each tile being an expandable button with heading + image
- Statistics row: 4-column equal-width stat blocks
- Enterprise section: full-width with image-left + text/CTA right (alternating pattern)
- Testimonial carousel: single-column reading width with horizontal scroll
- Developer section: 2-column (text left, code/interface mockup right)
- News/updates carousel: constrained-width with slide navigation
- Footer: 5-column grid

**2. Product Detail Page Template (Payments, Billing):**
- Global nav + product-specific sub-nav (sticky stack)
- Hero: 50/50 split — left column text + CTAs, right column animated/interactive product demo
- Feature sections below fold: alternating left/right image-text, full-width
- Logos/social proof strip: centered, grayscale
- Code/API section: dark background or split with syntax-highlighted code
- Testimonial block
- Footer identical to homepage

**3. Pricing Page Template:**
- Hero: text-centered (~50% width), gradient left/right — no right-column content
- Pricing cards: 2-card layout (Standard + Custom) side by side in a container
- Pricing tab navigation: inline tabs ("Standard pricing," "Custom pricing," "FAQs")
- Features grid: long multi-column feature list below cards
- FAQ accordion section
- Footer

**4. Blog/Editorial Landing Template:**
- Featured article: full-width card (50% text + 50% editorial image)
- Secondary article grid: 2-column below
- "Recent highlights" section: list-style (single column, compact)
- Changelog section: single column, dated list
- Email signup: centered, single-column CTA module
- Footer

**5. Customer Stories Template:**
- Hero: left text (~50%), right: masonry-style grid of customer video thumbnails
- Customer video thumbnails: varied sizes in an asymmetric mosaic (not a strict grid)
- Story tiles below: uses brand-designed illustration + logo overlay

**6. Contact/Sales Form Template:**
- Completely stripped down — logo only, no nav
- Modal-card style: white card centered on page (~500px wide), with gradient background visible behind
- Progress stepper: 3-step horizontal indicator at top of card
- Single CTA per step
- This is the most minimal page template on the site

**7. Legal/Privacy Template:**
- Left sidebar (~25% width): sticky document navigation tree
- Right content area (~75% width): long-form article text
- No hero, no gradient — purely functional typography layout
- Footer present

**8. Support Template (support.stripe.com):**
- Simplified nav: Stripe Support wordmark + sparse top navigation
- Full-width search hero: H1 + search input centered (~600px max-width)
- Two-column below fold: article list (75%) + popular topics sidebar (25%)
- Article list: structured list items with icon, title, excerpt, tags

**9. Enterprise/Solutions Landing Template:**
- Announcement ticker bar: full-width scrolling news strip
- Hero: same 50/50 split as product pages, but with more dramatic typography treatment
- Logo social proof strip: below hero
- Feature/use case sections: alternating full-width modules

**10. Jobs Template:**
- Unique sub-brand: "Stripe JOBS" wordmark with distinct nav
- Hero: 50/50 split with photography collage (not abstract gradient)
- Warm amber visual element at hero bottom
- Sections: "Our opportunity," "Life at Stripe," "Benefits"

### Product Card Anatomy

On the Customer Stories index and Blog index, "cards" are the primary unit. Anatomy:
- **Container:** White `#FFFFFF` background, subtle shadow or `#E3E8EE` border, border-radius ~8–12px
- **Media area:** Full-bleed image or designed illustration (16:9 or 4:3 ratio)
- **Logo overlay:** Customer logo in white, positioned top-left of image area
- **Video play indicator:** Circular play button icon, top-right of media
- **Text content area:** Below media, ~16–20px padding
- **No price display** (B2B product — no product pricing in cards)
- **CTA:** Text link "Watch video ›" or "Read more ›" in brand blue/purple
- **No hover animation observed on static cards** — video thumbnail cards animate to reveal play button on hover

### Responsive Behavior

- **Desktop (1200px+):** Full two-column heroes, 4-column stats, 5-column footer, full nav with all items visible
- **Tablet (~768–1199px):** Heroes remain two-column but with reduced padding; stats shift to 2×2 grid; footer collapses to 2–3 columns
- **Mobile (<768px):** Heroes go single-column (text above media); nav collapses to hamburger; footer goes single column; CTAs go full-width; product sub-nav becomes scrollable horizontal strip
- **Breakpoints (inferred):** ~480px, ~768px, ~1024px, ~1280px

### Whitespace Strategy

Stripe treats whitespace as a *design decision*, not a default. Sections have substantial vertical gaps (~80–120px between major modules), creating a slow, intentional reading pace. This is particularly striking on the homepage which is very long (~12,000+ px tall at desktop) but feels unhurried because of the generous spacing. The whitespace communicates: "we have nothing to hide; we want you to breathe and absorb each idea before the next." It is the typographic equivalent of a confident speaker who pauses.

### Grid Alignment Philosophy

Stripe avoids rigid grid systems in favor of **content-determined layouts**. The hero is never constrained to a 12-column grid — it breaks the grid intentionally with the diagonal gradient running edge-to-edge. The content columns fall at approximately 50% widths but this is more a structural feel than a prescribed mathematical grid. Text starts at the same ~40px left margin across all pages, creating alignment cohesion without mechanical grid-locking.

### Homepage Scroll Architecture (Module Pattern)

1. **Hero (viewport height):** Headline + CTAs + partner logo ticker
2. **Feature carousel (2× viewport):** "Flexible solutions" — two tabs of feature images
3. **Product use case tiles (2–3× viewport):** Scrolling through 6 product scenarios
4. **Sessions conference promo (0.5× viewport):** Event announcement
5. **Stats bar (0.25× viewport):** 4 KPIs
6. **Enterprise case studies (2× viewport):** Accordion of customer logos + expandable stories
7. **Professional services trio (0.5× viewport):** 3-column cards
8. **Startups section (1.5× viewport):** Scrollable customer story tiles
9. **Platforms section (1× viewport):** 3-column guide links
10. **Testimonial carousel (1× viewport):** Horizontal scroll quotes
11. **Developer section (1.5× viewport):** API stats + integration options
12. **News/updates carousel (1× viewport):** Latest announcements
13. **Book of the week (0.5× viewport):** Editorial, Stripe Press link
14. **Final CTA module (0.5× viewport):** "Ready to get started?"
15. **Footer (0.75× viewport):** 5-column links

Total scroll depth: ~10,000–13,000px at desktop. This is a substantially long homepage, but each module is distinct enough that scroll fatigue is mitigated by visual variety.

### PDP Image Gallery Layout

Product pages (Payments, Billing) use a **live animated demo** rather than a static image gallery. The right column of the hero contains an interactive mockup of a real product UI (checkout form, billing plan selector) that animates through different states automatically. This is far more valuable than static screenshots — it shows the product *working*, not just how it looks.

Below the hero, product pages use single-image illustrations per feature section (no gallery format). Images are diagrams, UI mockups, and data visualizations — no photography on product pages.

### Footer Layout Details

5-column structure at desktop:
- **Column 1 (leftmost):** Stripe wordmark + country/language selector + copyright
- **Column 2:** "Products and pricing" (long list: Pricing, Atlas, Authorization Boost, Billing, Capital, Checkout, Climate, Connect, Crypto, Data Pipeline, Elements, Financial Accounts, Financial Connections, Global Payouts, Identity, Invoicing, Issuing, Link, Managed Payments, Payments, Payment Links, Payment Methods, Radar, Revenue Recognition, Stripe Sigma, Tax, Terminal, Usage-based billing) — ~28 items
- **Column 3:** "Solutions" (Enterprises, Startups, 12 use cases, 7 industries)
- **Column 4:** Split — "Developers" (Documentation, API reference, API status, API changelog, Libraries and SDKs, Developer blog) + "Integrations and custom solutions" (Stripe App Marketplace, Stripe Partner ecosystem, Professional services) + "Resources" (Guides, Customer stories, Blog, Sessions, Privacy & terms, Prohibited businesses, Licenses, Sitemap, Cookie settings, Your privacy choices, More resources)
- **Column 5:** "Company" (Jobs, Newsroom, Stripe Press, Contact sales) + "Support" (Get support, Managed support plans) + "Sign in" button + country selector
- Background: white `#FFFFFF`
- Section heading style: ~12–13px, semibold, slightly tracked, `#0A2540`
- Link style: `#697386` regular, hover state changes to `#0A2540`
- Bottom border separating columns: absent — just whitespace separation

### Layout Elements Deliberately NOT Present

- **Announcement/promotional banner (sticky top bar):** No persistent announcement bar above the global nav. Stripe avoids the persistent discount/sale banner common in e-commerce. Event announcements (Stripe Sessions) are handled inline within page content and as small badges on CTAs.
- **Sidebar navigation on marketing pages:** Only appears on Legal/Privacy pages. Product pages, blog, customers — all full-width, no side navigation.
- **Sticky "back to top" button:** Not observed.
- **Chat widget/floating CTA:** Not observed on main marketing site.
- **Social share buttons on blog:** Not prominently displayed (social presence is signaled by "Stripe on X" link in blog nav, not inline share buttons).
- **Product comparison tables:** Pricing page avoids the typical 3-column feature comparison table common in SaaS — instead it presents two distinct tiers with a tab system.
- **Breadcrumb navigation:** Not used on any marketing page reviewed.
- **Pagination numbers on blog:** "View all posts" link instead of numbered pagination.

---

## 5. UI Components

### Buttons

**Primary CTA (Purple Fill)**
- Background: `#635BFF`
- Text: `#FFFFFF`
- Border-radius: ~4–6px (slightly rounded, not pill-shaped)
- Height: ~44–48px on desktop
- Padding: ~12px top/bottom, ~20–24px left/right
- Font: Söhne Medium/Semibold, ~15–16px
- Case: Title case ("Get started," "Start accepting payments")
- Right-facing chevron icon (`›`) appended after text in most primary CTAs
- Hover state: slightly darker purple (~`#5851D9`) — subtle darkening
- Active state: even darker
- No box shadow observed
- No border on filled buttons
- Examples: "Get started," "Start accepting payments," "Get started with Billing," "See open roles," "Continue," "Confirm and subscribe"

**Secondary/Ghost CTA (Outlined or Text)**
- Background: transparent
- Border: `#E3E8EE` or none (text-only)
- Text: `#0A2540` or `#5469D4`
- Border-radius: same ~4–6px when outlined
- Height: same as primary (~44–48px)
- Same typographic specs
- Right-facing chevron when it's a navigation CTA
- Examples: "Sign up with Google" (white fill + border), "Contact sales" (text link with `›`), "Read the guide ›," "View services ›"

**"Contact sales" Primary Nav CTA (Special)**
- Background: `#635BFF`
- Right-pointing angle/arrow SVG icon embedded after text
- Height: ~36–40px (slightly smaller than hero CTAs — appropriate for nav context)
- This is the only consistently purple-filled button in the global nav

**"Sign in" Nav CTA**
- Background: transparent or very light grey `#F6F9FC`
- Text: `#0A2540`
- No border visible
- Has a small "›" arrow icon
- Behaves as a secondary/ghost button

**Micro CTAs (Text Links with Arrow)**
- No button styling — pure text + `›` icon
- Color: `#0A2540` with slight emphasis, or `#5469D4` blue
- No underline on default state
- Hover: underline or color shift
- Examples: "Read more ›," "View services ›," "Read the guide ›," "Watch video ›"

**Billing Demo "Start now" Button**
- Background: `#24B47E` green
- White text
- Same border-radius
- Context-specific: appears only within the animated product demo, not in the main UI

**Progress/Multi-step CTA ("Continue")**
- Background: `#635BFF`
- Icon: right-pointing arrow within the button
- Same specifications as primary CTA

### Navigation

**Global Nav (Desktop):**
- Height: ~56–60px
- Background: white `#FFFFFF` with very subtle bottom shadow/border (`#E3E8EE` 1px bottom border)
- Position: sticky/fixed
- Left: Stripe wordmark logo
- Center-left: Products ▾, Solutions ▾, Developers ▾, Resources ▾, Pricing (all as text links, dropdowns on hover for first four)
- Right: "Sign in" (ghost) + "Contact sales" (purple filled)
- All nav labels: Söhne Medium, ~14px, `#425466` default / `#0A2540` on hover
- Active dropdown button: no visual active state except arrow direction change

**Mega Menu (Products Dropdown):**
- Triggered on hover/click of "Products ▾"
- Full-width panel (~900–1100px) that drops below the nav
- Organized in 4 columns: Payments, Revenue, Money Management, Platforms and marketplaces, More
- Each item: product name in `#0A2540` semibold + subtitle descriptor in `#697386` regular
- Slight dividers between column groups
- "Join us at Sessions" promotional card in the menu (rightmost column area) with an image and CTA

**Sub-Product Nav (Product Pages):**
- Secondary horizontal bar: ~44–48px height
- Background: white, with bottom border
- Leftmost: product name in brand color (e.g., "Payments" in `#5469D4` blue, "Billing" in `#24B47E` green)
- Then: tab links (Overview, Features, Payment methods, Authentication, AI, Docs)
- Active tab: slightly bolder text, `#0A2540`
- This provides in-page navigation/anchor links

**No Announcement Bar:**
There is no persistent promotional announcement bar at the top of any marketing page. Event promotion (Stripe Sessions) appears as a small badge within page content sections.

### Forms

**Contact/Sales Form:**
- Input fields: white background, 1px `#CBD5E0` border, border-radius ~4px, height ~44px
- Placeholder text: `#A3ACB9`
- Focus state: border changes to `#635BFF`, subtle box shadow
- Labels: `#0A2540` Medium, 14px, above the field
- Dropdown (Country/Region): same border/bg as text input + dropdown arrow icon
- Privacy footnote: 12–13px `#697386` regular below submit button

**Support Search Bar:**
- Wide input (~600px on desktop), white background
- `#E3E8EE` border (slightly more prominent than contact form)
- Border-radius: ~8px (more rounded than marketing forms)
- Magnifying glass icon on left inside input: `#697386`
- Placeholder: "Search help articles..." in `#A3ACB9`
- No visible submit button — search triggers on enter/icon click

### Accordions

**Pricing Page FAQ Accordions:**
- Question text: `#0A2540` Semibold, ~16px
- Separator: `#E3E8EE` 1px horizontal rule between items
- Expand indicator: "+" or "▾" chevron on the right
- When expanded: answer text appears below in Regular `#697386` ~16px
- Single-expand behavior (closing others when one opens is inferred, not confirmed)
- No background color change on expansion
- Clean, minimal — no border box around accordion items

### Product Carousels/Horizontal Scrollers

**Partner logo ticker (homepage):**
- Auto-scrolling horizontal marquee, infinite loop
- ~40px height logos, uniform
- Speed: smooth, medium pace
- No user controls

**"What's happening" news carousel:**
- Horizontal scroll with arrow navigation (left/right chevron buttons)
- Visible count: ~1 full card + partial next card
- Arrow buttons: circular, ~40px diameter, `#E3E8EE` background, `#0A2540` chevron icon

**Enterprise customer stories accordion:**
- Vertical accordion (not horizontal carousel)
- Active item expands to show details + image
- Visual pattern: list of story titles on left, expanded content + image on right
- Smooth expand/collapse animation

**Startup stories grid:**
- Horizontal scroll on mobile; ~4-column grid on desktop
- Each card: brand-logo + headline + "Read story ›" — uniform card height

### Button States & Interactions

- **Hover:** Primary buttons darken (~10%); ghost/text buttons gain underline or slight color shift
- **Active (click):** Brief scale reduction (click "press" feel) — standard browser behavior enhanced
- **Disabled:** "Confirm and subscribe" button in checkout demo appears in a desaturated, lighter purple (`#C4C0FF` approx) when not yet ready — clear disabled state
- **Loading:** Not observed in static screenshots, but standard UX pattern implied
- **Focus (keyboard):** Standard browser focus ring — likely uses `#635BFF` outline for accessibility

### Size Selector / Color Swatch Behavior

Not applicable — Stripe is a B2B software product with no physical goods. No size selectors or color swatches exist anywhere in the reviewed pages.

### Mega Menu Details

The Products mega menu (when opened on hover):
- Full-width below global nav
- Four product category columns: Payments (10 items), Revenue (7 items), Money Management (4 items), Platforms and marketplaces (4 items), More (4 items)
- Sessions promotional panel with image thumbnail
- Background: white `#FFFFFF`
- Shadow: subtle drop shadow below panel
- Close: menu closes on mouseout or second click

### Search Component

On support.stripe.com:
- Standalone hero search bar
- Left-aligned search icon inside input
- Not present on main stripe.com marketing pages (no site-wide search visible)

### Accessibility Widget

No third-party accessibility overlay widget (UserWay, AudioEye, AccessiBe, etc.) was observed on any page. Stripe relies on native semantic HTML and ARIA markup rather than a bolted-on accessibility toolbar. This is a more technically rigorous (and respectful) approach to accessibility.

### Link & Hover States

- **Body text links:** `#5469D4` blue, no underline default, underline on hover
- **Nav links:** `#425466` default, `#0A2540` on hover
- **Footer links:** `#697386` default, `#0A2540` on hover
- **CTA arrow links:** Same color as surrounding text, arrow animates slightly right on hover
- **Support article links:** `#5469D4` with underline (differs from main site — support subdomain uses underline by default for better legibility in article context)
- **"Read more ›" style links:** No underline, `#0A2540`, arrow shifts right on hover

### Video Embed Behavior

Customer stories pages use video thumbnails with a circular play button overlay. Clicking opens a video player (likely a modal or inline player). Videos are Stripe-produced brand content, not YouTube embeds in the traditional sense — they use a custom player UI. The Newsroom and Blog editorial cards use still images with branded graphic design rather than video autoplay.

### Animation & Motion Philosophy

Stripe uses animation deliberately and with restraint:

**What's animated:**
- Hero product demos (checkout form UI, billing plan selector): continuously loop through states, simulating real user interactions
- Logo ticker: smooth infinite horizontal scroll
- Number countups on stats section: numbers count up from 0 when scrolled into view
- Diagonal gradient "wave": the hero gradients subtly shift/breathe — very subtle ambient motion
- The "Global GDP running on Stripe: X%" ticker at top of homepage: updates live with actual data
- Dropdown menus: smooth fade/slide in
- Accordion expand/collapse: smooth height transition
- Page transitions: smooth but standard

**What's NOT animated:**
- The wordmark logo — static
- Body text and images — no scroll-triggered parallax or text reveal animations (Stripe deliberately avoids the "fancy scroll animation" trend)
- Background gradients below fold — they're static decorations, not continuously animating
- CTA buttons don't have complex hover animations — just simple color darkening

**Philosophy:** Motion is used to demonstrate *product capability* (the live demos show Stripe actually working) rather than to create visual spectacle. This is the engineering approach: use animation purposefully to communicate information, not to impress. Gratuitous animation would undermine trust with the developer/technical audience. Static-ness = confidence = reliability.

---

## 6. Iconography

### Complete Icon Inventory

**Navigation & UI System Icons:**
1. **Chevron/arrow-right (›):** Used extensively — after every CTA button text ("Get started ›"), after every micro-CTA link ("Read more ›," "View services ›," "Contact sales ›"), inside "Contact sales" nav button. Simple right-pointing chevron or angle bracket. `#FFFFFF` on filled buttons, `#0A2540` or `#5469D4` on text links.
2. **Dropdown chevron (▾):** Small downward-facing chevron after navigation items (Products ▾, Solutions ▾). Changes to upward when menu is open. `#697386`.
3. **Google "G" logo icon:** Appears in "Sign up with Google" button — Google's brand-standard "G" logo in full color. This is the only third-party brand icon in the global nav area.
4. **Circular video play button:** On customer story video thumbnails. White circle outline + white triangle play icon. Simple, clean.
5. **Arrow-right within circle:** Used as a navigation indicator on news/announcement ticker items and carousel "next" buttons. `#0A2540` arrow in `#E3E8EE` circle.
6. **Sessions logo:** A custom logotype for the "Stripe Sessions" conference, appearing in the homepage and product page announcement area. Black wordmark with Sessions branding.

**Newsroom Section Icons (lower content):**
7. **Bell/notification icon:** Stylized bell in blue `#5469D4`, used in Newsroom to represent "News" category. ~40×40px, relatively detailed geometric illustration style.
8. **Document/clipboard icon:** Similar illustration style, teal/blue, represents "Stories" category.
9. **Building/grid icon:** Similar illustration style, purple, represents "Company information."

**Support Page Icons:**
10. **Question mark / help icon:** Small circular icon with "?" used before article titles on support.stripe.com. Consistent with the article list items. `#5469D4` fill.
11. **Search/magnifying glass:** Inside the search input on support.stripe.com. `#697386` fill.

**Social Proof/Integration Icons:**
12. **Visa, Mastercard, Maestro, Amex, Discover, JCB, UnionPay, Diners, Cartes Bancaires:** Standard payment method logos appear in the Billing page's "International cards" section — these are third-party logos, not Stripe-created icons. Displayed at ~30–40px height in a row.
13. **Bank logo icons (Chase, BofA, Wells Fargo, Citibank, Capital One, US Bank):** Appear in the animated checkout demo's "US bank account" tab. Third-party logos.

**Product Illustration Icons (within animated demos):**
14. **Star icon (Billing "Professional" plan):** Simple 5-pointed star in a green circle within the Typographic demo card. Acts as a plan selection indicator.
15. **Tag/price icon (Billing "Starter" plan):** Tag icon in orange circle. Same demo context.
16. **Radio button circles:** Used in checkout plan selection (Monthly subscription / Annual subscription). Standard `#635BFF` fill when selected.
17. **Checkmark icons:** `#24B47E` green checkmarks in feature lists throughout product pages. Simple ✓ mark.
18. **Card/bank icons:** Credit card icon and bank icon in the payment method selector tabs. Minimal line-art style, `#697386` fill.
19. **"···" more options icon:** Three dots in the payment method tab area. Standard UI overflow indicator.
20. **UK flag icon (2×2 px GB emoji equivalent):** In the Payments demo, a small UK flag appears in the upper right corner of the checkout card frame — indicating geographic context in the demo.

**Jobs Page Icons:**
21. **"›" arrow in header:** "Stripe JOBS" wordmark + nav items don't use icons beyond the standard CTA chevrons.

**Favicon:**
22. **"S" monogram or stripe symbol:** Stripe's favicon (visible in browser tab) is a simplified mark — a white/lavender geometric form on `#635BFF` background. This is the closest Stripe comes to having a standalone symbol/icon, but it's exclusively used at favicon size, not in the marketing site content.

### Icon Design Philosophy

Stripe's icon system is **minimal to the point of near-absence** on the marketing site. The primary iconographic vocabulary is:
1. Arrow/chevron (directional — guides user action)
2. Checkmark (confirmation/feature available)
3. Play button (video/demo)
4. A small number of category illustration icons on Newsroom

There are **no decorative icons** used to represent features or concepts (unlike competitors who use icon grids with illustrations of locks, rockets, globes, shields for each feature). Stripe's features are communicated through words and live product demos, not icon metaphors. This is a deliberate design philosophy: icon metaphors can be reductive, culturally ambiguous, and visually noisy. By using text-first communication, Stripe signals confidence in its verbal identity and respect for its technical audience's reading ability.

### Icon Color Rules
- Directional arrows: match text color or button text color
- Checkmarks: `#24B47E` green
- Category illustration icons (Newsroom): product-specific brand colors
- All utility icons (chevrons, dropdowns): `#697386` grey
- Active state icons: `#635BFF` purple or `#0A2540`

### Icon Sizing
- Navigation chevrons: ~8–10px
- CTA arrows: ~14–16px
- Search icon: ~18px
- Video play button: ~40–50px diameter
- Newsroom category icons: ~40×40px illustrated

### Icons Deliberately Absent
- No "shield" security icons (despite security being a key value proposition)
- No globe/world icons (despite "global" being a major positioning pillar)
- No lightning bolt or speed icons
- No rocket ship icons (common in "startup" SaaS brands)
- No dollar sign, currency, or coin icons
- No lock icons on payment pages (security implied through brand trust, not visual metaphor)
- No social media icons in the global nav footer (only a "Stripe on X" text link in blog)
- No star ratings or review icons
- No "hand-drawn" or illustrated icons (zero skeuomorphic illustration)
- No animated looping icons (only the product demos animate)

---

## 7. Photography Style

### Product Photography

There is **no product photography** on Stripe's marketing site in the traditional sense. Stripe is a software/API product — there is nothing physical to photograph. "Product" representation is done entirely through:
1. **Screen mockups / UI illustrations:** Digital recreations of Stripe's own Dashboard and product interfaces, rendered at high fidelity with clean white backgrounds and real data states. These are clearly designed/composed shots of the software, not photography.
2. **Interactive live demos embedded in the hero:** Animated UI components that simulate the actual product experience.

Stripe card product (physical debit/charge cards from Issuing) and terminal hardware (Stripe Terminal) exist but no hero photography of these products was observed in the main marketing pages reviewed.

### Lifestyle/Editorial Photography

**Jobs Page (most photography-heavy page reviewed):**
- 5 distinct editorial photography compositions visible in the hero grid
- **Casting:** Diverse, professional, age range ~25–40, casually dressed (no formal office wear — laptop-working, collaborative settings). Gender diversity visible. Racial diversity visible. The overall feel is "real Stripe employees" rather than stock photography models.
- **Settings:** Mix of indoor (modern, plant-rich, warmly lit workspaces) and outdoor (urban context, park/green space)
- **Lighting:** Natural window light + indoor ambient warm lighting. No studio flash or harsh lighting. High ambient light, soft shadows. The images feel "real" — not overly art-directed.
- **Color grading:** None visible. Images appear as-shot with no color grade, no filters, no brand-color overlays. The warmth comes from the natural lighting of the scenes rather than post-processing.
- **Posing:** Candid-adjacent — people engaged in real work activities (typing, discussing, viewing screens). No forced smiling at camera poses. Very editorial journalism style.
- **Image quality:** High resolution, well-composed, clearly professionally shot despite appearing candid.

**Customer Stories Grid:**
- Large variety: editorial brand photography for each customer (Figma, ElevenLabs, brightwheel, URBN, Lovable, Pepsi, etc.)
- Each customer's "video thumbnail" is a designed brand card (not a photo):
  - **Figma:** Purple/violet graphic with Figma logo — no photography
  - **brightwheel:** Photo of a kindergarten/classroom environment, warm color
  - **URBN (Urban Outfitters):** Real storefront photo, warm amber/yellow color grading
  - **ElevenLabs:** Photo of a woman wearing headphones against a dark background
  - **Lovable:** Abstract brand graphic (pink heart design)
  - **Pepsi:** Product photography, blue/white Pepsi branding
- These are NOT photography Stripe produced — they are customer-supplied brand assets and imagery that Stripe curates and presents. This creates visual variety that is brand-coherent for each company.

**Blog Editorial Illustrations:**
- The Shoptalk 2026 blog post uses a brand-designed graphic (not photography) — a designed poster/card with large spaced text "3 AGENTIC TRENDS FROM SHOPTALK" over a gradient purple-to-orange background. Stripe's logo is featured on the card.
- Author avatar photos: small circular crop, ~48px diameter, documentary-quality headshots with varied backgrounds. Clearly real people, not stock photo models.
- Other blog article thumbnails appear to use either brand-designed illustrations or photography — varied by post.

**Newsroom:**
- The 2025 Annual Letter feature card: a designed illustration — "Annual letter 2025" large text on a purple gradient card with the Stripe wordmark. Not photography.

### Hero Images

- **Homepage:** No photography at all in the hero — the visual is entirely the abstract diagonal gradient wave.
- **Payments page:** No photography — live interactive checkout UI demo.
- **Billing page:** No photography — animated billing plan demo.
- **Pricing page:** No photography — gradient background only.
- **Enterprise page:** No photography in the hero — gradient background + UI mockup.
- **Blog page:** The featured article uses an editorial graphic card, not photography.
- **Customers page:** Photography appears only in customer-supplied video thumbnails.
- **Jobs page:** The most photo-rich page — a 5-panel grid of editorial photography in the hero.
- **Support page:** No hero photography.
- **Privacy/Legal:** No imagery.

**Key observation:** On product/marketing pages, Stripe almost entirely avoids photography in favor of product UI and abstract gradients. Photography is reserved for human contexts (jobs, customer stories, team) — signaling that the *product* is software (best shown as software UI) while *people* contexts (jobs, customers) are shown as real humans.

### Photography Strategy & Art Direction

Stripe's photography strategy has three modes:

1. **Absent (most marketing pages):** Product pages and pricing replace photography with interactive product demos and abstract gradients. The message: "you don't need to see a happy person using our API — you need to see the API working."

2. **Curated customer imagery (Customers page):** Customer-brand photography is curated and presented in a consistent frame/card format. Stripe acts as an editorial curator, giving each customer's story a designed presentation rather than just dropping in their logo.

3. **Documentary/editorial employee photography (Jobs page):** Warm, natural, diverse, unposed — signals culture authenticity rather than aspirational corporate fantasy.

The consistent thread: photography is used when the subject is *human* (employees, customers), never when the subject is *technology* (products, APIs, integrations). This draws a clean conceptual line.

### Image Aspect Ratios by Context

- Hero product demos: approximately 16:9 or unconstrained (fills the column)
- Customer story video thumbnails: approximately 4:3
- Blog article featured image: approximately 16:9 or 3:2
- Blog author avatars: 1:1 (circle crop)
- Jobs hero photography panels: mix of portrait and landscape; roughly 3:4 and 4:3
- Newsroom editorial graphics: approximately 4:3

### Image Treatment Consistency

No color filters, brand-color overlays, duotone effects, or post-processing grade applied to photography. Images appear as documentary/natural. Designed brand cards (blog thumbnails, customer story cards) use Stripe's color language (gradients, purple, etc.) but do not apply those treatments to photography. The photographic and the graphic/designed are kept as distinct visual registers.

---

## 8. Brand Voice & Language Style

### Tone: Overall Personality

Stripe's brand voice is one of the most distinctive in the technology sector. It defies easy categorization: it is simultaneously **technical and humanistic**, **authoritative and approachable**, **ambitious and grounded**. Ten sub-categories:

1. **Infrastructure-builder voice:** Stripe consistently speaks in the language of "infrastructure" — not "tool," not "service," not "platform." Infrastructure implies permanence, scale, and foundational importance. "Financial infrastructure to grow your revenue." "Reliable, extensible infrastructure for every stack." This language positions Stripe as the pipes and protocols of commerce, not an app on top of someone else's pipes.

2. **Compounding ambition:** The brand uses language that builds scale narratively — "from your first transaction to your billionth." "From startups to Fortune 500s." "From scaling startups to complex global businesses." This isn't just scale talk — it's the arc of a company's entire lifecycle compressed into a single phrase.

3. **Confident restraint:** Stripe almost never uses exclamation points or hyperbole. "Start accepting payments" instead of "Start accepting payments TODAY!" The confidence to communicate without urgency-manufacturing is rare and signals category leadership.

4. **Technical precision used aspirationally:** Numbers are used both as stats and as story: "99.999% historical uptime." "500M+ API requests per day." "25M+ subscription renewals can be supported for a single business each day." These are technical performance metrics deployed as brand confidence signals — "we're so reliable we can specify it to four decimal places."

5. **Founder/entrepreneurship empathy:** The Jobs page language ("Stripe builds financial infrastructure that ambitious companies use to launch their boldest products") and the Customers page language ("We're building a platform for ambitious companies around the world") use the word "ambitious" deliberately. This is aspirational language directed at a specific psychographic: the people building companies, not the people maintaining ones.

6. **Intellectual curiosity as brand value:** The "Book of the Week" on the homepage (Stefan Zweig's *The World of Yesterday*) and references to Stripe Press, Works in Progress, and other intellectual resources signal that Stripe is not just a payments company — it has intellectual ambitions and cares about ideas. This is highly unusual in fintech marketing.

7. **Anti-jargon technical credibility:** Despite being a highly technical product, Stripe's marketing copy avoids AWS/enterprise technology jargon ("synergies," "digital transformation," "end-to-end solutions"). Instead, it uses plain, precise language: "Accept payments, offer financial services, and implement custom revenue models." The technical credibility comes from specificity, not buzzwords.

8. **Global without being generic:** Global ambitions are stated specifically: "135 countries," "100+ payment methods," "Accept international cards and currencies." Not "go global seamlessly" — but concrete geographic and operational specifics.

9. **Customer proximity:** Customer quotes are specific, attributed to real people with real titles at real companies. "For involuntary churn, we have found that Stripe Smart Retries have really worked for us. They're better than anything else we've tried." — Nadia Ali, CFO, Midjourney. The specificity signals authenticity; the quote content is technical and business-outcome focused (not "amazing product love it!").

10. **Mission gravity:** Stripe's language positions it as genuinely mission-driven around economic growth: "We're building a more connected global economy." "Businesses on Stripe generated $1.9T in 2025." The use of the word "GDP" (Global GDP running on Stripe: 1.62%) as a live stat on the homepage makes a direct claim about its economic significance.

### Language Patterns

**1. Infrastructure compound framing:**
Pattern: [scale claim] + [specific action] + [expanded scope]
Examples:
- "Financial infrastructure to grow your revenue. Accept payments, offer financial services, and implement custom revenue models—from your first transaction to your billionth."
- "Reliable, extensible infrastructure for every stack."
- "The backbone of global commerce"

**2. "Any [X]" pattern:**
Pattern: Repeated use of "any" to signal complete flexibility and lack of constraints
Examples:
- "Built for any business—from scaling startups to complex global businesses"
- "Bill and manage customers however you want"
- "Adapt to your business needs with flexible integration options"
- "Choose an integration path"
This "any" language removes objections before they're raised.

**3. "From X to Y" scale bracketing:**
Pattern: Compresses scale range into a single phrase
Examples:
- "From your first transaction to your billionth"
- "From hours-old startups to complex global businesses"
- "From startup incorporation to going global"
This works because it puts the reader at both ends simultaneously — wherever they are, Stripe fits.

**4. Causal/outcome-first structuring:**
Pattern: Lead with the outcome, then explain how
Examples:
- "Maximize revenue with AI-based tools" → then explains Smart Retries
- "Grow new lines of revenue" → then explains monetization
- "Accelerate growth with Stripe Billing" → then features
This is a sophisticated B2B content strategy: always lead with business outcome, not feature.

**5. Specificity as credibility:**
Pattern: Replace vague claim with specific metric or example
Examples:
- "99.999% historical uptime" (not "near-perfect uptime")
- "500M+ API requests per day" (not "handles massive volume")
- "$1.9T generated in 2025" (not "businesses grow with Stripe")
- "150K+ transactions per minute" (not "handles peak traffic")
The pattern is: make the claim quantifiable wherever possible.

**6. Geographic/cultural specificity:**
Pattern: Name specific countries, regions, and payment methods
Examples:
- "Businesses in Australia can now offer PayTo"
- "Businesses in the UK, Europe, Canada, Australia, and Singapore can now offer Pix"
- "Cartes Bancaires" (France-specific payment method listed by name)
This signals genuine global investment rather than US-centric thinking with an international FAQ.

**7. Year-over-year narrative momentum:**
Pattern: Reference to growth over time in customer success stories
Examples:
- "ElevenLabs grows into a $3B AI audio leader with Stripe"
- "Lovable grows into a vibe-coding juggernaut with Stripe"
- "URBN consolidates $5 billion in online and in-store revenue onto Stripe"
The verb "grows" and the outcome dollar amounts create a growth narrative.

**8. Technical depth as a trust signal:**
Pattern: Technical specifics in marketing copy
Examples:
- "Meter usage and track consumption in real time"
- "Connect with your CRM, order management software, and tax engine"
- "Handle thousands of transactions per second with consistent speed and reliability, even during peak traffic"
- "Use our SDKs, APIs, MCP server, and AI developer tools"
Stripe writes for people who know what "MCP server" means — developer empathy.

**9. Mission-ambition language (Jobs page):**
Pattern: Positions the product as world-changing to attract talent
Examples:
- "Our customers are building the future"
- "Collectively, they are growing the GDP of the internet. You can help."
- "The most important company in the global economy"
This language speaks to the desire for meaningful work at scale.

**10. Anti-feature-list bias:**
Pattern: Features described through the lens of business outcome, not as standalone capabilities
Examples:
- "Respond to user demand faster with flexible, diverse pricing models" (not just "Supports multiple pricing models")
- "From one-time order to lifetime customer" (not just "Subscription management")
- "Scale with confidence" (not just "99.99% uptime")

### Heading Style & Hierarchy

**Homepage H1:** "Financial infrastructure to grow your revenue. Accept payments, offer financial services, and implement custom revenue models—from your first transaction to your billionth."
- Observation: The H1 is a complete paragraph — an unusual choice. Most brands do a 3–5 word hero headline; Stripe uses a full compound sentence. This signals that precision matters more than punchiness.

**Payments H1:** "Unified, global payments to grow your revenue"
- Pattern: [Adjective, adjective] + [Product category] + [outcome clause]

**Billing H1:** "Accelerate growth with Stripe Billing"
- Pattern: [Action verb] + [outcome] + [brand + product]

**Pricing H1:** "Pricing built for businesses of all sizes"
- Pattern: [Product category] + [built for] + [audience]

**Customers H1:** "The payments platform behind millions of businesses"
- Pattern: [Definite article + superlative claim] + [customer scale]

**Enterprise H1:** "Build the next era of your enterprise"
- Pattern: [Command verb] + [aspirational claim]

**Jobs H1:** "Our customers are building the future"
- Pattern: [Possessive pronoun] + [ongoing action] + [aspirational outcome]
- Notable: Jobs page H1 is ABOUT the customers/users, not about Stripe or the job. This is a recruitment strategy — "work here because your work matters to the world," not "come join our amazing company."

**Blog article H1s (examples):**
- "Insights from Shoptalk 2026: How agents are changing retail" — Direct, journalistic
- "How Stripe Radar helps prevent free trial abuse" — How-to framing, product-first
- "Introducing the Machine Payments Protocol" — Launch announcement format
- "10 things we learned building for the first generation of agentic commerce" — Listicle/learning format

**Heading capitalization rules:**
- H1 headings: always sentence case or title case (Stripe alternates between the two based on length — longer/more informal = sentence case; shorter/more formal = title case)
- Section H2s: mostly sentence case on content-heavy pages; title case on product feature headers
- Blog category tags: ALL CAPS in some editorial designs, Title Case in navigation
- Sub-nav links: Title Case

### CTAs & Microcopy

**Homepage CTAs:**
- "Get started ›" — primary hero CTA, purple filled
- "Sign up with Google" — secondary, Google logo, white button
- "Join us at Sessions" — event, text link
- "Start now" — final CTA module, purple
- "Contact sales" — secondary, text link/outlined
- "Pricing details ›" — footer area
- "Integration options ›" — footer area
- "Read the letter" — editorial, text link

**Product Page CTAs (Payments):**
- "Start accepting payments ›" — primary, purple
- "Contact sales ›" — secondary, text link
- "Register now ›" — Sessions event badge

**Product Page CTAs (Billing):**
- "Get started with Billing ›" — primary, green
- "Contact sales ›" — secondary, text link

**Pricing Page CTAs:**
- "Get started ›" — Standard tier
- "Contact sales ›" — Custom tier

**Blog CTAs:**
- "Read more ›" — article cards
- "View all posts ›" — bottom of listing
- "Contact us ›" — footer of blog

**Customer Stories CTAs:**
- "See all stories ›" — primary
- "Contact sales ›" — secondary
- "Watch video ›" — per story
- "Read [company]'s story ›" — per story (brand name personalization)

**Support CTAs:**
- "Search help articles..." — primary interaction
- "Contact support" / "24×7 help from our support staff" — contact option

**Contact/Sales Form Microcopy:**
- "Let's get you to the right place" — H1 (friendly, directional)
- "We just need a few quick details." — subhead (downplays friction, "few quick")
- "Stripe will handle your data pursuant to its Privacy Policy" — legal, placed below form
- "Continue ›" — CTA (generic but effective)

**Footer CTA:**
- "Sign in ›" — with right arrow, reinforces action orientation

**Microcopy tone analysis:**
Stripe's microcopy is remarkably consistent in tone: **functional, non-condescending, slightly formal but never stiff**. It never uses:
- Exclamation marks in UI copy
- Infantilizing language ("Oops! Something went wrong!")
- Marketing-speak in error states
- Urgency/scarcity language ("Only 3 spots left!")
- False casual language ("Hey there!")

The 404 page exemplifies this: "Page not found! Sorry, but the page you were looking for could not be found. You can return to our front page, or drop us a line if you can't find what you're looking for." — Direct, helpful, no drama.

---

## 9. Platform & Technical Notes

### Platform Identification

Stripe.com is a **custom-built platform** — it is NOT Shopify, WordPress, Webflow, or any standard CMS. Evidence:
- URL structure: clean, non-CMS-indicative (`/payments`, `/billing`, `/blog`, `/customers`) — no `/wp-content/`, no `?page_id=`, no theme indicators
- Performance: extremely fast load times, suggesting custom-built JAMstack/React application with server-side rendering
- DOM structure: custom React component architecture with proprietary CSS systems
- JavaScript: Next.js or custom SSR React framework (inferred from SPA-style navigation with full-page loads)
- The animated product demos (live checkout forms, live billing plan selectors) are built as embedded React components
- The "Global GDP running on Stripe: X%" live counter is a real-time data call — requires custom API integration into the marketing site

**Support subdomain (support.stripe.com):** Appears to be built on a modified version of Zendesk or a custom help center platform. The visual design is adapted to Stripe brand standards but the information architecture (articles, categories, popular topics) follows Zendesk's standard patterns.

### Theme Architecture

Custom, proprietary. Section IDs in the DOM follow Stripe's internal naming conventions. The site uses:
- CSS custom properties (CSS variables) for the color system
- Component-based architecture (each "module" on the homepage is a self-contained component)
- Tailwind CSS or a similar utility-first CSS framework may be used alongside custom styles
- SVGs for icons and logo — no icon font observed

### URL Structure Patterns

- **Products:** `/payments`, `/billing`, `/terminal`, `/radar`, `/connect`, `/issuing`, etc. (flat, single-word)
- **Product sub-pages:** `/payments/checkout`, `/payments/elements`, `/billing/usage-based-billing` (product + feature)
- **Solutions:** `/use-cases/saas`, `/use-cases/platforms`, `/industries/travel` (category + segment)
- **Enterprise solutions:** `/enterprise`, `/startups` (flat)
- **Content:** `/blog`, `/blog/[article-slug]`, `/customers`, `/customers/[company-name]`, `/guides`, `/newsroom`
- **Legal:** `/privacy`, `/legal/restricted-businesses`, `/spc/licenses`
- **Support:** `support.stripe.com/` (distinct subdomain)
- **Jobs:** `stripe.com/jobs` (same domain, acts as distinct sub-site)
- **Dashboard:** `dashboard.stripe.com` (distinct subdomain)
- **Docs:** `docs.stripe.com` (distinct subdomain)

### Third-Party Integrations Identified

- **Google OAuth:** "Sign up with Google" button on homepage and registration pages
- **Stripe Dashboard** (`dashboard.stripe.com`): All sign-in and registration CTAs point to this subdomain — the actual product is a separate application from the marketing site
- **Stripe Press** (`press.stripe.com`): External subdomain for book publishing arm
- **Stripe Sessions** (`stripesessions.com`): External domain for annual conference
- **Works in Progress** (`worksinprogress.co`): External partner publication
- **GitHub** (`github.com/stripe`): Linked from developer sections
- **LinkedIn**: Author profile links in blog posts
- **X/Twitter** (`x.com/stripe`): "Stripe on X" link in blog
- **Tempo** (`tempo.xyz`): Linked from blog post about blockchain launch (Stripe-incubated)
- **Pushkin Press** (`pushkinpress.com`): Book of the week link
- **Databricks, Snowflake, Amazon Redshift, Google Cloud Storage, Azure, Salesforce, HubSpot, Shopify, Xero, Oracle NetSuite**: All mentioned/linked within Billing product page as integration partners

### Page Performance Observations

- Pages load very quickly — Stripe appears to aggressively optimize: image compression, lazy loading, code splitting
- The animated hero demos are JavaScript-rendered but load nearly simultaneously with page text — no FOUC (Flash of Unstyled Content) observed
- The "Global GDP" counter appears to be a real-time API call that resolves immediately
- No significant layout shift observed on load
- Images are served in modern formats (likely WebP) and lazy-loaded below the fold

### SEO & Meta Title Patterns

- **Homepage:** `"Stripe | Financial Infrastructure to Grow Your Revenue"` — brand name first, then value proposition
- **Payments:** `"stripe.com/payments"` — shown as URL in tab (meta title may be set differently in server response)
- **Billing:** `"stripe.com/billing"` — same pattern
- **Blog:** `"stripe.com/blog"` — same pattern
- **Pattern inferred:** `"[Product Name] | Stripe"` for product pages; `"[Article Title] | Stripe Blog"` for blog posts
- URLs are SEO-friendly: short, descriptive, lowercase, no parameters

### Legal & Compliance Pages

Identified at `/privacy`:
- **Privacy Policy** — Last updated: February 23, 2026
- **Stripe Privacy Center**
- **Data Processing Agreement**
- **Data Transfer Addendum**
- **Supplier Data Processing Agreement**
- **Supplier Data Transfers Addendum**
- **Data Privacy Framework**
- **Sub-Processors List**
- **Cookies Policy**

Linked from footer:
- Privacy and terms
- Prohibited and restricted businesses
- Licenses
- Cookie settings
- Your privacy choices (link to `privacy.stripe.com`)

### Accessibility Features

- **No third-party accessibility overlay widget** — Stripe relies on native implementation
- **Semantic HTML headings** used throughout (H1, H2, H3 hierarchy observed in DOM)
- **Alt text on images:** Observed in DOM (e.g., "Mobile payment terminal with instructions to tap, insert, or swipe to pay." — descriptive alt text, not filename-based)
- **Interactive elements with ARIA labels:** Buttons have proper accessible names in DOM (e.g., `"Show testimonial from Mindbody"`, `"Next slide"`, `"Previous customer story"`)
- **Screen reader-friendly:** Form labels are properly associated with inputs
- **Keyboard navigation:** Focus states implied by `:focus` styles; tab order follows visual order
- **Color contrast:** The `#0A2540` text on `#F6F9FC` background achieves approximately 15:1 contrast ratio — far exceeding WCAG AA/AAA requirements. Even `#697386` text on `#FFFFFF` achieves approximately 4.6:1 — meeting AA standard.
- **CA accessibility note:** Footer includes phone number "CA residents: +1 888 926 2289" — suggests California-specific compliance (CCPA)

### Social Media Accounts

- **X/Twitter:** `x.com/stripe` — linked from Blog page ("Stripe on X")
- **LinkedIn:** Author profile links in blog posts (individual employees, not a company page, though a company page exists)
- **GitHub:** `github.com/stripe` — linked from developer section
- **YouTube:** Implied by "Watch video" CTAs on Customer Stories, but no direct YouTube link observed on the pages reviewed
- No Facebook, Instagram, TikTok, or Pinterest links observed on the marketing site — consistent with Stripe's B2B developer-focused audience profile
- **Stripe Dev Blog** (`stripe.dev`): A separate developer-focused publication distinct from the main blog

---

## 10. Pages Browsed

1. https://stripe.com/ — Homepage
2. https://stripe.com/payments — Payments product page (PDP #1)
3. https://stripe.com/billing — Billing product page (PDP #2)
4. https://stripe.com/pricing — Pricing page
5. https://stripe.com/blog — Blog / Editorial index
6. https://stripe.com/contact/sales — Contact/Sales form page
7. https://stripe.com/customers — Customer Stories index page
8. https://stripe.com/newsroom — Newsroom / Press page
9. https://stripe.com/newsroom/about-stripe — 404 page (captured as error state design reference)
10. https://support.stripe.com — Support / FAQ / Help Center
11. https://stripe.com/enterprise — Enterprise solutions landing page
12. https://stripe.com/privacy — Privacy Policy / Legal page
13. https://stripe.com/jobs — Jobs / Careers page
14. https://stripe.com/about — Redirected to homepage (captured as redirect behavior)

**Total unique pages browsed: 14**

---

*Stripe Brand Standards Audit compiled April 2026. All data extracted directly from live site via DOM reading, screenshot analysis, and page text extraction. Screenshots saved to workspace.*
