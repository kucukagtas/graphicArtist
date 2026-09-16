# 🎨 Ao Tanaka — Graphic Artist, Printmaker & Visual Designer Portfolio

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Sass](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white)](https://sass-lang.com/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)](https://github.com/features/actions)

<p align="center">
  <strong>A modern, responsive creative portfolio website showcasing analog printmaking, branding, screenprinting, and visual design craftsmanship.</strong>
</p>

[✨ Key Features](#-key-features) • [🛠️ Tech Stack](#️-tech-stack) • [📁 Project Structure](#-project-structure) • [🚀 Getting Started](#-getting-started) • [🌐 Deployment](#-deployment) • [📄 License](#-license)

---

</div>

## 📖 Overview

**Ao Tanaka Portfolio** is an expressive, multi-page portfolio website tailored for an independent graphic designer, printmaker, and art director. The project balances the organic, tactile aesthetic of analog printmaking (woodcut, screenprint, risograph) with sleek digital layout precision.

Engineered with a clean **Sass (SCSS)** architecture and structured static assets (`public/`), the project emphasizes fluid typography, interactive component states, accessible navigation, and optimized production stylesheets.

---

## ✨ Key Features

- **📱 Fully Responsive Layout:** Fluid design scaling seamlessly across mobile screens, tablets, laptops, and ultra-wide desktops via custom media queries in `scss/_mobile.scss`.
- **⌨️ Dynamic Hero Typewriter Effect:** Native JavaScript typewriter animation cycling through artist roles (*Graphic Artist*, *Printmaker*, *Visual Designer*) with custom pacing and caret styling.
- **🖼️ Interactive Lightbox Gallery (`projects.html`):** Grid layout of creative posters, packaging, and screenprints integrated with [Lightbox2](https://lokeshdhakar.com/projects/lightbox2/) for full-resolution modal previews and grouping.
- **🎠 Testimonial Carousel (`about.html`):** Smooth, touch-friendly client review slider powered by [Owl Carousel 2](https://owlcarousel2.github.io/OwlCarousel2/).
- **🛠️ Creative Process Breakdown:** Step-by-step presentation of creative workflow (*Ideation & Concept*, *Prototyping*, *Production & Carving*, *Print & Delivery*).
- **🎨 Modular Sass / SCSS Architecture:** Organized partials separating design tokens (colors, fonts, variables), layout components, and page-specific rules.
- **📬 Comprehensive Contact Page (`contact.html`):** Form interface with custom focus states, studio address, direct contact info, and social channels.
- **⚡ Automated Build Pipeline:** Ready-to-use npm scripts for Sass file watching and compressed production builds.
- **🚀 CI/CD Ready:** Pre-configured GitHub Actions workflow automatically compiling Sass and publishing the `public/` directory to **GitHub Pages**.

---

## 🛠️ Tech Stack

| Technology | Purpose |
| :--- | :--- |
| **HTML5** | Semantic, accessible markup across all pages (`index.html`, `about.html`, `projects.html`, `contact.html`) |
| **Sass / SCSS** | Modular styling with nested rules, variables, mixins, and automated compressed output |
| **Vanilla JavaScript** | Custom typewriter animation engine (`public/js/type-writer.js`) |
| **jQuery & Plugins** | Lightweight script handling for [Lightbox2](https://cdnjs.cloudflare.com/ajax/libs/lightbox2/2.11.5/js/lightbox.min.js) and [Owl Carousel 2](https://cdnjs.cloudflare.com/ajax/libs/OwlCarousel2/2.3.4/owl.carousel.min.js) |
| **Google Fonts** | Modern sans-serif typography using [Prompt](https://fonts.google.com/specimen/Prompt) |
| **Font Awesome 7** | Scalable vector iconography for services, process indicators, and social links |
| **Animate.css** | Subtle entry animations for hero elements |
| **GitHub Actions** | Automated CI/CD pipeline building Sass and deploying to GitHub Pages |

---

## 📁 Project Structure

```text
graphicArtist/
├── .github/
│   └── workflows/
│       └── deploy.yml          # Automated GitHub Pages CI/CD workflow
├── .gitignore                  # Excluded files (node_modules, OS files, logs)
├── LICENSE                     # MIT License
├── package.json                # Project scripts, metadata, and dependencies
├── package-lock.json           # Locked dependency versions
├── README.md                   # Project documentation
│
├── scss/                       # Modular Sass source files
│   ├── _about.scss             # Styles for About page & timeline
│   ├── _base.scss              # Global reset, typography, and container
│   ├── _contact.scss           # Form & contact information styles
│   ├── _footer.scss            # Footer layout & social links
│   ├── _header.scss            # Hero header & navigation styles
│   ├── _home.scss              # Home sections (process, skills, stats)
│   ├── _mobile.scss            # Responsive media query breakpoints
│   ├── _projects.scss          # Gallery grid & Lightbox customizations
│   ├── _utilities.scss         # Helper classes (buttons, padding, badges)
│   ├── _variables.scss         # Color palette, font definitions, and tokens
│   └── main.scss               # Main entrypoint importing all partials
│
└── public/                     # Static production distribution directory
    ├── css/
    │   ├── lightbox.min.css    # Lightbox modal stylesheet
    │   ├── main.css            # Compiled & compressed CSS from Sass
    │   └── owl.carousel.min.css# Owl Carousel stylesheet
    ├── img/                    # Optimized artwork images, logos & studio shots
    ├── js/
    │   ├── jquery.min.js       # jQuery library
    │   └── type-writer.js      # Typewriter effect script
    ├── about.html              # Biography, awards & testimonials page
    ├── contact.html            # Contact form & studio details page
    ├── index.html              # Home landing page with hero & process
    └── projects.html           # Artwork gallery & portfolio showcase
```

---

## 🚀 Getting Started

### Prerequisites

Make sure you have [Node.js](https://nodejs.org/) (v16 or newer) installed on your system:

```bash
node -v
npm -v
```

### 1. Clone the Repository

```bash
git clone https://github.com/kucukagtas/graphicArtist.git
cd graphicArtist
```

### 2. Install Dependencies

Install the project development dependencies (Dart Sass compiler):

```bash
npm install
```

### 3. Compile Sass

* **Development (Watch mode):** Automatically watches `scss/` and recompiles `public/css/main.css` on save:
  ```bash
  npm run watch
  ```

* **Production Build:** Compiles a compressed, minified CSS bundle:
  ```bash
  npm run build
  ```

### 4. Run Locally

Open `public/index.html` directly in your browser or use a local development server such as VS Code **Live Server**:

```bash
npx serve public
```

---

## 🌐 Deployment

### Deploying to GitHub Pages (Recommended)

This repository includes a pre-configured GitHub Actions workflow (`.github/workflows/deploy.yml`) that automatically builds Sass and deploys the `public/` directory:

1. Push the repository to GitHub:
   ```bash
   git remote add origin https://github.com/kucukagtas/graphicArtist.git
   git branch -M main
   git push -u origin main
   ```
2. On your GitHub repository page, go to **Settings** → **Pages**.
3. Under **Build and deployment** → **Source**, select **GitHub Actions**.
4. Every push to `main` will automatically build and publish your site!

### Deploying to Netlify or Vercel

If you prefer deploying on **Netlify** or **Vercel**:

* **Build Command:** `npm run build`
* **Publish Directory:** `public`

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — see the [LICENSE](LICENSE) file for details.
