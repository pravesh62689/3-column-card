## 2024-10-11 - Removed CSS @import for fonts
**Learning:** The static project used redundant `@import` statements for Google Fonts across multiple CSS files, causing sequential render-blocking downloads. Moving them to `<link>` tags in the HTML with `preconnect` allows parallel downloads and significantly improves Time to First Byte (TTFB) and First Contentful Paint (FCP).
**Action:** Always check for `@import` in CSS files when auditing static web projects; replace them with `<link>` tags in HTML for parallel loading.
