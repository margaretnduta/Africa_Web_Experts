# Africa Web Experts — Official Website

> **AI-powered web applications — modern, fast, and built to convert.**
> Based in Nairobi, Kenya. Serving clients globally.

![Status](https://img.shields.io/badge/status-live-brightgreen)
![Pages](https://img.shields.io/badge/pages-6-blue)
![Responsive](https://img.shields.io/badge/responsive-yes-success)
![SEO](https://img.shields.io/badge/SEO-optimized-orange)

---

## About

This repository contains the complete source code for the **Africa Web Experts (AWE)** website — a multi-page, fully responsive, SEO-optimized static website built for an AI-native web development agency based in Nairobi, Kenya.

Africa Web Experts builds production-grade web applications using AI-assisted development workflows, delivering projects in days instead of months. The website itself demonstrates this philosophy: clean code, fast performance, and modern design without relying on heavy frameworks or CMS dependencies.

**Live site:** [africawebexperts.com](https://awe.margaretwambui.co.ke)

---

## Pages

| File | Page | Description |
|------|------|-------------|
| `index.html` | Home | Landing page with hero, services overview, process steps, differentiators, tech stack, testimonials, and contact form |
| `services.html` | Services | Detailed breakdown of all 6 service offerings with features, delivery timelines, tech stacks, and individual CTAs |
| `process.html` | Process | Immersive vertical timeline of the 4-phase development process, AWE vs. traditional agency comparison, tools section |
| `whyawe.html` | Why AWE | Expanded differentiators, founder story, company values, client results with metrics, technical philosophy |
| `projects.html` | Projects | Portfolio showcasing 12 real client projects with category filtering, live site links, and WhatsApp inquiry buttons |
| `Contact.html` | Contact | Full contact form with validation, multiple contact channels (email, WhatsApp, phone), business hours, FAQ |

---

## Features

### Design & UI
- **Dark theme** with indigo/teal gradient accent system
- **Noise texture overlay** for depth and atmosphere
- **Animated floating orbs** on hero sections
- **Scroll-triggered reveal animations** with staggered delays
- **Hover micro-interactions** on cards, buttons, and navigation
- **Consistent design tokens** via CSS custom properties across all pages

### Navigation & Mobile
- **Fixed navbar** with backdrop blur and scroll shadow
- **Full-screen off-canvas mobile menu** with slide-and-fade animation
- **Staggered menu item entrance** (60ms sequential delay per item)
- **Hamburger-to-X animated toggle** with CSS transforms
- **Scroll position preservation** when opening/closing mobile menu
- **Escape key, backdrop tap, and resize auto-close** handlers
- **Touch event prevention** on menu overlay to prevent background scroll
- **Active page indicator** with gradient underline on current nav item

### SEO
- **Unique `<title>` and `<meta description>`** per page targeting specific keywords
- **Open Graph and Twitter Card meta** tags on every page
- **Structured data (JSON-LD)** schemas on every page:
  - `ProfessionalService` (home)
  - `Service` with `OfferCatalog` (services)
  - `HowTo` with steps (process)
  - `Organization` (why AWE)
  - `CollectionPage` (projects)
  - `ContactPage` with `ContactPoint` (contact)
  - `FAQPage` on 4 pages (services, process, why AWE, contact)
  - `BreadcrumbList` on all inner pages
- **Semantic HTML5** with proper heading hierarchy (single H1 per page)
- **Canonical URLs** on every page
- **`aria-label` attributes** on all sections and interactive elements
- **Descriptive `alt` text** on all images

### Performance
- **Zero JavaScript frameworks** — pure vanilla JS
- **No external CSS libraries** — all styles are custom
- **Font preconnect and display swap** for Google Fonts
- **Lazy-loaded images** with `loading="lazy"` and `onerror` fallbacks
- **Minimal DOM nesting** for fast rendering
- **CSS-only animations** wherever possible (JS only for intersection observer)

### Contact & Lead Generation
- **Full contact form** with client-side validation (name, email, phone, project type, budget selector, message)
- **Budget range picker** with selectable chip buttons
- **Loading spinner** and **animated success state** on form submission
- **Mailto fallback** pre-fills the user's email client with all form data
- **Multiple contact channels**: email link, WhatsApp deep link with pre-filled message, direct phone link
- **Business hours display** with automatic today-highlighting via JavaScript

### Portfolio (Projects Page)
- **12 real client projects** with live mockup images
- **Category filter system** (All, E-Commerce, Personal Brand, Services, Healthcare, Hospitality, Education)
- **"View Site" buttons** linking to live production URLs
- **"Ask on WhatsApp" buttons** with project-specific pre-filled messages
- **Image fallback placeholders** via `onerror` handler

---

## Tech Stack

| Category | Technology |
|----------|-----------|
| Markup | HTML5 (semantic) |
| Styling | CSS3 (custom properties, grid, flexbox, animations, media queries) |
| Scripting | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts — Plus Jakarta Sans, Inter, JetBrains Mono |
| Icons | Inline SVG (no icon library dependency) |
| Hosting | Static file hosting (Vercel / Netlify / GitHub Pages compatible) |

---

## Project Structure

```
africa-web-experts/
├── index.html          # Home / Landing page
├── services.html       # Services page
├── process.html        # Process page
├── whyawe.html         # Why AWE page
├── projects.html       # Projects / Portfolio page
├── Contact.html        # Contact page (capital C)
└── README.md           # This file
```

> **Note:** `Contact.html` uses a capital "C" in the filename. This is intentional and all internal links reference it correctly as `Contact.html`.

---

## Internal Linking Structure

All pages share a consistent navigation bar and footer with cross-page links:

```
index.html
├── #services (section)      → services.html (page)
├── #process (section)       → process.html (page)
├── #why-awe (section)       → whyawe.html (page)
├── #testimonials (section)  → projects.html (page)
└── #contact (section)       → Contact.html (page)
```

- **index.html** uses `#anchor` links for on-page navigation
- **All inner pages** use `filename.html` links for cross-page navigation
- **CTA buttons** across all pages link to `Contact.html`
- **Logo** on inner pages links to `index.html`; on index.html it links to `#hero`

---

## Responsive Breakpoints

| Breakpoint | Layout Changes |
|------------|---------------|
| `> 1024px` | Full desktop layout — 3-column grids, side-by-side sections |
| `768px – 1024px` | Tablet — 2-column grids, stacked alternating sections |
| `< 768px` | Mobile — single column, full-screen off-canvas menu, stacked buttons |
| `< 480px` | Small phone — reduced padding, smaller headings, compact elements |

---

## Deployment

This is a static website with no build step, no dependencies, and no server-side processing. Deploy by uploading the HTML files to any static hosting provider.

### GitHub Pages
```bash
# Push to main branch, enable Pages in repo settings
git add .
git commit -m "Deploy Africa Web Experts website"
git push origin main
```

### Netlify
```bash
# Drag and drop the project folder into Netlify dashboard
# Or connect the GitHub repo for automatic deploys
```

### Vercel
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel --prod
```

### Manual / cPanel / Shared Hosting
Upload all `.html` files to the `public_html` or root directory of your hosting account.

---

## Brand Design Tokens

These CSS custom properties define the visual identity and are consistent across all pages:

```css
:root {
  --bg: #0A0A0B;            /* Page background */
  --surface: #141416;        /* Card/section background */
  --surface-2: #1C1C1F;      /* Elevated surface */
  --border: #27272A;          /* Borders and dividers */
  --text-primary: #FAFAFA;    /* Primary text */
  --text-secondary: #94A3B8;  /* Secondary text */
  --text-muted: #64748B;      /* Muted/caption text */
  --indigo: #6366F1;          /* Primary brand color */
  --indigo-glow: #818CF8;     /* Hover state */
  --indigo-light: #A5B4FC;    /* Light accent */
  --teal: #14B8A6;            /* Secondary accent */
  --teal-light: #5EEAD4;      /* Light secondary */
  --gradient: linear-gradient(135deg, #6366F1, #14B8A6);
}
```

### Typography
- **Display / Headings:** Plus Jakarta Sans (700, 800)
- **Body:** Inter (400, 500, 600)
- **Monospace / Labels:** JetBrains Mono (500, 700)

---

## Browser Support

| Browser | Version |
|---------|---------|
| Chrome | 90+ |
| Firefox | 88+ |
| Safari | 14+ |
| Edge | 90+ |
| Mobile Safari (iOS) | 14+ |
| Chrome Android | 90+ |
| Samsung Internet | 14+ |

---

## Author

**Margaret Wambui**
Founder & Lead Engineer, Africa Web Experts
**Elvis Warutumo Gitau**

- Website: [africawebexperts.com](https://awe.margaretwambui.co.ke)
- Email: [hello@africawebexperts.com](mailto:hello@africawebexperts.com)
- WhatsApp: [+254 706 385 784](https://wa.me/254706385784)
- Location: Nairobi, Kenya

---

## License

Copyright © 2026 Africa Web Experts. All rights reserved.

This codebase is proprietary. Unauthorized reproduction, distribution, or use of this code or design is prohibited without explicit written permission from Africa Web Experts.

---

*Designed & built with AI.*