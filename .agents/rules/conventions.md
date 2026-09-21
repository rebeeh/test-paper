# Project Conventions & Guidelines

- **Platform Terminology**: Refer to this platform as **Quantitative Aptitude Learning & Assessment Portal** (never use the word "Suite").
- **Zero Build Tools & Dependencies**: Keep all modules 100% standalone, client-side, vanilla HTML/CSS/JavaScript. No npm/Vite/Webpack, no third-party runtime frameworks. Openable directly via double-click (`file://`) or statically hosted on GitHub Pages.
- **Self-Contained Modules**: Each practice tool, interactive visualizer, and timed test should be autonomous with its own internal styles and logic.
- **Hub-and-Spoke Navigation Invariant**: Every sub-page, mock test, interactive visualizer, and workbook MUST include visible, accessible, responsive links back to `index.html` ("Back to Home"). Ensure Home links appear in:
  1. Top sticky header / timer HUD bar.
  2. Initial start / introduction view.
  3. Final scorecard / completion action group.
  4. Footer or sticky navigation rail.
- **Portal Catalog & Counter Synchronization**: When introducing a new resource:
  1. Insert a `<div class="portal-card">` into the appropriate `.card-grid` inside `index.html` (ensure `.card-grid` is not closed prematurely).
  2. Maintain WebKit-safe per-section numbering via CSS counters scoped directly to `.card-grid` (`#01+`).
  3. Update `#searchCount` text to reflect the new total (`Showing all N resources`).
  4. Provide rich `data-category` and `data-keywords` for instant discovery.
  5. Update `docs/ARCHITECTURE.md` inventory and `README.md`.
