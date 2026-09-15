## 2024-05-18 - CSS @import performance bottleneck
**Learning:** Found that multiple CSS files (style.css, mediastyle.css) contained identical `@import` statements for Google Fonts, causing redundant blocking network requests and chaining font loading unnecessarily.
**Action:** Always verify if fonts are being loaded via `@import` in CSS files, especially in multiple files. Move them to `<link>` tags in the HTML `<head>` with `preconnect` to parallelize requests.
