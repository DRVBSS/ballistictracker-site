# ballistictracker.com

Marketing site for **BallisticTracker** (iOS app by Vega LLC). Plain static HTML/CSS — no build step, no dependencies. Hosted free on GitHub Pages, custom domain via Gandi.

## Files
```
index.html      Landing page
privacy.html    Privacy policy (required by the App Store)
support.html    Support / FAQ (required by the App Store)
styles.css      All styling (dark tactical theme, amber accents)
assets/         Logo, favicon, app screenshots
CNAME           Custom domain (ballistictracker.com) — do not delete
.nojekyll       Tells GitHub Pages to serve files as-is
```

## Editing
Just open the `.html` files and change the text. To preview locally, open `index.html` in a browser (or run `python3 -m http.server` in this folder and visit http://localhost:8000).

## ⚠️ Before launch: add your App Store link
The "Download on the App Store" buttons currently point to a placeholder. When your App Store listing exists (URL looks like `https://apps.apple.com/app/id123456789`), replace every occurrence of:
```
https://apps.apple.com/app/idREPLACE-ME
```
It appears in `index.html`, `privacy.html`, and `support.html`. Find/replace `REPLACE-ME` across all three.

## Deploy
GitHub Pages serves this repo automatically. Push to `main` and changes go live in ~1 minute.

DNS (at Gandi) points `ballistictracker.com` → GitHub Pages:
- **A** records (apex `@`): `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- **AAAA** records (apex `@`): `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
- **CNAME** (`www`): `<github-username>.github.io.`
