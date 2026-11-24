---
layout: default
title: Experience
permalink: /experience/
---

<section class="content-section" style="border-bottom:none;">
  <div class="container">
    <h2>Leadership &amp; Professional Experience</h2>
    {% for exp in site.data.experience %}
      <div class="card" style="margin-bottom:1.15rem;">
        <div class="card-meta">{{ exp.period }} &middot; {{ exp.location }}</div>
        <h3>{{ exp.role }} &mdash; {{ exp.organization }}</h3>
        <ul style="margin-top:0.4rem;">
          {% for b in exp.bullets %}
            <li>{{ b }}</li>
          {% endfor %}
        </ul>
      </div>
    {% endfor %}
  </div>
</section>
