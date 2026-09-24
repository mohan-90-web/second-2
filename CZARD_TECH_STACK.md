# CZARD Technology Stack

## CONFIRMED

- Shopify storefront/theme structure: Shopify routes, product JSON, cart endpoints, theme asset naming, Shopify checkout capture, and Shopify CDN assets.
- Custom Minimog-style theme runtime: `theme-global4765.js`, `main01f4.css`, vendor/theme assets, custom elements, cart drawer, deferred media, responsive matchMedia configuration.
- Lenis `1.1.18` smooth-scroll bundle and Lenis setup.
- GSAP `3.12.5` references; ScrollTrigger references in homepage/custom interactions.
- Three.js `0.172.0` and CSS3DRenderer dependency in the homepage experience.
- WebGL canvas scene, CSS3D product viewers, custom cursor, and scroll-controlled homepage state engine.
- JavaScript modules/custom elements, IntersectionObserver, requestAnimationFrame, media APIs, CSS keyframes/transforms, and sticky/fixed layers.
- Shopify cart and checkout flow, product variant forms, cart drawer, Shop Pay/payment asset bundle.
- GoKwik merchant integration files under `pdp.gokwik.co/merchant-integration/` and related checkout interception references.
- Sirv viewer integration (`scripts.sirv.com` and Sirv spin references).
- Vimeo player API capture under `player.vimeo.com/api/player.js`.
- WebEngage resources under `shp.webengage.com`, `c.webengage.com`, `apps/webengage`, and captured proxy files.
- External font providers and Shopify CDN preconnects.

## LIKELY

- The authored site is a Shopify Online Store theme with custom Liquid-generated HTML, because all downloaded HTML is rendered output rather than source Liquid and theme asset conventions are consistent.
- The main custom visual layer likely uses a combination of Three.js scene objects and CSS3DRenderer rather than a pure video background, because both renderer/canvas code and Sirv 360 resources are referenced.
- Product storytelling modules are custom theme sections composed with shared `luxe-*` scripts and CSS.
- Collection/product data likely came from Shopify Storefront/Ajax APIs; the download includes endpoint-shaped files and embedded JSON, but server-side API behavior cannot be proven offline.

## UNKNOWN

- Original Liquid source, build pipeline, repository, deployment configuration, and theme version are not included.
- Whether all captured CDN resources were loaded during the original crawl or merely discovered by dependencies is not determinable.
- Exact production browser performance, GPU fallback behavior, and all mobile substitutions cannot be proven without running the live or locally served capture.
- Exact video codecs, dimensions, durations, and image intrinsic dimensions for every binary asset are not established by the HTML alone.
- Checkout availability, payment success, inventory, customer account state, and GoKwik production behavior cannot be tested from this inspection and no purchase was attempted.
- Some routes and resources may be crawler-generated representations rather than directly navigable public URLs.

## Responsive architecture

Confirmed thresholds are distributed across CSS/JS: homepage `760px`; common theme mobile max `767px`, tablet max `1023px`; product sections at `1024px`, `560px`, `750px`, `990px`, `1200px`, `1279px`, and `1280px`; common grid changes at `768px` and `1280px`. Mobile changes include reduced homepage scroll height, responsive grids, navigation/menu changes, smaller product/story layouts, and media sizing changes. Exact rendered positions and per-component mobile animation changes are NOT DETERMINABLE without browser measurement.

## HTTrack and offline notes

HTTrack markers are present in HTML comments and the capture includes `hts-log.txt`, `hts-cache/`, `cookies.txt`, and crawler profile/cache files. URL flattening generated `.html` resources, duplicate domain directories, endpoint captures, and odd names such as the SVG path rendered as `M17.1 ... .html`. Repeated cart drawer and WebEngage files occur under multiple route directories. External/third-party mirrors include Apple Pay, Shopify, Vimeo, Sirv, WebEngage, GoKwik, WiseCart, Judge.me, and CloudFront resources. Dynamic requests, external fonts, Sirv spins, analytics, checkout/payment services, and server APIs may not function offline.
