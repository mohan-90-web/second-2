# CZARD Inspection Report

Inspection-only audit of the recursively downloaded workspace at `c:\My Web Sites\HWC`. No original HTTrack file was modified, deleted, renamed, moved, overwritten, or replaced. The six companion reports provide route, section, animation, asset, and technology detail.

## Executive Summary

The capture is a Shopify-based CZARD watch storefront with a highly custom home experience and a reusable editorial product template. The homepage is an immersive scroll-controlled scene using Three.js/WebGL, CSS3D product viewers, GSAP/ScrollTrigger, Lenis, external Sirv spins, video, and ambient audio. Product pages are long-form commerce stories: product purchase controls lead into close-ups, film, story, team, press, collection links, technical detail, heritage, packaging/warranty, newsletter, and footer.

The recursive download contains both authored storefront pages and large amounts of Shopify checkout, payment, analytics, tracking, external CDN, and crawler material. Offline fidelity is therefore partial: core HTML/CSS/media is present, while external/dynamic resources and API behavior may fail.

## Complete Project Structure

Top-level groups include the root capture files and HTTrack metadata; `www.czard.com` first-party pages/assets; `cdn.shopify.com`, `applepay.cdn-apple.com`, `player.vimeo.com`, `scripts.sirv.com`, `shp.webengage.com`, `portal.czard.com`, `pdp.gokwik.co`, `wisecart.convertwise.com`, and related external-domain mirrors; Shopify `cdn/shop/t/9/assets` theme files; product/collection/blog/policy pages; cart and checkout endpoints; and large Shopify checkout internals.

Recursive counts: 88 HTML, 48 CSS, 306 JS, 4 JSON, 497 JPG, 1 JPEG, 101 PNG, 77 SVG, 2 GIF, 9 MP4, 1 MP3, and 24 WOFF2. Inspectable resources occupy approximately 475.9 MB. No TypeScript source was found in the inventory. Source maps are referenced by bundles, but a complete usable original source tree is not present.

## Route Architecture

See `CZARD_ROUTE_MAP.md`. Confirmed customer-facing architecture includes home, collections, six products, information/policies, blog index/pagination, 29 blog articles, cart, and checkout capture. Technical endpoints/accounts/error pages are documented separately and are not promoted to authored navigation routes.

## Homepage Architecture

Source: `www.czard.com/index.html`, custom homepage section around the captured hero-house-of-CZARD markup and related `czard-*` assets. Exact visual order is navigation/preloader, immersive scene, intro, six numbered product chapters, film, final image/card scene, and footer. The scene scroll driver is `#scroller`; it is `1000vh` on larger screens and `500vh` below `760px`. Product chapters map to Veni, Vidi, Vici, Ecru, Lac Leman, and Jura Gruen. The homepage also uses a custom cursor, sound toggle, fullscreen film path, WebGL canvas, CSS3D layers, and external Sirv spins.

Approximate viewport height: only the scroll-driver values above are confirmed. Individual chapter heights, exact fold composition, and transition positions are NOT DETERMINABLE because the page is a single scene whose internal state is animated by scroll.

## Product Page Architecture

Source: `www.czard.com/products/*.html`; representative detail is Vidi. Confirmed sequence is documented in `CZARD_SECTION_MAP.md`. All six product routes use the same broad architecture with product-specific assets/content. Vidi confirms price `Rs. 14,999.00`, INR, product ID `9063535313050`, default variant `48886644506778`, one-year/lifetime warranty choices, and numbered-watch fee choices. Product forms connect to Shopify cart add behavior; no purchase was made.

## Navigation

The sitewide header exposes Home, All Watches, About CZARD, Contact Us, FAQs, and Cart. Product pages retain equivalent relative navigation. Product cross-navigation includes Compass color links, Geneva cards, trilogy cards, blog/article links, policies, and external Facebook, Instagram, LinkedIn, YouTube, and X destinations. The homepage `Enter Experience` and some `Discover`/box `BUY NOW` controls use `#` in the capture and are therefore placeholders or JS-driven controls. Account/search/menu behavior is supplied by custom navigation/theme code; exact open-state animation values are NOT DETERMINABLE globally.

## Scroll System

Lenis smooth scroll is confirmed with duration `1.2`, vertical orientation, smooth wheel, wheel multiplier `1`, touch multiplier `1.5`. GSAP ticker integration is present with requestAnimationFrame fallback, and ScrollTrigger refresh is connected to Lenis. The homepage uses scroll progress to drive the Three.js/CSS3D scene. Product pages add a `LuxeScroll` loop tracking position, delta, speed, viewport/document sizes, and normalized progress; the details walkthrough uses sticky positioning. Generic IntersectionObserver reveals use a `-50px` bottom root margin; custom product reveals use threshold `0.18` and bottom root margin `-8%`.

## Animation System

See `CZARD_ANIMATION_MAP.md`. Confirmed systems include scene rotation/transitions, CSS3D viewer motion, reveal observers, sticky step activation, 2-second team slideshow, press/image marquees, media autoplay/looping, dialog scale/backdrop transitions, and reduced-motion handling. Exact per-object scene values, all transition timings, and browser-rendered trigger locations are explicitly marked unknown where bundles do not expose them clearly.

## Image System

The theme uses hero/product/gallery/macro images, collection story sliders, packaging/care images, logos, icons, SVG loaders, payment icons, and external Sirv spins. Naming is systematic by product and section (`*-hero`, `*-view-*`, `*-walk-*`, `*-box-*`, `swiss-*-slider-*`). See `CZARD_ASSET_MAP.md` for categories and relationships.

## Video System

Six named product videos, three hashed Shopify CDN videos, and the ambient MP3 are captured in first-party theme assets. Product dial/gold/final videos are mostly muted/autoplay/loop inline media. Film uses deferred media/poster and user-start behavior in the theme runtime. Exact dimensions/durations/codecs are NOT DETERMINABLE from the HTML capture.

## Audio System

One local ambient file, `czard-ambientb25a.mp3`, is wired through `czard-sound04a5.js` and `czard-sound2fbd.css`. The homepage exposes a sound toggle. Autoplay persistence, exact volume, browser gesture fallback, and cookie/local-storage persistence are NOT DETERMINABLE without tracing/running the full runtime; browser autoplay policy necessarily applies.

## Typography

Fitzgerald is the custom display/brand family. Open Sans is bundled in extensive unicode subsets and styles. The HTML preloads Fitzgerald regular/bold and Open Sans Latin regular. External references include Cormorant Garamond, Jost, and Josefin Sans. Theme fallback families and exact component sizes are distributed across minified CSS; see the asset/theme files and companion reports. Exact rendered font fallback under offline conditions is NOT DETERMINABLE.

## CSS Architecture

CSS combines generic theme utilities and responsive grid primitives with custom CZARD navigation/access/sound/preloader/home/chapter/collection/about/contact/FAQ assets and product `luxe-*`, `swiss-*`, slideshow, video, and scrolling-promotion modules. Confirmed grid breakpoints include 768px, 1024px, and 1280px; common mobile/tablet thresholds are 767px/1023px. Fixed/sticky layers, high z-index overlays, transforms, opacity, clip/mask-related effects, keyframes, and reduced-motion queries are present. Full color/token extraction is distributed through minified bundles; a canonical single design-token file is not present.

## Responsive Architecture

Desktop and tablet/mobile rules are distributed rather than centralized. Confirmed breakpoints: homepage 760px; theme 767px/1023px; product/layout rules 560px, 750px, 768px, 990px, 1024px, 1200px, 1279px, and 1280px. Mobile reduces homepage scroll-driver height, changes grids/navigation/media sizing, and applies reduced-motion/accessibility branches where configured. Exact mobile product section order is generally preserved, but exact rendered dimensions are NOT DETERMINABLE offline.

## Ecommerce Architecture

Home -> collection -> product -> variant/warranty/number selection -> add to cart -> cart/cart drawer -> Shopify checkout. Captured cart endpoints include add/change/update/clear. Product pages carry variant and product IDs, quantity, price, and section data. GoKwik is present as a checkout/merchant integration. Shopify payment assets include cards, wallets, PayPal, Shop Pay, Apple Pay, Google Pay, Klarna, and other provider icons. This report does not validate payment execution.

## Third-Party Services

Shopify CDN/checkout, GoKwik, Sirv, Vimeo, WebEngage, Judge.me, WiseCart/ConvertWise, Apple Pay, CloudFront resources, external Google Fonts, social networks, and analytics/tracking endpoints are captured. Their presence does not guarantee offline execution.

## HTTrack Artifacts

HTTrack comments appear in HTML. `hts-log.txt`, `hts-cache/`, `cookies.txt`, and `winprofile.ini` are crawler artifacts. Flattened `.html` endpoint files, duplicated per-route cart drawer/WebEngage resources, hashed CDN trees, `default.html`, `0.html`, and the path-shaped `M17.1 ... .html` capture are artifacts or technical captures. Do not treat every file under external-domain folders as authored CZARD source.

## Confirmed Findings

Shopify storefront/checkout architecture; six products; four collection routes; blog and policy families; custom Three.js/WebGL/CSS3D homepage; Lenis 1.1.18; GSAP/ScrollTrigger references; IntersectionObserver and requestAnimationFrame; custom product storytelling; local ambient MP3; named product videos; Fitzgerald/Open Sans fonts; cart endpoints and GoKwik integration.

## Inferences

The original site was likely authored as a Shopify theme with custom Liquid sections and compiled/minified assets. The homepage likely depends on GPU/WebGL and remote Sirv services for its richest experience. `luxe-*` assets likely form a reusable product-story component system. These are informed interpretations, not source-level facts.

## Unknowns

Original Liquid/source repository, build pipeline, precise browser rendering, full media metadata, exact visual section viewport heights, every animation value, production API responses, inventory, checkout/payment success, account state, and external-service availability cannot be established from the downloaded files alone.
