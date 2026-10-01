# EntrePro Corporation

Website for EntrePro Corporation, the data strategy, architecture, and
leadership consultancy of Dr. Farid Mehovic (fractional CDO, data warehousing,
database performance, data migration, executive analytics).

## Structure

- `index.html` — home (hero, expertise, approach, results, experience
  timeline, clients & employers, research & patents, about, contact)
- `services.html` — fourteen services in four groups, plus engagement models
- `projects.html` — twenty projects with category filters
- `publications.html` — three patents and 21 publications grouped by decade
- `academic.html` — degrees, research history, teaching, invited talks, honors
- `assets/photos/` — hero photographs (see below)
- `styles.css` — styles, responsive down to phone width
- `script.js` — mobile menu, footer year, project filters
- `assets/favicon.svg` — site icon

It's plain static HTML/CSS/JS with no build step. Open `index.html` in a browser
to preview, or host it on any static host (GitHub Pages, Netlify, Cloudflare Pages).

## Photos

Each page has a photo slot in its hero. Drop these five files into
`assets/photos/` (JPEG, landscape, at least 1600 px wide, under ~400 KB each):

| File | Page | Suggested subject |
|---|---|---|
| `home.jpg` | Home | sunrise over mountains, a road toward the horizon, a city skyline at dawn |
| `services.jpg` | Services | people working at a whiteboard or around a table |
| `projects.jpg` | Projects | a bridge, a dam, or other large engineered structure |
| `publications.jpg` | Publications | a library or reading room |
| `academic.jpg` | Academic | a university campus or lecture hall |

Unsplash, Pexels, and Pixabay all offer photos free for commercial use with
no attribution required. Until a file is present, the slot shows a soft
gradient panel.

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
