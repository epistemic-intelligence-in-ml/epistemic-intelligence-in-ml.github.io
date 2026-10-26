---
layout: page
title: Programme
permalink: /schedule/
---

The workshop takes place over two days, **{{ site.workshop.date }}**, at
**{{ site.workshop.venue }}** in **{{ site.workshop.location }}**.

The programme will bring together invited talks, discussions, and a poster
session, with time to exchange ideas across the foundations and applications of
uncertainty in AI.

{% for session in site.data.schedule %}
<div class="topic">
  <h2>{{ session.title }}</h2>
  <p>{{ session.description }}</p>
</div>
{% endfor %}

{% include timetable.html %}
