# FD Iskandar Portfolio — Strategic Technologist for Water Utilities

Static website built with Hugo & PaperMod, deployed on Cloudflare Pages.

## About

This is the professional portfolio of **FD Iskandar**, a Strategic Technologist with 30+ years of experience in:

- **Digital Transformation** — ERP systems, cloud migration, process automation
- **Governance, Risk & Compliance (GRC)** — IT governance frameworks, vendor management, audit readiness
- **Non-Revenue Water (NRW)** — Water loss reduction strategies, SCADA systems, AI/ML applications
- **Cybersecurity** — Critical infrastructure protection, SCADA security, compliance

## Technology Stack

- **Static Site Generator:** Hugo v0.152+
- **Theme:** PaperMod
- **Hosting:** Cloudflare Pages
- **DNS:** Cloudflare
- **Language:** Indonesian (id)

## Project Structure

```
rinji-id/
├── content/              # Markdown files for pages & articles
│   ├── _index.md        # Homepage
│   ├── about.md         # About page
│   ├── contact.md       # Contact page
│   ├── expertise/       # Expertise domain pages
│   └── articles/        # Blog/article section (future)
├── themes/
│   └── PaperMod/        # Hugo theme (submodule)
├── static/              # Images, assets
├── hugo.toml            # Hugo configuration
├── .gitignore           # Git ignore rules
├── LICENSE              # MIT + CC-BY-4.0 for content
└── CLAUDE.md            # Development guidelines

```

## Local Development

### Prerequisites

- Hugo Extended v0.120+
- Git
- Modern web browser

### Setup

```bash
# Clone repository
git clone https://github.com/USERNAME/rinji-id.git
cd rinji-id

# Initialize submodules (for PaperMod theme)
git submodule update --init --recursive

# Run local server
hugo server --buildDrafts

# Visit http://localhost:1313
```

### Build for Production

```bash
# Clean build
hugo --minify

# Output is in ./public/ directory
```

## Deployment

This site is automatically deployed to Cloudflare Pages whenever you push to the `main` branch.

### Setup Cloudflare Pages

1. Connect GitHub repository to Cloudflare Pages
2. Configure build settings:
   - **Framework preset:** Hugo
   - **Build command:** `hugo --minify`
   - **Build output directory:** `public`
   - **Environment variable:** `HUGO_VERSION` = `0.152.2`
3. Point custom domain (rinji.id) to Cloudflare Pages

## Content Guidelines

### Page Structure

All pages include:
- Front matter with title, description, date (if applicable)
- Clean markdown formatting
- Internal links where relevant
- No company-specific identifiable information

### Adding New Articles

```bash
hugo new content articles/article-title.md
```

Edit the markdown file and deploy. Cloudflare Pages will auto-build on push.

## License

### Code & Configuration

MIT License — See `LICENSE` file for details.

### Website Content

Creative Commons Attribution 4.0 International (CC BY 4.0)

You are free to:
- Share and adapt the content
- Use for commercial purposes
- Distribute

As long as you provide **attribution to FD Iskandar**.

[CC BY 4.0 License](https://creativecommons.org/licenses/by/4.0/)

## Contact

- **Email:** contact@rinji.id
- **LinkedIn:** [FD Iskandar](https://linkedin.com/in/fd-iskandar)

## Author

**FD Iskandar** — Strategic Technologist | Digital Transformation | GRC | Water Utilities

---

*Built with ❤️ using Hugo & Cloudflare Pages*
