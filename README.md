# 🎨 Ta Onaka — Graphic Artist, Printmaker & Visual Designer Portfolio

<div align="center">

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](LICENSE)
[![Netlify Status](https://img.shields.io/badge/Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://taonaka.netlify.app)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![Sass](https://img.shields.io/badge/Sass-CC6699?style=for-the-badge&logo=sass&logoColor=white)](https://sass-lang.com/)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

<p align="center">
  <strong>A modern, responsive creative portfolio website showcasing analog printmaking, branding, screenprinting, and visual design craftsmanship.</strong>
</p>

<p align="center">
  <a href="https://taonaka.netlify.app" target="_blank" rel="noopener noreferrer">
    <img src="https://img.shields.io/badge/🌐_Live_Demo-taonaka.netlify.app-00C7B7?style=for-the-badge" alt="Live Demo" />
  </a>
</p>

[✨ Key Features](#-key-features) • [🛠️ Tech Stack](#️-tech-stack) • [📁 Project Structure](#-project-structure) • [🚀 Getting Started](#-getting-started) • [🌐 Deployment](#-deployment) • [📄 License](#-license)

---

</div>

## 📖 Overview

**Ta Onaka Portfolio** is an expressive, multi-page portfolio website tailored for an independent graphic designer, printmaker, and art director. The project balances the organic, tactile aesthetic of analog printmaking (woodcut, screenprint, risograph) with sleek digital layout precision.

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
- **🚀 Netlify CI/CD Deployment:** Configured with [netlify.toml](netlify.toml) to automatically compile Sass and serve the [public/](public/) directory directly to [taonaka.netlify.app](https://taonaka.netlify.app).

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
| **Netlify** | Continuous deployment, automated Sass build (`npm run build`), and edge hosting |

---

## 📁 Project Structure

```text
graphicArtist/
├── netlify.toml                # Netlify build & deployment configuration
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

### Live Deployment on Netlify

The live version of this project is hosted on **Netlify**:

👉 **[https://taonaka.netlify.app](https://taonaka.netlify.app)**

The project includes a root [`netlify.toml`](netlify.toml) configuration that automatically handles build and publication:

```toml
[build]
  publish = "public"
  command = "npm run build"
```

Every push to `main` triggers Netlify to:
1. Run `npm run build` to compile the compressed Sass bundle.
2. Publish the contents of the `public/` directory directly to the edge CDN.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE) — see the [LICENSE](LICENSE) file for details.
