# EIML Workshop Website

Jekyll source for the EIML workshop site, served via GitHub Pages at
<https://eiml.cc>. The repository is
<https://github.com/epistemic-intelligence-in-ml/epistemic-intelligence-in-ml.github.io>.
Keep `CNAME` and the deployment URL in `_config.yml` aligned with the custom domain.

## Run it locally

```bash
bundle install          # first time only
bundle exec jekyll serve # then open http://localhost:4000
```

`jekyll serve` live-reloads as you edit. Changes to `_config.yml` need a restart.

## Rolling over to a new year

First preserve the outgoing edition in the archive (see below), then update the
current edition. Use edition numbers rather than years as identifiers: EIML 2
and EIML 3 are both listed in the 2026 series calendar.

The site is data-driven, so a new edition is mostly editing config + data — not
templates. Each year:

1. **`_config.yml`** — update the `workshop:` block (edition, year, dates,
   location, contact). Update the `nav:` list only if pages change.
2. **`_data/`** — refresh the content:
   - `dates.yml` — submission/review/camera-ready/workshop dates
   - `speakers.yml` — confirmed invited speakers
   - `organisers.yml` — organising committee
   - `committee.yml` — programme committee
   - `schedule.yml` — programme formats (`title` and `description`), shown on Home and Programme
   - `timetable.yml` — tentative two-day timetable, shared by Home and Programme through `_includes/timetable.html`; keep unspecified sessions blank
   - `topics.yml` — topics of interest (if the scope shifts)
3. **Photos** — drop headshots into `assets/img/{speakers,organisers,committee}/`
   and set the matching `photo:` filename in the data file. Leave `photo:` blank
   for an initials placeholder.
4. Edit the prose on `index.md` / `calls-for-papers.md` if the framing changes.
   The landing page also contains the date-panel typography, travel details,
   and series timeline; update these when changing editions.

Tip: consider tagging each year (`git tag 2026`) before rolling over, so past
editions stay recoverable.

## Past events

The **Past events** navigation tab opens `/archive/`, which links to permanent
edition pages at `/archive/eiml1/`, `/archive/eiml2/`, and future edition paths.
Historical content lives in `_data/editions/`, independently of the current
workshop's `_config.yml` and top-level `_data/` files. Archive pages share the
site styling but have their own identity, metadata, and navigation.

To preserve another edition:

1. Add `_data/editions/eimlN.yml`, following an existing edition's schema. Set
   `slug`, numeric `number`, ordinal `edition`, and the edition's own dates,
   venue, people, programme, and source links. Keep historical affiliations.
2. Add `archive/eimlN/index.html` with `layout: edition`, `archive: true`,
   `edition: eimlN`, a title/description, and `permalink: /archive/eimlN/`.
3. Store any archived images in `assets/img/archive/eimlN/`. Use root-relative
   image paths in the edition data and record original image URLs in
   `photo_sources`. These local copies survive changes to the source website.
4. Record the retrieval date in `retrieved_on`; use `archive_notes` and
   `schedule_note` for conflicting or provisional source information. Optional
   sections are omitted when their lists are empty. Accepted papers can use
   `accepted_papers` (with presentation groups) or `poster_sessions`.
5. Run `bundle exec jekyll build` and inspect the landing page, new edition page,
   internal links, and mobile navigation. This repository currently tracks
   `_site/`, so include the regenerated output with source changes.

The archive landing page and archive navigation discover edition data automatically.
Do not change archived dates, affiliations, or content when rolling the current
site forward; make source-backed corrections directly to the relevant edition.

## Structure

```
_config.yml              site + per-year settings
_data/                   all year-specific content (YAML)
_data/editions/          independent records of past workshop editions
archive/                Past events landing page and permanent edition pages
_layouts/                default + page templates
_includes/               header, footer, reusable person card
assets/css/style.css     theme (colours in :root at the top)
assets/css/landing.css   current-edition theme and responsive landing page
assets/img/              logos, headshots, and credited venue photography
*.md                     the five pages (Home, Invited Talks, CfP, Dates, Programme)
```
