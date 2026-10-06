## 2024-10-06 - [Avoid duplicate CSS @import for fonts]
**Learning:** Found redundant `@import` statements for the same Google Fonts in multiple CSS files (`style.css`, `mediastyle.css`). This causes blocking network requests.
**Action:** Replaced CSS `@import` statements with `<link rel="preconnect">` and standard `<link rel="stylesheet">` tags in `index.html` to initiate network requests earlier, avoiding parser-blocking operations in stylesheets.
