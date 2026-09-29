## 2024-03-24 - [Render-Blocking Font @imports]
**Learning:** This static repository loads Google fonts via duplicate `@import` rules across multiple CSS files, causing severe sequential render-blocking chaining (Browser -> HTML -> CSS -> @import -> Fonts).
**Action:** Always replace CSS `@import` statements with HTML `<link rel="preconnect">` for third-party fonts to parallelize asset loading and speed up first paint.
