---
layout: page
title: <strong>Education</strong>
permalink: /education/
nav: true
nav_order: 2
description: Academic background.
---

<style>
  .education-list {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .education-entry {
    display: grid;
    grid-template-columns: 90px 1fr;
    gap: 1rem;
    align-items: start;
    padding: 1rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%);
  }

  .education-logo {
    width: 90px;
    height: 90px;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .education-logo img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    object-position: center;
    display: block;
  }

  .education-year {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.35rem;
  }

  .education-body h3 {
    color: #000;
    font-weight: 700;
    margin: 0 0 0.35rem 0;
  }

  .education-body p {
    margin: 0 0 0.25rem 0;
  }

  @media (max-width: 768px) {
    .education-entry {
      grid-template-columns: 70px 1fr;
      gap: 0.85rem;
    }

    .education-logo {
      width: 70px;
      height: 70px;
    }
  }
</style>

<div class="academic-page">

  <div class="section-card">
    <div class="education-list">

      <div class="education-entry">
        <div class="education-logo">
          <img src="{{ '/assets/img/comu.png' | relative_url }}" alt="Çanakkale Onsekiz Mart University">
        </div>
        <div class="education-body">
          <div class="education-year">2012–2019</div>
          <h3>PhD</h3>
          <p>Çanakkale Onsekiz Mart University</p>
          <p>Natural and Applied Sciences Institute, Fishing and Processing Technology</p>
          <p><strong>Thesis:</strong> Determination of Flesh Quality of Black Sea Trout (<em>Salmo labrax</em> PALLAS, 1814) Fed with Carotenoid-Supplemented Diets</p>
        </div>
      </div>

      <div class="education-entry">
        <div class="education-logo">
          <img src="{{ '/assets/img/comu.png' | relative_url }}" alt="Çanakkale Onsekiz Mart University">
        </div>
        <div class="education-body">
          <div class="education-year">2009–2012</div>
          <h3>MSc</h3>
          <p>Çanakkale Onsekiz Mart University</p>
          <p>Natural and Applied Sciences Institute, Fisheries</p>
          <p><strong>Thesis:</strong> Determination of Quality Parameters of Coated Products (Croquettes) Obtained from Different Seafood Species</p>
        </div>
      </div>

      <div class="education-entry">
        <div class="education-logo">
          <img src="{{ '/assets/img/comu.png' | relative_url }}" alt="Çanakkale Onsekiz Mart University">
        </div>
        <div class="education-body">
          <div class="education-year">2005–2009</div>
          <h3>BSc</h3>
          <p>Çanakkale Onsekiz Mart University</p>
          <p>Fisheries Faculty</p>
          <p>Fisheries Engineering</p>
        </div>
      </div>

      <div class="education-entry">
        <div class="education-logo">
          <img src="{{ '/assets/img/ist.png' | relative_url }}" alt="Istanbul University">
        </div>
        <div class="education-body">
          <div class="education-year">2023–Present</div>
          <h3>BSc</h3>
          <p>Istanbul University</p>
          <p>Open and Distance Education Faculty</p>
          <p>Radio, Television and Cinema</p>
        </div>
      </div>

    </div>
  </div>

</div>
