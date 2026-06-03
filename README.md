# EIML Workshop Website

Jekyll source for the EIML workshop site, served via GitHub Pages at
<https://eiml.github.io>.

## Run it locally

```bash
bundle install          # first time only
bundle exec jekyll serve # then open http://localhost:4000
```

`jekyll serve` live-reloads as you edit. Changes to `_config.yml` need a restart.

## Rolling over to a new year

The site is data-driven, so a new edition is mostly editing config + data — not
templates. Each year:

1. **`_config.yml`** — update the `workshop:` block (edition, year, dates,
   location, contact). Update the `nav:` list only if pages change.
2. **`_data/`** — refresh the content:
   - `dates.yml` — submission/review/camera-ready/workshop dates
   - `speakers.yml` — confirmed invited speakers
   - `organisers.yml` — organising committee
   - `committee.yml` — programme committee
   - `schedule.yml` — workshop-day programme
   - `topics.yml` — topics of interest (if the scope shifts)
3. **Photos** — drop headshots into `assets/img/{speakers,organisers,committee}/`
   and set the matching `photo:` filename in the data file. Leave `photo:` blank
   for a placeholder circle.
4. Edit the prose on `index.md` / `calls-for-papers.md` if the framing changes.

Tip: consider tagging each year (`git tag 2026`) before rolling over, so past
editions stay recoverable.

## Structure

```
_config.yml              site + per-year settings
_data/                   all year-specific content (YAML)
_layouts/                default + page templates
_includes/               header, footer, reusable person card
assets/css/style.css     theme (colours in :root at the top)
assets/img/              headshots
*.md                     the five pages (Home, Invited Talks, CfP, Dates, Schedule)
```
