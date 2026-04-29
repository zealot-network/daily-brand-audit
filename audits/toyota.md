# Toyota Brand Standards Audit, extracted from https://www.toyota.com and https://global.toyota across 13 pages (April 2026)

Toyota operates two distinct, deliberately disconnected digital universes. The first, toyota.com, is the consumer-facing property of Toyota Motor North America (TMNA). It is a polished, lifestyle-led, conversion-oriented marketing site built on Adobe Experience Manager with a custom client library prefixed `tcom-`. It runs the proprietary Toyota Type family in five weights, dark cinematic photography, and a brand red (`#eb0a1e`) restricted almost entirely to the logo and small interface accents. The second, global.toyota, is the corporate property of Toyota Motor Corporation (TMC), headquartered in Toyota City, Aichi. It is a far older jQuery-and-Slick stack with snake_case naming, formal stakeholder-relations voice, date-stamped corporate news, and the full philosophical apparatus of the company including the Toyota Philosophy, the Guiding Principles, the Toyota Way, the Toyota Production System, and the Toyoda Principles. The two sites share almost nothing visually. They do not share a typeface, a grid system, a navigation pattern, or a tone of voice. They share a single brand red, a single three-oval emblem, and a single ethos, captured in two phrases that recur across both properties: "ever-better cars" and "Customer First." This audit treats both as one brand standard, because together they form the complete Toyota expression as it is presented to the world in 2026.

## 1. Color Palette

The Toyota palette is unusual among global automotive brands. The dominant page color across the entire consumer site is not red. It is black. Red is reserved as a brand-identification accent and is almost never deployed inside the user interface as a system color. The palette is engineered around photography first, with neutrals and grays carrying the surface load and red carrying the trademark.

### 1.1 Brand red

Toyota uses two near-identical reds. They are functionally the same color and probably represent two source files synced at slightly different moments in the design system's history.

`#eb0a1e` is the dominant Toyota Red. It appears in the inline SVG of the three-oval header logo on every page of toyota.com. The exact declaration in the embedded stylesheet of the logo SVG is `fill: #eb0a1e`. This is the red that sits in the top-left corner of every page on the consumer site, behind the white wordmark, in a square pad that anchors the entire visual identity.

`#E10A1D` is a marginal variant used in the cart-badge dot inside the header shopping-cart icon. It is one stop darker than `#eb0a1e` and one stop bluer. The two reds are visually indistinguishable on screen.

Toyota Red is deployed sparingly. It appears on the logo background, in a small cart badge, and as the underlying accent for primary action and focus states inside the compiled stylesheet. It does not appear in CTAs, in body copy links, in section dividers, in section backgrounds, or as a fill behind product photography. The visible red footprint on a typical toyota.com page is no larger than the logo square in the header. This restraint is deliberate. Toyota treats red as the trademark mark, not as an interface color. The interface itself is black, white, and gray.

### 1.2 Neutral palette

The neutral palette does the surface work on toyota.com.

`#000000`, pure black, is the dominant page background on the homepage marquee carousel and on every vehicle Model Landing Page hero. It is set per-component inside inline CSS custom properties named `--gradientBottomColor` and `--gradientTopColor`. It is the default canvas behind every piece of vehicle photography on the site.

`#111111`, near-black, is an alternate hero background used on a smaller subset of slides. It also appears as `--bottomOuterGradient` on the Tacoma and RAV4 hero overlays. The choice between `#000000` and `#111111` looks like a regression rather than a system signal. Both register as black to the eye.

`#F6F6F6`, very light gray, is the fill of the social-icon rounded squares in the footer. It is the lightest non-white surface in the visible inline color set and appears in bands on light-mode product cards.

`#606060`, mid gray, is the stroke color of the account icon in the header. It serves as the primary utility-line color for outlined icons.

`#FFFFFF`, pure white, is the universal ink on dark pages. It is the color of body copy on the homepage marquee, vehicle hero headlines, the wordmark inside the red square, the "Learn More" arrow, and most footer copy until the dark legal bar at the bottom.

There is no warm neutral, no cool neutral, no champagne, no platinum, and no off-white in the inline color set. The grays are flat. They are designed to recede behind the photography, which carries the chroma.

### 1.3 Cinematic gradient overlays

Every hero on toyota.com uses an inline gradient overlay to push the photograph toward darkroom contrast. The component class is `lifestyle-gradient` and it accepts the following CSS custom properties:

`--gradientSize`, `--gradientTopColor`, `--gradientBottomColor`, `--outerGradient`, `--innerGradient`, `--topGradientSize`, `--topOuterGradient`, `--topInnerGradient`, `--bottomGradientSize`, `--bottomOuterGradient`, `--bottomMiddleGradient`, `--bottomInnerGradient`, `--bottomMobileGradientSize`, `--bottomTabletGradientSize`, `--bottomDesktopGradientSize`, and `--bottomDesktopLgGradientSize`.

These tokens take values like `rgba(0,0,0,0.71)`, `rgba(17,17,17,0)`, `rgba(17,17,17,0.58)`, and on the RAV4 hero, the only non-neutral example, `rgba(188,74,43,0)`, a warm rust-orange. The system is engineered to fade the top and bottom of every hero photograph into the page so headlines and CTAs sit on rich darkness without a hard edge. The motion timing for slide transitions is governed by `--swipeTransitionEasing` and `--swipeTransitionDuration`, exposed for editorial tuning per slide.

### 1.4 Vehicle paint colors as brand voice

The paint-color naming on each vehicle line carries more emotional voice than the rest of the palette combined. From the legal cutlines beneath the heroes and product imagery:

Tacoma: Wave Maker, Black, Celestial Silver Metallic, Underground, Mudbath.
4Runner: Ice Cap, Everest, Cutting Edge, Bronze Oxide, Heritage Blue, Grayscape.
Land Cruiser: Meteor Shower, Heritage Blue, Grayscape.
Highlander: Heavy Metal, Storm Cloud.
Camry: Ocean Gem, Supersonic Red.
RAV4: Storm Cloud, Urban Rock.

These names function as the emotional palette of the brand. Where Mercedes-Benz codifies its color philosophy in CSS variables, Toyota codifies it in vehicle finishes. The color voice of the brand lives on the cars themselves and is propagated through legal cutlines, never through the interface.

### 1.5 Status and functional color

The captured inline HTML did not expose a dedicated status palette for error, success, or warning states. These tokens live inside the compiled `clientlib-sitev2.min.41ca8fac1f997d49a8bcb18076268be0.css` external stylesheet rather than in the page-level inline style declarations. By inference from button class naming (`button primary`, `button secondary`, `button transparent`), the system follows a conventional primary, secondary, tertiary hierarchy. There is no inline evidence of status color usage in the consumer pages.

### 1.6 Color as restraint

Read as a system, the Toyota palette assigns surface to black, ink to white, structure to gray, and trademark to red. The vehicles carry the chroma. Photographic gradient overlays carry the mood. Toyota's color choice is to almost not have one. The single deliberate brand color on the page is the red square that holds the wordmark. Everything else recedes so the cars and their paint can speak.

## 2. Typography

Toyota's consumer typography is anchored on a single proprietary typeface, deployed in five weights, with semantic numeric class names that hide the actual sizes from the markup and let the system reflow type at every breakpoint without changing the HTML.

### 2.1 The proprietary family

Toyota Type is the only typeface preloaded on toyota.com. It appears in five weight files, each linked as a `.woff2` preload in the `<head>` of every page:

`ToyotaType-Light.woff2`, `ToyotaType-Book.woff2`, `ToyotaType-Regular.woff2`, `ToyotaType-Semibold.woff2`, and `ToyotaType-Bold.woff2`.

All five files are served from `/etc.clientlibs/tcom/clientlibs/clientlib-site/resources/fonts/`, the AEM client library path. The five-weight ramp gives the system enough range for editorial display, body copy, micro-utility, and emphasis without pulling a second family. There is no italic in the preloaded set. There is no serif companion. There is no monospace. Toyota Type is the entire consumer typography.

A secondary internal alias, `tcomBold`, appears in a utility stylesheet line on the homepage. It is functionally a synonym for Toyota Type Bold, used inside legacy components that pre-date the proprietary family preload.

The corporate property at global.toyota does not use Toyota Type. It serves generic system fallbacks via classes like `.title`, `.font_b`, and `.font_s`, with all type rules in `/pages/contents/css/common.css`, `common_en.css`, `parts.css`, `header_footer.css`, `style_list_en.css`, and `global_top_20240409.css`. The corporate site does not preload any custom typeface. This is one of the sharpest visual divergences between the two properties.

### 2.2 Semantic numeric type scale

The toyota.com type scale is exposed through class names, not CSS variables. The naming is structural rather than visual. The system has at least these levels in active use:

`heading-01` and `heading-01-b`. The largest display sizes. Used for top-level page titles. The All-Vehicles page H1 reads `<h1 class="ttac-headline heading-01-b">Toyota Vehicles</h1>`. The `-b` suffix denotes a bolder weight at the same size step.

`heading-02`. Vehicle MLP hero titles. The Camry hero is `<h1 class="title heading-02">2026 Camry</h1>`. The Tacoma, RAV4, 4Runner, and Land Cruiser heroes follow the same pattern. This is the brand's largest editorial size on a vehicle page.

`heading-03`. Sub-section heads inside a page. Examples include "Transform routine drives into thrilling escapes." on Camry and "Find the right offer for you." on every MLP.

`heading-04`. Vehicle-card titles inside a carousel of vehicles, and feature-section heads such as "i-FORCE MAX Hybrid Powertrain."

`heading-05`. Spec-value labels paired with feature names, such as "Available i-FORCE MAX Hybrid Powertrain" set as a paragraph in a spec block.

`display-04`. A specialized display size used for large interface labels such as the "Matches" filter count on the All-Vehicles page.

`body-01`, `body-02`, `body-03`. The body copy ramp, used for descriptive paragraphs under hero headlines and inside feature blocks. The most common body class on the homepage is `body-03`, used for short editorial lines like "Discover the right drive for you."

`legal-01`, `label-01`, and `eyebrow`. The micro-utility tier. Eyebrow is the small uppercase label that sits above headlines. Legal-01 is the disclaimer text inside the cutline modals. Label-01 is the form-and-control label size.

The system is named on the same numeric scale across all type families, which means a designer can reason about hierarchy without remembering specific pixel values. This is consistent with a modern AEM-driven design system, and it makes the markup readable from a content perspective rather than a visual-spec perspective.

### 2.3 Hierarchy in practice

A typical vehicle MLP follows a predictable type stack. The hero shows `heading-02` for the model name and year, with a paragraph at `body-02` for the starting MSRP. Sub-section blocks open with `heading-03` for the section concept and use `body-02` or `body-03` for the descriptive body. Spec blocks open with `heading-04` for the feature name and a paired `heading-05` for the spec value. Calls to action are set in the same Toyota Type at the size of the surrounding interface, not given a special type rank.

The corporate site uses a completely different system. Headings on global.toyota carry inline class names like `.title`, `.font_b`, and `.font_s` with no numeric scale. The visual hierarchy is established by typography size in CSS rather than by a token system. The type ramps from a large display heading on the editorial homepage tile down through body copy, captions, and date stamps formatted as "Apr. 02, 2026."

### 2.4 What Toyota's typography refuses

Toyota's consumer typography refuses to behave like luxury automotive typography. There are no thin neoclassical wordmarks. There are no oversized italic display headlines. There is no condensed sans-serif used for sub-brand logotypes. There is no shadow, no stroke, no all-caps editorial gesture. The brand voice in type is mid-weight, neutral, and engineered. Toyota Type at Semibold or Bold reads like a user-interface typeface that has been allowed to grow into editorial sizes. This is consistent with the brand position. Toyota does not present itself as a fashion object. It presents itself as a deeply engineered, deeply trusted product. The typography reflects that posture.

## 3. UI/UX Patterns

The Toyota consumer interface is engineered around a small set of repeating component patterns that work across every page on the site. The system is opinionated, consistent, and deeply instrumented for analytics and personalization.

### 3.1 Global header

Every page on toyota.com opens with the same global header. The structure is:

A red square containing the white three-oval mark anchored to the top-left corner. Three primary navigation buttons in the center: "Vehicles," "Shop," and "Support & Service," each implemented as `<button class="main-nav-link">` with sub-classes `select-vehicle`, `shopping-tools`, and `support`. A right-side cluster containing the shopping-cart icon with its red badge dot, the account icon for logged-out and logged-in states, and a hamburger for the mobile menu. A skip link that reads `<a href="#" class="skip">Skip to main content</a>`.

The header is sticky and does not change shape between vehicle pages, the homepage, and the All-Vehicles index. It is a single global component, externalized as an AEM experience fragment under `/content/experience-fragments/tcom/us/en/site/`.

### 3.2 Marquee and hero patterns

The homepage carries a five-slide autoplay marquee. The component class is `marquee-v2` with each slide as `marquee-slide-v2`. Slides autoplay at 8000 milliseconds per slide. Each slide carries a vehicle photograph, an eyebrow label, a `heading-02` headline, a short `body-03` line, and a single `button secondary dark no-image` CTA reading "Learn More" with the universal chevron arrow.

Vehicle MLPs use the `hero-v2` component instead of the marquee. The hero is a single looping autoplay video set as `<video autoplay="true" loop muted playsinline>` with a poster image fallback. The video autoplays muted on every load. The naming convention for the video files is `[VEHICLE-CODE]_MY[year]_WelcomeMat_TCOM_..._TYTW####000H.mp4`. Two file sizes are served, 768x538 for mobile and 1920x796 for tablet and desktop.

Below the hero on every MLP sits an "Info" button that surfaces a `data-cutline` modal containing the legal disclosure for the photography, listing trim levels and paint colors and noting "Options shown" or "Prototypes shown."

### 3.3 Sticky model subnav

Every vehicle MLP carries a sticky subnav below the main header. The class is `mlp-subnav-v4` with sub-classes `mlp-subnav` and `subnav-menu`. The subnav lists section anchors for each major page block such as `#performance`, `#overview`, and the section breadcrumb shows the model name and year together. The subnav is the primary way a user moves through a long MLP without scrolling back to the top.

### 3.4 Mobile-only sticky CTA bar

On mobile, the homepage and several vehicle pages carry a sticky bottom CTA bar with two action buttons. The two buttons are `<a class="button primary 10 block dark" href="/request-a-quote/">Request A Quote →</a>` and `<a class="button secondary 8 block dark" href="/kbb">Trade-In Value →</a>`. The numbers `10` and `8` in the class names are width tokens that govern flex sizing inside the bar. Primary is the higher-priority red equivalent in the system. Secondary is an outlined treatment.

### 3.5 Vehicle card grid and filter

The All-Vehicles page implements a faceted-filter component with a vehicle-card grid below it. The filter accepts six top-level categories as `<input name="vehicletype">` checkboxes: Cars, Electrified, Crossovers, SUVs, Trucks, Minivan. The card grid uses the `vehicle-cards` component with `vehicle-card` children. Each card carries a top-label band ("Hybrid EV," "Hybrid EV Available," "Plug-in Hybrid EV"), a jelly cutout vehicle image at a fixed angle, the model name, the year, the starting MSRP, and a "Learn More" CTA.

Jelly images are served from `https://tmna.aemassets.toyota.com/is/image/toyota/toyota/jellies/relative/2026/4runner/base.png` and similar paths, configurable via Adobe Scene7 query strings for size and crop.

### 3.6 Button system

The button system has at least these variants.

`button primary` is the highest-priority action. It renders as a filled button with white text on a dark fill on dark pages.

`button secondary` is the standard call-to-action style. It is most commonly seen with the modifier `dark no-image` on hero and marquee slides.

`button transparent` is the lowest-priority action, used for tertiary links inside content blocks.

`vis-button-inline-text` and `vis-control-cta` are inline text-style links used in legal cutlines and inside feature copy.

`text-link-inline` is the inline link inside body copy.

`info-button buttonDark` is the small "Info" button under hero photographs that surfaces the legal disclosure modal.

Every button is followed by an inline 12x12 chevron SVG with `fill="currentColor"` and a single path `d="M6.06825 0.905047C5.67772..."`. This arrow is the universal "Learn More" mark. It rotates by class for back-arrows and chevron variants but the path data is identical.

### 3.7 Spacing utility tokens

Spacing is governed by class-name tokens with explicit semantic values: `spacing-large-1-responsive-u-p`, `spacing-large-1-responsive-d-p`, `spacing-med-3-d-p`, `spacing-med-3-u-p`, `spacing-none-d`, `spacing-none-d-p`, and `spacing-large-3-r`. The naming convention encodes size (large, med, none), the numbered step within that size, the responsive breakpoint group (responsive, d for desktop, r for relative), and the side (u for up, p for padding). These tokens replace utility frameworks like Tailwind for vertical rhythm inside the component library.

### 3.8 State and theme classes

The system carries a small set of state classes that flag rendering posture: `dark`, `light`, `is-loaded`, `is-non-tablet`, `is-mobile`, `is-desktop`, `is-edited`, `is-lang-selector`, `hide`, `show`, `active`, `disabled`, `no-image`, `mobile-hide`, `nightshade`, `transparent`, `block`, `reverse`, `secondary`, `primary`. The `dark` and `light` classes drive the theme of an entire component subtree, allowing a single component implementation to render correctly on either a dark or light page background.

### 3.9 Geographic suppression flags

A unique feature of the toyota.com codebase is the dealer-region suppression system. Footer-level classes like `suppress-set`, `suppress-vi`, `suppress-pr`, `suppress-hi`, `suppress-boston`, `suppress-cat`, `suppress-chicago`, `suppress-cincinnati`, `suppress-denver`, `suppress-gst`, `suppress-kansascity`, `suppress-losangeles`, `suppress-newyork`, `suppress-portland`, and `suppress-sanfrancisco` correspond to Toyota's distinct dealer-network regions. Each can hide or show specific footer modules based on the user's geolocation. SET stands for Southeast Toyota, VI for U.S. Virgin Islands, PR for Puerto Rico, HI for Hawaii, GST for Gulf States Toyota. This is unusually granular regionalization for a national consumer site.

### 3.10 Personalization and analytics

Every interactive element on toyota.com carries Adobe Analytics attribution attributes: `data-aa-action`, `data-aa-content-section`, `data-aa-component`, and `data-aa-link-text`. The "aa" prefix denotes Adobe Analytics. These attributes drive the click-tracking taxonomy that feeds reporting dashboards. Adobe Target is wired through a global mutation observer that watches for `at-element-marker` insertions, which is how Target's experience swaps are stitched into the live page. The personalization layer is invisible to the visitor but is one of the most thoroughly instrumented in the auto industry.

## 4. Voice and Tone

Toyota carries two voices, one per property, and they are sharply distinct.

### 4.1 Toyota.com (TMNA) consumer voice

The consumer voice is short, present-tense, second-person, and emotional. Every marquee slide and hero block is a four-to-six-word lifestyle headline followed by a single CTA.

Representative homepage marquee headlines:

"Make every day a play day." (Tacoma)
"Our heritage. Your adventure." (Land Cruiser)
"Go where the road inspires." (Highlander)
"Discover the right drive for you." (All-Electric Family)

Representative section heads on vehicle pages:

"Built for the bold." (Tacoma)
"Powerfully dynamic." (Tacoma)
"Transform routine drives into thrilling escapes." (Camry)

Representative descriptive body, from the Land Cruiser MLP:

"Land Cruiser stays true to its roots with a bold, heritage-inspired design built for modern exploration. Featuring a classic 'TOYOTA' heritage grille, squared-off side mirrors and athletic fender flares, this icon is reimagined for today's adventures, whether tackling rugged trails or roaming city streets with confidence."

The vocabulary clusters into three emotional spaces. Trail and adventure language sits on trucks and SUVs. Family and lifestyle language sits on minivans and sedans. Capability language sits on the GR performance line and on TRD trims. The tone never lectures, never moralizes, and never asks the reader to think hard. It signals an emotional space and offers a CTA.

CTAs on the consumer site are functional: "Learn More," "Build," "Explore," "Request A Quote," "Trade-In Value," "Find a Dealer," "Build & Price," "View Offers," "Manage Preferences," "Schedule Service."

Disclaimers are written in warm second-person language. The external-link interstitial reads:

"You are now leaving Toyota.com. We're taking you to [3rd party website address] to connect you to the information you requested. Please note that we do not control and are not responsible for that website's content, products, services, or privacy or security practice. The website may independently collect your personal data and web usage information. Please review the privacy policy that may be posted on that website to learn more about the data handling practices on the site."

This is a legal notice rendered in customer-service language. It is unusually warm for a compliance modal and is consistent with the broader Toyota consumer voice.

### 4.2 Global.toyota (TMC) corporate voice

The corporate voice is institutional, third-person, formal, and stakeholder-bucketed. It is the voice of a publicly traded multinational addressing investors, regulators, employees, partners, and the press. Sentences are long and compound. The vocabulary is philosophical.

Representative passages from the Mobility page:

"Toyota is shifting toward a 'mobility company' in this once-in-a-century period of profound transformation. We are striving toward our goal of realizing the future mobility society. With an unceasing passion for beloved cars, we will remain committed to delivering ever-better cars to our customers."

From the Sustainability page:

"We, Toyota Motor Corporation and our subsidiaries, have inherited the spirit of 'Toyoda Principles' since our foundation, and have aimed to create a prosperous society through our business activities, based on 'the Guiding Principles at Toyota.'"

"We aim to be the 'best company in town' that is both loved and trusted by the people."

"We will contribute to the sustainable development of our society/planet by promoting sustainability, as we have, under the 'Toyota Philosophy,' based on the Sustainability Fundamental Policy and individual policies."

Repeating phrases across the corporate site: "Producing Happiness for All," "ever-better cars," "ever-changing innovation," "best company in town," "beloved cars," "Customer First," "Mutual Trust and Mutual Responsibility."

The corporate site organizes content under five stakeholder buckets: Customers, Employees, Business Partners, Shareholders, and Global Society / Local Communities. Each bucket carries a numbered Guiding Principle attached to its content. Date stamps follow the format "Apr. 02, 2026" on every news item, which gives the corporate site a newsroom posture.

### 4.3 The two-voice architecture

The split is intentional. TMNA owns the consumer relationship in North America and writes for the buyer and the owner. TMC owns the institutional identity for the global parent and writes for stakeholders. The two voices do not contradict each other. They occupy different registers of the same brand. A person who reads only toyota.com sees a friendly, lifestyle-led automaker who builds trucks for adventure and sedans for family life. A person who reads only global.toyota sees a Japanese industrial firm with a hundred-year philosophical lineage and a stakeholder-relations apparatus to match. Both are accurate. The brand sits on top of both.

### 4.4 What Toyota's voice refuses

The consumer voice never preaches sustainability at the visitor. The Beyond Zero pitch appears on individual vehicle pages and on the Electrified family hub, but it does not dominate the homepage or take over every product page. The corporate voice never markets vehicles. There are no MSRP figures, no trim names, no jellies on global.toyota. The two voices respect the boundary. The consumer voice respects the buyer's attention. The corporate voice respects the institution's seriousness. Neither imitates the other.

### 4.5 The missing tagline

Toyota in 2026 does not operate under a single global consumer tagline. "Let's Go Places," the long-running TMNA tagline of the 2010s, has been retired and does not appear in any captured page on the consumer site. "Start Your Impossible," the global Olympic-era tagline, survives only as a whitelisted external destination at startyourimpossible.com inside the external-link disclaimer modal. The closest thing to a current umbrella idea on toyota.com is the homepage section heading "Discover Toyota," but this functions more as a navigation cue than a brand promise. The corporate site uses "Producing Happiness for All" as an institutional mantra but does not push it to the consumer side.

The brand is operating in 2026 without a fixed tagline at the umbrella level and instead expresses itself through rotating, model-specific, four-to-six-word lifestyle headlines. This is unusual for a top-five global automaker and is a deliberate strategic choice that prioritizes product-level emotional storytelling over umbrella-level brand assertion.

## 5. Photography and Imagery

Toyota's consumer photography system is one of the most disciplined in the auto industry, with a clear hierarchy of formats, sources, and treatments.

### 5.1 Looping muted video as primary hero

Every vehicle MLP opens with a looping muted autoplay video. The implementation is `<video autoplay="true" loop muted playsinline>` with a poster image fallback for slow-network conditions. The video is paired with a `lifestyle-gradient` overlay that darkens the top and bottom of the frame so headline copy sits on rich darkness without requiring a hard-edged caption block.

Video file naming follows the convention `[VEHICLE-CODE]_MY[year]_WelcomeMat_TCOM_..._TYTW####000H.mp4`. The "WelcomeMat" suffix suggests an internal naming convention for the hero loop. Two file sizes are served, 768x538 for mobile and 1920x796 for tablet and desktop, both as `.mp4`.

### 5.2 Adobe Scene7 dynamic media pipeline

All non-video imagery on toyota.com is served from `https://tmna.aemassets.toyota.com/is/image/toyota/...`. This is Adobe Scene7, the dynamic media component of AEM. Images are stored once at full resolution and resized on-demand via query string. A typical image URL ends with `?fmt=jpeg&fit=crop&dpr=on,3&wid=1920`. This pipeline gives Toyota a single source of truth for every photograph and lets the system serve a perfectly sized, perfectly cropped, retina-aware image to every device without duplication.

Vehicle "jelly" cutouts, the transparent-background product images that anchor the All-Vehicles grid and the homepage card carousels, are served from a parallel path: `https://tmna.aemassets.toyota.com/is/image/toyota/toyota/jellies/relative/2026/4runner/base.png`. The "jellies" path is the same one Toyota uses for build-and-price configurator photography, which means the configurator and the marketing site share identical product imagery without any reconciliation work.

### 5.3 Photographic style

The cinematic style on consumer pages is consistent: lifestyle action shots, environmental drama, golden-hour or moody lighting, and photographic depth-of-field that places the vehicle in the foreground against a softened landscape. Trucks and SUVs sit in canyons, on dirt trails, in mountain settings. The Tacoma cuts through a desert wash. The 4Runner climbs a ridgeline. The Land Cruiser sits at a heritage angle in a wide landscape. The minivan and sedan photography moves to suburban and urban environments with family scenarios and clean architectural backdrops. The GR performance line gets motorsport-adjacent settings, often a track or a rural switchback.

Aspect ratios are uniform: 1920x796 desktop and 768x538 mobile. Every hero respects the same crop ratio so the composition reads cleanly at any screen size. The dark-mode treatment (`data-theme="dark"`) is the default. White type sits over rich photography. The brand voice in image is cinematic, weighted toward the natural world for trucks and SUVs and toward family life for sedans and minivans.

### 5.4 Alt text as utility, not brand expression

Alt text on toyota.com is sparse and functional: "slide bg image," "Model image," "Footer logo," "image," "Eyebrow logo." Decorative images carry `role="presentation"`. The descriptive marketing copy lives in the sibling `<h2>` and `<p class="copy">` elements rather than inside the `alt` attribute. This is acceptable accessibility practice when the marketing copy is adjacent to the image and the image itself does not carry information the user needs in isolation, but it is not best-in-class. A more rigorous brand might use alt text as another channel for emotional voice. Toyota does not.

### 5.5 The cutline as legal asset

Every hero photograph on a vehicle MLP carries an "Info" button that surfaces a `data-cutline` modal. The cutline lists the trim level, paint color, and any visual-effects disclosure. Representative examples:

Tacoma: "TRD Pro shown in Wave Maker with Black roof. TRD Off-Road shown in Celestial Silver Metallic. TRD PreRunner shown in Underground. TRD Sport shown in Mudbath. Options shown."

Land Cruiser: "Land Cruiser 1958 shown in Meteor Shower. Prototype shown with options. Production model may vary."

Camry: "XSE shown in Ocean Gem; SE shown in Supersonic Red. Vehicles shown with options using visual effects."

The cutline functions as a legal disclosure for the buyer who wants to know exactly what trim and paint they are looking at. It is a brand-level commitment to specificity and transparency that few automakers match.

### 5.6 Corporate imagery

Imagery on global.toyota is editorial rather than cinematic. The "Our Picks" tile on the homepage carries pull-quote photography from Toyota Times articles. The Mobility page uses diagrammatic illustrations rather than photographs to explain CASE, TNGA, and CJPT. The Sustainability page uses quote-card image overlays such as the Vice Chairman Sato message: "I believe that our mission is to provide goods and services that make people throughout the world happy, or, in other words, to mass produce happiness." The corporate visual system treats imagery as a vehicle for executive thought leadership, not as a vehicle for product seduction.

## 6. Iconography

Toyota's iconography is built almost entirely from inline SVG, with no sprite sheet, and follows a tight set of conventions.

### 6.1 The three-oval emblem

The three-oval mark is the central brand asset. Its symbolism is documented in detail on the corporate emblem page:

"The two perpendicular ovals inside the larger oval represent the heart of the customer and the heart of the company. They are overlapped to represent a mutually beneficial relationship and trust between each other. The overlapping of the two perpendicular ovals inside the outer oval symbolize 'T' for Toyota, as well as a steering wheel representing the vehicle itself. The outer oval symbolizes the world that embraces Toyota. Each oval is contoured with different stroke thicknesses, similar to the brush art in Japanese culture."

The emblem is rendered in two main forms across the consumer site. The header uses a 32x32 inline SVG with a red square background (`#eb0a1e`) and the three ovals in white. The footer uses the horizontal black wordmark, served from the Adobe DAM at `https://delivery.tcom.assetscs.toyota.com/adobe/assets/urn:aaid:aem:caee6520-2e75-4408-b632-247c747a3e53/as/VIS_toyota_logo_horiz_black_RGB_2023.svg`. The filename "VIS_toyota_logo_horiz_black_RGB_2023.svg" suggests an internal "VIS" design system identifier with a 2023 revision date.

### 6.2 The TOYOTA → TOYODA naming history

The corporate emblem page also documents the wordmark itself. The original family name was Toyoda. The company adopted "Toyota" because, in the writing of the Japanese characters, "Toyota" is rendered in eight strokes, a number associated with wealth and good fortune in Japanese tradition. In phonetics, the unvoiced "t" is considered cleaner than the voiced "d." This dual consideration of phonetic clarity and stroke-count auspicious-ness is the basis of the wordmark.

### 6.3 The universal chevron arrow

Every CTA on toyota.com is followed by a 12x12 inline SVG chevron arrow with `fill="currentColor"` and the path data `d="M6.06825 0.905047C5.67772..."`. This single arrow appears in primary CTAs, secondary CTAs, inline text links, mobile sticky-bar buttons, and breadcrumbs. It is the universal "next" mark of the brand and inherits the color of its surrounding text via `currentColor`. There is no second arrow style. There is no "external link" arrow variant in the captured HTML.

### 6.4 Social icons

Footer social icons render as 40x40 rounded squares with `fill="#F6F6F6"` light-gray fills and 1px black strokes. The component classes are `tcom-icon-social-facebook`, `tcom-icon-social-youtube`, `tcom-icon-social-instagram`, and `tcom-icon-social-tiktok`. The four-platform set matches Toyota's active social presence.

### 6.5 Utility icons

Header utility icons follow consistent sizing. The shopping cart is 41x41 with the red `#E10A1D` badge. The account icon is 16x16 in the inline state and 24x24 when expanded into the menu. The hamburger is 32x32. The skip-link target is hidden in the visible UI but exposed to screen readers.

Functional icons inside the page system are referenced from `/content/dam/toyota/shopping-tools/`: `TDR-BuildPrice-32.svg` and `TDR-FindDealer-32.svg`. The "TDR" prefix likely stands for an internal program name. These are the icons that anchor the homepage Shopping Tools section.

### 6.6 No sprite sheet

Toyota deliberately does not use an SVG sprite sheet. Every icon is inlined into the HTML where it appears. This adds page weight but improves caching and color-inheritance behavior. The chevron arrow inside a button correctly inherits the button's text color via `fill="currentColor"`, which would not be possible with a sprite reference. The trade-off favors visual consistency over file efficiency.

### 6.7 The corporate iconography

Global.toyota uses a different icon system entirely. Icons there are referenced as classes like `ico_arw`, `ico_pdf`, `ico_blank`, with snake_case naming consistent with the rest of the corporate stylesheet. The arrow is a small triangular shape rather than a chevron. The PDF icon flags downloadable documents. The "blank" icon flags external links that open in a new window. The corporate site's iconography is older and more functional than the consumer site's.

## 7. Layout and Grid

The two Toyota properties run on different grid systems.

### 7.1 The toyota.com grid

The consumer site uses the AEM core grid: `aem-Grid aem-Grid--12 aem-Grid--default--12`, with column wrappers of `aem-GridColumn aem-GridColumn--default--12`. The grid is twelve-column at every breakpoint, with column-span tokens applied per child to control width. The default behavior is a full-width single column.

Components themselves are wrapped in `cmp-experiencefragment` blocks (AEM experience fragments), `cmp-carousel` for sliding carousels, `cmp-text` for prose blocks, `cmp-teaser__title` for headed teasers, and `cmp-contentfragment` for structured content references. These are all AEM core components that ship with the platform.

Section vertical rhythm is controlled by the spacing utility tokens described in the UI/UX section. There is no Tailwind-style utility framework. The spacing system is closed and curated.

### 7.2 Page-level layout pattern

A typical toyota.com vehicle MLP follows this structure from top to bottom:

Sticky global header. Sticky model subnav. Hero with looping video and overlaid headline. "Find the right offer for you" offer block with regional dealer offers. Performance section with a heading and feature carousel. Design section with a heading and feature carousel. Connectivity section with a heading and feature carousel. Spec table with `heading-04` feature names and `heading-05` spec values. Build and Price CTA block. Related vehicles carousel. Footer.

The homepage follows a different structure: marquee carousel, "Explore All Vehicles" card grid, "Shopping Tools" three-card row, "Discover Toyota" editorial block, footer.

The All-Vehicles page is split: filter chrome on top (six checkboxes for vehicle type, plus price, MPG, and seating filters), then a vehicle-card grid below sorted by brand-curated order.

### 7.3 The global.toyota grid

The corporate site uses an older HTML idiom. Sections are wrapped in classes like `sec_contents`, `sec_contents_narrow`, `sec_contents_spread`, with `sec_bg_gray` flagging gray-background sections. Editorial content blocks use `picks_area`, `picks_tile_link`, `picks_image`, `picks_title_wrapper`, `picks_category`, `picks_time`, and `picks_title`. Card grids use `tile_wrapper`, `grid_tile`, `grid_image`, `grid_detail`, and `grid_title`. The figure caption pattern uses semantic `<dt>` and `<dd>` for term and description.

The grid is implemented in CSS via `display: grid` rules in the older stylesheets, with breakpoints managed inline rather than through a token system. The corporate site is not a modern responsive grid. It is a careful 2020-era responsive build with snake_case class names and a simpler, more print-influenced page rhythm.

### 7.4 Footer layout

The toyota.com footer is one of the most structured in the auto industry. It opens with a top action row containing privacy and accessibility links on the left and a "Manage Preferences" button plus four social icons on the right. Below that, five collapsible columns:

Column 1, "Shopping Tools": Kelley Blue Book Trade-In Value, Build Your Toyota, Search Inventory, Find a Dealer, Shop Online With SmartPath, Special Offers, What Fits My Budget, Payment Estimator, Request a Quote, Toyota Certified Used Vehicles, Buy Parts & Accessories.

Column 2, "Vehicles": All Toyota Vehicles, SUVs, Trucks, Cars, Crossovers, Electrified Vehicles, Hybrids, Hybrid Cars, Hybrid SUVs, TRD Pro Series, Nightshade Series, Gazoo Racing, All Upcoming Vehicles.

Column 3, "Helpful Links": Dealers, Deals and Incentives, Audio Multimedia & Connected Services, Mobile Phone Compatibility, Mobility, Toyota Fleet, Toyota Financial Services, Southeast Toyota Finance, Toyota Insurance.

Column 4, "Owners": Owners Home, ToyotaCare & Maintenance Plans, Safety Recalls & Service Campaigns, Service Centers, Service Specials, Safety Hub, Schedule Service, Warning Lights, Manuals & Warranties, Manage Payments, Rent a Toyota.

Column 5, "About Toyota": Careers, About Us, Our Company, Toyota Outfitters, Newsroom, Toyota Global, Motorsports, Plant Tours, Partner With Toyota, Hydrogen Fuel Cell Solutions.

Below the columns sits the horizontal black wordmark logo, followed by Contact Us, FAQs, and Español links. The bottom legal bar carries the copyright and the dealer-region suppression flags.

The five-column structure is unusually rich. It functions as a site map, a product index, an owner-services portal, and a corporate-relations hub all at once. It is the canonical example of a modern automotive footer.

## 8. Component Library

The toyota.com component library is a custom AEM client library extending the AEM core component set. The naming prefix is `tcom-`.

### 8.1 Custom components

`tcom-header`, `tcom-footer`, `tcom-footer-grid`, `tcom-footer-bottom`, `tcom-footer-section`, `tcom-footer-logo`, `tcom-footer-social-section` carry the global chrome.

`tcom-mobile-only`, `tcom-icon`, `tcom-social-icon`, `tcom-social-facebook`, `tcom-social-youtube`, `tcom-social-instagram`, `tcom-social-tiktok` carry breakpoint-specific behavior and social-platform identification.

`tcom-picture`, `tcom-shopping-tools-panel`, `tcom-loading` carry image rendering, the homepage shopping tools row, and load-state behavior.

### 8.2 Marketing components

`marquee-v2` and `marquee-slide-v2` carry the homepage carousel.

`hero-v2` and `hero-wrapper` carry the vehicle MLP hero.

`lifestyle-gradient` carries the cinematic photo overlay system.

`feature-carousel-container` carries the vehicle-feature carousels inside MLPs.

`panels-wrapper` and `accordion_panel_cont` carry expandable content panels.

`vehicle-cards`, `vehicle-card`, and `vehicle-cards-filter` carry the All-Vehicles grid and its filter chrome.

`tabbed-container__title` carries tabbed editorial blocks.

`mlp-subnav-v4`, `mlp-subnav`, and `subnav-menu` carry the sticky model subnav.

`core-ttac` is the title-text-asset CTA component (`ttac-headline` is the H1 inside it).

### 8.3 AEM core components

The system also runs the standard AEM core components: `cmp-experiencefragment`, `cmp-carousel`, `cmp-carousel__item`, `cmp-text`, `cmp-teaser__title`, `cmp-contentfragment`, `cmp-contentfragment__element`. These ship with AEM and are used wherever a custom component would not add value.

### 8.4 The corporate component library

Global.toyota uses a different component vocabulary entirely: `picks_area`, `picks_tile_link`, `picks_image`, `picks_title_wrapper`, `picks_category`, `picks_time`, `picks_title`, `sec_contents`, `sec_contents_narrow`, `sec_contents_spread`, `sec_bg_gray`, `tile_wrapper`, `grid_tile`, `grid_image`, `grid_detail`, `grid_title`, `message_tile`, `message_tile_news`, `figure_block`, `figure_title`, `figure_description`, `text_block`, `local_nav`, `local_nav_list`, `local_nav_anchor`, `def_inline`, `ico_arw`, `ico_pdf`, `ico_blank`, `font_b`, `font_s`, `marginb1`, `marginb_half`, `pdgr1`, `pdgr2`, `margint1`, `margint2`, `disp_ib`, `text_underline`. Snake-case throughout, with no `cmp-` or `tcom-` parallel.

The two libraries do not share any class names. They are independent codebases that happen to belong to the same brand.

## 9. Platform Notes

Toyota's web stack is one of the most thoroughly engineered in the industry, with deep instrumentation for personalization, analytics, performance monitoring, and security.

### 9.1 The toyota.com stack

Toyota.com runs on Adobe Experience Manager (AEM) as a Cloud Service. The signature paths are `/etc.clientlibs/tcom/clientlibs/...` for the client library and `/content/experience-fragments/tcom/us/en/site/...` for content fragments.

The AEM grid (`aem-Grid--*`), AEM core components (`cmp-*`), and AEM experience fragments are used throughout. The custom client library (`tcom-*`) extends AEM with Toyota-specific marketing components.

Personalization runs through Adobe Target. The integration uses a global `at-element-marker` mutation observer that watches for Target's experience swaps to be inserted into the live page, then stitches them into the rendered DOM. This is a standard pattern for Target on a single-page-application or AEM-driven marketing site.

Analytics runs through Adobe Analytics. Every interactive element carries `data-aa-*` attribution attributes (`data-aa-action`, `data-aa-content-section`, `data-aa-component`, `data-aa-link-text`). This is the Adobe Analytics naming convention for click-tracking taxonomy.

Real User Monitoring runs through Helix RUM, served from `rum.hlx.page`. Helix RUM is Adobe's open-source RUM library, originally built for the Helix project (now part of Adobe Edge Delivery Services). This gives Toyota live performance data on every visitor without a third-party agent.

Bot management and edge security run through Akamai. The bot-management script `https://www.toyota.com/akam/13/...` is loaded on every page. Akamai cancelled the redirect chain for `/electrification/` and `/usa/our-story/` during this audit because the requests were flagged as automated. Akamai is also responsible for the geographic IP detection that drives the dealer-region suppression system.

### 9.2 Preconnect hints

The `<head>` of every page carries preconnect hints to: `googleapis.com`, `googletagmanager.com`, `doubleclick.net`, `demdex.net` (Adobe Audience Manager), `smetrics.toyota.com` (Adobe Analytics edge collection), `toyota.tt.omtrdc.net` (Adobe Target edge), `bluekai.com` (Oracle Data Management Platform), `dnn506yrbagrg.cloudfront.net` (an unidentified CloudFront origin), `cdn.dg.toyota.com`, `socket.dg.toyota.com`, and `api.dg.toyota.coms` (note the trailing "s" on the last domain, which appears to be a typo in the source HTML).

### 9.3 Service configuration

A global `window.tcom_env` object on every page exposes service endpoints for: `vehicleData`, `dis` (Dealer Inventory Search), `waldo` (likely a deal-finder service), `oat` (likely Owner Action Tracking), `connectedServices`, `handraiser`, and `handraiserSms`. The OAuth tenant is `TMNA_Owners` with the realm at the site root. This is the layer that underpins the owner-account flows, the inventory search, and the SMS hand-raise capture.

### 9.4 Schema.org structured data

Every page carries an `application/ld+json` block with at minimum a `WebPage` type, the canonical URL, and the icon image. There is no full vehicle schema on MLPs in the captured HTML, which is a missed opportunity for product structured data but consistent with how most automotive sites render to search engines.

### 9.5 Localization

The hreflang configuration covers `en-US`, `es-US`, and `x-default`. The Spanish mirror lives at `/espanol/`. There is no French, no Korean, no Vietnamese, and no Tagalog mirror, despite Toyota's significant California and Texas owner base in those languages.

### 9.6 The global.toyota stack

The corporate site is a different platform entirely. It runs jQuery 3.3.1, Slick carousel (`slick.css` and `slick.min.js`), and a set of per-page injected stylesheets including `/pages/contents/css/common.css`, `common_en.css`, `parts.css`, `header_footer.css`, `style_list_en.css`, and `global_top_20240409.css`. The custom JavaScript object `GT.navi.header.print()` injects the global header at runtime.

The corporate site carries snake_case class names, uses `<dt>` and `<dd>` for figure captions, and includes table-based notes blocks that pre-date the CSS Grid era. It was redesigned in October 2020 (the path `/pages/contents/css/20201013/style.css` carries the redesign date) with a 2024 update layered on top (`header_footer.css?v=2024050113`).

Article content IDs on the corporate site are 8-digit integers (e.g., `26617055`). Date stamps follow the `Apr. 02, 2026` format. The bot-management is also Akamai (`https://global.toyota/akam/13/1b44f51b`), but the site otherwise shares no infrastructure with toyota.com.

### 9.7 The two-stack architecture as brand strategy

The fact that Toyota runs two completely independent web stacks for its consumer and corporate properties is itself a brand decision. TMNA is free to build a modern, analytics-driven, personalization-heavy marketing experience without compromising the editorial pace of the corporate site. TMC is free to maintain its institutional voice on a stable platform without being pressured to adopt every new marketing-tech requirement. The two organizations operate independently and the brand sits on top of that independence rather than being constrained by it.

### 9.8 Edge geolocation observation

A diagnostic note from the audit: the homepage HTML carried `data-country-code="LU"` (Luxembourg) on the page wrapper, which appears to be the Cloudflare-or-Akamai edge geolocation of the request origin. The 404 template version returned `data-country-code="US"`. This attribute is used to drive country-specific footer content but is not a privacy concern. It is mentioned here because it shows up in any reverse-engineering audit and would be a question if the brand wanted to suppress edge-IP exposure in markup.

## 10. Brand Architecture and Sub-Brands

Toyota carries a layered brand architecture that spans vehicles, sub-brands, sister brands, and editorial properties.

### 10.1 The Toyota master brand

Toyota Motor Corporation, headquartered in Toyota City, Aichi, Japan, is the parent. It owns the three-oval emblem, the Toyota wordmark, and the underlying philosophical apparatus (the Toyota Philosophy, the Guiding Principles, the Toyota Way 2020, the Toyota Code of Conduct, the Toyota Production System, and the Toyoda Principles). Toyota Motor North America (TMNA) is the U.S. subsidiary that operates toyota.com, the dealer network, the marketing programs, and the service infrastructure. The two layers are visually distinct but operationally aligned.

### 10.2 Vehicle taxonomy

The All-Vehicles filter on toyota.com exposes six top-level vehicle types: Cars, Electrified, Crossovers, SUVs, Trucks, Minivan. The active model lineup as of April 2026 spans:

SUVs: Corolla Cross, RAV4, RAV4 Plug-in Hybrid, bZ, bZ Woodland, C-HR, Grand Highlander, 4Runner, Toyota Crown Signia, Highlander, Land Cruiser, Sequoia.

Cars: Corolla, Corolla Hatchback, Prius, Prius Plug-in Hybrid, Camry, GR86, GR Corolla, GR Supra, Sienna, Toyota Crown, Mirai.

Trucks: Tacoma, Tundra.

Performance: GR86, GR Corolla, GR Supra (also listed under Cars).

The footer adds two performance-and-aesthetic series: TRD Pro Series (the off-road performance tier) and Nightshade Series (the blacked-out aesthetic tier). Both are trim-level expressions that overlay the main lineup rather than separate brands.

### 10.3 Trim and series naming

Toyota's trim and series names carry their own emotional voice: TRD Pro, TRD Off-Road, TRD PreRunner, TRD Sport, Trailhunter, Limited, Nightshade, XSE, SE, Woodland, 1958 (a Land Cruiser heritage trim), Heritage. The TRD prefix denotes Toyota Racing Development, the in-house performance arm. The Nightshade naming denotes the blacked-out aesthetic package across multiple lines. Trailhunter and Woodland denote outdoors-oriented packages on the 4Runner and bZ Woodland respectively. The 1958 trim on Land Cruiser is a deliberate call-back to the year the original FJ40 Land Cruiser was introduced in the United States.

### 10.4 Powertrain naming

Toyota's hybrid and gas powertrains carry branded names: i-FORCE MAX Hybrid Powertrain and i-FORCE Gas Powertrain. These names appear most prominently on the Tacoma MLP and increasingly across the truck and SUV lines. The i-FORCE naming positions the powertrain itself as a brand asset, parallel to the way General Motors uses Duramax or Ford uses EcoBoost.

### 10.5 Beyond Zero and the bZ family

Beyond Zero is Toyota's electrification umbrella. The verbatim pitch appears on multiple vehicle MLPs:

"Beyond Zero is Toyota's vision to reach carbon neutrality with our products, services and operations, and go beyond, as we find new ways to make a positive impact on our planet and society. The Hybrid EV Camry is one of the many ways we are reducing carbon emissions to drive toward our Beyond Zero vision."

The product expression of Beyond Zero is the bZ family of battery-electric vehicles, including the bZ, the bZ Woodland, and the bZ7 (revealed at Auto Shanghai 2025). The bZ family is rolled into a Toyota.com sub-page at `/electrified-vehicles/all-electric-family/`.

The Mobility section on global.toyota lists Beyond Zero with a full sub-architecture: Hydrogen (FCEV, Hydrogen-powered Engine), Batteries, BEV, HEV, PHEV, CJPT, Carbon Neutrality Efforts through Motorsports, Carbon Neutral Fuel, and Carbon Neutrality Efforts in Tohoku. This is a serious institutional commitment to a multi-pathway carbon neutrality strategy.

### 10.6 Lexus

Lexus is Toyota's luxury sister brand. It is referenced in the toyota.com external-link whitelist (`https://www.lexus.com`) and in the global.toyota Mobility page as a separate "Lexus Brand" section linking to `https://discoverlexus.com/` (the Lexus International site). Recent corporate news on global.toyota references the Lexus ES alongside the bZ7. Lexus has its own design system, its own typography, its own dealer network, and its own brand voice. It is not part of this Toyota audit but it is part of the Toyota brand architecture.

### 10.7 Gazoo Racing and TRD

Toyota Gazoo Racing is the global motorsports brand. It is referenced in two places on toyota.com (the footer link and the external-link whitelist) and prominently on global.toyota (the mobility page lists "Motorsports (GAZOO Racing) → https://toyotagazooracing.com/" and the global homepage hero on April 27 2026 carried "Rally Islas Canarias / Ogier wins after thrilling TGR-WRT intra-team contest"). The GR vehicle line on toyota.com (GR86, GR Corolla, GR Supra) is the consumer expression of Gazoo Racing.

TRD (Toyota Racing Development) is the U.S.-focused in-house performance and off-road arm. TRD Pro, TRD Off-Road, TRD PreRunner, and TRD Sport are trim-level expressions of TRD across the truck and SUV lines.

### 10.8 Toyota Times

Toyota Times (`https://toyotatimes.jp/en/`) is the editorial property of Toyota Motor Corporation. It is treated on global.toyota as an "Our Picks" tile on the homepage, with a dedicated banner image (`bnr_toyotatimes_en_3.jpg`), but is not embedded into the main site nav. It functions as a sister editorial brand that publishes long-form journalism about Toyota's people, products, and philosophy. It is one of the few automaker-owned editorial properties that meets professional editorial standards.

### 10.9 Other Toyota properties

The external-link disclaimer modal on toyota.com whitelists the following Toyota properties:

`https://pressroom.toyota.com/`, `https://toyotaaudioandconnectedservicessupport.com/`, `https://autoparts.toyota.com/`, `https://www.toyotacertified.com/`, `https://www.toyotamobility.com/`, `https://www.startyourimpossible.com/`, `https://support.toyota.com/`, `https://www.lexus.com`, `https://careers.toyota.com/`, `https://privacy.toyota.com/`, `https://disconnectaccess.toyota.com`, `https://treehouse.pro/toyota/quote`, `https://gazooracing.com/`, `https://toyotasgamedaygiveaways.com/`, and `https://www.toyotatirecenter.com`.

This list is the operational map of the brand. Each domain is a separate property serving a specific function, from press relations (pressroom) to audio support (toyotaaudioandconnectedservicessupport) to certified pre-owned (toyotacertified) to careers (careers) to privacy (privacy). The brand architecture is wide. Toyota chooses to operate dozens of domains rather than collapsing them into a single site.

### 10.10 Japanese brand concepts as institutional spine

Five concepts form the institutional spine of the brand on the corporate site:

The Toyota Philosophy, formalized in 2020, is described on the Vision and Philosophy page as "Toyota's founding spirit and its signpost in transition to a mobility company."

The Guiding Principles at Toyota are described as "Toyota's basic principles in management and stance towards our stakeholders."

The Toyota Way 2020 and the Toyota Code of Conduct are described as the "Outline of tenets employees should embrace to carry out the Toyota Philosophy." The Code of Conduct is published as a downloadable PDF (`code_of_conduct_001_en_2.pdf`).

The Toyota Production System is described as "an all-encompassing production system that is at the very heart of Toyota's corporate philosophy and is characterized by continuous improvement." This is the public-facing expression of kaizen, although the literal word "kaizen" does not appear in the captured HTML.

The Toyoda Principles are referenced once on the Sustainability page: "We, Toyota Motor Corporation and our subsidiaries, have inherited the spirit of 'Toyoda Principles' since our foundation."

The repeating institutional phrases that surface across the corporate site are: "Producing Happiness for All," "Customer First," "Mutual Trust and Mutual Responsibility," "ever-better cars," "ever-changing innovation," and "best company in town." These are the institutional brand voice in compressed form.

### 10.11 Sub-brands deliberately not mentioned on toyota.com

The corporate apparatus described above is largely absent from the consumer site. A buyer browsing toyota.com is not asked to consider the Toyota Production System, the Toyoda Principles, or the Guiding Principles. The consumer site is product-led. The corporate site is institution-led. The brand architecture is layered so that each audience encounters the right depth of the brand at the right moment.

---

## Summary

Toyota's brand standards in 2026 are defined by a deliberate two-property architecture, a single proprietary typeface, a black-and-white interface palette anchored by a tightly held brand red, a cinematic photography system, and a layered brand-and-sub-brand structure that spans vehicles, performance trims, an electrification umbrella, a luxury sister brand, a motorsports arm, an in-house editorial property, and a hundred-year philosophical lineage.

The consumer expression on toyota.com is engineered for emotional product storytelling at scale. Five-weight Toyota Type runs the editorial system. Looping muted hero videos run the photography. Twelve-column AEM grids run the layout. A custom `tcom-` component library extends AEM with marketing-grade carousels, marquees, vehicle cards, and sticky model subnavs. Adobe Target, Adobe Analytics, Adobe Audience Manager, Helix RUM, and Akamai run the personalization, instrumentation, and edge security. Dealer-region suppression flags allow the same site to render correctly in Southeast Toyota, Gulf States Toyota, Hawaii, Puerto Rico, the Virgin Islands, and every regional market in between. The voice is short, present-tense, second-person, and emotional, expressed through rotating lifestyle headlines per vehicle rather than a single global tagline.

The corporate expression on global.toyota is engineered for institutional stakeholder relations. The site runs an older jQuery and Slick stack with snake_case naming and the formal voice of a publicly traded multinational. Five stakeholder buckets organize the content: Customers, Employees, Business Partners, Shareholders, Global Society and Local Communities. The Toyota Philosophy, the Guiding Principles, the Toyota Way 2020, the Toyota Code of Conduct, the Toyota Production System, and the Toyoda Principles form the institutional spine. The mantra "Producing Happiness for All" runs through the sustainability and mobility narratives. CASE, TNGA, CJPT, Beyond Zero, and the LUNAR CRUISER project run through the technology narrative.

The two properties share a single brand red (`#eb0a1e`), a single three-oval emblem with documented Japanese symbolism, and a single ethos expressed in two recurring phrases: "ever-better cars" and "Customer First." Almost everything else differs. They use different typefaces, different grid systems, different component libraries, different content management systems, and different voices. The brand architecture is built to accommodate this difference. A consumer in Texas browsing the new Tacoma never has to encounter the Toyoda Principles. An institutional investor in Tokyo reading the Sustainability Report never has to scroll past a starting MSRP. Each audience meets the brand at the depth that fits.

The most distinctive standards in the Toyota system, ranked by how rare they are in the global automotive industry:

The two-stack consumer-and-corporate architecture, with completely independent infrastructure, is unusual. Most global automakers run a single platform across all properties.

The deliberate restraint in red usage is unusual. Toyota's brand red is one of the most recognized in the world but appears on a typical page only in the 32x32 logo square and the 4-pixel cart-badge dot. Most red-anchored brands deploy their red far more aggressively.

The cinematic dark-mode default with white type on rich photography is unusual for a mainstream non-luxury automaker. Most volume brands skew lighter and brighter to signal accessibility. Toyota chooses a more cinematic posture even on mainstream products.

The semantic numeric typography scale (`heading-01` through `heading-05`, `body-01` through `body-03`, `legal-01`, `label-01`) is unusual. Most consumer marketing sites either use a Tailwind-style utility framework or named typography roles like `display-large` or `headline-medium`. Toyota's numeric scale lets the system reflow without changing the markup.

The dealer-region suppression flag system is unusual. Few national consumer brands carry this much region-specific footer logic in their public HTML.

The tagline absence is unusual. Toyota in 2026 is operating without a single global consumer tagline at the umbrella level, which is a strategic choice that prioritizes per-product emotional storytelling over umbrella-brand assertion. Most top-five global automakers operate under a fixed tagline.

The vehicle paint-color naming as primary emotional palette is unusual. The chroma of the Toyota brand lives on the cars themselves (Wave Maker, Celestial Silver Metallic, Mudbath, Meteor Shower, Heritage Blue, Ice Cap, Bronze Oxide, Ocean Gem, Supersonic Red) rather than in the interface.

The depth of Japanese institutional philosophy on the corporate site is unusual. Few global automakers carry a hundred-year philosophical lineage as visible content on their corporate property. Toyota's commitment to publishing the Toyota Philosophy, the Guiding Principles, the Toyota Way, the Code of Conduct, and the Toyoda Principles as live editorial content is a significant brand asset.

Read together, the standards make Toyota one of the most coherent multi-property brand systems in the global automotive industry, despite the surface impression that the two properties have nothing to do with each other. The consumer site is the product expression. The corporate site is the institutional expression. The brand sits on top of both, expressed through the red square, the three ovals, and the two phrases that recur across the system: "ever-better cars" and "Customer First."

---

*Audit compiled April 28, 2026 from 13 web properties across toyota.com and global.toyota. CSS values, copy, and class names are quoted verbatim from the live HTML at the time of fetch. Where design tokens live in compiled external stylesheets rather than inline declarations, they are noted as such and not reproduced. This audit reflects the public-facing expression of the brand only and does not draw on internal style guides or unpublished design documentation.*
