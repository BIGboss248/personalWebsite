# Personal Developer Portfolio

A premium, interactive personal website designed to showcase software engineering projects, technical expertise, and blog posts. Built with a focus on web performance, accessibility (WCAG 2.1), and clean code structure.

🔗 **Live Demo:** [portfolio.yourdomain.com](https://yourdomain.com) *(Update with your live URL)*

---

## 🚀 Tech Stack

- **Framework:** [Next.js](https://nextjs.org/) (App Router)
- **Language:** [TypeScript](https://www.typescriptlang.org/)
- **Styling:** [Tailwind CSS](https://tailwindcss.com/)
- **Components:** [Shadcn UI](https://ui.shadcn.com/) / [Radix UI](https://www.radix-ui.com/)
- **Animations:** [Framer Motion](https://www.framer.com/motion/)
- **Contact Form Service:** [Resend](https://resend.com/) + Next.js Server Actions
- **Content Management:** Markdown / MDX
- **Deployment:** Self-Hosted VPS (Docker / Coolify / Traefik)

---

## ✨ Key Features

- **Dynamic Project Showcase:** A clean gallery displaying project details, tech stacks, links, and code repositories.
- **Skills Section:** A structured, categorized breakdown of technical skills mapped to project experiences.
- **Interactive Contact Form:** Secure contact form powered by Next.js Server Actions and Resend with real-time validation.
- **MDX Blog:** Markdown-based blog to share development learnings, with syntax highlighting and read-time estimation.
- **Dark Mode:** System preference auto-detection with smooth transition to manual toggle.
- **Fully Accessible:** Structured with semantic HTML5 markup and compliant with WCAG 2.1 accessibility standards.
- **Support multiple languages**
- **Themes**: Meaning user can choose a main color and the rest might get generated (I guess something like that the idea is a bit unbaked)

---

## 🛠️ Getting Started

### Prerequisites

Make sure you have Node.js installed:
- [Node.js](https://nodejs.org/) (v18.x or later)

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/personalWebsite.git
   cd personalWebsite
   ```

2. **Install dependencies:**
   ```bash
   npm install
   ```

3. **Configure Environment Variables:**
   Create a `.env.local` file in the root directory:
   ```env
   RESEND_API_KEY=your_resend_api_key
   ```

4. **Run the development server:**
   ```bash
   npm run dev
   ```
   Open [http://localhost:3000](http://localhost:3000) in your browser to view the site.

5. **Build for production:**
   ```bash
   npm run build
   ```

### 🐳 Self-Hosting with Docker

This project is optimized for self-hosting. To deploy using Docker:

1. **Enable Standalone Mode**:
   Ensure `output: 'standalone'` is configured in your `next.config.js`.

2. **Docker Compose Setup**:
   Create a `docker-compose.yml` file in the root:
   ```yaml
   services:
     web:
       build: .
       ports:
         - "3000:3000"
       environment:
         - RESEND_API_KEY=${RESEND_API_KEY}
       restart: always
   ```

3. **Deploy using Coolify (Recommended)**:
   - Connect your Github repository to your self-hosted [Coolify](https://coolify.io) instance.
   - Coolify will automatically build the standalone Docker container, provision Let's Encrypt SSL, and route traffic to it.

---

## 📐 Engineering & Development Process

This project is built following a structured Software Development Life Cycle (SDLC) framework, detailing everything from requirement gathering to testing and deployment.

For full details on the planning, user stories, requirements, and long-term roadmap, see [PROCESS.md](./PROCESS.md).
