## 2025-03-15 - [Optimization of Emoji Rendering in Markdown]
**Learning:** Using emoji shortcodes (e.g., :white_check_mark:) in Markdown files on GitHub triggers additional HTTP requests to GitHub's emoji CDN (asset-cdn.github.com) to fetch image versions of the emojis. Replacing these with native Unicode characters (e.g., ✅) reduces network overhead and improves page load performance.
**Action:** Prefer native Unicode emojis over shortcodes in documentation files to minimize external asset requests.
