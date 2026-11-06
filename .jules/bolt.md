## 2023-11-06 - CSS @import Render Blocking
**Learning:** Using `@import` within CSS files causes the browser to download files sequentially (HTML -> CSS -> Font), significantly delaying the critical rendering path and causing FOUT (Flash of Unstyled Text) or slow visual loads.
**Action:** Always extract `@import` font loading into `<link rel="preconnect">` and `<link rel="stylesheet">` tags directly in the HTML `<head>` for parallel downloading.
