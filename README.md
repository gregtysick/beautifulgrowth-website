# beautifulgrowth-website

Temporary holding page and future BeautifulGrowth website repository.

Current state:

- public-facing holding page in `index.html`
- simple stylesheet in `styles.css`
- prepared for later cPanel deployment

Goal:

- push from GitHub and deploy into Namecheap hosting once the server-side Git deployment path is finalized.

Deployment:

- primary path: GitHub push to `main` triggers a GitHub Actions deploy to cPanel over SSH
- fallback path: cPanel Git Version Control can still be used for manual pull/deploy checks
- required secrets for the automatic path:
  - `CPANEL_HOST`
  - `CPANEL_USER`
  - `CPANEL_PORT`
  - `CPANEL_SSH_KEY`
  - `CPANEL_DOCROOT`
