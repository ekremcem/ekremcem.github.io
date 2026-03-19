---
layout: page
title: <strong>Education</strong>
permalink: /education/
nav: true
nav_order: 1
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

  .course-list {
    display: flex;
    flex-direction: column;
  }

  .course-entry {
    padding: 0.7rem 0;
    border-bottom: 1px solid color-mix(in srgb, var(--global-divider-color) 70%, transparent 30%);
  }

  .course-entry:last-child {
    border-bottom: none;
  }

  .course-year {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.15rem;
  }

  .course-title {
    font-weight: 700;
    color: var(--global-text-color);
    line-height: 1.5;
    margin-bottom: 0.1rem;
  }

  .course-support {
    margin: 0;
    line-height: 1.5;
    color: var(--global-text-color);
    font-style: italic;
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

  <div class="section-card">
    <h2 class="section-title">Cources</h2>

    <div class="course-list">
      <div class="course-entry">
        <div class="course-year">2026</div>
        <div class="course-title">Webinar of Ocean Sessions – Future of the High Seas</div>
        <p class="course-support">Copernicus, the Copernicus Marine Service and Mercator Ocean International (Virtual)</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2026</div>
        <div class="course-title">Webinar of Ocean Sessions – MyOcean Pro Viewer Usage</div>
        <p class="course-support">Copernicus, the Copernicus Marine Service and Mercator Ocean International (Virtual)</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2024</div>
        <div class="course-title">Webinar of Functional Food from Algae</div>
        <p class="course-support">EU-funded Algae4IBD Project (Virtual)</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2023</div>
        <div class="course-title">Advancing Scholarly Publishing through Evolution, Equity, and Empowerment</div>
        <p class="course-support">9th ACSE Annual Meeting (Virtual)</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2020</div>
        <div class="course-title">Training Course on Green Aquaculture</div>
        <p class="course-support">Technology for the Belt &amp; Road Countries, China (Virtual)</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2020</div>
        <div class="course-title">Computer Application in Fisheries “R Software”</div>
        <p class="course-support">Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM) (Virtual)</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2020</div>
        <div class="course-title">Project Proposal Training for Horizon 2020 Era-net Calls</div>
        <p class="course-support">Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM) (Virtual)</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2017</div>
        <div class="course-title">Amino Acid Analysis and Application Training with HPLC</div>
        <p class="course-support">Agilent Technologies, Trabzon, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2016</div>
        <div class="course-title">HPLC Setup and Usage Training</div>
        <p class="course-support">Agilent Technologies, Trabzon, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2016</div>
        <div class="course-title">Use of SPSS Statistical Package Program in Agricultural Research</div>
        <p class="course-support">Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM), Isparta, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2015</div>
        <div class="course-title">Trial Techniques and Statistics in Agricultural Research</div>
        <p class="course-support">Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM), Isparta, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2015</div>
        <div class="course-title">Use of Statistical Package Programs in Agricultural Research</div>
        <p class="course-support">Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM), Isparta, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2015</div>
        <div class="course-title">Editor and Writer Training Seminar</div>
        <p class="course-support">The National Academic Network and Information Center (ULAKBİM), Antalya, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2015</div>
        <div class="course-title">Academic Article Writing Course</div>
        <p class="course-support">TEOL Language School, Trabzon, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2014</div>
        <div class="course-title">National Academic AR-GE Support Presentation and Project Proposal Preparation Training</div>
        <p class="course-support">The Scientific and Technological Research Council of Türkiye (TÜBİTAK), Antalya, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2008</div>
        <div class="course-title">ISO 9001, ISO 2000 and Internal Auditor Certification Program</div>
        <p class="course-support">Utku Counseling, Çanakkale, Türkiye</p>
      </div>

      <div class="course-entry">
        <div class="course-year">2008</div>
        <div class="course-title">One Star Diver Training Program</div>
        <p class="course-support">Confédération Mondiale des Activités Subaquatiques, CMAS</p>
      </div>
    </div>
  </div>

</div>
