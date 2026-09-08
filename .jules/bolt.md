
## 2026-09-08 - [Optimizing Google Fonts Loading]
**Learning:** Using `@import` in CSS for external fonts blocks parallel downloading and is detrimental to frontend performance.
**Action:** Always load external web fonts using `<link rel="preconnect">` and `<link rel="stylesheet">` directly in the HTML `<head>` instead of `@import` inside the CSS.
