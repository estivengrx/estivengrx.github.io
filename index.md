---
layout: default
title: Home
description: Computational physics and high-energy physics portfolio by Estiven Castrillón.
physics_visual: true
---
<section class="hero">
  <div class="hero-copy">
    <p class="eyebrow">Physics · computation · measurement</p>
    <h1>I build transparent computational tools for physics.</h1>
    <p class="lede">I am Estiven Castrillón, a physics student at Universidad de Antioquia in Medellín. My current focus is high-energy physics, numerical methods, Monte Carlo simulation, and reproducible scientific code.</p>
    <div class="hero-actions">
      <a class="button" href="{{ '/projects/' | relative_url }}">Explore projects</a>
      <a class="text-link" href="https://github.com/estivengrx">GitHub ↗</a>
    </div>
  </div>
  <div class="hero-visual"><img src="{{ '/assets/images/physics-hero.svg' | relative_url }}" alt="" aria-hidden="true"></div>
</section>

<section class="section">
  <div class="section-heading"><p class="eyebrow">Selected work</p><h2>Evidence, not a list of buzzwords.</h2></div>
  <div class="card-grid">
    {% assign featured = site.projects | where: "featured", true %}
    {% for project in featured %}
    <article class="card">
      {% if project.image %}<a class="card-image" href="{{ project.url | relative_url }}"><img src="{{ project.image | relative_url }}" alt="{{ project.image_alt }}"></a>{% endif %}
      <p class="eyebrow">{{ project.category }}</p>
      <h3><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h3>
      <p>{{ project.summary }}</p>
      <a class="text-link" href="{{ project.url | relative_url }}">Read the project →</a>
    </article>
    {% endfor %}
  </div>
</section>

<section class="callout">
  <p class="eyebrow">Working direction</p>
  <h2>From measured signals to collision-level questions.</h2>
  <p>I am developing a foundation across scientific Python, C++, ROOT, detector concepts, and statistical learning. I document what is implemented, what is still experimental, and where the limitations are.</p>
</section>
