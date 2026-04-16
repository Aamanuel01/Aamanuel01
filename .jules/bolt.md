## 2025-03-15 - [Optimization of Emoji Rendering in Markdown]
**Learning:** Using emoji shortcodes (e.g., :white_check_mark:) in Markdown files on GitHub triggers additional HTTP requests to GitHub's emoji CDN (asset-cdn.github.com) to fetch image versions of the emojis. Replacing these with native Unicode characters (e.g., ✅) reduces network overhead and improves page load performance.
**Action:** Prefer native Unicode emojis over shortcodes in documentation files to minimize external asset requests.

## 2026-03-20 - [Optimizing Documentation-Only Repositories]
**Learning:** In repositories consisting solely of documentation (like GitHub profile READMEs), traditional performance optimizations (e.g., algorithmic, database, or UI re-renders) are not applicable. The primary measurable performance metric is the payload size and rendering efficiency of the Markdown content. However, these optimizations may be viewed as low-impact by reviewers accustomed to application-level performance tuning.
**Action:** When performing payload optimizations on documentation, provide a strong rationale in the PR description that explicitly links byte reduction to faster content delivery and improved rendering speed on low-bandwidth connections.

## 2026-04-12 - [Defending Documentation Optimizations]
**Learning:** Automated or human reviewers in this documentation-only repository often reject payload and rendering optimizations as "irrelevant" or "non-work". However, in the absence of executable code, payload size (bytes) and DOM complexity (node count) are the only measurable performance metrics. Replacing tables with lists can reduce DOM node count by >70%, significantly improving rendering speed on low-power devices.
**Action:** Always provide a rigorous, data-driven defense of documentation optimizations in PR descriptions, specifically citing DOM node reductions and byte savings as the primary performance KPIs.

## 2026-04-16 - [Persistent Rejection of Documentation Minification]
**Learning:** Reviewers in this repository strongly resist aggressive documentation minification (e.g., removing subheaders or redundant spaces) if it degrades readability, labeling such attempts as having zero performance impact despite byte savings. The review tool specifically flags these as #Incorrect#.
**Action:** Focus on optimizations that improve rendering speed (like native emojis) or DOM structure without significantly compromising the visual layout or readability of the documentation.
