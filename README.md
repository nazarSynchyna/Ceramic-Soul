# Ceramic Soul

A multi-page frontend website for a ceramic studio, focused on showcasing handmade products, workshop storytelling, and customer contact/newsletter forms.  
The project is built with **Vite 7** and uses modular **SCSS**, interactive UI behavior in vanilla **JavaScript**, and production asset optimization.

---

## 🔗 Demo

Check out the live website on GitHub Pages:  
👉 **[Live Demo](https://nazarsynchyna.github.io/ceramic-soul/)**

---

## Overview

Ceramic Soul is implemented as a static, multi-page web project with the following public pages:

- `index.html` — landing page with hero, activities, contact form, and works slider
- `catalog.html` — product catalog with tabbed content sections
- `blog.html` — blog cards with expandable/interactive read behavior
- `about.html` — workshop story, contact section, and embedded map

The codebase includes:

- reusable header/menu/footer patterns across pages
- responsive layout classes and componentized SCSS partials
- form validation logic for contact and newsletter forms
- Swiper-based gallery slider
- production image optimization through Vite plugin integration

---

## Tech Stack

### Core

- **HTML5** (multi-page architecture)
- **SCSS / Sass** (modular styles with partials)
- **JavaScript (ES Modules)** for UI behavior
- **Vite 7** (`vite@^7.3.1`) as the build tool

### Styling & CSS processing

- **Sass** (`sass@^1.97.3`) for preprocessing
- **PostCSS** (`postcss@^8.5.6`)
- **postcss-pxtorem** (`postcss-pxtorem@^6.1.0`) with global px→rem conversion:
  - `rootValue: 16`
  - `propList: ["*"]`
  - conversion enabled in media queries

### UI & interaction libraries

- **Swiper** (`swiper@^12.1.1`) for the works slider
- **JustValidate** (`just-validate@^4.3.0`) for form validation
- **Font Awesome Kit** (loaded via script tag in HTML)
- **Google Fonts (Barlow)**

### Build-time optimization

- **vite-plugin-imagemin** (`vite-plugin-imagemin@^0.6.1`) configured with:
  - `gifsicle`
  - `optipng`
  - `mozjpeg`
  - `pngquant`
  - `svgo`

---

## Implemented Features (from current code)

- Multi-page routing/build inputs via Vite Rollup config:
  - `index.html`, `catalog.html`, `blog.html`, `about.html`
- Mobile burger menu and overlay navigation structure on all pages
- Catalog tab UI structure (`catalog__tab`, `catalog__content-item`)
- Works slider markup (`.swiper`, `.swiper-wrapper`, navigation arrows, pagination)
- Contact form blocks (`name`, `email`, `question`, consent checkbox)
- Newsletter form blocks (`email`, consent checkbox)
- Embedded Google Map section on About page
- Shared SEO/social meta tags across pages (Open Graph/Twitter metadata)
- Favicon/manifest support via `public/favicon/*`

---

## Project Structure

```text
ceramic-soul/
├─ about.html                  # About page (story, contact form, map)
├─ blog.html                   # Blog page with article cards
├─ catalog.html                # Catalog page with category tabs/cards
├─ index.html                  # Landing page (hero, activities, contact, slider)
├─ package.json                # Dependencies and npm scripts
├─ package-lock.json
├─ postcss.config.js           # PostCSS + pxtorem configuration
├─ vite.config.js              # Vite build config + image optimization + multi-page inputs
├─ public/
│  └─ favicon/                 # Favicon set, manifest, platform icons
└─ src/
   ├─ css/                     # Compiled/auxiliary CSS assets
   ├─ img/                     # Project image assets (promo, works, form, about, etc.)
   ├─ js/                      # Frontend JavaScript (UI logic, validation, interactions)
   ├─ logo/                    # Brand logo assets
   └─ sass/                    # SCSS source structure (base/layout/components/media)
```

---

## Installation

```bash
npm install
```

---

## Available Scripts

The repository currently defines these scripts in `package.json`:

```bash
npm run build
```

- Builds the multi-page production bundle using Vite with configured image optimization.

```bash
npm test
```

- Placeholder script that exits with an error (`"Error: no test specified"`).

---

## Build Notes

- Project is configured for **build output** and multi-page bundling.
- No `dev` script is currently defined in `package.json`; add one if local dev server workflow is needed (e.g., `vite`).

---

## Credits

Created by **Nazar Synchyna**.
