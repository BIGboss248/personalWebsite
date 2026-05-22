# Project Tasks & Roadmap

This checklist tracks the tasks required to build, test, deploy, and maintain the personal website, structured according to the SDLC phases defined in [PROCESS.md](file:///d:/scripts/personalWebsite/PROCESS.md).

---

## Phase 1: Research, Ideation & UI/UX Design
- [ ] **Analyze Inspiration & References**
  - [ ] Study portfolios: Brittany Chiang, Adham Dannaway, Matt Farley
  - [ ] Collect header and layout design ideas (Travelling Distribution, Benjamin Jochims, Saumya Chaturvedi)
- [ ] **Map User Flows**
  - [ ] Outline visitor paths (Landing -> Projects -> Contact)
  - [ ] Define recruiter flow (Quick access to key projects, resume download)
- [ ] **Create Mockups & Wireframes**
  - [ ] Design wireframes for clean responsive layout grids
  - [ ] Use mockups to refine layout, color palettes, and typography
  - [ ] Plan interactive elements, hover transitions, and mobile menu behaviors

---

## Phase 2: Environment Setup & Engineering Standards
- [ ] **Configure Project Repository**
  - [ ] Set up version control (Git) with `main`/`production` and `dev`/`feature` branches
  - [ ] Setup `AGENTS.md` to track agent collaboration configurations
- [ ] **Establish Coding Quality & Tooling**
  - [ ] Set up Next.js / framework project in the workspace
  - [ ] Configure ESLint, Prettier, and TypeScript rules
  - [ ] Set up pre-commit hooks (e.g., Husky, lint-staged) for linting and formatting
- [ ] **Design System Foundation**
  - [ ] Set up `index.css` with CSS variables for color palettes, typography, and spacing tokens

---

## Phase 3: MVP Core Implementation (Static Pages)
- [ ] **About Me Section**
  - [ ] Draft value proposition and professional background copy
  - [ ] Build responsive layout and typography
- [ ] **Skills Section**
  - [ ] Create a visual presentation for technical expertise (languages, frameworks, tools)
- [ ] **Project Showcase**
  - [ ] Select top projects to showcase
  - [ ] Build a grid/gallery showing descriptions, tech stack tags, and links (live demos / source code)
- [ ] **Resume Download**
  - [ ] Format and upload the PDF resume
  - [ ] Add direct download link and button

---

## Phase 4: Dynamic Features & Content Integration
- [ ] **Contact Form Integration**
  - [ ] Create responsive frontend contact form component
  - [ ] Configure Resend API for backend email transmission
  - [ ] Add form validation, anti-spam mechanisms, and success/error states
- [ ] **Blog/Articles Setup (Markdown/MDX)**
  - [ ] Setup MDX parser and blog directory structure
  - [ ] Create blog layout template with responsive typography
  - [ ] Write first markdown article to test parsing and rendering

---

## Phase 5: Polish, Animation & Quality Assurance
- [ ] **Interactive Polish & Animations**
  - [ ] Add micro-animations and smooth transitions (using Framer Motion or pure CSS)
  - [ ] Style hover states for all interactive links and buttons
- [ ] **Testing & Verification**
  - [ ] Set up component and unit test suites
  - [ ] Write end-to-end user flow tests using Playwright
  - [ ] Perform manual cross-browser and mobile device responsiveness testing
- [ ] **Performance & SEO Audit**
  - [ ] Optimize images (formats, responsive sizes) and build bundle sizes
  - [ ] Run Lighthouse tests to verify scores of 90+ for Performance, SEO, and Accessibility

---

## Phase 6: Infrastructure, Deployment & Launch
- [ ] **Infrastructure Provisioning**
  - [ ] Set up a self-hosted VPS (Hetzner, DigitalOcean, etc.)
  - [ ] Configure reverse proxy (Nginx, Caddy, or Traefik) and Let's Encrypt SSL
- [ ] **Containerization & Deployment Tools**
  - [ ] Create a multi-stage Dockerfile or setup Next.js standalone output
  - [ ] Set up Coolify (recommended) or Docker Compose for environment configuration
- [ ] **CI/CD Pipeline Setup**
  - [ ] Configure automated deployments (GitHub Actions or Coolify webhook on push to `main`)
- [ ] **Monitoring & Analytics**
  - [ ] Integrate self-hosted analytics (Umami or Plausible)
  - [ ] Set up error monitoring (Sentry) and Web Vitals tracking

---

## Phase 7: Scaling & Long-Term Growth
- [ ] **CDN & Caching**
  - [ ] Place Cloudflare in front of the VPS for global edge caching and DDoS protection
- [ ] **Server Optimization**
  - [ ] Optimize static site generation (SSG) to minimize runtime CPU usage
  - [ ] Configure Redis for cache coordination if scaling horizontally
- [ ] **Continuous Maintenance**
  - [ ] Set up Dependabot for automatic dependency updates and security patches
  - [ ] Schedule regular refactoring sessions to minimize technical debt
