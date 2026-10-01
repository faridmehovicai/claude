# EntrePro Corporation

Website for EntrePro Corporation, a business consulting firm that helps founders
and growing businesses with strategy, operations, finance, and leadership.

## Structure

- `index.html` — single-page site (hero, services, approach, about, contact)
- `styles.css` — styles, responsive down to phone width
- `script.js` — mobile menu and footer year
- `assets/favicon.svg` — site icon

It's plain static HTML/CSS/JS with no build step. Open `index.html` in a browser
to preview, or host it on any static host (GitHub Pages, Netlify, Cloudflare Pages).

## Hosting on entrepro.biz (GitHub Pages)

The `CNAME` file tells GitHub Pages to serve the site at `entrepro.biz`.

1. In the GitHub repo, go to **Settings → Pages**, set the source to
   **Deploy from a branch**, and pick the branch holding this site (root folder).
2. In Wix, open **Domains → entrepro.biz → Manage DNS Records** and set:
   - **A** records for `entrepro.biz` (host `@`) pointing to
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
     (remove any other A records on `@`)
   - **CNAME** for `www` pointing to `faridmehovicai.github.io`
3. Once DNS has updated (minutes to a few hours), go back to **Settings → Pages**
   and tick **Enforce HTTPS**.

## Before going live

- Replace the placeholder email and phone in the Contact section of `index.html`.
- The contact form uses `mailto:`; point its `action` at a form service
  (e.g. Formspree) to receive submissions directly.
- Review the service descriptions so they match what you offer.
