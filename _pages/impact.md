---
layout: page
title: Impact
permalink: /impact/
nav: true
nav_order: 10
description: Media visibility, outreach, and wider impact.
---

<style>
  .impact-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.4rem;
  }

  .impact-card {
    display: block;
    text-decoration: none;
    color: inherit;
    border: 1px solid var(--global-divider-color);
    border-radius: 16px;
    overflow: hidden;
    background: var(--global-bg-color);
    transition: transform 0.18s ease, box-shadow 0.18s ease;
  }

  .impact-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 24px rgba(0, 0, 0, 0.08);
    text-decoration: none;
    color: inherit;
  }

  .impact-thumb {
    width: 100%;
    aspect-ratio: 16 / 10;
    overflow: hidden;
    background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%);
  }

  .impact-thumb img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  .impact-body {
    padding: 0.95rem 1rem 1rem 1rem;
  }

  .impact-year {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.35rem;
    font-size: 0.92rem;
  }

  .impact-title {
    font-weight: 700;
    line-height: 1.5;
    margin-bottom: 0.45rem;
    color: var(--global-text-color);
  }

  .impact-source {
    font-size: 0.88rem;
    color: var(--global-text-color);
    opacity: 0.8;
    line-height: 1.45;
  }
</style>

<div class="section-card">
  <h2 class="section-title">Media & Outreach</h2>

  <div class="impact-grid">
    <a class="impact-card" href="https://doi.org/10.1038/d41586-023-02314-0" target="_blank" rel="noopener">
      <div class="impact-thumb">
        <img src="{{ '/assets/img/impact001.png' | relative_url }}" alt="Nature feature">
      </div>
      <div class="impact-body">
        <div class="impact-year">2023</div>
        <div class="impact-title">I sample Antarctica’s seaweed to improve human health</div>
        <div class="impact-source">Where I Work, Nature · Nic Fleming</div>
      </div>
    </a>

    <a class="impact-card" href="https://polarjournal.ch/en/2023/07/31/medical-use-for-antarctic-seaweed/" target="_blank" rel="noopener">
      <div class="impact-thumb">
        <img src="{{ '/assets/img/impact002.png' | relative_url }}" alt="Polar Journal feature">
      </div>
      <div class="impact-body">
        <div class="impact-year">2023</div>
        <div class="impact-title">Medical Use for Antarctic Seaweed?</div>
        <div class="impact-source">Polar Journal · Julia Hager</div>
      </div>
    </a>

    <a class="impact-card" href="https://www.aa.com.tr/tr/gundem/turk-bilim-insanlarinin-guney-kutbundaki-laboratuvari-antarktika/2860096" target="_blank" rel="noopener">
      <div class="impact-thumb">
        <img src="{{ '/assets/img/impact003.png' | relative_url }}" alt="Anadolu Ajansı feature">
      </div>
      <div class="impact-body">
        <div class="impact-year">2023</div>
        <div class="impact-title">Türk Bilim İnsanlarının Güney Kutbu’ndaki Laboratuvarı: Antarktika</div>
        <div class="impact-source">Anadolu Ajansı · Şebnem Coşkun</div>
      </div>
    </a>
  </div>
</div>
