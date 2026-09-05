# Nudge website

The marketing, privacy, terms, and support pages for the Nudge iOS app.
Plain HTML and CSS. No build step. Deployed on Vercel.

## Pages

| File | Purpose |
|---|---|
| `index.html` | Landing page |
| `privacy.html` | Privacy policy (App Store Connect privacy URL) |
| `terms.html` | Terms of use, supplementing Apple's standard EULA |
| `support.html` | Support page (App Store Connect support URL) |

`vercel.json` turns on clean URLs, so `/privacy.html` redirects to `/privacy`.

## Before going live

Replace the support email placeholder in every page:

```bash
sed -i '' 's/\[SUPPORT EMAIL\]/you@yourdomain.com/g' *.html
```

Then commit and push. Vercel deploys `main` automatically.

## Editing

Edit the HTML directly. Keep the effective date at the top of the privacy
policy and the terms current whenever their content changes.
