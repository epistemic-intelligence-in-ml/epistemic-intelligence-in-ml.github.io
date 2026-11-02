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
   location, contact, venue building, street, postcode, city and map URL). Set
   `invited_speaker_slots` to the total planned invited speakers; unfilled slots
   appear as compact “To be announced” placeholders. Update the `nav:` list only if pages change.
2. **`_data/`** — refresh the content:
   - `dates.yml` — submission/review/camera-ready/workshop dates
   - `speakers.yml` — confirmed invited speakers
   - `organisers.yml` — organising committee
   - `committee.yml` — programme committee
   - `participants.yml` — confirmed participant names and affiliations only; remove test rows and duplicates before adding entries
   - `schedule.yml` — programme formats (`title` and `description`), shown on Programme
   - `timetable.yml` — tentative two-day timetable on Programme through `_includes/timetable.html`; keep unspecified sessions blank
   - `topics.yml` — topics of interest (if the scope shifts)
3. **Photos** — drop headshots into `assets/img/{speakers,organisers,committee}/`
   and set the matching `photo:` filename in the data file. Leave `photo:` blank
   for an initials placeholder.
   Speaker profiles share `_includes/confirmed-speakers.html` on the landing
   page and Invited speakers; Programme shows a compact names list.
   Portrait spaces are reserved while `photo` is blank; add
   e.g. `isabel-valera.jpg`, `ilja-kuzborskij.jpg` and `willem-waegeman.jpg` to
   `assets/img/speakers/`, then set each filename in `_data/speakers.yml`.
   `research_interests` describes each speaker's area; assign talk titles and
   timetable slots only when confirmed separately.
4. Keep `index.md` focused on the people attending: featured speakers, compact
   organiser profiles and all confirmed participants via
   `_includes/participant-preview.html`, also used on the Participants page.
   Show each entry as Name (Affiliation), without a numerical participant count.
   The primary navigation separates
   Programme (`schedule.md`), Speakers (`invited-talks.md`), Participants (`participants.md`), Travel
   (`travel.md`), About (`about.md`) and Past events. About holds the full topic
   descriptions, organiser profiles and workshop history; regional sightseeing and onward travel are
   in a disclosure on Travel. Update the date panel and current-edition history
   when changing editions. Legacy homepage anchors are preserved.
   Edit `calls-for-papers.md` if the framing changes.
   Keep `travel.md` aligned with the exact workshop building. Its D1 directions
   are based on CISPA's locations page and International Welcome Hub; CISPA's
   general directions to its main C0 building do not apply to D1.

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
*.md                     current pages (Overview, Programme, Speakers, Participants, Travel, About, plus supporting pages)
```
