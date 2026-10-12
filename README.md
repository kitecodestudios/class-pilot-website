# ClassPilot website

Public FAQ + privacy policy for App Store / Play listing URLs.

Live (after Cloudflare Pages deploy): `https://class-pilot.pages.dev/`  
Privacy: `https://class-pilot.pages.dev/privacy.html`  
(`/privacy` redirects to `/privacy.html`.)

App source: [kitecodestudios/class-pilot](https://github.com/kitecodestudios/class-pilot)

## Local preview

```bash
python3 -m http.server 8080
```

Open http://localhost:8080

## Deploy on Cloudflare Pages (free)

1. [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. Select this repo (`kitecodestudios/class-pilot-website`)
3. Settings:
   - **Project name:** `class-pilot` (so the URL is `class-pilot.pages.dev`)
   - **Production branch:** `main`
   - **Framework preset:** None
   - **Build command:** *(empty)*
   - **Build output directory:** `/` (leave as root)
4. **Save and Deploy**
5. Confirm `https://class-pilot.pages.dev/privacy.html`

Optional later: **Custom domains** → `classpilot.app`.

## Edit checklist

- [ ] Replace App Store / Google Play `href="#download"` with real store URLs in `index.html`
- [ ] Keep `privacy.html` in sync with the app’s `assets/privacy/privacy_policy.md` when that policy changes
- [ ] Optional custom domain + HTTPS
