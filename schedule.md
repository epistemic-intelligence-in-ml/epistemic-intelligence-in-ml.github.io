---
layout: page
title: Programme
permalink: /schedule/
---

The workshop takes place over two days, **{{ site.workshop.date }}**, at
**{{ site.workshop.venue }}**, **{{ site.workshop.venue_building }}**, in **{{ site.workshop.location }}**.
See [how to get to CISPA]({{ '/travel/' | relative_url }}) for the address and travel directions.

{% include timetable.html %}

<section class="programme-speakers" id="invited-speakers" aria-labelledby="speakers-heading">
  <div class="speakers-heading"><h2 id="speakers-heading">Confirmed invited speakers</h2><a class="text-link" href="{{ '/invited-talks/' | relative_url }}">View speaker page <span aria-hidden="true">→</span></a></div>
{% include confirmed-speakers.html heading_level=3 %}
</section>

<details class="programme-details">
  <summary>About the session formats</summary>
  <div class="programme-formats">
{% for session in site.data.schedule %}
    <div class="programme-format"><h3>{{ session.title }}</h3><p>{{ session.description }}</p></div>
{% endfor %}
  </div>
</details>
