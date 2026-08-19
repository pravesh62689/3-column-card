## 2024-05-15 - CSS @import blocks parallel rendering
**Learning:** Found duplicate Google Font `@import` statements inside CSS files. This is an anti-pattern as the browser must sequentially download the CSS, parse it, and then discover and download the font stylesheet, blocking render.
**Action:** Always move third-party font requests to the HTML `<head>` using `<link rel="stylesheet">` and add `<link rel="preconnect">` for the origins to parallelize downloads.
