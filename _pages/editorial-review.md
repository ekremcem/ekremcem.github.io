---
layout: page
title: <strong>Editorial & Review</strong>
permalink: /editorial-review/
nav: true
nav_order: 6
description: Editorial roles and peer-review contributions.
---

<style>
  .record-list {
    display: flex;
    flex-direction: column;
    gap: 1rem;
  }

  .record-entry {
    display: grid;
    grid-template-columns: 110px 1fr;
    gap: 1rem;
    align-items: center;
    padding: 1rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%);
  }

  .record-logo {
    width: 110px;
    height: 140px;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .record-logo img {
    width: 100%;
    height: 100%;
    display: block;
  }

  .record-logo--cover img {
    object-fit: cover;
    object-position: center;
  }

  .record-logo--contain img {
    object-fit: contain;
    object-position: center;
  }

  .record-date {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.2rem;
    font-size: 0.98rem;
  }

  .record-role {
    font-weight: 700;
    color: var(--global-text-color);
    margin-bottom: 0.2rem;
    line-height: 1.5;
  }

  .record-name {
    margin: 0;
    line-height: 1.5;
    display: flex;
    align-items: center;
    gap: 0.35rem;
    flex-wrap: wrap;
  }

  .record-name-text {
    font-style: italic;
    color: var(--global-text-color);
  }

  .record-link {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    font-size: 0.95rem;
    line-height: 1;
    color: var(--global-theme-color);
    transform: translateY(-1px);
  }

  .record-link:hover {
    text-decoration: none;
    opacity: 0.8;
  }

  .project-call {
    margin: 0;
    line-height: 1.5;
    color: var(--global-text-color);
  }

  .peer-review-grid {
    column-count: 2;
    column-gap: 2rem;
  }

  .peer-review-row {
    break-inside: avoid;
    display: grid;
    grid-template-columns: minmax(0, 1fr) auto auto;
    gap: 0.8rem;
    align-items: baseline;
    padding: 0.28rem 0;
    border-bottom: 1px solid color-mix(in srgb, var(--global-divider-color) 70%, transparent 30%);
  }

  .peer-review-journal {
    min-width: 0;
    color: var(--global-text-color);
  }

  .peer-review-count {
    font-weight: 700;
    color: var(--global-text-color);
    white-space: nowrap;
  }

  .peer-review-years {
    color: var(--global-theme-color);
    white-space: nowrap;
  }

  .peer-review-note {
    margin-top: 1rem;
    color: var(--global-text-color);
    line-height: 1.6;
  }

  .peer-review-note a {
    text-decoration: none;
    color: var(--global-theme-color);
    margin-left: 0.2rem;
  }

  .peer-review-note a:hover {
    opacity: 0.8;
  }

  @media (max-width: 768px) {
    .record-entry {
      grid-template-columns: 80px 1fr;
      gap: 0.85rem;
      align-items: start;
    }

    .record-logo {
      width: 80px;
      height: 105px;
    }

    .peer-review-grid {
      column-count: 1;
    }

    .peer-review-row {
      grid-template-columns: minmax(0, 1fr) auto auto;
      gap: 0.6rem;
    }
  }
</style>

<div class="academic-page">

  <div class="section-card">
    <h2 class="section-title">Editorial</h2>

    <div class="record-list">
      <div class="record-entry">
        <div class="record-logo record-logo--cover">
          <img src="{{ '/assets/img/TRJFAS.jpg' | relative_url }}" alt="TRJFAS">
        </div>
        <div class="record-content">
          <div class="record-date">2024 - Present</div>
          <div class="record-role">Topic Editor</div>
          <p class="record-name">
            <span class="record-name-text">Turkish Journal of Fisheries and Aquatic Sciences (TRJFAS)</span>
            <a class="record-link" href="https://www.trjfas.org/" target="_blank" rel="noopener" aria-label="Visit Turkish Journal of Fisheries and Aquatic Sciences website" title="Journal website">🔗</a>
          </p>
        </div>
      </div>

      <div class="record-entry">
        <div class="record-logo record-logo--cover">
          <img src="{{ '/assets/img/aquast.jpg' | relative_url }}" alt="Aquaculture Studies">
        </div>
        <div class="record-content">
          <div class="record-date">2025 - Present</div>
          <div class="record-role">Topic Editor</div>
          <p class="record-name">
            <span class="record-name-text">Aquaculture Studies</span>
            <a class="record-link" href="https://www.aquast.org/" target="_blank" rel="noopener" aria-label="Visit Aquaculture Studies website" title="Journal website">🔗</a>
          </p>
        </div>
      </div>

      <div class="record-entry">
        <div class="record-logo record-logo--cover">
          <img src="{{ '/assets/img/frontiers.jpg' | relative_url }}" alt="Frontiers in Aquaculture">
        </div>
        <div class="record-content">
          <div class="record-date">2025 - 2026</div>
          <div class="record-role">Special Issue Editor: Aquatic Natural Products and Aquaculture: Production, Chemical Characterization, and Functional Applications</div>
          <p class="record-name">
            <span class="record-name-text">Frontiers in Aquaculture</span>
            <a class="record-link" href="https://www.frontiersin.org/research-topics/74526/aquatic-natural-products-and-aquaculture-production-chemical-characterization-and-functional-applications" target="_blank" rel="noopener" aria-label="Visit Frontiers in Aquaculture page" title="Journal website">🔗</a>
          </p>
        </div>
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">Project Review</h2>

    <div class="record-list">
      <div class="record-entry">
        <div class="record-logo record-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="record-content">
          <div class="record-date">2025</div>
          <div class="record-role">Remote Evaluator</div>
          <p class="project-call">TUBITAK-CAS Bilateral Cooperation Call, Academic Research Funding Programmes Directorate (ARDEB) - TUBİTAK</p>
        </div>
      </div>

      <div class="record-entry">
        <div class="record-logo record-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="record-content">
          <div class="record-date">2025</div>
          <div class="record-role">Remote Evaluator</div>
          <p class="project-call">TUBITAK-1002 Short Term Support Module Funding Program, Academic Research Funding Programmes Directorate (ARDEB) - TUBİTAK</p>
        </div>
      </div>

      <div class="record-entry">
        <div class="record-logo record-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="record-content">
          <div class="record-date">2023</div>
          <div class="record-role">Remote Evaluator</div>
          <p class="project-call">TUBITAK-1001 The Scientific and Technological Research Projects Funding Program, Academic Research Funding Programmes Directorate (ARDEB) - TUBİTAK</p>
        </div>
      </div>

      <div class="record-entry">
        <div class="record-logo record-logo--contain">
          <img src="{{ '/assets/img/tubitak.png' | relative_url }}" alt="TÜBİTAK">
        </div>
        <div class="record-content">
          <div class="record-date">2022</div>
          <div class="record-role">Observer Panelist</div>
          <p class="project-call">TUBITAK-1001 The Scientific and Technological Research Projects Funding Program, Academic Research Funding Programmes Directorate (ARDEB) - TUBİTAK</p>
        </div>
      </div>

      <div class="record-entry">
        <div class="record-logo record-logo--contain">
          <img src="{{ '/assets/img/NOAA.png' | relative_url }}" alt="NOAA">
        </div>
        <div class="record-content">
          <div class="record-date">2019 - 2020</div>
          <div class="record-role">Remote Evaluator</div>
          <p class="project-call">Saltonstall-Kennedy Grant Program, National Oceanic and Atmospheric Administration (NOAA)</p>
        </div>
      </div>
    </div>
  </div>

  <div class="section-card">
    <h2 class="section-title">Peer Review</h2>

    <div class="peer-review-grid">
      <div class="peer-review-row"><span class="peer-review-journal">Food Chemistry</span><span class="peer-review-count">86</span><span class="peer-review-years">2016–2025</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Algal Research</span><span class="peer-review-count">21</span><span class="peer-review-years">2023–2025</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Current Research in Nutrition and Food Science Journal</span><span class="peer-review-count">13</span><span class="peer-review-years">2019–2020</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Aquatic Food Studies</span><span class="peer-review-count">5</span><span class="peer-review-years">2025</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Çanakkale Onsekiz Mart University Journal of Marine Sciences and Fisheries</span><span class="peer-review-count">5</span><span class="peer-review-years">2019–2023</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Aquaculture Studies</span><span class="peer-review-count">3</span><span class="peer-review-years">2024–2025</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Journal of Applied Phycology</span><span class="peer-review-count">3</span><span class="peer-review-years">2020–2021</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Environmental Monitoring and Assessment</span><span class="peer-review-count">2</span><span class="peer-review-years">2021</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Journal of the Black Sea Mediterranean Environment</span><span class="peer-review-count">2</span><span class="peer-review-years">2023</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">The European Zoological Journal</span><span class="peer-review-count">2</span><span class="peer-review-years">2024</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Aquaculture Nutrition</span><span class="peer-review-count">1</span><span class="peer-review-years">2025</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Cahiers de Biologie Marine</span><span class="peer-review-count">1</span><span class="peer-review-years">2023</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Food &amp; Function</span><span class="peer-review-count">1</span><span class="peer-review-years">2016</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Journal of Animal Science and Veterinary Medicine</span><span class="peer-review-count">1</span><span class="peer-review-years">2020</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Oriental Journal of Chemistry</span><span class="peer-review-count">1</span><span class="peer-review-years">2019</span></div>

      <div class="peer-review-row"><span class="peer-review-journal">LWT - Food Science and Technology</span><span class="peer-review-count">39</span><span class="peer-review-years">2017–2021</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Food Research International</span><span class="peer-review-count">19</span><span class="peer-review-years">2017–2020</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Biological Trace Element Research</span><span class="peer-review-count">8</span><span class="peer-review-years">2021</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Turkish Journal of Fisheries and Aquatic Sciences</span><span class="peer-review-count">5</span><span class="peer-review-years">2017–2018</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Food Chemistry Advances</span><span class="peer-review-count">4</span><span class="peer-review-years">2022–2024</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">European Food Research and Technology</span><span class="peer-review-count">3</span><span class="peer-review-years">2022–2024</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Asian Fisheries Science</span><span class="peer-review-count">2</span><span class="peer-review-years">2019</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">International Journal of Fisheries Science and Research</span><span class="peer-review-count">2</span><span class="peer-review-years">2017–2019</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Thalassas: An International Journal of Marine Sciences</span><span class="peer-review-count">2</span><span class="peer-review-years">2021</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Aquaculture International</span><span class="peer-review-count">1</span><span class="peer-review-years">2025</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Aquatic Sciences and Engineering</span><span class="peer-review-count">1</span><span class="peer-review-years">2021</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Fisheries &amp; Aquatic Life</span><span class="peer-review-count">1</span><span class="peer-review-years">2025</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">International Journal of Analytical Techniques</span><span class="peer-review-count">1</span><span class="peer-review-years">2017</span></div>
      <div class="peer-review-row"><span class="peer-review-journal">Marine Life Science &amp; Technology</span><span class="peer-review-count">1</span><span class="peer-review-years">2020</span></div>
    </div>

    <p class="peer-review-note">
      You can see detailed peer review and editorial records here
      <a href="https://www.webofscience.com/wos/author/record/W-5068-2017" target="_blank" rel="noopener" aria-label="View Web of Science peer review and editorial record" title="Web of Science record">🔗</a>
    </p>
  </div>

</div>
