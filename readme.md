# Project EDEN website

This repository contains the source files for the Project EDEN website. It is a small, static academic project site: the page is written in HTML and CSS, with client-side JavaScript for language selection. There is no application server or build step.

## Files

- `index.html` — the one-page site, its styles, and the Members section.
- `translations.js` — editable page translations and i18next setup.
- `assets/eden-project-logo.png` — the project logo used in the page header.
- `assets/member-placeholder.svg` — the placeholder portrait used for member cards.

### Editing the site

Edit `index.html` to change the page content or layout. Edit `translations.js` to change translated text. Member cards are in the Members section of `index.html`; replace each placeholder name, academic position, and image path with the person's details and a picture in `assets/`.

You can preview the site by opening `index.html` in a browser. The language selector loads i18next from its public CDN, so translation switching requires an internet connection.

## Cloudflare Pages

The site is ready for a Cloudflare Pages static deployment from this repository:

1. Create a Pages project and connect this GitHub repository.
2. Select the `eden-website` branch (or the branch you intend to publish).
3. Leave the build command blank; set the build output directory to `.` (the repository root).
4. Deploy. Cloudflare Pages serves `index.html` directly.

After the first deployment, add the site's custom domain in the Pages project settings. The domain's authoritative DNS must point to the nameservers shown by the DNS provider you choose. Cloudflare Pages will show the required DNS record and verify the custom domain before serving it over HTTPS.
