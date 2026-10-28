# EntrePro Corporation website — context for Claude

This repository is the public website of EntrePro Corporation, the consulting
practice of Dr. Farid Mehovic (La Jolla, California). It is live at
https://entrepro.biz. Read this file first; it records decisions the owner has
already made so they are not re-litigated.

## How the site is built and deployed

- Plain static HTML/CSS/JS, no build step. Pages: `index.html`, `services.html`,
  `projects.html`, `publications.html`, `academic.html`. Shared `styles.css`
  and `script.js`. Photos in `assets/photos/` (all CC0; see `CREDITS.md` there).
- Deploys automatically via GitHub Actions (`.github/workflows/pages.yml`) on
  every push to `main`, which is the default branch. Work on `main`.
  Other branches are leftovers and can be ignored.
- Custom domain `entrepro.biz` is set in GitHub Pages; HTTPS is enforced.
  DNS lives at Wix (A records to GitHub Pages, `www` CNAME to
  `faridmehovicai.github.io`). Email `info@entrepro.biz` forwards to the
  owner's Gmail via ImprovMX.
- To preview changes, open the HTML files in a browser or screenshot with
  Playwright (Chromium is pre-installed in cloud sessions).

## Decisions the owner has made (keep these)

- **No inbound solicitation.** The owner works full-time elsewhere. There is
  no contact form, no "book a call" or "get in touch" buttons, no
  call-to-action bands. The company email appears only in the footer as plain
  company information. The Services page states that EntrePro paused new
  engagements in February 2026 and is not taking on work.
- **Tone:** portfolio and credentials, not sales. Content is drawn from the
  owner's resume, project history, and publications (originally in the
  owner's Google Drive).
- **Location:** La Jolla, California (not Austin; Austin was a corporate
  filing address only).
- **Data Context:** a former research initiative the owner has disbanded. Do
  not describe it as current. Talk titles that contain the words "Data
  Context" remain in the publications list as historical record.
- **Photos:** light, inspiring, real photographs (nature, consulting
  situations). No dark abstract backgrounds. Must be fee-free (CC0 / public
  domain); Openverse (api.openverse.org) with `license=cc0,pdm` is the source
  that works from cloud sessions.
- **Privacy:** never publish the owner's personal phone number, home address,
  or personal Gmail address on the site.
- The owner's portrait is in `assets/photos/farid-mehovic.jpg`, used in the
  About section.

## Related material

- `marketing/linkedin/` — the LinkedIn Company Page kit (copy, logo, banner,
  optional posts). The page exists at linkedin.com/company/entrepro-corporation.
- `README.md` — hosting, DNS, and email setup details.

## Working with the owner

The owner is not a developer. Explain in plain terms, one step at a time,
and say exactly where to click. Avoid jargon such as "branch", "merge", or
"PR" unless necessary; when a change is pushed to `main`, it is live within
about a minute, and that is all they need to know.
