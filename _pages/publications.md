---
layout: default
title: Publications
permalink: /publications/
---

<section class="content-section" style="border-bottom:none;">
  <div class="container">
    <h2>Conference Publications</h2>
    {% for pub in site.data.publications %}
      <div class="pub-item">
        <div class="pub-header">
          <span class="pub-year">{{ pub.year }}</span>
          <span class="pub-title">{{ pub.title }}</span>
        </div>
        <div class="pub-authors">{{ pub.authors }}</div>
        <div class="pub-venue">{{ pub.venue }} ({{ pub.date }})</div>
        <div class="pub-actions">
          <button class="pill-btn" onclick="toggleDrawer('page-bib-{{ pub.id }}')">BIB</button>
          <button class="pill-btn" onclick="toggleDrawer('page-abs-{{ pub.id }}')">Abstract</button>
        </div>
        <div id="page-bib-{{ pub.id }}" class="pub-drawer">
          <pre>{{ pub.bibtex }}</pre>
        </div>
        <div id="page-abs-{{ pub.id }}" class="pub-drawer">
          <p>{{ pub.abstract }}</p>
        </div>
      </div>
    {% endfor %}
  </div>
</section>
