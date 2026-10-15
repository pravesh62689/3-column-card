## 2023-10-15 - CSS @import Bottleneck
**Learning:** Using `@import` within CSS files blocks parallel asset downloading, causing fonts to load much later and leading to a flash of unstyled text or delayed rendering, especially on slow connections.
**Action:** Always prefer `<link rel="preconnect">` and `<link rel="stylesheet">` tags in the HTML `<head>` for fetching external resources like Google Fonts, as the HTML parser immediately starts fetching them in parallel with other assets.
