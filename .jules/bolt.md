## 2024-10-14 - Optimize Google Fonts Loading
**Learning:** Replaced CSS `@import` statements for Google Fonts with HTML `<link>` tags and `preconnect` resource hints. Using `@import` delays discovery of font resources until the CSS is downloaded and parsed. Removing duplicate `@import` statements also reduces unnecessary network requests.
**Action:** Always prefer `<link>` tags with `preconnect` in HTML over `@import` in CSS for external font resources to ensure parallel downloading and faster First Contentful Paint.
