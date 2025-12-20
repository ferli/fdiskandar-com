# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**Rinji.id** is a static artifact website—a philosophy-driven digital archive focused on long-term thinking about technology, systems, and leadership. It contains:

- **Philosophy**: Principles around simplicity, data sovereignty, and long-term orientation
- **Static Architecture**: No database, no dynamic backend, no CMS—just HTML, CSS, and semantic structure
- **Content Strategy**: Essays about infrastructure (laptop-as-server), water business systems (PDAM), and leadership decision-making
- **Distribution**: Deployed as static assets via Cloudflare Pages or similar edge networks

### Key Design Principles

The site embodies three core principles:
1. **Radical Simplicity** – No unnecessary complexity; prefer Bash scripts over Kubernetes, static files over databases
2. **Data Sovereignty** – Full control over content; portable, vendor-independent systems
3. **Long-term Orientation** – Decisions made for 5-year relevance, not monthly trends

## Structure

```
/                          # Root: main landing pages
├── index.html             # Homepage with content list
├── manifesto.html         # Core philosophical statement
├── 404.html              # Error page (philosophical tone)
├── style.css             # Single stylesheet (no framework)
├── robots.txt            # SEO configuration
├── sitemap.xml           # Content discovery
├── setup-rinji-id.ps1    # Bootstrapping script (PowerShell)
└── catatan/              # Essays and strategic notes
    └── index.html        # Content index
```

## Development Commands

Since this is a static site with no build process, development is minimal:

**View locally:**
```bash
# Use any HTTP server; Python is commonly available:
python -m http.server 8000
# Then visit http://localhost:8000
```

**Validate HTML structure:**
```bash
# Check for broken links in HTML:
grep -r "href=" *.html catatan/ | grep -v "^http"
```

**CSS validation:**
- Inspect `style.css` for CSS variable consistency (all variables defined in `:root`)
- Use browser DevTools to test dark mode (`prefers-color-scheme: dark`)
- Test responsive breakpoint at 600px

## Design System

### CSS Architecture

The stylesheet uses **CSS custom properties (variables)** rather than preprocessors:

**Light Mode (default):**
```css
--bg-page: #faf9f7        /* Page background */
--text-body: #1c1917      /* Body text */
--text-heading: #0c0a09   /* Headings */
--text-meta: #78716c      /* Metadata, captions */
--border: #e7e5e4         /* Borders, dividers */
--accent: #292524         /* Emphasis */
```

**Dark Mode:** Automatically inverts via `@media (prefers-color-scheme: dark)`

**Typography:**
- **Serif** (Crimson Pro): Body text, article content
- **Sans** (Plus Jakarta Sans): Headings, navigation, UI
- **Mono** (JetBrains Mono): Metadata, code, timestamps

### Semantic Classes

- `.meta` – Small, uppercase metadata labels
- `.content-list` – Styled list of linked articles with title, description
- `.pillar` – Philosophy/principle container (used in manifesto)
- `.page-404` – Centered error page layout
- `[aria-current="page"]` – Navigation highlight (accessibility-first)

### Responsive Design

- **Desktop baseline:** 18px font size, 660px max-width container
- **Mobile (<600px):** 16px font size, reduced padding
- **Print:** Semantic structure preserved; links show URLs in parentheses

## Content Structure

All pages follow this pattern:

```html
<div class="container">
  <header>
    <nav aria-label="Navigasi utama">
      <!-- Logo + 3-item nav: Beranda, Manifesto, Catatan -->
    </nav>
  </header>
  <main>
    <article>
      <!-- Content here -->
    </article>
  </main>
  <footer>
    <!-- Copyright, Latin motto -->
  </footer>
</div>
```

### Metadata (Open Graph)

Every page includes OG tags for social sharing:
- `og:type`: "website" or "article"
- `og:url`: Full canonical URL
- `og:locale`: "id_ID" (Indonesian)

### Favicon

Embedded SVG data URI with red "R" on dark background—no external file dependency.

## Adding New Content

**New article in catatan/:**

1. Create `catatan/article-name.html`
2. Copy header/nav/footer from `catatan/index.html` or another article
3. Update `<title>`, `<meta name="description">`, and OG tags
4. Add article content in `<article>` tags
5. Update `catatan/index.html` to link the new article in the appropriate section (Infrastruktur, Bisnis Air Minum, Kepemimpinan)

**Styling considerations:**
- No new CSS classes needed for basic content; use `<h2>`, `<h3>`, `<p>`, `<blockquote>`, `<hr>`
- For lists: use `.content-list` if you need styled article links
- For philosophical principles: use `.pillar` + `.pillar-title` + `.pillar-num`

## Deployment

The site is designed for **static hosting** (Cloudflare Pages, GitHub Pages, AWS S3, etc.):

1. Upload entire repository to edge/CDN
2. Set `404.html` as custom 404 handler
3. Set cache headers to long TTL (content rarely changes)
4. Verify `robots.txt` and `sitemap.xml` are accessible at root

**Post-deployment:** Update `sitemap.xml` with new articles and their last-modified dates.

## Language & Localization

- **Primary language:** Indonesian (Bahasa Indonesia)
- **HTML lang attribute:** `lang="id"` on all pages
- **Content style:** Formal, philosophical, long-form essays
- **No translation automation:** Content is curated and hand-written in Indonesian

## Philosophy in Code

The codebase itself reflects the stated principles:

- **No frameworks:** Plain HTML5 + CSS3, no JavaScript
- **Semantic markup:** `<article>`, `<header>`, `<nav>`, `<main>`, `aria-*` attributes
- **Print-friendly:** Full stylesheet for print media
- **Accessibility:** ARIA labels, semantic HTML, high color contrast (WCAG AA+)
- **Performance:** Single CSS file, minimal HTTP requests, no external JS
- **Longevity:** Standards-based code that will work in browsers 5+ years from now

## Common Questions

**Q: Where are draft articles stored?**
A: They're typically in external tools (notes, docs); the repo contains only published content. Drafts are never committed here.

**Q: Can we add JavaScript for interactivity?**
A: No—this contradicts the design philosophy. If a feature requires JS, reconsider whether it's essential.

**Q: Should we optimize images?**
A: There are no images in the current design. If images are added, ensure they're optimized (WebP with fallback) and stored in `/assets/images/`.

**Q: How do we handle analytics?**
A: Keep it minimal. Consider privacy-respecting options like Fathom or no analytics at all, in line with the philosophy of simplicity and data sovereignty.
