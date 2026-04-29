# xAI Brand Standards Audit: extracted from https://x.ai across 13 pages (April 2026)

## 1. Color Palette
xAI's color system is one of the most aggressively monochromatic in tech. The site is engineered around a near-black background, white type, and a single semantic accent (orange) that is reserved almost exclusively for ambient gradient washes behind hero treatments. The overall mood is closer to an observatory control room or a high-end terminal than a consumer app. Every color choice reinforces the company's positioning: scientific, serious, infrastructure-grade, and "first-principles" rather than expressive.
### Primary brand
- **#0A0A0A**. the canonical xAI background black. Found in homepage hero canvases, news article hero placeholders, the body `bg-background` token, and as the fill for the Grok product card cosmic SVG (`<rect .. stroke="url(#paint0_linear_33863_16843)">` over `#0A0A0A`). It is just barely off pure black; the slight warmth keeps OLED displays from looking inert and gives the page a "deep space" rather than "void" register. Strategic intent: convey gravitas and infrastructure scale (this is a company that owns "Colossus"), and make rendered SVG and white type feel like instrumentation readouts.
- **#0C0C0B**. the secondary "card" or "media frame" black, used as the fallback fill on news hero rectangles (`bg-[#0C0C0B]`) and on the framed device mockup blocks under the API and Developer Docs cards. It is one luminance step warmer than #0A0A0A so cards visibly separate from the page background without ever introducing actual contrast. The 0.4% delta is intentional. xAI does not use gray cards; they use "blacks at slightly different temperatures."
- **#FFFFFF (white)**. the primary content color, used for body type, navigation, headings, logo `currentColor` fill, and the gradient `stop-color="white"` anchors on every decorative SVG (Grok-loop, API-frame, Docs-stack). Appears explicitly as `#ffffff` in the contact page CSS. Its purpose: sole legibility carrier in an otherwise dark surface, and the start-stop of every fade-to-black gradient.
### Secondary / accent
- **rgba(255, 99, 8, 0.1)**. the only true non-monochrome accent in the entire production palette. It is xAI orange (approximately #FF6308), used at 10% alpha in the multi-stop hero glow gradient on the homepage SuperGrok / "Understand the Universe" section: `linear-gradient(to right, rgba(255, 99, 8, 0.1), rgba(255, 99, 8, 0.1), rgba(189, 201, 230, 0.1), rgba(151, 196, 255, 0.1), rgba(151, 196, 255, 0.1))`. Strategic intent: orange reads as "ignition," "rocket exhaust," and "Tennessee data center heat". all SpaceX-adjacent metaphors that became literal once xAI joined SpaceX. It is never used opaque on the website.
- **rgba(189, 201, 230, 0.1)**. a desaturated pale-blue ("steel haze"), used in the same homepage gradient as a transitional step between orange and full blue. The hex equivalent is approximately #BDC9E6. Strategic intent: a "twilight horizon" middle tone that prevents the orange-to-blue jump from looking like a children's rainbow.
- **rgba(151, 196, 255, 0.1)**. a soft sky blue (approximately #97C4FF) at 10% alpha, used as the cool end of the same hero gradient and in additional ambient washes. Strategic intent: paired with orange, it produces a sunrise/sunset sky impression. xAI never uses this blue as an actionable UI color (links, buttons), only as ambient atmosphere.
- **rgba(255, 255, 255, 0.1)**. the workhorse "secondary" surface tint on the Grok page (used to mask gradients into the background). Functionally a 10% white over black.
- **`from-steel`**. a Tailwind theme color name used in the 404 page gradient (`from-steel to-background`). The name implies a cool gray, consistent with the ambient blue family. Not a public hex.
### Code-syntax accent palette (Grok page only, code mockup)
The Grok page renders a fake React `useDebounce` snippet. The exact colors mirror GitHub's classic dark syntax theme:
- **#24292E**. the slate "code editor" background fill behind the snippet on the Grok page.
- **#F97583**. keyword red ("import," "function," "const," "return"). Pulls from GitHub's "primer-dark" red.
- **#9ECBFF**. string yellow / peach for quoted module names and strings.
- **#79B8FF**. function and variable name blue.
- **#B392F0**. purple for `useState`, `useEffect`, `setTimeout`, `clearTimeout` (built-in/library identifiers).
- **#FFAB70**. orange for parameter / property tokens.
- **#75FBA6**. neon green for return values and arrow functions.
- **#E1E4E8 / #e1e4e8**. the off-white code base text color.
These colors are not part of xAI's website-level palette. They appear once, inside an illustrative code window, and are an obvious appropriation of the GitHub Primer dark syntax theme. Strategic intent: instant developer trust signal, "you know this color theme."
### Backgrounds
- **#0A0A0A** as `bg-background` token. every page background.
- **#0C0C0B** as the inset card / media frame on news cards.
- Decorative SVG masks paint linear gradients from `white` (top) to `#0A0A0A` (bottom) at the 80% stop, producing the signature "scanned from above" fade on every diagrammatic illustration (Grok loop, API panel, Docs stack).
- Hero canvases use full-bleed `<canvas>` elements stacked on radial-gradient masks (`mask:radial-gradient(circle at center, black, transparent)`) to dim the edges and recenter focus.
### Text colors
- **`text-primary`** = white at 100% (`#FFFFFF`) for headings, top-level navigation when active, body copy, and footer legal text.
- **`text-primary/85`** = white at 85% alpha. the prose-class body text color (`prose-p:text-primary/85`, `prose-li:text-primary/85`, `prose-td:text-primary/85`). Used on Safety, Brand Guidelines, and any /legal page.
- **`text-primary/50`** = white at 50% alpha. inactive nav links (`text-primary/50 mono-tag hover:text-primary`), placeholder text in the "What do you want to know?" textarea (`placeholder:text-primary/50`), and the secondary CTA captions on news cards.
- **`text-secondary`**. used for paragraph body in product cards ("Grok is your cosmic guide...", "Supercharge your applications..."). The token resolves to roughly the same family as `text-primary` but lighter on hover. Visually equivalent to a soft warm white.
- **`text-accent`**. used only in the prose `prose-code:text-accent` style for inline `<code>` on legal/safety pages. The accent token is the orange; it is the only place opaque orange shows up in body content.
### Button colors
The button system is implemented as a single component with three variants, all routed through CSS custom properties:
- **Primary CTA filled** (`Try Grok` in the Grok hero, `Grok Web` mobile-buttons row): `--btn-bg: theme(colors.primary)` (white), `--btn-border: theme(colors.primary)` (white), `--btn-text: theme(colors.background)` (#0A0A0A black), `--btn-hover: theme(colors.primary/80%)` (white at 80% alpha). The button is white-on-black, inverts to slightly translucent on hover. Strategic intent: in a dark UI, full white is the most assertive thing possible, and treating the brand's signature CTA as "the brightest object on the page" reads as confidence.
- **Primary CTA outline** (the universal "Try Grok," "Read announcement," "Sign up now," "Build with API"): `--btn-bg: transparent`, `--btn-border: theme(colors.primary/25%)` (white at 25%), `--btn-hover: theme(colors.secondary/20%)` (warm-white at 20%), `--btn-text: theme(colors.primary)` (white). Pill-shaped (`rounded-full`), uppercase mono type. This is by far the most common button on the site.
- **404 page outline**: `--btn-border: theme(colors.primary)` full white, `--btn-hover: theme(colors.primary/20%)`. identical to the standard outline but at full border opacity. Subtle reinforcement that the "Back to home" CTA is more emphatic.
- **"Use now / Build now / Learn more" pill** (inside product cards): identical to the outline button but smaller (`px-3.5 py-1.5`, `[&>[data-slot=icon]]:size-3`). The pill uses `pointer-events-none group-hover:bg-[--btn-hover]` so the hover state is triggered by the *card* hover, not the button. Strategic intent: the entire card is the click target; the pill is a visual stand-in for "this is interactive."
### UI state colors
- **Hover** on buttons: `--btn-hover: theme(colors.secondary/20%)` for outline, `theme(colors.primary/80%)` for filled.
- **Hover** on links / nav: `text-primary/50` to `text-primary` (the inactive state literally raises opacity from 50% to 100% on hover). On hover within product cards, headings shift from default to `group-hover:text-primary`, and supporting paragraph text shifts from `text-secondary` to `group-hover:text-primary`.
- **Logo hover**: header logo button has `hover:bg-white/10`. a 10% white hover wash, the only place on the site that uses an explicit white hover background.
- **Focus ring**: every button declares `data-[focus]:outline-blue-500` (Tailwind blue-500, approximately #3B82F6). This is the only blue accent that ever activates intentionally for the user, and only via keyboard focus, not visible by default.
- **Disabled**: `data-[disabled]:opacity-50`. universal 50% opacity for disabled state. The submit button in the homepage hero textarea ships in disabled-50% by default until you type.
- **Active nav link**: `text-primary` (full white). The current page's nav item has 100% opacity; all others sit at 50%.
- **Group-hover focus crosshairs**: product cards reveal four small `bg-primary` (white) corner pip squares (`-left-1 -top-1 z-10 size-2`) on hover. a deliberate "Hasselblad reticle" or "scope crosshair" treatment that signals scientific instrumentation.
### Border / divider
- **`border-border`**. the primary divider token, used on every section break (`border-b`, `border-t`, `border-l`) and on the article rows in the news feed. It resolves to a desaturated near-black slightly lighter than `#0A0A0A` (estimated approximately #1A1A1A at full opacity).
- **`border-primary/10`**. a 10% white border, used on product card outline hover state.
- **`border-primary/25%`**. the 25% white border that defines all outline buttons.
- **`border-border/50`**. a semi-transparent border on the global footer divider.
- Horizontal hairline gradient: `bg-gradient-to-r from-transparent via-white to-transparent opacity-40` is used as a one-pixel divider above the SuperGrok wordmark on the homepage. The divider literally fades in from black to white to black, which is more like a horizon than a rule.
### Announcement bar
xAI does not use a colored announcement bar. The pattern they substitute is an "inline announcement," shown bottom-left under the homepage hero search box: `Announcing Grok Voice Think Fast 1.0: Our fastest and most capable voice model yet.` paired with a Read announcement outline button. Color: white text on the same `#0A0A0A` background, no fill, no shadow. The mobile fallback shrinks the text to just "Think Fast 1.0" and replaces the descriptive headline with the version number alone.
### Footer
- Background: `#0A0A0A` (continuous with body, no separation tone).
- Top divider: `border-t border-border/50`. a single hairline against pure black.
- Column heading: `mono-tag text-sm` rendered in white at full opacity. No `[ ]` brackets here, just a plain caps-mono label ("Try Grok On," "Products," "API," "Company," "Resources").
- Link color: white at 100%, `hover:underline` on hover. No alternative tint, no muted footer gray.
- The footer occupies five equal columns (`md:grid-cols-5`) on desktop and stacks fully on mobile.
### Notable absences
- **No purple, no green, no red, no yellow** anywhere on a primary content surface. The only chromatic colors in the palette are orange #FF6308 at 10% alpha, soft blue #97C4FF at 10% alpha, steel haze #BDC9E6 at 10% alpha, and Tailwind's blue-500 focus ring (visible only with keyboard focus).
- **No mid-tone grays** as cards or chips. xAI does not use #2A2A2A or #3A3A3A surfaces. They differentiate elements with one-pixel hairlines and gradient masks rather than a tonal gray system.
- **No gradient buttons.** Every button is a pill outline or a flat fill. Gradients are reserved for atmospheric backgrounds and SVG fade-outs.
- **No "success green" or "error red" semantic system** visible on the marketing site. Only the focus blue functions semantically; everything else carries semantic meaning through type, spacing, and animation.
- **No dark-mode toggle.** The page is locked to dark (`localStorage 'theme': 'dark'`, attribute defaulted to `dark`, color-scheme tokenized to dark only). xAI is dark by decree.
- **No company-specific orange logo color** (the X / xAI logo is rendered with `fill="currentColor"`, so it inherits white. there is no signature "xAI orange logo" or "Grok purple logo"). Brand identity comes from form, not chroma.
---
## 2. Typography
xAI runs a three-family stack served via Next.js' built-in font loader (woff2 only, no third-party [fonts.googleapis.com](http://fonts.googleapis.com)). Three CSS variables are bound to `__variable_c1e5c9`, `__variable_d00f93`, and `__variable_4de444`. Based on the woff2 fingerprints (nine distinct font files preloaded), the stack resolves to:
- **Display / sans (primary)**: a custom or licensed grotesque consistent with **Inter** or **PP Mori**, used for everything that is not a "tag." Weights observed in the wild: 300 (light, used in 404 mega numerals), 400 (regular), 500 (medium, used for `prose-strong`), 600 (semibold, used for `prose-strong:font-semibold`).
- **Mono (tag and tracking-widest)**: an open-aperture industrial monospace consistent with **JetBrains Mono** or **IBM Plex Mono**, used wherever the class `font-mono` or the custom `mono-tag` utility is applied. This is the typeface that gives every nav item, every CTA button, and every footer column header that "AS-BUILT DRAWING" feel.
- **Serif**: not visible in any rendered page. Reserved class only.
The body is set up via Tailwind's `antialiased font-sans` class and inherits `text-primary` (white). The site is set in pure dark mode.
### H1 specs
- **Class**: `text-balance text-3xl tracking-tight md:text-4xl lg:text-5xl`.
- **Family**: sans (primary grotesque).
- **Size**: 1.875rem (30 px) on mobile, 2.25 rem (36 px) at md, 3 rem (48 px) at lg. xAI never goes above 5xl on standard headings.
- **Weight**: 400 (regular). The site explicitly overrides prose defaults with `prose-headings:font-normal`. xAI does not use bold display type.
- **Line-height**: implicit (Tailwind default approximately 1). The combination of `text-balance` plus `tracking-tight` and a low weight is the signature.
- **Letter-spacing**: tight (`tracking-tight`, approximately -0.025em).
- **Transform**: none (sentence case).
- **Color**: white (`text-primary`).
- **Examples**: "AI for all humanity" (homepage), "Grok is your truth-seeking AI companion for unfiltered answers with advanced capabilities in reasoning, coding, and visual processing." (Grok hero), "xAI Brand Guidelines" (legal/brand-guidelines), "Page not found" (404 fallback at `text-2xl lg:text-3xl`).
### H2 specs
- **Class**: `text-balance text-3xl tracking-tight md:text-4xl lg:text-5xl` (visually identical to H1. they share the display style).
- **Family**: sans.
- **Size**: same as H1. 30 / 36 / 48 px.
- **Weight**: 400.
- **Line-height**: implicit, paired with `text-balance` to lock the orphan word.
- **Letter-spacing**: -0.025em.
- **Transform**: sentence case.
- **Color**: white.
- **Examples**: "Latest news" (homepage), "Chat with Grok. the truth-seeking AI chatbot" (Grok page), "Work with a powerful AI assistant," "Take your company to the next level."
### H3 specs
- **Class**: `text-xl` (and `leading-6` on news article cards). On product cards, just `text-xl group-hover:text-primary`.
- **Family**: sans.
- **Size**: 1.25 rem (20 px). exactly half a step up from body 16 px.
- **Weight**: 400.
- **Line-height**: 1.5 rem (24 px) on news cards.
- **Letter-spacing**: default.
- **Color**: `text-primary` (white) at full or 85% in prose.
- **Examples**: "Grok," "API," "Developer Docs" (product cards), "Realtime search," "Understand documents," "Supercharge your code," news article titles ("Grok Voice Think Fast 1.0," "Grok Speech to Text and Text to Speech APIs," "xAI joins SpaceX").
### H4 / H5 / H6 specs
- H4: Used inside the prose container only (legal pages). Class: `prose-h4:mt-6`. Inherits the sans family at 400 weight; size delegated to Tailwind Typography defaults. approximately 1.125 rem (18 px).
- H5: Same prose convention. `prose-h5:mt-6`. Approx 1 rem (16 px), weight 400.
- H6: `prose-h6:mt-6`. Approx 0.875 rem (14 px), weight 400.
### Body text
- Default: 1 rem (16 px), weight 400, line-height 1.5, color `text-primary` or `text-primary/85` depending on whether it is in a prose container.
- Body classes vary by section: `text-sm/6` on tags (approximately 14 px / 24 px line-height), `text-lg sm:text-xl` on the SuperGrok promotional paragraph ("Do more with Grok. Unlock a SuperGrok subscription on [Grok.com](http://Grok.com).". 18 / 20 px), `leading-6` on sidebar product blurbs, `text-balance` ubiquitous.
### Nav text
- **Class**: `text-primary/50 mono-tag hover:text-primary px-3 py-1.5 text-sm`.
- **Family**: mono (`mono-tag`).
- **Size**: 0.875 rem (14 px).
- **Weight**: 400.
- **Letter-spacing**: extended (the `mono-tag` utility implies a wider tracking, consistent with `tracking-widest` on the buttons; no `uppercase` on the nav itself but the type is mono and reads quasi-engineered).
- **Transform**: title case (Grok, API, Company, Colossus, Careers, News, Shop, SpaceX, Twitter glyph).
- **Color**: 50% white inactive, 100% white active and on hover.
### Button text
- **Class**: `font-mono text-base/6 uppercase tracking-widest sm:text-sm`.
- **Family**: mono.
- **Size**: 1 rem / 1.5 line-height on mobile (`text-base/6`), 0.875 rem (14 px) at sm.
- **Weight**: 400 (mono regular).
- **Letter-spacing**: `tracking-widest` approximately 0.1em. This is dramatic, deliberate, and is the signature voice of the xAI button.
- **Transform**: ALL CAPS (`uppercase`).
- **Color**: white in outlines, black on white in primary fills.
- **Examples**: "TRY GROK," "READ ANNOUNCEMENT," "USE NOW," "BUILD NOW," "LEARN MORE," "SIGN UP NOW," "EXPLORE MORE," "READ," "GROK WEB," "GROK ON X," "iOS," "ANDROID," "BUILD WITH API," "LET'S TALK."
### Label / badge / tag text
- **Class**: `mono-tag flex items-center gap-2 text-sm`. a recurring three-character motif that reads `[ Products ]`, `[ Blog ]`, `[ Our Mission ]`, `[ Our principles ]`, `[ Offices ]`, `[ Capabilities ]`, `[ Enterprise ]`, `[ Minutes to launch ]`, `[ For projects big and small ]`, `[ Pricing ]`, `[ What's new ]`, `[ Grok for Business ]`, `[ Grok Imagine ]`, `[ Our Gigafactory of Compute ]`, `[ Our Purpose ]`, `[ Join us ]`, `[ What to expect ]`, `[ Enterprise Inquiry ]`. These bracketed labels are xAI's substitute for an eyebrow heading.
- The brackets are real characters in the markup.
- News article date stamps use the same convention: `mono-tag text-xs leading-6` for "April 23, 2026," "April 17, 2026," "February 02, 2026."
- Article tag pills also use the mono-tag utility: `mono-tag text-xs` for "grok voice," "company."
### Form text
- The hero `textarea` placeholder ("What do you want to know?") sets `placeholder:text-primary/50`. Family: sans. Size: defaults to body (16 px). The textarea is `h-[120px]`, padded `py-5 pl-4 pr-16`, on a `bg-background` (true black) ground, encapsulated in a 1-px gradient border.
- Form labels on the Grok Enterprise inquiry form ("First Name *", "Last Name *", "Email Address *", "Company Name *", "Company Size *", "Job Title/Role *") render in mono-tag at `text-sm`, white. Required fields marked with a single `*` after the label.
### Footer text
- Column headers: `mono-tag text-sm`, white, no brackets.
- Footer links: `hover:underline` on a default sans link. body weight, body size, white at 100%.
- Footer is dense and unstyled. no fancy typographic treatment, no cap-eq sizing.
### Uppercase / lowercase usage rules
xAI uses case as a structural signal, not a stylistic flourish:
- **Uppercase** only on buttons (`uppercase tracking-widest`). Never on headings, never on nav, never on body.
- **Sentence case** on every heading and every body run.
- **Title case** on nav (`Grok`, `API`, `Company`).
- **Lowercase** on news tag pills (`grok voice`, `company`). This subtle drop into lowercase under news cards is the only place xAI uses all-lowercase, and it codes the tag as a system-generated taxonomy term rather than editorial content.
### Letter-spacing distribution
- `tracking-tight` (-0.025em): all headings.
- `tracking-widest` (0.1em): all buttons, all uppercase moments.
- Default: nav, body, mono tags, footer.
- The juxtaposition of `tracking-tight` headings against `tracking-widest` mono buttons creates xAI's signature typographic tension: the headline is dense and confident, the call to action is technical and engineered.
### Font-weight distribution
- 300 (light): only the giant 404 numerals `font-mono text-[10rem] font-light` and `text-[20rem]` at sm. This is the only place light weight appears.
- 400 (regular): everything else by default.
- 500 (medium): table headers in prose (`prose-th:font-medium`).
- 600 (semibold): inline `<strong>` in prose only (`prose-strong:font-semibold`).
xAI never uses 700 / 800 / 900 / black weights. Headings stay at 400 by override (`prose-headings:font-normal`).
### Type scale philosophy
- A compressed scale: body (16) to tag (14) to small tag (12) to H3 (20) to display (30 / 36 / 48). No 60+ px monumental display, no 64-pixel hero numerals (except the 404).
- The scale is asymmetric: huge jumps between 20 and 30 (a 50% step) and from 30 to 48 (60% step), but tiny jumps between 12 / 14 / 16. This makes "headings vs everything else" the dominant typographic relationship and de-emphasizes intermediate hierarchy.
- Strategic intent: the page reads as "system output." The body, tags, and nav all sit in a narrow band like rows of a status console, while the display headings rise above them like banner messages.
### Application by page type
- **Homepage**. H1 ("AI for all humanity") at lg:5xl, H2 ("Latest news") at lg:5xl, supporting body in 16 px sans, `mono-tag` brackets for section eyebrows, mono uppercase pills for CTAs.
- **/grok product page**. Same scale, H1 visually displayed only at lg breakpoint (`sr-only lg:not-sr-only`), H2s at lg:5xl, supporting body 16 px, plus a faux GitHub code window in monospace.
- **/api page**. Mono-tag eyebrows, full pricing tables in mono numbers (`grok-4.20-reasoning`, `$2.00`, `$0.20`, `2M`).
- **/company, /careers, /colossus**. same scale, even more reliance on the bracketed eyebrow pattern.
- **/news index**. date stamps in mono at 12 px, headlines as H3 at 20 px, body in 16 px sans, "READ" pills in uppercase mono.
- **/legal/\* pages and /safety**. wrapped in `prose prose-invert` so headings cascade through prose-h1 (3xl) to prose-h2 to prose-h3 (10mt to 6mt to 6mt) at `font-normal`. Code blocks render in mono on a `bg-secondary/20` chip, `text-accent` orange. Body color drops to `text-primary/85`.
- **404 page**. outlier. Uses `font-mono text-[10rem] sm:text-[20rem] font-light` numerals with a `from-steel to-background bg-gradient-to-b to-[75%] bg-clip-text text-transparent` treatment. The 404 numerals fade from steel-blue to background-black at the 75% stop. This is the most expressive moment of typography on the site and exists nowhere else.
---
## 3. Logo & Wordmark
### Primary logo
The xAI mark is a custom geometric "X" inscribed in 24x24, the right stroke being a vertical bar that reads as both an "i" and the second leg of an X. Per the SVG path, the mark is two negative-space slashes meeting around a central vertical: `M2.30047 8.77631L12.0474 23H16.3799L6.63183 8.77631H2.30047..`. It is monolithic, uppercase only by implication (no lowercase variant exists on the site), and renders with `fill="currentColor"` so it inherits the parent text color. On the live site it is therefore always rendered in white (#FFFFFF). The site provides a "Right click to copy SVG" affordance via `aria-label="xAI Logo - Right click to copy SVG"`. a small but unusual hospitality gesture toward developers and designers.
There is also a **type-in-form** wordmark, "Grok," displayed as a custom-drawn SVG path on the homepage SuperGrok module. The wordmark "G-R-O-K" is rendered as filled paths (no live type), with an inner shadow filter (`filter id="filter0_i_33774_13227"`) that gives the letterforms a subtle pressed, illuminated edge. Color: a top-to-bottom white gradient from `stop-color="white" stop-opacity="0.9"` to `stop-opacity="0.5"`.
### Header placement
- **Desktop** (`lg:flex`): Logo at far left at `class="size-8"` (32x32 px), wrapped in an `<a aria-label="xAI Homepage" href="/">`. Then the primary nav (`Grok / API / Company / Colossus / Careers / News / Shop / SpaceX / Twitter`) immediately to its right with `ml-3` left-margin. Then push-right `Try Grok` outline pill button.
- **Mobile** (`lg:hidden`): Logo at left, hamburger icon at right (a three-bar icon, drawn inline as an SVG with three round-cap stroked rectangles), no inline nav. The `Try Grok` button still appears alongside the hamburger.
- The header is `fixed inset-x-0 top-0 z-50`. It carries a `from-black duration-200 lg:from-black/75` gradient overlay that fades out at scroll-top, plus a `bg-background/25 backdrop-blur` band that activates on scroll. Header height: `lg:h-20` (80 px) with `py-4` padding.
### Footer treatment
xAI does not lock up the logo in the footer. The footer is purely typographic. five mono-tag column headers, link lists, no logo, no tagline, no certification badges. The logo only ever appears in the header. This is unusual: most enterprise sites repeat the logo in the footer for brand reinforcement. xAI treats the logo as a header-only element and lets the URL itself be the footer's brand signal.
### Favicon
- Path: `/favicon.ico`
- Size: 32x32, type `image/x-icon`. One static favicon, no platform variants exposed in HTML metadata (no apple-touch-icon, no maskable variants in the head).
### OpenGraph / Twitter image
- Homepage: `https://x.ai/opengraph-image.png?6014284994b18e1d`, 1280x672.
- Grok page: `https://x.ai/grok/opengraph-image-s2iyx8.png?a8af9e875584db92`, 1280x672.
- Safety page: `https://x.ai/safety/opengraph-image-wktepx.png?f140e9b340fe0bf5`, 2400x1260.
- Twitter handle attribution: `@xaboratory` (both `twitter:site` and `twitter:creator`).
### Logo variations
- The only published logo variation is the primary geometric X. There is no "wordmark + symbol" lockup, no horizontal lockup, no stacked lockup, no mono-color reverse (because the live site is always dark. the white-on-black is the only state).
- The wordmarks for "Grok" and "xAI" that appear in dedicated SVG drawings (the giant "GROK" wordmark on the SuperGrok module, and the giant "Grok" wordmark drawn under the Grok page hero) are bespoke per-module artwork, not a reusable logo asset.
### Clear space
Implicit via the `-m-1 inline-flex .. p-1` wrapper on the header logo button. a 4 px / 0.25 rem clear-space ring around the SVG. There is no published clear space rule in the brand-guidelines page; that page only governs partner usage of the Marks and refers users to a downloadable logo pack ("Download our logos") rather than publishing pixel-level rules.
### Sizing
- Header logo: `size-8` (32 px square).
- Per the public brand guidelines page: usage is permitted "only \[if the logo is used\] exactly as provided at the download link below, without any alteration or adjustment." No published minimum size, no published max. the rule is "use only the artwork file we ship."
### Co-branding
- The header includes `SpaceX` and the X glyph as inline nav items linking off-site. Following the February 2026 SpaceX acquisition, xAI's navigation literally now contains a link to its parent company's homepage.
- The site explicitly says `"Note: xAI is a separate company from X (formerly Twitter)."` on /legal/brand-guidelines, which contradicts how the audience naturally reads the X-glyph nav item but is legally accurate.
- In the news article "xAI joins SpaceX," the article hero is a flat `bg-[#0C0C0B]` placeholder rectangle with no co-branded lockup. xAI does not show a SpaceX-and-xAI lockup graphic anywhere on the site.
### Logo-to-nav relationship
The 24x24 SVG is drawn at the same baseline height as the nav text (`text-sm`, 14 px caps height). The mono nav characters cap at roughly 10 px tall while the logo is 32 px, producing a 3:1 visual ratio between logo and nav text. The 12 px gap (`ml-3`) between logo and the first nav item ("Grok") is generous, telegraphing that the logo is an anchor mark rather than a participant in the menu.
### Strategic interpretation
- The X-as-logo signals "scientific shorthand" (the unknown variable, the multiply operator, the chromosome). Drawing it as a rendered geometric object rather than a typeface character means it can never be confused with the typed character `X` in the navigation.
- White-on-black with `currentColor` inheritance is a developer-grade gesture: any partner who copies the SVG inherits the right color automatically.
- Refusing to put the logo in the footer reads as Apple-tier confidence: the URL is enough.
- The "Right click to copy SVG" cue in the aria-label confirms the audience: developers and designers, who will copy the asset rather than wait for a brand-pack download.
---
## 4. Layout & Grid System
### Content max-width
- **Standard container**: `mx-auto w-full px-4 lg:px-6 xl:max-w-7xl`. The xl breakpoint pins to 80 rem / 1280 px. Below xl, the layout is full-width with `px-4` (mobile) or `px-6` (desktop) gutters.
- **Prose container** (legal, safety, brand guidelines): `mx-auto w-full px-4 lg:px-6 lg:max-w-3xl`. narrowed to 48 rem / 768 px for reading length.
- **Hero textarea form**: `max-w-3xl` (768 px), centered.
### Homepage section sequence
The xAI homepage is essentially seven stacked sections, each separated by `border-border` hairlines:
1. **Fixed header** with logo, primary nav, Try Grok CTA.
2. **Full-viewport hero** (`h-svh`) with the giant "Grok" wordmark SVG centered at 50% opacity, an 80 px tall textarea form ("What do you want to know?") in the upper third of the section, and a bottom row containing a downward-pointing scroll-arrow icon plus the announcement copy with a "Read announcement" outline button.
3. **Products grid** ("AI for all humanity"). three columns at lg, stacked on mobile. Each cell contains an H3, a paragraph, an SVG illustration (Grok cosmic loop, API panel, Docs document stack), and a "Use now / Build now / Learn more" pill button. Cells use `border-border border-t lg:border-l lg:border-t-0` so the dividers form a seamless grid without box outlines.
4. **"Understand The Universe" supergraphic**. a full-bleed gradient-text moment, with `Understand` left-aligned and `The Universe` right-aligned, both bg-clipped on `from-secondary to-primary` gradients. Sits over a circular `<canvas>` ambient background.
5. **SuperGrok promo**. centered SVG wordmark, the orange-blue ambient gradient wash described in section 1, two body lines, one outline "Sign up now" CTA.
6. **Latest news**. vertical list of three news rows with a `[ Blog ]` mono-tag eyebrow, an "Explore more" outline button anchored top-right, and rows separated by `border-b py-16`. Each row has a date stamp on the left, headline + body + tag pill in the middle column, and a 16:10 aspect-ratio media frame on the right (currently empty `bg-[#0C0C0B]`).
7. **Footer**. five-column link group, no logo.
### Product List Page (PLP). n/a / alternative
xAI does not have a PLP in the e-commerce sense. The closest equivalents are:
- **Products grid on the homepage** ("AI for all humanity"): three product tiles (Grok, API, Developer Docs), each occupying a third of a 12-column grid at lg, stacking to single column at md and below. Each tile is `from-secondary/10 border-border border-t via-transparent to-transparent lg:border-l lg:border-t-0 lg:hover:bg-gradient-to-b`. On hover the tile gradients in a subtle warm wash and reveals four corner crosshair pips.
- **News index** (`/news`): a vertical feed of articles, not a grid. Each row is a horizontal flex layout (date \| content \| hero block).
- **API model and pricing list** (`/api`): a stacked card list of model rows, each card showing model name, "New" badge if applicable, body description, and four spec columns ("Capabilities," "Context window," "Text Input," "Image Input," "Output").
### Product Detail Page (PDP). n/a / alternative
- **/grok** is the closest analog. Its layout: full-viewport hero (giant "Grok" wordmark backdrop, "Try Grok" + "Build with API" CTAs), then a stack of feature sections. each H2 headline + supporting body + a centered hero image or interactive illustration. Sections include "Chat with Grok. the truth-seeking AI chatbot," "Work with a powerful AI assistant," "\[ Grok Imagine \] AI image and video generation," "Available anywhere," "Let's play."
- **/news/\[slug\]** is a more traditional article PDP: date stamp, H1 headline, optional H2 subheadline ("Scaling Up Reinforcement Learning"), prose body, embedded benchmark tables and charts, footer.
- **/api/voice** and **/api/imagine** are product-specific API detail pages.
- **/grok/business** and **/grok/government** function as "audience PDPs," each with `[ Grok for Business ] / [ Grok for Government ]` mono-tag eyebrows, headline, capability list, pricing tile, and an enquiry form.
### Editorial / content layouts
- News article pages: 768 px max-width prose container, sentence-case headlines, generous `py-16 sm:py-32` vertical padding, embedded benchmark tables (`prose-th:py-2 prose-th:font-medium prose-td:py-2 prose-td:text-primary/85`), inline `<code>` chips with `bg-secondary/20`, a "Latest news" trailing module, and footer.
- The article hero placeholder is a large 16:10 `bg-[#0C0C0B]` block that is empty until populated with an image.
### Support page layouts
- /security, /safety, /legal/\* all use the same `prose prose-invert` container at `lg:max-w-3xl` with `prose-h1:text-3xl prose-headings:font-normal prose-p:text-primary/85 prose-a:text-primary prose-a:underline prose-code:bg-secondary/20 prose-code:text-accent`. Tables are styled minimally; lists use default disc bullets; horizontal rules render via `prose-hr:border-border`.
### Section padding rhythm
- Standard section: `py-16 sm:py-32`. 64 px / 128 px vertical. This is xAI's signature breathing room and is applied to almost every section on every page.
- Hero: `h-svh` (full small-viewport height). On mobile this is the device viewport height; on desktop it produces a giant first impression.
- Hero inner spacing: `mt-20 flex h-full w-full items-center` to push content below the fixed 80 px header and center it vertically.
- Footer: `pb-32 md:pb-64`. 128 px / 256 px bottom padding before the page ends, producing the "lots of breath at the bottom" feel.
- Inter-section spacing inside a container: `space-y-16 sm:space-y-32`.
### Element spacing
- Inter-card gap on grids: `gap-0 lg:grid-cols-3 lg:-space-x-px`. zero gap with a negative margin to merge borders into shared hairlines (a one-pixel grid).
- Inter-paragraph gap: `space-y-6` (24 px) for blocks of body text.
- Inline gap on button rows: `gap-2` (8 px) or `gap-3` (12 px) depending on context.
- Header nav gap: `gap-4` (16 px) between major nav items.
### Responsive breakpoints
xAI uses Tailwind's default breakpoints throughout:
- **sm**: 640 px. most `sm:py-32`, `sm:text-sm` activations.
- **md**: 768 px. `md:flex-row`, `md:grid-cols-5`.
- **lg**: 1024 px. primary breakpoint where the desktop nav appears, hero copy switches from short to long form, the products grid becomes three-column.
- **xl**: 1280 px. the `xl:max-w-7xl` container ceiling.
The page is mobile-first: the desktop nav is hidden by default and revealed at `lg:flex`, the mobile hamburger is `visible lg:hidden`.
### Whitespace philosophy
- xAI uses whitespace as a luxury signal. Every section has `py-16 sm:py-32` (and often `space-y-16 sm:space-y-32` between subsections) so the page feels like a museum interior at desktop breakpoint.
- Cards use generous interior padding (`px-0 py-10 lg:p-8`) and a `gap-10` between text and illustration.
- Footer has a 256 px bottom padding (`md:pb-64`).
- The empty 16:10 hero placeholders on news cards are deliberately empty. they hold space for imagery that may not be ready yet, rather than collapsing.
### Scroll depth
- Homepage: approximately 4x viewport height end to end (full-svh hero plus three desktop viewports of stacked sections plus 256 px footer).
- /grok page: approximately 6x viewport height (full-svh hero plus capability cards plus Grok Imagine gallery plus multi-platform availability plus games gallery plus footer).
- /news index: longest page (approximately 8x viewport), one row per article, approximately 28 articles back to November 2023.
### Full-bleed vs contained
- **Full-bleed**: the hero canvas, background gradients, "Understand The Universe" supergraphic, the signal hairlines (`bg-gradient-to-r from-transparent via-white to-transparent` 1-px lines stretched edge-to-edge).
- **Contained at xl:max-w-7xl**: every other content surface. products grid, news list, footer, hero text content (the canvas behind it is full-bleed but the form and CTAs are contained).
- **Contained at lg:max-w-3xl**: prose / legal / safety pages.
The site avoids "boxed cards on a colored background" entirely. Everything either bleeds to viewport edge or fills the 1280-px content frame.
---
## 5. UI Components
### Buttons
xAI ships exactly two button shapes: a **rounded-full pill** (almost everything) and a **rounded-full circular icon button** (`aspect-square` for hamburger and submit). All buttons share the base class `relative isolate inline-flex shrink-0 items-center justify-center border font-mono text-base/6 uppercase tracking-widest`.
**Sizes:**
- Standard: `gap-x-3 px-4 py-2 sm:text-sm`. Used for "Try Grok," "Read announcement," "Sign up now."
- Compact pill: `gap-x-2 px-3.5 py-1.5 sm:text-sm`. Used for product card "Use now," news "Read."
- Icon-only: `aspect-square gap-x-3 px-4 py-2`. Used for the hamburger and the textarea submit arrow.
**Variants:**
- **Primary filled (white)**: `[--btn-bg:theme(colors.primary)] [--btn-border:theme(colors.primary)] [--btn-hover:theme(colors.primary/80%)] [--btn-text:theme(colors.background)]`. Used on the Grok hero "Try Grok" / "Grok Web" / "Build with API."
- **Primary outline (white at 25%)**: `[--btn-bg:transparent] [--btn-border:theme(colors.primary/25%)] [--btn-hover:theme(colors.secondary/20%)] [--btn-text:theme(colors.primary)]`. Used everywhere else.
- **404 outline (white at 100%)**: `[--btn-border:theme(colors.primary)] [--btn-hover:theme(colors.primary/20%)]`.
**States:**
- Default: as above.
- Hover: `hover:bg-[--btn-hover]` swaps the background to the hover token.
- Focus: `data-[focus]:outline data-[focus]:outline-2 data-[focus]:outline-offset-2 data-[focus]:outline-blue-500`.
- Disabled: `data-[disabled]:opacity-50`.
- Touch hit-area expander: each button declares a hidden 44x44 px touch target overlay only on touch pointers.
**Icon buttons:** the textarea submit is `aspect-square gap-x-1.5 px-3 py-1` filled white, with a 16 px upward arrow. The hamburger is the same shape but outline.
### Navigation
- **Desktop primary nav**: nine items (Grok, API, Company, Colossus, Careers, News, Shop, SpaceX, X glyph). Items 1-6 link to `/grok`, `/api`, `/company`, `/colossus`, `/careers`, `/news`. Items 7-9 are external (`https://shop.x.ai`, `https://spacex.com/`, `https://x.com`). Inactive at 50% white, active at 100% white. Shop / SpaceX / X glyph carry `target="_blank"`.
- **Mobile primary nav**: hidden by default; replaced with a hamburger icon. The hamburger triggers a JS-driven sheet (not in the rendered SSR HTML).
- **Sub-nav**: xAI does not use a horizontal sub-nav. Section anchors on /api are exposed via fragment URLs (`/api#capabilities`, `/api/voice`, `/api/imagine`) rather than a tabs row.
- **Breadcrumbs**: none. xAI does not use breadcrumbs anywhere on the site, including news articles. Navigation back is implicit (header logo links to `/`).
- **Announcement strip**: see section 1. Inline within the hero, not a banded top-of-page strip.
### Product / feature cards
- **Homepage products grid card**: `group relative flex h-full flex-col space-y-4 px-0 py-10 lg:p-8 from-secondary/10 border-border border-t via-transparent to-transparent lg:border-l lg:border-t-0 lg:hover:bg-gradient-to-b gap-10 overflow-hidden md:flex-row lg:flex-col`. On hover: applies the warm gradient wash (`bg-gradient-to-b`) and reveals four white pip squares at the corners. Contains an H3, a paragraph, an SVG illustration, and a pill button.
- **Grok page capability cards** (Realtime search, Understand documents, Supercharge your code, Find meaning with Grok Think, Talk with Grok Voice): same shape and same border treatment, but the illustration is an embedded UI mockup rather than a vector loop.
- **API model card**: row-based, with model name plus optional "New" badge as H3, capability list, and four data columns (Context window, Text Input, Image Input, Output) right-aligned.
### "PDP" equivalents. model spec / pricing
- **/api models list**: each model (`grok-4.20-reasoning`, `grok-4.20-non-reasoning`, `grok-4-1-fast-reasoning`, `grok-4-1-fast-non-reasoning`, plus a "Show older models" reveal containing eight prior models) renders as a row with `2M $2.00 $2.00 $6.00` columns. Prices in USD per million tokens. Older models are progressively disclosed via a Show older models toggle.
- **Cost calculator**: an interactive widget with a model dropdown, three slider inputs (Text Input Tokens 0 to 500k, Image Input Tokens 0 to 500k, Output Tokens 0 to 5k), and a live-updated cost readout (`$0.26`) implemented via shadow DOM number-flow animation.
- **Grok for Business pricing**: two tile pricing cards (Business at `$30 / month`, Enterprise at `Let's talk`), with feature-inclusion lists below ("SOC 2 Compliance," "Role Based Access Control," "Increased rate limits," "No training on your data," "Team and seat management," "Consolidated billing," "Domain Verification and Claims," "User analytics," "Custom data retention," "Apps (Google Drive and more)," "Advanced audit and security controls," "Custom Single Sign On (SSO)," "Directory Sync (SCIM)," "Custom Role Based Access Control," "Advanced User and Access Management," "Dedicated onboarding and ongoing support," "Customer-Managed Encryption Keys," "Application-Level Encryption," "Dedicated Data Plane").
### Forms
- **Hero textarea** (homepage and Grok page): `<textarea name="query"> placeholder="What do you want to know?"`. Wrapped in a `bg-gradient-to-tr p-px from-primary/5 to-primary/20` gradient ring on a `rounded-3xl` container. Autofocus ring `focus:ring-2 focus:ring-zinc-500`. Submit is the icon-square white pill at bottom-right. The form does not POST in the public HTML; it relies on JS to redirect to `grok.com`.
- **Inputs (Grok Enterprise inquiry)**: First Name *, Last Name *, Email Address *, Company Name *, Company Size * (dropdown: 1 to 149, 150 to 999, 1,000 to 9,999, Over 10,000), Job Title/Role *, Which xAI product are you interested in purchasing? * (dropdown: API (General API inquiries), Grok Imagine API, Grok Voice API, Grok Enterprise, Grok Enterprise Vault), Other, Enterprise Needs *, Request access submit button.
- **Validation**: required fields marked with a single asterisk; no inline error messaging visible in SSR.
- **Newsletter**: xAI does not run a newsletter sign-up form on the marketing site. There is no email capture form on the homepage, the news index, or the footer. This is a notable absence.
- **Cookie consent**: not present in the rendered HTML for any of the pages we audited. The legal/cookie-policy URL exists but no banner is displayed to a default visitor.
### Accordions
- xAI does not use accordions in primary nav, FAQs, or content. The /api page has a `[+] Show older models` reveal that functions as a single-element disclosure but is not a full accordion. Legal pages render flat, not collapsed.
### Footer
Already covered in section 1 and 4. Five columns: Try Grok On, Products, API, Company, Resources. No logo, no legal copyright line, no language switcher, no newsletter, no social icons (the X / SpaceX nav is in the header, not the footer).
### Other
- **Search**: there is no global search affordance on the marketing site. The hero "What do you want to know?" textarea is the closest equivalent and routes to [grok.com](http://grok.com), not site search.
- **Modal**: none observed. Even the "Right click to copy SVG" affordance is implemented via OS-level context menu, not a modal.
- **Toast**: none observed.
- **Loading state**: the API page has an inline animated typewriter "Installing Grok.." treatment in the Quickstart section, plus a "Grok 4 Heavy / Processing / approximately 10 min left / Agent 1 / Agent 2 / Agent 3" multi-agent processing animation on the Grok page and the /news/grok-4 article.
- **Empty state**: news cards ship with empty `bg-[#0C0C0B]` 16:10 placeholders for hero imagery. The placeholders are intentional and form a regular rhythm down the news feed.
- **Video**: the marketing site relies on rendered SVG animations and image carousels rather than embedded video. No `<video>` or YouTube iframes were observed in the SSR HTML.
- **Scroll animations**: Heavy use of `style="opacity:0;transform:translateY(40px)"` on hero elements, with JS unmasking on scroll. The wordmark fade-in on the Grok page hero is the most visible example.
- **Chips**: tag pills on news rows (`mono-tag text-xs`) function as type-only chips, not interactive filters.
- **Tables**: pricing tables on /api and /grok/business render as styled HTML tables with `prose-th:py-2 prose-th:font-medium`. No fancy zebra striping, no hover row highlighting.
### Accessibility observations
- Buttons declare a `[@media(pointer:fine)]:hidden` 44 px touch overlay specifically to give touch users the WCAG-recommended hit area without affecting mouse users. This is a thoughtful pattern.
- The site uses real `<button type="button">` and `<a aria-label="...">` instead of div-buttons.
- The Grok hero declares `<h1 class="sr-only lg:not-sr-only">Grok is your truth-seeking AI companion...</h1>`. meaning the H1 is screen-reader-only on mobile and visible on desktop. SEO crawlers and assistive technology still get a real H1.
- The logo button has `aria-label="xAI Logo - Right click to copy SVG"`.
- Focus state is real (`outline-blue-500`), if subtle.
- Color contrast is high: white on near-black is well above WCAG AAA. The 50% white nav text on near-black (approximately 4.5:1 contrast) just clears AA for normal text and is the only borderline contrast moment on the site.
- The "What do you want to know?" textarea has no associated visible `<label>`, only a placeholder. The submit button's `aria-label="Submit a query to Grok"` is the only assistive cue.
---
## 6. Iconography
### Icon library
xAI uses **Heroicons** (Tailwind Labs' icon set), inlined as SVGs with `data-slot="icon"` and `aria-hidden="true"`. Verifiable via path-data fingerprints:
- The down-arrow on the homepage hero matches Heroicons solid `arrow-down`.
- The diagonal up-right arrow on every CTA matches Heroicons outline `arrow-up-right`.
- The hamburger matches Heroicons solid `bars-3`.
- The submit-up arrow inside the search box matches Heroicons solid `arrow-up`.
- The 404 page back-arrow matches Heroicons solid `arrow-right`.
### Style
- Mostly **solid (filled) Heroicons** when used as primary indicators (down arrow on hero, hamburger).
- **Outline Heroicons** with `stroke-width="1.5"` for in-button arrows on CTAs ("Use now," "Build now," "Sign up now"). xAI consistently chooses the outline variant when the icon is decorative-trailing on a button and the solid variant when the icon is the only content of the button.
- Stroke caps: `stroke-linecap="round"`, `stroke-linejoin="round"`.
### Where icons appear
- Hero: the giant scroll-down arrow (Heroicons `arrow-down`, `size-6`, white at full opacity, positioned at the bottom of the hero).
- Buttons: every CTA pill (filled or outline) ends in a 16 px outline `arrow-up-right`, which is xAI's universal "this leads off the standard flow" indicator. The arrow is `size-5 sm:size-4` on full-size buttons and `size-4 sm:size-3` on compact pills.
- Mobile nav: the hamburger icon, solid bars-3.
- Form submit: the upward `arrow-up` icon inside the search box.
- 404 back-button: a solid `arrow-right` chevron.
- Decorative SVGs (Grok loop, API panel, Docs stack, multi-agent processing animation, etc.) are bespoke per-module artwork, not part of the icon library.
### Sizing
- `size-3`: 12 px (compact pill button icons at sm).
- `size-4`: 16 px (default CTA icon, mobile compact icons).
- `size-5`: 20 px (default CTA icon at desktop).
- `size-6`: 24 px (hero scroll-arrow indicator).
- `size-8`: 32 px (header logo).
- All icons inherit `currentColor` so they pick up the parent text color.
### Color
- All icons render in white (`currentColor` resolves to `text-primary`) on a black ground.
- Inside white-filled buttons, the icon flips to black (parent button has `--btn-text:theme(colors.background)`).
- No multicolor icons. Heroicons are monochromatic, and xAI does not paint in custom hues. Icons never use orange, blue, or any of the secondary palette.
### Notable absences
- **No social icons in the footer.** Social presence is exposed only through nav text labels (`SpaceX`, X glyph) and through the contact page text links ("Visit xAI on X," "Visit Grok on X," "Join Grok on Discord"). Discord, Apple App Store, Google Play are referenced by name but not by icon glyph.
- **No status / certification icons** (no SOC 2 logo, no GDPR badge, no AICPA mark) on /security or /grok/business, even though these certifications are mentioned in copy. xAI lets the certification name appear as text in the body.
- **No file-format icons** on /safety, even though it links to several PDFs ("Frontier Artificial Intelligence Framework," "Grok 4 Fast model card," "Grok Code Fast 1 model card," "Grok 4 model card"). The links render as standard underlined text.
### Philosophy
xAI treats icons as wayfinding affordances, not visual ornament. The arrow vocabulary is consistent and minimal. down-arrow says "scroll," up-right arrow says "go elsewhere," up-arrow says "submit," right-arrow says "next." Heroicons gives them a clean default; the brand chooses sizes and colors but never restyles the glyphs themselves. This maintains visual consistency with the broader Tailwind-built web while keeping xAI's identity in the type and layout, not the icons.
---
## 7. Photography Style
xAI is essentially a **photography-free** brand on the marketing site. There is no studio photography, no environmental supercomputer photography, no founder portraits, no team photos, no lifestyle imagery. Every visual on the homepage and most subpages is either a typographic moment, a vector SVG illustration, a generated rendering, or a UI screenshot.
### Imagery types observed
- **Vector illustrations (cosmic / orbital geometry)**: the homepage products grid uses three custom SVGs. a Grok orbit/spaceship loop (the spinning trajectory around a planet), an API panel diagram (a wireframed control panel with crosshairs), and a Docs document stack (offset rectangles representing pages). Color: white strokes / fills on `#0A0A0A`, with vertical fade-out gradients. All artwork is line-based, geometric, and reads as "scientific instrument schematic."
- **Typographic supergraphics**: "Understand The Universe" rendered as a 5-rem display in `bg-gradient-to-l from-secondary to-primary`, "Grok" rendered as a 32x212 viewBox bespoke wordmark behind the Grok hero, and "GROK" rendered as a 310x80 viewBox illuminated wordmark on the SuperGrok module.
- **UI screenshots / app mockups**: the Grok page's main content image is `app-ui.0bf0a7dc.webp` (3060x1490) showing the Grok chat interface across web and mobile devices. Color-graded to match the site dark mode.
- **Generated AI artwork (Grok Imagine)**: the /grok page features a gallery of Grok-generated images described in detailed alt-text-style captions: "Lockheed SR-71 Blackbird flying through an abstract sky," "An astronaut standing on the surface of an alien planet, with a spaceship in the background and multiple moons in the sky," "A volcano surrounded by ice," "A superposition of a cat in a hyperbolic time chamber in the style of Van Gogh," "An origami Cybertruck," "Cherry blossoms beneath a sunset sky," "A sketch of a multi-sided 3d geometric shape on paper," "A dog drinking a cup of tea in a library," "A closeup of a guitar player's hand holding a pick," "A burger with double meat patty placed on a plate," "A female warrior holding a sword, with intricate armor and a confident expression," "An abstract composition using geometric shapes and vibrant colors," "Elon Musk as a character in the animated series Rick and Morty," "A serene mountain lake at sunset," "A cyberpunk-inspired city at night," "An elderly person, capturing every wrinkle and expression," "A dewdrop on a spider web." The gallery serves dual purposes: as proof of capability and as the dominant photographic register on the page.
- **Benchmark charts**: blog posts (e.g., /news/grok-4) embed line charts and bar charts ("Humanity's Last Exam," "Pass@1 Accuracy (%)," "GPQA Science," "LiveCodeBench (Jan to May)," "Competitive Coding," "USAMO 2025 Olympiad Math Proofs," "HMMT 2025 Competitive Math," "AIME'25 Competition Math," "ARC-AGI-2 Abstraction and Reasoning"). Charts are monochromatic (white lines on black with hairline gridlines). true to the broader visual system.
- **Loading/processing animations**: the multi-agent "Grok 4 Heavy / Processing / approximately 10 min left / Agent 1 / Agent 2 / Agent 3 / Thought for 10 minutes" sequence is an animated illustration that reappears on /grok and /news/grok-4.
### Lifestyle, hero, color grading
- **Lifestyle imagery**: not present. xAI does not show humans, environments, devices in physical use, or any "people-using-AI" visuals. The Grok app UI screenshot is the only "in use" image on the site.
- **Hero imagery**: typographic. Each hero is built on a typography supergraphic (the "Grok" word fading in over a circular canvas) instead of a hero photo.
- **Color grading**: every visual is graded to match the dark mode site. backgrounds at #0A0A0A or #0C0C0B, foreground in white, with optional ambient gradients in orange-to-blue at 10% alpha. Even the AI-generated gallery on /grok is presumably curated to fit this register; the site's dark surface frames the imagery uniformly.
### Image quality
- All images are served via Next.js' `_next/static/media/..webp` pipeline at 2x density (e.g., 3060x1490 source for a roughly 1500-px display).
- `loading="lazy"` is applied to non-hero images.
- Decorative SVGs are inline (no external request); content imagery is served as `webp`.
### Recurring motifs
- **Cosmic / orbital geometry**: the Grok product card SVG is a spaceship's flight path circling a body. The "Understand The Universe" supergraphic. The SuperGrok module's circular `<canvas>` ambient. The descriptive AI-generated gallery (astronaut, planet, sunset).
- **Schematic / engineering line art**: the API panel SVG (with a wireframed monitor and a circular indicator), the Docs stack SVG (with a bordered document grid), the multi-agent processing diagrams. These read as engineering drawings or AS-BUILT documentation.
- **Crosshair and pip squares**: the four-corner pip overlay on hovered product cards, plus the circular indicator dot and tracking rectangle in the API panel SVG. Hasselblad / scope reticle vocabulary.
- **Particle / canvas ambient**: nearly every section has a `<canvas>` element used for a JS-rendered particle field or radial gradient that subtly responds to scroll. These canvases are positioned absolutely at the section's center with `mask:radial-gradient(circle at center, black, transparent)`.
### What is NOT shown
- **No human faces**, no founders, no Elon Musk (despite being mentioned in the AI gallery prompt: "Elon Musk as a character in the animated series Rick and Morty". the only mention of him is inside an AI prompt).
- **No employee or team photography** on /careers, /company, or /colossus, even though the company prides itself on being a "focused and mighty team."
- **No supercomputer / data center photography** on /colossus, despite the page being literally named "Colossus." The page substitutes statistics ("200K GPUs," "194 Petabytes/s," "3.6 Terabits/s," "\> 1 Exabyte") and a timeline for visual evidence of the facility.
- **No office photography** on /company, even though the page enumerates Palo Alto, Seattle, San Francisco, Tennessee, and London UK.
- **No customer logos or testimonial photography** on /grok/business, even though SOC 2, GDPR, CCPA are mentioned.
- **No press / event photography**.
- **No product unboxing / merch photography** despite the existence of a `shop.x.ai` link in the nav.
This absence is itself the brand position. xAI says: "We are a research lab, not a marketing brand. The product is the visual."
---
## 8. Brand Voice & Language Style
This is the most distinctive layer of the xAI brand and the place where the company differentiates itself most sharply from OpenAI, Anthropic, Google DeepMind, and Meta. The voice is the antithesis of the fuzzy-friendly assistant register that has come to dominate AI marketing.
### Tone & emotional register
xAI writes the way a senior engineer at SpaceX writes a Slack channel pinned message at 3 AM after a successful test fire. The register is:
- **Short, declarative, confident.** Sentences average eight to twelve words. There are almost no hedges, qualifiers, or "we believe."
- **Cosmic-scale ambition juxtaposed with breakneck operational urgency.** The site routinely pairs phrases like "Understand the Universe" with "Move quickly and fix things." It is a deliberately Musk-coded tonal blend (high-mission rhetoric plus speed-of-execution rhetoric).
- **Pseudo-mathematical formality.** The careers page principle "Coding is greater than or equal to x for all x" is rendered as a literal mathematical statement (using the universal-quantifier symbol). The page does not translate this into English. The audience is expected to read mathematical notation.
- **Dry, near-zero emoji, no exclamation points except in self-deprecating moments.** The phrase "We are also introducing a new SuperGrok Heavy tier with access to Grok 4 Heavy" is written in standard report tone. The only place exclamation points show up is in the original 2023 announcement: "Grok is an AI modeled after the Hitchhiker's Guide to the Galaxy. It is intended to answer almost anything and, far harder, even suggest what questions to ask!"
- **Self-mythology.** The Colossus page begins: "We're running the world's biggest supercomputer, Colossus. Built in 122 days. Outpacing every estimate. It was the most powerful AI training system yet. Then we doubled it in 92 days to 200k GPUs. This is just the beginning." Each sentence is a load-bearing claim. There is no equivocation.
- **Civilizational stakes.** "AI for all humanity," "advance scientific discovery and understand the universe," "accelerate human scientific discovery," "the world's smartest AI," "build AI systems that can help humanity understand the world better." The frame is always species-level, not user-level.
- **Direct provocation, occasionally.** The Grok positioning leans on the word "truth-seeking" and "unfiltered," which is intentional contrast against perceived competitor sanitization. From /grok: "Grok is your truth-seeking AI companion for unfiltered answers with advanced capabilities in reasoning, coding, and visual processing."
### Narrative voice
- **First-person plural** ("We," "Our," "Us") for company statements: "We're a focused and mighty team connected by our curiosity, commitment, and unwavering drive." "We challenge conventional thinking by breaking down problems to their fundamental truths." "We were told it would take 24 months to build. So we took the project into our own hands, questioned everything, removed whatever was unnecessary, and accomplished our goal in four months."
- **Second-person direct address** for product copy: "Grok is your cosmic guide." "Grok is your truth-seeking AI companion." "Give your team superpowers." "Take your company to the next level."
- **Imperative voice on CTAs and section sub-heads**: "Try Grok," "Build now," "Use now," "Sign up now," "Read announcement," "Find answers," "Start talking," "Dive Deep," "Join us."
- **Documentary / deck voice on the Colossus page** ("Built in 122 days. Outpaced every estimate."). Reads like an ad for a moonshot.
### Heading patterns
xAI's heading conventions are remarkably consistent:
- **Mission-scale H1s on home pages**: "AI for all humanity" (homepage products section), "Understand the Universe" (company page, written as the site mission), "Build AI That Advances Humanity" (careers).
- **Imperative product headlines**: "Chat with Grok. the truth-seeking AI chatbot," "Work with a powerful AI assistant," "Talk with Grok Voice," "Find meaning with Grok Think," "Deep dive with Grok Heavy," "Supercharge your code," "Understand documents."
- **System / category H2s**: "Latest news," "Models that fit your needs," "Ready for your business," "Models and pricing."
- **Featured product names rendered in title case as H3**: "Grok," "API," "Developer Docs," "Realtime search," "Vision," "Voice API," "Tool calling," "Image generation," "Search."
- **Mono-tag eyebrows in brackets**: see section 2 for the exhaustive list.
- **Date-stamped headlines on news**: H3 article titles paired with a `mono-tag` date below each row.
- **Co-opted equation as principle heading**: "Coding is greater than or equal to x for all x" (careers).
### Complete CTA inventory by page context
**Header / global**
- `Try Grok` (everywhere; primary outline pill).
- Mobile: hamburger icon (no label).
**Hero. homepage**
- `What do you want to know?` (textarea placeholder; the textarea plus submit-up arrow is itself a CTA).
- `Read announcement` (desktop) / `Think Fast 1.0` (mobile). outline pill linking to /news/grok-voice-think-fast-1.
**Hero. Grok page**
- `Try Grok` (filled white pill, links to [https://grok.com/?referrer=website](https://grok.com/?referrer=website)).
- `Build with API` (outline pill, links to [https://console.x.ai](https://console.x.ai)).
**Hero. /grok/business**
- `Sign up below` (passive prompt, not a button).
- `Read our announcement`.
**Hero. /careers**
- `View Open Roles` (filled / outline depending on layout).
- `Apply Now` (within step 1 of the interview process).
**Hero. /api**
- `Multi-Agent API` (link).
- `Documentation` (link).
- `Start building` (outline pill in Quickstart).
- `View docs` (in the Grok 4.20 spotlight).
- `Cost calculator` (label on widget).
- `Contact sales` (outline pill).
**Hero. /colossus**
- (no hero CTA; the page is informational).
**Products grid (homepage)**
- `Use now` (Grok card, links to [https://grok.com](https://grok.com)).
- `Build now` (API card, links to [https://console.x.ai](https://console.x.ai)).
- `Learn more` (Developer Docs card, links to [https://docs.x.ai](https://docs.x.ai)).
**SuperGrok promo (homepage)**
- `Sign up now` (outline pill, links to [https://grok.com/plans](https://grok.com/plans)).
**Latest news section**
- `Explore more` (outline pill, links to /news).
- `Read` (per-row outline pill).
**Grok page feature cards**
- `Find answers` (Find meaning with Grok Think).
- `Start talking` (Talk with Grok Voice).
- `Dive Deep` (Deep dive with Grok Heavy).
- `Analyze this document` (Understand documents).
- `Write a debounce hook in React` (Supercharge your code. appears as the example prompt).
**Grok page "Available anywhere"**
- `Grok Web` (filled).
- `Grok on X` (outline).
- `iOS` (outline).
- `Android` (outline).
**News article footer**
- `Try SuperGrok` (filled).
- `Access the API` (outline).
**Enterprise inquiry**
- `Request access` (form submit).
- `Let's talk` (Enterprise pricing card primary CTA).
- `Create a team` (Business pricing card primary CTA).
**Contact page**
- `Email support`, `Call support`, `Email sales`, `Visit xAI on X`, `Visit Grok on X`, `Join Grok on Discord`.
**Careers**
- `View Open Roles`.
- `Apply Now`.
**404 page**
- `Back to home`.
### Product description formula
xAI uses a consistent "Verb plus Capability plus Promise" pattern for product blurbs:
- **Grok**: "Grok is your cosmic guide, now accessible on [grok.com](http://grok.com), iOS, and Android. Explore the universe with AI."
- **API**: "Supercharge your applications with Grok's enhanced speed, precision, and multilingual capabilities."
- **Developer Docs**: "Learn how to quickly install Grok at the heart of your applications and explore guides covering common use cases."
- **Realtime search**: "Gain insights from X trends, analyzing real-time data and user sentiment across industries."
- **Reasoning**: "Understand the universe: solve humanity's most difficult scientific problems with deep thought."
- **Vision**: "See the world through vision, interpreting images and visuals with sharp, insightful understanding."
- **Voice API**: "Build real-time voice agents with speech-to-text, text-to-speech, and conversational AI capabilities."
- **Tool calling**: "Craft agentic experiences with both server-side and client-side tool calling with our Agent Tools API."
- **Image generation**: "Bring your ideas to life with image generation, creating visuals that are as unique as you are."
- **Search (API)**: "Tap into the now with real-time search, pulling fresh, relevant data from the web and X instantly."
- **Understand documents**: "Condense lengthy documents into concise summaries, highlighting key points and actionable findings."
- **Supercharge your code**: "Receive code guidance, solutions, and best practices without executing or debugging."
- **Find meaning with Grok Think**: "Discover profound insights with Grok Think, connecting dots and revealing truths in complex ideas."
- **Talk with Grok Voice**: "Engage in seamless conversations with Grok Voice, experiencing natural, fluid dialogue like never before."
- **Deep dive with Grok Heavy**: "The most powerful version of Grok. Now available with a SuperGrok Heavy subscription on all platforms."
- **Grok Imagine**: "Create stunning images and videos from text prompts. Edit, remix, and share your creations with the Grok community."
- **Colossus**: "We're running the world's biggest supercomputer, Colossus. Built in 122 days. Outpacing every estimate."
The formula:
1. Open with an imperative verb that paints a worldview action ("Understand," "See," "Build," "Bring," "Tap into," "Engage," "Discover," "Supercharge," "Gain insights," "Condense").
2. Pivot through the capability ("the universe," "the world through vision," "the now," "lengthy documents into concise summaries").
3. Close with the differentiator ("with deep thought," "with sharp, insightful understanding," "as unique as you are," "powered by native tool use," "in 122 days").
Sentences average two to three clauses. Paragraphs are rarely longer than two sentences.
### Recurring language patterns
- **"Truth-seeking"** is the canonical adjective for Grok. It appears in the meta description, the H1 of /grok, and the page title. It positions Grok against perceived competitor "guard-railed" or "evasive" behavior.
- **"Frontier"** is xAI's preferred adjective for capability ("frontier models," "frontier intelligence," "frontier AI products," "frontier capabilities," "Frontier Artificial Intelligence Framework"). Where Anthropic says "state of the art," xAI says "frontier."
- **"Understand"** as a verb: "Understand the universe," "Understand documents," "Understand the world better," "frontier-level multimodal understanding." This is the company's mission-verb.
- **"Cosmic" / "universe" / "humanity"** appear as the core lexicon of mission rhetoric. Grok is called "your cosmic guide." Mission statements include "advance human comprehension," "advance scientific discovery," "accelerate human scientific discovery," "advance our collective understanding of the universe."
- **"First principles"**. the careers page principle "Reasoning from First Principles" is rendered with title-case capitalization, signaling its status as a doctrine.
- **"Move quickly and fix things"**. a deliberate pun-twist on Facebook's old "Move fast and break things." xAI has rewritten the phrase to emphasize *fixing*, signaling responsibility while keeping speed.
- **"Exceptional"** is the recurring talent qualifier ("Exceptional Software Engineer" job titles, "Exceptional candidates are welcome to apply," "exceptional skills and mindset we're looking for").
- **"State of the art" / "industry-leading" / "best in the world"** is liberally claimed: "Grok 4 is the most intelligent model in the world," "the lowest hallucination rate on the market," "industry-leading speed," "the world's biggest supercomputer," "the best assistant in the world is now Enterprise ready."
- **Speed and quantification.** Time and scale appear constantly: "Built in 122 days," "doubled in 92 days," "200K GPUs," "194 Petabytes/s," "3.6 Terabits/s," "\> 1 Exabyte," "2M context window," "\$0.20 per million tokens," "256,000 context window," "\$30 / month," "\$6B Series C," "\$20B Series E."
- **"We" / "our"**. the brand never refers to itself in third person except in legal text. There is no "xAI offers..." marketing copy. It is always "We're running..." / "Our mission is..." / "We build AI..."
### Brand-specific terminology
- **Grok**: the consumer / chat product, named for the verb coined in Heinlein's *Stranger in a Strange Land* and re-popularized by *The Hitchhiker's Guide to the Galaxy*.
- **SuperGrok / SuperGrok Heavy**: paid subscription tiers on [grok.com](http://grok.com).
- **Grok Heavy / Grok 4 Heavy**: the "most powerful" tier of any given Grok generation, accessed via SuperGrok Heavy. Uses parallel test-time compute and a multi-agent processing pattern.
- **Grok Voice / Grok Think / Grok Imagine**: capability sub-brands (voice chat, reasoning, image / video generation).
- **Grok Voice Think Fast 1.0**: latest voice model.
- **Grok 4 / Grok 4.1 / Grok 4.20 / Grok 3 / Grok 2 / Grok 1.5 / Grok 1.5V / Grok-1**: model versioning.
- **Grok Code Fast 1**: agentic coding model.
- **Grok 4 Fast / Grok 4-1 Fast**: latency-optimized variants.
- **Grok 4.20 Multi-Agent API**: positioning headline on /api.
- **Grok Collections API**: RAG system.
- **Agent Tools API**: tool-calling API.
- **Grok Voice Agent API**: voice agent platform.
- **Grokipedia**: the company's encyclopedic property at [grokipedia.com](http://grokipedia.com).
- **Grok Business / Grok Enterprise / Grok Enterprise Vault**: tiered enterprise products.
- **xAI for Government / DOW (Department of War) / GSA OneGov**: government program.
- **Colossus**: the company's supercomputer / data center, currently 200K GPUs in Memphis, TN, with a roadmap to 1M GPUs.
- **Memphis**: the geographic / facility shorthand for Colossus (also the URL slug `/memphis`, suggesting an internal route page).
- **PromptIDE**: legacy 2023 development environment for prompt engineering.
- **Frontier Artificial Intelligence Framework**: xAI's published safety doctrine PDF.
- **HUMAIN, OneGov, KSA, El Salvador**: partner / customer references.
### How the brand refers to itself
- Lowercase "x" plus uppercase "AI" produces **xAI** (always one token, always with that case). Never "XAI" / "Xai" / "X AI."
- The Twitter handle for the corporate account is `@xaboratory`. a portmanteau of "x" plus "laboratory". a subtle research-lab gesture that doesn't surface elsewhere on the site.
- Email domains use `@x.ai` (`legal@x.ai`, `media@x.ai`, `safety@x.ai`, `vulnerabilities@x.ai`).
- xAI repeatedly clarifies it is **separate from X (formerly Twitter)** in legal copy ("Note: xAI is a separate company from X (formerly Twitter)") even though the two share the X-glyph and now both fall under SpaceX ownership.
- The acquired-by-SpaceX framing is presented as continuity, not transition: the news article ("xAI joins SpaceX") and the addition of "SpaceX" to the header nav are the only marks of corporate change.
---
## 9. Platform & Technical Notes
### CMS / platform
- **Next.js (App Router)**, evidenced by `_next/static/chunks/..`, `(main)/layout`, `(memphis)/layout`, the `__next_f.push` streaming flight payloads, and the `app/(main)/grok/page-9f5a2e5e7389397c.js` route segments. The build ID is `xW8fiUOQTqOFozjA33OVP`.
- **React Server Components / streaming**: `<!--$--><!--/$-->` boundary comments and the `$Sreact.fragment` flight payloads confirm RSC.
- **Tailwind CSS**: ubiquitous utility classes (`mx-auto`, `w-full`, `bg-background`, `text-primary`, etc.) plus the `prose prose-invert` plugin. Tailwind Typography, Tailwind Forms, and Tailwind Container Query plugins are likely in play.
- **Custom theme / design system**: see the `__variable_c1e5c9 __variable_d00f93 __variable_4de444 bg-background text-primary` body class. Three CSS variables define the typeface stack; semantic tokens include `colors.primary`, `colors.secondary`, `colors.background`, `colors.border`, `colors.accent`, `colors.steel`, plus `colors.primary/{10,25,50,80,85}%` alpha steps.
- **NUQS** (`NuqsAdapter` in the layout): URL search-param state library for client components.
- **`next-themes`**: the inline IIFE at the top of `<body>` reads `localStorage.theme || 'dark'`, attaches the class to `<html>`, and locks the color scheme. Hardcoded to `dark` with no system override.
- **Custom polyfills bundle**: `/_next/static/chunks/polyfills-42372ed130431b0a.js`.
### Theme
- Dark only (no light mode). The `dark` value is hard-coded in `("class","theme","dark","dark",..)`.
### Section / template patterns
- A handful of recurring section components: hero with full-svh, products grid (`gap-0 lg:grid-cols-3 lg:-space-x-px`), capability list (3-column horizontal), pricing tiles, news index row, prose container.
- `(main)` and `(memphis)` are two separate route groups, suggesting an alternate layout for the Memphis / Colossus content.
### URL patterns
- Top-level: `/`, `/grok`, `/api`, `/company`, `/colossus`, `/careers`, `/news`, `/contact`, `/safety`, `/security`, `/legal`, `/privacy-portal`, `/london`, `/memphis`.
- Nested products: `/grok/business`, `/grok/business/enquire`, `/grok/government`, `/grok/government/enquire`, `/api/voice`, `/api/imagine`.
- News articles: `/news/[slug]` with kebab-case slugs (`/news/grok-voice-think-fast-1`, `/news/grok-stt-and-tts-apis`, `/news/xai-joins-spacex`, `/news/grok-imagine-api`, `/news/series-e`, `/news/grok-business`, `/news/grok-collections-api`, `/news/us-gov-dept-of-war`, `/news/grok-voice-agent-api`, `/news/el-salvador-partnership`, `/news/grok-4-1-fast`, `/news/grok-goes-global`, `/news/grok-4-1`, `/news/onegov`, `/news/grok-4-fast`, `/news/grok-code-fast-1`, `/news/government`, `/news/grok-4`, `/news/grok-3`, `/news/series-c`, `/news/grok-1212`, `/news/grok-image-generation-release`, `/news/api`, `/news/grok-2`, `/news/series-b`, `/news/grok-1.5v`, `/news/grok-1.5`, `/news/grok-os`, `/news/prompt-ide`, `/news/grok`).
- Legal: `/legal`, `/legal/privacy-policy`, `/legal/terms-of-service`, `/legal/terms-of-service-enterprise`, `/legal/faq`, `/legal/faq-enterprise`, `/legal/help-center`, `/legal/acceptable-use-policy`, `/legal/brand-guidelines`, `/legal/cookie-policy`, `/legal/data-processing-addendum`, `/legal/europe-privacy-policy-addendum`, `/legal/subprocessor-list`.
- Career routes: `/careers`, `/careers/open-roles`.
- Off-site product properties: `https://grok.com`, `https://grok.x.com`, `https://grokipedia.com`, `https://shop.x.ai`, `https://docs.x.ai`, `https://console.x.ai`, `https://status.x.ai`, `https://trust.x.ai`, `https://hackerone.com/x`.
- App store: `https://apps.apple.com/app/apple-store/id6670324846?pt=126952307&ct=x.ai%20Direct%20Link&mt=8` and `https://play.google.com/store/apps/details?id=ai.x.grok&hl=en`. Apple App ID is `6670324846`. Google Play package is `ai.x.grok`. The campaign attribution token `pt=126952307&ct=x.ai Smart App Banner&mt=8` is consistent across pages.
### Third-party integrations
- **Mixpanel** for analytics, token `0b4055a12491884bcb6f34a5aa2718b6`, embedded in the layout's `WebsiteAnalyticsProvider` props.
- **Cloudflare** as edge / CDN. The Cloudflare beacon script is loaded with token `27a51fc7d1cd4058b900b2eea7bb7061`. Cloudflare WAF is referenced explicitly on /security.
- **Wiz** is referenced on /security as a "continuous threat detection" provider.
- **HackerOne** for vulnerability disclosure ([https://hackerone.com/x](https://hackerone.com/x)).
- **Apple Smart App Banner**: `<meta name="apple-itunes-app" content="app-id=6670324846, affiliate-data=pt=126952307&ct=x.ai%20Smart%20App%20Banner&mt=8"/>`.
- **AWS S3** is referenced in /security as the encryption-at-rest store ("encrypted at rest using server-side encryption with Amazon S3 managed keys (SSE-S3)").
- **No Google Tag Manager / GA / Segment** detected in the SSR HTML.
- **No CMP / OneTrust** banner detected (no cookie consent banner serves to default visitors).
### Performance observations
- Nine font files preloaded eagerly (`<link rel="preload" .. as="font" type="font/woff2" crossorigin="">`). This is aggressive font preloading and is the single biggest factor in the visual load experience.
- Four CSS files preloaded with `data-precedence="next"`.
- 30+ JS chunks listed in `<head>` as async, including a 38496 vendor bundle, multiple page-segment chunks, plus webpack runtime.
- Image strategy: `loading="lazy"` on non-hero, `webp` exclusively for content imagery, inline SVG for decorative artwork (no extra HTTP).
- Streaming HTML via React Server Components (the `__next_f.push` calls) reduces TTFB.
### SEO title patterns
- Homepage: `xAI: Understand the Universe`.
- Grok: `Grok. Truth-seeking AI Chatbot with Voice & Image Generation | xAI`.
- API: `API: Frontier Models for Reasoning & Enterprise | xAI`.
- Company: `Company: Accelerating Scientific Discovery | xAI`.
- Careers: `Careers: Build AI That Advances Humanity | xAI`.
- Colossus: `Colossus: The World's Largest AI Supercomputer | xAI`.
- News index: `News: Research, Product & Company Updates | xAI`.
- Contact: `Contact: Get in Touch with xAI | xAI`.
- Safety: `Safety | xAI`.
- Security: `Security: Data Protection & Trust | xAI`.
- Brand Guidelines: `Brand Guidelines | xAI`.
- News article: `Grok 4 | xAI`.
The pattern is `[Page topic]: [Specific descriptor] | xAI`, with the colon-separated descriptor doubling as a marketing claim ("World's Largest," "Truth-seeking," "Frontier Models for Reasoning & Enterprise").
### Meta description patterns
- Homepage: "xAI is an AI company building Grok. Our mission is to advance scientific discovery and understand the universe."
- Grok: "Learn about Grok, xAI's truth-seeking AI chatbot. Voice chat, image and video generation, real-time search, coding help, and advanced reasoning. on web, iOS, Android."
- Safety: "xAI remains committed to the safety of our models and products. Read more in our Frontier Artificial Intelligence Framework and our model cards."
OG description (consistent across most pages): "xAI builds Grok, an AI chatbot with voice chat, image and video generation, real-time search, and advanced reasoning. Try Grok at [grok.com](http://grok.com)."
### Legal / policy URLs
- `/legal/privacy-policy`, `/legal/terms-of-service`, `/legal/terms-of-service-enterprise`, `/legal/acceptable-use-policy`, `/legal/cookie-policy`, `/legal/data-processing-addendum`, `/legal/europe-privacy-policy-addendum`, `/legal/subprocessor-list`, `/legal/brand-guidelines`, `/legal/faq`, `/legal/faq-enterprise`, `/legal/help-center`. The Privacy Portal lives at `/privacy-portal`. Trust Portal at `https://trust.x.ai`.
### Accessibility notes
- `lang="en"` on `<html>`, `suppressHydrationWarning` on `<html>`.
- `aria-label` on the logo button, the textarea submit button, the hero textarea ("Submit a query to Grok").
- `<h1 class="sr-only lg:not-sr-only">` on /grok, exposing the H1 to screen readers and SEO at all breakpoints.
- Focus ring uses `outline-blue-500`.
- Touch hit-area expander on every button (described in section 5).
- Gradient text uses `bg-clip-text text-transparent`, which can be invisible to assistive tools that don't support the property; xAI mitigates this by ensuring the gradient text is decorative ("Understand The Universe") rather than load-bearing.
### Structured data
- No JSON-LD `@type=Organization` / `@type=WebSite` blocks observed in the SSR HTML for any page audited. xAI does not publish structured data, which is unusual for a brand of this scale.
- Open Graph metadata is present on every page (og:title, og:description, og:site_name, og:image, og:image:width/height, og:type).
- Twitter cards: `summary_large_image`, `@xaboratory` on both site and creator.
- Apple Smart App Banner declared.
- `<link rel="canonical">` on every page.
- `<link rel="icon">` only at 32x32 (no apple-touch-icon, no maskable / theme-color manifest).
---
## 10. Pages Scraped
A total of 13 distinct URLs were directly accessed and parsed for this audit, plus the master `/sitemap.xml` for URL discovery. Pages are grouped by page type below.
**Homepage**
- [https://x.ai](https://x.ai). Marketing homepage, dark hero, products grid, news feed, footer.
**Product / capability pages**
- [https://x.ai/grok](https://x.ai/grok). Grok consumer chat product PDP, full-length scroll with hero, capability cards, Grok Imagine gallery, multi-platform availability.
- [https://x.ai/api](https://x.ai/api). API PDP with capability matrix, enterprise features, model and pricing list, cost calculator.
- [https://x.ai/grok/business](https://x.ai/grok/business). Grok for Business audience PDP and pricing tiles plus enterprise inquiry form.
**Infrastructure / company narrative pages**
- [https://x.ai/colossus](https://x.ai/colossus). Supercomputer narrative with stats and timeline.
- [https://x.ai/company](https://x.ai/company). Mission, principles, offices, milestone timeline.
**Talent / hiring pages**
- [https://x.ai/careers](https://x.ai/careers). Hiring purpose, principles, benefits, featured roles, interview process.
**Editorial / news pages**
- [https://x.ai/news](https://x.ai/news). News index with 28+ article rows from November 2023 to April 2026.
- [https://x.ai/news/grok-4](https://x.ai/news/grok-4). Sample long-form blog post / model launch announcement (July 2025) with benchmark charts and embedded chat trace.
**Trust & safety pages**
- [https://x.ai/safety](https://x.ai/safety). Frontier AI Framework and model card links.
- [https://x.ai/security](https://x.ai/security). Trust statement, vulnerability reporting, product security details.
**Legal / brand pages**
- [https://x.ai/legal/brand-guidelines](https://x.ai/legal/brand-guidelines). Public brand mark usage guide, attribution rules, logo download CTA.
**Contact pages**
- [https://x.ai/contact](https://x.ai/contact). Direct contact channels (support, sales, X, Discord, media, safety).
**URL discovery (not parsed for content but used to map the site)**
- [https://x.ai/sitemap.xml](https://x.ai/sitemap.xml). XML sitemap exposing 60+ canonical URLs across all sections of the site.