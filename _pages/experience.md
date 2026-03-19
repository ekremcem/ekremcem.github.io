---
layout: page
title: <strong>Experience</strong>
permalink: /experience/
nav: true
nav_order: 3
description: Research, administrative roles, skills, and languages.
---

<style>
  .exp-entry {
    display: grid;
    grid-template-columns: 90px 1fr;
    gap: 1rem;
    align-items: center;
    padding: 1rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%);
    margin-bottom: 1rem;
  }

  .exp-logo {
    width: 90px;
    height: 90px;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .exp-logo img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    object-position: center;
    display: block;
  }

  .exp-date {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.3rem;
  }

  .exp-role {
    font-weight: 700;
  }

  @media (max-width: 768px) {
    .exp-entry {
      grid-template-columns: 70px 1fr;
      gap: 0.85rem;
      align-items: start;
    }

    .exp-logo {
      width: 70px;
      height: 70px;
    }
  }
</style>

<div class="split-grid">
  <div>

    <div class="section-card">
      <h2 class="section-title">Work Experience</h2>

      <div class="exp-entry">
        <div class="exp-logo">
          <img src="{{ '/assets/img/koyun.png' | relative_url }}" alt="Sheep Breeding Research Institute">
        </div>
        <div>
          <div class="exp-date">2021 – Present</div>
          <div class="exp-role">Researcher</div>
          <p>Sheep Breeding Research Institute, Department of Fisheries — Balıkesir</p>
        </div>
      </div>

      <div class="exp-entry">
        <div class="exp-logo">
          <img src="{{ '/assets/img/tae.png' | relative_url }}" alt="National Antarctic Science Expedition">
        </div>
        <div>
          <div class="exp-date">2023</div>
          <div class="exp-role">Researcher / Expedition Participant</div>
          <p>7th National Antarctic Science Expedition</p>
        </div>
      </div>

      <div class="exp-entry" style="margin-bottom: 0;">
        <div class="exp-logo">
          <img src="{{ '/assets/img/sumae.jpeg' | relative_url }}" alt="Central Fisheries Research Institute">
        </div>
        <div>
          <div class="exp-date">2013 – 2021</div>
          <div class="exp-role">Researcher</div>
          <p>Central Fisheries Research Institute, Aquaculture Department — Trabzon</p>
        </div>
      </div>
    </div>

    <div class="section-card">
      <h2 class="section-title">Administrative Roles</h2>

      <div class="timeline-entry compact" style="background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%); padding: 1rem; border-radius: 14px; margin-bottom: 1rem;">
        <div class="timeline-year" style="color: var(--global-theme-color); font-weight:700;">2025 – Present</div>
        <div class="timeline-body">
          <strong><h3>Chairman</h3></strong>
          <p>Local Fisheries Ethics Committee</p>
        </div>
      </div>

      <div class="timeline-entry compact" style="background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%); padding: 1rem; border-radius: 14px;">
        <div class="timeline-year" style="color: var(--global-theme-color); font-weight:700;">2013 – 2021</div>
        <div class="timeline-body">
         <strong>Unit Head</strong>
          <p>Recirculating Aquaculture System Unit, Central Fisheries Research Institute</p>
        </div>
      </div>
    </div>

  </div>

  <div>

    <div class="section-card">
      <h2 class="section-title">Skills</h2>
      <div class="tag-cloud">
        <span class="tag-pill">Aquaculture</span>
        <span class="tag-pill">Marine biochemistry</span>
        <span class="tag-pill">Seafood chemistry</span>
        <span class="tag-pill">Macroalgae</span>
        <span class="tag-pill">Marine natural products</span>
        <span class="tag-pill">Secondary metabolites</span>
        <span class="tag-pill">Bivalves</span>
        <span class="tag-pill">Polar science</span>
        <span class="tag-pill">HPLC</span>
        <span class="tag-pill">RAS systems</span>
        <span class="tag-pill">Project development</span>
        <span class="tag-pill">Academic editing</span>
        <span class="tag-pill">R statistics</span>
        <span class="tag-pill">Scallop biology</span>
        <span class="tag-pill">Oyster biology</span>
        <span class="tag-pill">Marine toxins</span>
      </div>
    </div>

    <div class="section-card">
      <h2 class="section-title">Languages</h2>
      <div class="metric-row">
        <div>
          <h3>Turkish</h3>
          <p>Native</p>
        </div>
      </div>
      <div class="metric-row">
        <div>
          <h3>English</h3>
          <p>Advanced</p>
        </div>
        <div class="metric-meta">YDS: 85 (2022) · YÖKDİL: 88.75 (2022)</div>
      </div>
    </div>

  </div>
</div>
