# personalWebsite

This repository is my personal website showcasing my projects and skills creating web apps and native apps.
Right now I follow a set of steps in identifing exacly the need and problem at the start and then follow up on the rest of the steps

## 1. Ideation & Problem Definition

### The problem

I want to show and market my skills to be hired as a software engineer more specificly a web app and website developer.

### The target audience

My target audience are small to medium sized businesses and organizations that need a website or web app developed for their needs. They may not have the budget for a large development firm, but they need a professional website that can help them grow their business.

### Goals and success metrics

- The website should be professional, modern, and easy to navigate.
- The website should be mobile-friendly and responsive.
- The website should be fast and efficient.
- The website should be secure and reliable.
- The website should be easy to update and **maintain**.
- The website should generate leads for my services.

## 2. Research and feasibility

The idea is to show the ability to design greate websites while showing clients the that I have the ability and know how to implement those designs in real world senerios and prove it to them with the quality and functionality of the website.

### Existing solutions and market research

Some good examples (per gemini)

- https://brittanychiang.com/
- https://www.adhamdannaway.com/contact
- https://mattfarley.ca/

### For header

- https://www.travellingdistribution.com/
- https://benjaminjochims.de/

### For layout

- https://saumyachaturvedi.com/

## 3. Requirements gathering

### Functional requirements

- **Project Showcase**: A gallery of past projects with descriptions, tech stacks, and links to live demos/source code.
- **Skills Section**: A visual representation of technical expertise (languages, frameworks, tools).
- **Contact Form**: A functional way for potential clients to reach out directly.
- **About Me**: A brief professional background and value proposition.
- **Blog/Articles**: (Optional) A section to share technical knowledge and thought leadership.
- **Resume Download**: A direct link to download a PDF version of my CV.

### Non-functional requirements

- **Performance**: Lighthouse score of 90+ for performance and SEO.
- **Responsiveness**: Seamless experience across mobile, tablet, and desktop.
- **Accessibility**: Compliance with WCAG 2.1 standards.
- **Security**: Protection against common web vulnerabilities (XSS, CSRF) and secure contact form handling.

### User stories & use cases

- **As a recruiter**, I want to quickly see the developer's top projects so that I can assess their technical fit for a role.
- **As a business owner**, I want to contact the developer easily so that I can discuss a potential project.
- **As a visitor**, I want the site to load quickly on my phone so that I don't lose interest.

## 4. Technical Stack (Proposed)

- **Frontend**: Next.js or React for a dynamic yet SEO-friendly experience.
- **Styling**: Tailwind CSS for rapid, responsive UI development.
- **Deployment**: Vercel or Netlify for automated CI/CD.
- **Backend/CMS**: Payload CMS or Markdown files for easy content management.

## 5. Project Roadmap & Phases


1.  **Phase 1**: MVP(Minimum Viable Product) with About, Skills, and Projects (Static).
2.  **Phase 2**: Integration of a Contact Form and CMS for blog posts.
3.  **Phase 3**: Advanced animations (Framer Motion) and performance optimization.

## System & Architecture Design

- **Functional requirements**: What features must exist?
- **Non-functional requirements**: Performance, security, scalability, UX.
- **User stories & use cases**: “As a user, I want to ___ so that ___.”  

## 6. UI/UX Design

- **User flow mapping**
- **Wireframes & mockups**
- **Prototyping**

## 7. Setting up a dev enviroment

- Setup [[AGENTS.md]]
- **Set up version control**: Git with GitHub/GitLab/Bitbucket.
	- Setting up dev(or feature) and production branches.
- **Define coding standards**: Style guides, code reviews, linting.
- **Testing while coding**: Unit tests, integration tests, test-driven development if possible.
- **CI/CD pipeline**: Automate build, test, deploy. (GitHub Actions)

## 8. Testing & Quality Assurance

- **Automated tests**: Unit, integration, end-to-end, pre-commit tests.
- **Manual testing**: UX testing, exploratory tests.

## 8. Deployment & Release

- **Environments**: Dev → Staging → Production.
- **Monitoring setup**: Logs, error tracking (Sentry), performance metrics (Prometheus/Grafana).
- **Release strategy**: Canary releases, blue-green deployment, or full rollout.

## 9. Maintenance & Continuous Improvement

- **Monitor user feedback**: Surveys, app reviews, analytics.
- **Fix bugs & patch security**: Continuous support.
- **Refactor & optimize**: Clean code, improve performance, reduce tech debt.
- **Feature roadmap**: Plan next iterations.

## 10. Scaling & Long-term Growth

- **Optimize infrastructure**: Containers (Docker), orchestration (Kubernetes).
- **Performance scaling**: Horizontal/vertical scaling, caching, CDNs.
- **New features & innovation**: Keep evolving with user needs and tech trends.
- **Documentation**: Update technical + user docs.
