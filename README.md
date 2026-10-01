# EntrePro Corporation

Website for EntrePro Corporation, the data strategy, architecture, and
leadership consultancy of Dr. Farid Mehovic (fractional CDO, data warehousing,
database performance, data migration, executive analytics).

## Structure

- `index.html` — home (hero, expertise, approach, results, experience
  timeline, clients & employers, research & patents, about)
- `services.html` — fourteen services in four groups, plus engagement models
- `projects.html` — twenty projects with category filters
- `publications.html` — three patents and 21 publications grouped by decade
- `academic.html` — degrees, research history, teaching, invited talks, honors
- `assets/photos/` — hero photographs (see below)
- `marketing/linkedin/` — LinkedIn Company Page kit: copy for every field, logo and banner images, launch posts
- `styles.css` — styles, responsive down to phone width
- `script.js` — mobile menu, footer year, project filters
- `assets/favicon.svg` — site icon

It's plain static HTML/CSS/JS with no build step. Open `index.html` in a browser
to preview, or host it on any static host (GitHub Pages, Netlify, Cloudflare Pages).

## Photos

Hero photographs live in `assets/photos/`. All five are CC0 / public domain,
found through Openverse and sourced from StockSnap; `assets/photos/CREDITS.md`
records the title, photographer, and source page for each. To swap one, replace
the file with a landscape JPEG of at least 1200 px width and keep the filename.

## Hosting on entrepro.biz (GitHub Pages)

The site deploys automatically through GitHub Actions
(`.github/workflows/pages.yml`) on every push to the repository's default
branch. Pages is enabled with source "GitHub Actions" and custom domain
`entrepro.biz` under **Settings → Pages**.

DNS, in Wix under **Domains → entrepro.biz → Manage DNS Records**:

- **A** records for host `@` pointing to `185.199.108.153`,
  `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
  (remove any other A records on `@`)
- **CNAME** for host `www` pointing to `faridmehovicai.github.io`

Once DNS has propagated, tick **Enforce HTTPS** under Settings → Pages.

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

