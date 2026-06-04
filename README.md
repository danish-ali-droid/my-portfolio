# 🌐 Personal Portfolio Website

> A production-ready, fully responsive portfolio showcasing DevOps engineering capabilities, automated CI/CD workflows, and cloud infrastructure integration — built to the standards of modern web engineering.

[![Deploy](https://github.com/danish-ali-droid/danish-ali-droid.github.io/actions/workflows/deploy.yaml/badge.svg)](https://github.com/danish-ali-droid/danish-ali-droid.github.io/actions/workflows/deploy.yaml)
![Hosted on GitHub Pages](https://img.shields.io/badge/Hosted_on-GitHub_Pages-222?logo=github&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 💻 About the Project

This portfolio is more than a digital résumé — it's a proof-of-concept for modern web engineering standards.

Every decision, from the modular CSS architecture to the artifact-driven deployment pipeline, reflects the practices of a production-grade web project. Built entirely with vanilla HTML5, CSS3, and JavaScript, it deliberately avoids unnecessary framework overhead while still delivering smooth animations, responsive layouts, and cross-browser compatibility.

The goal is to demonstrate that clean engineering and great user experience aren't mutually exclusive — and that infrastructure thinking belongs at every layer of a project, not just the backend.

---

## 🛠️ Tech Stack & Tools

| Layer | Technology |
|---|---|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript (ES6+) |
| **Typography** | Google Fonts — Outfit, JetBrains Mono |
| **Styling & UI** | Custom CSS with CSS Variables, Responsive Web Design, CSS Grid & Flexbox, Keyframe Animations |
| **CI/CD** | GitHub Actions — artifact build & automated deployment |
| **Hosting** | GitHub Pages |
| **Version Control** | Git & GitHub |

---

## ✨ Key Features

- **🤖 Automated CI/CD Pipeline** — Every push to `main` triggers a GitHub Actions workflow that builds the site artifact and deploys it directly to GitHub Pages. Zero manual steps.

- **📱 Fully Responsive** — Optimized across all device breakpoints — Desktop, Tablet, and Mobile — using semantic CSS Grid and Flexbox layouts.

- **⚡ Zero-Dependency Frontend** — No JavaScript frameworks, no bundlers, no bloat. Pure HTML, CSS, and JS delivering fast load times and maximum compatibility.

- **🎨 Component-Driven Design** — Modular, reusable CSS architecture using custom properties (variables) for consistent theming and easy maintenance.

- **🌐 Cross-Browser Compatible** — Built with standard web APIs and progressive enhancement principles to ensure consistent rendering across all modern browsers.

- **✍️ Custom Animations** — Smooth entrance animations, floating badges, rotating rings, and scroll-triggered reveals — all built with CSS keyframes, no animation library required.

- **🏷️ Personal Branding** — Consistent visual identity throughout, using a refined dark/green color system and monospace typography inspired by terminal aesthetics.

---

## 🚀 Getting Started

To run this project locally, you only need a browser — no build tools or package managers required.

### Prerequisites

- Git installed on your machine
- Any modern web browser (Chrome, Firefox, Edge, Safari)

### Clone & Run

```bash
# 1. Clone the repository
git clone https://github.com/danish-ali-droid/danish-ali-droid.github.io.git

# 2. Navigate into the project directory
cd danish-ali-droid.github.io

# 3. Open the site in your browser
#    On Linux/macOS:
open index.html
#    Or simply drag index.html into any browser window
```

> No `npm install`. No build step. Just open `index.html` and it runs.

---

## 🤖 CI/CD Pipeline Architecture

This project uses a fully automated, artifact-driven deployment pipeline powered by **GitHub Actions**.

```
┌─────────────────────────────────────────────────────────────────────┐
│                        CI/CD PIPELINE FLOW                          │
│                                                                     │
│   git push (main)                                                   │
│        │                                                            │
│        ▼                                                            │
│   ┌──────────┐    ┌────────────────┐    ┌───────────────────────┐  │
│   │ Checkout │───▶│ Configure Pages│───▶│  Upload Site Artifact │  │
│   │  Code    │    │  (GH Pages     │    │  (upload-pages-       │  │
│   │  (v4)    │    │   setup)       │    │   artifact@v3)        │  │
│   └──────────┘    └────────────────┘    └───────────┬───────────┘  │
│                                                     │              │
│                                                     ▼              │
│                                         ┌───────────────────────┐  │
│                                         │   Deploy to GitHub    │  │
│                                         │   Pages (v4)          │  │
│                                         │   → Live Production   │  │
│                                         └───────────────────────┘  │
└─────────────────────────────────────────────────────────────────────┘
```

### How it works

1. **Trigger** — A `push` to the `main` branch (or a manual `workflow_dispatch`) kicks off the pipeline.
2. **Build Job** — The workflow checks out the source code, configures the GitHub Pages environment, then packages the entire repository as a deployable artifact using `actions/upload-pages-artifact@v3`.
3. **Deploy Job** — A separate `deploy` job (dependent on a successful `build`) picks up that artifact and publishes it live using `actions/deploy-pages@v4`.
4. **Concurrency Control** — The `cancel-in-progress: true` setting ensures only one deployment runs at a time, preventing race conditions on rapid successive pushes.

> The pipeline uses least-privilege permissions: `contents: read`, `pages: write`, and `id-token: write` — nothing more.

---

## 🤝 Let's Connect

I'm always open to discussing DevOps, cloud infrastructure, or exciting engineering opportunities.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Danish_Ali-0a66c2?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/danish-ali-47950b366)
[![GitHub](https://img.shields.io/badge/GitHub-danish--ali--droid-222?logo=github&logoColor=white)](https://github.com/danish-ali-droid)

Whether you're a recruiter, an engineering manager, or a fellow developer — feel free to reach out. I'm actively building in public and always looking to collaborate on meaningful projects.

---

<p align="center">
  Built with 💚 by <strong>Danish Ali</strong> — DevOps & Cloud Engineer
</p>
