## 2024-10-22 - CSS @import Chaining Bottleneck
**Learning:** Found that `@import` statements for Google Fonts were duplicated across multiple CSS files, causing synchronous blocking and redundant network requests.
**Action:** Always prefer HTML `<link>` tags with `preconnect` for external fonts over CSS `@import` to enable parallel asset downloading and eliminate CSS file chaining.
