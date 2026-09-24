# CZARD Animation and Scroll Map

Values are reported only where present in captured source. Where a browser measurement or missing source is required, the value is explicitly marked unknown.

| Section/system | Trigger | Element | Property / start -> end | Duration/easing | Scroll/pin behavior |
|---|---|---|---|---|---|
| Sitewide smooth scroll | wheel/touch scroll | document through Lenis | eased scroll position | Lenis `duration: 1.2`, vertical, `smoothWheel: true`, `wheelMultiplier: 1`, `touchMultiplier: 1.5`; easing function exact runtime result is NOT DETERMINABLE | Lenis emits scroll events; GSAP ticker drives it when available, otherwise `requestAnimationFrame`; ScrollTrigger refresh is connected. |
| Generic theme reveals | IntersectionObserver entry | theme reveal elements | CSS classes change visibility/transform/opacity | Observer bottom root margin `-50px`; CSS duration/easing varies by class and is NOT DETERMINABLE universally | No pin confirmed. |
| Product custom reveals | IntersectionObserver entry | product story/section elements | reveal classes, commonly opacity/transform | threshold `0.18`, root margin `0px 0px -8% 0px`; per-class timing varies | Normal document scroll. |
| Homepage scene | scroll progress | Three.js camera/objects, CSS3D product layers, overlays | rotation, position, visibility, opacity, scene state; exact start/end per object varies | GSAP/ScrollTrigger present; per-tween duration/ease values are NOT DETERMINABLE for every scene transition from the mirrored/minified bundle. | `#scroller` is `1000vh`, or `500vh` below `760px`; scene is scroll-controlled rather than a pinned DOM section. |
| 360-degree products | scene scroll/state and viewer interaction | Sirv CSS3D viewers | viewer rotation/position | NOT DETERMINABLE | CSS3D layers live over WebGL; external Sirv `.spin` resources may not work offline. |
| Product details walkthrough | scroll position | sticky details panel and four step states | active step, image/text transforms and visibility | Custom `LuxeScroll` loop tracks scroll, delta, speed, viewport/document height and normalized progress; exact timing NOT DETERMINABLE | Sticky positioning confirmed; exact top offset NOT DETERMINABLE globally. |
| Team slideshow | timer/autoplay | slideshow slides | active slide/translate/opacity | interval `2000ms`; transition duration/easing NOT DETERMINABLE from capture | Normal scroll; slides may autoplay while visible. |
| Press/logo strip | CSS animation | logo marquee | translate transform | keyframe timing NOT DETERMINABLE universally | Continuous marquee; no pin confirmed. |
| Image marquees | CSS animation | opposing image rows | translate transform | keyframe timing NOT DETERMINABLE universally | Continuous opposing movement; no pin confirmed. |
| Product videos | media autoplay | dial/gold/final videos | playback from start; loop and muted attributes are present on product media | Media timing equals file duration; exact transition NOT DETERMINABLE | Inline video; most are autoplaying, muted, looping. |
| Film video | poster click/deferred-media load | film video | poster/deferred element -> loaded video; autoplay added on load for native video | JS calls `play()`; duration/easing NOT APPLICABLE | User-started/deferred; film has controls in representative product capture. |
| Dialog/account transitions | open/close | dialog and backdrop | scale `0.8 -> 1`, opacity `0 -> 1` on open; reverse on close | `0.6s` cubic-bezier `(0.7, 0, 0.2, 1)`; backdrop `0.8s` same cubic-bezier | Desktop media rule starts at `751px`; backdrop is animated. |
| Reduced motion | media query | animated components | animations disabled/simplified | Controlled by `prefers-reduced-motion`; exact component-by-component fallback varies | No assumption about browser setting. |

## Libraries searched

Confirmed: Lenis, GSAP/ScrollTrigger references, Three.js/CSS3DRenderer references, WebGL, canvas, requestAnimationFrame, IntersectionObserver, CSS transforms/opacity/keyframes, sticky/fixed positioning. No Locomotive Scroll or Framer Motion references were found in the first-party capture. A literal `three.js` filename match is not reliable because the homepage loads the library by CDN URL; Three.js is confirmed by the homepage dependency and renderer usage.

## Limits

The downloaded project contains minified bundles, repeated theme captures, and absent source maps for some custom bundles. Exact per-element transform values, viewport-relative trigger positions, and all easing/duration pairs cannot be reconstructed without running the site in a browser; these remain NOT DETERMINABLE rather than inferred.
