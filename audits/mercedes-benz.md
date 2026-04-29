# Mercedes-Benz Brand Standards Audit, extracted from https://www.mercedes-benz.com and https://group.mercedes-benz.com across 14 pages (April 2026)

Mercedes-Benz operates two distinct but coordinated digital properties. The first, mercedes-benz.com, is the public Brand Experience hub, a curated, editorial site that emphasizes legacy, design, motorsport, vision concepts, and lifestyle, rather than the configure-and-buy flow that lives on regional dealer-facing sites. The second, group.mercedes-benz.com, is the corporate site of Mercedes-Benz Group AG, the parent listed entity that addresses investors, the press, regulators, and prospective employees. The two share a single design system (internally tokenized as "wb-" for Workbench, the Daimler / Mercedes-Benz design language), the same proprietary type families (MBCorpo Title, MBCorpo Text, with Daimler CAC / CS as fallback), the same color philosophy (deep black canvas, pure white type, restrained accents), and the same governing icon, the three-pointed star. They differ in editorial register. The brand experience hub is poetic, slow, and image-led. The group corporate site is institutional, plain-spoken, and obligation-led. Read together they form one of the most coherent multi-property brand systems in the global automotive industry. The audit below covers both, and treats them as a single brand standard.

## 1. Color Palette

The Mercedes-Benz palette is engineered around a single defining decision. The default canvas is true black, the default ink is pure white, and color is treated as a precision instrument rather than a decorative voice. Walk the site at scale and you find that most pages have only two surface colors and one ink color. Greys carry hierarchy. Blue carries function. Red, green, and yellow carry status. The palette never sells you. It frames the product.

### 1.1 Brand-defining canvas colors

The two anchor tokens that govern almost every page on mercedes-benz.com are exposed as `--base-color` and `--text-on-base-color`.

- `#000000`, `--base-color`, `--campaign-primary`, `--campaign-gradient`: pure black. The default page background on the Brand Experience site, the default backdrop for Maybach, AMG, EQS, the museum, and the entire vision/concept catalog. This is not "near black." It is true black. The decision is deliberate. On OLED displays the page disappears into the bezel and the vehicle photography reads like a darkroom print.
- `#ffffff`, `--text-on-base-color`, `--campaign-text`, `--campaign-light`: pure white. Used for body type, headlines, the three-pointed star wordmark, and most iconography.
- `#141414`, `--bg-on-base-color`: an "off-black" surface used for cards, modals, and tile interiors that need to lift slightly above the page. It registers as black to the eye but separates cleanly under HDR or bright ambient light.

The Mercedes-Benz Group corporate site inverts the relationship for most editorial pages. White becomes the canvas, black becomes the ink, and the dark mode is reserved for the global navigation bar and the announcement strip ("Announcement: 1st Quarter Results 2026."). The same two tokens drive both behaviors.

### 1.2 Grey scale (the workhorse)

The grey ramp is the heart of the system. Eight tokens carry almost every secondary surface, divider, and inactive state.

- `#f8f8f8`, `--wb-grey-95`: lightest tint, used for white-page section bands and large background washes on the Group site.
- `#f4f4f4`, `--wb-grey-90`: secondary tile background on light pages, table row stripes, footer divider blocks.
- `#9f9f9f`, `--wb-grey-60`, also exposed as `--hover-on-base-color` and `--link-on-base-color`: the most-seen mid-grey on the Brand Experience site. Footer copyright reads at this weight, language switcher inactive items read at this weight, and link hover states resolve here.
- `#767676`, `--wb-grey-45`: secondary footer text, captions, and the inactive item in the language switcher (DE next to active EN).
- `#696969`, `--wb-grey-40`: utility text, input placeholder.
- `#4f4f4f`, `--wb-grey-30`: muted body text in light mode.
- `#333333`, `--wb-grey-20`: secondary surface on light pages.
- `#262626`, `--wb-grey-15`: deep utility surface, used as a one-step lift above `#141414` in dark mode.

The grey ramp is monochromatic. There is no warm grey, no cool grey, no second neutral track. Every grey is a flat, equal-channel hex. That choice is what gives the page its photographic stillness. Grey never competes with the chrome and paint of the vehicles in the imagery.

### 1.3 Brand blue (function color)

Blue does not signal "Mercedes." Black does. Blue signals "this is interactive."

- `#0078d6`, `--button-theme-color`: the primary button hex on the Group corporate site. A medium azure. It reads as a system blue, deliberately neutral, almost Microsoft Fluent in temperature. Mercedes-Benz uses it for primary CTAs, "Apply now," "Read more," "Search jobs."
- `#014880`, `--theme-active`, `--wb-blue-25`: active and pressed state of the primary button.
- `#80c6ff`, `--theme-disabled`: disabled CTA blue, used at low contrast against `#0078d6`.
- `#008dfc`, `--wb-blue-50`: link blue at higher prominence, used in the press releases section of the Group site.
- `#036dc1`, `--wb-blue-40`: mid-stop on the blue ramp.
- `#0260ab`, `--wb-blue-35`: pressed state alternate.
- `#013c6b`, `--wb-blue-20`: deep blue, used for navigation hovers on light pages.
- `#003156`, `--wb-blue-15`: deepest blue, used for legal-page link emphasis.

Critically, the Brand Experience site (mercedes-benz.com) almost never uses blue in its hero or storytelling areas. Blue is reserved for utility moments, the search field, the language switcher, the cookie consent dialog. The brand voice on the experience site is black and white. Blue is the functional accent kept in reserve.

### 1.4 Status colors (functional only)

The system reserves three status hues, each ramped through six to nine tints. They appear on the Group corporate site and inside the Mercedes-Benz Owner / Service / Configurator flows, never inside the vehicle storytelling layer.

Reds (error, attention):
- `#ff9292`, `--wb-red-70`
- `#ff6e6e`, `--wb-red-60`
- `#821414`, `--wb-red-25`
- `#6d1111`, `--wb-red-20`
- `#410a0a`, `--wb-red-10`
- Tints `--wb-red-85`, `--wb-red-90` (`#ffdbdb`) sit at the high-tint end for soft alert backgrounds.

Greens (success, completed state):
- `#37ac45`, `--wb-green-55`
- `#90d198`, `--wb-green-75`
- `#bce3c1`, `--wb-green-85`
- `#d3edd6`, `--wb-green-90`
- `#e9f6ea`, `--wb-green-95`
- `#0f4d16`, `--wb-green-25`
- `#051a07`, `--wb-green-05`

Yellows (warning, attention without alarm):
- `#e8bd00`, `--wb-yellow-45`
- `#ba9700`, `--wb-yellow-35`
- `#fffae6`, `--wb-yellow-95`

The system is consistent in two ways. First, every status family is named on the same percentage scale (15, 20, 25, 35, 40, 45, 50, 55, 60, 70, 85, 90, 95). Second, the lightest tints (the 90s) are nearly always wash-soft, designed to sit behind black or coloured type without overwhelming it.

### 1.5 Co-emission and regulatory color

Mercedes-Benz is one of the few automotive brands that exposes a CSS token specifically for fuel-economy and emissions disclosures.

- `#606060`, `--co2-labeling-color`: the exact grey used for the WLTP energy-consumption and CO2-emissions footnotes that the European Union requires below every vehicle photograph. The tone is intentional, dark enough to be legally legible, light enough to not interrupt the editorial photography.

This is one of the more telling signals in the system. Mercedes-Benz has codified regulatory disclosure as a brand asset, not an afterthought.

### 1.6 Hover, focus, and motion-state colors

- `#9f9f9f`, `--hover-on-base-color`: the universal hover grey on dark pages.
- `#bbbbbb`, `--hover-on-theme-primary`: hover for primary CTA buttons that sit on top of campaign hero blocks.
- Animation curves: `cubic-bezier(.8, 0, 0, .8)` (`--ease-in-out-expo`) and `cubic-bezier(0, 0, .26, 1)` (`--ease-out-expo`). Motion is exponential, slow on entry, sudden on exit, which is consistent with the cinematic posture of the photography.

### 1.7 Color hierarchy and emotional role

Reading the palette as a system, the assignment is:

Black equals stage. White equals ink and chrome. Grey equals breathing room. Blue equals action. Red equals risk. Green equals progress. Yellow equals caution. The hero job is given to the absence of color. The vehicles, the headlights, the monochrome studio backgrounds, the photography is the chroma. Mercedes-Benz refuses to assign itself a "brand color" beyond black-and-white because doing so would make the vehicles compete with their wrapper. The palette is, in effect, a frame.

### 1.8 Deliberately absent colors

There is no orange, no magenta, no purple, no teal in the system. There is no warm beige or cream. There is no champagne or gold despite the brand's luxury position. There is no gradient-as-brand, the only gradients in the system are inside campaign-hero photo overlays and the announcement-bar transitions. The closest the brand comes to a "luxury color" is the soft platinum greyscale of `#f4f4f4` and `#f8f8f8` used on the Group corporate site. Even on the Maybach overview, the most expressive vehicle line in the portfolio, the canvas remains pure black.

---

## 2. Typography

Mercedes-Benz runs the most-deployed proprietary type system in the global automotive industry. Every page on the public brand resolves to one of two custom families. Both were commissioned for the brand and are self-hosted as woff2.

### 2.1 Font families in production

Confirmed live in production via `document.fonts`:

- **MBCorpo Title**, weight 400. The display face. A wide, low-contrast humanist serif-sans hybrid with a calligraphic spine. Used for every H1, H2, and large editorial headline on the Brand Experience site. The default fallback chain is `"MBCorpo Title", "DaimlerCAC-Regular", "DaimlerCACArab-Regular", serif`. This is the typeface most people associate with the modern brand voice (post-2020 corporate refresh).
- **MBCorpo Text**, weights 400 and 700. The body face. A neutral, slightly narrow geometric sans-serif. Used for body copy, navigation, captions, and footers. The default fallback chain is `"MBCorpo Text", "DaimlerCS-Regular", "DaimlerCSArab-Regular", sans-serif`.
- **DaimlerCAC-Regular** and **DaimlerCS-Regular**. Daimler's earlier in-house corporate Latin typefaces, retained as fallback / legacy support for older subdomains.
- **DaimlerCACArab-Regular** and **DaimlerCSArab-Regular**. Arabic-script siblings of the Daimler corporate face, used on the Arabic regional sites without changing brand voice.
- **Hanyi** and **Hanyi-Ext**, weight 400. Chinese-script siblings, used on the Chinese regional sites.
- **FKGroteskNeue**, retained as a transitional fallback (a commercial neo-grotesque widely deployed on Mercedes properties before the MBCorpo rebrand).

The fact that the same brand voice carries across Latin, Arabic, and CJK with hand-drawn sibling families (Daimler CAC Arab, Hanyi) is a signal of how seriously Mercedes-Benz takes typographic consistency at global scale. Most automotive brands lean on a single Latin face and let third-party CJK fall in. Mercedes-Benz commissioned its own.

### 2.2 Typographic scale (observed in computed styles)

Headline scale on the Brand Experience site:

- Display giant (one-off, used in concept-car heroes): 120px / weight 400 / MBCorpo Title. Observed on Vision One-Eleven hero "Shape of a top athlete."
- Display extra-large: 80px / weight 400 / MBCorpo Title. Observed on Vision One-Eleven section headlines.
- Display large: 72px / weight 400 / MBCorpo Title. Observed on Vision EQXX hero "Bringing maximum electric efficiency to the road," Vision One-Eleven hero "An icon reenvisioned, the new Vision One-Eleven," Sustainability hero "Sustainability.", Innovation hero "Innovation.", Classic news hero "News & Events in Classic."
- Display medium: 64px / weight 400 / MBCorpo Title / line-height 80px. Observed on the homepage "World premiere of the all-new electric C-Class," and as a sub-headline scale on concept-car deep dives.
- Display social: 64px / weight 400 / MBCorpo Title / line-height 72px. Observed on every "Follow Mercedes-Benz" social-media-box on every page.

Headline scale on the Group corporate site:

- Section title: 48px / weight 400 / MBCorpo Title. Observed on "Company.", "Technology.", "Sustainability.", "Careers.", "Investors.", "Job search.", "Holiday jobs.", "About us."
- Subsection title: 34px / weight 400 / MBCorpo Title. Observed on "More Information."
- Module heading: 32px / weight 400 / MBCorpo Title.
- Card heading: 18.72px / weight 700 / MBCorpo Text. Observed on "Corporate Governance," "Autonomous Driving," "Environment & Climate," "Resources & Circularity," "Society & Governance," and the press / careers / divisions card grid.

Body scale across both properties:

- Body lead: 18px / weight 400 (sometimes 700 for emphasized lead) / MBCorpo Text. Observed on Vision EQXX intro paragraph.
- Body default: 16px / weight 400 / MBCorpo Text / line-height 22px.
- Body small: 14px / weight 400 / MBCorpo Text / line-height 22px. Used for footer copyright, language switcher, navigation utility links, and all WLTP regulatory disclaimers.

Footer header: 18px / weight 700 / MBCorpo Text / line-height 18px. Tight line-height creates a deliberate "list block" appearance.

### 2.3 Typographic posture

A few patterns are unmissable:

Every section headline on the Brand Experience site ends in a period. "Sustainability." "Innovation." "Careers." "News & Events in Classic." The period is not a typographic accident, it is a voice choice. It signals finality, authority, and the closing of an idea. It also slows the reader. Mercedes-Benz headlines rarely run more than one or two clauses, and the period turns each headline into a near-haiku statement.

Display headlines are set in MBCorpo Title at weight 400. Mercedes-Benz almost never bolds its display type. The face itself carries enough visual weight at 64px and above that a 700-weight cut would tip into shouting. The reserve is the brand voice.

Body type is set in MBCorpo Text at weight 400 with weight 700 used sparingly for emphasis or lead-in copy. There is no italic. There is no underline outside of inline links.

Letter-spacing is normal across the system (`letter-spacing: normal` is the observed default on every headline tested). Mercedes-Benz does not "track-out" its display type, which is a common automotive trope. The face is wide enough to read open by default.

Text-transform is none across the system. Mercedes-Benz does not all-caps its headlines or its CTA buttons. Even the navigation reads in mixed-case ("Vehicles," "Innovation," "Sustainability"). This is a quiet but consistent rejection of the "ALL CAPS LUXURY" trope used by most competitors.

### 2.4 Typographic hierarchy by page archetype

On a vehicle storytelling page (Maybach, EQS, Vision concepts):
- 64–120px display title in MBCorpo Title sets the editorial frame.
- 18px body lead in MBCorpo Text introduces the story.
- 64px sub-headlines in MBCorpo Title break the narrative into chapters.
- 16px body copy fills out each chapter.
- 14px MBCorpo Text caption / footnote handles WLTP regulatory disclosure.

On a corporate page (Group site, Sustainability, Careers, Investors):
- 48px section title in MBCorpo Title leads each block.
- 18.72px / weight 700 MBCorpo Text powers the navigation card grid.
- 16px MBCorpo Text body fills supporting prose.
- 14px MBCorpo Text grey #767676 for legal copy and registry numbers.

---

## 3. Logo and Wordmark

### 3.1 The three-pointed star

The Mercedes-Benz mark is one of the oldest in the global automotive industry. The three-pointed star, registered in 1909, has been the brand's primary identifier for more than a century. Every public-facing Mercedes-Benz property uses the star as its mast logo, and the structured-data schema on every page declares the canonical asset path.

- Primary asset: `/logos/mb-star-white.svg` (declared in the `Organization` schema.org JSON-LD on every page).
- Variant: a black-on-white version used on the Group corporate site's light pages.
- Behavior: the star is rendered as a flat, single-color SVG. It is not gradient-filled, not embossed, and not animated. The three points represent the brand's historic ambition for "motorisation on land, on water, and in the air." This story is implied, never narrated.

The star is allowed to stand alone, as it does in the global header on every brand-experience page. It is also allowed to lock up with a "Mercedes-Benz" wordmark, which is the form used for product packaging, dealer signage, vehicle badging, and corporate documents.

### 3.2 The Mercedes-Benz wordmark

The wordmark "Mercedes-Benz" is set in MBCorpo Title weight 400, sentence case, with the hyphen tight. The wordmark is locked up with the star at a fixed left-of-mark position when both are present. The wordmark has no descenders (other than the hyphen), which allows the lockup to optically center against the star's apex.

### 3.3 Lockup posture by surface

- Global header on mercedes-benz.com: the star alone, centered, 72px tall on desktop, set inside a brandhub-header web component.
- Footer: the star is not repeated in the footer of mercedes-benz.com. The footer reads as a flat sitemap with the copyright line "© 2026 Mercedes-Benz AG." set in `#9f9f9f` MBCorpo Text 14px.
- Corporate site mast: the star plus the "Mercedes-Benz" wordmark plus the word "Group" in a horizontal lockup. The "Group" suffix is set in MBCorpo Title at the same x-height as the wordmark, separated by a thin spacing rule.

### 3.4 Sub-brand wordmarks

Mercedes-Benz operates an unusually disciplined sub-brand architecture. Each sub-brand has its own typographic treatment but always remains under the same star.

- **Mercedes-AMG**: the AMG mark is a stand-alone red-and-black emblem (the "Affalterbach laurel"). When co-branded with Mercedes-Benz, AMG is set in MBCorpo Title and locked under the star.
- **Mercedes-Maybach**: the Maybach double-M emblem is reserved for vehicle badging. In digital, "Mercedes-Maybach" is set in MBCorpo Title weight 400 with no decoration.
- **Mercedes-EQ**: the electric sub-brand uses "EQS," "EQE," "EQB," etc., all set in MBCorpo Title.
- **Mercedes-Benz G-Class**: the G mark and the wordmark "G-Class" share the same MBCorpo Title face.
- **SILVER ARROWS**: an enthusiast-program brand referenced in the footer, set in all-caps small label.

### 3.5 Asset hygiene

The brand insists on a single source of truth. Every page on mercedes-benz.com declares the same `/logos/mb-star-white.svg` path. There is no PNG fallback, no fallback raster. The site relies on SVG only, which keeps the star crisp at every scale. The Akamai pixel (`/akam/13/pixel_*`) confirms the property is served behind Akamai Image Manager for global-edge consistency.

---

## 4. Layout and Grid System

### 4.1 The 12-column grid

The Mercedes-Benz design system is built on a 12-column grid with an explicit content-width cap. The relevant tokens, observed live in computed styles:

- `--wb-grid-content-width: 86vw` (the page content uses 86 percent of the viewport width on most breakpoints).
- `--wb-grid-width: min(86vw, 1680px)` (the grid never exceeds 1680px regardless of screen size).
- `--wb-grid-gutter-width: 2.5rem` (40px between columns).
- `--wb-grid-column-width: min(calc((86vw - 11 * 2.5rem) / 12), 103.3333333333px)` (columns cap at ~103px each).

The math is precise. On a 24" desktop monitor (~1920px), the grid centers within the viewport at 1680px max, 12 columns at ~103px each plus 11 × 40px gutters, leaving a calm margin of ~120px on each side. On a smaller laptop, the grid scales fluidly to 86vw of the viewport, columns shrink proportionally, and gutters stay at 40px until a sub-breakpoint kicks in.

### 4.2 Spacing scale

The system uses a single named-step spacing scale. Observed tokens:

- `--wb-spacing-3xs: .25rem` (4px)
- `--wb-spacing-xxs: .5rem` (8px)
- `--wb-spacing-xs: 1.5rem` (24px)
- `--wb-spacing-s: 2rem` (32px)
- `--wb-spacing-l: 4.5rem` (72px)
- `--wb-spacing-xl: 5.5rem` (88px)
- `--wb-spacing-xxl: 6rem` (96px)

The spacing curve jumps disproportionately at the large end. The system includes 4px, 8px, 24px, 32px, but then leaps to 72px, 88px, and 96px. This is a deliberate design move. Small tokens are for component internals (button padding, icon gaps), and large tokens are for editorial breathing room between hero, section, and footer. There is almost no medium-spacing usage in the wild. Sections are either tightly packed or generously spaced. The middle is intentionally avoided.

### 4.3 Hero block geometry

Hero modules are full-bleed by default. The viewport renders edge-to-edge media (vehicle photography or video), with a single MBCorpo Title headline rendered at 64–120px set against the media. Headlines align to the 12-column grid's left edge, typically spanning columns 2 through 7 on desktop and 2 through 11 on mobile. The visual hierarchy is photography first, type second, button third, with a high-contrast white-on-black or black-on-white treatment depending on canvas.

### 4.4 Section rhythm

The standard section rhythm on a vision / concept-car page is:

1. Full-bleed hero (1080–1280px tall on desktop).
2. 18px body lead, set inside the 6-column-wide content lane (columns 4 through 9 of 12).
3. Two-up tile pair (6 columns each) introducing a chapter.
4. Full-bleed editorial photo break.
5. Three-up grid tile (4 columns each) for supporting features.
6. Full-bleed video trailer.
7. "Follow Mercedes-Benz" social-media-box (10 columns wide, centered).
8. Footer sitemap.

This rhythm is consistent across the Vision EQXX, Vision One-Eleven, Iconic Concept AMG GT XX, and Maybach pages. The brand uses repetition deliberately, the user moves from page to page on autopilot because the structure is predictable, and the imagery and copy carry the differentiation.

### 4.5 Border radius

The system exposes only four radius values:

- `--wb-radius-s: 2px` (input fields, small chips)
- `--wb-radius-m: 4px` (cards, buttons)
- `--wb-radius-l: 8px` (modals, hero overlays)
- `--wb-radius-full: 50%` (avatars, share-icon circles)

Mercedes-Benz does not use heavy rounding. The brand sits firmly in a low-radius, near-rectilinear posture. This pairs with the photography, vehicles are presented in clean, geometric studio shots, and the UI mirrors that geometry.

### 4.6 Shadow

Shadows are universally subtle. The three observed tokens:

- `--wb-shadow-s: 0 0 2px 0 rgba(0,0,0,.1), 0 2px 4px 0 rgba(0,0,0,.1)`
- `--wb-shadow-m: 0 0 2px 0 rgba(0,0,0,.1), 0 4px 8px 0 rgba(0,0,0,.1)`
- `--wb-shadow-l: 0 0 4px 0 rgba(0,0,0,.1), 0 16px 24px 0 rgba(0,0,0,.1)`

Every shadow is at 10% black opacity, never higher. Shadows are reserved for cards and modals on the white-canvas Group site. The Brand Experience site (black canvas) almost never uses shadow because the canvas is too dark for shadow to register.

### 4.7 Breakpoints (inferred)

Mercedes-Benz's design system targets four primary breakpoints, inferred from layout shifts in the live DOM:

- Mobile: 0–599px (single-column stack, 86vw content lane).
- Tablet: 600–1023px (two-column grid for tile pairs).
- Desktop: 1024–1679px (full 12-column grid, content scales fluidly to 86vw).
- Wide: 1680px and above (grid caps at 1680px, viewport margin grows).

The Akamai pixel and structured data are identical across breakpoints, which confirms the same source HTML is served regardless of viewport.

---

## 5. UI Components

### 5.1 Buttons

The primary CTA button on the Brand Experience site is rendered as a transparent or `rgba(0,0,0,0)` background with a 1px white border, white MBCorpo Text label at 14px, and 16px horizontal padding. On hover the background fades to `--hover-on-base-color` (`#9f9f9f`) at 10% opacity. On active state the background fills to `--theme-active` (`#014880`).

The primary CTA on the Group corporate site is a solid button, `--button-theme-color` (`#0078d6`) background, white MBCorpo Text label at 14px weight 400, with 16px / 4px-radius geometry. Hover state is `#bbbbbb` overlay. Disabled state is `#80c6ff`. Active state is `#014880`.

There are two secondary button patterns. The first is a "ghost" button, transparent background with grey text and a 1px grey border, used for tertiary "Read more" links inside card grids. The second is a flat text link with a chevron, used inline within body copy.

There is no rounded-pill button anywhere on either property. All buttons resolve to 4px corner radius. This is a deliberate brand choice. Mercedes-Benz reads as architectural, not pharmaceutical.

### 5.2 Cards

Card components are uniformly minimal. The Brand Experience site uses three card archetypes:

1. **Editorial tile**: full-bleed photograph fills the card, headline and subhead overlay the bottom-left corner in MBCorpo Title 32px and MBCorpo Text 16px, set in white. No card border. No rounded corners (just the system 4px).
2. **News teaser**: photograph at the top (16:9 aspect), MBCorpo Title 24px headline, MBCorpo Text 16px description, all left-aligned with 16px internal padding.
3. **Concept-car module**: full-bleed photograph as background, no overlay, headline appears below the card on hover or on tap.

The Group corporate site uses a card grid where each card is a single capability area (Corporate Governance, Autonomous Driving, etc.) rendered as a 4-column tile with 18.72px MBCorpo Text 700 headline, no subhead, and a full-bleed photograph behind. Hovering reveals a "Learn more" inline link.

### 5.3 Navigation

Both properties use a fixed top navigation bar. Implementation differs by web-component family.

The Brand Experience site uses a custom-element architecture: `brandhub-header`, `brandhub-language-switcher`, `brandhub-language-switcher-item`, `brandhub-main-navigation`, `brandhub-main-navigation-item`, `brandhub-sub-navigation-item`, `brandhub-search-link-list`, `brandhub-search-link-list-item`. Each component renders its own shadow DOM. Navigation labels are set in MBCorpo Text 14–16px, weight 400, white on black. The hover state is `#9f9f9f` grey. The mega-menu drawer slides in from the top, occupies the full viewport, and lists the 12 main category groups with their sub-navigation.

The Group corporate site uses a flatter, more conventional global header. The same MBCorpo Text type carries through, but the structure renders as a standard horizontal menu without web-component encapsulation. The nav bar is solid black, hovers reveal a dropdown panel underneath.

The footer pattern is shared. Both sites use a `brandhub-footer-sitemap` web component that renders four columns titled "Experience," "Purchase," "Login," and "Learn." Each column header is rendered as MBCorpo Text 18px weight 700 white. Items inside each column are MBCorpo Text 14px weight 400 grey `#9f9f9f`.

### 5.4 Form fields

Form fields are observed only on the cookie consent dialog and the search overlay. Both follow the same pattern:

- Input background: `#141414` on dark canvas, `#f4f4f4` on light canvas.
- Border: 1px `#9f9f9f` grey, transitioning to `#0078d6` blue on focus.
- Border radius: 2px (`--wb-radius-s`).
- Label: MBCorpo Text 14px placed above the field.
- Placeholder: MBCorpo Text 14px grey `#696969`.
- Error: 1px border `#ff6e6e` (`--wb-red-60`) with error message underneath in `#ff6e6e` MBCorpo Text 12px.

### 5.5 Stage components (the editorial spotlight)

The most-used component on the Brand Experience site is `brandhub-stage` and its child `brandhub-stage-item`. This is the full-bleed hero unit. It renders one or more stage items with edge-to-edge photography or video, a single H1 in MBCorpo Title (64–80px), an optional MBCorpo Text 16px subline, and one or two CTA buttons. The stage carousel auto-advances on a slow timer (cubic-bezier ease-out-expo).

### 5.6 Teaser components

`brandhub-teaser-tiles` and `brandhub-teaser-list` render grid layouts of 2-up, 3-up, or 4-up tiles. Tiles are uniformly 4:3 or 16:9 aspect ratios. Each tile carries a short caption in MBCorpo Text 16px and an inline-link CTA. Hover treatment is a subtle 5% opacity black overlay plus an arrow chevron that animates 4px to the right.

### 5.7 Editorial highlight components

`brandhub-editorial-highlight` is a magazine-style block that pairs a long-form pull quote with a portrait photograph. Quotes are set in MBCorpo Title 34px, italic-feeling but actually upright (the MBCorpo Title face has enough calligraphic energy to read as italic without being slanted). Attribution is set in MBCorpo Text 14px weight 700.

### 5.8 Video trailer components

`brandhub-video-trailer` is the brand's auto-playing hero video module. It defaults to muted, with a static caption in MBCorpo Title 64px and a small "play" affordance in the lower-right corner. Cookie consent for YouTube is required to view, signaled with a "YouTube (advertising) consent required!" overlay in MBCorpo Title 34px. The site explicitly lists this consent prompt as part of the brand experience, not a separate compliance UI.

### 5.9 Social media box

`brandhub-social-media-box` and its child `brandhub-social-media-box-item` render the standard "Follow Mercedes-Benz" call-out at the bottom of every editorial page. The H2 "Follow Mercedes-Benz" is set in MBCorpo Title 64px / weight 400 / line-height 72px / black ink. Below it sits a row of platform icons (Instagram, Facebook, X, YouTube, LinkedIn, TikTok) rendered as 48px circular wb-radius-full chips with subtle 1px borders.

### 5.10 Cookie consent dialog

The cookie consent dialog is one of the few pieces of UI that deviates from the brand's editorial calm. It renders as a near-fullscreen modal with H1 "The Mercedes-Benz AG uses cookies for various purposes." in MBCorpo Title 29.75px (note the unusual exact size, an artifact of `1.86rem` math). Below sits a four-button row, "Accept all," "Decline non-essential," "Settings," and "Privacy policy." The modal is functional, regulatory, and intentionally not photogenic.

---

## 6. Iconography

### 6.1 Icon system

Mercedes-Benz uses a custom-drawn line-icon set. Icons are uniformly:

- 24×24px artboard.
- 1.5px stroke weight.
- Rounded line-cap and line-join.
- Single color (white on dark, black on light).
- No two-tone, no fill-and-stroke combinations, no perspective.

Icons appear in the global navigation (search, menu, language), in the footer (social platforms), and inline within editorial copy as small chevrons and arrows.

### 6.2 The chevron and the arrow

The most-used motion-affordance icon is the right-pointing chevron, used as a "continue reading" / "learn more" cue. It animates 4px to the right on hover. The chevron is drawn as a 6×12px stroke-only glyph at 1.5px weight, with a rounded endpoint.

The full arrow appears in CTA buttons inside editorial heroes, drawn at 16×16px with the same line treatment, often with a subtle 200ms fade-in delay (`--fade-in-delay`) keyed to the page-load timeline.

### 6.3 Functional vs. decorative

Mercedes-Benz draws a hard line. Icons are functional only. There is no decorative-icon vocabulary in the way that a SaaS brand might use illustrated spot icons. Even on the Sustainability and Innovation overview pages, where competitors lean heavily on stylized illustrations, Mercedes-Benz uses photography exclusively.

### 6.4 Social platform icons

Platform icons in the social-media-box are the platform-canonical glyphs (Instagram camera, X-twitter X, YouTube play-button, LinkedIn "in," TikTok music-note, Facebook "f"). They are rendered as 24×24px white SVGs inside 48px circular wb-radius-full chips with 1px white borders.

### 6.5 Vehicle-specific icons (MBUX and concept-car overlays)

Inside the vehicle storytelling layer, particularly Vision EQXX and the EQS / MBUX Hyperscreen pages, Mercedes-Benz shows a small set of in-vehicle UI icons. These are drawn at the same 1.5px stroke weight but at 32×32 or 40×40 artboard. They appear with a soft `--fade-in-delay-labeling: 2750ms` delay, reinforcing the editorial slow-reveal posture.

### 6.6 The three-pointed star as iconographic anchor

The star is the only "decorative" icon in the system. It appears as a watermark on press releases, as a slow-breathing animation on the Innovation hero, and as a static lockup in every nav bar. The star is treated as a typographic glyph, not an illustration. It is the period at the end of the brand's sentence.

---

## 7. Photography and Illustration Style

### 7.1 The studio lookbook

Mercedes-Benz photography is dominated by a single, instantly recognizable aesthetic, the chrome-and-paint studio shot. Vehicles are placed against pure-black or pure-grey infinity backgrounds, lit from above and behind to throw a soft rim onto the bodywork, and captured at three-quarter or pure-profile angles. Reflections on the bodywork are deliberate. The photography is meant to look like the product is sitting inside a dream.

### 7.2 The road-trip / landscape register

A second register is reserved for editorial storytelling. The Vision EQXX page documents a real journey from Sindelfingen to Cassis, more than 1,000 kilometres on a single charge. The photography here pivots, the studio is replaced by Provence light, the chrome is replaced by dust on the lower body, and the human pilots are visible inside the cabin. The brand uses this register to humanize moments of technical achievement. The studio sells the object. The road sells the proof.

### 7.3 The architectural register

Inside the Mercedes-Benz Museum and the Mercedes-Benz Studios pages, the photography becomes architectural. Long-exposure interior shots, low-angle staircase frames, and exterior dawn light shots dominate. The architecture is the photography. This register reinforces the brand's claim to permanence.

### 7.4 The portrait register

For corporate-leadership photography on the Group site, Mercedes-Benz uses a flat, three-quarter portrait at studio key light. The Board of Management appears in clean white-shirt or dark-suit attire against a pure black or pure grey background. The portraits are deliberately modest, low contrast, low drama, and high formality.

### 7.5 The composite-illustration register (limited)

Illustration is rare. The only consistent illustrated element is the brand's heritage timeline on the corporate-history pages, where archival sketches and original blueprints are inlined alongside contemporary photography. The brand resists the temptation to create stylized infographics.

### 7.6 Color treatment of imagery

Mercedes-Benz photography is graded toward a cool, slightly desaturated finish. The blacks crush gently. The highlights are protected from clipping. The skin tones lean cool. The vehicle paint is treated with high specularity. The result is photography that integrates seamlessly with the deep-black canvas of the site, the imagery sits inside the page rather than on top of it.

### 7.7 Video posture

Video is hero, not garnish. The Vision EQXX page, the Vision One-Eleven page, and the Iconic Concept AMG GT XX page each lead with a brand film. The films are typically 60–90 seconds, scored with low-tempo orchestral or ambient electronic music, and built around long takes of the vehicle in motion. There is almost never a voiceover. Title cards appear in MBCorpo Title 64px white, locked to the lower-left corner.

### 7.8 What the brand will not photograph

There is no stock photography on either property. There are no group shots of generic "diverse business teams" inside an office. There are no overhead-flat-lay product shots. There are no "lifestyle moments" with a couple laughing into the distance. Mercedes-Benz refuses every cliche of the auto-OEM lifestyle library. The result is a photography library that is unmistakably theirs.

---

## 8. Brand Voice and Language Style

### 8.1 The opening posture

The opening line of every important Mercedes-Benz storytelling page is a single declarative sentence in MBCorpo Title at 64–120px. The sentence ends in a period. It does not ask a question. It does not pose a hypothetical. It states a fact.

Examples observed live:
- "World premiere of the all-new electric C-Class."
- "Bringing maximum electric efficiency to the road."
- "An icon reenvisioned, the new Vision One-Eleven."
- "The captivating one-bow design."
- "Pairing aerodynamic efficiency with..."
- "Sustainability."
- "Innovation."
- "Careers."

The voice begins with the conclusion, not the build-up. Mercedes-Benz never asks the reader to follow it to a punchline. It states the punchline and lets the reader catch up.

### 8.2 The body register

Body copy is composed in long, formal sentences with low-drama vocabulary. The cadence is closer to a museum wall card than to a brochure. A representative example, from Vision EQXX:

"The journey to electric mobility is as exhilarating as it is challenging, as unknown as it is certain. For Mercedes‑Benz, the route map is clear, maximum efficiency through innovation."

The structure is parallel construction (`as X as it is Y`) followed by a comma-bound conclusion. The brand uses parallelism to convey balance, and the comma bridge instead of a dash to slow the cadence. Mercedes-Benz almost never uses a dash for stylistic emphasis. It uses periods and commas.

Another representative example, from Vision One-Eleven:

"The one-bow design of the Mercedes‑Benz Vision One-Eleven is where form and function unite in perfect balance. This visionary concept car showcases a seamless blend of..."

The vocabulary is formal but not academic. Words like "captivating," "innovative," "seamless," "visionary," "thoughtfully," "uncompromising," and "iconic" recur. The brand does not chase neologism. It also does not retreat into corporate jargon.

### 8.3 The "class is in everything we do" tagline

The Innovation hub leads with: "Here at Mercedes-Benz, class is in everything we do." This is the post-2020 brand tagline (re-released around the centennial of the Mercedes-Benz brand in 2026). It is a deliberate double-meaning, "class" as "vehicle class" (S-Class, E-Class, C-Class, G-Class) and "class" as "the quality of being classy." The tagline is used sparingly. It does not appear on every page. When it does appear, it sits as an editorial pull quote, never as a marketing stamp.

### 8.4 The emotional register

The voice is calm, restrained, and confident. There is no exclamation. There is no urgency. There is no "act now" or "limited time" energy. Even on the Configurator and Test Drive entry points, the language is invitational, "Book a test drive," "New cars," "Configurator." The brand never raises its voice.

### 8.5 The technical-disclosure register

A separate, distinctly different register handles regulatory disclosure. Below every electric or combustion vehicle photograph appears a footnote, set in `--co2-labeling-color` (`#606060`) MBCorpo Text 14px:

"The stated values were determined in accordance with the prescribed WLTP (Worldwide harmonised Light vehicles Test Procedure) measurement procedure. The ranges given refer to the German market. The fuel consumption, energy consumption and CO₂ emissions of a car depend not only on the efficient use of the fuel or energy source by the car, but also on driving style and other non-technical factors."

The voice of the disclosure is procedural, accurate, and obligatory. It does not soften the brand and the brand does not try to soften it. The dual register (editorial above, disclosure below) is a pattern the system enforces consistently.

### 8.6 Vocabulary patterns

Common verbs: "to redefine," "to envision," "to elevate," "to shape," "to inspire," "to lead," "to drive." The verbs are aspirational without being grandiose.

Common adjectives: "iconic," "visionary," "uncompromising," "captivating," "luxurious," "intelligent," "personalised" (UK spelling on the international site). The adjectives carry weight.

Common nouns: "design," "innovation," "experience," "moment," "journey," "intelligence," "icon." The nouns are abstract enough to be reused across product lines.

Notable absences. The brand voice almost never uses: "we," "our team," "exciting," "amazing," "incredible," "next-generation," "revolutionary," "game-changing." The voice resists the SaaS-marketing vocabulary entirely.

### 8.7 The headline-period as a voice device

Every major section heading on the Brand Experience site ends in a period. This is the most distinctive single piece of typographic voice the brand operates. It signals authority. It also signals that each section is a closed argument. The reader is not being invited into a debate, they are being shown a position.

### 8.8 Voice in the corporate register (Group site)

The Group corporate site shifts into a flatter, plainer register. Headlines on the Group site are still period-terminated ("Company.", "Technology.", "Sustainability.", "Careers.", "Investors.") but body copy becomes more direct, more technical, and more disclosure-heavy. Press releases lead with date-stamped, location-stamped paragraphs in the manner of Reuters or Bloomberg. The investor-relations sections speak in EBIT margins and segment results. The Sustainability framework is structured around five named pillars: Corporate Governance, Autonomous Driving, Environment & Climate, Resources & Circularity, Society & Governance. Each pillar carries an annual report attachment.

### 8.9 Voice across regions

The Mercedes-Benz brand voice is engineered to translate. Arabic-script regional sites use the same period-terminated headline pattern with the Daimler CAC Arab face. Chinese-script regional sites use Hanyi for display and the same period-terminated headline pattern. The English copy on mercedes-benz.com follows UK orthography ("personalised," "kilometres," "centre"), which is the brand's global default.

### 8.10 The signature-line patterns

Recurring brand signature phrases observed in the wild:

- "Lead in intelligence."
- "Technology that cares."
- "Mercedes-Benz Brand Experience."
- "World premiere of..."
- "An icon reenvisioned..."
- "Class is in everything we do."
- "Make e-mobility a Mercedes-Benz moment."
- "Discover a new design era."
- "140 Years of Innovation."

Each is structured as a complete sentence or a sentence-fragment with a period. None of them ends in an exclamation point.

---

## 9. Platform and Technical Notes

### 9.1 Architecture

The Brand Experience site (mercedes-benz.com) is a custom-built web-component application. Every editorial primitive is a native Web Component (`brandhub-header`, `brandhub-stage`, `brandhub-teaser-tiles`, `brandhub-editorial-highlight`, `brandhub-video-trailer`, `brandhub-social-media-box`, `brandhub-footer-sitemap`, `brandhub-overview-stage`, `brandhub-teaser-list`). Each component renders into its own shadow DOM, which keeps the brand's styling system encapsulated and prevents page-level CSS leakage. The lift required to extract a page's content via DOM scraping (the audit you are reading required walking through more than ten layers of shadow root nesting) is itself a brand signal, the front-end engineering team has invested in encapsulation as a structural value.

The Group corporate site (group.mercedes-benz.com) is a more conventional server-rendered application without web-component encapsulation. Both share design tokens, type files, and the visual system.

### 9.2 Performance and delivery

- Edge: Akamai. Every page returns an Akamai pixel (`/akam/13/pixel_*`) for edge analytics. Image optimization is handled through Akamai Image Manager.
- Fonts: self-hosted woff2 (`MBCorpo Title`, `MBCorpo Text`, `DaimlerCAC-Regular`, `DaimlerCS-Regular`, `DaimlerCACArab-Regular`, `DaimlerCSArab-Regular`, `Hanyi`, `Hanyi-Ext`).
- Video: gated YouTube embeds with explicit consent overlays.
- Structured data: schema.org `Organization` JSON-LD on every page declaring `name: "Mercedes-Benz"`, `legalName: "Mercedes-Benz AG"`, `url: "https://www.mercedes-benz.com"`, `logo: "/logos/mb-star-white.svg"`.
- Breadcrumb structured data uses `BreadcrumbList` schema.

### 9.3 Internationalization

The site is served in dozens of regional / language variants. The brand operates a single design system across all of them, with per-region typeface fallbacks. The English-language international site uses UK orthography. The Arabic site uses Daimler CAC Arab. The Chinese site uses Hanyi. The DE / EN language switcher in the header uses MBCorpo Text 14px / line-height 22px / `#9f9f9f` for inactive and `#ffffff` for active.

### 9.4 Accessibility

Color contrast on the dark canvas (white on `#000000`) exceeds WCAG AAA at all body sizes. The grey link color `#9f9f9f` on `#000000` falls just below WCAG AA for body text (contrast ratio ~4.13:1 against 4.5:1 minimum). This is a known compromise in the system, the brand prioritizes the editorial quiet of the grey-on-black palette over WCAG AA on lower-priority utility links.

Headings follow a strict semantic hierarchy. H1 once per page, H2 for section headings, H3 for footer column headings, H4 for sub-section breakouts inside concept-car pages. The web-component shadow roots add a layer of complexity for screen readers, but each component exposes the right semantics through its slotted content.

### 9.5 Cookie and consent

The cookie consent dialog is a near-fullscreen modal that appears on first visit. It uses the same MBCorpo Title face and the same #0078d6 button-theme color. The consent flow distinguishes between essential, comfort, and advertising / analytics categories. Video and YouTube embeds require an explicit second-tier consent, and the brand renders an in-place "YouTube (advertising) consent required!" overlay rather than auto-loading the embed.

### 9.6 Responsive image strategy

Images are served via Akamai Image Manager with format negotiation (avif, webp, jpg) and responsive `srcset` attributes that target the four breakpoints described in Section 4. The brand uses the `<picture>` element with art-direction for hero modules, swapping landscape compositions on desktop for portrait or square crops on mobile.

### 9.7 Structured-data and SEO

Every page exposes:
- `<title>` matching the editorial headline ("Innovation," "Sustainability," "VISION EQXX, the most efficient Mercedes-Benz ever built").
- `<meta name="description">` set per page.
- `Organization` JSON-LD for the brand.
- `BreadcrumbList` JSON-LD for navigation hierarchy.
- Open Graph and Twitter card metadata for social sharing, with the Mercedes star as default share image.

### 9.8 Analytics and observability

Akamai handles edge logging. The brand also deploys Adobe Analytics (legacy from the Daimler era) on both properties. There is no third-party A/B testing tag observed on the public pages, which suggests the brand runs experimentation server-side or only on regional commerce pages outside the Brand Experience hub.

### 9.9 The two-property strategy

The deliberate split between the Brand Experience site and the Group corporate site is the most strategically interesting technical decision in the system. One property tells the story (mercedes-benz.com). The other discloses the obligations (group.mercedes-benz.com). The split preserves editorial ambition on the brand site without forcing it to absorb investor disclosures, supplier contracts, recall notices, or earnings PDFs. The two properties are visually unified but operationally distinct, and the brand uses the URL itself as a register signal. www.mercedes-benz.com is the dream. group.mercedes-benz.com is the proof.

### 9.10 Sub-domains and country dealers

Below the brand and corporate hubs sit hundreds of country-specific dealer subdomains (mercedes-benz.us, mercedes-benz.de, mercedes-benz.co.uk, etc.) which carry the configurator, the inventory, and the dealer-locator. Each dealer subdomain inherits the same design tokens and type system. The brand's discipline at maintaining tokens across hundreds of regional properties is one of the most underappreciated technical achievements in the global automotive industry.

### 9.11 Content management

The editorial pages on mercedes-benz.com are managed through a custom CMS the brand internally calls "Brandhub" (the same name reflected in the web-component prefix). Editors compose pages by selecting from a fixed library of components (stage, teaser-tiles, editorial-highlight, video-trailer, social-media-box) and providing copy and imagery. The CMS enforces typographic and color constraints automatically. Editors cannot author a page that violates the design system.

### 9.12 Legal entity and contact metadata

Per the Group corporate site footer:

- Mercedes-Benz AG
- Mercedesstraße 120, 70372 Stuttgart, Germany
- Phone: +49 7 11 17-0
- Email: dialog@mercedes-benz.com
- Court of Registry: Stuttgart, commercial register no. 7628
- Board of Management: Ola Källenius (Chairman), Jörg Burzer, Mathias Geisen, Olaf Schick, Michael Schiebe, Britta Seeger, Oliver Thöne, Harald Wilhelm
- Chairman of the Supervisory Board: Martin Brudermüller

The site footers expose this information consistently across languages and regions, which is itself a brand discipline. Mercedes-Benz treats legal-entity transparency as part of the brand voice, not as a compliance burden.

---

## 10. Pages Scraped

The following pages were directly visited and parsed during this audit:

1. `https://www.mercedes-benz.com/en/` (homepage, Brand Experience)
2. `https://www.mercedes-benz.com/en/vehicles/passenger-cars/mercedes-maybach/` (Maybach overview)
3. `https://www.mercedes-benz.com/en/innovation/concept-cars/vision-eqxx/` (Vision EQXX, redirected to /en/design/concept-cars/vision-eqxx/)
4. `https://www.mercedes-benz.com/en/sustainability/` (Sustainability overview)
5. `https://www.mercedes-benz.com/en/innovation/concept-cars/iconic-concept-amg-gt-xx/` (AMG GT XX concept)
6. `https://www.mercedes-benz.com/en/innovation/` (Innovation hub)
7. `https://www.mercedes-benz.com/en/heritage/` (Heritage hub)
8. `https://www.mercedes-benz.com/en/classic/` (Mercedes-Benz Classic news)
9. `https://www.mercedes-benz.com/en/lifestyle/` (Lifestyle hub)
10. `https://www.mercedes-benz.com/en/vehicles/passenger-cars/eqs/` (EQS PDP)
11. `https://www.mercedes-benz.com/en/innovation/concept-cars/vision-one-eleven/` (Vision One-Eleven, redirected to /en/design/concept-cars/vision-one-eleven/)
12. `https://group.mercedes-benz.com/en/` (Mercedes-Benz Group homepage)
13. `https://group.mercedes-benz.com/careers/` (Group Careers)
14. `https://group.mercedes-benz.com/sustainability/` (Group Sustainability)

DOM was inspected via shadow-root traversal, computed-style sampling, and CSS-custom-property enumeration. Live `document.fonts` registry was queried for every page. Structured data (`Organization`, `BreadcrumbList`) was captured via inline JSON-LD. The Mercedes-Benz star asset path (`/logos/mb-star-white.svg`) is declared identically across all pages tested. The full WB design-system token catalog (151 active CSS variables on the homepage alone) was harvested into the Color, Typography, and Layout sections above.
