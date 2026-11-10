# BeautifulGrowth.co

Source for the public one-page [BeautifulGrowth.co](https://beautifulgrowth.co/) website.

## Current status — November 10, 2026

The present landing page is approved for public use as an introductory/credibility site. It is intentionally simple; the eventual full site will be planned separately.

The current design uses a midnight-blue palette and a decorative wave SVG in the hero. The page includes:
- The hero headline: "Make your business easier to run and easier to grow."
- Three service lanes: BeautifulGrowth, BeautifulClicks, and BeautifulLedgers (labelled "In development").
- A three-step "Start with the business. Not the tool." section.
- Email-based contact through `hello@beautifulgrowth.co`. There is no contact form or submission backend.

The content, structure, and design are acceptable for now. Avoid speculative redesign work without further approval. The hero's wave graphic was not clearly visible in the owner's latest screenshot; deployment and CSS should be checked if that detail matters.

## Files

- `index.html` — the complete page, including the **currently active inline CSS**. This is the styling source currently used by the live HTML.
- `assets/hero-blue-waves.svg` — hero wave artwork referenced by the inline CSS.
- `styles.css` — legacy separate stylesheet retained in the repository and deployment; currently **not linked by index.html**.
- `.github/workflows/deploy.yml` — GitHub Actions FTPS deployment.

## Publishing

Changes pushed to `main` trigger a GitHub Actions workflow which uploads `index.html`, `styles.css`, and `assets/hero-blue-waves.svg` to the FTPS login root. In this hosting configuration the FTP login root is the site's public document root; **do not add a nested `public_html/` prefix**. The workflow uses repository secrets `FTP_SERVER`, `FTP_USERNAME` and `FTP_PASSWORD`.

Check the Actions run and public response after any future change. Earlier deployment troubleshooting encountered unrelated files and a pre-existing Git checkout in a nested `public_html/` directory; do not delete that directory wholesale.

## Internal project context

The private project, decisions, and dated journal are in the BeautifulGrowth Managed Folder, under:
- `Obsidian/ExecFunc/BeautifulGrowth/Projects/BeautifulGrowth.co/`
- `Obsidian/ExecFunc/BeautifulGrowth/_scribe/journals/2026/11/`

Look for **"BeautifulGrowth.co — Approved Landing Page & Agent Handoff — 2026-11-10"** and **"2026-11-10 — BeautifulGrowth.co Website Closeout Journal"**. These newer Dropbox records supersede the older November 9 project/snapshot descriptions. Keep private planning materials in the Managed Folder rather than this public repository.

## Next checks, not current blockers

- Confirm actual external email delivery/reply to `hello@beautifulgrowth.co`.
- If needed, verify that `/assets/hero-blue-waves.svg` loads publicly and that the wave is visibly rendered.
- Later, consider founder information, approved case studies, dedicated service pages, accessible intake, mobile QA and a full site.
