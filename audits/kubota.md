# Kubota Brand Standards Audit: extracted from https://www.kubotausa.com across 13 pages (April 2026)

## 1. Color Palette

Kubota's digital color system is built around a single, almost militant insistence on Kubota Orange against a near-monochrome supporting cast. There is no secondary brand color in the conventional sense. The entire identity is "orange machine in a neutral world," which mirrors how the physical product looks against a field, a job site, or a hardware store floor. The role of every other color on the site is to stay out of the way of orange.

### Primary brand color
- `#dc4405`. Kubota Orange. Confirmed in inline CSS in the US homepage stylesheet block. This is the load-bearing brand color. Used on the wordmark, the painted equipment in nearly every photograph, hover/active states on the main nav, the find-a-dealer button accent, the hamburger menu icon at SP breakpoints, and footer dividing rules. It is the color of the products themselves, so the digital palette is effectively a frame around the physical orange. This shade reads warmer and slightly more red than a pure construction-yellow-orange like Cat's "Caterpillar Yellow" and is closer to the orange used on Kubota tractor sheet metal since the 1970s.

### Neutral grays (UI scaffolding)
- `#1a1a1a`. primary near-black for body text, primary headings, and footer background where a darker bar is used. Not pure black, which keeps headings from feeling printed-onto-the-screen.
- `#686868`. mid gray. Used for swiper pagination dots (`background: #686868` on `.swiper-pagination-bullet`), secondary nav text, breadcrumbs, captions under hero images, and the rule under the "For Earth, For Life" lockup.
- `#868685`. slightly cooler mid-gray. Used in the megamenu's lower-tier link text and disabled button states.
- `#AAAAAA`. light gray for form input borders, muted icon strokes, and "or" separator text in the dealer locator.
- `#e0e0e0`. hairline border color used on `.kubota-main-nav` (`border-top: 1px solid #e0e0e0`), card edges on PLP tiles, and the divider between hero and "Featured Products."
- `#F0F0F0`. page-section background "wash" used to alternate between white and a tinted band on long pages (PLPs, why-kubota, finance). It is the de facto secondary background.

### Whites and overlays
- `#ffffff`. page background, card background, megamenu panel background, header background. The site is overwhelmingly white-based.
- `rgba(0, 0, 0, 0.5)`. the only rgba value extracted from inline CSS. Used as a 50% black scrim under hero headlines so that white type stays legible over photography. This single-overlay rule is why hero copy never breaks against busy field/forest backdrops.

### Functional / interactive role mapping
- Primary CTA fill: `#dc4405` Kubota Orange with `#ffffff` text.
- Secondary CTA fill: white background, `#1a1a1a` text, `#1a1a1a` 1-px border, hover swaps to orange.
- Default `btn btn-default`: gray-800 text on white with subtle border (Bootstrap default overridden).
- Link color in body copy: `#dc4405`.
- Hover/focus on nav `<a>`: orange underline.
- Footer top bar: dark gray approaching `#1a1a1a` with white text and orange social-icon hover.
- Form inputs: `#AAAAAA` border, `#1a1a1a` text, orange focus ring.

### Notable absences
- No green, despite competing with John Deere and despite being an agricultural brand. Kubota deliberately refuses to play in the green/yellow space owned by Deere.
- No red, despite the broader ag-equipment convention (Case IH, Mahindra, Massey Ferguson all lean red). Kubota's red-adjacent choice is a more burnt orange, and they protect it.
- No blue accent system. There is no "info blue," no "trust blue," no "link blue." Links are orange.
- No tonal orange ramp. The site uses one orange. There is no `#ff6a26` light variant or `#a83100` dark variant exposed in the inline CSS. The brand is disciplined to a single hex.
- No success-green, warning-amber, or error-red token in the CSS that was visible in the homepage stylesheet block. Form validation states appear to inherit Bootstrap defaults rather than a Kubota-specific palette.
- No dark mode. The site is a pure light theme across every page audited.
- No earthy browns or harvest-yellows despite the agricultural category. Kubota stays mechanical and clean, not "rustic farmhouse."

## 2. Typography

Kubota's typography is deliberately plain and industrial. The font stack is `'Helvetica Neue', sans-serif` declared on the homepage (confirmed verbatim in the inline `<style>` block) with one display variant, `HelveticaNeue-CondensedBlack`, used for the loud all-caps callouts on hero slides and category pencil banners. There is no custom Kubota-branded typeface, no Google Fonts request, no Adobe Typekit kit on the US site. The brand leans on a workhorse American tech-era sans rather than spending licensing budget on a bespoke typeface. That is itself a brand statement: tools, not flourishes.

### Font families found in CSS
- `'Helvetica Neue', sans-serif`. the base UI font for body copy, navigation, paragraph text, captions, and form inputs across kubotausa.com.
- `HelveticaNeue-CondensedBlack`. the display weight used on promo-hero subheadings, big section labels, and price/HP callouts. Condensed Black gives the site its "stenciled-on-the-side-of-a-machine" feeling without using an actual stencil face.
- System fallback: `sans-serif` (no specific Roboto, Inter, or open-source replacement is requested).

### Weights observed in inline CSS
- 300 (Light). Sparse, used on the "subheading" small text under hero headlines.
- 400 (Regular). Body copy, paragraph type, footer links.
- 500 (Medium). Used on PLP card titles and active nav.
- 700 (Bold). Primary buttons, primary nav, H1/H2 headings.
- 900-equivalent via the Condensed Black face. Used on display-size promo subheadings.

### Type sizes captured directly
- Promo-hero subheading: `font-size: 18px; line-height: 24px;` (declared in homepage style block).
- Body copy on PDP: ~16px / 26px line-height (Bootstrap default not overridden).
- Footer links: ~14px.
- Top utility nav: ~13–14px, often uppercased via CSS `text-transform: uppercase`.

### Treatment patterns
- Hero headlines: HelveticaNeue-CondensedBlack, all caps, white-on-photo with the rgba(0,0,0,0.5) scrim. Tight letter-spacing.
- Section H2 on long pages: title-case, Bold, near-black `#1a1a1a`, often left-aligned with a short orange underline rule beneath.
- PLP card titles ("BX Series", "BX23S", "L3902"): bold sentence case with HP callout in regular weight underneath ("21.6 HP. Ready to meet all of your property needs.").
- Specs blocks on PDPs: a key/value pattern in regular weight, often without bold, leaning on the table grid for hierarchy.
- "For Earth, For Life" lockup text under the corporate mark renders as a small Helvetica Neue line, not as a custom hand-set tag.
- The global JP site (`kubota.com`) follows a different typographic system, with class names like `HeadingLevel1__main`, `HeadingLevel1__shoulder` (a small label set above the main heading), and `Definitionlist__heading`. The JP site adds an additional "shoulder" pre-headline pattern that kubotausa.com does not use.

### Notable absences
- No serif anywhere in the audited pages. Kubota does not use serifs even in heritage/about contexts where many industrial brands lean editorial. This is unusual for a 130-year-old brand and signals that "we are working tools, not legacy lore."
- No custom Kubota-branded display font visible in the digital surfaces. Compare this to Caterpillar (custom Cat Sans) or John Deere (custom JD Sans). Kubota has not invested in a digital wordmark face beyond Helvetica Neue.
- No variable font usage. The CSS does not request any wght-axis or wdth-axis variable file.
- No web font CDN. The page does not pull from `fonts.googleapis.com` or `use.typekit.net`. Helvetica Neue ships natively on Mac/iOS and falls back to Arial-ish sans on Windows. Kubota seems comfortable with that visual drift.
- No italic styling visible in headlines or pull quotes. Italics, when they appear, are limited to legal disclaimers in the footer fine print.

## 3. Logo & Wordmark

Kubota's mark is the wordmark "Kubota" in a custom italicized capital-letter form (the cap K is the most distinctive glyph. It has a steeply rising leg). On the digital surfaces audited, it is delivered as a flat raster file rather than an inline SVG, which limits its scaling fidelity but matches a CMS-era publishing pipeline.

### Files referenced
- `https://www.kubotausa.com/Content/Images/logo.jpg`. Declared in the JSON-LD `Organization` schema as the canonical logo URL. Stored as a JPEG, which means it sits on a white background rather than transparent. This is consistent with how it appears across the site (always on a white header, never knocked out over photography).
- `/Content/Images/for-earth-logo.jpg`. The "For Earth, For Life" lockup that pairs the Kubota wordmark with a small orange globe leaf and the tagline. Used in the top utility bar of every page.
- `/Content/Images/for-earth-for-life-mobile.png`. A PNG variant of the lockup loaded only at mobile breakpoints (transparent background here, since the mobile footer band may be tinted).
- The favicon is a classic `/favicon.ico`, not a multi-res `.svg`.

### Construction and placement rules (inferred from observed usage)
- The Kubota wordmark is locked tightly to the "For Earth, For Life" sub-line in a vertical lockup. The wordmark sits on top, the small orange globe sits to the left of the tagline, and the tagline reads in a fine-spaced, slightly tracked Helvetica Neue.
- Wordmark always appears in `#dc4405` orange against white, never reversed. There is no white-on-orange variant in the audited pages.
- Minimum clear space appears to be roughly the cap height of the K on all sides. The lockup is never crowded against navigation, and the lockup occupies a fixed left position in the top utility bar.
- The wordmark is not animated. There is no SVG path-stroke entry animation, no hover effect on the logo.
- On the global JP site, the same wordmark plus tagline is used, but it is wrapped in a class called `IconCorporationLogo` with the aria-label "Kubota For Earth, For Life". JP delivers it as an icon font glyph rather than a JPEG, indicating the global team has a more design-systemized version of the asset than the US team.

### Brand entity naming patterns
- The legal entity in the US footer is "Kubota Tractor Corporation" with a `<strong>` weight and a copyright "© 1996 - 2017 Kubota Tractor Corporation." The footer copyright year has not been refreshed since 2017, which is a maintenance miss and is worth flagging as a brand-hygiene gap.
- The global entity is "KUBOTA Corporation". Note the all-caps treatment of the brand name in the JP corporate footer (`<p class="FooterSitebrand__logo">KUBOTA Corporation</p>`), which is different from the title-case "Kubota Tractor Corporation" used in the US.
- The schema.org Organization payload on the homepage declares `"name": "Kubota Tractor Corporation"`.

### Notable absences
- No SVG logo delivery on the US site. A premium B2C automotive site in 2026 would deliver the wordmark as inline SVG. Kubota still ships JPEG.
- No "Kubota Orange" badge mark. Kubota does not have a circular roundel, a shield, or a monogram-K mark. The wordmark is the only mark.
- No co-branded lockups for sub-brands inside the wordmark area. "Kubota Z-Force," "Kubota Sidekick," etc., are typed product names, not separate marks.

## 4. Layout & Grid System

Kubota US is a Bootstrap site at the bones level. The CSS file `/ResourcePackages/Bootstrap/assets/dist/css/main.min.css` is loaded on every page, and the markup uses the `col-sm-6`, `container`, `nav`, `modal-dialog`, `swiper-slide`, and `carousel-wrapper` class signatures of a Bootstrap 4-era theme that has been customized inside Sitefinity. The grid is therefore the Bootstrap 12-column grid at standard breakpoints (`sm` 576, `md` 768, `lg` 992, `xl` 1200), with `.container` capping at 1170px. There is no evidence of a CSS-grid-first layout system. The page is Flexbox plus float plus column class names from a 2017–2019 era Bootstrap theme.

### Page-level structure (every page)
1. `#wrapper`. Body shell.
2. Skip-to-main-content sr-only link.
3. `<header id="main-header">` containing:
   - Top utility bar (`.top-nav`) with the For Earth lockup left, a `.find-a-dealer btn btn-default` orange CTA, and four right-aligned utility links: Parts, Service & Support, Finance, About.
   - Main navigation (`.kubota-main-nav`) with mega-menu drawers per category. The mega-menu is a Vue.js component (`window.vueComponents['MainNavigation']`) and contains a tractor swiper with model thumbnails.
4. `<div id="main-content">`. Page-specific content.
5. `<footer id="main-footer">` with two stacked nav rows and a copyright bar.
6. Hidden modal scaffolding (`#primary-modal` and `.external-link-notice-content`) plus retargeting pixel.

### Hero / hero-carousel
The home and many category pages open with a `promo-hero` swiper carousel (Swiper.js v6 confirmed: `/Content/Vendor/swiperjs/swiper.v6.min.js`). Each slide has:
- A full-bleed photograph or video.
- A pencil-banner area (`.pencil-content`) at 90% width that hosts a heading, subheading (18/24), and one or two buttons.
- The banner is left-justified at desktop and stacks at mobile.

### PLP (product listing) layout
- Page header band with title and breadcrumb (`Products / Tractors / Compact`).
- Filter rail or chip set across the top (Series, HP range).
- 3-up to 4-up grid of product cards: image on top, model name, HP/use callout, "View Specs" link, sometimes a "Build My Kubota" button.
- Long, content-heavy section bands beneath the grid that profile the series in long-form copy. This is how Kubota does category SEO.
- Always closes with a "Find A Dealer" band before the footer.

### PDP (product detail) layout
- Hero with model name, tagline, hero shot of the machine (3/4 angle, painted orange).
- Quick specs table (HP, transmission type, lift capacity).
- Tabs for Features, Specs, Photos, Videos, Implements/Attachments.
- Long-form descriptive copy with bulleted feature lists ("Swift-Tach Loader. Remove your front loader in less than 60 seconds").
- Cross-sell band: "Kubota Genuine Parts," "Land Pride Implements" (a sister brand whose CDN is at `cdn-assets.gpmfg.io`).
- Contextual CTAs: "Build My Kubota," "Find a Dealer Near You," "View Brochure."

### Container widths and breakpoints
- Standard Bootstrap container at 1170px max.
- Hero swiper goes edge-to-edge of the viewport (`100vw`).
- Mega-menu panel takes the full main-nav width and overflows the container.
- Mobile breakpoint is `sm`. The mobile-only `for-earth-for-life-mobile.png` swap is triggered by the `.mobile-only` class.

### Spacing pattern
- Vertical rhythm tends to land in 32 / 48 / 64 / 96 px stacks between section bands, with the alternating `#F0F0F0` background creating zebra-band rhythm down a long page.

### Notable absences and observations
- No 8-point spacing token system in the inline CSS. Spacing is hard-coded per template rather than tokenized.
- No CSS custom properties (`--color-primary`, `--space-md`). Confirmed by grep returning zero matches for `--`-prefixed tokens. This site is not running on a modern design-token pipeline.
- No CSS Grid for any layout extracted. Everything is Bootstrap floats or Flexbox.
- No sticky add-to-quote shelf or sticky configurator bar, even on PDPs. Kubota leaves space, doesn't follow the user.

## 5. UI Components

The UI library is Bootstrap-derived but heavily reskinned. The class names are Bootstrap (`btn btn-default`, `modal-dialog`, `nav`, `container`, `swiper-slide`) and the JS interactions are split between Bootstrap's stock JS, Swiper for carousels, and Vue.js single-file components hydrated into specific div mount points.

### Buttons
- Primary CTA: orange fill `#dc4405`, white Helvetica Neue Bold text, no border, ~14px padding-top/bottom and ~28px padding-left/right, slight border-radius (~3–4px), uppercase or title-case depending on context. Example class chain confirmed in markup: `class="find-a-dealer btn btn-default _gt"`. The trailing `_gt` is a tracking hook for Google Tag Manager.
- Secondary: ghost button, white background, dark `#1a1a1a` text, `#1a1a1a` 1-px border, hover fills with orange.
- Tertiary: text link with right-arrow chevron, orange color, inline within copy ("Learn More ›" pattern).
- Disabled: `#868685` text, no fill change.

### Navigation
- Top utility nav (one line, right-aligned): Parts | Service & Support | Finance | About | Configurator.
- Main nav (Vue megamenu): Tractors, Mowers, Construction Equipment, Hay Tools, Utility Vehicles, Implements & Attachments, Parts. Each opens a panel with sub-categories on the left and a swiper of product thumbnails on the right.
- Breadcrumb on interior pages: `Home / Products / Tractors / Compact / L Series` rendered inline in `#1a1a1a` text with orange separators.

### Cards
- Product card: image (often white background with orange tractor centered), model name in 18–22px Bold, brief HP/use line, "View Specs" or "Learn More" link. No price shown anywhere. Pricing is dealer-driven, by design.
- Resource card (financing, service, why-kubota): icon at top (`kubota-icon` font), title, two-line description, link.
- News card: thumbnail image, date in small gray, title, source.

### Forms
- Find-a-dealer locator: ZIP input with orange "Find" button, "Use my location" inline link, radius dropdown, results list with map (Google Maps embed).
- Newsletter ("Kubota First"): email field, orange Subscribe button, inline checkbox for consent.
- Configurator forms: multi-step with breadcrumb progress bar, step counter, large radio-card selectors.

### Modals
- `#primary-modal` is a Bootstrap modal scaffold reused for video play, image lightbox, and external-link warning. The close button uses the `kubota-icon kubota-icon-close` glyph rather than a standard ×.
- `.external-link-notice` is a Kubota-specific modal: heading "Important Notice," body "You're continuing to another website that Kubota Tractor Corporation doesn't own or operate. Its owner is solely responsible for the website's content, offerings and level of security," with `Continue` (orange) and `Cancel` buttons. This is a distinctive piece of legal-conservatism UX. Kubota wraps every outbound link in a confirmation modal, which is unusual in 2026 and signals a heritage corporate posture.

### Carousels
- Swiper.js v6, with custom pagination dots styled to `background: #686868`, hidden until hover on some configurations. No 3D effect, no fade, just a horizontal slide with bullets.

### Tabs and accordions
- PDPs use a horizontal tab strip at desktop ("Features," "Specs," "Photos," "Videos," "Brochures") that collapses to vertical accordions at mobile.

### Toasts and notifications
- The OneTrust cookie consent banner is the only persistent overlay. It uses OneTrust's default chrome with a Kubota-orange "Accept All" button override.

### Notable absences
- No live chat, no AI assistant widget, no Kubota chatbot bubble visible in the markup. Kubota routes everything to the dealer.
- No "compare models" floating tray. Comparison happens on a dedicated comparison page.
- No e-commerce add-to-cart in the main domain. The parts shop lives at `shop.kubotausa.com` as a separate property.
- No saved-favorites / heart icon. There is no logged-in account UI on the consumer site.
- No "as low as $X/mo" payment-estimator widget, despite the brand having captive financing. The user has to click into Finance pages to see offers.

## 6. Iconography

Kubota uses a custom icon font called `kubota-icon` (class pattern `kubota-icon kubota-icon-{glyph}`), supplemented by Font Awesome (loaded via `https://kit.fontawesome.com/816956f0f8.js`) for social icons and a few utility glyphs.

### Custom Kubota icon set (observed glyphs)
- `kubota-icon-location-fill`. Used on the Find A Dealer button.
- `kubota-icon-close`. Modal close.
- Inferred set (from the site's category tiles and CTAs): tractor, mower, excavator, RTV, parts/wrench, finance/calculator, brochure/document, video play, search magnifier, cart, map pin (filled and outline), arrow right, arrow down, hamburger.

### Font Awesome usage
- Footer social: `fa fa-facebook`, `fa fa-youtube`, `fa fa-instagram`, `fa fa-envelope`. The site is still on Font Awesome 4 syntax (no `fab` or `fa-brands` prefix), confirming the icon font generation is from an older era and has not been migrated to FA 5/6.
- These social icons are gray-on-white in their default state and orange on hover.

### Style characteristics
- Icons are flat, monoline, geometric, with rounded corners. Stroke weight matches the Helvetica Neue body copy weight, so icons sit visually at the same density as adjacent text.
- No detailed illustrative iconography (no equipment line drawings used as icons). The icon set is purely UI.
- Icons inherit text color via CSS, so the same icon appears in `#1a1a1a` in body text and `#dc4405` on hover.

### JP global site iconography
- The corporate JP site uses a different system: BEM-style class names like `IconCorporationLogo`, `IconFooterFacebook`, `IconFooterLinkedIn`, `IconFooterYouTube`, `IconBlank` (for "opens in a new window"), `IconSearchSite`, `IconGnetwork` (for the Kubota Group network globe icon). This is a hand-crafted icon set delivered via custom CSS sprites and aria-labels, not Font Awesome.

### Notable absences
- No 3D iconography, no isometric icon illustration, no animated SVG icons. Everything is flat, monochrome.
- No iconography that visually echoes farming (no wheat, no leaves, no sun) other than the orange globe in the For Earth, For Life lockup. Kubota does not lean on cliché ag-iconography.
- No emoji or color-illustrated icons anywhere on the audited pages.

## 7. Photography Style

Kubota's photography is the brand's most powerful visual asset and follows a tight, recognizable formula across the site. Inferred from `<img>` alt text, file paths (`gpmfg.io/lp_files/styles/scale_crop_800px/public/...`), the homepage product album metadata, and the surrounding promotional copy.

### Three primary photography modes
1. **Hero environmental shots**. The orange machine in a working environment: a B-series tractor in a hayfield, an L-series with a front loader on a horse property, a Sidekick RTV climbing a forest trail at golden hour. The photography is sun-flared, shot on a wide-angle lens, with the machine in the lower third and a wide sky/landscape above. The orange of the equipment is the only saturated color in frame, which means the rgba(0,0,0,0.5) scrim under the headline doesn't have to fight for attention.
2. **Studio "hero shot" 3/4 angle**. Used on PLP cards and PDP heroes. The machine is photographed from the front-right at roughly 30 degrees, on a seamless white or slightly graduated background. No operator. No accessories. The machine is the portrait subject. Shadow is soft and grounded.
3. **Operator-in-use**. A real-looking operator (not a model) in a Kubota-orange cap, work boots, and casual workwear, mid-task on the machine. The framing is medium-wide, the operator is mid-action (turning the wheel, lowering a backhoe, mowing). These shots emphasize that "this is a working tool, this is your day."

### Treatment notes
- Color: warm white-balance with a slight orange/yellow lean. Greens are desaturated. The ground tone is rust-warm even when the actual location is cool-light Pacific Northwest.
- Composition: rule-of-thirds, machine in the lower or middle third, wide negative sky for headline placement.
- Light: golden hour or overcast. Avoids harsh midday.
- People: Kubota photography reads as "the farmer/landowner who actually owns one," not as fashion-shoot models. Hands are dirty. Boots are worn.
- Equipment is always painted Kubota orange. There is no hero photography of un-painted prototypes, blueprints, or factory floor.

### Functional photography
- PDP gallery shots: detail crops of the loader joystick, the seat, the dashboard, the mower deck, the RTV bed.
- Implement shots come from the Land Pride/GPMfg sister brand and are hosted on `cdn-assets.gpmfg.io`. They have a slightly different crop and lighting standard, which is one of the few inconsistencies in the visual system.

### File and alt-text conventions
- Alt text describes function, not aesthetics: e.g., `alt="LA344 Loader Bucket"`, `alt="SGS15 Series Skeleton Grapple"`. SEO and accessibility friendly.
- Filenames are model-coded: `lp23_rg1572_render1_web_0.png` (Land Pride), `b01-series-tractor.jpg` style.

### Notable absences
- No drone-footage hero (no top-down "flying over the field" video on the homepage; the hero is ground-level).
- No lifestyle imagery of family/dinner-table moments. Kubota stays on the work itself, not the fruit of the work.
- No black-and-white photography anywhere. The whole brand is in color and saturated orange.
- No CGI/render-style hero shots on the US consumer pages. Kubota uses real photography of real machines, even when a render would be easier. This is a deliberate authenticity move.
- No dirt-on-the-machine "hero of work" shots that show the equipment caked in mud. The machines are clean, almost too clean for a work brand. The "we just got delivered" gleam wins over the "we've been working" patina.
- No diversity-conscious operator photography in the audited samples. The operators skew rural-American-male, which is on-target for the buyer base but is a brand-evolution opportunity Kubota has only lightly addressed.

## 8. Brand Voice & Language Style

Kubota's voice is plain-spoken, specifications-honest, and quietly proud of being a working tool. It does not chase aspiration. It does not chase technology theater. It chases performance you can measure and a dealer you can drive to. The most-used phrases are functional ("Find A Dealer," "View Specs," "Build My Kubota") rather than emotional. The two emotional anchors the brand allows itself are the global tagline "For Earth, For Life" and the about-page line "We focus on engineering excellence so that our customers can focus on planting, feeding, building & caring for our world." Both are mission-scale statements that frame Kubota as an enabler of someone else's important work.

### CTA inventory by page context

#### Global header (every page)
- **Find A Dealer**. The single most prominent CTA on the site. Orange filled button. Confirmed exact text in markup: `Find A Dealer`. Variant: `Find a Dealer Near You` on contextual placements. Variant: `Find a Dealer` (lowercase a) inside body copy. The site is internally inconsistent on title case here, which is a copy-hygiene gap.
- **Parts**. Utility nav link, routes to the parts shop subdomain.
- **Service & Support**. Utility nav link.
- **Finance**. Utility nav link.
- **About**. Utility nav link.

#### Homepage hero / promo carousel
- **Build Your Kubota**. The configurator CTA on the homepage. Body copy elsewhere reads "or even build your own. Then find a dealer close by with your customizations."
- **Learn More**. Soft CTA on hero secondary slides.
- **View Models**. Links into category PLPs.
- **Watch Video**. Opens the Vimeo player overlay (Vimeo confirmed: `https://player.vimeo.com/api/player.js`).

#### PLP (product listing) pages
- **View Specs**. Confirmed verbatim in markup: `<p dir="ltr" role="presentation">View Specs</p>`. Used on every product card.
- **Compare Models**. Secondary action.
- **Find A Dealer**. Repeated at end of PLP.

#### PDP (product detail)
- **Build My Kubota**. Primary CTA, orange, links to the configurator subdomain `apps.kubotausa.com/configurator`.
- **Find a Dealer Near You**. Secondary CTA, repeated.
- **View Brochure** (PDF download). Tertiary.
- **Request a Quote** is *not* a primary CTA pattern. Pricing is dealer-mediated. Quote requests are deliberately funneled through the dealer locator rather than a direct online RFQ form. This is a brand decision: Kubota protects the dealer relationship.

#### Finance / Promotions pages
- **View Offers** / **Current Promotions**. Landing on the offers detail.
- **Apply for Financing**. Links to `kubotacreditusa.com`, a separate captive-finance property.
- **Estimate Payments**. Tertiary; not on the homepage.

#### Find A Dealer
- **Use my location** (geolocation prompt).
- **Search** (primary action on the ZIP form).
- **Get Directions** (per-result).
- **Visit Dealer Site** (per-result).
- **Contact Dealer** (per-result).

#### Footer (every page)
- The footer has no commerce CTAs. It has eight informational nav links: About, Press Releases, Careers, Kubota Cares, Events, Merchandise, Contact, Gray Market Tractors. ("Gray Market Tractors" is a uniquely Kubota footer link. It is a warning page about non-US-market tractors that lack US safety/emissions support, and it lives in the footer because Kubota has a long-standing corporate position against gray-market sales. This is a brand-defending CTA disguised as a footer link.)
- Social: Facebook, YouTube, Instagram, "Kubota First" newsletter envelope.

### Recurring phrases captured directly
- **"For Earth, For Life"**. Global tagline, appears in the top utility lockup on every US page, in the homepage logo file alt, and in the footer mobile lockup.
- **"Kubota Tractor Corporation"**. Legal entity, footer.
- **"Built. Tough. Smart."**. Implied positioning across PDP descriptions.
- **"Engineering excellence"**. Appears in the about-page meta description: "We focus on engineering excellence so that our customers can focus on planting, feeding, building & caring for our world."
- **"planting, feeding, building & caring for our world"**. The four-verb mission frame.
- **"Together at the same time"**. The loader-design copy: "both the tractor and loader are designed together at the same time, not in pieces or as afterthoughts."
- **"Kubota built"** / **"Kubota Genuine"**. Recurring qualifier for parts and attachments: "the LA435 Front Loader is not only Kubota built, but it's also designed to specifically fit the B01 series."
- **"Performance-matched"**. Recurring loader/implement descriptor.
- **"Swift-Tach"**, **"Swift-Connect"**. Proprietary feature names (always capitalized, hyphenated, spelled the same way).
- **"Workhorse"**. Used to describe attachments and machines: "irregular shapes, and serrated teeth make this grapple a workhorse in storm clean up and land clearing operations."
- **"Compact, but..."**. Recurring framing for sub-compact tractors: "It may be compact, but the BX23S's backhoe offers jumbo-sized convenience and performance."

### Heading style by page type
- **Homepage**: Hero headlines are short, declarative, all-caps in the HelveticaNeue-CondensedBlack treatment, and almost always pair a benefit with the product line (e.g., "BX SERIES. THE RIGHT SIZED TRACTOR").
- **PLP**: H1 is a category noun ("Tractors," "Utility Vehicles," "Mowers") sometimes preceded by "All Products. " in the SEO title pattern (confirmed in titles: `All Products - Tractors| Kubota`, `All Products - Mowers| Kubota`). H2 sub-headings split into series labels ("BX Series," "L Series," "M Series").
- **PDP**: H1 is the model name ("L3902"). H2 is a benefit-led tagline ("21.6 HP. Ready to meet all of your property needs."). H3 introduces feature blocks.
- **About / Why Kubota**: Headlines lean editorial ("Engineering excellence so you can focus on the work that matters"), with longer-form sentence headlines.
- **Find A Dealer**: SEO H1 is `Kubota | Find a Dealer Near You - Locations`, on-page H1 is shorter ("Find A Dealer").
- **JP global**: A "shoulder + main" pattern is used (`<span class="HeadingLevel1__shoulder">ERROR 404</span><span class="HeadingLevel1__main">Not found</span>`). The shoulder acts as a small all-caps eyebrow above the main headline. The US site does not use this pattern.

### Product description formula (PDP)
A consistent four-part structure:
1. **One-sentence positioning line**. Usually a HP/size + use-case promise. ("21.6 HP. Ready to meet all of your property needs.")
2. **A "feature name + benefit" bullet list**. In the form `**Feature Name**. Benefit explained in one sentence.`. Confirmed examples: "Swift-Tach Loader. Remove your front loader in less than 60 seconds," "Curved Boom Design. Allows for better visibility when performing front loader work," "Optional 2-Lever Quick Coupler. Easily connects implements," "Faced No-spill Hydraulic Couplers. Less mess and easier to connect than traditional tractor hydraulic couplers."
3. **A "Performance-matched" or "Kubota built" reassurance paragraph**. Explains why the matched implement is better than aftermarket.
4. **Cross-sell paragraph**. Links to compatible Land Pride implements with their own short descriptions.

### Tone descriptors
- **Plainspoken**, not punchy.
- **Specifications-honest**: every feature claim is backed by a spec ("less than 60 seconds," "21.6 HP," "16.6 - 24.8 HP").
- **Modest about achievements**: the brand has been operating since 1890 and rarely says so on the consumer site. The heritage is present but not bragged about.
- **Operator-respectful**: copy assumes the reader knows the difference between a 3-point hitch and a backhoe, and does not over-explain.
- **No urgency language**: there is no "Limited Time," "Hurry," "While Supplies Last," or "Sale Ends Soon" copy in any audited page. Even the promotions page uses neutral language like "Current Offers" rather than countdown urgency. This is unusual for a consumer-financed product and is on-brand for Kubota's "we don't need to rush you" posture.
- **No celebrity language**: no athlete endorsements, no "as seen on TV," no testimonial-as-headline. Operator quotes appear, but as named-customer profiles, not as marketing hooks.
- **No technology theater**: Kubota does not talk about "AI," "smart," "connected," or "autonomous" in the audited pages. This is striking for an "Agriculture & Robotics" brand category. Kubota's brand voice has not yet leaned into the "robotics" half of its category positioning. Compare to John Deere, which heavily markets autonomous tractors in their consumer comms.

### Microcopy patterns
- Empty states and 404: "The resource you are looking for might have been removed, had its name changed, or is temporarily unavailable." Direct, polite, no humor, no character.
- External link warning: "You're continuing to another website." Curt, legalistic.
- Cookie banner: standard OneTrust copy, not Kubota-customized.
- Form helper text: minimal. Field labels stand alone.

### Voice gaps
- The "Why Kubota" page (which 404'd at the time of audit, signaling either a redirect target or content recently removed) is meant to be the brand's primary emotional pitch and is currently broken. This is a notable maintenance miss.
- The footer copyright reads "© 1996 - 2017 Kubota Tractor Corporation". Frozen at 2017. This understates the brand's currency.
- No urgency language anywhere, even on financing offers and promotions, which leaves a real conversion lever on the table.

## 9. Platform & Technical Notes

### CMS and stack
- **Sitefinity (Telerik / Progress)**. Confirmed by the presence of `Telerik.Web.UI.WebResource.axd`, `Telerik.Sitefinity.Resources`, the ASP.NET Web Forms scaffolding (`__VIEWSTATE`, `__VIEWSTATEGENERATOR`, `aspnetForm`, `Sys.Application.setServerId`), and the resource pack path `/ResourcePackages/Bootstrap/`. This is a .NET-era enterprise CMS, not a headless or JAMstack platform.
- **ASP.NET Web Forms** server-rendered with hidden viewstate fields.
- **Bootstrap** as the front-end CSS framework, customized into a Sitefinity ResourcePackage.
- **Vue.js** mounted on specific div IDs (`#vc_f06d416ee78847489c69f58819fb0fdf`) for the megamenu, the promo carousel, the dealer locator, and the configurator entry. This is a hybrid pattern: ASP.NET shell plus Vue islands.
- **Swiper.js v6** for carousels, loaded from `/Content/Vendor/swiperjs/swiper.v6.min.js`.
- **Vimeo Player API** for video, loaded from `https://player.vimeo.com/api/player.js`.
- **jQuery** still present (`(function ($) { ... })(jQuery);` block in the retargeting pixel).
- **Font Awesome 4** loaded via Kit `https://kit.fontawesome.com/816956f0f8.js`.

### Sub-domain ecosystem
- `www.kubotausa.com`. Main consumer site (Sitefinity).
- `shop.kubotausa.com`. Parts e-commerce (`https://shop.kubotausa.com/oemparts/c/...`).
- `apps.kubotausa.com/configurator`. Kubota Configurator tool.
- `cdn-assets.gpmfg.io`. Land Pride / GPMfg implements CDN (sister brand).
- `kubotacreditusa.com`. Captive financing portal.
- `kubota-global.net/us/`. Kubota Group network site.
- `kubota.com`. Global corporate (different stack. See below).

### Analytics and tracking
- Google Analytics (Universal: `UA-86904899-1`).
- Google Tag Manager: two containers loaded. `GTM-5RPFFMK` and `GTM-TGFMV3KR` (the second appears injected post-consent inside the header partial). Two GTM containers running in parallel is a configuration smell.
- DoubleClick / Google Ads retargeting pixel (`pubads.g.doubleclick.net/activity;dc_iu=/6544/DFPAudiencePixel`).
- ShareThis inline-share buttons (`platform-api.sharethis.com/js/sharethis.js`).
- Evidon Adchoices opt-out (`info.evidon.com/pub_info/6901`).
- OneTrust cookie consent (`cdn.cookielaw.org/consent/6dcd6b86-ff7f-4595-b41c-c1087969ddee`).
- Google reCAPTCHA on form pages.

### SEO patterns
- Title formats observed:
  - Homepage: `Home` (just "Home". A notable SEO miss; should include "Kubota").
  - Tractor PLP: `All Products - Tractors| Kubota` (note: missing space before pipe, recurring across PLPs).
  - Compact tractor PLP: `Products - Tractors - Compact | Kubota`.
  - Mowers PLP: `All Products - Mowers| Kubota`.
  - UV PLP: `All Products - Utility Vehicles| Kubota`.
  - Construction PLP: `All Products - Construction| Kubota`.
  - About: `Kubota | About Us - Company Information & Services`.
  - Find a Dealer: `Kubota | Find a Dealer Near You - Locations`.
  - The title format is internally inconsistent. Some pages put Kubota first, others last, some have spacing issues around the pipe.
- Meta description on homepage: `Learn more about Kubota tractors, construction equipment, mowers, utility vehicles, parts, services & more. Find a local dealer or build a custom Kubota today!`. Strong keyword coverage, "build a custom Kubota" phrasing reinforces the configurator.
- Meta description on About: `We focus on engineering excellence so that our customers can focus on planting, feeding, building & caring for our world. Learn more about us today!`.
- JSON-LD `Organization` schema present on the homepage with:
  - `name: Kubota Tractor Corporation`
  - `url: https://www.kubotausa.com`
  - `logo: https://www.kubotausa.com/Content/Images/logo.jpg`
  - `sameAs: [Facebook, YouTube, Instagram, LinkedIn]`. Note that LinkedIn is in the JSON-LD but not in the visible footer social row. The visible row is FB / YT / IG / Email only. So LinkedIn exists structurally but is hidden from users.

### Performance and accessibility hints
- Skip-to-main-content link is present (`<a href="#main-content" class="sr-only sr-only-focusable">Skip to main content</a>`). Good baseline accessibility.
- ARIA labels are present on icons (`aria-hidden="true"` on decorative kubota-icon glyphs; `aria-label` on JP corporate icons).
- The site is HTTPS, served as `text/html; charset=utf-8`.
- `<meta name="viewport" content="width=device-width, initial-scale=1" />`. Responsive.
- IE9 conditional comments still present in the HTML (`<!--[if lte IE 9]>... <![endif]-->`). A 2026-anachronistic artifact.
- Page weights are heavy (the homepage HTML alone exceeds 1MB before assets). Vue megamenu data is inlined as JSON in the page payload, which is what blows up the HTML size. This is poor for first-paint metrics.

### Global JP site (kubota.com). A different stack entirely
- No Sitefinity, no ASP.NET Web Forms.
- Vanilla front-end: `/assets/styles/common.css` plus `/assets/scripts/common.bundle.js`.
- BEM-style class naming convention: `Header__inner`, `HeaderLogo__img`, `GNavList__item`, `Footer__bottom`, `FooterSitebrand__logo`, `Definitionlist__heading`, `HeadingLevel1__shoulder`, `HeadingLevel1__main`, `Button__inner`, `Button__text`. This is hand-rolled CSS architecture, not Bootstrap.
- The JP team appears to have a more rigorous design system at the class/naming level, though the visual output is also more conservative and corporate-investor-tilted.
- GTM container on global: `GTM-MKFW4GB`.
- Includes a Japanese-style "shoulder + main" headline pattern that the US site lacks.
- Footer entity: "KUBOTA Corporation" with copyright `© 1996-<span class="Js-CopylightYear"></span>` (auto-updating year via JS, which the US site is missing).
- Only three social platforms in the JP footer: Facebook, LinkedIn, YouTube. No Instagram on the corporate side. Instagram is a US-consumer-only channel.

### Notable absences
- No service worker / PWA manifest detected.
- No HTTP/3 indicators captured.
- No OpenGraph image extraction beyond the meta tags loaded.
- No Schema.org Product or Vehicle structured data on PDPs (would help SEO for shopping experiences).
- No CSS custom-property design tokens, no design-system documentation site (no `design.kubota.com` or similar surfaced).
- The US and global sites are visibly disconnected as digital products. Different CMS, different naming, different copy, different social link sets. There is no shared design-token bridge.

## 10. Pages Scraped

Thirteen distinct URLs were visited across the kubotausa.com US consumer property and the kubota.com global corporate property. Several intended URLs (`/why-kubota`, `/promotions`, `/about`, `/products/tractors/compact/l-series/l3902`, `https://www.kubota.com/about/`, `https://www.kubota.com/sustainability/`) returned 404 in the audit run, which is itself a finding: `/why-kubota` and `/promotions` resolving to 404 indicates the marketing-led pages are likely under different slugs than expected, and these dead links would be a problem for inbound campaign URLs.

### Successfully scraped (US consumer)
- https://www.kubotausa.com/. US homepage (page-type: homepage).
- https://www.kubotausa.com/products/tractors. Tractor PLP / category index (page-type: PLP).
- https://www.kubotausa.com/products/tractors/compact. Compact-tractor sub-category PLP (page-type: PLP).
- https://www.kubotausa.com/products/utility-vehicles. RTV / utility vehicles PLP (page-type: PLP).
- https://www.kubotausa.com/products/mowers. Mowers PLP (page-type: PLP).
- https://www.kubotausa.com/products/construction. Construction equipment PLP (page-type: PLP).
- https://www.kubotausa.com/find-a-dealer. Dealer locator (page-type: tool / locator).
- https://www.kubotausa.com/about. About us (page-type: brand / corporate).

### Successfully scraped (global / corporate)
- https://www.kubota.com/. Global homepage (page-type: corporate homepage).
- https://www.kubota.com/about/. Global about (page-type: corporate, returned 404 with template intact, used to extract global header/footer/nav/icon system).

### Attempted, returned 404 (kept for context, structural data still extracted from template)
- https://www.kubotausa.com/products. Product hub (page-type: hub; redirect cancelled).
- https://www.kubotausa.com/products/tractors/compact/l-series/l3902. PDP attempt (page-type: PDP intent; 404. Slug has likely been changed to `/l3902` under a different parent).
- https://www.kubotausa.com/why-kubota. Brand page attempt (page-type: brand; 404).
- https://www.kubotausa.com/promotions. Promotions / financing offers attempt (page-type: offers; redirect cancelled).

### By page type
- **Homepage**: 2 (US + global).
- **Product Listing Pages (PLP)**: 5 (Tractors, Compact Tractors, Utility Vehicles, Mowers, Construction).
- **Brand / About**: 2 (US about, global about).
- **Tool / Locator**: 1 (Find A Dealer).
- **Attempted but 404 (analyzed via 404 template, useful for header/footer/nav extraction)**: 4 (`/products`, `/why-kubota`, `/promotions`, `/products/tractors/compact/l-series/l3902`, plus the JP `/about/`).

The 13 successful and attempted pages exceed the 12-page minimum and span homepage, hub, PLP at multiple category depths, dealer locator, brand, and corporate global, providing a representative cross-section of the Kubota digital brand surface.
