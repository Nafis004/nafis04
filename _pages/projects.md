---
layout: default
title: Projects
permalink: /projects/
---

<section class="content-section" style="border-bottom:none;">
  <div class="container">
    <h2>Engineering &amp; Simulation Projects</h2>
    {% for proj in site.data.projects %}
      <div class="card" style="margin-bottom:1.25rem;">
        <div class="card-meta">{{ proj.date }} &middot; {{ proj.category }}</div>
        <h3>{{ proj.title }}</h3>
        <p>{{ proj.summary }}</p>
        <ul>
          {% for b in proj.bullets %}
            <li>{{ b }}</li>
          {% endfor %}
        </ul>
        <div class="tag-list" style="margin-top:0.75rem; margin-bottom:0;">
          {% for tool in proj.tools %}
            <span class="tag">{{ tool }}</span>
          {% endfor %}
        </div>
      </div>
    {% endfor %}
  </div>
</section>
