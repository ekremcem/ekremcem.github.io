---
layout: page
title: <strong>Impact</strong>
permalink: /impact/
nav: true
nav_order: 10
description: Media visibility, outreach, and wider impact.
---

<style>
.impact-list{
  display:flex;
  flex-direction:column;
  gap:1.6rem;
}

.impact-card{
  display:grid;
  grid-template-columns:320px 1fr;
  gap:1.2rem;
  border:1px solid var(--global-divider-color);
  border-radius:16px;
  overflow:hidden;
  background:var(--global-bg-color);
  padding:1rem;
}

.impact-media{
  width:100%;
  min-height:240px;
  display:flex;
  align-items:stretch;
}

.impact-media-frame{
  width:100%;
  min-height:240px;
  border:1px solid #d6d6d6;
  border-radius:12px;
  overflow:hidden;
  background:#f6f6f6;
  box-shadow:0 2px 8px rgba(0,0,0,.04);
}

.impact-media-frame img{
  width:100%;
  height:100%;
  display:block;
  object-fit:cover;
}

.impact-media-frame.video-frame{
  padding:.35rem;
  background:#fff;
}

.twitter-tweet{
  margin:0 !important;
  width:100% !important;
}

.impact-body{
  padding:.15rem 0;
  display:flex;
  flex-direction:column;
  justify-content:center;
}

.impact-year{
  color:var(--global-theme-color);
  font-weight:700;
  margin-bottom:.3rem;
}

.impact-title{
  font-weight:700;
  font-size:1.05rem;
  line-height:1.5;
  margin-bottom:.55rem;
}

.impact-title a{
  text-decoration:none;
  color:inherit;
}

.impact-title a:hover{
  color:var(--global-theme-color);
}

.impact-source{
  font-size:.92rem;
  line-height:1.65;
  color:var(--global-text-color);
}

.impact-source a{
  color:var(--global-theme-color);
  text-decoration:none;
}

.impact-source a:hover{
  text-decoration:underline;
}

@media(max-width:860px){
  .impact-card{
    grid-template-columns:1fr;
  }
}
</style>

<div class="section-card">
  <h2 class="section-title">Media & Outreach</h2>

  <div class="impact-list">

    <div class="impact-card">
      <div class="impact-media">
        <div class="impact-media-frame">
          <img src="{{ '/assets/img/nature.jpg' | relative_url }}" alt="Nature feature" loading="lazy">
        </div>
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
        <div class="impact-media-frame">
          <img src="{{ '/assets/img/polarj.jpg' | relative_url }}" alt="Polar Journal feature" loading="lazy">
        </div>
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
        <div class="impact-media-frame">
          <img src="{{ '/assets/img/anadolu.jpg' | relative_url }}" alt="Anadolu Ajansı feature" loading="lazy">
        </div>
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
      <div class="impact-media">
        <div class="impact-media-frame video-frame">
          <blockquote class="twitter-tweet" data-dnt="true" data-theme="light">
            <a href="https://twitter.com/anadoluajansi/status/1641817643434008579"></a>
          </blockquote>
        </div>
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

<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
<script>
document.addEventListener('DOMContentLoaded', function () {
  function loadTwitterEmbeds() {
    if (window.twttr && window.twttr.widgets) {
      window.twttr.widgets.load();
    }
  }

  loadTwitterEmbeds();

  const twitterScript = document.querySelector('script[src*="platform.twitter.com/widgets.js"]');
  if (twitterScript) {
    twitterScript.addEventListener('load', loadTwitterEmbeds);
  }
});
</script>
