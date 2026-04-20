# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for Vinx Pest Control, a pest control company serving South Carolina and Virginia. The site is a vanilla HTML/CSS/JavaScript project without a build system or framework.

## Project Structure

```
Vinx Pest Control Website/
├── index.html              # Homepage
├── about.html              # About page
├── contact.html            # Contact page
├── get-quote.html          # Quote request form
├── css/style.css           # Main stylesheet
├── js/
│   ├── script.js           # Main JavaScript (mobile menu, forms, animations)
│   └── main.js             # Additional JS
├── services/               # Service-specific pages (7 pages)
│   ├── residential-pest-control.html
│   ├── commercial-pest-control.html
│   ├── bed-bug-control.html
│   ├── mosquito-control.html
│   ├── termite-control.html
│   ├── rodent-control.html
│   └── cockroach-control.html
├── locations/              # Location-specific pages (~50 pages for SC/VA cities)
├── images/                 # Image assets organized by year and type
└── vinxpestcontrol-com-*   # WordPress backup export (reference only)
```

## Development

This is a static site with no build process. To preview:
- Open any HTML file directly in a browser, or
- Use a local server: `python -m http.server 8000` or `npx serve`

## Design System

CSS variables are defined in both `css/style.css` and inline in HTML files:
- Primary green: `#36A74D` / `#39b44a`
- Dark green: `#113D3C`
- Fonts: Oswald (headings), system fonts (body)
- Icons: Font Awesome 6.4.0 (CDN)

## Page Templates

All pages share a common structure:
1. Top bar with phone number
2. Main nav with logo, dropdown menus, and "Get A Quote" CTA
3. Page-specific content sections
4. Footer with contact info and links

When creating new pages:
- Use relative paths (`../css/style.css`, `../images/...`) from subdirectories
- Include fallback for logo image via `onerror` attribute
- Maintain consistent nav menu structure across all pages

## Key JavaScript Features (js/script.js)

- Mobile menu toggle with click-outside-to-close
- Header scroll effects
- Form validation with notification system
- Scroll-triggered animations using IntersectionObserver
- Phone number auto-formatting for tel inputs
- FAQ accordion functionality

## WordPress Backup

The `vinxpestcontrol-com-*` directory contains extracted WordPress data including:
- Plugin configurations (Divi theme, SEO plugins, etc.)
- Cached CSS/JS from the original WordPress site
- This is reference material from the original site, not active code
