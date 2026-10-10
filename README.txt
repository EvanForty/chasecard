CHASECARD — SINGLE-FILE DEPLOYMENT

The entire application, stylesheet, logo and 26 card images are embedded in index.html. No JavaScript, CSS or image directories are required. Google Fonts is optional; the site has local system-font fallbacks.

1. Extract this ZIP.
2. Upload index.html and vercel.json to the ROOT of the existing GitHub repository, replacing those files. Do not upload the ZIP itself.
3. In Vercel, ensure Root Directory points to that repository root, not public or another subfolder. Framework: Other. Clear old Build/Install Command overrides. Output Directory is . (a single dot), supplied by vercel.json.
4. Deploy the NEW commit, not the previous one. Do not reuse the old build cache.

Old public/src/assets folders can remain: this configuration serves the root index.html and it has no dependency on them. No npm install, build or environment variables are needed.

Original observed failure: the deployed HTML requested /src/app.js, /src/style.css, /src/brand.css and /assets/cards/charizard.png, all of which returned HTTP 404. This package removes those requests entirely.

The page can also be opened directly from index.html to inspect it before deployment. This is the same informational landing page, not a payment or payout backend.
