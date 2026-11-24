---
layout: default
title: Research
permalink: /research/
---

<section class="content-section" style="border-bottom:none;">
  <div class="container">
    <h2>Research Experience</h2>
    {% for item in site.data.research %}
      <div class="highlight-card">
        <div class="meta">{{ item.period }} &middot; {{ item.role }}</div>
        <h3>{{ item.title }}</h3>
        <p style="margin-bottom:0.5rem;"><strong>Supervisor:</strong> {{ item.advisor }} ({{ item.institution }})</p>
        <p>{{ item.summary }}</p>
        <ul>
          {% for bullet in item.highlights %}
            <li>{{ bullet }}</li>
          {% endfor %}
        </ul>
        <div class="tag-list" style="margin-top:0.85rem; margin-bottom:0;">
          {% for tool in item.tools %}
            <span class="tag">{{ tool }}</span>
          {% endfor %}
        </div>
      </div>
    {% endfor %}
  </div>
</section>
