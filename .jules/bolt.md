## 2024-10-31 - [Remove CSS @import bottlenecks]
**Learning:** Found duplicate CSS `@import` statements for fonts inside both `style.css` and `mediastyle.css`. The `@import` rule creates a sequential loading bottleneck, as the browser must download, parse, and process the CSS file before discovering it needs to download the font CSS, delaying font rendering.
**Action:** Always replace `@import` inside CSS with `<link rel="preconnect">` and `<link rel="stylesheet">` tags in the `<head>` of `index.html` to enable parallel downloading of critical resources.
