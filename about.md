---
layout: page
title: About the workshop
permalink: /about/
---

<div class="about-page">
  <section class="landing-section about-section" id="about" aria-labelledby="about-heading">
    <div class="section-heading">
      <h2 id="about-heading">Why epistemic intelligence?</h2>
    </div>
    <div class="section-prose">
      <p>AI systems increasingly make predictions and decisions in situations where their knowledge is incomplete. Recognising these limits is essential to knowing when to rely on a prediction, seek more information, or reconsider a decision.</p>
      <p>This ability to understand and reason about the limits of one's knowledge is what we call <strong>epistemic intelligence</strong>. The workshop connects philosophical, mathematical, and statistical foundations with the practical challenges of building AI that can learn and act reliably under uncertainty.</p>
    </div>
  </section>

  <section class="landing-section topics-section" id="topics" aria-labelledby="topics-heading">
    <div class="section-heading section-heading-wide">
      <h2 id="topics-heading">Topics</h2>
      <p>What does it take for AI to reason well when its knowledge is incomplete?</p>
    </div>
    <div class="landing-topics">
{% for topic in site.data.topics %}
      <details class="landing-topic">
        <summary><span class="topic-number" aria-hidden="true">0{{ forloop.index }}</span><h3>{{ topic.title }}</h3><span class="topic-toggle" aria-hidden="true"></span></summary>
        <div class="landing-topic-body">
          <p>{{ topic.description }}</p>
          <ul>{% for point in topic.points %}<li>{{ point }}</li>{% endfor %}</ul>
        </div>
      </details>
{% endfor %}
    </div>
  </section>

  <section class="landing-section organisers-section" id="organisers" aria-labelledby="organisers-heading">
    <div class="section-heading section-heading-wide">
      <h2 id="organisers-heading">Organising team</h2>
      <p>Bringing together perspectives from across the community.</p>
    </div>
    <div class="people organising-people">
{% for p in site.data.organisers %}
{% include person-card.html person=p folder="organisers" %}
{% endfor %}
    </div>
  </section>

  <section class="landing-section history-section" id="history" aria-labelledby="history-heading">
    <div class="section-heading">
      <h2 id="history-heading">Workshop history</h2>
    </div>
    <div class="section-prose"><p>EIML began at EurIPS 2025 in Copenhagen, bringing together researchers interested in how machine learning can recognise and respond to gaps in its knowledge. The second edition, at ICML 2026 in Seoul, expanded the conversation to generative AI, robustness, safety, and continual learning. EIML3 continues this journey in the Saarbrücken region, connecting the foundations of imprecision and uncertainty with the needs of modern AI.</p></div>
    <ol class="edition-trail">
      <li><a href="{{ '/archive/eiml1/' | relative_url }}"><span class="edition-year">2025 · Copenhagen</span><strong>EIML1 @ EurIPS</strong><span>Where the conversation began <span aria-hidden="true">↗</span></span></a></li>
      <li><a href="{{ '/archive/eiml2/' | relative_url }}"><span class="edition-year">2026 · Seoul</span><strong>EIML2 @ ICML</strong><span>Broadening the perspective <span aria-hidden="true">↗</span></span></a></li>
      <li class="edition-current"><span class="edition-year">2026 · Saarbrücken</span><strong>EIML3 @ Saarbrücken</strong><span>The conversation continues</span></li>
    </ol>
  </section>
</div>
