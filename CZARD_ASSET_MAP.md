# CZARD Asset Map

## Inventory totals

Recursive workspace counts: 497 `.jpg`, 1 `.jpeg`, 101 `.png`, 77 `.svg`, 2 `.gif`, 9 `.mp4`, 1 `.mp3`, 24 `.woff2`, 48 `.css`, 306 `.js`, 88 `.html`, and 4 `.json` files. Inspectable web/media resources total approximately 475,888,213 bytes. This includes first-party captures, Shopify checkout bundles, external-domain mirrors, and crawler artifacts.

## Important first-party theme assets

### LOGO / UI

- `www.czard.com/cdn/shop/t/9/assets/logo14d6.png`
- `logo-white6abf.png`
- `logo_gradient_headerbd36.png`
- `loader-dial-dark73c4.svg`
- `loader-dial-base75cc.svg`
- `Star3e96.svg`, `metric7313.svg`
- Sitewide SVG/icon assets and Shopify payment SVGs under checkout assets.

Exact dimensions for the majority of these local images are NOT DETERMINABLE from file names alone; HTML metadata gives homepage OG image `1720 x 1008` and Vidi OG image `1080 x 1350`.

### PRODUCT / PRODUCT MACRO

Product-specific names identify the page and role: `veni-hero`, `veni-view-front`, `veni-view-dial`, `veni-view-45`, `veni-walk-*`; corresponding `vidi-*` and `vici-*`; plus `*-box-care`, `veni-box-inbox`, and the Geneva `swiss-*-hero`, `swiss-*-story`, `swiss-*-slider-*` families. These serve hero, gallery, detail walkthrough, packaging/care, and collection-story sections.

### BACKGROUND / MOUNTAIN OR ENVIRONMENT

- `swiss_heritage_BG.webp45f8.jpg`
- Geneva/Swiss collection hero and slider families
- Homepage scene background/texture resources embedded by the homepage custom section and external Sirv viewers.

No asset is categorized as a literal mountain image unless its page content establishes that use; exact semantic classification beyond filenames is NOT DETERMINABLE.

### VIDEO

Local theme media:

- `czard-ambientb25a.mp3` (ambient audio)
- `veni-dial8e44.mp4`, `veni-golddamer11b1.mp4`
- `vidi-dial41e2.mp4`, `vidi-golddamer3f59.mp4`
- `vici-diala6b1.mp4`, `vici-golddamerc332.mp4`
- Three Shopify CDN product/film MP4s under `www.czard.com/cdn/shop/videos/c/vp/` with hashed names.

Video dimensions, duration, and codecs are NOT DETERMINABLE from the HTML capture alone. Product markup confirms autoplay/muted/loop behavior for most inline videos; film markup supplies poster/deferred loading and controls where present.

### FONTS

- `Fitzgerald-Regular3e90.woff2`, `Fitzgerald-Italic...`, `Fitzgerald-Bold018b.woff2`, and bold italic variant: brand/display family.
- Open Sans WOFF2 families: Latin, Latin-ext, Cyrillic, Cyrillic-ext, Greek, Greek-ext, Hebrew, Vietnamese, math, and symbols; regular and italic variants.
- External page references include Cormorant Garamond, Jost, and product-page Josefin Sans. Offline availability is not guaranteed for those external references.

### OTHER / TRACKING / SERVICE

WebEngage images/scripts, Judge.me placeholder media, Sirv viewer references, GoKwik integration, Shopify payment icons, Vimeo player API, Apple Pay resources, and WebEngage tracking captures are present. `backblue.gif` and `fade.gif` are root-level legacy/crawler resources.

## Asset relationships

HTML product templates reference the named hero/gallery/video assets; custom CSS controls their aspect ratios/positioning; `luxe-*`, `swiss-*`, `slideshow*`, `video*`, and theme JS initialize reveal, walkthrough, slideshow, and purchase behavior. Homepage custom JS references Sirv spins, scene images, product destinations, and the ambient MP3. Some Sirv/CDN resources are external or mirrored incompletely, so offline rendering may fail.

## File sizes

The complete byte-size inventory is preserved by the original files. Representative custom assets range from sub-kilobyte CSS/SVG helpers to ~32 KB navigation/access JS and ~23 KB custom showcase CSS. The ambient MP3 is approximately 1.46 MB. Individual image/video dimensions and compressed sizes for all 700+ visual files are NOT DETERMINABLE here without decoding each binary resource.
