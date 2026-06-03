---
layout: page
title: Home
permalink: /
---

<div class="hero">
  {% if site.workshop.logo and site.workshop.logo != "" %}
  <img class="hero-logo" src="{{ '/assets/img/logo/' | append: site.workshop.logo | relative_url }}" alt="{{ site.workshop.short_name }} logo">
  {% endif %}
  <p class="eyebrow">{{ site.workshop.date }} · {{ site.workshop.location }}</p>
  <p class="eyebrow">{{ site.workshop.short_name }}</p>
  <h1>{{ site.workshop.full_name }}</h1>
  <p class="subtitle">{{ site.workshop.subtitle }}</p>
  {% if site.workshop.conference_logo and site.workshop.conference_logo != "" %}
  <img class="hero-conf-logo" src="{{ '/assets/img/logo/' | append: site.workshop.conference_logo | relative_url }}" alt="{{ site.workshop.conference }} logo">
  {% endif %}
</div>

EIML@EurIPS 2025 and EIML2@ICML2026 marked the beginning of a growing community that cares about Epistemic Intelligence
in Machine Learning.
The conversation continues at EIML3@NeurIPS2026.

## Why are we doing this?

Epistemic Intelligence in Machine Learning (EIML) studies how learning systems recognise, represent, reason about, and
act under the limits of their knowledge. Modern ML systems---including foundation models, generative models, autonomous
agents, and AI-enabled engineering systems---are increasingly deployed in open-ended environments where failures are
often epistemic: hallucination, unsafe extrapolation, brittle behaviour under distribution shift, catastrophic
forgetting, overconfident decisions, and poor communication of uncertainty all arise when a system cannot distinguish
what is known from what is unknown.

The first EIML workshop, held at EurIPS 2025, established the theme of epistemic intelligence around epistemic
uncertainty in machine learning. The second edition, accepted at ICML 2026, broadened the agenda toward unknown
unknowns, robustness, safety, alignment, foundation models, and real-world impact. The proposed NeurIPS 2026 workshop is
the natural third step in the series: after establishing the community and broadening its application scope, this
edition asks what must be in place for EIML to become a principled field. By foundations, we mean five coupled layers:
conceptual foundations that define knowledge, ignorance, epistemic uncertainty, and epistemic agency; representational
foundations that specify mathematical objects for partial knowledge; inferential foundations that determine which
guarantees survive misspecification, weak prior information, partial identification, and distribution shift;
computational foundations that characterise the tractability of epistemic reasoning at ML scale; and engineering
foundations that govern how epistemic signals are communicated and acted upon in deployed systems.

Why now? There is growing momentum around uncertainty-aware, reliable, and safe ML, but the relevant communities remain
fragmented. Statistics studies Bayesian, frequentist, conformal, second-order, and imprecise probabilistic accounts of
uncertainty. Mathematics and computer science provide formalisms for learning theory, optimisation, representation,
computation, and complexity. Engineering studies how epistemic signals behave under communication, networking, robotics,
and deployment constraints. Philosophy analyses knowledge, ignorance, rational belief, explanation, agency, and
responsibility. These fields address overlapping problems but often use incompatible languages. Without a dedicated
foundational forum, EIML risks becoming a collection of parallel literatures rather than a coherent research programme.
NeurIPS is the ideal venue to crystallise shared problems, explicitly contrast frameworks, and coordinate the next phase
of the field.

## Topics

<p class="topic-hint">Click a topic to see the key questions it raises.</p>

<div class="topic-accordion">
  {% for topic in site.data.topics %}
  <details class="topic-item">
    <summary>{{ topic.title }}</summary>
    <div class="topic-content">
      {% if topic.description and topic.description != "" %}<p>{{ topic.description }}</p>{% endif %}
      {% if topic.points and topic.points.size > 0 %}
      <ul>{% for point in topic.points %}<li>{{ point }}</li>{% endfor %}</ul>
      {% endif %}
    </div>
  </details>
  {% endfor %}
</div>

## Important Dates

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

[//]: # (For full details see [Calls for Papers]&#40;{{ '/calls-for-papers/' | relative_url }}&#41;,)

[//]: # ([Important Dates]&#40;{{ '/important-dates/' | relative_url }}&#41;, and)

[//]: # ([Schedule]&#40;{{ '/schedule/' | relative_url }}&#41;.)

## Confirmed Speakers

<div class="speakers">
  {% for s in site.data.speakers %}
    {% include speaker-card.html speaker=s %}
  {% endfor %}
</div>

## Organising Committee

<div class="people">
  {% for p in site.data.organisers %}
    {% include person-card.html person=p folder="organisers" %}
  {% endfor %}
</div>

## Programme Committee

{% include person-list.html people=site.data.committee %}

If you have any queries, feel free to write to
[{{ site.workshop.contact_email }}](mailto:{{ site.workshop.contact_email }}).
