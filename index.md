---
layout: page
title: Home
permalink: /
landing: true
---

<section class="landing-hero" aria-labelledby="workshop-heading">
  <div class="hero-copy">
    <p class="section-kicker">The 3rd Workshop on Epistemic Intelligence in Machine Learning</p>
    <p class="hero-when">{{ site.workshop.date }} · CISPA, Saarbrücken</p>
    <h1 id="workshop-heading">AI that understands<br>the limits of its<br><em>knowledge.</em></h1>
    <p class="hero-intro">How can AI systems recognise what they know, identify what they do not know, and act appropriately under uncertainty?</p>
    <p class="hero-description">EIML3 brings together research on uncertainty, robustness, generalisation, continual learning, and reliable decision-making to explore this question.</p>
    <div class="hero-actions">
      <a class="button button-primary" href="#about">Explore the workshop <span aria-hidden="true">↗</span></a>
      <a class="text-link" href="#venue">Plan your visit <span aria-hidden="true">→</span></a>
    </div>
  </div>
  <aside class="event-panel" aria-label="Workshop at a glance">
    <div class="event-logo-wrap"><img class="event-logo" src="{{ '/assets/img/logo/' | append: site.workshop.logo | relative_url }}" alt="EIML3 Saarbrücken" width="2172" height="724"></div>
    <div class="event-details">
      <p class="event-eyebrow">December 2026</p>
      <p class="event-days"><span>02</span><span class="date-dash">—</span><span>03</span></p>
      <p class="event-weekdays">Wednesday &amp; Thursday</p>
      <div class="event-location">
        <p>Saarbrücken, Germany</p>
        <a href="#venue">{{ site.workshop.venue }}</a>
      </div>
      <p class="event-context">A pre-NeurIPS meeting</p>
      <a class="event-travel" href="#getting-here">Paris ↔ Saarbrücken <span>About 2 hours by direct train <span aria-hidden="true">↗</span></span></a>
    </div>
  </aside>
</section>

<section class="landing-section invited-speakers-section" id="invited-speakers" aria-labelledby="invited-speakers-heading">
  <div class="section-heading"><h2 id="invited-speakers-heading">Invited speakers</h2></div>
  <p class="speakers-status">To be announced.</p>
</section>

<section class="landing-section about-section" id="about" aria-labelledby="about-heading">
  <div class="section-heading">
    <p class="section-kicker">The idea</p>
    <h2 id="about-heading">Better AI begins with<br>knowing its limits.</h2>
  </div>
  <div class="section-prose">
    <p>AI systems increasingly make predictions and decisions in situations where their knowledge is incomplete. Recognising these limits is essential to knowing when to rely on a prediction, seek more information, or reconsider a decision.</p>
    <p>This ability to understand and reason about the limits of one's knowledge is what we call <strong>epistemic intelligence</strong>. The workshop connects philosophical, mathematical, and statistical foundations with the practical challenges of building AI that can learn and act reliably under uncertainty.</p>
  </div>
</section>

<section class="landing-section history-section" aria-labelledby="history-heading">
  <div class="section-heading"><p class="section-kicker">The EIML story</p><h2 id="history-heading">A growing conversation.</h2></div>
  <div class="section-prose"><p>EIML began at EurIPS 2025 in Copenhagen, bringing together researchers interested in how machine learning can recognise and respond to gaps in its knowledge. The second edition, at ICML 2026 in Seoul, expanded the conversation to generative AI, robustness, safety, and continual learning. EIML3 continues this journey in Saarbrücken, connecting the foundations of imprecision and uncertainty with the needs of modern AI.</p></div>
  <ol class="edition-trail">
    <li><a href="{{ '/archive/eiml1/' | relative_url }}"><span class="edition-year">2025 · Copenhagen</span><strong>EIML1 @ EurIPS</strong><span>Where the conversation began <span aria-hidden="true">↗</span></span></a></li>
    <li><a href="{{ '/archive/eiml2/' | relative_url }}"><span class="edition-year">2026 · Seoul</span><strong>EIML2 @ ICML</strong><span>Broadening the perspective <span aria-hidden="true">↗</span></span></a></li>
    <li class="edition-current"><span class="edition-year">2026 · Saarbrücken</span><strong>EIML3 @ Saarbrücken</strong><span>The conversation continues</span></li>
  </ol>
</section>

<section class="landing-section topics-section" id="topics" aria-labelledby="topics-heading">
  <div class="section-heading section-heading-wide">
    <div><p class="section-kicker">Topics</p><h2 id="topics-heading">Three perspectives.<br>One shared question.</h2></div>
    <p>What does it take for AI to reason well when its knowledge is incomplete?</p>
  </div>
  <div class="landing-topics">
{% for topic in site.data.topics %}
    <details class="landing-topic"{% if forloop.first %} open{% endif %}>
      <summary><span class="topic-number" aria-hidden="true">0{{ forloop.index }}</span><h3>{{ topic.title }}</h3><span class="topic-toggle" aria-hidden="true"></span></summary>
      <div class="landing-topic-body">
        <p>{{ topic.description }}</p>
        <ul>{% for point in topic.points %}<li>{{ point }}</li>{% endfor %}</ul>
      </div>
    </details>
{% endfor %}
  </div>
</section>

<section class="landing-section programme-section" id="programme" aria-labelledby="programme-heading">
  <div class="section-heading section-heading-wide">
    <div><p class="section-kicker">Programme · {{ site.workshop.date }}</p><h2 id="programme-heading">Two days to exchange ideas.</h2></div>
    <p>Invited talks, discussions, and a poster session, with time to connect across disciplines.</p>
  </div>
  <div class="programme-formats">
{% for session in site.data.schedule %}
    <div class="programme-format"><span class="format-number" aria-hidden="true">0{{ forloop.index }}</span><h3>{{ session.title }}</h3><p>{{ session.description }}</p></div>
{% endfor %}
  </div>
  <div class="programme-note"><p>The detailed two-day schedule will be announced here.</p><a class="text-link" href="{{ '/invited-talks/' | relative_url }}">Invited speakers <span aria-hidden="true">↗</span></a></div>
</section>

<section class="landing-section organisers-section" id="organisers" aria-labelledby="organisers-heading">
  <div class="section-heading section-heading-wide"><div><p class="section-kicker">The people behind EIML3</p><h2 id="organisers-heading">Organising team</h2></div><p>Bringing together perspectives from across the community.</p></div>
  <div class="people">
{% for p in site.data.organisers %}
{% include person-card.html person=p folder="organisers" %}
{% endfor %}
  </div>
</section>

<section class="landing-section venue-section" id="venue" aria-labelledby="venue-heading">
  <div class="section-heading">
    <p class="section-kicker">The setting</p>
    <h2 id="venue-heading">Meet in Saarbrücken.<br>Stay curious.</h2>
  </div>
  <figure class="city-photo">
    <img src="{{ '/assets/img/venue/saarbruecken-ludwigsplatz.jpg' | relative_url }}" alt="Ludwigskirche and the surrounding baroque buildings on Ludwigsplatz in Saarbrücken" width="1800" height="814" loading="lazy">
    <figcaption>Ludwigsplatz, Saarbrücken · <a href="https://commons.wikimedia.org/wiki/File:Panorama_Saarbr%C3%BCcken_5986.jpg">Hanspeter Hofer / Wikimedia Commons</a> · <a href="https://creativecommons.org/licenses/by-sa/4.0/">CC BY-SA 4.0</a> · resized</figcaption>
  </figure>
  <div class="venue-introduction">
    <div class="venue-copy">
      <p class="venue-name">{{ site.workshop.venue }}</p>
      <p>Join us at <a href="{{ site.workshop.venue_url }}">CISPA</a> in beautiful Saarbrücken, a city on the River Saar where a lively research community meets old-town squares, riverside walks, and a distinctive Franco-German character.</p>
      <p>Beyond the workshop, explore the cafés around St. Johanner Markt, the baroque Ludwigskirche, and the paths along the river.</p>
      <a class="text-link" href="https://tourismus.saarbruecken.de/en">Discover Saarbrücken <span aria-hidden="true">↗</span></a>
    </div>
    <div class="travel-panel" id="getting-here">
      <p class="section-kicker">Before NeurIPS</p>
      <h3>A short journey.<br>A fresh conversation.</h3>
      <div class="rail-route" aria-label="Saarbrücken to Paris, about two hours by direct train"><span>Saarbrücken</span><span class="rail-line" aria-hidden="true"></span><span>Paris</span></div>
      <p class="rail-duration">About 2 hours <span>by direct train</span></p>
      <p>Meet on 2–3 December ahead of the <a href="https://neurips.cc/Conferences/2026/Dates">NeurIPS 2026 Paris programme (9–13 December)</a>. Direct rail connections make it easy to combine both visits.</p>
      <a class="text-link" href="https://www.bahn.de/reisen/view/verbindung/saarbruecken/paris.shtml">Explore the train connection <span aria-hidden="true">↗</span></a>
    </div>
  </div>
  <div class="research-neighbours">
    <div><p class="section-kicker">A city of ideas</p><h3>A close-knit research community</h3></div>
    <div><p>Saarbrücken is home to institutes working across artificial intelligence, computer science, and information security, alongside Saarland University.</p>
      <ul class="institute-links">
        <li><a href="https://cispa.de/en">CISPA <span aria-hidden="true">↗</span></a></li>
        <li><a href="https://www.mpi-inf.mpg.de/">Max Planck Institute for Informatics <span aria-hidden="true">↗</span></a></li>
        <li><a href="https://www.mpi-sws.org/">Max Planck Institute for Software Systems <span aria-hidden="true">↗</span></a></li>
        <li><a href="https://www.dfki.de/en/web">German Research Center for Artificial Intelligence (DFKI) <span aria-hidden="true">↗</span></a></li>
        <li><a href="https://www.kist-europe.eu/">KIST Europe <span aria-hidden="true">↗</span></a></li>
      </ul>
    </div>
  </div>
</section>

<section class="contact-strip" aria-labelledby="contact-heading">
  <div><p class="section-kicker">Keep in touch</p><h2 id="contact-heading">Join the conversation.</h2></div>
  <a class="text-link" href="mailto:{{ site.workshop.contact_email }}">{{ site.workshop.contact_email }} <span aria-hidden="true">↗</span></a>
</section>
