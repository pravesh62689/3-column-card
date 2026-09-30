## 2024-03-14 - [CSS @import Performance]
**Learning:** This codebase uses CSS `@import` statements for loading Google Fonts, which blocks parallel rendering and significantly delays the First Contentful Paint. Furthermore, the imports were duplicated in multiple files.
**Action:** Always scan CSS files for `@import` statements and move external resource loading (like fonts) to HTML `<link>` tags with `preconnect` resource hints to improve the critical rendering path.
