# Notes for AI assistants working on this repo

Read `README.md` first — it documents where every piece of content lives, how deployment works, and which theme files are locally overridden.

Conventions the owner has asked for:

- Name is never bold; the Chinese name (赵璧和) follows it in smaller type.
- Navigation and section titles are capitalized (About, Publications, News, CV, Selected Publications).
- News items show month and year only; paper titles in news are quoted and italic.
- Publication buttons in this order: Abs, arXiv (or "Paper" when no arXiv ID), Code, Bib.
- Publications sorted by year, then first-author papers first, then most recent first — this is the order in `_bibliography/papers.bib`.
- Venue badge colors come from the Nature (NPG) palette in `_data/venues.yml`; every venue must have a distinct color.
- Thumbnails are letterboxed into a 2:1 white frame via CSS; do not crop images.
- Footer shows only the copyright line.
- No postal address on the site.
- Supervisors and advisors are written with "Prof.".

Publication-list CSS is duplicated in `_layouts/about.liquid` and `_pages/publications.md`; change both.
`_config.yml` edits need a restart of the local Docker preview. The deploy is GitHub Actions → `gh-pages`; Pages must keep serving `gh-pages`.
