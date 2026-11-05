## 2024-11-05 - Avoid CSS @import for Web Fonts
**Learning:** In a static HTML/CSS structure, using duplicate `@import` rules inside CSS for Google Fonts forces the browser to sequentially load the HTML, parse the CSS, discover the import, and then download the font files (which can cause severe render blocking and duplicate requests if imported multiple times).
**Action:** Always favor `<link rel="stylesheet">` and `<link rel="preconnect">` in the HTML `<head>` over CSS `@import` statements to parallelize resource loading.
