## 2024-09-24 - CSS @import duplication
**Learning:** This static site had CSS `@import` rules duplicated in both `style.css` and `mediastyle.css`, compounding the blocking nature of `@import`. Standard line-ending replacements can easily fail on these files due to CRLF `\r\n`.
**Action:** When inspecting static CSS files, look out for `@import` duplication across responsive stylesheets. Always use Python regex replacements for safe multi-line editing of CRLF source files.
