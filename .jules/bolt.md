## 2024-05-17 - [Font @import Performance Anti-Pattern]
**Learning:** Found a significant anti-pattern where Google Fonts were being loaded via duplicated `@import` statements across multiple CSS files, causing blocking network requests and waterfall loading delays.
**Action:** Always migrate `@import` font declarations in CSS to `<link rel="preconnect">` and `<link rel="stylesheet">` tags in the HTML `<head>` to allow parallel downloading and improve First Contentful Paint.
