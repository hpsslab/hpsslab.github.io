# HPSS Lab website

Jekyll source for the High Performance Systems and Software Lab at Colorado School of Mines. GitHub Pages serves the site at <https://hpss.mines.edu/>. The `CNAME` file retains that domain.

## Local preview

```sh
bundle install
bundle exec jekyll serve
```

Open the local address printed by Jekyll. To build without serving:

```sh
bundle exec jekyll build
```

The build writes to `_site/`, which Git ignores. Generated files and local dependencies should not be committed.

## Content

- `_pages/*.html`: primary pages, written as HTML with Liquid templates.
- `_data/research.yml`: topic explanations, methods, figures, captions, and supporting project links. AI Acceleration appears first. Topics with `home: true` appear in the homepage research overview.
- `_data/publist.yml`: publications, including year, research area, authors, venue, and paper links. Keep entries ordered by year, newest first.
- `_data/publication_areas.yml`: publication group order and navigation labels. Each publication's `area` matches a group `id`.
- `_data/phd_members.yml`, `_data/master_members.yml`, `_data/bachelor_members.yml`: current students.
- `_data/alumni_members.yml`: former students. Leave unknown completion dates and destinations unspecified.
- `_data/news.yml`: news, newest first. Headlines support Markdown links.
- `_data/software.yml`: software repositories. The public page shows research implementations and tools.
- `_includes/`: shared navigation, footer, publication entries, and people entries.
- `css/main.scss`: styles. It uses system fonts and has no Bootstrap dependency.
- `js/site.js`: mobile navigation. Publications are grouped by topic and remain available without JavaScript.

Set the public research interest form URL in `_config.yml`. Add portraits under `images/teampic/` and set each person's `photo` filename in the corresponding data file. A missing portrait uses initials.

The former `/vacancies.html` address redirects to `/vacancies/`. CoRtEx and the SMILE demos are separate project sites linked by their full public URLs. This repository does not replace their sources.

The original template's example picture gallery, lecture calendar, and template instructions remain in the repository but are excluded from the build.

See [content sources](docs/content-sources.md) for the November 2026 refresh and unresolved source links.

## Review

Build the site, then check the main pages at desktop and narrow mobile widths. Check the menu and publication topic links. Confirm that internal anchors resolve, portraits load, and student status changes appear in the correct group.

The original site used the Allan Lab Jekyll template. Existing license and attribution files remain in the repository.
