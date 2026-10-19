---
layout: default
title: Projects
description: Selected computational physics, experimental physics, and HEP projects.
---
<section class="page-intro">
  <p class="eyebrow">Portfolio</p>
  <h1>Projects</h1>
  <p class="lede">A small, evidence-led selection. Public repositories are linked directly; private work is labelled as development and has no fabricated results.</p>
</section>
<div class="filters" aria-label="Project filters">
  <button class="filter active" data-filter="all">All</button>
  <button class="filter" data-filter="HEP">HEP</button>
  <button class="filter" data-filter="Monte Carlo">Monte Carlo</button>
  <button class="filter" data-filter="ML">ML</button>
  <button class="filter" data-filter="Laboratory">Laboratory</button>
  <button class="filter" data-filter="Numerical methods">Numerical methods</button>
</div>
<div class="project-list">
{% for project in site.projects %}
  <article class="project-row" data-tags="{{ project.tags | join: ',' }}">
    {% if project.image %}<a class="project-thumb" href="{{ project.url | relative_url }}"><img src="{{ project.image | relative_url }}" alt="{{ project.image_alt }}"></a>{% endif %}
    <div><p class="eyebrow">{{ project.category }}{% if project.status %} · {{ project.status }}{% endif %}</p><h2><a href="{{ project.url | relative_url }}">{{ project.title }}</a></h2></div>
    <p>{{ project.summary }}</p>
    <a class="text-link" href="{{ project.url | relative_url }}">View →</a>
  </article>
{% endfor %}
</div>
<section class="section compact-section">
  <div class="section-heading"><p class="eyebrow">More in development</p><h2>Building the HEP foundation.</h2></div>
  <div class="card-grid">
    <article class="card"><p class="eyebrow">C++ · HEP</p><h3>Particle-physics learning laboratory</h3><p>A private pedagogical C++20/CMake project covering four-vectors, kinematics, toy Monte Carlo, and detector concepts. No public link or completed-result claim yet.</p></article>
    <article class="card"><p class="eyebrow">HEP workflow</p><h3>HEP project template</h3><p>A private scaffold for ROOT, Geant4, CMake, Python, notebooks, and tests. It is infrastructure in development, not a finished simulation.</p></article>
    <article class="card"><p class="eyebrow">ROOT · local</p><h3>ROOT practice macros</h3><p>Local introductory macros for histograms, graphs, random numbers, and text-file input. TODO: publish with a README before linking it.</p></article>
  </div>
</section>
<script>
document.querySelectorAll(".filter").forEach(button => button.addEventListener("click", () => {
  document.querySelectorAll(".filter").forEach(item => item.classList.remove("active"));
  button.classList.add("active");
  const filter = button.dataset.filter;
  document.querySelectorAll(".project-row").forEach(row => {
    row.hidden = filter !== "all" && !row.dataset.tags.split(",").includes(filter);
  });
}));
</script>
