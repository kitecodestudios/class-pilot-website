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

## Keep this site aligned with the app

This repo does not update when the app repo changes. After a product or policy change in ClassPilot, update the matching page here, then deploy Cloudflare Pages. The live site at `class-pilot.pages.dev` stays on the last deploy until then.

| App change | Update here |
| --- | --- |
| `assets/privacy/privacy_policy.md` | `privacy.html` (same facts, HTML) |
| Pricing, free tier, Family trial, offer codes, support email | `index.html` FAQ and feature list |
| Pause, breaks, fees, reminders, or other parent-facing behavior | `index.html` FAQ and Features |
| New store screenshots worth showing | `images/` and the How it looks gallery |

Store listing paste-text stays in the app at `docs/STORE_LISTING.md`. This site is the public FAQ and privacy URL.

## Edit checklist

- [ ] Replace App Store / Google Play `href="#download"` with real store URLs in `index.html`
- [ ] Optional custom domain + HTTPS
