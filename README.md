# VHDL Manual Site (`Site/`)

No-build static site for GitHub Pages. This repository folder provides stable HTTPS URLs required by App Store Connect.

## Files

- `index.html`: marketing/landing page
- `privacy/index.html`: privacy policy URL
- `support/index.html`: support URL with contact + troubleshooting
- `terms/index.html`: terms of use URL
- `assets/app-icon.png`: app icon used on the marketing page
- `styles.css`: shared styling
- `404.html`: custom not-found page for GitHub Pages

## Local preview (no build step)

From the monorepo root:

```bash
cd Site
python3 -m http.server 8000
```

Open `http://localhost:8000/`.

## GitHub Pages publishing

1. Push the `Site/` submodule repository (`vhdl_manual_site`) to GitHub.
2. In the `vhdl_manual_site` repo settings, open **Pages**.
3. Set source to **Deploy from a branch**.
4. Select branch `main` (or your published branch) and folder `/ (root)`.
5. Save and wait for GitHub Pages deployment to complete.
6. Verify these paths load over HTTPS:
   - `/`
   - `/privacy/`
   - `/support/`
   - `/terms/`

## App Store Connect URL map

Use one of the hosting modes below.

### Project Pages mode

If GitHub username is `<username>` and repo name is `vhdl-manual-site`:

- Marketing URL: `https://<username>.github.io/vhdl-manual-site/`
- Privacy Policy URL: `https://<username>.github.io/vhdl-manual-site/privacy/`
- Support URL: `https://<username>.github.io/vhdl-manual-site/support/`
- Terms of Use URL: `https://<username>.github.io/vhdl-manual-site/terms/`

Current repo remote is `mdovale/vhdl_manual_site`. If you keep that exact repository name, replace `vhdl-manual-site` with `vhdl_manual_site` in all project-pages URLs.

### Custom domain mode

If a custom domain is configured:

- Marketing URL: `https://<domain>/`
- Privacy Policy URL: `https://<domain>/privacy/`
- Support URL: `https://<domain>/support/`
- Terms of Use URL: `https://<domain>/terms/`

## Required owner placeholders

Replace these before production submission:

- Optional legal specificity in Terms of Use governing-law jurisdiction text
