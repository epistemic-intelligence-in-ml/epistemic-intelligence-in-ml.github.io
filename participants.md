---
layout: page
title: Confirmed participants
permalink: /participants/
description: "Confirmed EIML3 participants and their institutional affiliations."
---

<p class="page-lead">Researchers joining us at EIML3 on {{ site.workshop.date }}.</p>

<table class="data participants-table">
  <caption class="visually-hidden">Confirmed participants and affiliations for {{ site.workshop.date }}</caption>
  <thead>
    <tr><th scope="col">Name</th><th scope="col">Affiliation</th></tr>
  </thead>
  <tbody>
{% for participant in site.data.participants %}
    <tr>
      <th scope="row">{{ participant.name | escape }}</th>
      <td>{{ participant.affiliation | escape }}</td>
    </tr>
{% endfor %}
  </tbody>
</table>
