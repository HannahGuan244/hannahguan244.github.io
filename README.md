# hannahguan244.github.io

Personal academic site built with [al-folio](https://github.com/alshedivat/al-folio) v1.
Layouts, styles and scripts come from the `al_folio_*` gems; this repo holds content and config.

## Where things live

| What                                    | File                                       |
| --------------------------------------- | ------------------------------------------ |
| Bio, teaching, awards                   | `_pages/about.md`                          |
| Publications (+ "selected" on About)    | `_bibliography/papers.bib`                 |
| Publication thumbnails                  | `assets/img/publication_preview/`          |
| News items                              | `_news/`                                   |
| Social links                            | `_data/socials.yml`                        |
| CV                                      | `assets/cv.pdf`, `_pages/cv.md`            |
| Site settings                           | `_config.yml`                              |

`_layouts/about.liquid` is a local copy of al_folio_core's About layout, changed so that
content after `<!-- below-publications -->` in `about.md` renders below the selected publications.

Site-specific CSS goes in `_sass/_custom.scss`, imported by a local copy of al_folio_core's
`assets/css/main.scss` (the only change there is the final `@use "custom";`).

## Local development

```bash
bundle install
bundle exec jekyll serve --livereload
```

Then open `http://localhost:4000`.

## Deployment

Pushing to `main` runs `.github/workflows/deploy.yml`, which builds the site and pushes `_site`
to the `gh-pages` branch. GitHub Pages must be set to serve from the `gh-pages` branch
(Settings → Pages → Build and deployment → Deploy from a branch → `gh-pages` / root).
