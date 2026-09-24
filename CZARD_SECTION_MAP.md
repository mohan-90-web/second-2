# CZARD Section Map

## Homepage: `www.czard.com/index.html`

The page is a custom scene rather than a normal stack of independent Shopify sections. The visible sequence is:

1. Full-screen navigation and loading/preloader layer.
2. Immersive Three.js WebGL scene with CSS3D layers and live Sirv 360-degree viewers.
3. Intro: CZARD logo, "Forget you are in ..." positioning copy, Swiss/Geneva copy, and `Enter Experience` control.
4. Six product chapters: I Veni, II Vidi, III Vici, IV Ecru, V Lac Leman, VI Jura Gruen.
5. The Film chapter/fullscreen film overlay path.
6. Final image/card scene.
7. Footer and linked sitewide content.

`#scroller` is the scene's scroll driver. The homepage declares `1000vh`; a media rule changes it to `500vh` below `760px`. Exact per-section viewport heights inside the scene are NOT DETERMINABLE FROM DOWNLOADED FILES because the visual sections are state transitions within one canvas/CSS3D composition.

Backgrounds are predominantly the custom dark scene, product imagery, external Sirv spins, and video/image cards. Typography uses the custom CZARD styles plus Fitzgerald/Open Sans and page-level external font references. Navigation and sound controls remain over the scene; product chapter links resolve to the six product routes.

## Product page sequence

Confirmed from `products/vidi.html`; the same named custom template is used by Veni, Vici, Ecru, Lac Leman, and Jura Gruen, with product-specific data/assets:

1. Loading/preloader and site header.
2. Product hero: hero image, edition/title, description, specifications, color links.
3. Warranty and numbered-watch fee variant controls.
4. Price and add-to-cart form.
5. Close-up image strip, eight images in the representative Vidi capture.
6. Autoplaying dial video.
7. Story: “What Vidi Meant”.
8. “The Film” heading and deferred film video with poster/controls.
9. “The Team” heading and three-slide watchmaker slideshow, 2-second autoplay interval.
10. “In the Press” heading and moving press-logo strip.
11. Genève collection cards: Écru, Lac Leman, Jura Gruen.
12. Four-step details walkthrough: Dial, Case, Strap, Crown.
13. Gold watch video.
14. Heritage note about Tasti Tondi pushers.
15. Movement section: Japanese VK64, chronograph, TMI VK64, 32,768 Hz.
16. Detailed product specification section.
17. Office/location carousel: Dubai, Geneva, Helsinki, Surat.
18. Two opposing image marquees.
19. Compass trilogy cards: Veni, Vidi, Vici.
20. Box contents, care, and warranty section.
21. Final autoplaying video.
22. Newsletter join section.
23. Footer.

The other product pages must be treated as data variants of this structure; presence of every item on every page is not assumed. Product-specific differences are encoded in each HTML file and referenced media names.

## Collection pages

Collection pages have a header/navigation, collection title/intro, product grid/cards, filtering or sorting controls where present in the capture, cart drawer wiring, newsletter/footer, and links into the six product pages. Exact card count and rendered viewport height vary by route and are not treated as universal.

## Shared interactions

Header links, cart icon/cart drawer, account/search/theme components, page transition layer, newsletter form, product variant selection, quantity controls, related-product links, policy links, and social links recur across templates. Generic theme assets handle common behavior; CZARD custom assets handle homepage/about/contact/FAQ/chapter and product storytelling behavior.
