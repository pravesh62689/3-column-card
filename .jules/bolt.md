## 2023-10-24 - CSS Import Blocking
**Learning:** Using `@import` in CSS files to load Google Fonts creates a render-blocking request chain. The browser has to download the CSS, parse it, and then go discover and fetch the fonts, significantly delaying First Contentful Paint.
**Action:** Always prefer `<link rel="preconnect">` and `<link rel="stylesheet">` tags directly in the `<head>` of the HTML to parallelize font fetching.
