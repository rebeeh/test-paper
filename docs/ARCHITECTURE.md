# Architecture & Technical Decisions

## Overview
**Quantitative Aptitude Learning & Assessment Portal** is a high-performance, responsive, standalone web portal for quantitative aptitude training, placement preparation (CRT), and competitive exams (CAT, GATE, Banking, SSC, UPSC).

### Core Principles
- **Zero Build Tools & Zero Dependencies**: Fully client-side (vanilla HTML5, modern CSS3, vanilla JavaScript). Openable directly via double-click (`file://`) or statically hosted on GitHub Pages.
- **Self-Contained Modules**: Each test, practice tool, and workbook is an autonomous file containing its own styles, logic, questions, and markup to eliminate fragile cross-file bundle dependencies.
- **Mobile-First & Accessible**: Fluid typography, responsive grids, high-contrast WCAG 2.1 AA tokens, keyboard accessibility, and mobile-safe touch targets.

---

## File & Module Inventory

| File | Category | Description | Key Features |
| :--- | :--- | :--- | :--- |
| [`index.html`](../index.html) | Hub / Dashboard | Central portal navigation, concept cheat sheets, and launchpad for all mocks. | Hamburger navigation drawer with safe-area insets, scroll lock, concept modals, dark high-contrast theme. |
| [`aptitude-basics-2.html`](../aptitude-basics-2.html) | Learning Workbook | Visual workbook covering 7 core arithmetic & reasoning topics. | Sticky navigation rail, custom inline SVG diagrams, worked examples, speed shortcuts. |
| [`maths_practice_test.html`](../maths_practice_test.html) | Timed Mock | 50-question, 20-minute timed mock on Profit & Loss, Simple & Compound Interest. | Sticky top timer HUD, instant explanation modal/cards, weakness diagnostics, printable scorecard. |
| [`Number_System_Practice-2.html`](../Number_System_Practice-2.html) | Timed Mock | 50-question, 20-minute sectional mock for Number Systems. | Live timer, instant question feedback, categorized final review. |
| [`Prime_Factorisation_HCF_LCM_50_Question_Quiz.html`](../Prime_Factorisation_HCF_LCM_50_Question_Quiz.html) | Timed Mock | 50-question, 20-minute test on Primes, Prime Factorisation, HCF, and LCM. | Randomized questions & options, navigation grid, printable scorecard. |
| [`quant_quiz.html`](../quant_quiz.html) | Timed Mock | 50-question, 20-minute Quant Sprint on Work, Speed & Distance, and Percentages. | Live timer, topic-level performance breakdown, instant error explanations. |
| [`aptitude_50_questions_20min.html`](../aptitude_50_questions_20min.html) | Timed Mock | 50-question, 20-minute challenge on foundational arithmetic. | Prev/Next question stepper, worked solutions, question status review list. |
| [`factors-practice.html`](../factors-practice.html) | Interactive Drill | 5-tier progressive difficulty practice drill for factors, primes, LCM, and HCF. | Dynamic question generator, instant validation, error review log. |
| [`hcf_lcm_2_number_interactive.html`](../hcf_lcm_2_number_interactive.html) | Visualizer | Interactive 2-number factor and Venn diagram visualizer (range 1–200). | Real-time factor decomposition, shared Venn factor intersection. |
| [`hcf_lcm_3_number_interactive.html`](../hcf_lcm_3_number_interactive.html) | Visualizer | Interactive 3-number factor and Venn diagram visualizer (A, B, C). | Pairwise and 3-way factor overlap visualization, live step-by-step arithmetic. |
| [`README.md`](../README.md) | Documentation | Public-facing documentation, exam targets, module index, deployment instructions. | Formatted for GitHub presentation. |
| [`.agents/rules/`](../.agents/rules/) | Agent Rules | Modular AI agent instructions (`architecture.md`, `conventions.md`). | Auto-discovered by Antigravity. |
| [`.gitignore`](../.gitignore) | VCS Configuration | Ignores OS artifacts, IDE settings, logs, and temporary caches. | Clean repository hygiene. |

---

## Architecture Decision Records (ADRs)

### ADR 1: Zero-Dependency Client-Side Architecture
- **Context**: Users need immediate, frictionless access on any device, local offline study, and direct GitHub Pages deployment without Node/npm build steps.
- **Decision**: All pages are standalone HTML files containing their own embedded CSS and JS (or linking only to Google Fonts/CDN assets).
- **Consequence**: Avoids build pipeline friction and deployment breakage. Each module can be tested and developed in total isolation.

### ADR 2: Strict Terminology Standards ("Portal", Never "Suite")
- **Context**: The project was initially referred to with inconsistent naming, including "Suite".
- **Decision**: Use "Quantitative Aptitude Learning & Assessment Portal" (or "Quantitative Aptitude Portal"). Never use "Suite".
- **Consequence**: Unified branding across all HTML titles, headings, meta tags, and documentation.

### ADR 3: Mobile Navigation & Touch Ergonomics in `index.html`
- **Context**: Smaller mobile viewports (360px–768px) had cramped navigation and poor touch targets.
- **Decision**: Implemented an animated 44×44px hamburger button with accessible ARIA attributes (`aria-expanded`, `aria-controls`, `aria-label`), a frosted backdrop blur drawer, minimum 48px vertical touch targets, safe-area inset padding (`env(safe-area-inset-top)`), and a background scroll lock (`body.nav-open { overflow: hidden; }`).
- **Consequence**: Smooth mobile UX meeting WCAG 2.1 touch target guidelines.

### ADR 4: Autonomous Timed Mock Engine Design
- **Context**: Multiple timed mocks require consistent UX (20-minute timer, progress tracking, question review, scoring).
- **Decision**: Implement a clean, predictable state pattern within each mock script:
  - State object tracking `answers`, `timer`, `isSubmitted`.
  - Fixed 20-minute countdown with visual warning colors at 5m/2m thresholds.
  - Final scorecard rendering with percentage, topic breakdown, and printable styles (`@media print`).
- **Consequence**: High reliability with zero cross-test state leakage.

### ADR 5: Hub-and-Spoke Navigation & Child Page Home Links
- **Context**: Autonomous sub-pages (mocks, visualizers, workbooks) must allow users to freely return to the main dashboard without relying solely on browser history.
- **Decision**: Every child page must provide dedicated, styled "Back to Home" (`index.html`) links in its top HUD, start screen, and final scorecard/footer.
- **Consequence**: Users never get trapped in a quiz or workbook; portal continuity is preserved across mobile and desktop.
