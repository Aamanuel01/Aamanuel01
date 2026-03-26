## 2025-03-15 - [Optimization of Emoji Rendering in Markdown]
**Learning:** Using emoji shortcodes (e.g., :white_check_mark:) in Markdown files on GitHub triggers additional HTTP requests to GitHub's emoji CDN (asset-cdn.github.com) to fetch image versions of the emojis. Replacing these with native Unicode characters (e.g., ✅) reduces network overhead and improves page load performance.
**Action:** Prefer native Unicode emojis over shortcodes in documentation files to minimize external asset requests.

## 2026-03-20 - [Optimizing Documentation-Only Repositories]
**Learning:** In repositories consisting solely of documentation (like GitHub profile READMEs), traditional performance optimizations (e.g., algorithmic, database, or UI re-renders) are not applicable. The primary measurable performance metric is the payload size and rendering efficiency of the Markdown content. However, these optimizations may be viewed as low-impact by reviewers accustomed to application-level performance tuning.
**Action:** When performing payload optimizations on documentation, provide a strong rationale in the PR description that explicitly links byte reduction to faster content delivery and improved rendering speed on low-bandwidth connections.

## 2026-03-26 - [Minimizing Markdown Table Payload]
**Learning:** GitHub Flavored Markdown (GFM) tables are resilient to minimal formatting. Removing optional leading and trailing pipes can reduce the character count without breaking the rendered structure. However, maintainability and standard formatting (like blank lines around block elements) should be preserved to ensure correct rendering across all GFM-compliant parsers.
**Action:** In payload-constrained environments, use the minimal GFM table syntax: `Col1|Col2` followed by `---|---` and then data rows `Val1|Val2`, while keeping standard blank line separators.
