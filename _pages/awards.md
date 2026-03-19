---
layout: page
title: <strong>Awards</strong>
permalink: /awards/
nav: true
nav_order: 9
description: Awards, recognitions, and distinctions.
---

<style>
  .award-list {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .award-entry {
    display: grid;
    grid-template-columns: 110px 1fr;
    gap: 1rem;
    align-items: center;
    padding: 1rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%);
  }

  .award-logo {
    width: 110px;
    height: 110px;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .award-logo img {
    width: 100%;
    height: 100%;
    display: block;
  }

  .award-logo--contain img {
    object-fit: contain;
    object-position: center;
  }

  .award-date {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.2rem;
    font-size: 0.98rem;
  }

  .award-role {
    font-weight: 700;
    color: var(--global-text-color);
    margin-bottom: 0.2rem;
    line-height: 1.5;
  }

  .award-name {
    margin: 0;
    line-height: 1.5;
    color: var(--global-text-color);
    font-style: italic;
  }

  @media (max-width: 768px) {
    .award-entry {
      grid-template-columns: 80px 1fr;
      gap: 0.85rem;
      align-items: start;
    }

    .award-logo {
      width: 80px;
      height: 80px;
    }
  }
</style>

<div class="academic-page">

  <div class="section-card">
    <h2 class="section-title">Awards</h2>

    <div class="award-list">
      <div class="award-entry">
        <div class="award-logo award-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="award-content">
          <div class="award-date">2026</div>
          <div class="award-role">Publication Incentive Award</div>
          <p class="award-name">The Scientific and Technological Research Council of Türkiye (TÜBİTAK)</p>
        </div>
      </div>

      <div class="award-entry">
        <div class="award-logo award-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="award-content">
          <div class="award-date">2025</div>
          <div class="award-role">Publication Incentive Award</div>
          <p class="award-name">The Scientific and Technological Research Council of Türkiye (TÜBİTAK)</p>
        </div>
      </div>

      <div class="award-entry">
        <div class="award-logo award-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="award-content">
          <div class="award-date">2023</div>
          <div class="award-role">Publication Incentive Award</div>
          <p class="award-name">The Scientific and Technological Research Council of Türkiye (TÜBİTAK)</p>
        </div>
      </div>

      <div class="award-entry">
        <div class="award-logo award-logo--contain">
          <img src="{{ '/assets/img/claricate.svg' | relative_url }}" alt="Clarivate">
        </div>
        <div class="award-content">
          <div class="award-date">2019</div>
          <div class="award-role">Top Peer Reviewer of 2019</div>
          <p class="award-name">Publons Peer Review Award for Top 1% in Agricultural Sciences</p>
        </div>
      </div>

      <div class="award-entry">
        <div class="award-logo award-logo--contain">
          <img src="{{ '/assets/img/claricate.svg' | relative_url }}" alt="Clarivate">
        </div>
        <div class="award-content">
          <div class="award-date">2018</div>
          <div class="award-role">Top Peer Reviewer of 2018</div>
          <p class="award-name">Publons Peer Review Award for Top 1% in Agricultural Sciences</p>
        </div>
      </div>

      <div class="award-entry">
        <div class="award-logo award-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="award-content">
          <div class="award-date">2012</div>
          <div class="award-role">Publication Incentive Award</div>
          <p class="award-name">The Scientific and Technological Research Council of Türkiye (TÜBİTAK)</p>
        </div>
      </div>

      <div class="award-entry">
        <div class="award-logo award-logo--contain">
          <img src="{{ '/assets/img/japan.png' | relative_url }}" alt="Turkish-Japanese Marine Forum">
        </div>
        <div class="award-content">
          <div class="award-date">2012</div>
          <div class="award-role">Best Poster Presentation</div>
          <p class="award-name">Harmonization of Bio-diversity and Marine Industries Symposium organized by Turkish-Japanese Marine Forum</p>
        </div>
      </div>
    </div>
  </div>

</div>
