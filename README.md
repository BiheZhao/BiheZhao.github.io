# bihezhao.github.io

Personal academic website of Bihe Zhao, built with [al-folio](https://github.com/alshedivat/al-folio) v1.x (Jekyll) and served by GitHub Pages at https://bihezhao.github.io/.

## How deployment works

- Push to `main` → the **Deploy site** GitHub Action builds the site and pushes the result to the `gh-pages` branch.
- GitHub Pages is configured to serve the `gh-pages` branch (Settings → Pages → Source). Do not switch it back to `main`.
- A deploy takes about 2 minutes. Check progress under the repo's **Actions** tab.
- Nothing needs to be installed locally to publish: edit, commit, push.

## Editing content

| What | Where |
| --- | --- |
| Bio text, intro paragraph | `_pages/about.md` (body). "third-year" needs a manual bump each autumn. |
| Profile photo | `assets/img/prof_pic.jpg` — square crop, ~1200px. |
| Social icons under the photo | `_data/socials.yml` — order in the file = order on the page. |
| Publications | `_bibliography/papers.bib`. Order in the file = order on the page (within a year: first-author papers first, then most recent first). `selected = {true}` shows a paper on the home page. |
| Paper links / buttons | bib fields: `arxiv` (ID) → "arXiv" button; otherwise `html`, `pdf`, or `doi` → "Paper" button; `code` → "Code"; `bibtex_show = {true}` → "Bib". Order is fixed: Abs, arXiv/Paper, Code, Bib. |
| Paper thumbnails | put a PNG/JPG in `assets/img/publication_preview/`, add `preview = {file.png}` to the bib entry. Any aspect ratio works: images are letterboxed into a 2:1 white frame. |
| Venue badges (name, color, link) | `_data/venues.yml`. Colors are the Nature (NPG) palette; keep new venues in the same family. |
| News | one Markdown file per item in `_news/`, named `YYYY-MM-DD-slug.md`. Only month and year are shown. Paper titles go in quotes and italics: `"*Title*" was accepted at **VENUE 2027**.` |
| CV page | `_data/cv.yml` (RenderCV format). PDF at `assets/pdf/Bihe_Zhao_CV.pdf`. |
| Favicon | `assets/img/favicon.png` (256px) and `assets/img/apple-touch-icon.png` (180px). |
| Site metadata, fonts, feature flags | `_config.yml`. Requires a restart of the local preview to take effect. |

## Local preview (optional)

Requires Docker. From the repo root:

```bash
docker compose up
# open http://localhost:8080 — rebuilds on save; restart after editing _config.yml
```

If a replaced image does not update in the preview, the container has cached the old resized copies: `docker compose down` then `docker compose up` again.

## Customizations (local overrides of theme files)

These files shadow the theme's own and are the place to change look and layout. Deleting one falls back to the theme default.

| File | What it changes |
| --- | --- |
| `_layouts/about.liquid` | Home page: name not bold, Chinese name from `name_native` in `_config.yml`, photo level with the name, icons under the photo, phone layout (name centered, smaller photo), and all publication-list CSS (badge font, 2:1 thumbnails, column widths per breakpoint). |
| `_pages/publications.md` | Same publication-list CSS as above, for the Publications page. Keep the two in sync. |
| `_layouts/bib.liquid` | One publication entry: button order and labels only. Rest is the theme's. |
| `_layouts/cv.liquid` | Custom clean CV layout (sections: Education, Experience, Awards). |
| `_includes/header.liquid` | Navbar name not bold. |
| `_includes/news.liquid` | News dates as month + year. |

Badge font is Barlow Semi Condensed, loaded via the Google Fonts URL in `_config.yml` (`third_party_libraries.google_fonts`).

## Upgrading al-folio

Bump the pinned `al_*` gem versions in `Gemfile`, then run `bundle exec al-folio upgrade audit` (or check the Action log). The overrides above may need a look after a major upgrade.

## Old versions

Previous versions of the site (the original w3.css page and an intermediate plain-HTML rebuild) are archived in the private repo `BiheZhao/website-archive`. They are not deployed.
