# ChronosPera — Marketing Site

A single-page marketing website for **ChronosPera**, a small distributed technology studio building software, AI/data, cloud, and cybersecurity solutions — and the team behind their flagship product, **Time Wallet**.

**Tagline:** Time. Innovation. Elevated.

## Overview

This is a static, single-file HTML site (`index.html`) with no build step and no external framework dependencies. All CSS and JavaScript are inline in the file. Fonts are loaded from Google Fonts (`Cormorant Garamond` for display type, `Inter` for body text).

## Sections

The page is a single scrollable document with the following sections, each addressable via anchor links in the nav:

| Section | Anchor | Description |
|---|---|---|
| Header / Nav | — | Fixed header with logo, nav links, and a "Get in Touch" CTA. Collapses to a slide-out menu on mobile. |
| Home | `#home` | Hero section with headline, intro copy, CTAs, and a team-location strip. |
| Solutions | `#solutions` | Five service areas: Software Development, AI & Data Engineering, Cloud & DevOps, Cybersecurity, Digital Experience. |
| Time Wallet | `#time-wallet` | Promo for the flagship product (in development). |
| Industries | `#industries` | Industries served: Finance & FinTech, Healthcare, Retail & Commerce, Startups & Enterprise. |
| About Us | `#about` | Team grid — seven people across India, Sri Lanka, Pakistan, Nepal, and the Philippines. |
| Careers | `#careers` | No open roles listed, but invites contact. |
| Insights | `#insights` | Placeholder for future blog/articles. |
| Contact | `#contact` | Contact form (front-end only — see note below). |
| Footer | — | Site links and copyright. |

## Features

- **Responsive design** — breakpoints at 920px (nav collapses to a mobile drawer) and 780px/400px for smaller layout tweaks.
- **Scroll-aware header** — header background/blur/padding change on scroll (`header.scrolled`).
- **Scroll-spy navigation** — active nav link updates based on which section is in view (`IntersectionObserver`).
- **Reveal-on-scroll animations** — elements fade/slide in as they enter the viewport.
- **Animated hero graphics** — SVG skyline with flickering "window" lights and a slowly rotating decorative clock face.
- **Built-in FAQ chatbot** — a lightweight, fully local assistant (bottom-right widget) that matches user input against a keyword-based FAQ list. No external API calls.
- **Contact form** — front-end only; currently just shows a confirmation message on submit.
- **Accessibility touches** — focus-visible outlines, `aria-label`/`aria-live`/`aria-expanded` attributes on interactive elements, reduced-motion support via `prefers-reduced-motion`.
- **SEO/meta** — Open Graph tags, Twitter card, and JSON-LD `Organization` schema.

## Tech Stack

- Plain HTML5, CSS3 (custom properties / CSS variables for theming), and vanilla JavaScript
- No build tools, package manager, or dependencies required
- Google Fonts (Cormorant Garamond, Inter) via CDN

## Getting Started

No installation needed — it's a single static file.

```bash
# Open directly in a browser
open index.html

# Or serve locally (recommended, so relative behavior matches production)
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Before Going Live

A few things are marked in the code as placeholders to update once the site has a real domain:

- **Open Graph URLs** (`og:url`, JSON-LD `url`) — currently set to `https://www.chronospera.com/`.
- **Contact form** — currently front-end only (`e.preventDefault()` + reset). Wire it up to a real form backend or email service before launch.
- **Chatbot** — fully local/static FAQ matching; swap in a real API if more dynamic responses are needed.

## Customization Notes

- Color palette, spacing, and easing are defined as CSS custom properties at the top of the `<style>` block (`:root`), making theme changes straightforward.
- Section content (services, industries, team members, FAQ replies) is written directly in the HTML/JS and can be edited in place — no CMS or data layer.

## License

© 2026 ChronosPera. All rights reserved.
