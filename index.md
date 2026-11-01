---
layout: page
title: Home
permalink: /
landing: true
---

<section class="landing-hero" aria-labelledby="workshop-heading">
  <div class="hero-copy">
    <p class="section-kicker">The 3rd Workshop on Epistemic Intelligence in Machine Learning</p>
    <h1 id="workshop-heading">AI that understands<br>the limits of its<br><em>knowledge.</em></h1>
    <p class="hero-intro">How can AI systems recognise what they know, identify what they do not know, and act appropriately under uncertainty?</p>
    <div class="hero-actions">
      <a class="button button-primary" href="{{ '/schedule/' | relative_url }}">View programme <span aria-hidden="true">→</span></a>
      <a class="text-link" href="{{ '/travel/' | relative_url }}">Plan your visit <span aria-hidden="true">→</span></a>
    </div>
  </div>
  <aside class="event-panel" aria-label="Workshop at a glance">
    <div class="event-logo-wrap"><img class="event-logo" src="{{ '/assets/img/logo/' | append: site.workshop.logo | relative_url }}" alt="EIML3 Saarbrücken" width="2172" height="724"></div>
    <div class="event-details">
      <p class="event-eyebrow">December 2026</p>
      <p class="event-days"><span>02</span><span class="date-dash">—</span><span>03</span></p>
      <p class="event-weekdays">Wednesday &amp; Thursday</p>
      <div class="event-location">
        <p>{{ site.workshop.venue_city }}, near Saarbrücken</p>
        <a href="{{ '/travel/' | relative_url }}">CISPA {{ site.workshop.venue_building }}</a>
      </div>
      <p class="event-context">A pre-NeurIPS meeting</p>
    </div>
  </aside>
</section>

<section class="landing-section overview-intro" id="about" aria-labelledby="overview-about-heading">
  <h2 id="overview-about-heading">A meeting of perspectives.</h2>
  <div>
    <p>EIML3 brings together research on uncertainty, robustness, generalisation, continual learning, and reliable decision-making. We connect the foundations of uncertainty with the practical challenges of modern AI.</p>
    <div class="overview-about-links">
      <a class="text-link" id="topics" href="{{ '/about/#topics' | relative_url }}">Topics <span aria-hidden="true">→</span></a>
      <a class="text-link" id="organisers" href="{{ '/about/#organisers' | relative_url }}">Organising team <span aria-hidden="true">→</span></a>
      <a class="text-link" href="{{ '/about/#history' | relative_url }}">Workshop story <span aria-hidden="true">→</span></a>
    </div>
  </div>
</section>

<section class="overview-links" aria-label="Workshop information">
  <div class="overview-link" id="programme">
    <h2>Programme</h2>
    <p>Two days of invited talks, posters and open discussion.</p>
    <a class="text-link" id="timetable-heading" href="{{ '/schedule/' | relative_url }}">View tentative timetable <span aria-hidden="true">→</span></a>
    <a class="text-link overview-speakers-link" id="invited-speakers" href="{{ '/invited-talks/' | relative_url }}">Meet the speakers <span aria-hidden="true">→</span></a>
  </div>
  <div class="overview-link">
    <h2>Participants</h2>
    <p>Confirmed participants from across the research community.</p>
    <a class="text-link" href="{{ '/participants/' | relative_url }}">See who’s joining <span aria-hidden="true">→</span></a>
  </div>
  <div class="overview-link" id="venue">
    <h2>Venue &amp; travel</h2>
    <p>CISPA {{ site.workshop.venue_building }}<br>{{ site.workshop.venue_street }}, {{ site.workshop.venue_city }}</p>
    <a class="text-link" id="getting-here" href="{{ '/travel/' | relative_url }}">How to get to CISPA <span aria-hidden="true">→</span></a>
  </div>
</section>
