# Engineering Process & SDLC Spec

This document details the Software Development Life Cycle (SDLC) process, research, requirements, and planning for the personal website.

---

## 1. Ideation & Problem Definition

### The Problem

I want to show and market my skills to be hired as a software engineer—specifically as a web application and website developer.

### The Target Audience

My target audience is small to medium-sized businesses and organizations that need a **professional website** or **web app** to help grow their business.

### Goals and Success Metrics

- The website should be professional, modern, and easy to navigate.
- The website should be mobile-friendly and responsive.
- The website should be fast, secure, and reliable measured by:
  - [Google Page Speed Insights](https://pagespeed.web.dev/)
  - [PostHog](https://eu.posthog.com/) (If setup)
  - [Google Search Console](https://search.google.com/)

- The website should be easy to update and maintain.
- The website should generate leads for my services.

---

## 2. Research & Feasibility

The goal is to demonstrate design capabilities while proving to clients that I have the technical know-how to implement these designs in real-world scenarios.

### Inspiration & Competitive Analysis

- **Portfolios:**
  - [Brittany Chiang](https://brittanychiang.com/)
  - [Adham Dannaway](https://www.adhamdannaway.com/contact)
  - [Matt Farley](https://mattfarley.ca/)
- **Header inspiration:**
  - [Travelling Distribution](https://www.travellingdistribution.com/)
  - [Benjamin Jochims](https://benjaminjochims.de/)
- **Layout inspiration:**
  - [Saumya Chaturvedi](https://saumyachaturvedi.com/)

---

## 3. Requirements Gathering

### Functional Requirements

- **Project Showcase**: A gallery of past projects with descriptions, tech stacks, and links to live demos/source code.
- **Skills Section**: A visual representation of technical expertise (languages, frameworks, tools).
- **Contact Form**: A functional way for potential clients to reach out directly.
- **About Me**: A brief professional background and value proposition.
- **Blog/Articles**: (Optional) A section to share technical knowledge and thought leadership.
- **Resume Download**: A direct link to download a PDF version of my CV.

### Non-Functional Requirements

- **Performance**: Lighthouse score of 90+ for performance and SEO.
- **Responsiveness**: Seamless experience across mobile, tablet, and desktop.
- **Accessibility**: Compliance with WCAG 2.1 standards.
- **Security**: Protection against common web vulnerabilities (XSS, CSRF) and secure contact form handling.

### User Stories & Use Cases

- **As a recruiter**, I want to quickly see the developer's top projects so that I can assess their technical fit for a role.
- **As a business owner**, I want to contact the developer easily so that I can discuss a potential project.
- **As a visitor**, I want the site to load quickly on my phone so that I don't lose interest.

---

## 4. Project Roadmap & Phases

- **Phase 1**: MVP (Minimum Viable Product) with About, Skills, and Projects (Static pages).
- **Phase 2**: Integration of a Contact Form (via Resend) and Markdown/MDX for blog posts.
- **Phase 3**: Advanced animations (Framer Motion) and performance optimization.

---

## 5. UI/UX Design

- **User flow mapping**: Mapping navigation paths from landing page to projects and contact forms.
- **Wireframes & mockups**: Creating layout grids for clean responsive alignment.
- **Prototyping**: Interactive testing of hover transitions and mobile menus.

---

## 6. Setting Up a Dev Environment

- Setup `AGENTS.md`
- **Version Control**: Git with GitHub (maintaining `main`/`production` and `dev`/`feature` branches).
- **Coding Standards**: Prettier, ESLint, and TypeScript configurations.
- **Testing**: Pre-commit hooks for linting, and component test suites.
- **CI/CD Pipeline**: Automated deployment to VPS on git push (via Coolify or custom GitHub Actions + Webhooks).

---

## 7. Testing & Quality Assurance

- **Automated Tests**: Unit, integration, end-to-end (Playwright), and pre-commit checks.
- **Manual Testing**: Cross-browser UX testing and mobile device testing.

---

## 8. Deployment & Release

- **Environments**: Local Dev → Production (VPS / Self-Hosted Docker Container).
- **Infrastructure**: Single VPS (Hetzner, DigitalOcean, or similar) with **Nginx** or **Caddy** or **Traefik** as a reverse proxy, managing SSL (Let's Encrypt).
- **Deployment Tool**: **Coolify** (recommended for UI-based hosting) or a multi-stage **Docker Compose** configuration with PM2 fallback.
- **Monitoring**: Web Vitals monitoring, self-hosted analytics (e.g., Umami or Plausible self-hosted), and error tracking (Sentry).
- **Release Strategy**: Git-based continuous deployment triggering container rebuilds.

---

## 9. Maintenance & Continuous Improvement

- **Monitor Feedback**: Analytics review, form submissions, and user interactions.
- **Security Patches**: Automatic dependency updates via Dependabot.
- **Refactoring**: Reducing technical debt, optimizing package bundle sizes.

---

## 10. Scaling & Long-Term Growth

- **Edge & CDN Caching**: Placing **Cloudflare** in front of the self-hosted VPS for global edge caching of static assets and DDoS protection.
- **Standalone Docker Output**: Enabling Next.js standalone mode (`output: 'standalone'`) to build highly optimized, lightweight Docker images.
- **Caching Layer**: Integrating **Redis** if scaling past a single server instance to coordinate cache storage.
- **Static Site Generation (SSG)**: Pre-rendering content at build time to reduce runtime CPU load on the VPS.
- **Asset Optimization**: Setting up a custom cache folder structure for Next.js image optimization inside the Docker volume.
