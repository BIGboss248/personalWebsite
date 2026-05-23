# Engineering Process & SDLC Spec

This document details the Software Development Life Cycle (SDLC) process, research, requirements, and planning for the personal website, aligned with our modern 9-phase project process.

---

## Phase 1: Ideation, Strategy & Briefing

### 1. Problem & User Definitions

#### Define the Problem
I want to show and market my skills to be hired as a software engineer—specifically as a web application and website developer.

#### Identify Target Users
My target audience is small to medium-sized businesses and organizations that need a **professional website** or **web app** to help grow their business. Technical recruiters are also primary target users looking to quickly assess my technical capabilities.

#### Set Goals & Success Metrics
- The website should be professional, modern, and easy to navigate.
- The website should be mobile-friendly and responsive.
- The website should be fast, secure, and reliable measured by:
  - [Google Page Speed Insights](https://pagespeed.web.dev/) (target score of 90+)
  - [PostHog](https://eu.posthog.com/) (privacy-first click tracking)
  - [Google Search Console](https://search.google.com/) (SEO and indexing)
- The website should be easy to update and maintain.
- The website should generate leads for my services.

### 2. Strategy Session & Project Brief
- **The "Why"**: Showcase developer capability, build trust, and acquire clients/roles.
- **Target Audience**: Business owners, managers, and technical recruiters.
- **Category Definition**: Portfolio website & Marketing/Business site (hybrid).
- **Goals & Core Actions**: Lead generation (contact form submission), trust building, and resume download.
- **Key Attributes & Emotions**: Trust, minimalism, premium, modern, professional.
- **Competitor Research & References**:
  - **Portfolios:**
    - [Brittany Chiang](https://brittanychiang.com/)
    - [Adham Dannaway](https://www.adhamdannaway.com/contact)
    - [Matt Farley](https://mattfarley.ca/)
  - **Header inspiration:**
    - [Travelling Distribution](https://www.travellingdistribution.com/)
    - [Benjamin Jochims](https://benjaminjochims.de/)
  - **Layout inspiration:**
    - [Saumya Chaturvedi](https://saumyachaturvedi.com/)

### 3. Requirements Gathering

#### Functional Requirements
- **Project Showcase**: A gallery of past projects with descriptions, tech stacks, and links to live demos/source code.
- **Skills Section**: A visual representation of technical expertise (languages, frameworks, tools).
- **Contact Form**: A functional way for potential clients to reach out directly.
- **About Me**: A brief professional background and value proposition.
- **Blog/Articles**: (Optional) A section to share technical knowledge and thought leadership.
- **Resume Download**: A direct link to download a PDF version of my CV.

#### Non-Functional Requirements
- **Performance**: Lighthouse score of 90+ for performance and SEO.
- **Responsiveness**: Seamless experience across mobile, tablet, and desktop.
- **Accessibility**: Compliance with WCAG 2.1 standards.
- **Security**: Protection against common web vulnerabilities (XSS, CSRF) and secure contact form handling.

#### User Stories & Use Cases
- **As a recruiter**, I want to quickly see the developer's top projects so that I can assess their technical fit for a role.
- **As a business owner**, I want to contact the developer easily so that I can discuss a potential project.
- **As a visitor**, I want the site to load quickly on my phone so that I don't lose interest.

### 4. Project Release Milestones (Roadmap)
- **Phase 1 (Current)**: Strategy, design, and environment setup.
- **Phase 2**: MVP (Minimum Viable Product) with About, Skills, and Projects (Static pages).
- **Phase 3**: Integration of a Contact Form (via Resend) and Markdown/MDX for blog posts.
- **Phase 4**: Advanced animations (Framer Motion) and performance optimization.

---

## Phase 2: Structure, Visual Identity & Design (UX/UI)

### 1. User Flow Mapping
- **Visitor Flow**: Landing Page -> Projects Showcase -> Contact Form.
- **Recruiter Flow**: Landing Page -> Quick Project Review -> Resume Download.
- Mapping done via chatbot/Antigravity using [Mermaid](https://mermaid.js.org/).

### 2. Sitemap & Page Hierarchy
- **Core Pages**:
  - Home (Landing with Hero, Skills, Projects, Contact, Footer)
  - Blog/Articles (Dynamic lists and MDX content pages)
- **Section Layouts**:
  - Navigation, Hero, Skills, Projects/Work, Blog Posts, Contact Form, Footer.
- **Legal/Compliance Pages**:
  - Privacy Policy (Telemetry disclosures, data retention)
  - Terms of Service

### 3. Visual Identity & Asset Gathering
- **Theming & Color Palette**: Cool and modern dark/light mode configurations. CSS variables mapping backgrounds, alternating section colors, border accents, and brand accents.
- **Typography & Logos**: Clean fonts (e.g., Outfit/Inter from Google Fonts). Simple typographic personal logo.
- **Imagery & Icon Sourcing**: Sourced/generated illustrations using AI or SVG vectors, Lucide React icon package.

### 4. Designing
- Page layout generated and prototyped in [Google Stitch](https://stitch.withgoogle.com/).
- Centralized component styling tokens mapped to global CSS variables.

### 5. Technical Architecture & Caching Strategy
- **Rendering Strategy**: Next.js App Router.
  - Home Page: Static Site Generation (SSG) / ISR for fast page loading.
  - Blog/MDX Pages: SSG with MDX parser.
  - Contact Form: Client-Side component communicating with a Server Action.

---

## Phase 3: Dev Environment Setup & Coding Foundation

### 1. Version Control & Standards
- Git repository with `main`/`production` and `dev`/`feature` branches.
- Prettier and ESLint for static analysis and coding consistency.

### 2. Workspace Optimization
- Setup `AGENTS.md` for AI context.
- `.vscode/settings.json`, `launch.json`, `tasks.json`, and `mcp.json` configuration for tools and execution.

### 3. Framework Initialization & Routing Prep
- Next.js initialized using standard configurations.
- Route constants mapped statically to avoid hardcoded strings.
- Client & Static Info Files (emails, handles) centralized in config.

---

## Phase 4: UI & Framework Development

### 1. Layout & Styling Setup
- Configure global CSS variables (`index.css`) matching Phase 2 specifications.
- Root layout scaffolding with correct meta tags, html framing, fonts, and responsive wrappers.

### 2. Component Implementation
- Separate client components (e.g., contact form, theme switchers) from server components (projects, static text).
- Environment variables secured on server side.
- Image components with Next.js built-in optimization.

### 3. Page Checklist
- Rendering and caching strategies defined.
- Content loading via localized configurations.
- Skeletal states using `Suspense` for data streaming.
- Metadata and structured JSON-LD schemas.

### 4. Data Mutations & Caching
- Server Actions for Contact Form submissions.
- Animations (GSAP or pure CSS) layered in at final implementation step.

---

## Phase 5: Quality Assurance & Performance Testing

### 1. Manual & Exploratory Testing
- Multi-device and cross-browser testing (Chrome, Safari, Firefox, Edge).

### 2. Automated Testing
- Unit tests for helper functions.
- Integration tests using Playwright for form submissions and core navigation flow.

### 3. Speed & SEO Diagnostics
- Lighthouse performance audits targeting 90+ across all metrics.

---

## Phase 6: Analytics, Monitoring & Compliance

### 1. Monitoring Stack Configuration
- Sentry integration for real-time error tracking.
- PostHog for privacy-first click analytics and traffic flow.

### 2. Legal & Privacy Hardening
- Telemetry opt-in cookie banner consent gate.
- Masking/scrubbing of PII in telemetry logs.
- Auto-purge retention rules for logs.

### 3. Advanced Instrumentation
- OpenTelemetry if analytics scale demands.

---

## Phase 7: Build & Deployment

### 1. Build Compilation Optimization
- Setup compiler features and dev caching options.

### 2. Environment Variables Configuration
- Separation of development and production `.env` parameters.

### 3. CI/CD & Release Strategy
- Automatic deployment to VPS (Coolify or custom docker runner) upon pushing to the `main` branch.

---

## Phase 8: Maintenance & Continuous Improvement
- Weekly analytic and crash reviews.
- Backlog management via GitHub issues.
- Package updates and code refactoring.

---

## Phase 9: Infrastructure Scaling & Documentation
- Containerization using Docker.
- Caching via CDN (Cloudflare) and Redis database layer.
- Developer onboarding and support documentation.

---

## 🔄 The Continuous Workflow Loop
1. **Plan**: Identify issues/enhancements from telemetry.
2. **Build**: Implement updates and run local tests.
3. **Measure**: Inspect updated Lighthouse scores and Sentry reports.
4. **Learn**: Examine user interaction changes.
5. **Iterate**: Continuous feature/fix cycles.
