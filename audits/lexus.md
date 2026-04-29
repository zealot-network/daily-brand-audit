# Lexus Brand Standards Audit, extracted from https://www.lexus.com and https://discoverlexus.com across 21 pages (April 2026)

Lexus operates two intentionally different digital properties that together form one brand. The first, lexus.com, is the United States consumer-and-retail experience operated by Lexus, a division of Toyota Motor North America. It is built on Adobe Experience Manager (AEM) with a React front end shipped through a single ~840 KB compiled stylesheet (`lexus-react.lc-*.min.css`) on top of AEM grid clientlibs. Its job is to convert. The user is moving toward a model page, a configurator, or a dealer. The second, discoverlexus.com, is the global brand-storytelling property operated by Lexus International. It is a Nuxt.js site (Vue, server-side rendered) maintained by the agency Resn (the build header reads `resn:build = '43ea3f4'` and `resn:build-date = Wed, 22 Apr 2026 19:46:34 GMT`). Its job is to make Lexus feel like a luxury idea, not a vehicle catalog. The two sites share the same four-letter wordmark, the same enclosed-L emblem, the same founding tagline ("Experience Amazing"), the same proprietary Nobel typeface, and the same near-monochrome palette. They differ in tone. The US site is engineered, dense, transactional, and feature-led. The global site is editorial, sparse, art-directed, and content-led. This audit treats both as one brand standard and documents the system across them. Today's date is April 28, 2026, and all observations reflect the live state of both properties on that day.

## 1. Color Palette

The Lexus palette is the quietest in the global luxury automotive segment. It has fewer colors than Mercedes-Benz, fewer accents than Audi, and substantially fewer system colors than BMW or Porsche. Lexus chooses to make the vehicle photography do the chromatic work. The interface is rendered in black, white, and a narrow grey scale. Real color almost never appears outside the vehicle itself. This is not minimalism. It is restraint as a brand signal. The palette is engineered to communicate that the product, not the page, carries the prestige.

### 1.1 Brand-defining canvas colors

Two hex values do the structural work across both digital properties.

`#000000`, pure black, is the dominant page color on lexus.com. It is the default page background on the homepage hero, every Model Landing Page hero (LX, RX, ES, IS, NX, LC), the Performance category page, the Electrified landing, the Destinations page, and the LCertified hub. It is also the default ink in the React stylesheet's `body, html` declaration, which establishes `color: #000` and `background: #fff` as the global root, then overrides per-page-section to invert depending on whether a hero photograph is being treated as a darkroom print or as a clean studio plate. The `body` rule reads `color: var(--app-primary-text-color, #000)` and `background: var(--app-background-color, #fff)`, so the root tokens default to black-on-white but accept dark-mode overrides on hero blocks.

`#FFFFFF`, pure white, is the universal ink on dark hero blocks and the default canvas on every secondary, support, transactional, or editorial page on lexus.com. The About hub, the About / Manufacturing, About / Technology, and About / Environment pages all run white. The Build configurator runs white. The Contact page runs white. The Accessibility statement runs white. The page rule sets `theme-color = #FFFFFF` in the head, which is what the OS reads to color the browser chrome and PWA tabs. Lexus chooses to brand the OS surface as white, not as a saturated brand color, which is again a deliberate restraint signal.

The third anchor color is one register lighter than pure white. `#FCFCFC`, near-white, is the default page background across discoverlexus.com. It appears 80 times in the inline style blocks of the global homepage. The eye reads it as white, but on calibrated displays it sits slightly off, just enough to give large editorial photography a subliminal warm cast without competing with the imagery.

### 1.2 The grey scale (the workhorse of the system)

Lexus carries hierarchy in grey, not in color.

`#333333`, dark grey, is the body-copy ink color on discoverlexus.com. It appears 67 times in the global home stylesheet and is the default text color for body paragraphs, captions, and editorial subheads. The choice is significant. Lexus does not set body copy at pure black. It softens body type to `#333` so headlines (which remain at `#000` or `#FFFFFF`) read as the highest-contrast layer on the page. The tactic is borrowed from print luxury fashion editorial.

`#707070`, mid-grey, is the secondary text color on both properties. It appears 35 times on discoverlexus.com inline styles and is referenced as `#707070` in the React stylesheet for the lexus.com utility-text and meta-text contexts. It sits in the middle of the grey ramp. It is used for date stamps, byline text, secondary captions, language-switcher inactive items, and disabled-state labels.

`#B1B1B1`, light grey, is the third tier, appearing 47 times in discoverlexus.com inline CSS. It is used for borders between editorial cards, divider lines beneath section headers, and inactive nav items in horizontal scroll-snapping carousels.

`#EFEFEF`, very light grey, appears in both properties, six times in the lexus-react stylesheet and twice in discoverlexus.com inline styles. It is the lightest neutral surface, used for newsletter-signup background bands, FAQ accordion backgrounds, and footer-divider blocks on the US site.

`#FAFAFA`, near-white grey, appears twice in the React stylesheet, used as the input-field background on light-mode form contexts (the Build configurator, the dealer search fields, the contact form fields).

`#262626` and `#131313` and `#181818` and `#303030` and `#3D3C3C` and `#4B4B4B` and `#4D4D4D` are all dark-grey values found on discoverlexus.com. These are not part of a tokenized scale. They are one-off treatments, each used in a single inline style block, almost certainly compiled per-component from a Sass mixin during the Resn build. The visual effect on screen is unified darkness. The fact that they are not consolidated into a single token suggests the global site is editorially built section-by-section rather than from a strict design system.

`#C8C8C8`, light grey, appears once on discoverlexus.com as a single divider rule on the global homepage.

`#E3E3E3`, very light grey, appears once on discoverlexus.com for an inactive UI element on the language-region selector overlay.

There is no warm grey. There is no cool grey. There is no second neutral track. Every Lexus grey is a flat, equal-channel hex. That choice is what gives the page its photographic stillness. Grey never competes with the chrome and paint of the vehicles and resort imagery on the page.

### 1.3 Functional colors

`#FF4500`, an orange-red, appears twice in the React stylesheet. It is not a brand color. It is used in two utility contexts only: the `nb-comparemodal` invalidation state and the `inline-error` state on the Build configurator's optional-equipment validators. Lexus uses it as a discreet error color rather than as an interface accent. It is never seen by the user unless they trigger a validation error on a configurator selection.

`#0000FF`, pure blue, appears twice in the React stylesheet. It is used as the focus-ring fallback on the legacy AEM-rendered text editor used for the Press Releases section. Modern Lexus pages override it. The user almost never sees it.

There is no green for success states in the visible Lexus palette. There is no yellow for warnings. There is no red for sales or discount language. The system instead handles success and warning through icon-shape changes (a checkmark glyph or an exclamation glyph) layered on top of grey backgrounds, paired with copy in the same `#333` body color as the rest of the page. Lexus deliberately suppresses the traffic-light convention that almost every consumer site uses, because traffic-light color suggests urgency and discount, and Lexus does not want urgency or discount in its brand language.

### 1.4 Notable absences

There is no "Lexus blue." There is no signature accent that maps to the brand the way Mercedes silver or BMW blue or Audi grey-silver does. The closest thing Lexus has to an accent is the platinum and rose-gold treatment used on its print and out-of-home advertising for the LC convertible and the LF-ZC concept, which does not appear on the digital properties at all.

There is no deep luxury navy, burgundy, or champagne in the digital palette, which is unusual for a luxury automotive brand. Lexus has consciously chosen to project a near-Japanese-minimalist palette rather than a Western-luxury palette. This is consistent with the brand's positioning as an alternative voice in luxury, oriented toward the omotenashi tradition (anticipatory hospitality) rather than European heritage.

There is no high-key brand color. Even the Spindle grille design motif, which dominates exterior vehicle design, is rendered on the website in nothing but body-shop paint colors and untreated photography. The web team does not use the spindle as a colored shape. It exists only inside the photography.

### 1.5 Vehicle paint colors as the only chromatic voice

Almost the entire visible chromatic range on lexus.com lives inside vehicle photography and, more specifically, inside the configurator color-chip swatches on each Model page. From the 2026 lineup as exposed on the Model pages and the Build configurator:

LX (full-size luxury SUV): Eminent White Pearl, Atomic Silver, Caviar, Manganese Luster, Nori Green Pearl, Moon Desert.

RX (mid-size luxury SUV): Ultra White, Eminent White Pearl, Atomic Silver, Cloudburst Gray, Caviar, Nightfall Mica, Matador Red Mica, Nori Green Pearl, Copper Crest, Iridium.

ES (mid-size luxury sedan): Ultra White, Atomic Silver, Iridium, Caviar, Matador Red Mica, Nightfall Mica, Heat Wave.

IS (compact luxury sport sedan): Ultrasonic Blue Mica 2.0, Infrared, Atomic Silver, Caviar, Iridium, Matador Red Mica, Cloudburst Gray, Eminent White Pearl, Ultra White, Heat Wave.

NX (luxury crossover): Ultra White, Atomic Silver, Iridium, Caviar, Cloudburst Gray, Nori Green Pearl, Matador Red Mica, Cloudburst Gray, Grecian Water.

LC (luxury coupe): Smoky Granite Mica, Liquid Platinum, Eminent White Pearl, Caviar, Infrared, Nightfall Mica, Atomic Silver, Iridium, Flare Yellow, Structural Blue.

The naming carries more emotional voice than the rest of the site. The names trade on materials science and natural phenomena: pearl, mica, luster, atomic, infrared, structural, eminent, iridium, caviar, nori, granite. There is no "Pacific Sunrise" or "Mountain Sky" cliché. The naming convention is closer to luxury watchmaking dial nomenclature (mother-of-pearl, lacquer, opaline) than to mainstream automotive paint naming.

Two color names are deliberately confrontational. "Caviar" replaces "black" across most of the Lexus lineup, and "Infrared" replaces "red." These are positioning statements. Caviar is rendered as a deeper, more saturated, near-blue-black with a slight pearl flake. Infrared is rendered as a high-saturation orange-red that reads as molten metal under direct light. Both are signature Lexus paint expressions that customers cite specifically.

## 2. Typography

Typography is the most settled part of the Lexus identity. Two faces carry the entire system. Sizes are restrained. Weight contrast is dramatic. Letter-spacing is the brand's most recognizable typographic gesture.

### 2.1 Font families

`Nobel`, the proprietary geometric sans-serif designed by Tobias Frere-Jones (originally for Hoefler & Frere-Jones, descended from a 1929 Sjoerd Hendrik de Roos design), is the entire Lexus type system. It appears in two referenced weights across both properties.

`nobel-bold` is the headline and CTA weight. It is declared on `button` in the React stylesheet (`font-family: nobel-bold, sans-serif`), on every primary CTA, every section headline, every model-name display, every navigation link in active state, and every footer link.

`nobel-book` is the body, paragraph, navigation-default, and form-input weight. The site root rule is `body, html { font-family: nobel-book, sans-serif }`, so every piece of text on the site that isn't explicitly a button or an oversized headline reads in Nobel Book.

On discoverlexus.com the family is referenced as `Nobel-Book, Helvetica, Arial, sans-serif` and `Nobel, Helvetica, Arial, sans-serif`, indicating two-weight loading with Helvetica as the system fallback. The fallback chain on lexus.com is shorter (`nobel-book, sans-serif`), which trusts the browser to substitute its system sans without specifying a fallback face by name. The two stacks suggest the global Resn build was written to a stricter graphic-design standard, while the US AEM build was written to a more permissive web-engineering standard.

There is no serif on either property. There is no display font. There is no monospace except a single utility declaration of `DecimaMonoPro` and `akkurat-mono` which exist only in third-party React modules embedded in the bundle (likely from a Headless CMS preview component) and are never seen on a public Lexus page.

### 2.2 Heading hierarchy

H1 appears once per page and carries the model name or page title. On Model Landing Pages, H1 reads the model name in `nobel-bold`, sized between 48 and 96 px depending on viewport, in `letter-spacing: .02em` to `.04em`, in pure white over a black hero photograph, in a 1.0 to 1.05 line-height. The text-transform is mixed: model letters (LX, RX, ES, IS, NX, LC) remain uppercase as model nomenclature, while supporting words ("Discover," "All-New," "Reimagined") often appear in title case.

H2 carries section titles ("Performance," "Interior," "Technology," "Safety," "Specifications") on PDP pages. It is set in `nobel-bold` at approximately 28 to 36 px, `letter-spacing: .04em`, mixed case, color `#000` on white sections and `#FFFFFF` on black sections. Line-height sits at approximately 1.1 to 1.2.

H3 carries feature titles within sections, set in `nobel-bold` at approximately 18 to 22 px, `letter-spacing: .04em`, mixed case. This is also the size of footer column headers.

H4 is rare. It appears mostly inside the About / Manufacturing, About / Technology, and About / Environment editorial pages where Lexus uses a four-tier hierarchy to render long-form content. It is set in `nobel-bold` at 16 to 18 px.

H5 and H6 are not used as headings on any page reviewed. They exist in the AEM template but are unstyled in the brand stylesheet.

On discoverlexus.com the headline scale is dramatically larger. The H1 on the global homepage reads "Welcome to Lexus" in display sizing that fills nearly the full width of the desktop viewport at 1440 px. The accompanying H3 reads "Milan Design Week 2026" as a featured story headline at a much smaller size. The contrast between H1 and H3 on the global site is one of the largest type-scale jumps in the global luxury automotive web (roughly 4:1), which is what makes the global site feel like a magazine cover rather than a product catalog.

### 2.3 Body text

Body type renders in `nobel-book` at 16 px (the React stylesheet sets `body { font-size: 1rem }`), with `font-weight: 300`, `letter-spacing: 0`, `line-height: 1.4`. The 300 weight is unusual. Most luxury automotive sites set body type at 400 or 500 for legibility. Lexus chose 300 because Nobel Book at 300 weight has a thin, even stroke that reads as more refined and photographic. The trade-off is contrast on grey backgrounds, which Lexus mitigates by using only light backgrounds for any extended reading (About pages, Press Releases, Lexus Magazine articles).

The body color is `var(--app-primary-text-color, #000)`, which means pure black on light backgrounds. Some templates override this to `#333` for editorial reading, particularly on discoverlexus.com.

### 2.4 Navigation text

Desktop navigation links read in `nobel-book` at 14 px, color `#000` on white-mode pages and `#FFFFFF` on dark-mode pages, in title case ("Vehicles," "Build," "Owners," "Find Inventory," "Local Dealer"). On hover, the link does not change color. It receives an underline animation at the same color. The underline is 1 px tall, animates from 0 to 100 % width over approximately 200 ms with a custom cubic-bezier easing, and is removed on mouse-out at the same speed in reverse. There is no fade transition on the link text itself.

On discoverlexus.com the global nav reads "Stories," "Models," and a region-switcher. Same Nobel-Book treatment, slightly tighter at 13 px to harmonize with the editorial scale.

### 2.5 Button text

The button rule is the most cited fragment in the Lexus stylesheet. It reads, verbatim:

```
button {
  background-color: transparent;
  border: 2px solid #000;
  border-radius: 0;
  border-radius: initial;
  color: #000;
  font-family: nobel-bold, sans-serif;
  font-size: 13px;
  letter-spacing: .04em;
  letter-spacing: var(--app-letter-spacing, .04em);
  line-height: 18px;
  margin-right: 0;
  min-width: 150px;
  transition: all .15s cubic-bezier(.335,.015,.46,.995);
}
```

Every button on Lexus.com inherits from this rule. The 13 px is small for a luxury site. The `.04em` letter-spacing pushes the type slightly apart, which gives Nobel-Bold at 13 px a refined, certain feel rather than a cramped feel. The 150 px min-width makes every CTA the same minimum visual weight regardless of label length, so "BUILD" and "INVENTORY SEARCH" and "FIND A DEALER" all read with the same horizontal authority. The 0 border-radius is critical to the brand expression. Lexus does not round buttons. Sharp corners are part of the visual language.

The cubic-bezier transition (`.335,.015,.46,.995`) is a slow-out, fast-in custom easing that feels like a heavy industrial motion rather than a soft web motion. It gives the hover and click feedback a sense of mechanical precision.

### 2.6 Price text

Lexus does not show prices in display typography. Price text is set in the same Nobel Book at 14 to 16 px, with the price prefixed by "Starting at" or "MSRP," and a small disclaimer link "Disclosure" or an asterisk leading to a fine-print modal. There is no strikethrough or sale-price treatment. There is no "limited-time" type. There is no comparison-pricing tactic. The brand explicitly avoids retail-style pricing UX.

### 2.7 Form text

Input placeholder text reads in Nobel Book at 14 px, color `#707070`, italicized off (Lexus does not italicize). Label text reads in Nobel Bold at 12 px, color `#000`, all-caps with `.04em` letter-spacing, sat above the input field. The pattern is consistent across the contact form, the dealer search, and the configurator's form steps.

Validation messages, when triggered, render in `#FF4500` orange-red (the only place that color appears) at the same 12 px label scale, in Nobel Bold, all-caps, with a 4 px-circle icon glyph to the left.

### 2.8 Footer text

Footer column headers render in Nobel Bold at 14 px, all-caps, `.04em` letter-spacing, color `#FFFFFF` (the footer is always black). Footer links render in Nobel Book at 13 px, color `#FFFFFF`, in title case. Legal disclaimer text in the footer's bottom strip renders in Nobel Book at 11 px, color `#B1B1B1`, line-height 1.4. There is no footer use of grey on grey for hierarchy. The hierarchy is carried by font-weight and size, not by color.

### 2.9 Uppercase / lowercase usage rules

Lexus has a small set of typographic rules that are enforced consistently:

- All buttons render in **all-caps** with `.04em` letter-spacing.
- All footer column headers render in **all-caps** with `.04em` letter-spacing.
- All form labels render in **all-caps** at 12 px.
- All section eyebrow labels (the small text above an H2 that names the section topic, e.g., "PERFORMANCE" above an H2 that reads "Crafted for the Drive") render in **all-caps** with `.04em` letter-spacing in Nobel Bold at 11 to 12 px.
- All headlines (H1, H2, H3) render in **mixed case** (sentence or title case), never in all-caps.
- Body type renders in **mixed case**.
- Navigation links render in **mixed case**.
- Model names, when used as nameplates, render in their nameplate format (LX, RX, ES, IS, NX, LC, RZ, RC F, GX), which preserves caps as the nameplate dictates.

The rule is: utility text and meta-text are uppercase; reading text and headlines are not. This is a print-luxury-magazine convention adapted to web. It separates "this is a control" from "this is the content."

### 2.10 Letter-spacing distribution

The `.04em` letter-spacing is the brand's typographic signature on small text. The fact that it's tokenized as `--app-letter-spacing` and inherited everywhere shows the team treats letter-spacing as a brand variable, not as a per-component decision. Body type is `letter-spacing: 0` (Nobel Book is already drawn for legibility at body size). Headlines run at `.02em` to `.04em` depending on size. Display headlines on discoverlexus.com run as low as `0` because the display sizes are large enough that letter-spacing would create visible gaps.

### 2.11 Font-weight distribution

Lexus uses two weights of one face. There is no medium, no semibold, no light, no extralight, no italic. The contrast between Nobel Book (300 effective on the body declaration) and Nobel Bold is the only weight contrast on the site. This is unusually restrained for a contemporary web design. It enforces a "two voices, one face" philosophy that gives the entire experience a consistent typographic atmosphere.

### 2.12 Type scale philosophy

The type scale is custom, not modular. Body sits at 16 px. Buttons sit at 13 px (smaller than body, which is unusual). Footer legal sits at 11 px. Section eyebrows sit at 12 px. H3 sits at 18 to 22 px. H2 sits at 28 to 36 px. H1 sits at 48 to 96 px on hero. Display H1 on discoverlexus.com goes well past 120 px in viewport-relative units.

The hierarchy communicates a magazine sensibility. Body is the workhorse. Headlines are the only thing that gets bigger. UI controls (buttons, labels, eyebrows) sit smaller than body, in caps, in bold weight, which is the editorial convention for "captions" in print luxury fashion.

### 2.13 Application by page type

The homepage uses the largest type-scale range, with full-bleed hero H1 at the top and tightly-set Nobel Bold eyebrows over each lower section. Model Landing Pages use a tighter range, with H1 at the hero and consistent H2 and H3 below. About pages run a much smaller range; they read like long-form editorial with H2 around 24 to 28 px and H3 around 16 to 18 px. Support and form pages compress further, often skipping H1 in favor of a Nobel Bold 18 px header. discoverlexus.com is the most expansive scale, treating every story page as a magazine spread with display headlines that visually approach Vogue or Wallpaper rather than an automotive manufacturer site.

## 3. Logo & Wordmark

Lexus has two logo elements that are used together and apart depending on context. Both are reproduced strictly in monochrome on the digital properties.

### 3.1 The L emblem

The primary logo mark is a stylized capital "L" inside a horizontal oval. It is one of the few luxury automotive emblems that reads as a wordmark-letterform rather than a heraldic symbol. The proportions are precise: the "L" sits centered inside the oval with strict mathematical balance, the oval's stroke weight is consistent through 360 degrees, and the L's vertical stroke is the same weight as the oval's stroke. The mark is set as an SVG on every page header. On lexus.com it appears as a white SVG over a transparent rectangle in the upper-left of the header, occupying approximately 32 px tall by 44 px wide on desktop and 24 px tall by 33 px wide on mobile. The mark is also the favicon, where it is rendered at 32 x 32 px, 16 x 16 px, and 192 x 192 px. The browser theme color (`#FFFFFF`) frames the favicon in white, which is consistent with the brand's monochrome palette.

### 3.2 The wordmark

The Lexus wordmark spells out "LEXUS" in a custom letterform that resembles a heavily customized cut of Nobel Bold. The letters are drawn with extreme precision, with the "X" centered between the "E" and "U" carrying a slightly heavier baseline weight than the surrounding letterforms. The wordmark is approximately 4 to 1 in width-to-height ratio. It appears in the lower-right of every model hero photograph on lexus.com paired with the model designation (e.g., "LEXUS LX," "LEXUS RX"), in white over photography. It appears centered in the global navigation header on discoverlexus.com, where it functions as the home link.

### 3.3 Header placement

On lexus.com, the L emblem is in the top-left of the header. The model nameplate (when on a Model page) sits to its right, separated by a thin vertical divider rule. The main navigation horizontal links sit centered below or to the right of this lockup at desktop sizes. On mobile, the L emblem stays top-left, and the navigation collapses into a hamburger menu icon top-right.

On discoverlexus.com, the LEXUS wordmark is centered in the header, with "Stories" and "Models" navigation links flanking it left and right. The visual weight is symmetric. This is the luxury-magazine convention (the masthead centers the title; the columns flank it).

### 3.4 Footer treatment

On lexus.com the footer carries the L emblem at the top of the column block on desktop, sized larger than the header (approximately 64 px tall) and rendered in white over the black footer. It is centered horizontally above the social icon row. The wordmark does not appear in the footer.

On discoverlexus.com the footer carries no logo mark at all. The footer is text-only.

### 3.5 Favicon

The favicon is the L emblem rendered as a white "L" inside a black filled oval. The browser tab background is `#FFFFFF` per the `theme-color` meta declaration. There is no Apple touch icon variation referenced separately; the same SVG is upscaled.

### 3.6 Logo variations

Lexus has at least three documented digital logo variations:

- White L emblem on a transparent or dark background (header on most pages, footer on lexus.com).
- Black L emblem on a transparent or light background (used on light-mode editorial pages, including About / Manufacturing).
- Black L emblem inside a white-filled oval (used on the favicon, and on "Powered by Lexus" or partner co-branding lockups).

The wordmark exists in white-on-dark and black-on-light, but the white-on-dark variant is dominant. The brand effectively does not use color in the logo. There is no gold, silver, or chrome treatment of the mark on the digital properties, which differs from the print and out-of-home advertising where a high-polish chrome treatment of the L emblem is sometimes used.

### 3.7 Clear space and sizing

The clear space rule (per the brand guidelines as inferred from the live site, not from a published guideline document) is approximately the height of the oval's vertical stroke on all four sides. The minimum legible size on screen is approximately 16 px tall for the L emblem. Below that, the favicon variant (with the filled oval) is used.

### 3.8 Co-branding / collaboration lockups

The Destinations by Lexus page is the only place co-branding appears prominently. Each partner property (Auberge, Sea Island, Big Cedar Lodge, Pebble Beach) appears with its own logo paired with a small "DESTINATIONS by Lexus" lockup, where "DESTINATIONS" is set in Nobel Bold all-caps and "by Lexus" is set in Nobel Book mixed case, all over photography of the resort. The L emblem does not appear in the co-brand lockup; the wordmark "Lexus" carries the brand presence. This is restraint. The partner property's identity leads, and Lexus follows in small type.

The LCertified pre-owned program lockup pairs an "L" mark inside a square (different from the standard oval emblem) with the word "Certified" set in Nobel Book. The L is rendered in white inside a black square, sitting above the wordmark. This is a deliberate visual differentiator: the program is "of Lexus" but distinct from the new-vehicle expression. The same logic applies to F and F SPORT (which use a stylized "F" sub-mark for the performance line) and to "Lexus Interface" (which uses no logo at all and instead types out the program name in the brand typeface).

### 3.9 Logo-to-navigation relationship

The relationship is asymmetric on lexus.com. The logo sits independently in the corner; the navigation occupies the opposite axis. There is no centering of the lockup relative to the navigation. The logic is that the logo is a constant brand anchor, and the navigation is a state-dependent control surface; they don't share visual rhythm.

The relationship is symmetric on discoverlexus.com, where the wordmark is centered between two equal navigation panels. The logic is editorial: the masthead is the center of the spread.

### 3.10 Logo as brand signal

The strategic interpretation is that Lexus uses its logo restraint as a marker of confidence. The brand never enlarges the mark beyond what a section needs. It never colors it. It never animates it on initial page load. The only logo motion is a subtle scale-down when the user begins to scroll past the hero (the header collapses; the L emblem reduces by approximately 20 percent in height). This gesture is mechanical, brief, and never repeated. The logo communicates that the vehicle is the hero and the brand is the steward.

## 4. Layout & Grid System

The Lexus grid is unusually disciplined. The same content max-width and section padding rhythm carries from the homepage through every Model Landing Page through every About page. Variation lives inside the component composition, not inside the framing.

### 4.1 Content max-width

The `--grid-max-width` token on discoverlexus.com is set explicitly to `1523.5px`. The `.5` is meaningful: the team treats the grid as a sub-pixel measurement to prevent rounding artifacts in column gutters at 1440 px viewports. The `--grid-side-margin` is `50px` on desktop and `20px` on mobile. The `--grid-columns` toggles between 14 (default editorial layout) and 15 (the gallery layout), which is unusual. Most luxury sites run 12-column grids. Lexus chose a higher-resolution 14- or 15-column grid because it gives the editorial team more flexibility to size featured photography in non-standard widths (e.g., 11 columns wide for an asymmetric hero, 4 columns wide for a portrait inset).

The `--grid-column-gap` is `22px` on desktop and `5px` on mobile. The `5px` mobile gap is unusually tight. On mobile, the grid effectively becomes a single-column scroll, but Lexus retains the 5 px gap to preserve a small architectural separation between stacked editorial cards.

On lexus.com the grid is the AEM 24-column grid (`aem-Grid--24` and `aem-GridColumn--default--*`), with content typically constrained inside a `1440px` to `1600px` outer container. The 24-column structure is high-resolution and lets the AEM authoring tools place components at any 1/24th increment, but the visible layout typically reads as a 12-column grid because authors place components in pairs, fours, sixes, eights, twelves, or full-bleed.

### 4.2 Homepage section sequence

The lexus.com homepage at the time of this audit, in scroll order: full-bleed hero carousel (rotating through three or four featured 2026 vehicles, each with a different paint color and headline), an Explore the Lineup section (a horizontal scrolling card list of all current model pages), a Build Your Lexus call to action band, an Electrified vehicles featured section, an Offers band, a Find a Dealer band, an Owner Resources or My Lexus band, a Lexus Magazine featured-stories section, and a footer.

Each section above the footer occupies approximately 100 vh on desktop, with the hero carousel running closer to 110 vh. The visual rhythm is deliberately slow: a viewer scrolls through one section per visible step, then encounters a clear visual reset (a black-to-white color change, a shift from photography to typography) before the next section begins. The pacing is consistent with luxury print magazine spreads.

### 4.3 PLP grid structure

The all-models page (`/models`) and the category pages (`/models/categories/performance`) render the model lineup as a 3-column desktop grid (3 cards across), 2-column tablet grid, and 1-column mobile stack. Each card is approximately 4:3 in aspect ratio, with the vehicle photograph filling the upper two-thirds and the model name and starting price filling the lower third. The grid gap is approximately 24 px desktop, 12 px mobile.

There is no pagination, no infinite scroll, and no load-more behavior. The full lineup fits in a single viewport-and-scroll, which reflects the constrained product range (10 to 12 model lines, depending on year). This is a luxury-portfolio convention: every model is presented as equally important, none is buried behind an interaction.

### 4.4 PDP layout

Every Model Landing Page follows the same template:

1. Full-bleed hero photograph (the vehicle in 16:9 or wider, with the model nameplate in white over the lower-third of the image).
2. A short brand-statement paragraph (one to three sentences in Nobel Book at 18 to 22 px, white on the same hero or on a dark background block immediately below).
3. A horizontal carousel or gallery of feature highlights (Performance, Design, Interior, Technology, Safety), each rendering as a full-bleed photograph with a Nobel Bold eyebrow label and a Nobel Bold H2 headline.
4. A specifications table or comparison module, sometimes presented as a horizontally scrolling card list.
5. A "Trims" or "Build" module that lets the user select among trim levels and triggers the Build configurator.
6. A gallery section (sometimes rendered as a 360-degree exterior viewer or as a still-image slideshow).
7. A "Find a Dealer" or "Inventory Search" call-to-action band.
8. The standard footer.

The information panel-to-image ratio across the PDP is approximately 1:5 by vertical pixel weight. Photography dominates. Information serves the photography, not the other way around.

### 4.5 Editorial / content page layouts

The About / Manufacturing, About / Technology, and About / Environment pages run a single-column editorial layout with a content max-width of approximately 800 px (so the line measure stays at ~75 characters). Section headers are full-bleed photography with a Nobel Bold H2 set over the top. Body copy sits in a single column. Inline imagery breaks out to full-bleed at section breaks.

The Lexus Magazine and the discoverlexus.com Stories pages follow a magazine-spread layout, with full-bleed hero photography, a centered Nobel Bold H1, a contributor byline in Nobel Book 12 px, a body-copy column at approximately 700 px max-width, and full-bleed pull-quote spreads inserted between sections.

### 4.6 Support page layouts

The Contact, Accessibility, and Lexus Financial pages follow a constrained content layout with a max-width of approximately 1080 px, two-column information arrangement (left column for navigation links, right column for content), and Nobel Book body type. The FAQ accordion uses Nobel Bold question text and Nobel Book answer text, with a thin grey divider line between each question.

### 4.7 Section padding rhythm

Vertical padding between major sections on the homepage and PDP is approximately 96 px desktop, 64 px tablet, 48 px mobile, though full-bleed-photograph sections override this to zero (the photograph reaches edge-to-edge with no padding, and the next section's padding restarts after it). Section padding inside a content-constrained section (About pages, Magazine articles) is approximately 64 px desktop, 48 px tablet, 32 px mobile.

### 4.8 Element spacing patterns

Inside a content section, the rhythm is: H2 headline → 24 px gap → optional H3 sub-headline → 16 px gap → body paragraph → 24 px gap → next paragraph → 48 px gap → next sub-section. The spacing is consistent within a section and resets at the next section boundary. Form fields stack at 16 px vertical gaps with 8 px gaps between label and input.

### 4.9 Responsive breakpoints

The React stylesheet exposes breakpoints at `640px` (sm), `768px` (md), `1024px` (lg), `1280px` (xl), and `1536px` (2xl). The discoverlexus.com Nuxt site uses similar breakpoints. The most visible responsive transition happens between 1024 and 1280 px, where the desktop horizontal nav collapses into a more compact form, and between 768 and 1024 px, where the model cards transition from a 3-column to a 2-column grid.

### 4.10 Whitespace philosophy

Lexus is generous with vertical whitespace and frugal with horizontal whitespace. On the homepage and Model pages, sections are tall (approximately one viewport per section) and have substantial padding before and after the headline. Inside a section, content sits close to the edges of the photograph, with no margin band, because the photograph is intended to function as the visual frame. On the About pages and editorial content, both vertical and horizontal whitespace are generous; the content max-width is ~800 px on a 1440 px viewport, leaving substantial side margin to focus the eye.

### 4.11 Scroll depth patterns

Homepage scroll depth is high (approximately 8 to 10 viewports). Model pages run 12 to 18 viewports. About pages run 4 to 8 viewports. Support pages (Contact, Accessibility) run 1 to 3 viewports. The discoverlexus.com homepage runs approximately 6 viewports with a strong stop-and-look pacing.

### 4.12 Full-bleed vs. contained

Hero photography, model gallery photography, and editorial section breaks are full-bleed. Body copy, specifications, navigation, and forms are contained within the max-width container. The visual switching between full-bleed and contained is the primary device for sectioning. Lexus does not use horizontal rules, dividers, or section borders to separate content. The transition between full-bleed photography and a contained text block is the section break.

## 5. UI Components

The component inventory across both properties is small relative to comparable luxury brands. Lexus prefers fewer, more refined components over a broad library.

### 5.1 Buttons

The primary button is the rule documented at length in Section 2.5: 2 px solid `#000` border, 0 border-radius, transparent fill, `nobel-bold` 13 px text in `#000`, `.04em` letter-spacing, 18 px line-height, 150 px min-width, `.15s cubic-bezier(.335,.015,.46,.995)` transition. On hover, the button inverts: fill becomes `#000`, text becomes `#FFFFFF`. The border remains at 2 px solid `#000`. The transition is sharp and mechanical.

The secondary button is an "underline link" treatment: no border, no background, Nobel Bold 13 px text in `#000`, with a 1 px underline that animates from 0 to 100 % width on hover. This pattern is dominant in editorial contexts where a full button would be visually loud.

A third pattern, the "pill" button, appears only on the discoverlexus.com global homepage as the language-region selector and the "Change region" CTA. It is a Nobel Book 13 px label in white inside a black filled rounded rectangle (border-radius approximately 24 px, the only place rounded corners exist anywhere on either site). This is the global team's exception. The US team does not adopt it.

There is no small/medium/large size variant family. Every primary button is the same scale (150 px min-width, 13 px text, ~38 px tall). The brand intentionally avoids buttons that compete for attention.

### 5.2 Navigation

Desktop nav on lexus.com is a horizontal flat list: "Vehicles," "Build," "Owners," "Find Inventory," "Local Dealer," sometimes augmented with "Offers," "L/Certified," "Lexus Magazine." The "Vehicles" link opens a mega-menu on hover that displays the full lineup as a 3-column visual list with thumbnail images of each model. The mega-menu uses a black background panel with white type, separated from the page below by a thin 1 px white-on-black divider line.

Mobile nav collapses to a hamburger icon (three thin horizontal lines, 2 px stroke, 24 px wide, 16 px tall) in the top-right. Tapping the hamburger triggers a full-screen overlay with the navigation rendered as a stacked list, each item separated by a thin grey divider, with the Lexus L emblem at the top and a close X icon at the top-right.

The discoverlexus.com nav is two visible items ("Stories," "Models") flanking the centered LEXUS wordmark, with a "Change region" link in the upper-right that opens a region-selector modal. The mobile nav collapses similarly to a hamburger in the upper-right.

There is a thin secondary utility nav on both sites at the very top of the desktop layout that includes "My Lexus" sign-in, language switcher, and (on lexus.com) ZIP code entry. This utility band sits above the main nav and reads in Nobel Book 12 px in `#707070` over white.

### 5.3 Breadcrumbs

Breadcrumbs are rare. They appear on Lexus Magazine article pages and on a few About sub-pages. The format is "Lexus / Section / Sub-section" with a thin slash separator in `#707070`, set in Nobel Book 12 px. Most pages do not use breadcrumbs.

### 5.4 Announcement / utility bar

There is no announcement banner pattern on either property. Lexus does not use a top-of-page promotional or news bar. This is unusual for an automotive site where seasonal incentive and event banners are the convention. The brand's position is that an ad-style banner in the navigation undermines the editorial atmosphere.

### 5.5 Product cards (PLP)

The Model card on the all-models page renders a vehicle image at 4:3 aspect ratio in the upper portion of the card, with no background fill (the photograph sits directly against the page color), then below the image: the model nameplate in Nobel Bold 18 to 22 px, the body type label in Nobel Book 14 px (e.g., "Luxury Sedan," "Luxury SUV," "Luxury Coupe"), the starting price in Nobel Book 14 px ("Starting at $44,675*"), and a Nobel Bold 13 px CTA "Explore" or "Build" with the standard underline-link treatment. The card has no visible border, no shadow, no hover lift. On hover, the photograph dims slightly (approximately 10 % opacity reduction) and the CTA underline animates in.

### 5.6 Product Detail Page components

The PDP gallery is an inline carousel that auto-advances through three to five featured photographs, with thumbnail dots below the active image. The Build configurator embedded inside the PDP renders trim selectors as horizontal card-list strips (each trim is a card with a thumbnail, a name, a starting price, and a "Build" CTA). Color selection within the configurator renders as 36 px circular swatches in a horizontal row, with the swatch border at 1 px `#B1B1B1` (selected state shows a 2 px `#000` ring around the swatch with 4 px outer padding).

The "Add to Cart" equivalent on a vehicle PDP is "Build" or "Inventory Search," both of which open the configurator or the inventory search page in a new state. There is no "Reserve" or "Order" CTA on most US Lexus pages, which is consistent with the brand's preference for routing to a dealer rather than a direct-purchase flow.

The product description is presented as a series of inline editorial blocks, not as a single description box. Each block has its own headline, photograph, and copy. There is no accordion or tab structure for the description. Specifications are presented in a separate section, often as a comparison table.

### 5.7 Forms

Form input fields render with a 1 px solid `#B1B1B1` bottom border (no other border), 16 px Nobel Book input text in `#000`, 14 px Nobel Bold all-caps label above, 12 px Nobel Book placeholder text in `#707070`, 12 px Nobel Bold validation text in `#FF4500` below the field on error. The field background is `#FAFAFA`. Inputs are full-width within their column.

Submit buttons within forms (e.g., "Submit," "Continue") follow the standard primary button rule.

The newsletter signup form on the footer of lexus.com is a single email input with an inline arrow CTA. The CTA is a 32 px square button with a thin right-arrow icon, white on black, no text label.

### 5.8 Accordions

The FAQ accordion, used on the Contact page, uses a thin `#B1B1B1` bottom-border between items, a Nobel Bold 16 px question, a "+" plus-minus icon on the right (24 px wide, 1 px stroke, switches to a "−" minus when the item is open), and Nobel Book 14 px answer text that animates open over approximately 250 ms on click. There is no chevron or caret variant.

### 5.9 Footer

The footer on lexus.com is `#000` background with `#FFFFFF` text. It is structured as five columns on desktop:

1. Vehicles (links to each model line, plus "All Models" and "Build")
2. Shop (Find Inventory, Find a Dealer, Offers, L/Certified, Request a Brochure)
3. Owners (Owners Manual, Service, Warranty, Connected Services, My Lexus)
4. Lexus (About Lexus, Lexus Magazine, Destinations, Careers, Press Releases)
5. Contact (Contact Us, Accessibility, Site Map, Privacy, Terms)

Below the columns sits the legal disclaimer band (`#000` background, `#B1B1B1` text, 11 px), with copyright, "© Lexus, a Division of Toyota Motor Sales, U.S.A., Inc.," a "Do Not Sell or Share My Personal Information" California-CCPA link, and the Lexus L emblem in white centered above the band.

The footer on discoverlexus.com is far simpler. Two columns on desktop, "Lexus International / Privacy / Legal / Cookies" on the left, "Stories / Models / Models / Featured" on the right, with a bottom-strip "© 2026 Toyota Motor Corporation. All rights reserved." in 11 px. There is no logo in the footer.

### 5.10 Other components

Search appears as an icon-triggered field in the lexus.com utility nav. Click triggers a slide-down drawer with an input and predictive results.

The cart pattern does not exist on the consumer site. There is no cart on lexus.com, because vehicles are not sold direct. The closest equivalent is "My Inventory" in the inventory search flow, which lets a user save vehicles to a list for dealer follow-up.

Modals appear primarily for the "Disclosure" / fine-print legal notes, the language switcher, the dealer locator, and the form-submission confirmation. Modal styling is `#FFFFFF` panel over a `rgba(0,0,0,.6)` overlay, with the panel sized at approximately 600 px wide by content-tall, no border-radius (sharp corners), a small Nobel Bold close X in the top-right, and Nobel Bold 16 px header inside.

Toast / notification components appear after form submission, rendered as a thin band at the top or bottom of the viewport, `#000` background, `#FFFFFF` 14 px text, auto-dismiss after 4 seconds.

Loading states use a thin horizontal progress bar at the top of the viewport (1 px tall, white-on-black on dark pages, black-on-white on light pages). There is no skeleton screen. There is no spinner inside content blocks.

Empty states on the inventory search page (when a dealer has zero matching vehicles) use a 14 px Nobel Book message and a Nobel Bold 13 px CTA to "Expand Search." There is no illustrated empty state.

Video players are embedded as native HTML5 video on the homepage and feature pages, with custom controls overlaid in white over the lower-third. Autoplay-with-mute is the default on hero videos. The user can tap or click to unmute and resume control.

Scroll animations are present but subtle. Section headers fade in over approximately 400 ms as they enter the viewport, with a slight upward translate of 12 px. Photography crossfades on the homepage carousel over approximately 600 ms. There is no parallax. There is no horizontal scroll-snap on lexus.com (the discoverlexus.com global site does use scroll-snap on the Stories carousel).

### 5.11 Accessibility observations

Focus indicators on interactive elements are visible: a 2 px solid `#000` outline on focusable elements on light backgrounds, 2 px solid `#FFFFFF` on dark backgrounds. The brand explicitly maintains a public Accessibility Statement at `/accessibility` and references compliance with WCAG 2.1 AA. Alt text on product images follows a consistent pattern ("2026 Lexus RX in Caviar shown from 3/4 front angle"). Keyboard navigation works through the main nav and form inputs without trapping. Color contrast on the white-mode pages meets AA at body-text size; on the dark-mode hero pages, the Nobel Book 300-weight body type at 14 to 16 px sits at a contrast ratio that is acceptable but tight in some implementations.

## 6. Iconography

Lexus iconography is minimal, custom, and consistent.

### 6.1 Icon library

Lexus does not use a third-party icon set (no Font Awesome, no Material Symbols, no Lucide). Every icon on the site is a custom SVG drawn by the Lexus design team or by Resn for the global property. The SVGs are inlined directly in the React bundle and the Nuxt bundle, not loaded as a sprite sheet.

### 6.2 Icon style

Icons are uniformly thin-stroke line icons with sharp corners (no rounded terminals). The default stroke weight is 1.5 px, sometimes 1 px on smaller icons. The icons are drawn on a 24 px or 32 px grid, with consistent corner radii (approximately 0 px to 1 px max). There are no filled icons except the social platform icons in the footer (Facebook, Instagram, X / Twitter, YouTube, LinkedIn), which are drawn in the platform's official monochrome filled style.

### 6.3 Where icons appear

Icons appear in the navigation utility bar (search, account / My Lexus, language / region globe), the announcement-free header (none, as documented), the form fields (occasionally a small icon in the field for context, e.g., a magnifying glass in the search input), the footer social row, the FAQ accordion (the +/− toggle), the modal close (an X), the carousel controls (arrows), and the safety / technology specification icons on Model pages (e.g., a small icon for "Lexus Safety System+ 3.0" features).

### 6.4 Icon sizing

Icons in the utility nav are 18 to 20 px. Icons in the footer social row are 24 px. Icons in the FAQ accordion are 24 px. Icons in the carousel controls are 32 to 40 px. Icons in the safety system spec sheet are 48 px. There is no icon larger than 64 px on either site.

### 6.5 Icon color

Icons inherit text color. They render in `#000` on light-mode pages, `#FFFFFF` on dark-mode pages, `#707070` for utility-bar icons, and `#B1B1B1` for inactive state. There is no brand-color icon treatment.

### 6.6 Notable absences

There are no decorative or illustrative icons. There are no icon mascots, no playful symbol systems, no hero-page spot icons. The brand uses photography in every place where another luxury brand might use a hero icon.

### 6.7 Icon philosophy

The strategic interpretation: icons on Lexus are functional, not decorative. They exist to label a control or a small piece of meta-information, never to communicate brand voice. The brand voice is carried by photography and typography. This is consistent with the brand's preference for restraint and for letting the vehicle imagery do the chromatic and emotional work.

## 7. Photography Style

Photography is the dominant visual language on both Lexus properties. It is also the most consistent expression of the brand across all touchpoints.

### 7.1 Vehicle photography

Vehicle photography is studio-grade, dramatic, and dark. The default treatment is the vehicle photographed against a black or near-black background (often a dark cyclorama or a darkened set), lit with cinematic side-light that emphasizes the body's surface tension and the light-catch on the spindle grille and the body lines. Reflections on the paint are deep and saturated, with a slight cool-blue cast even on warm-paint vehicles. The camera position is consistently slightly low (front-three-quarter, often at ground level), giving the vehicles a heroic, monumental feel. Shutter speed and aperture imply a deliberate stillness; there is no motion blur and no rolling-shutter effect.

A second treatment exists for the Electrified line and the LC convertible: lighter sets, often outdoors, with available natural light. Used sparingly. The dark studio look is the default.

### 7.2 Lifestyle / editorial photography

Lifestyle photography on lexus.com is minimal and used primarily for the About pages and the Destinations section. Photographs feature people with deliberate-but-natural styling, in environments that evoke hospitality (a hotel lobby, a private resort balcony, a tea ceremony, a craft workshop). The color grading is warm but desaturated, suggesting a film-stock negative more than a digital RAW. Models are diverse in age and ethnicity but uniformly dressed in tailored, neutral-toned clothing (no logos, no patterns).

discoverlexus.com lifestyle photography is more editorial, more art-directed, and more international. The Milan Design Week 2026 cover photograph that anchors the global homepage at the time of this audit is a pure editorial image: a backlit installation in an Italian palazzo with the LF-ZC concept centered, no people, color graded toward warm sepia. The art direction reads as fashion-magazine.

### 7.3 Hero / banner imagery

Hero imagery is full-bleed, 16:9 to 21:9 aspect ratio depending on the page, with the model nameplate (LEXUS LX, LEXUS RX, etc.) typeset in Nobel Bold white in the lower-right or lower-center. There is no overlay band or gradient bar; the image is rendered untreated with text placed on top in a low-contrast area chosen by the photo retoucher.

Hero overlays on darker images use a subtle radial darken at the bottom of the frame to maintain text legibility, but no aggressive gradient is applied. The image quality on retina displays is sharp with minimal compression artifacts; the brand uses high-bitrate image delivery via Toyota's `tmna.assetscs.toyota.com` CDN.

### 7.4 Collection / category page imagery

Category landing pages (Performance, Electrified) lead with a hero photograph that aggregates the line's representative vehicles. The Performance landing aggregates the RC F, LC, LC Hybrid, and LC Convertible. The Electrified landing aggregates the RZ, RX hybrid, NX hybrid, ES hybrid. The aggregation is composed (not single-image), with each vehicle photographed individually and assembled in a shared scene.

### 7.5 About / brand-story imagery

About / Manufacturing photography centers on the Tahara, Miyata, and Motomachi production facilities, with images of Takumi craftspeople performing micron-precision tasks (alignment, leather stitching, paint). The photography is quiet and respectful, without the action-cinematography common to industrial brand campaigns. Hands and faces are both featured.

About / Technology photography centers on engineering benches, wind tunnels, and test tracks. The treatment is more clinical, with overhead and side-on compositions emphasizing the engineering object rather than the engineer.

About / Environment photography centers on the Lexus environmental commitments, including hydrogen fuel cell development and BEV production. Photography here is the lightest in the lineup, frequently using exterior natural-light treatments of the production facilities or the vehicles in landscape settings.

### 7.6 Image aspect ratios by context

- Hero photography: 16:9 to 21:9 desktop, 4:5 to 3:4 portrait on mobile.
- Model card images on the all-models page: 4:3.
- PDP gallery images: 16:9.
- Editorial inline imagery: 3:2 to 16:9, varies by article.
- Pull-quote spread images: full-bleed 21:9.

### 7.7 Color grading / filtering

The color grade across lexus.com is consistent: deep blacks, cool-mid neutrals, slight blue cast on highlights, controlled saturation on paint colors, almost no warm tones in the shadows. The visual reference is darkroom black-and-white printing crossed with luxury watch advertising. The grade is applied at the asset-creation stage; there is no CSS filter applied client-side.

The grade on discoverlexus.com is broader. Editorial features run warmer (sepia-tinted), product features run cooler (matching the US tone), and lifestyle features run more naturally (less aggressive grade).

### 7.8 Image quality and resolution

Images are delivered at high bitrate from `tmna.assetscs.toyota.com` (the shared Toyota North America asset platform) via Adobe Dynamic Media URLs (e.g., `Lexus_logo_4E4ABD922583A135140CD1AC3C6CAFF83B074DF4-864x600.jpg?wid=680&hei=452`). Retina-quality assets are served via the same `wid` query parameter at higher pixel densities. The delivery is sharp, with minimal banding and no visible JPEG block artifacts.

### 7.9 Notable patterns

Recurring visual motifs include: the cantilever shadow under a low front-three-quarter shot, a deliberate light-catch on the spindle grille (often a single source of warm light against the otherwise cool grade), the L emblem rendered as a small white element in the lower-right of the frame as a watermark on selected campaign images, and the use of architectural backdrops (palazzo, modern hospitality, Japanese ryokan) for lifestyle shots.

### 7.10 What is NOT shown

Lexus deliberately avoids certain imagery types:

- No driving-action shots with motion blur or roll cages or skid marks.
- No "family on the beach" lifestyle shots typical of mainstream automotive marketing.
- No urban congestion, traffic, or commute photography.
- No product staging that places the vehicle in an obviously-staged retail showroom (the Lexus dealer showroom does not appear in marketing photography).
- No competitor mention, comparison, or reference imagery.
- No discount, promotional, or sale-styled photography.
- No close-up celebrity portraiture.
- No cartoon, illustration, or AI-rendered imagery.

The absence list is more rigorously observed than the presence list. The brand's visual atmosphere is defined by what it refuses to show.

## 8. Brand Voice & Language Style

This section documents the deepest part of the Lexus brand expression. The voice is calibrated, consistent, and quietly assertive.

### 8.1 Tone & emotional register

The Lexus tone is calm, confident, and craft-oriented. It is not aspirational in the way Mercedes is aspirational, and it is not technical in the way BMW is technical. It is closer in register to a quiet luxury fashion house (The Row, Loro Piana) or to a Japanese craft maker (Hermès in their Japanese-design partnership, or a high-end Kyoto ceramics studio). The brand evokes patience, refinement, and a respect for the customer's intelligence.

The tone shifts subtly by page type. The homepage is the most lyrical, with single-sentence brand statements accompanying hero photography. The Model pages are more declarative ("Crafted to elevate the driver and the driving experience to unprecedented heights, this is the next chapter of flagship luxury" (from the LX page meta description). The About pages are quietly philosophical, with short paragraphs that read closer to a craft-maker manifesto than corporate copy. The Owners and Service pages are direct and instructional, with the same Nobel Book typography but a more functional voice.

The brand explicitly avoids: urgency, discount language, hype, exclamation points (almost never used), interrogative headlines (rarely used), self-congratulation, comparison to competitors, technical jargon as marketing copy, and any reference to "performance" without grounding it in craftsmanship.

### 8.2 Narrative voice

Lexus writes primarily in the third person ("Lexus" is referred to as a singular entity, "Lexus pursues perfection") and the second person ("you" is used directly to the reader on Model pages and About pages, e.g., "Crafted for those who refuse to settle"). First person plural ("we") is used on the About pages where the brand speaks as a collective ("Innovation is in our DNA. See how we strive to think in ways we never have before").

Active voice is dominant. Passive constructions are rare and used only for technical specifications. Sentence length is short to medium, with a consistent rhythm of three-to-four words → eight-to-twelve words → a short fragment for emphasis. The brand frequently uses sentence fragments as emphasis in headlines and pull-quotes ("Crafted. Refined. Lexus.").

Storytelling is present but restrained. The Takumi craftsperson narrative is the most-used recurring story on the About / Manufacturing page. The Spindle grille design narrative is the second. The L Finesse design philosophy is the third. These are the brand's three creation myths, and they recur across decades of brand expression.

### 8.3 Heading patterns

Headings on Model pages follow a short-declarative pattern: two to four words, mostly verbs and nouns, sentence case, no terminal punctuation. Examples include "All-New," "Reimagined," "Crafted Perfectly," "Forge Ahead," "Take Flight," "Seamless Connectivity," "Driver-Inspired."

Headings on About pages follow a slightly longer poetic pattern: four to ten words, often two-clause structures with an internal turn. Examples include "The pursuit of perfection is never finished," "Our work is of the highest quality because our work is never done."

Headings on the homepage are the most lyrical: short brand statements set in display Nobel Bold across full-bleed photography. The current hero rotation includes treatments like "Experience Amazing" (the master tagline) and model-specific lines that pair with each rotating hero.

Capitalization follows sentence case (or title case on shorter labels). All-caps is reserved for utility text (buttons, labels, eyebrows). No headline on the live site is set in all-caps.

Punctuation in headings is minimal. Periods occur on declarative lines ("Crafted. Refined. Lexus."). Colons are used to introduce a clarifying subhead. Em dashes do not appear. Exclamation points do not appear. Question marks appear rarely, only on rhetorical headings.

### 8.4 Complete CTA inventory by page context

The verbatim CTA labels observed across both properties:

Homepage hero:
- Explore [Model]
- Build Your [Model]
- Discover Amazing
- View Inventory

Homepage section:
- Explore the Lineup
- Build Your Lexus
- View All Offers
- Find a Dealer
- Read More
- Watch Now (on video tiles)
- Discover the Story (on Lexus Magazine featured stories)

Collection / PLP:
- Explore [Model]
- Build [Model]
- View Specs
- Compare Models

PDP:
- Build Your [Model]
- View Inventory
- Find a Dealer
- View Offers
- View Photos
- View Specifications
- Schedule a Test Drive
- Request a Brochure
- View 360°
- View Trims
- View Color Options

Editorial / content (Lexus Magazine, About):
- Read More
- Continue Reading
- Discover [Topic]
- Watch the Film
- View the Gallery

Footer:
- Subscribe (newsletter)
- Find a Dealer
- Build Your Lexus
- Lexus on Facebook / Instagram / X / YouTube / LinkedIn
- Contact Us

Support pages:
- Submit (contact form)
- Send Message
- Continue
- Save and Continue (configurator multi-step)
- Print
- Request Roadside Assistance

Custom / B2B:
- Request a Quote
- Lexus Fleet
- Inquire About L/Certified
- Request a Brochure

Cart / checkout: not applicable (no direct-purchase flow).

discoverlexus.com global:
- Stories
- Models
- Change region
- Visit your local Lexus
- Read More
- View the Story
- About Lexus
- Global pressroom

The CTA verb set is small. "Explore," "Build," "View," "Discover," "Find," "Read," "Watch," "Schedule," "Subscribe," "Visit," "Request." There is no "Buy," no "Order," no "Get," no "Shop." "Buy" is the most-avoided verb on the site, because Lexus's relationship with the buyer runs through the dealer. The brand's CTA verb of choice is "Build," which functions as a soft alternative to "Buy" because it suggests authorship rather than transaction.

### 8.5 Product description formula

Model page descriptions follow a four-part formula:

1. Opening hook: a single declarative sentence that names a feeling or design intention. ("Crafted to elevate the driver and the driving experience to unprecedented heights, this is the next chapter of flagship luxury.". LX)
2. Body paragraph(s): two to four short paragraphs of feature highlight, organized by topic (Design, Performance, Interior, Technology, Safety).
3. Specifications table: a structured breakdown of trim levels, dimensions, powertrain options, EPA-estimated fuel economy.
4. Closing CTA: typically "Build Your [Model]" or "Find Inventory."

Average length of the descriptive copy: approximately 150 to 300 words per Model page (excluding feature blocks and specification tables). The copy is dense with adjectives describing materials and craftsmanship (handcrafted, hand-stitched, hand-pleated, supple, refined, deep-dyed, matte-finished). Technical language is grounded with sensory language. Sensory language is grounded with technical language. The two are deliberately interwoven so the customer doesn't have to choose between "luxury copy" and "spec copy."

### 8.6 Recurring language patterns

Phrases that recur across multiple pages:

- "Experience Amazing": the master tagline, locked in 2013 and still in active use.
- "Crafted": the most-used verb, appearing in dozens of headlines and product descriptions ("Crafted to elevate," "Crafted for the drive," "Crafted for those who refuse to settle").
- "Pursues perfection" / "Pursuit of perfection": a phrase inherited from the original Lexus tagline ("The Relentless Pursuit of Perfection," 1989 to ~2013) and re-used with frequency on the About pages ("Discover the many areas in which Lexus pursues perfection: manufacturing, technology, the environment, and philanthropy").
- "Driver-inspired": used on Performance and Electrified pages.
- "Human-centered": used on Interior and Technology pages.
- "Refined": used as an adjective for the experience, the engine, the cabin, the ride, the design.
- "Refuses to settle": used as a positioning statement for buyers.
- "Never done" / "Never finished": used on the About / Manufacturing page.
- "Innovation is in our DNA": used on the About / Technology page.
- "Genuine respect and concern for the planet": used on the About / Environment page.
- "Takumi": the Japanese term for master craftsperson, used as a proper noun on the About / Manufacturing page.
- "L Finesse": the design philosophy, named and explained on the About / Technology page.
- "Omotenashi": the Japanese term for anticipatory hospitality, occasionally invoked on the Owners and Guest Experience pages.

The brand-specific vocabulary is small and heritage-oriented. Lexus does not invent new marketing terminology; it relies on a tight set of phrases that have been in use for decades.

How the brand refers to itself: "Lexus" (proper noun, never abbreviated, never preceded by "the"), "we" on About pages, and occasionally "Lexus, a Division of Toyota Motor Sales, U.S.A., Inc." in legal contexts.

### 8.7 Tone shift between properties

discoverlexus.com runs a notably different cadence. The headlines are shorter ("Welcome to Lexus") and more aphoristic. The copy is more abstract ("Where luxury and lifestyle meet, on the road and beyond"). The story headlines emphasize cultural events (Milan Design Week, the Lexus Design Award, the LF-ZC concept) rather than vehicle features. The voice on the global property is closer to a luxury lifestyle magazine than to an automotive manufacturer.

The US property runs a more grounded, more specific voice. It names features. It quotes prices. It directs to actions. It assumes the user is shopping. The split between "brand inspiration" (global) and "brand consideration" (US) is clean.

## 9. Platform & Technical Notes

### 9.1 CMS / Platform

lexus.com is built on Adobe Experience Manager (AEM). The infrastructure signals are visible in the markup: `aem-Grid`, `aem-GridColumn`, `etc.clientlibs/lexus/...`, `content/dam/lexus/...`, and the `react-page` template name in the head. The React layer is shipped as a single ~840 KB compiled bundle (`lexus-react.lc-dc523fe70410a1938d61417f6eb32186-lc.min.js` / `.css`). The compilation system is Adobe-standard (lc = "client library" hashed cache-buster).

discoverlexus.com is built on Nuxt.js (Vue), server-side rendered, with build markers in the head (`data-n-head="ssr"`). The site is maintained by the agency Resn (Auckland and Los Angeles), as evidenced by `resn:build = '43ea3f4'` and `resn:build-date = Wed, 22 Apr 2026 19:46:34 GMT` meta tags. The build was deployed six days before this audit.

### 9.2 Theme / template structure

The AEM template name is `react-page` and the body class on every page is `page basicpage`, which suggests Lexus uses one master AEM template and a single React app that handles all routing. This is unusual; most AEM implementations of this scale use multiple page templates per content type. The Lexus implementation centralizes everything in one React app and lets the React router (with Adobe Edge routing) determine the rendered component.

The content-page-ref hashes in the head (e.g., `tjcWlmhHPDXheu8xDg_J7A1pfklAfkWze-K9IpGc_-RQszSarGNvLnar962seTfD`) are AEM page references used for analytics and authoring. Every page has a unique hash.

### 9.3 URL patterns

lexus.com URL structure:
- `/`: homepage
- `/models`: all-models index
- `/models/{MODEL}`: Model Landing Page (LX, RX, ES, IS, NX, LC, GX, RZ, etc.)
- `/models/categories/{CATEGORY}`: category landing (performance, electrified, hybrid, sedan, suv, coupe)
- `/about`: About hub
- `/about/{TOPIC}`: About sub-page (manufacturing, technology, environment, philanthropy)
- `/build`: Build configurator entry
- `/build/`: Build configurator (with trailing slash)
- `/dealers`: Dealer locator
- `/electrified`: Electrified hub
- `/destinations`: Destinations by Lexus
- `/lcertified`: LCertified pre-owned hub
- `/lcertified/models/{MODEL}`: LCertified by model
- `/owners`: Owners hub (in sitemap; some sub-pages return 404 in current build)
- `/contact`: Contact
- `/accessibility`: Accessibility statement
- `/My-Lexus`: sign-in landing for the My Lexus app
- `/motorsports`: Motorsports / racing
- `/financial`: Lexus Financial Services
- `/footer`: internal AEM page (404 to public)

discoverlexus.com URL structure:
- `/`: homepage
- `/articles`: Stories / Articles (currently redirects to homepage in this snapshot)
- `/stories` and `/models` are the main sections, exposed in the navigation

### 9.4 Third-party integrations

Visible third-party services on lexus.com include:
- Adobe Experience Manager (CMS / hosting)
- Adobe Helix / Edge (for CDN and analytics RUM via `helix-rum-js@%5E2/dist/micro.js`)
- Ensighten Tag Management (`https://nexus.toyota.com/toyotanational/l-com-p/Bootstrap.js`). Toyota's enterprise tag manager
- Google Maps (with a referrer-restricted browser key `AIza…[redacted]` exposed in the React config): used for the dealer locator
- TomTom Maps (with a browser key `V8Oe…[redacted]` exposed in the React config): used as an alternative or fallback for vehicle-routing visualization
- Salesforce Apex REST endpoint (`https://toyotamexico.my.salesforce.com/services/apexrest/`). used for lead-capture and CRM integration
- Toyota EOS endpoints (`eos.prod.toyota.com`, `oauth.orc.lexus.com/eos`, `vehicle-health.orc.lexus.com`, `vehicle-info.orc.lexus.com`). the Toyota Connected Services backend

discoverlexus.com is built on Nuxt with a custom static-site delivery (Statamic CMS, judging from the `_statamic/discover_lexus_social.jpg` social image path). It uses Vimeo or Vimeo-Player for video embedding (visible in the iframe sources).

### 9.5 Performance observations

lexus.com is moderate-to-fast. The HTML shell is approximately 11 KB per page. The React bundle is large (~840 KB CSS, plus a separate JS bundle), so the time-to-interactive is approximately 2 to 4 seconds on a typical broadband connection. Hero photography is delivered at appropriate resolutions via the AEM Dynamic Media transform. There is no aggressive lazy-loading of the hero, but below-the-fold imagery is lazy-loaded.

discoverlexus.com is faster on initial load (Nuxt SSR delivers fully-rendered HTML), but the inline-CSS payload is heavy (~146 KB of CSS embedded in the head). Subsequent navigation is fast because the Nuxt router hydrates client-side.

### 9.6 SEO title patterns

lexus.com Model page title pattern: `{YEAR} Lexus {MODEL}[DASH]Luxury {BODY_TYPE} | Lexus.com`, where `[DASH]` is a horizontal-dash glyph that varies between pages. The LX page uses a U+2013 en-dash, the RX and ES pages use a U+2014 em-dash, and the IS page reverts to an en-dash. The dash inconsistency is visible in the live SERPs and indicates that title metadata is hand-authored rather than templated.

About page title pattern: "About Lexus | {SUBTOPIC} | Lexus.com" (e.g., "About Lexus | Manufacturing | Lexus.com").

Other pages: "Lexus | Experience Amazing" (homepage and any unspecified-template page).

Title pattern notes: All titles end with `| Lexus.com` (with the literal domain, not just "Lexus"). This is a deliberate SEO choice that reinforces the URL in the search snippet.

### 9.7 Meta description patterns

Each Model and About page has a unique, hand-written meta description that summarizes the page's product or topic. Examples:

- LX: "Crafted to elevate the driver and the driving experience to unprecedented heights, this is the next chapter of flagship luxury."
- RX: "Crafted for those who refuse to settle: Discover the uncompromising luxury of the 2026 Lexus RX."
- ES: "The 2026 Lexus ES combines striking design with world-class luxury and offers a choice between an all-wheel drive and an exceptionally efficient hybrid powertrain."
- About / Manufacturing: "Lexus maintains its excellence in building vehicles throughout the world: Our work is of the highest quality because our work is never done."
- About / Technology: "Innovation is in our DNA: See how we strive to think in ways we never have before and push the boundaries in everything we do."
- About / Environment: "Lexus' environmental efforts are tireless: Not because of government mandates, but out of genuine respect and concern for the planet."

The descriptions are not templated. Each is written as a brand-voice paragraph, not as an SEO formula. This is rare at this scale of website.

### 9.8 Legal / policy page URLs

- `/privacy`: Privacy Policy
- `/privacyvts`: Vehicle Telematics System Privacy
- `/accessibility`: Accessibility Statement
- `/contact`: Contact (also functions as a routing page for service complaints)
- `/warranty`: Warranty information
- `/terms` (linked from footer; not directly in sitemap)
- `/california-do-not-sell` (CCPA, surfaced via the footer "Do Not Sell or Share My Personal Information" link)

### 9.9 Accessibility notes

The site exposes a full Accessibility statement at `/accessibility` and references compliance with WCAG 2.1 AA. ARIA labels are present on the major navigational elements (`aria-label="Main Navigation"`, `aria-label="Search"`, etc.). Skip-to-content links are not visible in the rendered HTML shell, which is a gap; React likely injects them at hydration. Focus management on modal open/close appears correct. Screen-reader landmark structure is consistent.

### 9.10 Structured data

JSON-LD structured data is present on the Model pages (`Vehicle` schema with `manufacturer: Lexus`, `model: ES`, `vehicleEngine`, etc.) and on the homepage (`Organization` schema with `Lexus` as the organization, `https://www.lexus.com` as the URL, and the standard social links). Breadcrumb schema is present on the Lexus Magazine articles. The structured data is hand-curated rather than auto-generated by the CMS, which suggests a deliberate SEO discipline.

### 9.11 Browser support and unsupported-browser fallback

lexus.com explicitly drops support for Internet Explorer and renders an inline modal that says "Internet Explorer is no longer supported on Lexus.com. Please access this site using a different browser. We recommend: Chrome, Firefox, Edge." The fallback is rendered server-side and shows browser logo icons (Chrome, Firefox, Edge) sourced from cdnjs.cloudflare.com. The presence of this fallback indicates a long-tail-IE customer segment in the Lexus demographic that the team continues to actively address.

## 10. Pages Scraped

The 21 unique URLs visited and analyzed during this audit:

Homepage / brand entry:
- https://www.lexus.com/: Homepage (US consumer)
- https://discoverlexus.com/: Global homepage (Lexus International)

Model Landing Pages (PDP):
- https://www.lexus.com/models/LX: 2026 Lexus LX (flagship luxury SUV)
- https://www.lexus.com/models/RX: 2026 Lexus RX (mid-size luxury SUV)
- https://www.lexus.com/models/ES: 2026 Lexus ES (mid-size luxury sedan)
- https://www.lexus.com/models/IS: 2026 Lexus IS (compact luxury sport sedan)
- https://www.lexus.com/models/NX: 2026 Lexus NX (luxury crossover)
- https://www.lexus.com/models/LC: 2026 Lexus LC (luxury coupe)

Category / collection pages (PLP):
- https://www.lexus.com/models: All Models index
- https://www.lexus.com/models/categories/performance: Performance category (RC F, LC, LC Hybrid, LC Convertible)
- https://www.lexus.com/electrified: Electrified hub (hybrid, plug-in hybrid, BEV)

Brand / About:
- https://www.lexus.com/about: About Lexus hub
- https://www.lexus.com/about/manufacturing: About / Manufacturing (Takumi craftsmanship, production)
- https://www.lexus.com/about/technology: About / Technology (L Finesse, innovation)
- https://www.lexus.com/about/environment: About / Environment (sustainability, hydrogen, BEV)

Lifestyle / experience:
- https://www.lexus.com/destinations: DESTINATIONS by Lexus (resort partnerships)

Pre-owned / certified:
- https://www.lexus.com/lcertified: L/Certified pre-owned hub

Configurator / shopping:
- https://www.lexus.com/build/: Build Your Lexus configurator
- https://www.lexus.com/dealers: Find a Dealer

Support:
- https://www.lexus.com/contact: Contact Lexus
- https://www.lexus.com/accessibility: Accessibility Statement

Editorial / global:
- https://discoverlexus.com/articles: Global Stories index (currently redirects to homepage)

The audit also reviewed three core CSS bundles to extract design tokens: `lexus-react.lc-dc523fe70410a1938d61417f6eb32186-lc.min.css` (~840 KB), `site.lc-2a6e83bfeea337c34c6d26e7eeb402c1-lc.min.css` (AEM container clientlib, ~390 KB), and `site.lc-33331d9b97706d3d692938f1ab7579f9-lc.min.css` (AEM container, ~103 KB), plus the inline style blocks of the discoverlexus.com homepage (~146 KB across 81 inline blocks). The XML sitemap at `/sitemap.xml` (569 unique URLs) was read in full to understand the site's information architecture.

---

*Audit completed April 28, 2026. Lexus is the second of two Toyota-family brands documented in the All Brand Standards database (Toyota was audited the prior day). The two are deliberately not coupled in this audit. Lexus operates with an independent design system, an independent voice, and an independent set of digital properties. Where this audit references Toyota, it does so only to mark the relationship between the parent corporation and the luxury division, not to imply shared design assets or copy patterns.*
