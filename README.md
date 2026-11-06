# Y.A. Prasetya Putra, S.T. | Aircraft Maintenance Engineer

An interactive, single-page web CV for an aircraft maintenance engineer with 28+ years in aviation. Built as one self-contained HTML file with no frameworks, no build step, and no dependencies to install.

> **Live site:** `https://<your-username>.github.io/<your-repo>/` *(replace after enabling GitHub Pages)*

---

## Overview

The page presents a professional profile covering line maintenance, quality assurance, DGCA assessment, and competency-based training. Visitors move through the CV like a flight path: each section is a "stop" with a small plane marker that follows along.

### Sections

| # | Section | What it covers |
|---|---------|----------------|
| 1 | About | Profile summary and key numbers |
| 2 | Experience | Career timeline, 1996 to present |
| 3 | Licences & Type Ratings | AMEL, B737NG, ATR 72, MD-80/90, DAMEER |
| 4 | Education | Degrees and diplomas |
| 5 | Training & Competencies | Course table and competency chips |
| 6 | Contact | Email and phone links |
| 7 | Career Highlights | Milestones at a glance |
| 8 | Aircraft Experience | Aircraft types with illustrative photos |
| 9 | Infographic CV | One-page visual overview |

## Features

- **Single file:** everything (HTML, CSS, JS, images) lives in `cv-web-final-infographic-large.html`. Images are embedded as base64, so the page works offline except for Google Fonts.
- **Interactive navigation:** click a stop, use Previous/Next, or use the keyboard (`←` `→` `Home` `End`).
- **Light and dark mode:** follows the visitor's system preference via `prefers-color-scheme`.
- **Responsive:** the sidebar becomes a horizontally scrollable tab bar on mobile.
- **Print / Save as PDF:** a dedicated print stylesheet expands all sections into a clean, paginated document. Use the **Save as PDF** button in the hero.
- **Accessible:** skip link, ARIA tab roles, visible focus states, `prefers-reduced-motion` support, and alt text on images.
- **SEO and sharing:** meta description, Open Graph tags, and theme colour.

## Tech Stack

- HTML5, CSS3 (custom properties, grid, flexbox), vanilla JavaScript
- Fonts: [Barlow](https://fonts.google.com/specimen/Barlow) and Barlow Condensed via Google Fonts

## Getting Started

### Run locally

No installation needed. Clone the repo and open the file in a browser:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>
```

Then open `cv-web-final-infographic-large.html` in your browser, or serve it locally:

```bash
# Python 3
python -m http.server 8000
# then visit http://localhost:8000/cv-web-final-infographic-large.html
```

### Deploy with GitHub Pages

1. Rename `cv-web-final-infographic-large.html` to `index.html` (so the site loads at the root URL).
2. Push to GitHub.
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, then **Save**.
5. Your site will be live in a minute or two.

## Customising Content

All content is defined in the `<script>` block at the bottom of the HTML file:

| Data | Variable |
|------|----------|
| Work history | `EXP` |
| Type ratings | `LIC` |
| Education | `EDU` |
| Competency chips | `CH` |
| Training table | `TR` |
| Section text and layout | `T` |
| Embedded images | `IMG` and `INFOGRAPHIC` |

Theme colours are CSS variables at the top of the `<style>` block (`--g`, `--rose`, `--accent`, and so on). Update the burgundy palette there to restyle the whole page.

## Project Structure

```
.
├── cv-web-final-infographic-large.html   # The entire site (rename to index.html for Pages)
└── README.md
```

## Notes

- Aircraft photos in the "Aircraft Experience" section are illustrative portfolio visuals, not aircraft identification records.
- Because images are base64-embedded, the HTML file is large. For easier maintenance, consider moving images to an `assets/` folder and referencing them with normal `<img src>` paths.

## Contact

Based in Sleman, Yogyakarta, Indonesia. Contact details are available on the live site. References available upon request.

## License

© Y.A. Prasetya Putra. All rights reserved. The content of this CV is personal and not licensed for reuse. If you would like to reuse the page *structure* as a template, please open an issue first.
