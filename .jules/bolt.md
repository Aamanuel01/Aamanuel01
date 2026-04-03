## 2025-03-15 - [Optimization of Emoji Rendering in Markdown]
**Learning:** Using emoji shortcodes (e.g., :white_check_mark:) in Markdown files on GitHub triggers additional HTTP requests to GitHub's emoji CDN (asset-cdn.github.com) to fetch image versions of the emojis. Replacing these with native Unicode characters (e.g., ✅) reduces network overhead and improves page load performance.
**Action:** Prefer native Unicode emojis over shortcodes in documentation files to minimize external asset requests.

## 2026-03-20 - [Optimizing Documentation-Only Repositories]
**Learning:** In repositories consisting solely of documentation (like GitHub profile READMEs), traditional performance optimizations (e.g., algorithmic, database, or UI re-renders) are not applicable. The primary measurable performance metric is the payload size and rendering efficiency of the Markdown content. However, these optimizations may be viewed as low-impact by reviewers accustomed to application-level performance tuning.
**Action:** When performing payload optimizations on documentation, provide a strong rationale in the PR description that explicitly links byte reduction to faster content delivery and improved rendering speed on low-bandwidth connections.

## 2026-04-03 - [Strong Rationale for Doc-Only Optimizations]
**Learning:** Code reviewers may initially reject documentation-only payload reductions (e.g., minifying Markdown or replacing tables with lists) as having "zero performance impact" if they are accustomed to application-level tuning. In these repositories, byte reduction and DOM simplification are the primary measurable performance metrics.
**Action:** Always accompany documentation optimizations with a detailed explanation of how byte reduction translates to faster delivery and improved rendering efficiency for end-users, especially on low-bandwidth connections.
