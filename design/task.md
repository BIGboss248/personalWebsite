# Project Tasks & Roadmap

This checklist tracks the tasks required to build, test, deploy, and maintain the personal website, structured according to the 9-phase process defined in [PROCESS.md](PROCESS.md).

---

## Phase 1: Ideation, Strategy & Briefing

- [x] **Problem & User Definitions**
  - [x] Define the Problem: What exact pain point are we solving?
  - [x] Identify Target Users: Recruiters, business owners, and visitors.
  - [x] Set Goals & Success Metrics: Target load speeds, user engagement, and visual feedback.
- [x] **Strategy Session & Project Brief**
  - [x] Document the "Why" for creating the website.
  - [x] Set Category Definition (Portfolio / Business hybrid).
  - [x] Define Goals & Core Actions (Form submission, resume download).
  - [x] Choose Key Attributes & Emotions (Trust, minimalism, premium).
  - [x] Competitor Research: Analyze 3-5 portfolios (Brittany Chiang, Adham Dannaway, Matt Farley, etc.).
  - [x] Use AI to visit sample websites and store design concepts as Markdown in the repository.

---

## Phase 2: Structure, Visual Identity & Design (UX/UI)

- [ ] **User Flow Mapping**
  - [ ] Draw User Flows (Landing -> Projects Archive -> Project Detail -> Contact) using Mermaid.
- [ ] **Sitemap & Page Hierarchy**
  - [ ] Define Navigation & Hierarchy (Home, Projects Archive, Project Detail, Blog, Legal/Compliance pages).
- [ ] **Visual Identity & Asset Gathering**
  - [ ] Collect Mood Board Inspiration (Behance, Dribbble, Pinterest).
  - [ ] Theming & Color Palette: Design setups for Light and Dark themes.
  - [ ] Typography & Logos: Choose font pairings and design/source personal logos.
  - [ ] Imagery & Icon Sourcing: Gather/generate assets and choose an icon set (Lucide).
- [ ] **Designing**
  - [ ] Generate designs and page layouts using Figma or Google Stitch.
  - [ ] Centralized Component Design (Buttons, Cards, Forms, Inputs) to establish styling tokens.
- [ ] **Technical Architecture & Caching Strategy**
  - [ ] Evaluate Page Cacheability based on dynamic/static content.
  - [ ] Select Rendering Strategy (SSG for Home/Projects/Blog, Server Actions for mutations).

---

## Phase 3: Dev Environment Setup & Coding Foundation

- [/] **Version Control & Standards**
  - [x] Initialize Git repository with standard `.gitignore`.
  - [x] Define branching strategy (`main`/`production` and `dev`/`feature`).
  - [ ] Setup coding standards (Prettier, ESLint, TypeScript).
- [ ] **Workspace Optimization**
  - [ ] Set Up AI Context (`AGENTS.md`).
  - [ ] IDE Configuration (`.vscode/settings.json`, `launch.json`, `tasks.json`, `mcp.json`).
- [ ] **Framework Initialization & Routing Prep**
  - [ ] Initialize Tech Stack (Next.js project).
  - [ ] Route Mapping: Define and map routes in a dedicated constants file.
  - [ ] Client & Static Info Files: Store static variables in a config file.
  - [ ] Internationalization (i18n): Prepare multi-language routing and loaders early.

---

## Phase 4: UI & Framework Development

- [ ] **Layout & Styling Setup**
  - [ ] Apply Global Theme: Configure global CSS variables (`index.css`).
  - [ ] Scaffold Root Layout: Scaffolding with HTML frame, fonts, lang attributes, and hydration tags.
  - [ ] Layout Screen Compatibility: Ensure navigation headers and footers are responsive.
- [ ] **Component Implementation**
  - [ ] Build core UI components (Hero, About, Skills grid, Project cards, Footer).
  - [ ] Separate Client/Server logic to maximize loading speed.
  - [ ] Ensure secrets are never exposed on client components.
  - [ ] Image Optimization: Use built-in tags and configure source domains.
  - [ ] Link Optimization: Use prefetching with built-in linking tags.
- [ ] **Page Checklist**
  - [ ] Choose rendering and caching strategy for Home, Projects Archive, Project Detail, and Blog pages.
  - [ ] Load translations and text through dictionaries (no hardcoded copy).
  - [ ] Implement data streaming: Wrap dynamic blocks in `Suspense` with skeleton loading states.
  - [ ] Handle page metadata and JSON-LD schemas.
  - [ ] Build custom error-handling routes (404, error boundary fallback).
  - [ ] Update sitemaps and robots rules.
- [ ] **Data Mutations & Caching**
  - [ ] Optimize Data Fetching: Use parallel fetching (`Promise.all`).
  - [ ] Implement Server Functions: Use Server Actions for Contact Form submissions.
  - [ ] Cache Configuration: Declare caching lifetimes.
  - [ ] Animations: Add micro-animations/transitions (Framer Motion, CSS, or GSAP).

---

## Phase 5: Quality Assurance & Performance Testing

- [ ] **Manual & Exploratory Testing**
  - [ ] Multi-device Testing: Mobile, tablet, desktop viewports.
  - [ ] Cross-browser Audits: Safari, Chrome, Firefox, Edge.
- [ ] **Automated Testing**
  - [ ] Unit Tests: Test helper utilities and simple UI components.
  - [ ] Integration & E2E Tests: Test user flows (contact form submission) using Playwright.
- [ ] **Speed & SEO Diagnostics**
  - [ ] Run audits on Google Page Speed Insights (Target 90+ across all metrics).
  - [ ] Check performance metrics in Search Console and Web Vitals.

---

## Phase 6: Analytics, Monitoring & Compliance

- [ ] **Monitoring Stack Configuration**
  - [ ] Error & Crash Tracking: Integrate Sentry.
  - [ ] Product Analytics: Set up PostHog.
  - [ ] Infrastructure & Vitals: Configure database alerts and cache hit monitors.
- [ ] **Legal & Privacy Hardening**
  - [ ] PII Scrubbing: Enable automatic scrubbing of emails/passwords from logs.
  - [ ] Data Residency: Ensure GDPR compliance where applicable.
  - [ ] Consent Gate: Initialize analytics and telemetry tools only after explicit cookie consent.
  - [ ] User Rights (DSAR): Support user data tracking and deletion.
  - [ ] Retention Rules: Set log expiration to auto-purge (30 to 90 days).
  - [ ] Disclosures: List monitoring tools and AI processing in the Privacy Policy.
- [ ] **Advanced Instrumentation**
  - [ ] OpenTelemetry (OTel): Set up collectors if scale warrants.

---

## Phase 7: Build & Deployment

- [ ] **Build Compilation Optimization**
  - [ ] Enable build cache settings (Turbopack).
  - [ ] Setup compilers (React Compiler) for optimized rendering.
- [ ] **Environment Variables Configuration**
  - [ ] Secrets Management: Configure `.env.local` locally.
  - [ ] Environment Separation: Split values into development and production configurations.
  - [ ] Runtime Loading: Support post-build environment injection.
- [ ] **CI/CD & Release Strategy**
  - [ ] CI Pipeline: Automated build and lint checks on merge requests.
  - [ ] CD Rollout: Configure VPS target platform and setup releases (Canary/Blue-Green).

---

## Phase 8: Maintenance & Continuous Improvement

- [ ] **Monitor & Adjust**: Review error reports, user drop-offs, and analytics weekly.
- [ ] **Agile Backlog**: Track bugs and enhancements via issue trackers (GitHub).
- [ ] **Refactoring**: Reduce technical debt and update dependencies.
- [ ] **Roadmap Planning**: Plan iterations based on actual usage metrics.

---

## Phase 9: Infrastructure Scaling & Documentation

- [ ] **Orchestration**: Package application using Docker.
- [ ] **Caching Layer**: Optimize with Redis caching database and CDN (Cloudflare).
- [ ] **Documentation**: Maintain setup guides, API references, and user guides.

---

## 🔄 The Continuous Workflow Loop

- [ ] **Plan**: Gather telemetry and user feedback, outline sprint items.
- [ ] **Build**: Code in small chunks, test locally.
- [ ] **Measure**: Track PageSpeed, Sentry crashes, and telemetry.
- [ ] **Learn**: Study telemetry deviations and user reviews.
- [ ] **Iterate**: Repeat cycles continuously., API references, and user guides.

---

## 🔄 The Continuous Workflow Loop

- [ ] **Plan**: Gather telemetry and user feedback, outline sprint items.
- [ ] **Build**: Code in small chunks, test locally.
- [ ] **Measure**: Track PageSpeed, Sentry crashes, and telemetry.
- [ ] **Learn**: Study telemetry deviations and user reviews.
- [ ] **Iterate**: Repeat cycles continuously.
