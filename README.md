# OpenTavu — marketing site

Static single-page landing for **https://opentavu.com**. One file, no build step, no
dependencies (fast, free to host).

## Deploy (GitHub Pages)

1. Push this folder to a **public** repo under the `opentavu` org (e.g. `opentavu/site`).
2. Repo → **Settings → Pages** → Source: *Deploy from a branch* → `main` / `/ (root)`.
3. Custom domain: `opentavu.com` (the `CNAME` file already sets it). Tick **Enforce HTTPS**.
4. Point DNS (see below), then wait a few minutes for the certificate.

## DNS (edit in Hostinger's DNS panel for opentavu.com — it's currently parked)

- Apex `opentavu.com` → **A** records to GitHub Pages:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- `www` → **CNAME** → `opentavu.github.io`

GitHub shows the exact records to use in **Settings → Pages** after you add the domain —
confirm there in case the IPs change.

## Edit

Everything lives in `index.html` (inline CSS). Update copy/CTAs there; the contact CTA
points to `support@opentavu.com`. To use the logo image instead of the text wordmark,
drop a PNG in the repo and swap the `.brand` markup for an `<img>`.
