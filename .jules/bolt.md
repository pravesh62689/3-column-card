## 2024-05-15 - CSS @import duplication
**Learning:** Found an anti-pattern where the same Google Fonts `@import` statement was duplicated twice in `style.css` and twice in `mediastyle.css`. Because `@import` blocks parallel downloads, these multiple chained downloads delay the first paint.
**Action:** When inspecting frontends with multiple CSS files, check for duplicated or overused `@import` rules. Move third-party font/asset loads to HTML `<link rel="preconnect">` and `<link rel="stylesheet">` tags in the `<head>` whenever possible.
