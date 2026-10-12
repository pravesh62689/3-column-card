## 2024-05-24 - HTML `<link>` Resource Prioritization vs CSS `@import`

**Learning:** CSS `@import` blocking behavior creates sequential waterfalls. When duplicate `@imports` exist across multiple stylesheets, FCP (First Contentful Paint) is heavily delayed. In projects with CRLF endings, standard Python string replacements can fail silently unless line endings are normalized or explicitly handled via regex.

**Action:** Prefer HTML `<link rel="preconnect">` and `<link rel="stylesheet">` over CSS `@imports` for faster font loading. When using scripts to automate edits in CRLF files, use `newline=''` on file I/O and consider regex (e.g., `re.sub(r'pattern(\r?\n)?', '', content)`) for robust string replacements that handle both LF and CRLF seamlessly.
