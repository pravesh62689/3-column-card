## 2024-05-24 - @import Render Blocking

**Learning:** Duplicate `@import` rules in multiple CSS files (`style.css` and `mediastyle.css`) block parallel downloads and delay rendering of web fonts by requiring the CSS object model to build before fetching.
**Action:** Always prefer `<link rel="stylesheet">` with `preconnect` in HTML `<head>` over `@import` in CSS files for web fonts to parallelize asset loading and improve the critical rendering path.
