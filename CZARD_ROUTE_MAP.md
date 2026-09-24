# CZARD Route Map

Inspection basis: recursive capture under `www.czard.com`, plus root-level third-party mirrors. Routes below are only represented by downloaded files. HTTrack changed URL semantics into `.html` files and some captured endpoints.

## Primary Routes

| URL/path | Source | Purpose and connections |
|---|---|---|
| `/` | `www.czard.com/index.html` | Custom immersive home experience; links to all watches, product chapters, information pages, cart, film overlay, and social destinations. |
| `/collections` | `www.czard.com/collections.html` | Collection landing/index; links to all collections and products. |
| `/collections/all` | `www.czard.com/collections/all.html` | All products collection. |
| `/collections/chronograph-watches` | `www.czard.com/collections/chronograph-watches.html` | Chronograph collection/product grid. |
| `/collections/mechaquartz-watches` | `www.czard.com/collections/mechaquartz-watches.html` | Mechaquartz collection/product grid. |
| `/collections/swiss-automatic-watches` | `www.czard.com/collections/swiss-automatic-watches.html` | Swiss automatic collection/product grid. |
| `/products/veni` | `www.czard.com/products/veni.html` | Compass product detail page; cross-links Vidi/Vici and collection products. |
| `/products/vidi` | `www.czard.com/products/vidi.html` | Compass product detail page; representative complete product template. |
| `/products/vici` | `www.czard.com/products/vici.html` | Compass product detail page. |
| `/products/ecru` | `www.czard.com/products/ecru.html` | Geneva product detail page. |
| `/products/lac-leman` | `www.czard.com/products/lac-leman.html` | Geneva product detail page. |
| `/products/jura-gruen` | `www.czard.com/products/jura-gruen.html` | Geneva product detail page. |
| `/cart` | `www.czard.com/cart.html` | Shopify cart view; related captured endpoints live under `cart/`. |
| `/blogs/news` | `www.czard.com/blogs/news.html` | Blog index. `news2679.html`, `news4658.html`, and `news9ba9.html` are additional paginated captures. |
| `/blogs/news/{article}` | `www.czard.com/blogs/news/*.html` | 29 captured watchmaking/brand articles; footer/header connect them to information, product, and social routes. |

## Information and Policy Routes

`/pages/about-us`, `/pages/contact`, `/pages/faqs`, `/pages/czard-chapter-system`, `/pages/lifetime-warranty`, `/pages/service-warranty-policy`, `/pages/shipping-policy`, `/pages/refund-policy`, `/pages/privacy-policy`, and `/pages/terms-of-service` are represented by matching files under `www.czard.com/pages/`.

There are also duplicate Shopify policy captures under `www.czard.com/policies/`.

## Utility, Checkout, and Capture Routes

`default.html`, `0.html`, `billingAddress.html`, `deliveryAddress.html`, `preferences/index.html`, `users/index.html`, `catalog/index.html`, `api/index.html`, `api/collect.html`, `cdn.html`, `cdn/wpm/index.html`, `apps/webengage/index.html`, and the checkout capture under `checkouts/cn/.../en-ina7d2.html` are technical, account, checkout, tracking, or error captures rather than authored customer-facing routes. `products/index.html` and `collections/index.html` are index/redirect stubs.

## Ecommerce Endpoints

Captured cart resources include `cart/add.js`, `cart/change.js`, `cart/update.json`, and `cart/clear.js`. Product forms submit to the Shopify cart add route and carry variant, quantity, product, and section values. The checkout capture includes Shopify checkout internals and payment assets. No purchase was performed.

## Route Relationships

Home -> Collections -> Product -> cart/add -> Cart -> Shopify checkout. Header/footer links also reach About, Contact, FAQs, Chapter System, blog, policies, and social networks. Product pages connect laterally through Compass color selectors, Geneva collection cards, related-product cards, and product-specific assets.

Exact browser-visible active states, menu transition timing, and any route only created dynamically by a server/API are NOT DETERMINABLE FROM DOWNLOADED FILES.
