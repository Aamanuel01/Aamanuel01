## 2025-03-15 - [Optimization of Emoji Rendering in Markdown]
**Learning:** Using emoji shortcodes (e.g., :white_check_mark:) in Markdown files on GitHub triggers additional HTTP requests to GitHub's emoji CDN (asset-cdn.github.com) to fetch image versions of the emojis. Replacing these with native Unicode characters (e.g., ✅) reduces network overhead and improves page load performance.
**Action:** Prefer native Unicode emojis over shortcodes in documentation files to minimize external asset requests.

## 2025-03-16 - [Payload Size Optimization for Profile README]
**Learning:** For documentation-only repositories (like GitHub Profile READMEs), performance can be measured by payload size. Removing redundant HTML comments (template boilerplate), stripping trailing whitespace, and minifying Markdown tables reduces the number of bytes transferred, leading to faster profile page loads.
**Action:** Always strip GitHub template comments and unnecessary whitespace from Markdown documentation to minimize network overhead.
