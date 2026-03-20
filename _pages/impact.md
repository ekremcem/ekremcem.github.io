---
layout: page
title: Impact
permalink: /impact/
nav: true
nav_order: 10
description: Media visibility, outreach, and wider impact.
---

<style>
  .impact-list {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
  }

  .impact-card {
    display: grid;
    grid-template-columns: 280px 1fr;
    gap: 1.15rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 16px;
    overflow: hidden;
    background: var(--global-bg-color);
  }

  .impact-media {
    width: 100%;
    min-height: 210px;
    background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%);
    overflow: hidden;
  }

  .impact-media img {
    width: 100%;
    height: 100%;
    display: block;
    object-fit: cover;
  }

  .impact-video-box {
    display: flex;
    align-items: center;
    justify-content: center;
    min-height: 210px;
    padding: 1rem;
    background: color-mix(in srgb, var(--global-bg-color) 90%, var(--global-theme-color) 10%);
    color: var(--global-theme-color);
    font-weight: 700;
    text-align: center;
    line-height: 1.5;
  }

  .impact-body {
    padding: 1rem 1.05rem 1rem 0;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .impact-year {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.3rem;
    font-size: 0.95rem;
  }

  .impact-title {
    font-weight: 700;
    line-height: 1.5;
    margin-bottom: 0.55rem;
    color: var(--global-text-color);
    font-size: 1.02rem;
  }

  .impact-title a {
    color: inherit;
    text-decoration: none;
  }

  .impact-title a:hover {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .impact-source {
    font-size: 0.92rem;
    line-height: 1.65;
    color: var(--global-text-color);
    opacity: 0.95;
  }

  .impact-source a {
    color: var(--global-theme-color);
    text-decoration: none;
  }

  .impact-source a:hover {
    text-decoration: underline;
  }

  @media (max-width: 860px) {
    .impact-card {
      grid-template-columns: 1fr;
    }

    .impact-body {
      padding: 0 1rem 1rem 1rem;
    }

    .impact-media,
    .impact-video-box {
      min-height: 220px;
    }
  }
</style>

<div class="section-card">
  <h2 class="section-title">Media & Outreach</h2>

  <div class="impact-list">

    <div class="impact-card">
      <div class="impact-media">
        <img src="{{ '/assets/img/nature.jpg' | relative_url }}" alt="Nature feature">
      </div>
      <div class="impact-body">
        <div class="impact-year">2023</div>
        <div class="impact-title">
          <a href="https://doi.org/10.1038/d41586-023-02314-0" target="_blank" rel="noopener">I sample Antarctica’s seaweed to improve human health</a>
        </div>
        <div class="impact-source">
          Where I Work, Nature. <a href="https://www.linkedin.com/in/nic-fleming-8a572844/" target="_blank" rel="noopener">Nic Fleming</a>. Photo: <a href="https://www.instagram.com/sebnemcoskun/" target="_blank" rel="noopener">Şebnem Coşkun</a>.
        </div>
      </div>
    </div>

    <div class="impact-card">
      <div class="impact-media">
        <img src="{{ '/assets/img/polarj.jpeg' | relative_url }}" alt="Polar Journal feature">
      </div>
      <div class="impact-body">
        <div class="impact-year">2023</div>
        <div class="impact-title">
          <a href="https://polarjournal.ch/en/2023/07/31/medical-use-for-antarctic-seaweed/" target="_blank" rel="noopener">Medical Use for Antarctic Seaweed?</a>
        </div>
        <div class="impact-source">
          Polar Journal. <a href="https://www.linkedin.com/in/julia-hager-77812142/" target="_blank" rel="noopener">Julia Hager</a>. Photo: <a href="https://linkedin.com/in/michael-wenger-phd?skipRedirect=true&miniProfileUrn=urn%3Ali%3Afsd_profile%3AACoAAAgujQEBeHEpC4ksR2gKjH7FKaZDl9LpPM4" target="_blank" rel="noopener">Michael Wenger</a>.
        </div>
      </div>
    </div>

    <div class="impact-card">
      <div class="impact-media">
        <img src="{{ '/assets/img/anadolu.jpg' | relative_url }}" alt="Anadolu Ajansı feature">
      </div>
      <div class="impact-body">
        <div class="impact-year">2023</div>
        <div class="impact-title">
          <a href="https://www.aa.com.tr/tr/gundem/turk-bilim-insanlarinin-guney-kutbundaki-laboratuvari-antarktika/2860096" target="_blank" rel="noopener">Türk Bilim İnsanlarının Güney Kutbu’ndaki Laboratuvarı: Antarktika</a>
        </div>
        <div class="impact-source">
          Anadolu Ajansı. Photo: <a href="https://www.instagram.com/sebnemcoskun/" target="_blank" rel="noopener">Şebnem Coşkun</a>.
        </div>
      </div>
    </div>

    <div class="impact-card">
      <div class="impact-video-box">
        Video interview
      </div>
      <div class="impact-body">
        <div class="impact-year">2023</div>
        <div class="impact-title">
          <a href="https://www.aa.com.tr/tr/gundem/turk-bilim-insanlarinin-guney-kutbundaki-laboratuvari-antarktika/2860096" target="_blank" rel="noopener">Türk bilim insanları 7. Ulusal Antarktika Bilim Seferi kapsamında yer bilimleri, yaşam bilimleri, fiziki bilimler ve sosyal bilimler konularında 18 ayrı projeyi Antarktika'ya taşıdı.</a>
        </div>
        <div class="impact-source">
          Anadolu Ajansı. Interview: <a href="https://www.instagram.com/sebnemcoskun/" target="_blank" rel="noopener">Şebnem Coşkun</a>.
        </div>
      </div>
    </div>

  </div>
</div>
