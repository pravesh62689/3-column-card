## 2024-10-16 - CSS @import Serialization
**Learning:** This static frontend relies on `@import` statements in CSS to load Google Fonts, which creates a serial request chain blocking rendering until both the CSS and font stylesheet are downloaded. Furthermore, there's a duplication of the `@import` statements in the CSS files which can add slightly more overhead.
**Action:** Replace CSS `@import` statements with `<link rel="preconnect">` and `<link rel="stylesheet">` tags in the HTML `<head>` for faster parallel loading of fonts.
