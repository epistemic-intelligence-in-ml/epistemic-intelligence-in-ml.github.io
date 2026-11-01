---
layout: page
title: Programme
permalink: /schedule/
---

<p class="page-lead">Two days of invited talks, posters and open discussion.</p>
<p class="page-meta">{{ site.workshop.date }} · <a href="{{ '/travel/' | relative_url }}">CISPA {{ site.workshop.venue_building }}, {{ site.workshop.venue_city }}</a></p>

{% include timetable.html %}

<section class="programme-speakers" id="invited-speakers" aria-labelledby="speakers-heading">
  <div class="speakers-heading"><h2 id="speakers-heading">Confirmed invited speakers</h2><a class="text-link" href="{{ '/invited-talks/' | relative_url }}">Meet the speakers <span aria-hidden="true">→</span></a></div>
  <ul class="programme-speaker-names">
{% for speaker in site.data.speakers %}
    <li>{{ speaker.name | escape }}</li>
{% endfor %}
  </ul>
  <p class="speaker-schedule-note">Talk titles and timetable slots will be announced.</p>
</section>

<details class="programme-details">
  <summary>About the session formats</summary>
  <div class="programme-formats">
{% for session in site.data.schedule %}
    <div class="programme-format"><h3>{{ session.title }}</h3><p>{{ session.description }}</p></div>
{% endfor %}
  </div>
</details>
