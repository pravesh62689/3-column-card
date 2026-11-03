## 2024-11-02 - Duplicate Google Fonts @import
**Learning:** Found duplicate `@import` statements for Google Fonts in both `style.css` and `mediastyle.css`. This caused redundant network requests and blocked CSS parsing.
**Action:** Always check for redundant external resource loads in CSS files and migrate them to `<link>` tags in the HTML `<head>` with `preconnect` to allow parallel loading and avoid render-blocking CSS imports.
