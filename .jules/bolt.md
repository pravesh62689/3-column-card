## 2024-10-29 - [Eliminate CSS @import for fonts]
**Learning:** Using `@import` in CSS to load Google Fonts (or any external resources) introduces a performance bottleneck because the browser must wait to download and parse the CSS file before discovering the font dependency. This blocks parallel downloads.
**Action:** When reviewing frontend code, check CSS files for `@import` statements for fonts. Move them to `<link rel="stylesheet">` tags in the HTML `<head>` and use `<link rel="preconnect">` for the font domains to accelerate the TLS handshake and connection establishment.
