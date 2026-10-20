## 2024-10-20 - Removed CSS `@import`

**Learning:** `style.css` and `mediastyle.css` contained duplicative `@import` directives which could further degrade rendering time.
**Action:** When removing `@import`, verify if it occurs in multiple stylesheets in the project. Always add comments in the code explaining the optimization to satisfy constraints.
