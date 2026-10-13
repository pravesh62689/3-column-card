## 2023-10-27 - CSS @import Render Blocking
**Learning:** Found multiple instances of Google Fonts being loaded via `@import` in CSS files, which blocks rendering and sequentializes network requests. The imports were also duplicated across `style.css` and `mediastyle.css`.
**Action:** Always move third-party font loading from CSS `@import` directly into HTML `<head>` using `<link rel="stylesheet">` alongside `<link rel="preconnect">` to parallelize asset fetching and reduce First Contentful Paint (FCP).
