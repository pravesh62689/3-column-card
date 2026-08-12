## 2026-08-12 - [Google Fonts Loading]
**Learning:** Loading Google Fonts via @import in multiple CSS files (style.css, mediastyle.css) prevents parallel loading and causes render-blocking.
**Action:** Removed @import rules from CSS files and added <link rel="preconnect"> and <link rel="stylesheet"> tags directly to index.html's <head>.
