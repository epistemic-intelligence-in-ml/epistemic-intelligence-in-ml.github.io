---
layout: page
title: Important Dates
permalink: /important-dates/
---

All deadlines are end of day **Anywhere on Earth (AoE)** unless otherwise noted.

<table class="data">
  <thead>
    <tr><th>Date</th><th>Milestone</th></tr>
  </thead>
  <tbody>
  {% for d in site.data.dates %}
    <tr>
      <td class="when">{{ d.date }}</td>
      <td>{{ d.milestone }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>

The workshop takes place on **{{ site.workshop.date }}** in
**{{ site.workshop.location }}**, co-located with {{ site.workshop.conference }}.
