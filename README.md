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

## Email: info@entrepro.biz → Gmail

The site lists `info@entrepro.biz`. To forward it to your Gmail for free, use
[ImprovMX](https://improvmx.com):

1. Sign up at improvmx.com with `entrepro.biz` and set the alias
   `info` → your Gmail address.
2. In Wix **Manage DNS Records**, add:
   - **MX** `@` → `mx1.improvmx.com` (priority 10)
   - **MX** `@` → `mx2.improvmx.com` (priority 20)
   - **TXT** `@` → `v=spf1 include:spf.improvmx.com ~all`
   (remove any other MX records on `@`)
3. Optional: to reply *as* info@entrepro.biz from Gmail, add it under
   Gmail **Settings → Accounts → Send mail as** using ImprovMX's SMTP details.

The contact form posts to [FormSubmit](https://formsubmit.co), which emails each
submission to `info@entrepro.biz`. The very first submission sends a one-time
activation email to that address; click the link in it to turn the form on.
