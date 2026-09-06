# bihezhao.github.io

Personal academic website of Bihe Zhao, built with [al-folio](https://github.com/alshedivat/al-folio) v1.x and deployed to GitHub Pages by the `Deploy site` GitHub Action on every push to `main`.

## Editing

| What                   | Where                                   |
| ---------------------- | --------------------------------------- |
| Bio, address, photo    | `_pages/about.md`, `assets/img/prof_pic.jpg` |
| Publications           | `_bibliography/papers.bib` (`selected = {true}` shows a paper on the home page; `preview = {file.png}` adds a thumbnail from `assets/img/publication_preview/`) |
| Venue badges           | `_data/venues.yml`                      |
| News                   | one Markdown file per item in `_news/`  |
| CV page                | `_data/cv.yml`; PDF at `assets/pdf/Bihe_Zhao_CV.pdf` |
| Social links           | `_data/socials.yml`                     |
| Site settings          | `_config.yml` (`name_native` is the Chinese name shown after your name) |
| Layout overrides       | `_layouts/about.liquid`, `_layouts/cv.liquid`, `_includes/header.liquid`, `_includes/news.liquid` shadow the theme's files; delete one to fall back to the theme default |

## Uploading your own files

- Profile photo: replace `assets/img/prof_pic.jpg` (a roughly square crop looks best).
- CV PDF: replace `assets/pdf/Bihe_Zhao_CV.pdf`, or change `cv_pdf` in `_pages/cv.md` and `_data/socials.yml`.
- Paper thumbnails: put a PNG or JPG in `assets/img/publication_preview/` and add `preview = {filename.png}` to that paper's entry in `_bibliography/papers.bib`. Wide images (about 2:1) fit the column best.

## Local preview

```bash
docker compose up
# then open http://localhost:8080
```

## Upgrading al-folio

Bump the pinned `al_*` gem versions in `Gemfile` and run `bundle exec al-folio upgrade audit`. See the al-folio docs for details.
