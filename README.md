# beautifulgrowth-website

Temporary holding page and future BeautifulGrowth website repository.

Current state:

- public-facing holding page in `index.html`
- simple stylesheet in `styles.css`
- prepared for later cPanel deployment

Goal:

- push from GitHub and deploy into Namecheap hosting once the server-side Git deployment path is finalized.

Deployment:

- primary path: GitHub push to `main` triggers a GitHub Actions deploy to the server over FTPS
- deploy target: `public_html/` on the Namecheap cPanel account
- manual fallback: cPanel Git Version Control can still be used for pull/deploy checks
- required secrets for the automatic path:
  - `FTP_SERVER`
  - `FTP_USERNAME`
  - `FTP_PASSWORD`
- note: shell access is not enabled on this hosting account yet, so FTP is the active deploy bridge for now
