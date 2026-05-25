# Outbound-in-a-Box landing page

Single-file static HTML. No build step, no dependencies. Deploy by uploading the `site/` folder (this one) to any static host.

## Files

| File | What |
|---|---|
| `index.html` | The landing page (single file, inline CSS) |
| `sample-delivery.csv` | The 5-row sample CSV, linked from the page for public download |

## Fastest deploy: Netlify Drop (no signup, ~60 seconds)

1. Open <https://app.netlify.com/drop> in your browser.
2. Drag the **entire `site/` folder** (this one) onto the dotted-line area on the page. Drop it.
3. Netlify uploads it and assigns a random subdomain like `https://lucky-narwhal-abc123.netlify.app`.
4. Click the URL → you have a live site. Done.

Optional after deploy:
- **Claim the site** — Netlify shows a "Sign up to claim" button. Free account, gives you ability to rename the subdomain (e.g. `outbound-in-a-box.netlify.app`) and add a custom domain.
- **Custom domain** — if you want to use a subdomain like `outbound.oracleiq.info`, add a CNAME record at your DNS provider pointing to the Netlify URL.

## Alternative: Vercel

If you have the Vercel CLI installed:

```bash
cd "/Users/cadenmcclure/Documents/Money Printer/site"
vercel --prod
```

It'll ask you to sign in (browser) and pick a project name. Then deploys to `https://<project>.vercel.app`.

## Alternative: GitHub Pages

If you want it under a `oracleiq.github.io/outbound-in-a-box` URL:

1. Create a new repo on GitHub
2. Push `site/` contents to the repo root
3. Repo Settings → Pages → enable on `main` branch
4. Wait ~1 min, visit the URL

## After deploying

1. Send the URL to me — I'll update the dogfood batch drafts to reference it (replaces the bare email-only pitch with "see oracleiq.info/outbound" credibility cue).
2. Optionally point a custom domain at it. Most credible: `outbound.oracleiq.info` (subdomain you already control).

## What's deliberately NOT on the page (yet)

- Stripe Payment Links (when you set up Stripe, we add Buy buttons that go straight to checkout instead of mailto — reduces friction)
- Customer logos / testimonials (none yet — add after first 3 customers)
- Founder photo / About page (consider adding once you have a Twitter following / domain authority — fine to defer)
- Privacy policy / Terms (recommended before scaling marketing; not blocking first dollar)

## Updating the page

Edit `index.html` in any text editor. Drag-drop the updated `site/` folder onto Netlify again — it replaces the old version. No build step.
