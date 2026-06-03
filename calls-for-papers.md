---
layout: page
title: Calls for Papers
permalink: /calls-for-papers/
---

Epistemic Intelligence in Machine Learning (EIML) studies how learning systems
recognise, represent, reason about, and act under the limits of their knowledge.
Modern ML systems — including foundation models, generative models, autonomous
agents, and AI-enabled engineering systems — are increasingly deployed in
open-ended environments where failures are often epistemic: hallucination,
unsafe extrapolation, brittle behaviour under distribution shift, catastrophic
forgetting, overconfident decisions, and poor communication of uncertainty all
arise when a system cannot distinguish what is known from what is unknown.

Building on the first EIML workshop at EurIPS 2025 and the second at ICML 2026,
this third edition at {{ site.workshop.conference }} turns to the field's
*foundations*. The aim is not to repeat a broad uncertainty workshop, but to
clarify the conceptual, mathematical, statistical, computational, engineering,
and philosophical bases on which the field should develop. The relevant
communities remain fragmented — statistics, mathematics and computer science,
engineering, and philosophy address overlapping problems in often incompatible
languages — and without a dedicated foundational forum, EIML risks becoming a
collection of parallel literatures rather than a coherent research programme.

We seek contributions from researchers across machine learning, statistics,
philosophy of science, decision theory, and related disciplines. We welcome
works-in-progress and mature research alike, and especially submissions that
challenge prevailing assumptions, propose novel benchmarks, or provide insight
into the philosophical and foundational dimensions of uncertainty in AI.

## Topics

To this end, topics to be covered include, but are not limited to:

{% for topic in site.data.topics %}
<div class="topic">
  <h3>{{ topic.title }}</h3>
  {% if topic.description and topic.description != "" %}
  <p>{{ topic.description }}</p>
  {% endif %}
  {% if topic.points and topic.points.size > 0 %}
  <ul>
    {% for point in topic.points %}
    <li>{{ point }}</li>
    {% endfor %}
  </ul>
  {% endif %}
</div>
{% endfor %}

## Reviewing Policy for Authors

Given the strong interest in EIML and the expected number of submissions, we
warmly encourage authors to also participate in the reviewing process. In
particular, we kindly ask that at least one author per submission be willing to
serve as a reviewer.

This community-driven approach helps us ensure a fair, timely, and high-quality
review process, while also fostering a more engaged and collaborative research
community. Reviews will, of course, be assigned based on your expertise.

We sincerely appreciate your support in helping make
{{ site.workshop.short_name }} a success.

## Key Dates

<table class="data">
  <tbody>
  {% for d in site.data.dates %}
    <tr>
      <td class="when">{{ d.date }}</td>
      <td>{{ d.milestone }}</td>
    </tr>
  {% endfor %}
  </tbody>
</table>

For submission questions, contact
[{{ site.workshop.contact_email }}](mailto:{{ site.workshop.contact_email }}).
