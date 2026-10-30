## 2023-10-30 - Replace CSS @import with HTML link tags for Web Fonts
**Learning:** In static HTML/CSS sites, developers frequently use `@import` inside CSS files to load Google Fonts, unaware that this delays font downloading since the browser must first download and parse the CSS to discover the font request, causing a waterfall effect.
**Action:** Next time I encounter web font loading, I will immediately check if `@import` is used in CSS and swap it for `<link>` tags with `preconnect` in the HTML `<head>` for a quick, measurable render-blocking improvement.
