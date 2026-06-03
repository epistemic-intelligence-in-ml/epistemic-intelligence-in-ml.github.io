---
layout: page
title: Schedule
permalink: /schedule/
---

Workshop day: **{{ site.workshop.date }}**, {{ site.workshop.location }}.

_The schedule below is provisional and subject to change._

<table class="data">
  <thead>
    <tr><th>Time</th><th>Session</th></tr>
  </thead>
  <tbody>
  {% for s in site.data.schedule %}
    <tr>
      <td class="when">{{ s.time }}</td>
      <td>{{ s.item }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>
