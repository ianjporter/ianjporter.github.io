# Ian Porter — portfolio starter (modern accessible edition)

A minimalist tile-based portfolio framework with **HTML, CSS, and JavaScript**. White/black with restrained red, yellow and blue geometric accents. No CDN, external fonts, dependencies, package manager, or build step. Works on GitHub Pages.

**You supply the writing.** All bracketed text is placeholder content.

## File map

```text
index.html          Homepage with six linked tiles
about.html          About page
experience.html     Experience page
projects.html       Projects with editable case-study sections
skills.html         Skills page
writing.html        Writing & Research page
contact.html        Contact page
css/styles.css      Entire style system (edit color tokens at top)
js/main.js          Progressive-enhancement mobile menu and footer year
assets/favicon.svg  Browser icon with primary-color accents
ACCESSIBILITY.md    Detailed accessibility checklist for your content
.nojekyll           GitHub Pages compatibility marker
```

## Preview it

Open `index.html` in a browser, or launch a local web server from this folder:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.

## Editing the site

1. In `index.html`, replace the hero placeholders and the six tile descriptions with your own text. The existing tiles all work as links to other pages.
2. Add your content on individual pages by replacing bracketed placeholders. Copy an HTML block if you need more cards, jobs, projects or other entries.
3. Edit the labels and destinations if you'd like different tiles. When adding a tile, update its `href` and create the matching `.html` file.
4. To change the name, professional title or header menu, edit the `header` on **each of the seven HTML pages**. (In VS Code, use global Find/Replace.) This duplication keeps every page navigable even if JavaScript is unavailable.
5. Customize fonts, red/yellow/blue accents, spacing and layout through variables at the top of `css/styles.css`.
6. Put images or a PDF résumé in `assets/` and link to them using relative URLs.

**Accessibility matters when adding content:** Review [ACCESSIBILITY.md](ACCESSIBILITY.md). The framework provides accessibility-friendly structure, but your images, media, PDFs and new content must also be accessible. No website is automatically WCAG-compliant just because the template has semantic HTML.

## Publishing on GitHub Pages

1. In GitHub, create a public repository. A repository named `YOURUSERNAME.github.io` publishes at `https://YOURUSERNAME.github.io/`; another name publishes as a project site with a path segment.
2. Upload the **contents** of this folder to the root of the repository (`index.html` should be in the root), and commit changes.
3. Navigate to **Settings → Pages → Build and deployment**. Choose **Deploy from a branch**; select `main` and `/(root)`; save.
4. Follow the published website link displayed in Pages settings.

Reference: https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Accessibility implementation details

- Navigation, tiles and skip link work by keyboard and screen reader.
- At narrow widths the menu button uses `aria-expanded`, `aria-controls`, native button semantics, and Escape-to-close with focus return.
- If JavaScript is disabled, navigation links remain visible; no critical navigation is JS-only.
- Interactive targets are generously sized. `:focus-visible` styling is high-contrast, and reduced-motion preferences are respected.
- We intentionally use **system sans-serif fonts**. This avoids network dependencies and preserves reader-friendly font rendering.

## Limitations

GitHub Pages hosts static files: contact forms require an external submission service or backend. Do not add fake email addresses or links that lead nowhere. Before sharing this with hiring committees, replace placeholders and manually test the final content as outlined in the accessibility checklist.
