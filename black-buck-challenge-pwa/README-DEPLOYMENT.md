# The Black Buck Challenge — Vercel PWA starter

This is a first working static-site package based on the Black Buck Challenge content and the existing separated brand-asset collection. It is intended to be reviewed and customized before public launch.

## Files
- `index.html` — website content and sections
- `styles.css` — responsive visual design
- `app.js` — mobile menu and service-worker registration
- `manifest.json` — PWA metadata
- `service-worker.js` — basic offline caching
- `assets/` — existing separated visual assets

## Preview locally
You can open `index.html` to inspect the basic page. For PWA/service-worker testing, run a local web server (service workers do not work reliably from a `file://` URL). For example, if Python is installed:
`python -m http.server 8000`
Then open `http://localhost:8000`.

## Deploy to Vercel
1. Extract this ZIP to a folder on your computer.
2. Create a GitHub repository and upload the contents of this folder to the repository root.
3. In Vercel, choose **Add New → Project**, import that repository, and select **Other** as the framework preset. No build command is required; the output directory is the project root (`.`).
4. Deploy and test the Vercel preview URL.
5. In Vercel → Project → Settings → Domains, add `black-buck-challenge.com` and follow the exact DNS instructions shown there.
6. In GoDaddy DNS, change only the records Vercel tells you to change. Do not delete MX, TXT, or other email-related records unless you know they are no longer needed.

## Important before launch
- The store buttons are placeholders; no checkout or product sales are connected.
- The donation/participation process is not yet connected. Do not accept or solicit funds through the site until the legal structure, governance, disclosures, and secure payment processor are ready.
- Book download/purchase links are placeholders until the final ebook files and publishing/distribution links are supplied.
- The PWA manifest references the existing logo image for its icon. Before launch, create proper square 192x192 and 512x512 PNG icons and update `manifest.json`.
- Confirm the chosen final homepage images and replace any assets as desired. The project includes a starter visual direction, not a claim that the site is already published.
- The service worker caches the core page for basic offline access. Test the PWA in Chrome DevTools → Application → Manifest and Service Workers after deployment.
- The page currently uses Google Fonts through CSS; if you want fonts to work fully offline, bundle local font files or switch to system fonts.

## Suggested next additions
1. Final business-plan ebook PDF link.
2. Memoir cover and final PDF/EPUB purchase links.
3. Secure hosted checkout for T-shirts and books.
4. Donation provider and participation form.
5. Privacy policy, terms, accessibility check, analytics choice, and any required nonprofit/financial disclosures.
