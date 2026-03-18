---
layout: page
permalink: /committees/
title: Committees
nav: true
nav_order: 7
description: Committees, working groups, scientific boards, and organizational roles.
---

<div class="academic-page">
  <div class="section-card">
    <h2>Committees</h2>
    <ul class="entry-list">
      {% for item in site.data.boards.items %}
      <li>
        <span class="entry-title">{{ item.title }}</span>
        <span class="entry-meta">{{ item.dates }} · {{ item.organization }}</span>
      </li>
      {% endfor %}
    </ul>
  </div>
</div>
