# tlnrpg.com — landing page

A single static page served by **GitHub Pages** at the apex domain `tlnrpg.com`.
It links visitors to the companion app at `https://characters.tlnrpg.com` (a
separate Vercel project).

## Update
Edit `index.html`, then:

```bash
git add index.html && git commit -m "update landing" && git push
```

GitHub Pages redeploys automatically on push to `main`.

## Hosting / DNS
- **Pages source:** branch `main`, folder `/` (root).
- **Custom domain:** `tlnrpg.com` (set via the `CNAME` file in this repo).
- **DNS (at Squarespace)** — apex `A` records to GitHub Pages + `www` CNAME:
  - `A  @  185.199.108.153`
  - `A  @  185.199.109.153`
  - `A  @  185.199.110.153`
  - `A  @  185.199.111.153`
  - `CNAME  www  keldren.github.io`
- `.nojekyll` disables Jekyll processing (serve files as-is).

Unrelated to this repo: `characters.tlnrpg.com` → Vercel (the app), and Resend
email records — both live alongside these in Squarespace DNS.
