## 2024-05-18 - [CSS @import Performance Anti-Pattern]
**Learning:** Found duplicate Google Fonts `@import` statements in both `style.css` and `mediastyle.css`. The use of `@import` inside CSS causes sequential file loading (render-blocking delay), severely impacting font discovery and First Contentful Paint.
**Action:** Always replace `@import` inside CSS with `<link rel="preconnect">` and `<link>` directly in the HTML `<head>` for faster parallel loading.
