
Haklısın. Bundan sonra her değişiklikte kodun tamamını vereceğim. Aşağıda yalnızca ilgili proje başlığı İngilizce olarak değiştirilmiş tam kod yer alıyor.

---
layout: page
title: Projects
permalink: /projects/
nav: true
nav_order: 3
description: Projects as project leader and researcher.
---

<style>
  .project-controls {
    display: flex;
    justify-content: flex-end;
    margin-bottom: 1rem;
    position: relative;
  }

  .project-filter-toggle {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.45rem 0.9rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.95rem;
  }

  .project-filter-panel {
    display: none;
    position: absolute;
    top: 2.7rem;
    right: 0;
    z-index: 20;
    width: min(430px, 95vw);
    padding: 0.95rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: var(--global-bg-color);
    box-shadow: 0 8px 24px rgba(0, 0, 0, 0.08);
  }

  .project-filter-panel.open {
    display: block;
  }

  .filter-title {
    font-weight: 700;
    margin-bottom: 0.35rem;
  }

  .filter-subtitle {
    font-size: 0.88rem;
    color: var(--global-theme-color);
    margin-bottom: 0.7rem;
  }

  .filter-group {
    margin-bottom: 0.85rem;
  }

  .filter-group-title {
    font-weight: 700;
    font-size: 0.9rem;
    margin-bottom: 0.35rem;
  }

  .filter-options {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem 0.8rem;
  }

  .filter-options label {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.92rem;
    cursor: pointer;
  }

  .filter-options .count {
    color: var(--global-theme-color);
    font-size: 0.85rem;
  }

  .filter-actions {
    display: flex;
    justify-content: space-between;
    margin-top: 0.8rem;
    gap: 0.6rem;
  }

  .filter-btn {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.4rem 0.8rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.9rem;
  }

  .project-section-title {
    margin: 1.35rem 0 0.8rem 0;
  }

  #researcherTitle { margin-top: 3rem; }

  .project-leader-list,
  .project-researcher-list {
    display: flex;
    flex-direction: column;
    gap: 1.3rem;
  }

  .project-card {
    border: 1px solid var(--global-divider-color);
    border-radius: 18px;
    background: var(--global-bg-color);
    overflow: hidden;
  }

  .project-card-inner {
    display: grid;
    grid-template-columns: 300px 1fr;
    gap: 1.2rem;
    padding: 1rem;
  }

  .project-thumb {
    width: 100%;
    aspect-ratio: 1 / 1;
    display: flex;
    align-items: stretch;
  }

  .project-thumb-frame {
    
    width: 100%;
    aspect-ratio: 1 / 1;
    border: none;
    border-radius: 14px;
    overflow: hidden;
    background: #f7f7f7;
    box-shadow: 0 2px 8px rgba(0, 0, 0, 0.04);
  }

  .project-thumb-frame img {
    width: 100%;
    height: 100%;
    object-fit: contain;
    display: block;
  }

  .project-body {
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  .project-year {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.22rem;
  }

  .project-title {
    font-weight: 700;
    font-size: 1.02rem;
    line-height: 1.5;
    color: var(--global-text-color);
    margin-bottom: 0.32rem;
  }

  .project-funder {
    font-style: italic;
    line-height: 1.55;
    margin-bottom: 0.45rem;
    color: var(--global-text-color);
  }

  .project-meta {
    line-height: 1.65;
    margin-bottom: 0.7rem;
    color: var(--global-text-color);
  }

  .project-chips {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
    margin-bottom: 0.65rem;
  }

  .project-chip {
    display: inline-flex;
    align-items: center;
    padding: 0.22rem 0.55rem;
    border-radius: 999px;
    background: color-mix(in srgb, var(--global-divider-color) 20%, transparent 80%);
    color: #111;
    font-size: 0.82rem;
    line-height: 1.2;
  }

  .project-sdgs {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
    margin-bottom: 0.8rem;
  }

  .project-sdgs img {
    width: 34px;
    height: 34px;
    object-fit: contain;
    display: block;
  }

  .project-actions {
    display: flex;
    flex-wrap: wrap;
    gap: 0.5rem;
  }

  .project-action {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.38rem 0.75rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.88rem;
  }

  .project-action:hover {
    color: var(--global-theme-color);
  }

  .project-panel {
    display: none;
    padding: 0 1rem 1rem 1rem;
  }

  .project-panel.open {
    display: block;
  }

  .project-panel-card {
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: color-mix(in srgb, var(--global-bg-color) 92%, var(--global-theme-color) 8%);
    padding: 0.95rem 1rem;
    line-height: 1.72;
  }

  .project-output-group + .project-output-group {
    margin-top: 1rem;
    padding-top: 1rem;
    border-top: 1px solid color-mix(in srgb, var(--global-divider-color) 70%, transparent 30%);
  }

  .project-output-title {
    font-weight: 700;
    margin-bottom: 0.35rem;
  }

  .project-output-item {
    margin-bottom: 0.7rem;
    line-height: 1.68;
  }

  .project-output-item:last-child {
    margin-bottom: 0;
  }

  .project-simple {
    padding: 1rem 0;
    border-bottom: 1px solid color-mix(in srgb, var(--global-divider-color) 70%, transparent 30%);
  }

  .project-simple:last-child {
    border-bottom: none;
  }

  .project-simple .project-funder {
    margin-bottom: 0.35rem;
  }

  .project-empty {
    display: none;
    margin-top: 1rem;
    color: var(--global-text-color);
  }

  @media (max-width: 900px) {
    .project-card-inner {
      grid-template-columns: 1fr;
    }

    .project-thumb,
    .project-thumb-frame {
    
      min-height: 220px;
    }
  }

  .project-action.outputs { margin-left:auto; }

  .project-action.outputs {
    margin-left: auto !important;
    font-weight: 700 !important;
    color: var(--global-theme-color) !important;
  }

  .sdg-hover-tooltip{
    position: fixed;
    z-index: 9999;
    background: #111;
    color: #fff;
    padding: 5px 8px;
    border-radius: 6px;
    font-size: 0.78rem;
    line-height: 1.2;
    white-space: nowrap;
    pointer-events: none;
    opacity: 0;
    transform: translate(-50%, -8px);
    transition: opacity 0.08s ease;
  }

  .sdg-hover-tooltip.show{
    opacity: 1;
  }
</style>

<div class="section-card">
  <div class="project-controls">
    <button class="project-filter-toggle" type="button" id="projectFilterToggle">Filter</button>
    <div class="project-filter-panel" id="projectFilterPanel">
      <div class="filter-title">Filter projects</div>
      <div class="filter-subtitle">Showing <span id="projectVisibleCount">0</span> of <span id="projectTotalCount">0</span></div>

      <div class="filter-group">
        <div class="filter-group-title">Quick</div>
        <div class="filter-options">
          <label><input type="checkbox" value="all" id="projectFilterAll"> All <span class="count" id="projectCountAll">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Role</div>
        <div class="filter-options">
          <label><input type="checkbox" value="leader"> As a project leader <span class="count" id="projectCountLeader">(0)</span></label>
          <label><input type="checkbox" value="researcher"> As a researcher <span class="count" id="projectCountResearcher">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Project type</div>
        <div class="filter-options">
          <label><input type="checkbox" value="TÜBİTAK"> TÜBİTAK <span class="count" id="projectCountTubitak">(0)</span></label>
          <label><input type="checkbox" value="TAGEM"> TAGEM <span class="count" id="projectCountTagem">(0)</span></label>
          <label><input type="checkbox" value="AR-GE"> AR-GE <span class="count" id="projectCountArge">(0)</span></label>
          <label><input type="checkbox" value="COMU-BAP"> COMU-BAP <span class="count" id="projectCountComubap">(0)</span></label>
          <label><input type="checkbox" value="BAP"> BAP <span class="count" id="projectCountBap">(0)</span></label>
          <label><input type="checkbox" value="KUTUP-1001"> KUTUP-1001 <span class="count" id="projectCountKutup">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Topic</div>
        <div class="filter-options">
          <label><input type="checkbox" value="Aquaculture"> Aquaculture <span class="count" id="projectCountAquaculture">(0)</span></label>
          <label><input type="checkbox" value="Fisheries"> Fisheries <span class="count" id="projectCountFisheries">(0)</span></label>
          <label><input type="checkbox" value="Management"> Management <span class="count" id="projectCountManagement">(0)</span></label>
          <label><input type="checkbox" value="Genetics"> Genetics <span class="count" id="projectCountGenetics">(0)</span></label>
          <label><input type="checkbox" value="Biodiversity"> Biodiversity <span class="count" id="projectCountBiodiversity">(0)</span></label>
          <label><input type="checkbox" value="Polar Science"> Polar Science <span class="count" id="projectCountPolar">(0)</span></label>
          <label><input type="checkbox" value="Climate Change"> Climate Change <span class="count" id="projectCountClimate">(0)</span></label>
          <label><input type="checkbox" value="Biotechnology"> Biotechnology <span class="count" id="projectCountBiotech">(0)</span></label>
          <label><input type="checkbox" value="Seafood"> Seafood <span class="count" id="projectCountSeafood">(0)</span></label>
          <label><input type="checkbox" value="Water quality"> Water quality <span class="count" id="projectCountWater">(0)</span></label>
          <label><input type="checkbox" value="Fish Disease"> Fish Disease <span class="count" id="projectCountDisease">(0)</span></label>
        </div>
      </div>

      <div class="filter-actions">
        <button class="filter-btn" type="button" id="projectClearFilters">Clear</button>
        <button class="filter-btn" type="button" id="projectCloseFilters">Close</button>
      </div>
    </div>
  </div>

  <h2 class="section-title project-section-title" id="leaderTitle">As a Project Leader</h2>
  <div class="project-leader-list" id="leaderList">

    <div class="project-card project-entry" data-role="leader" data-tags="leader,TAGEM,AR-GE,Aquaculture,Seafood,Climate Change,Biotechnology">
      <div class="project-card-inner">
        <div class="project-thumb">
          <div class="project-thumb-frame">
            <img src="{{ '/assets/img/proje3.jpg' | relative_url }}" alt="Project image">
          </div>
        </div>
        <div class="project-body">
          <div class="project-year">2027–2030</div>
          <div class="project-title">Assessment of the Bioecological Characteristics of Oyster Species in the Changing Sea of Marmara Ecosystem and Evaluation of Marine Heatwave Impacts on Their Reproductive Biology</div>
          <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
          <div class="project-meta"><strong>Project Leader:</strong> Dr. Ekrem Cem Çankırılıgil<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
          <div class="project-chips">
            <span class="project-chip">TAGEM</span>
            <span class="project-chip">AR-GE</span>
            <span class="project-chip">Aquaculture</span>
            <span class="project-chip">Seafood</span>
            <span class="project-chip">Climate Change</span>
            <span class="project-chip">Biotechnology</span>
          </div>
          <div class="project-sdgs">
            <img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2">
            <img src="{{ '/assets/img/sdg6.png' | relative_url }}" alt="SDG 6">
            <img src="{{ '/assets/img/sdg12.png' | relative_url }}" alt="SDG 12">
            <img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13">
            <img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14">
          </div>
          <div class="project-actions">
            <button class="project-action" type="button" data-target="pl1a">Abstract</button>
            <button class="project-action" type="button" data-target="pl1b">Budget</button>
            <button class="project-action" type="button" data-target="pl1c">Team</button>
            <button class="project-action" type="button" data-target="pl1d">Collaborators</button>
          </div>
        </div>
      </div>
      <div class="project-panel" id="pl1a"><div class="project-panel-card">This project aims to comprehensively investigate the bioecological characteristics of European oyster (<em>Ostrea edulis</em>) and Pacific oyster (<em>Magallana gigas</em>) distributed in the Sea of Marmara, and to determine the effects of marine heatwaves on their reproductive biology. Within this scope, monthly sampling will be conducted at selected stations along the southern Marmara coasts, during which environmental parameters (temperature, salinity, dissolved oxygen, and nutrient concentrations) will be monitored. These data will be evaluated in relation to growth patterns and gonadal development. Meristic and morphometric measurements, condition indices, growth parameters, and fundamental population dynamic characteristics will be calculated for all collected individuals. In muscle and gonadal tissues, proximate composition, fatty acid profiles, amino acid composition, glycogen content, and lipid quality indices will be determined to reveal seasonal nutritional changes associated with reproductive cycles. To elucidate feeding ecology, stable isotope analyses will be performed, and Bayesian dietary models will be employed. Histological examinations of gonadal tissues will allow the seasonal progression of gonad development stages to be monitored, enabling the determination of reproductive periods and their relationships with environmental fluctuations. During the spawning season, mature individuals selected from the field will be used in controlled marine heatwave simulation experiments. Physiological and biochemical responses, including energy metabolites (ATP/ADP/AMP), glycogen levels, anaerobic end-products, and antioxidant enzyme activities, will be measured to assess the effects of thermal stress. Moreover, since thermal shock may trigger spawning in mature oysters, gamete release and gonad quality will be monitored to clarify the potential influence of heat stress on reproductive output.</div></div>
      <div class="project-panel" id="pl1b"><div class="project-panel-card">1.750.000 TL</div></div>
      <div class="project-panel" id="pl1c"><div class="project-panel-card">Prof. Dr. Umur Önal, Abdulkadir Yağcı, Dr. Öğr. Üyesi Güzin Gül, Dilara Bulut, Dr. Dalida Bedikoğlu, Tunç Özdemir, Hüseyin Bıçakcı, Sedat Küçükbaş, Assoc. Prof. Dr. Meral Apaydın Yağcı, Haşim İnceoğlu, Engin Kocabaş, Prof. Dr. İlknur Ak, Ayten Torun, Ramazan Aymaz</div></div>
      <div class="project-panel" id="pl1d"><div class="project-panel-card">Çanakkale Onsekiz Mart University, Istanbul University</div></div>
    </div>

    <div class="project-card project-entry" data-role="leader" data-tags="leader,TAGEM,AR-GE,Aquaculture,Seafood,Biotechnology">
      <div class="project-card-inner">
        <div class="project-thumb">
          <div class="project-thumb-frame">
            <img src="{{ '/assets/img/proje2.jpg' | relative_url }}" alt="Project image">
          </div>
        </div>
        <div class="project-body">
          <div class="project-year">2023–2026</div>
          <div class="project-title">Evaluation of Biochemical Composition, Feeding Ecology, Reproductive Characteristics and Spawning Techniques of Scallop Species</div>
          <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
          <div class="project-meta"><strong>Project Leader:</strong> Dr. Ekrem Cem Çankırılıgil<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
          <div class="project-chips">
            <span class="project-chip">TAGEM</span>
            <span class="project-chip">AR-GE</span>
            <span class="project-chip">Aquaculture</span>
            <span class="project-chip">Seafood</span>
            <span class="project-chip">Biotechnology</span>
          </div>
          <div class="project-sdgs">
            <img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2">
            <img src="{{ '/assets/img/sdg6.png' | relative_url }}" alt="SDG 6">
            <img src="{{ '/assets/img/sdg12.png' | relative_url }}" alt="SDG 12">
            <img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13">
            <img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14">
          </div>
          <div class="project-actions">
            <button class="project-action" type="button" data-target="pl2a">Abstract</button>
            <button class="project-action" type="button" data-target="pl2b">Budget</button>
            <button class="project-action" type="button" data-target="pl2c">Team</button>
            <button class="project-action" type="button" data-target="pl2d">Collaborators</button>
            <button class="project-action" type="button" data-target="pl2e" class="project-action outputs">View project outputs</button>
          </div>
        </div>
      </div>
      <div class="project-panel" id="pl2a"><div class="project-panel-card">This study will obtain fundamental biological data for scallop cultivation, which has high economic value in Türkiye and worldwide. In this context, scallops will be procured from five different regions of the Marmara Sea through monthly sampling. The basic population dynamic parameters, proximate composition, nutritional characteristics, gametogenic cycles, and environmental conditions of the scallops will be determined. First, the scallops’ condition indices and basic population parameters will be determined, and then the analyses will be performed. In order to determine changes in chemical composition, proximate composition (moisture, protein, fat, ash, carbohydrate), fatty acid composition, antioxidant activity, and total carotenoid amounts will be determined in muscle and gonad tissues. Elemental analyses will be performed in muscle, digestive sac, gill, and mantle tissues to determine toxic metal accumulations, a crucial risk in bivalves. Nutritional characteristics will be determined by both stable isotope analysis and modelling of fatty acid groups. The histologically determined gametogenic cycles (reproductive period) of scallops will be associated with seawater nutrient composition and physicochemical properties. After the breeding period of the scallops has been determined, mature individuals will be procured from suitable stations and used in breeding studies. Different techniques (physical and thermal shock) will be applied in reproductive studies, and the quality parameters and fertilization rates of the obtained gametes will be determined. With the project results, fundamental data about this species, which has excellent potential for the aquaculture sector, will be revealed.</div></div>
      <div class="project-panel" id="pl2b"><div class="project-panel-card">400.000 TL</div></div>
      <div class="project-panel" id="pl2c"><div class="project-panel-card">Alpaslan Kara, Haşim İnceoğlu, Engin Kocabaş, Abdulkadir Yağcı, Assoc. Prof. Dr. Meral Apaydin Yağcı, Dr. Cemal Dayanıklı, Prof. Dr. Umur Önal, Prof. Dr. Nermin Berik, Dr. Güzin Gül, Prof. Dr. İlknur Ak, Prof. Dr. Gülen Türker, Dr. Yaprak Gürkan, Sefa Marangoz, Dilara Bulut, Tunç Özdemir, Hüseyin Bıçakcı, Sedat Küçükbaş, Gülşen Akıncı</div></div>
      <div class="project-panel" id="pl2d"><div class="project-panel-card">Çanakkale Onsekiz Mart University, Istanbul University</div></div>
      <div class="project-panel" id="pl2e"><div class="project-panel-card"><div class="project-output-group"><div class="project-output-title">Papers</div><div class="project-output-item">2022 — Veske E., Çankırılıgil E.C., Yavuzcan Yıldız H., <em>Seasonal Proximate Composition, Amino Acid and Trace Metal Contents of the Great Mediterranean scallop (Pecten jacobaeus) Collected from the Gulf of Antalya</em>, <em>Journal of Anatolian Environmental and Animal Sciences</em>, 7(3):358–366.</div></div></div></div>
    </div>

    <div class="project-card project-entry" data-role="leader" data-tags="leader,TÜBİTAK,KUTUP-1001,AR-GE,Polar Science,Climate Change,Biodiversity">
      <div class="project-card-inner">
        <div class="project-thumb">
          <div class="project-thumb-frame">
            <img src="{{ '/assets/img/proje1.jpg' | relative_url }}" alt="Project image">
          </div>
        </div>
        <div class="project-body">
          <div class="project-year">2022–2024</div>
          <div class="project-title">Biological Activity Evaluation of Macroalgae Distributed on Horseshoe Island (Antarctica) Coasts by Determining Nutrient Composition and Phytochemical Contents</div>
          <div class="project-funder">Supported by Presidency of the Republic of Türkiye, the Ministry of Industry and Technology, and TÜBİTAK MAM Polar Research Institute</div>
          <div class="project-meta"><strong>Project Leader:</strong> Dr. Ekrem Cem Çankırılıgil<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
          <div class="project-chips">
            <span class="project-chip">TÜBİTAK</span>
            <span class="project-chip">KUTUP-1001</span>
            <span class="project-chip">AR-GE</span>
            <span class="project-chip">Polar Science</span>
            <span class="project-chip">Climate Change</span>
            <span class="project-chip">Biodiversity</span>
            <span class="project-chip">Marine Natural Products Chemistry</span>
          </div>
          <div class="project-sdgs">
            <img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2">
            <img src="{{ '/assets/img/sdg6.png' | relative_url }}" alt="SDG 6">
            <img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13">
            <img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14">
          </div>
          <div class="project-actions">
            <button class="project-action" type="button" data-target="pl3a">Abstract</button>
            <button class="project-action" type="button" data-target="pl3b">Budget</button>
            <button class="project-action" type="button" data-target="pl3c">Team</button>
            <button class="project-action" type="button" data-target="pl3d">Collaborators</button>
            <button class="project-action" type="button" data-target="pl3e" class="project-action outputs">View project outputs</button>
          </div>
        </div>
      </div>
      <div class="project-panel" id="pl3a"><div class="project-panel-card">In this project, the distribution of macroalgae species on Horseshoe Island, Antarctica, was determined and their biological activities and various characteristics were investigated in detail. Our study analysed red, brown, and green macroalgae species and determined the nutrient composition, fatty acid and amino acid contents, and phenolic substance composition of these species. In addition, antioxidant, anti-inflammatory, antidiabetic, anti-Alzheimer, and antimicrobial activities of algae were also evaluated. Our analyses revealed that all algal species were within safe limits in terms of macro and micro elements. Especially <em>Urospora penicilliformis</em> attracted attention with its high crude protein and fat values. In terms of protein quality, the highest DIAAS scores were obtained from red algae, and especially green algae stood out with high PUFA amounts. While antioxidant activity was found to be high in most of the algae, antidiabetic activity in green algae and activity against Alzheimer’s disease in brown and red algae were at remarkable levels. Especially the alcohol extract of <em>Ulva intestinalis</em> showed effective antimicrobial activity against <em>Staphylococcus aureus</em>, which is considered an important finding in the search for alternative treatment methods. Our study is the first research on macroalgae populations on Horseshoe Island and provides an important starting point for the conservation and understanding of the island’s biodiversity.</div></div>
      <div class="project-panel" id="pl3b"><div class="project-panel-card">1.200.000 TL</div></div>
      <div class="project-panel" id="pl3c"><div class="project-panel-card">Prof. Dr. İlknur Ak, Prof. Dr. Gülen Türker, Dr. Alpaslan Kara, Dr. Erdinç Veske, Assoc. Prof. Dr. Meral Apaydın Yağcı, Engin Kocabaş, Prof. Dr. Nermin Berik</div></div>
      <div class="project-panel" id="pl3d"><div class="project-panel-card">Çanakkale Onsekiz Mart University</div></div>
      <div class="project-panel" id="pl3e">
        <div class="project-panel-card">
          <div class="project-output-group">
            <div class="project-output-title">Papers</div>
            <div class="project-output-item">2026 — Ak İ., Çankırılıgil E. C., <em>Biodiversity and Distribution Patterns of Benthic Macroalgae on Horseshoe Island, Antarctica, with New Records</em>, <em>Polar Biology</em>, 49(13).</div>
          </div>
          <div class="project-output-group">
            <div class="project-output-title">Presentations</div>
            <div class="project-output-item">2025 — Çankırılıgil E.C., Ak İ., <em>Antarktika Makroalgleri ve İklim Değişikliği: Horseshoe Adası Örneği</em>. National Polar Sciences Symposium, 5–6 November 2025, İzmir, Türkiye, Oral presentation.</div>
            <div class="project-output-item">2024 — Çankırılıgil E.C., Ak İ., Türker G., Berik N., <em>Profiling Chemical Components of Seaweed Species from the Antarctic Peninsula</em>. 8th National Polar Sciences Symposium, 8 November 2024, Kocaeli, Türkiye, Oral presentation.</div>
            <div class="project-output-item">2024 — Çankırılıgil E.C., Ak İ., Apaydın Yağcı M., Türker G., Kara A., Veske E., Kocabaş E., Berik N., <em>Snapshots of Marine Life at Horseshoe Island, Antarctica: Highlights from Underwater Observations and Specimen Collections</em>. 8th National Polar Sciences Symposium, 8 November 2024, Kocaeli, Türkiye, Poster presentation.</div>
            <div class="project-output-item">2024 — Ak İ., Çankırılıgil E.C., <em>Observations on the Diversity of Benthic Macroalgae Along the Shores of Horseshoe Island, Antarctica</em>. 8th National Polar Sciences Symposium, 8 November 2024, Gebze, Kocaeli, Türkiye, Poster presentation.</div>
            <div class="project-output-item">2023 — Çankırılıgil E.C., Ak İ., Türker G., Kara A., Veske E., Apaydın Yağcı M., Kocabaş E., Berik N., <em>Antarktika Horseshoe Adası Makroalgleri: Yedinci Ulusal Antarktika Bilim Seferi Kapsamında Yapılan Çalışmalar</em>. 7th National Polar Sciences Symposium, 4 December 2023, İstanbul, Türkiye, Oral presentation.</div>
          </div>
          <div class="project-output-group">
            <div class="project-output-title">Other presentations</div>
            <div class="project-output-item">2024 — Çankırılıgil E.C., <em>Marine Life in Antarctica</em>. Maltepe Kadir Has Science and Art Center, Student Seminar, 9 November 2024, İstanbul, Türkiye.</div>
            <div class="project-output-item">2023 — Çankırılıgil E.C., <em>Algae in Extreme Climate Conditions: The Case of Horseshoe Island</em>. Horseshoe Island and Glacial Lakes Biodiversity Workshop, 5–6 December 2023, Erzurum, Türkiye.</div>
            <div class="project-output-item">2023 — Çankırılıgil E.C., <em>7th National Turkish Antarctic Expedition</em>. T.C. Ministry of Agriculture and Forestry, I. Regional Group Meeting, July 2023, Yalova, Türkiye.</div>
            <div class="project-output-item">2023 — Çankırılıgil E.C., <em>Studies Carried Out in the 7th National Turkish Antarctic Expedition</em>. Career Talks in ÇOMÜ Faculty of Marine Sciences and Technology, June 2023, Çanakkale, Türkiye.</div>
          </div>
        </div>
      </div>
    </div>

  </div>

  <h2 class="section-title project-section-title" id="researcherTitle">As a Researcher</h2>
  <div class="project-researcher-list" id="researcherList">

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Fisheries,Management">
      <div class="project-year">2027–2030</div>
      <div class="project-title">GEN-KARADENİZ: Küçük Pelajik Türlerde Genetik Yaklaşımlı İzleme Altyapısının Oluşturulması</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Zehra Duygu Düzgüneş<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Fisheries</span><span class="project-chip">Management</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture">
      <div class="project-year">2027–2030</div>
      <div class="project-title">Determination of Maintenance and Growth Requirements in Black Sea Salmon (<em>Salmo labrax</em>) Using a Factorial Approach</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Osman Tolga Özel<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,BAP,AR-GE,Aquaculture">
      <div class="project-year">2026–2027</div>
      <div class="project-title">Yavru (Fingerling) Karaca Mersin (<em>Acipenser gueldenstaedtii</em>) Balıklarında Protein İhtiyaçlarının Belirlenmesi Üzerine Bir Araştırma</div>
      <div class="project-funder">Supported by Çukurova University, BAP</div>
      <div class="project-meta"><strong>Project Leader:</strong> Prof. Dr. Oğuz Taşbozan<br><strong>Executive Organization:</strong> Çukurova University, The Faculty of Fisheries</div>
      <div class="project-chips"><span class="project-chip">BAP</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TÜBİTAK,KUTUP-1001,AR-GE,Polar Science">
      <div class="project-year">2026–2028</div>
      <div class="project-title">Determining the Marine Connectivity Between Dominant Predator and Prey Groups in Horseshoe Island, Antarctica, Using eDNA, Visual Observations, and Deep Learning-Based Image Analysis</div>
      <div class="project-funder">Supported by Presidency of the Republic of Türkiye, the Ministry of Industry and Technology, and TÜBİTAK MAM Polar Research Institute</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Merve Karakuş<br><strong>Executive Organization:</strong> Mediterranean Fisheries Research, Production and Training Institute</div>
      <div class="project-chips"><span class="project-chip">TÜBİTAK</span><span class="project-chip">KUTUP-1001</span><span class="project-chip">AR-GE</span><span class="project-chip">Polar Science</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg6.png' | relative_url }}" alt="SDG 6"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture">
      <div class="project-year">2026–2029</div>
      <div class="project-title">Development of Aquaculture Techniques and Feeding Strategies for Freshwater Mullet (<em>Squalius lepidus</em>) Using a Factorial Model</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Ali Atilla Uslu<br><strong>Executive Organization:</strong> Elazığ Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Fisheries,Biodiversity">
      <div class="project-year">2024–2027</div>
      <div class="project-title">Determination of Ichthyoplankton Composition in the Gulf of Edremit and Macrozoobenthic Biodiversity in Artificial Reef Areas</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Alpaslan Kara<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Fisheries</span><span class="project-chip">Biodiversity</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Fisheries,Management">
      <div class="project-year">2023–2026</div>
      <div class="project-title">Transition to Ecosystem-Based Fisheries Management in the Sea of Marmara and Preparation of a Fisheries Management Plan</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Alpaslan Kara<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Fisheries</span><span class="project-chip">Management</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg11.png' | relative_url }}" alt="SDG 11"><img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Fish Disease,Aquaculture">
      <div class="project-year">2023–2027</div>
      <div class="project-title">Development of a Combined Vaccine Against Vibriosis and Photobacteriosis (Pasteurellosis) in Sea Bass under GMP Standards</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Ahmet Demir<br><strong>Executive Organization:</strong> ATAFEN</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">TAGEM AR-GE</span><span class="project-chip">AR-GE</span><span class="project-chip">Fish Disease</span><span class="project-chip">Aquaculture</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Biodiversity">
      <div class="project-year">2022–2024</div>
      <div class="project-title">Biotechnological Material Production from an Invasive Species, Zebra Mussel (<em>Dreissena polymorpha</em> (Pallas, 1771))</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Assoc. Dr. Meral Apaydın Yağcı<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Biodiversity</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"><img src="{{ '/assets/img/sdg15.png' | relative_url }}" alt="SDG 15"></div>
      <div class="project-actions"><button class="project-action" type="button" data-target="rs1" class="project-action outputs">View project outputs</button></div>
      <div class="project-panel" id="rs1"><div class="project-panel-card"><div class="project-output-group"><div class="project-output-title">Presentations</div><div class="project-output-item">2025 — Apaydın Yağcı M., Yağcı A., Çankırılıgil E. C., Kocabaş E., <em>A Preliminary Study on the Zooplankton Fauna of Gölbaşı Lake (Bursa/Kestel – Türkiye)</em>. The XVII International Rotifer Symposium, 4–8 August 2025, Rio de Janeiro, Brazil, Poster presentation.</div></div></div></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Water quality">
      <div class="project-year">2021–2022</div>
      <div class="project-title">The Effect of Mucilage on the Marmara Ecosystem</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Engin Kocabaş<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Water quality</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg6.png' | relative_url }}" alt="SDG 6"><img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Fisheries">
      <div class="project-year">2020–2022</div>
      <div class="project-title">Research on the Reduction of Bycatch in Shrimp Fisheries by Beam Trawl in the Sea of Marmara</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Haşim İnceoğlu<br><strong>Executive Organization:</strong> Sheep Breeding Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Fisheries</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture">
      <div class="project-year">2020–2022</div>
      <div class="project-title">Black Soldier Fly (<em>Hermetia illucens</em>, L.) and Mealworm (<em>Tenebrio molitor</em>, L.) Larvae Usage on Fish Feed Instead of Fish Meal and Effects on Growth Parameters, Amino Acid and Fatty Acid Compositions in Rainbow Trout (<em>Oncorhynchus mykiss</em>)</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Nedim Örnekçi<br><strong>Executive Organization:</strong> Elazığ Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
      <div class="project-actions"><button class="project-action" type="button" data-target="rs2" class="project-action outputs">View project outputs</button></div>
      <div class="project-panel" id="rs2"><div class="project-panel-card"><div class="project-output-group"><div class="project-output-title">Papers</div><div class="project-output-item">2023 — Uslu, A.A., Özel, O.T., Örnekçi, G.N., Çelik, B., Çankırılıgil, E.C., Çoşkun, İ., Uslu Şenel, G., <em>Insect Larval Meal as a Possible Alternative to Fish Meal in Rainbow Trout (Oncorhynchus mykiss) diets: Black Soldier Fly (Hermetia illucens), Mealworm (Tenebrio molitor)</em>, <em>Journal of Limnology and Freshwater Fisheries Research</em>, 9(1):43–52.</div></div><div class="project-output-group"><div class="project-output-title">Presentations</div><div class="project-output-item">2021 — Uslu A.A., Özel O.T., Çelik B., Çankırılıgil E.C., Çoşkun İ., <em>Fish Meal Replacement by Mealworm (Tenebrio molitor) Larvae Meal in Diets for Rainbow Trout (Oncorhynchus mykiss)</em>. FABA 2021, International Symposium on Fisheries and Aquatic Sciences, 7–8 September 2021, İzmir, Türkiye, Oral presentation.</div><div class="project-output-item">2021 — Uslu A.A., Özel O.T., Örnekçi N., Çankırılıgil E.C., Çoşkun İ., Şenel G.U., <em>Black Soldier Fly (Hermetia illucens) Prepupae Meal as a Possible Alternative to Fish Meal in Rainbow Trout (Oncorhynchus mykiss) Diets</em>. TURFAJ 2021, 2nd International Congress of the Turkish Journal of Agriculture - Food Science and Technology, October 2021, Gazimağusa, Oral presentation.</div></div></div></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture,Seafood">
      <div class="project-year">2017–2021</div>
      <div class="project-title">A Research on the Possibilities of Using Some Phytobiotic-Containing Diets in Black Sea Trout (<em>Salmo trutta labrax</em> Pallas, 1811) Nutrition</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Osman Tolga Özel<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span><span class="project-chip">Seafood</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
      <div class="project-actions"><button class="project-action" type="button" data-target="rs3" class="project-action outputs">View project outputs</button></div>
      <div class="project-panel" id="rs3">
        <div class="project-panel-card">
          <div class="project-output-group">
            <div class="project-output-title">Papers</div>
            <div class="project-output-item">2025 — Çankırılıgil E. C., Berik N., <em>Unlocking the Nutritional Potential of Endemic Salmonid Species (Black Sea Salmon, Salmo labrax): Carotenoids and Their Impact on Fillet Characteristics</em>, <em>Turkish Journal of Fisheries and Aquatic Sciences</em>, 25(12), 27539.</div>
            <div class="project-output-item">2023 — Özel O.T., Çankırılıgil E.C., Ertürk-Gürkan S., Coşkun İ., Türe M., <em>Influence of Laurel (Laurus nobilis) Essential Oil on Gut Function of Black Sea Salmon (Salmo labrax) Juveniles</em>, <em>Tropical Animal Health and Production</em>, 54(6):390.</div>
            <div class="project-output-item">2022 — Çankırılıgil E.C., Berik N., Çakmak E., Özel O.T., Alp-Erbay E., <em>Dietary Carotenoids Influence Growth, Fillet Pigmentation, and Quality Characteristics of Black Sea Trout (Salmo labrax Pallas, 1814)</em>, <em>Thalassas: An International Journal of Marine Sciences</em>, 38:793–809.</div>
            <div class="project-output-item">2020 — Çankırılıgil E.C., Berik N., Alp Erbay E., <em>Optimization of Hydrolization Procedure for Amino Acid Analysis in Fish Meat with HPLC-DAD by Response Surface Methodology (RSM)</em>, <em>Ege Journal of Fisheries and Aquatic Sciences</em>, 37(2):113–123.</div>
            <div class="project-output-item">2020 — Çankırılıgil E.C., Berik N., <em>Chemical Composition of the Black Sea Trout (Salmo labrax Pallas, 1814): A Comparative Study</em>, <em>Aquatic Research</em>, 3(4):208–219.</div>
            <div class="project-output-item">2020 — Kasapoglu N., Çankırılıgil E.C., Çakmak E., Özel O. T., <em>Meristic and Morphometric Characteristics of the Black Sea Salmon, Salmo labrax Pallas, 1814 Culture Line: An Endemic Species for Eastern Black Sea</em>, <em>Journal of Fisheries</em>, 8(3):935–939.</div>
            <div class="project-output-item">2018 — Özel O.T., Çakmak E., Çoşkun İ., Çankırılıgil E.C., <em>Evaluation of Growth Performance and Intestine Villi Morphology of Black Sea Trout (Salmo trutta labrax) Fed with Different Protein Levels Containing Diets</em>, <em>Ege Journal of Fisheries and Aquatic Sciences</em>, 35(2):125–130.</div>
          </div>
          <div class="project-output-group">
            <div class="project-output-title">Presentations</div>
            <div class="project-output-item">2019 — Çankırılıgil E.C., Berik N., <em>Effects of Astaxanthine, Canthaxanthin and Lycopene Containing Diets on the Chemical Quality and Textural Properties of the Black Sea Trout (Salmo labrax) Fillets</em>. BioEco2019 International Biodiversity & Ecology Sciences Symposium, 26–28 September 2019, Istanbul, Türkiye, Oral presentation.</div>
            <div class="project-output-item">2019 — Çankırılıgil E.C., Berik N., <em>Histological Examination of Black Sea Trout (Salmo labrax) Fed by Carotenoid Containing Diets</em>. BioEco2019 International Biodiversity & Ecology Sciences Symposium, 26–28 September 2019, Istanbul, Türkiye, Poster presentation.</div>
            <div class="project-output-item">2018 — Ozel O., Türe M., Cakmak E., Cimagil R., Çankırılıgil E.C., Kutlu İ., <em>Effects of Dietary Daphne (Laurus nobilis L.) and Fennel (Foeniculum vulgare L.) Essential Oils on Some Intestinal Bacteria of Black Sea Trout (Salmo labrax)</em>. 4th International Agriculture Congress, 5–8 July 2018, Kırşehir, Türkiye, Oral presentation.</div>
            <div class="project-output-item">2017 — Çankırılıgil E.C., Berik N., <em>Amino Acid Composition of Cultured Black Sea Trout (Salmo trutta labrax PALLAS, 1811)</em>. SEAB 2017, International Symposium on EuroAsian Biodiversity, 5–8 July 2017, Minsk, Belarus, Oral presentation.</div>
            <div class="project-output-item">2017 — Çankırılıgil E.C., Çakmak E., Özel O.T., Kasapoğlu N., <em>Black Sea Trout (Salmo trutta labrax PALLAS, 1811) Culture in Turkey and Morphometric Characteristics of Fifth Culture Generation</em>. SEAB 2017, International Symposium on EuroAsian Biodiversity, 5–8 July 2017, Minsk, Belarus, Oral presentation.</div>
          </div>
        </div>
      </div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture,Biotechnology">
      <div class="project-year">2017–2021</div>
      <div class="project-title">Determination of the Success of Using Cryopreserved Sperm (Artificial Insemination) in Rainbow Trout (<em>Oncorhynchus mykiss</em>) Aquaculture</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Atife Tuba Beken<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span><span class="project-chip">Biotechnology</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Water quality">
      <div class="project-year">2020–2021</div>
      <div class="project-title">Determination of Water Quality and Carrying Capacity of Deriner Dam Lake</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dilek Fidan<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Water quality</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg6.png' | relative_url }}" alt="SDG 6"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,Management">
      <div class="project-year">2020</div>
      <div class="project-title">Conventionalization of Black Sea Trout (<em>Salmo labrax</em>) Culture</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Eyüp Çakmak<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">Training</span><span class="project-chip">Management</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg8.png' | relative_url }}" alt="SDG 8"><img src="{{ '/assets/img/sdg9.png' | relative_url }}" alt="SDG 9"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture,Seafood">
      <div class="project-year">2015–2019</div>
      <div class="project-title">Determination of the Bioecology and Aquaculture Characteristics of the Mullet Species (<em>Mugil cephalus</em>, <em>Liza aurata</em>) in the Eastern Black Sea</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Ayça Altuntaş<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span><span class="project-chip">Seafood</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg13.png' | relative_url }}" alt="SDG 13"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
      <div class="project-actions"><button class="project-action" type="button" data-target="rs4" class="project-action outputs">View project outputs</button></div>
      <div class="project-panel" id="rs4"><div class="project-panel-card"><div class="project-output-group"><div class="project-output-title">Papers</div><div class="project-output-item">2024 — Çankırılıgil E.C., Altuntaş A., <em>Chemical Composition of Two Grey Mullet Species (Chelon auratus, Mugil cephalus): A Comparative Study on Wild and Aquaculture-Adapted Species</em>, <em>Çanakkale Onsekiz Mart University Journal of Marine Sciences and Fisheries</em>, 7(1):52–66.</div></div><div class="project-output-group"><div class="project-output-title">Presentations</div><div class="project-output-item">2017 — Çankırılıgil E.C., Güven A., Balçık Mısır G., <em>Kültüre Alınan Altınbaş Kefalin (Liza aurata) Kas Dokusu ve Atıklarının Amino Asit Kompozisyonunun Belirlenmesi</em>. 19th National Fisheries Symposium, 12–15 September 2017, Sinop, Türkiye, Poster presentation.</div><div class="project-output-item">2017 — Kasapoğlu N., Güven A., Çakmak E., Çankırılıgil E.C., Firidin Ş., <em>Karadeniz Kefal Avcılığında Hedef Dışı Av Oranları</em>. 19th National Fisheries Symposium, 12–15 September 2017, Sinop, Türkiye, Poster presentation.</div></div></div></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture">
      <div class="project-year">2015–2017</div>
      <div class="project-title">Broodstock Management in Sturgeon Breeding</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Bilal Akbulut<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Genetics,Biodiversity">
      <div class="project-year">2014–2016</div>
      <div class="project-title">Analysis of the Genetic Structure of Brown Trout (<em>Salmo trutta</em> L.) Population in Turkey Using Microsatellite DNA and mtDNA Markers</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Dr. Oğuzhan Eroğlu<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Genetics</span><span class="project-chip">Biodiversity</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
      <div class="project-actions"><button class="project-action" type="button" data-target="rs5" class="project-action outputs">View project outputs</button></div>
      <div class="project-panel" id="rs5"><div class="project-panel-card"><div class="project-output-group"><div class="project-output-title">Papers</div><div class="project-output-item">2019 — Çakmak E., Çankırılıgil E.C., Düzgüneş Z.D., Özel O.T., Eroğlu O., Firidin Ş., <em>Triploid Black Sea Trout (Salmo labrax Pallas, 1814) Induced by Heat Shock and Evaluation of Triploidy with Different Techniques</em>, <em>Genetics of Aquatic Organisms (GenAqua)</em>, 3(1):01–07.</div></div></div></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,TAGEM,AR-GE,Aquaculture">
      <div class="project-year">2013–2015</div>
      <div class="project-title">Nutritional Requirements of Black Sea Trout (<em>Salmo trutta labrax</em>)</div>
      <div class="project-funder">Supported by Republic of Türkiye, Ministry of Agriculture and Forestry, General Directorate of Agricultural Research and Policies (TAGEM)</div>
      <div class="project-meta"><strong>Project Leader:</strong> Eyüp Çakmak<br><strong>Executive Organization:</strong> Central Fisheries Research Institute</div>
      <div class="project-chips"><span class="project-chip">TAGEM</span><span class="project-chip">AR-GE</span><span class="project-chip">Aquaculture</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
      <div class="project-actions"><button class="project-action" type="button" data-target="rs6" class="project-action outputs">View project outputs</button></div>
      <div class="project-panel" id="rs6"><div class="project-panel-card"><div class="project-output-group"><div class="project-output-title">Papers</div><div class="project-output-item">2023 — Özel O.T., Çakmak E., Çankırılıgil E.C., Düzgüneş Z.D., Çimagil R., Batır E., <em>Comparison of reproductive performance of Black Sea salmon broodstock (Salmo labrax PALLAS, 1814) reaching first sexual maturity at different ages</em>, <em>Ege Journal of Fisheries</em>, 40(3):166–173.</div><div class="project-output-item">2023 — Özel O.T., Çakmak E., Çankırılıgil E.C., Çimagil R., Düzgüneş Z.D., <em>Reproductive Performance of Hatchery-Originated Black Sea Salmon Broodstocks' (Salmo labrax PALLAS, 1814) F5 and F6 Filial Generations</em>, <em>Acta Aquatica Turcica</em>, 40(3):166–173.</div><div class="project-output-item">2022 — Çakmak E., Firidin Ş., Aksungur N., Çavdar Y., Kurtoğlu İ.Z., Aksungur M., Özel O.T., Çankırılıgil E.C., Düzgüneş Z.D., Esin B., <em>Improving Reproductive Yield of the Black Sea Salmon (Salmo labrax PALLAS, 1814) with a Selective Breeding Program</em>, <em>Aquatic Sciences and Engineering</em>, 37(3):161–168.</div></div><div class="project-output-group"><div class="project-output-title">Presentations</div><div class="project-output-item">2022 — Özel O.T., Çakmak E., Çankırılıgil E.C., Düzgüneş Z.D., Çimagil R., <em>Farklı Yaşlarda Cinsel Olgunluğa Ulaşan Karadeniz Somonu Anaçlarının (Salmo labrax PALLAS, 1811) Üreme Performansı</em>. 6th National Trout Symposium, 15–16 September 2022, Isparta, Türkiye, Oral presentation.</div><div class="project-output-item">2022 — Özel O.T., Çakmak E., Çankırılıgil E.C., Çimagil R., Düzgüneş Z.D., <em>Kuluçkahane Kökenli F5 ve F6 Nesil Karadeniz Somonu Anaçlarının (Salmo labrax PALLAS, 1811) Üreme Performansı İlişkisi</em>. 6th National Trout Symposium, 15–16 September 2022, Isparta, Türkiye, Oral presentation.</div><div class="project-output-item">2016 — Çankırılıgil E.C., Çakmak E., Özcan Akpınar İ., <em>Histological Development of the Digestive Tract of Black Sea Trout (Salmo trutta labrax PALLAS, 1811) During Larval Ontogeny</em>. 41st CIESM Congress, Living Resources & Marine Ecosystems Committee, 12–16 September 2016, Kiel, Germany, Full-text.</div><div class="project-output-item">2016 — Kasapoğlu N., Çakmak E., Çankırılıgil E.C., <em>Differences Between Cultured and Wild Black Sea Trout (Salmo trutta labrax) Otoliths: A Comparative Study</em>. 41st CIESM Congress, Living Resources & Marine Ecosystems Committee, 12–16 September 2016, Kiel, Germany, Full-text.</div></div></div></div>
    </div>

    <div class="project-simple project-entry" data-role="researcher" data-tags="researcher,COMU-BAP,BAP,AR-GE,Seafood">
      <div class="project-year">2010–2012</div>
      <div class="project-title">Determination of Quality Parameters of Coated Products (Croquettes) Obtained from Different Seafood</div>
      <div class="project-funder">Supported by Çanakkale Onsekiz Mart University, COMU-BAP</div>
      <div class="project-meta"><strong>Project Leader:</strong> Prof. Dr. Nermin Berik<br><strong>Executive Organization:</strong> Çanakkale Onsekiz Mart University, Marine Sciences and Technology Faculty</div>
      <div class="project-chips"><span class="project-chip">COMU</span><span class="project-chip">COMU-BAP</span><span class="project-chip">BAP</span><span class="project-chip">AR-GE</span><span class="project-chip">Seafood</span></div>
      <div class="project-sdgs"><img src="{{ '/assets/img/sdg2.png' | relative_url }}" alt="SDG 2"><img src="{{ '/assets/img/sdg14.png' | relative_url }}" alt="SDG 14"></div>
      <div class="project-actions"><button class="project-action" type="button" data-target="rs7" class="project-action outputs">View project outputs</button></div>
      <div class="project-panel" id="rs7">
        <div class="project-panel-card">
          <div class="project-output-group">
            <div class="project-output-title">Papers</div>
            <div class="project-output-item">2018 — Çankırılıgil E.C., Berik N., <em>Sensorial Evaluation of Fish Croquettes Produced from Different Seafood</em>, <em>Aquatic Sciences and Engineering</em>, 3(3):96–101.</div>
            <div class="project-output-item">2018 — Çakmak E., Çankırılıgil E.C., Özel, O.T., <em>The Fifth Culture Generation of Black Sea Trout (Salmo trutta labrax): Culture Characteristics, Meat Yield and Proximate Composition</em>, <em>Ege Journal of Fisheries and Aquatic Sciences</em>, 35(1):103–110.</div>
            <div class="project-output-item">2017 — Çankırılıgil E.C., Berik N., <em>Effects of Deep-Frying to Sardine Croquettes’ Chemical Composition</em>, <em>Ege Journal of Fisheries and Aquatic Sciences</em>, 34(3):293–302.</div>
            <div class="project-output-item">2017 — Çankırılıgil E.C., Berik N., <em>Gökkuşağı Alabalığı (Oncorhynchus mykiss) Kroketlerinin Soğuk Muhafazada (+4°C) Raf Ömrünün Belirlenmesi</em>, <em>Turkish Journal of Aquatic Sciences</em>, 32:35–48.</div>
            <div class="project-output-item">2017 — Çankırılıgil E.C., Berik N., <em>Changes in Fatty Acid and Mineral Compositions of Rose-Shrimp Croquettes during Production Process</em>, <em>American Journal of Food Technology</em>, 12(4):254–261.</div>
            <div class="project-output-item">2011 — Berik N., Çankırılıgil E.C., Kahraman D., <em>Determination of Quality Attributes and Production of Fingers from Rainbow Trout (Oncorhynchus mykiss) Fillet</em>, <em>Kafkas Univ Vet Fak Derg</em>, 17:735–740.</div>
          </div>
          <div class="project-output-group">
            <div class="project-output-title">Presentations</div>
            <div class="project-output-item">2017 — Çankırılıgil E.C., Berik N., <em>Element Composition of Farmed Rainbow Trout (Oncorhynchus mykiss) Obtained from Fish Farm in the Mount Ida</em>. ISEEP-2017 VIII International Symposium on Ecology and Environmental Problems, 4–7 October 2017, Çanakkale, Türkiye, Poster presentation.</div>
            <div class="project-output-item">2017 — Çankırılıgil E.C., Berik N., <em>Farklı Su Ürünlerinden Elde Edilen Kaplama Ürünlerin Duyusal Özelliklerinin Belirlenmesi</em>. 19th National Fisheries Symposium, 12–15 September 2017, Sinop, Türkiye, Poster presentation.</div>
            <div class="project-output-item">2016 — Çankırılıgil E.C., Berik N., <em>Changes in Fatty Acid and Mineral Compositions of Rose-Shrimp Croquettes during Production Process</em>. 63rd Scientific Conference with International Participation “Food Science, Engineering and Technology 2016”, 21–22 October 2016, Plovdiv, Bulgaria, Oral presentation.</div>
            <div class="project-output-item">2012 — Çankırılıgil E.C., Berik N., <em>Production of Croquettes from Deep-Water Rose Shrimp (Parapenaeus longirostris) Meat</em>. Turkish-Japanese Marine Forum, Harmonization of Biodiversity and Marine Industries Symposium, 9–12 November 2012, Çanakkale, Türkiye, Poster presentation.</div>
            <div class="project-output-item">2013 — Çankırılıgil E.C., Berik N., <em>Gökkuşağı Alabalığı (Oncorhynchus mykiss) Kroketlerinin Soğuk Muhafazada (+4ºC) Raf Ömrünün Belirlenmesi</em>. 17th National Fisheries Symposium, 3–6 September 2013, İstanbul, Türkiye, Poster presentation.</div>
            <div class="project-output-item">2010 — Berik N., Çankırılıgil E.C., Kahraman D., <em>Alabalık (Oncorhynchus mykiss) Eti Kullanılarak Hazırlanan Kroketlerin Besin Bileşimi ve Duyusal Analizleri Açısından İncelenmesi</em>. 2nd National Trout Symposium, 6–8 July 2010, Karaman, Türkiye, Poster presentation.</div>
          </div>
        </div>
      </div>
    </div>

  </div>

  <p class="project-empty" id="projectEmpty">No projects match the selected filters.</p>
</div>

<script>
(function () {
  const filterToggle = document.getElementById('projectFilterToggle');
  const filterPanel = document.getElementById('projectFilterPanel');
  const closeFilters = document.getElementById('projectCloseFilters');
  const clearFilters = document.getElementById('projectClearFilters');
  const filterAll = document.getElementById('projectFilterAll');
  const visibleCount = document.getElementById('projectVisibleCount');
  const totalCount = document.getElementById('projectTotalCount');
  const emptyMsg = document.getElementById('projectEmpty');
  const leaderTitle = document.getElementById('leaderTitle');
  const researcherTitle = document.getElementById('researcherTitle');
  const leaderList = document.getElementById('leaderList');
  const researcherList = document.getElementById('researcherList');

  const countMap = {
    all: document.getElementById('projectCountAll'),
    leader: document.getElementById('projectCountLeader'),
    researcher: document.getElementById('projectCountResearcher'),
    'TÜBİTAK': document.getElementById('projectCountTubitak'),
    'TAGEM': document.getElementById('projectCountTagem'),
    'AR-GE': document.getElementById('projectCountArge'),
    'COMU-BAP': document.getElementById('projectCountComubap'),
    'BAP': document.getElementById('projectCountBap'),
    'KUTUP-1001': document.getElementById('projectCountKutup'),
    'Aquaculture': document.getElementById('projectCountAquaculture'),
    'Fisheries': document.getElementById('projectCountFisheries'),
    'Management': document.getElementById('projectCountManagement'),
    'Genetics': document.getElementById('projectCountGenetics'),
    'Biodiversity': document.getElementById('projectCountBiodiversity'),
    'Polar Science': document.getElementById('projectCountPolar'),
    'Climate Change': document.getElementById('projectCountClimate'),
    'Biotechnology': document.getElementById('projectCountBiotech'),
    'Seafood': document.getElementById('projectCountSeafood'),
    'Water quality': document.getElementById('projectCountWater'),
    'Fish Disease': document.getElementById('projectCountDisease')
  };

  function getTags(node) {
    return (node.dataset.tags || '').split(',').map(s => s.trim()).filter(Boolean);
  }

  function updateCounts() {
    const nodes = Array.from(document.querySelectorAll('.project-entry'));
    const counts = {};
    nodes.forEach(node => {
      counts.all = (counts.all || 0) + 1;
      counts[node.dataset.role] = (counts[node.dataset.role] || 0) + 1;
      getTags(node).forEach(tag => counts[tag] = (counts[tag] || 0) + 1);
    });
    Object.keys(countMap).forEach(key => {
      if (countMap[key]) countMap[key].textContent = `(${counts[key] || 0})`;
    });
    totalCount.textContent = nodes.length;
  }

  function applyFilters() {
    const selected = Array.from(filterPanel.querySelectorAll('input[type="checkbox"]'))
      .filter(cb => cb.checked && cb.value !== 'all')
      .map(cb => cb.value);

    const nodes = Array.from(document.querySelectorAll('.project-entry'));
    let shown = 0, shownLeader = 0, shownResearcher = 0;

    nodes.forEach(node => {
      const haystack = [node.dataset.role, ...getTags(node)];
      const match = selected.length === 0 || selected.every(tag => haystack.includes(tag));
      node.style.display = match ? '' : 'none';
      if (match) {
        shown++;
        if (node.dataset.role === 'leader') shownLeader++;
        if (node.dataset.role === 'researcher') shownResearcher++;
      }
    });

    leaderTitle.style.display = shownLeader ? '' : 'none';
    researcherTitle.style.display = shownResearcher ? '' : 'none';
    leaderList.style.display = shownLeader ? '' : 'none';
    researcherList.style.display = shownResearcher ? '' : 'none';
    visibleCount.textContent = shown;
    emptyMsg.style.display = shown ? 'none' : 'block';
    filterAll.checked = selected.length === 0;
  }

  function clearAll() {
    Array.from(filterPanel.querySelectorAll('input[type="checkbox"]')).forEach(cb => cb.checked = false);
    filterAll.checked = true;
    applyFilters();
  }

  filterToggle.addEventListener('click', () => filterPanel.classList.toggle('open'));
  closeFilters.addEventListener('click', () => filterPanel.classList.remove('open'));
  clearFilters.addEventListener('click', clearAll);
  filterAll.addEventListener('change', () => { if (filterAll.checked) clearAll(); });

  Array.from(filterPanel.querySelectorAll('input[type="checkbox"]')).forEach(cb => {
    if (cb !== filterAll) {
      cb.addEventListener('change', () => {
        if (cb.checked) filterAll.checked = false;
        applyFilters();
      });
    }
  });

  document.addEventListener('click', e => {
    if (!filterPanel.contains(e.target) && !filterToggle.contains(e.target)) {
      filterPanel.classList.remove('open');
    }
  });

  document.querySelectorAll('.project-action').forEach(button => {
    button.addEventListener('click', () => {
      const target = document.getElementById(button.dataset.target);
      if (!target) return;
      const parentCard = button.closest('.project-card, .project-simple');
      parentCard.querySelectorAll('.project-panel').forEach(panel => {
        if (panel !== target) panel.classList.remove('open');
      });
      target.classList.toggle('open');
    });
  });

  updateCounts();
  clearAll();
})();
</script>

<script>
(function () {
  const sdgNames = {
    "SDG 1": "No Poverty",
    "SDG 2": "Zero Hunger",
    "SDG 3": "Good Health and Well-Being",
    "SDG 4": "Quality Education",
    "SDG 5": "Gender Equality",
    "SDG 6": "Clean Water and Sanitation",
    "SDG 7": "Affordable and Clean Energy",
    "SDG 8": "Decent Work and Economic Growth",
    "SDG 9": "Industry, Innovation and Infrastructure",
    "SDG 10": "Reduced Inequalities",
    "SDG 11": "Sustainable Cities and Communities",
    "SDG 12": "Responsible Consumption and Production",
    "SDG 13": "Climate Action",
    "SDG 14": "Life Below Water",
    "SDG 15": "Life on Land",
    "SDG 16": "Peace, Justice and Strong Institutions",
    "SDG 17": "Partnerships for the Goals"
  };

  let tooltip = document.querySelector('.sdg-hover-tooltip');
  if (!tooltip) {
    tooltip = document.createElement('div');
    tooltip.className = 'sdg-hover-tooltip';
    document.body.appendChild(tooltip);
  }

  function moveTooltip(e) {
    tooltip.style.left = e.clientX + 'px';
    tooltip.style.top = (e.clientY - 10) + 'px';
  }

  document.querySelectorAll('.project-sdgs img').forEach(img => {
    img.removeAttribute('title');
    img.addEventListener('mouseenter', e => {
      const key = (img.getAttribute('alt') || '').trim();
      tooltip.textContent = sdgNames[key] || key;
      tooltip.classList.add('show');
      moveTooltip(e);
    });
    img.addEventListener('mousemove', moveTooltip);
    img.addEventListener('mouseleave', () => {
      tooltip.classList.remove('show');
    });
  });
})();
</script>

şimdi https://ekremcem.github.io/presentations/ sayfaya ekleme yapıcaz. iki tane poster bildiri eklenecek en üste. ben sana özetleri word olarak atıyorum sen formate göre gerekli bilgileri çek. isimler vb. ingilizce adları al onları koda ekle. kodu bir sonraki komutta atıcam. İngilizce olacak.

sonra other preseantation kısmında da şu ikisini ekleyeceksin. onları aşağıya yazıyorum 
Çankırılıgil E.C., 2026. Preliminary Findings on the Bioecological Characteristics of Scallops Distributed in the Sea of Marmara. INTERREG NEXT “Black Sea Basin 2021-2027”, Project BSB01206 TIMMOD-NEXT. National Stakeholder Meeting, 11 June 2026, Trabzon (Invited speaker)konuşmacı)
Çankırılıgil E.C., 2026. Biotechnological Potential of Antarctic Macroalgae. INTERREG NEXT “Black Sea Basin 2021-2027”, Project BSB01206 TIMMOD-NEXT. National Stakeholder Meeting, 11 June 2026, Trabzon (Invited speaker)


Tamam. Word dosyalarındaki iki poster bildirinin İngilizce başlık, yazar, etkinlik, tarih, yer ve sunum türü bilgilerini çıkarıp Poster Presentations bölümünün en üstüne, mevcut formatı aynen koruyarak ekleyeceğim.

Other Presentations bölümünün en üstüne de şu iki kaydı ekleyeceğim:

Çankırılıgil E.C., 2026. Preliminary Findings on the Bioecological Characteristics of Scallops Distributed in the Sea of Marmara. INTERREG NEXT “Black Sea Basin 2021–2027”, Project BSB01206 TIMMOD-NEXT. National Stakeholder Meeting, 11 June 2026, Trabzon, Türkiye. Invited speaker.

Çankırılıgil E.C., 2026. Biotechnological Potential of Antarctic Macroalgae. INTERREG NEXT “Black Sea Basin 2021–2027”, Project BSB01206 TIMMOD-NEXT. National Stakeholder Meeting, 11 June 2026, Trabzon, Türkiye. Invited speaker.

Sonraki mesajda Word dosyalarını ve kodun mevcut son halini gönderdiğinde, başka hiçbir şeyi değiştirmeden doğrudan kopyalanmaya hazır tam kodu vereceğim.



Yapıştırılan metin(15).txt
Belge
ayrıca poster özetlerine ab kodları olarak 2 ve 14 ekle. other presntations olanlara da 2, 13, 14 ekle. bu arada kodda poster presentations diye bölüm yok. conferense presentatiosn var. hepsi orda olacak. sadece bahsettiğim iki tanesi en altta other yazan yerde olacak. kodu yazıyorum. son final hali ver.




45s düşündü
İki poster bildiri Conference Presentations bölümünün en üstüne; iki davetli konuşma Other Presentations bölümünün en üstüne eklendi. Tür adları italik, SDG kodları belirttiğin şekilde işlendi. Özetlerdeki İngilizce başlık ve yazar bilgileri esas alındı. 

 


presentations_final.md




Kitaplık
/
presentations_final.md


---
layout: page
title: Presentations
permalink: /presentations/
nav: true
nav_order: 5
description: Conference and other presentations in reverse chronological order.
---

<style>
  .presentations-controls {
    display: flex;
    justify-content: flex-end;
    margin-bottom: 1rem;
    position: relative;
  }

  .filter-toggle {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.45rem 0.9rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.95rem;
  }

  .filter-panel {
    display: none;
    position: absolute;
    top: 2.7rem;
    right: 0;
    z-index: 20;
    width: min(380px, 94vw);
    padding: 0.95rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: var(--global-bg-color);
    box-shadow: 0 8px 24px rgba(0,0,0,0.08);
  }

  .filter-panel.open {
    display: block;
  }

  .filter-title {
    font-weight: 700;
    margin-bottom: 0.35rem;
  }

  .filter-subtitle {
    font-size: 0.88rem;
    color: var(--global-theme-color);
    margin-bottom: 0.7rem;
  }

  .filter-group {
    margin-bottom: 0.85rem;
  }

  .filter-group-title {
    font-weight: 700;
    font-size: 0.9rem;
    margin-bottom: 0.35rem;
  }

  .filter-options {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem 0.8rem;
  }

  .filter-options label {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.92rem;
    cursor: pointer;
  }

  .filter-options .count {
    color: var(--global-theme-color);
    font-size: 0.85rem;
  }

  .filter-actions {
    display: flex;
    justify-content: space-between;
    margin-top: 0.8rem;
    gap: 0.6rem;
  }

  .filter-btn {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.4rem 0.8rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.9rem;
  }

  .presentation-section-title {
    margin: 1.25rem 0 0.6rem 0;
  }

  .presentation-list {
    display: flex;
    flex-direction: column;
  }

  .presentation-entry {
    padding: 0.85rem 0;
    border-bottom: 1px solid color-mix(in srgb, var(--global-divider-color) 70%, transparent 30%);
  }

  .presentation-entry:last-child {
    border-bottom: none;
  }

  .presentation-year {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.2rem;
  }

  .presentation-text {
    line-height: 1.65;
    color: var(--global-text-color);
  }

  .self-author {
    color: var(--global-theme-color);
    font-weight: 700;
  }

  .presentation-title {
    font-weight: 700;
    color: var(--global-text-color);
  }

  .presentation-event {
    font-style: italic;
  }

  .presentation-meta {
    margin-top: 0.55rem;
  }

  .presentation-links {
    display: inline-flex;
    align-items: center;
    gap: 0.45rem;
    flex-wrap: wrap;
    margin-left: 0.35rem;
    vertical-align: middle;
  }

  .presentation-link {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    color: var(--global-theme-color);
    line-height: 1;
    cursor: pointer;
    background: none;
    border: none;
    padding: 0;
    font-size: 0.95rem;
  }

  .presentation-link:hover {
    opacity: 0.8;
    text-decoration: none;
  }

  .presentation-link.rg img {
    width: 16px;
    height: 16px;
    display: block;
  }

  .sdg-trigger img {
    width: 16px;
    height: 16px;
    display: block;
  }

  .sdg-wrap,
  .cite-wrap {
    position: relative;
    display: inline-flex;
    align-items: center;
  }

  .sdg-trigger,
  .cite-trigger {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0;
    background: none;
    border: none;
    color: var(--global-theme-color);
    cursor: pointer;
    font-size: 0.95rem;
    line-height: 1;
  }

  .sdg-popover,
  .cite-popover {
    display: none;
    position: absolute;
    top: 1.8rem;
    left: 0;
    z-index: 15;
    min-width: 240px;
    max-width: min(92vw, 420px);
    padding: 0.7rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 12px;
    background: var(--global-bg-color);
    box-shadow: 0 8px 24px rgba(0,0,0,0.08);
  }

  .sdg-wrap.open .sdg-popover,
  .cite-wrap.open .cite-popover {
    display: block;
  }

  .sdg-icons {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  .sdg-icons img {
    width: 36px;
    height: 36px;
    object-fit: contain;
    display: block;
  }

  .cite-label {
    font-weight: 700;
    margin-bottom: 0.35rem;
    font-size: 0.9rem;
  }

  .cite-text {
    font-size: 0.88rem;
    line-height: 1.55;
    color: var(--global-text-color);
    margin-bottom: 0.45rem;
  }

  .copy-cite-btn {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.28rem 0.7rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.82rem;
  }

  .presentation-chips {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
  }

  .presentation-chip {
    display: inline-flex;
    align-items: center;
    padding: 0.22rem 0.55rem;
    border-radius: 999px;
    background: color-mix(in srgb, var(--global-divider-color) 20%, transparent 80%);
    color: #111;
    font-size: 0.82rem;
    line-height: 1.2;
  }

  .presentation-empty {
    display: none;
    margin-top: 1rem;
    color: var(--global-text-color);
  }
</style>

<div class="section-card">
  <div class="presentations-controls">
    <button class="filter-toggle" type="button" id="filterToggle">Filter</button>

    <div class="filter-panel" id="filterPanel">
      <div class="filter-title">Filter presentations</div>
      <div class="filter-subtitle">Showing <span id="visibleCount">0</span> of <span id="totalCount">0</span></div>

      <div class="filter-group">
        <div class="filter-group-title">Quick</div>
        <div class="filter-options">
          <label><input type="checkbox" value="all" id="filterAll"> All <span class="count" id="countAll">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Sections</div>
        <div class="filter-options">
          <label><input type="checkbox" value="conference presentations"> Conference presentations <span class="count" id="countConference">(0)</span></label>
          <label><input type="checkbox" value="other presentations"> Other presentations <span class="count" id="countOther">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Types</div>
        <div class="filter-options">
          <label><input type="checkbox" value="oral presentation"> Oral presentation <span class="count" id="countOral">(0)</span></label>
          <label><input type="checkbox" value="poster presentation"> Poster presentation <span class="count" id="countPoster">(0)</span></label>
          <label><input type="checkbox" value="full-text"> Full-text <span class="count" id="countFullText">(0)</span></label>
          <label><input type="checkbox" value="invited speaker"> Invited speaker <span class="count" id="countInvited">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Format / scope</div>
        <div class="filter-options">
          <label><input type="checkbox" value="international symposium"> International <span class="count" id="countInternational">(0)</span></label>
          <label><input type="checkbox" value="national symposium"> National <span class="count" id="countNational">(0)</span></label>
          <label><input type="checkbox" value="virtual"> Virtual <span class="count" id="countVirtual">(0)</span></label>
          <label><input type="checkbox" value="workshop"> Workshop <span class="count" id="countWorkshop">(0)</span></label>
          <label><input type="checkbox" value="seminar"> Seminar <span class="count" id="countSeminar">(0)</span></label>
          <label><input type="checkbox" value="meeting"> Meeting <span class="count" id="countMeeting">(0)</span></label>
        </div>
      </div>

      <div class="filter-actions">
        <button class="filter-btn" type="button" id="clearFilters">Clear</button>
        <button class="filter-btn" type="button" id="closeFilters">Close</button>
      </div>
    </div>
  </div>

  <h2 class="section-title">Conference Presentations</h2>
  <div class="presentation-list" id="conferenceList"></div>

  <h2 class="section-title presentation-section-title">Other Presentations</h2>
  <div class="presentation-list" id="otherList"></div>

  <p class="presentation-empty" id="presentationEmpty">No presentations match the selected filters.</p>
</div>

<script>
  (function () {
    const entries = [{"section": "conference presentations", "year": 2026, "sort_date": "2026-08-31", "authors": "Çankırılıgil E.C., Uslu A.A., Özel O.T.", "cite_authors": "Çankırılıgil, E. C., Uslu, A. A., & Özel, O. T.", "title_html": "Protein and Lipid Quality of Fillets from Rainbow Trout Fed Diets Containing Black Soldier Fly and Mealworm Meals", "event": "11th National Limnology Symposium", "date_place": "31 August–2 September 2026, Balıkesir, Türkiye", "date_display": "2026, August 31–September 2", "location": "Balıkesir, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2026, "sort_date": "2026-08-31", "authors": "Çankırılıgil E.C., Özel O.T., Çoşkun İ., Berik N., Çakmak E.", "cite_authors": "Çankırılıgil, E. C., Özel, O. T., Çoşkun, İ., Berik, N., & Çakmak, E.", "title_html": "Effects of Carotenoids on the Intestinal Histomorphology of Black Sea Trout (<em>Salmo labrax</em>)", "event": "11th National Limnology Symposium", "date_place": "31 August–2 September 2026, Balıkesir, Türkiye", "date_display": "2026, August 31–September 2", "location": "Balıkesir, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "other presentations", "year": 2026, "sort_date": "2026-06-11", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Preliminary Findings on the Bioecological Characteristics of Scallops Distributed in the Sea of Marmara", "event": "INTERREG NEXT “Black Sea Basin 2021–2027”, Project BSB01206 TIMMOD-NEXT, National Stakeholder Meeting", "date_place": "11 June 2026, Trabzon, Türkiye", "date_display": "2026, June 11", "location": "Trabzon, Türkiye", "tags": ["invited speaker", "meeting"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg13", "sdg14"]}, {"section": "other presentations", "year": 2026, "sort_date": "2026-06-11", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Biotechnological Potential of Antarctic Macroalgae", "event": "INTERREG NEXT “Black Sea Basin 2021–2027”, Project BSB01206 TIMMOD-NEXT, National Stakeholder Meeting", "date_place": "11 June 2026, Trabzon, Türkiye", "date_display": "2026, June 11", "location": "Trabzon, Türkiye", "tags": ["invited speaker", "meeting"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2025, "sort_date": "2025-11-05", "authors": "Çankırılıgil E.C., Ak İ.", "cite_authors": "Çankırılıgil, E. C., & Ak, İ.", "title_html": "Antarktika Makroalgleri ve İklim Değişikliği: Horseshoe Adası Örneği", "event": "National Polar Sciences Symposium", "date_place": "5–6 November 2025, İzmir, Türkiye", "date_display": "2025, November 5–6", "location": "İzmir, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/398987908_Antarctic_Macroalgae_and_Climate_Change_The_Case_of_Horseshoe_Island", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2025, "sort_date": "2025-08-04", "authors": "Apaydın Yağcı M., Yağcı A., Çankırılıgil E. C., Kocabaş E.", "cite_authors": "Apaydın Yağcı, M., Yağcı, A., Çankırılıgil, E. C., & Kocabaş, E.", "title_html": "A Preliminary Study on the Zooplankton Fauna of Gölbaşı Lake (Bursa/Kestel – Türkiye)", "event": "The XVII International Rotifer Symposium", "date_place": "4–8 August 2025, Rio de Janeiro, Brazil", "date_display": "2025, August 4–8", "location": "Rio de Janeiro, Brazil", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/394522886_A_preliminary_study_on_the_Rotifera_fauna_of_Golbasi_Lake_Kestel_Bursa-Turkiye", "links": [], "sdgs": ["sdg14"]}, {"section": "conference presentations", "year": 2024, "sort_date": "2024-11-08", "authors": "Çankırılıgil E.C., Ak İ., Apaydın Yağcı M., Türker G., Kara A., Veske E., Kocabaş E., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Apaydın Yağcı, M., Türker, G., Kara, A., Veske, E., Kocabaş, E., & Berik, N.", "title_html": "Snapshots of Marine Life at Horseshoe Island, Antarctica: Highlights from Underwater Observations and Specimen Collections", "event": "8th National Polar Sciences Symposium", "date_place": "8 November 2024, Kocaeli, Türkiye", "date_display": "2024, November 8", "location": "Kocaeli, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/387327570_Snapshots_of_Marine_Life_at_Horseshoe_Island_Antarctica_Highlights_from_Underwater_Observations_and_Specimen_Collections", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2024, "sort_date": "2024-11-08", "authors": "Çankırılıgil E.C., Ak İ., Türker G., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Türker, G., & Berik, N.", "title_html": "Profiling Chemical Components of Seaweed Species from the Antarctic Peninsula", "event": "8th National Polar Sciences Symposium", "date_place": "8 November 2024, Kocaeli, Türkiye", "date_display": "2024, November 8", "location": "Kocaeli, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/387327560_Profiling_Chemical_Components_of_Seaweed_Species_from_the_Antarctic_Peninsula", "links": [], "sdgs": ["sdg2", "sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2024, "sort_date": "2024-11-08", "authors": "Ak İ., Çankırılıgil E.C.", "cite_authors": "Ak, İ., & Çankırılıgil, E. C.", "title_html": "Observations on the Diversity of Benthic Macroalgae Along the Shores of Horseshoe Island, Antarctica", "event": "8th National Polar Sciences Symposium", "date_place": "8 November 2024, Gebze, Kocaeli, Türkiye", "date_display": "2024, November 8", "location": "Gebze, Kocaeli, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/387327564_Observations_on_the_Diversity_of_Benthic_Macroalgae_Along_the_Shores_of_Horseshoe_Island_Antarctica", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2023, "sort_date": "2023-12-04", "authors": "Çankırılıgil E.C., Ak İ., Türker G., Kara A., Veske E., Apaydın Yağcı M., Kocabaş E., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Türker, G., Kara, A., Veske, E., Apaydın Yağcı, M., Kocabaş, E., & Berik, N.", "title_html": "Antarktika Horseshoe Adası Makroalgleri: Yedinci Ulusal Antarktika Bilim Seferi Kapsamında Yapılan Çalışmalar", "event": "7. Ulusal Kutup Bilimleri Sempozyumu", "date_place": "4 December 2023, İstanbul, Türkiye", "date_display": "2023, December 4", "location": "İstanbul, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/377223123_Macroalgae_of_Horseshoe_Island_Antarctica_Studies_Conducted_in_the_Seventh_National_Antarctic_Science_Expedition", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-09-20", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Nutritional Composition and Texture Profile of Wild and Culture Adapted Blue Crab (<em>Callinectes sapidus</em>) Meat", "event": "The 8th Aquatic Biodiversity International Conference (ABIC 8)", "date_place": "20–22 September 2022, Sibiu, Transylvania, Romania", "date_display": "2022, September 20–22", "location": "Sibiu, Transylvania, Romania", "tags": ["oral presentation", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/363668764_Nutritional_Composition_and_Texture_Profile_of_Wild_and_Culture_Adapted_Blue_Crab_Callinectes_sapidus_Meat", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-09-15", "authors": "Özel O.T., Çakmak E., Çankırılıgil E.C., Düzgüneş Z.D., Çimagil R.", "cite_authors": "Özel, O. T., Çakmak, E., Çankırılıgil, E. C., Düzgüneş, Z. D., & Çimagil, R.", "title_html": "Farklı Yaşlarda Cinsel Olgunluğa Ulaşan Karadeniz Somonu Anaçlarının (<em>Salmo labrax</em> PALLAS, 1811) Üreme Performansı", "event": "6th National Trout Symposium", "date_place": "15–16 September 2022, Isparta, Türkiye", "date_display": "2022, September 15–16", "location": "Isparta, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/363668832_Ilk_Cinsel_Olgunluga_Farkli_Yaslarda_Ulasan_Karadeniz_Somonu_Anaclarinin_Salmo_labrax_PALLAS_1814_Ureme_Performansinin_Karsilastirilmasi", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-09-15", "authors": "Özel O.T., Çakmak E., Çankırılıgil E.C., Çimagil R., Düzgüneş Z.D.", "cite_authors": "Özel, O. T., Çakmak, E., Çankırılıgil, E. C., Çimagil, R., & Düzgüneş, Z. D.", "title_html": "Kuluçkahane Kökenli F5 ve F6 Nesil Karadeniz Somonu Anaçlarının (<em>Salmo labrax</em> PALLAS, 1811) Üreme Performansı İlişkisi", "event": "6th National Trout Symposium", "date_place": "15–16 September 2022, Isparta, Türkiye", "date_display": "2022, September 15–16", "location": "Isparta, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/363668839_Kuluckahane_Kokenli_F5_ve_F6_Nesil_Karadeniz_Somonu_Anaclarinin_Salmo_labrax_PALLAS_1811_Ureme_Performansi_Iliskisi", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-06-01", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "A Preliminary Study on the Antioxidant Activity and Amino Acid Composition of Marine Sponge <em>Aplysina aerophoba</em> Collected from Northeastern Aegean Sea", "event": "5th National Marine Sciences Congress", "date_place": "1–3 June 2022, Trabzon, Türkiye", "date_display": "2022, June 1–3", "location": "Trabzon, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/361109263_A_Preliminary_Study_on_the_Antioxidant_Activity_and_Amino_Acid_Composition_of_Marine_Sponge_Aplysina_aerophoba_Collected_from_Northeastern_Aegean_Sea", "links": [], "sdgs": ["sdg3", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-01-14", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Determination of Amino Acid Composition, Color and Texture Profile of Fresh and Processed Sea Cucumber (<em>Holothuria tubulosa</em>)", "event": "Tokyo Summit-V, 5th International Conference on Innovative Studies of Contemporary Sciences", "date_place": "14–16 January 2022, Tokyo, Japan", "date_display": "2022, January 14–16", "location": "Tokyo, Japan", "tags": ["oral presentation", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/357869097_Determination_of_Amino_Acid_Composition_Color_and_Texture_Profile_of_Fresh_and_Processed_Sea_Cucumber_Holothuria_tubulosa", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-11-04", "authors": "Çankırılıgil E.C., Ak İ.", "cite_authors": "Çankırılıgil, E. C., & Ak, İ.", "title_html": "Amino Acid Composition of Seaweeds from Çanakkale, Türkiye", "event": "HydroMediT 2021 - 4th International Congress on Applied Ichthyology, Oceanography & Aquatic Environment", "date_place": "4–6 November 2021, Greece", "date_display": "2021, November 4–6", "location": "Greece", "tags": ["oral presentation", "full-text", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/356913912_Amino_Acid_Composition_of_Seaweeds_from_Canakkale_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-11-04", "authors": "Çankırılıgil E.C., Ak İ.", "cite_authors": "Çankırılıgil, E. C., & Ak, İ.", "title_html": "Amino Acid Composition of <em>Ceramium rubrum</em> (Rhodophyceae) from North Aegean Sea, Türkiye", "event": "HydroMediT 2021 - 4th International Congress on Applied Ichthyology, Oceanography & Aquatic Environment", "date_place": "4–6 November 2021, Greece", "date_display": "2021, November 4–6", "location": "Greece", "tags": ["poster presentation", "full-text", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/356914177_Amino_Acid_Composition_of_Ceramium_rubrum_Rhodophyceae_from_North_Aegean_Sea_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-10-01", "authors": "Uslu A.A., Özel O.T., Örnekçi N., Çankırılıgil E.C., Çoşkun İ., Şenel G.U.", "cite_authors": "Uslu, A. A., Özel, O. T., Örnekçi, N., Çankırılıgil, E. C., Çoşkun, İ., & Şenel, G. U.", "title_html": "Black soldier fly (<em>Hermetia illucens</em>) prepupae meal as a possible alternative to fish meal in Rainbow trout (<em>Oncorhynchus mykiss</em>) diets", "event": "TURFAJ 2021, 2nd International Congress of the Turkish Journal of Agriculture - Food Science and Technology", "date_place": "October 2021, Gazimağusa", "date_display": "2021, October", "location": "Gazimağusa", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/357737768_Black_soldier_fly_Hermetia_illucens_prepupae_meal_as_a_possible_alternative_to_fish_meal_in_Rainbow_trout_Oncorhynchus_mykiss_diets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-09-07", "authors": "Uslu A.A., Özel O.T., Çelik B., Çankırılıgil E.C., Çoşkun İ.", "cite_authors": "Uslu, A. A., Özel, O. T., Çelik, B., Çankırılıgil, E. C., & Çoşkun, İ.", "title_html": "Fish Meal Replacement by Mealworm (<em>Tenebrio molitor</em>) Larvae Meal in Diets for Rainbow Trout (<em>Oncorhynchus mykiss</em>)", "event": "FABA 2021 - International Symposium on Fisheries and Aquatic Sciences", "date_place": "7–8 September 2021, İzmir, Türkiye", "date_display": "2021, September 7–8", "location": "İzmir, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/356378976_Fish_Meal_Replacement_by_Mealworm_Tenebrio_molitor_Larvae_Meal_in_Diets_for_Rainbow_Trout_Oncorhynchus_mykiss", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-09-26", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Effects of Astaxanthine, Canthaxanthin and Lycopene Containing Diets on the Chemical Quality and Textural Properties of the Black Sea Trout (<em>Salmo labrax</em>) Fillets", "event": "BioEco2019 International Biodiversity & Ecology Sciences Symposium", "date_place": "26–28 September 2019, Istanbul, Türkiye", "date_display": "2019, September 26–28", "location": "Istanbul, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/336150403_Effects_of_Astaxanthine_Canthaxanthin_and_Lycopene_Containing_Diets_on_the_Chemical_Quality_and_Textural_Properties_of_the_Black_Sea_Trout_Salmo_labrax_Fillets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-09-26", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Histological Examination of Black Sea Trout (<em>Salmo labrax</em>) Fed by Carotenoid Containing Diets", "event": "BioEco2019 International Biodiversity & Ecology Sciences Symposium", "date_place": "26–28 September 2019, Istanbul, Türkiye", "date_display": "2019, September 26–28", "location": "Istanbul, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/336150472_Histological_Examination_of_Black_Sea_Trout_Salmo_labrax_Fed_by_Carotenoid_Containing_Diets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-04-20", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Evaluation of Fatty Acid Compositions of Commercial Fish Oils Considering Recommended Omega Fatty Acid Uptake for a Healthy Diet", "event": "4. Uluslararası Anadolu Tarım, Gıda, Çevre ve Biyoloji Kongresi", "date_place": "20–22 April 2019, Afyonkarahisar, Türkiye", "date_display": "2019, April 20–22", "location": "Afyonkarahisar, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/332544748_Evaluation_of_Fatty_Acid_Compositions_of_Commercial_Fish_Oils_Considering_Recommended_Omega_Fatty_Acid_Uptake_for_a_Healthy_Diet", "links": [], "sdgs": ["sdg2", "sdg3", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-04-20", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Seasonal Fatty Acid Composition of Green Seaweed (<em>Ulva rigida</em>)", "event": "4. Uluslararası Anadolu Tarım, Gıda, Çevre ve Biyoloji Kongresi", "date_place": "20–22 April 2019, Afyonkarahisar, Türkiye", "date_display": "2019, April 20–22", "location": "Afyonkarahisar, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/332544744_Seasonal_Fatty_Acid_Composition_of_Green_Seaweed_Ulva_Rigida", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2018, "sort_date": "2018-07-05", "authors": "Ozel O., Türe M., Cakmak E., Cimagil R., Çankırılıgil E.C., Kutlu İ.", "cite_authors": "Ozel, O., Türe, M., Cakmak, E., Cimagil, R., Çankırılıgil, E. C., & Kutlu, İ.", "title_html": "Effects of Dietary Daphne (<em>Laurus nobilis</em> L.) and Fennel (<em>Foeniculum vulgare</em> L.) Essential Oils on Some Intestinal Bacteria of Black Sea Trout (<em>Salmo labrax</em>)", "event": "4th International Agriculture Congress", "date_place": "5–8 July 2018, Kırşehir, Türkiye", "date_display": "2018, July 5–8", "location": "Kırşehir, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/328957639_Effects_of_dietary_daphne_Laurus_nobilis_L_and_fennel_Foeniculum_vulgare_L_oils_on_some_intestinal_bacteria_of_Black_Sea_trout_Salmo_labrax", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-10-27", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "The Processing of Pufferfish and Usage of Tetrodotoxin in the Pharmaceutical Industry", "event": "Jubilee International Scientific Conference “Bulgaria of the Regions”", "date_place": "27–28 October 2017, Plovdiv, Bulgaria", "date_display": "2017, October 27–28", "location": "Plovdiv, Bulgaria", "tags": ["poster presentation", "full-text", "international symposium"], "rg": "https://www.researchgate.net/publication/320620528_The_Processing_of_Pufferfish_and_Usage_of_Tetrodotoxin_in_the_Pharmaceutical_Industry", "links": ["https://regions.uard.bg/index.php/jubilee/jisc/paper/view/140"], "sdgs": ["sdg3", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-10-04", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Element Composition of Farmed Rainbow Trout (<em>Oncorhynchus mykiss</em>) Obtained from Fish Farm in the Mount Ida", "event": "ISEEP-2017 VIII. International Symposium on Ecology and Environmental Problems", "date_place": "4–7 October 2017, Çanakkale, Türkiye", "date_display": "2017, October 4–7", "location": "Çanakkale, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/320191714_Element_Composition_of_Farmed_Rainbow_Trout_Oncorhynchus_mykiss_Obtained_from_Fish_farm_in_the_Mount_Ida", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-10-04", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "The Seasonal Elemental Composition of Green Seaweed (<em>Ulva rigida</em>) Collected from Canakkale, Türkiye", "event": "ISEEP-2017 VIII. International Symposium on Ecology and Environmental Problems", "date_place": "4–7 October 2017, Çanakkale, Türkiye", "date_display": "2017, October 4–7", "location": "Çanakkale, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/320191598_The_Seasonal_Elemental_Composition_of_Green_Seaweed_Ulva_rigida_Collected_from_Canakkale_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-09-12", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Farklı Su Ürünlerinden Elde Edilen Kaplama Ürünlerin Duyusal Özelliklerinin Belirlenmesi", "event": "19. Ulusal Su Ürünleri Sempozyumu", "date_place": "12–15 September 2017, Sinop, Türkiye", "date_display": "2017, September 12–15", "location": "Sinop, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/320011682_Farkli_Su_Urunlerinden_Elde_Edilen_Kaplama_Urunlerin_Duyusal_Ozelliklerinin_Belirlenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-09-12", "authors": "Çankırılıgil E.C., Güven A., Balçık Mısır G.", "cite_authors": "Çankırılıgil, E. C., Güven, A., & Balçık Mısır, G.", "title_html": "Kültüre Alınan Altınbaş Kefalin (<em>Liza aurata</em>) Kas Dokusu ve Atıklarının Amino Asit Kompozisyonunun Belirlenmesi", "event": "19. Ulusal Su Ürünleri Sempozyumu", "date_place": "12–15 September 2017, Sinop, Türkiye", "date_display": "2017, September 12–15", "location": "Sinop, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/319998160_Kulture_Alinan_Altinbas_Kefalin_Liza_aurata_Kas_Dokusu_ve_Atiklarinin_Amino_Asit_Kompozisyonunun_Belirlenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-09-12", "authors": "Kasapoğlu N., Güven A., Çakmak E., Çankırılıgil E.C., Firidin Ş.", "cite_authors": "Kasapoğlu, N., Güven, A., Çakmak, E., Çankırılıgil, E. C., & Firidin, Ş.", "title_html": "Karadeniz Kefal Avcılığında Hedef Dışı Av Oranları", "event": "19. Ulusal Su Ürünleri Sempozyumu", "date_place": "12–15 September 2017, Sinop, Türkiye", "date_display": "2017, September 12–15", "location": "Sinop, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/320557038_Karadeniz_Kefal_Avciliginda_Hedef_Disi_Av_Oranlari", "links": [], "sdgs": ["sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Çankırılıgil E.C., Çakmak E., Özel O.T., Kasapoğlu N.", "cite_authors": "Çankırılıgil, E. C., Çakmak, E., Özel, O. T., & Kasapoğlu, N.", "title_html": "Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811) Culture in Türkiye and Morphometric Characteristics of Fifth Culture Generation", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318318294_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811_Culture_in_Turkey_and_Morphometric_Characteristics_of_Fifth_Culture_Generation", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Amino Acid Composition of Cultured Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811)", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318318094_Amino_Acid_Composition_of_Cultured_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Scallop Species in Türkiye and Evaluation in terms of Food Safety Considering 9th Task Group of Marine Strategy Framework Directive", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318318091_Scallop_Species_in_Turkey_and_Evaluation_in_terms_of_Food_Safety_Considering_9th_Task_Group_of_Marine_Strategy_Framework_Directive", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Kasapoğlu N., Düzgüneş E., Çankırılıgil E.C.", "cite_authors": "Kasapoğlu, N., Düzgüneş, E., & Çankırılıgil, E. C.", "title_html": "Biodiversity in the Black Sea Bottom Trawl Fisheries and Processing Possibilities of Discard Species", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318339614_Biodiversity_in_the_Black_Sea_Bottom_Trawl_Fisheries_and_Processing_Possibilities_of_Discard_Species", "links": [], "sdgs": ["sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-11-03", "authors": "Çankırılıgil E.C., Berik N., Çakmak E.", "cite_authors": "Çankırılıgil, E. C., Berik, N., & Çakmak, E.", "title_html": "Meat Color Changes in Different Generations of Cultured Black Sea Trout (<em>Salmo trutta labrax</em>): A Preliminary Study", "event": "FABA 2016, International Symposium on Fisheries and Aquatic Sciences", "date_place": "3–5 November 2016, Antalya, Türkiye", "date_display": "2016, November 3–5", "location": "Antalya, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310704030_Meat_color_changes_in_different_generations_of_cultured_Black_Sea_trout_Salmo_trutta_labrax_a_preliminary_study", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-11-03", "authors": "Çankırılıgil E.C., Alp Erbay E.", "cite_authors": "Çankırılıgil, E. C., & Alp Erbay, E.", "title_html": "Effect of Different Thawing Techniques on Color of Black Sea Trout (<em>Salmo trutta labrax</em>) Fillets", "event": "FABA 2016, International Symposium on Fisheries and Aquatic Sciences", "date_place": "3–5 November 2016, Antalya, Türkiye", "date_display": "2016, November 3–5", "location": "Antalya, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310704780_Effect_of_Different_Thawing_Techniques_on_Color_of_Black_Sea_Trout_Salmo_trutta_labrax_Fillets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-11-03", "authors": "Kasapoğlu N., Çankırılıgil E.C., Çakmak E.", "cite_authors": "Kasapoğlu, N., Çankırılıgil, E. C., & Çakmak, E.", "title_html": "A Preliminary Study on Growth Characteristics of Striped Sea Bream, <em>Lithognathus mormyrus</em>, in the Black Sea", "event": "FABA 2016, International Symposium on Fisheries and Aquatic Sciences", "date_place": "3–5 November 2016, Antalya, Türkiye", "date_display": "2016, November 3–5", "location": "Antalya, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310721246_A_PRELIMINARY_STUDY_ON_GROWTH_CHARACTERISTICS_OF_STRIPED_SEA_BREAM_Lithognathus_mormyrus_IN_THE_BLACK_SEA", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-10-21", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Changes in Fatty Acid and Mineral Compositions of Rose-Shrimp Croquettes during Production Process", "event": "63rd Scientific Conference with International Participation “Food Science, Engineering and Technology 2016”", "date_place": "21–22 October 2016, Plovdiv, Bulgaria", "date_display": "2016, October 21–22", "location": "Plovdiv, Bulgaria", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310705586_Changes_in_Fatty_Acid_and_Mineral_Compositions_of_Rose-Shrimp_Croquettes_During_Production_Process", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-09-12", "authors": "Çankırılıgil E.C., Çakmak E., Özcan Akpınar İ.", "cite_authors": "Çankırılıgil, E. C., Çakmak, E., & Özcan Akpınar, İ.", "title_html": "Histological Development of the Digestive Tract of Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811) During Larval Ontogeny", "event": "41th CIESM Congress, Living Resources & Marine Ecosystems Committee", "date_place": "12–16 September 2016, Kiel, Germany", "date_display": "2016, September 12–16", "location": "Kiel, Germany", "tags": ["oral presentation", "poster presentation", "full-text", "international symposium"], "rg": "https://www.researchgate.net/publication/310705507_Histological_Development_of_the_Digestive_Tract_of_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811_During_Larval_Ontogeny", "links": ["https://ciesm.org/online/archives/abstracts/pdf/41/CIESM_Congress_2016_Kiel_article_0330.pdf"], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-09-12", "authors": "Kasapoğlu N., Çakmak E., Çankırılıgil E.C.", "cite_authors": "Kasapoğlu, N., Çakmak, E., & Çankırılıgil, E. C.", "title_html": "Differences Between Cultured and Wild Black Sea Trout (<em>Salmo trutta labrax</em>) Otoliths: A Comparative Study", "event": "41th CIESM Congress, Living Resources & Marine Ecosystems Committee", "date_place": "12–16 September 2016, Kiel, Germany", "date_display": "2016, September 12–16", "location": "Kiel, Germany", "tags": ["oral presentation", "poster presentation", "full-text", "international symposium"], "rg": "https://www.researchgate.net/publication/310719575_Differences_Between_Cultured_and_Wild_Black_Sea_Trout_Salmo_trutta_labrax_Otoliths_A_Comparative_Study", "links": ["https://ciesm.org/online/archives/abstracts/pdf/41/CIESM_Congress_2016_Kiel_article_0519.pdf"], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2015, "sort_date": "2015-09-18", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Mineral Contents of Meat and Digestive Glands of Scallops (<em>Flexopecten glaber</em>) Caught in Çanakkale Strait, Türkiye", "event": "MACODESU 2015, Conference of Sea and Coastal Development in the frame of Sustainability", "date_place": "18–20 September 2015, Trabzon, Türkiye", "date_display": "2015, September 18–20", "location": "Trabzon, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/280134261_Mineral_Contents_of_Meat_and_Digestive_Glands_of_Scallops_Flexopecten_glaber_Catched_in_Canakkale_Strait_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2013, "sort_date": "2013-09-03", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Gökkuşağı Alabalığı (<em>Oncorhynchus mykiss</em>) Kroketlerinin Soğuk Muhafazada (+4ºC) Raf Ömrünün Belirlenmesi", "event": "17. Ulusal Su Ürünleri Sempozyumu", "date_place": "3–6 September 2013, İstanbul, Türkiye", "date_display": "2013, September 3–6", "location": "İstanbul, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831368_Gokkusagi_Alabaligi_Oncorhynchus_mykiss_Kroketlerinin_Soguk_Muhafazada_4C_Raf_Omrunun_Belirlenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2012, "sort_date": "2012-11-09", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Determination of Proximate Composition and Sensory Attributes of Scallop (<em>Flexopecten glaber</em>) Gonads", "event": "Turkish-Japanese Marine Forum, Harmonization of Bio-diversity and Marine Industries Symposium", "date_place": "9–12 November 2012, Türkiye", "date_display": "2012, November 9–12", "location": "Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/314209537_Determination_of_Proximate_Composition_and_Sensory_Attributes_of_Scallop_Flexopecten_glaber_Gonads", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2012, "sort_date": "2012-11-09", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Production of Croquettes from Deep-Water Rose Shrimp (<em>Parapenaeus longirostris</em>) Meat", "event": "Turkish-Japanese Marine Forum, Harmonization of Bio-diversity and Marine Industries Symposium", "date_place": "9–12 November 2012, Çanakkale, Türkiye", "date_display": "2012, November 9–12", "location": "Çanakkale, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/261830662_Production_of_Croquettes_from_Deep-Water_Rose_Shrimp_Parapenaeus_longirostris_Meat", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2011, "sort_date": "2011-10-25", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Çanakkale Balık Halinden Temin Edilen Deniz Tarağına (<em>Flexopecten glaber</em>) Farklı Pişirme Tekniklerinin Uygulanması", "event": "16. Ulusal Su Ürünleri Sempozyumu", "date_place": "25–27 October 2011, Antalya, Türkiye", "date_display": "2011, October 25–27", "location": "Antalya, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831190_Canakkale_Balik_Halinden_Temin_Edilen_Deniz_Taragina_Flexopecten_glaber_Farkli_Pisirme_Tekniklerinin_Uygulanmasi", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2010, "sort_date": "2010-07-06", "authors": "Berik N., Kahraman D., Çankırılıgil E.C.", "cite_authors": "Berik, N., Kahraman, D., & Çankırılıgil, E. C.", "title_html": "Alabalık (<em>Oncorhynchus mykiss</em>) Marinatlarının Duyusal ve Besin Değeri Bakımından Değerlendirilmesi", "event": "2. Ulusal Alabalık Sempozyumu", "date_place": "6–8 July 2010, Karaman, Türkiye", "date_display": "2010, July 6–8", "location": "Karaman, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831194_Alabalik_Oncorhynchus_mykiss_Marinatlarinin_Duyusal_ve_Besin_Degeri_Bakimindan_Degerlendirilmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2010, "sort_date": "2010-07-06", "authors": "Berik N., Çankırılıgil E.C., Kahraman D.", "cite_authors": "Berik, N., Çankırılıgil, E. C., & Kahraman, D.", "title_html": "Alabalık (<em>Oncorhynchus mykiss</em>) Eti Kullanılarak Hazırlanan Kroketlerin Besin Bileşimi ve Duyusal Analizleri Açısından İncelenmesi", "event": "2nd National Trout Symposium", "date_place": "6–8 July 2010, Karaman, Türkiye", "date_display": "2010, July 6–8", "location": "Karaman, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831381_Alabalik_Oncorhynchus_mykiss_Eti_Kullanilarak_Hazirlanan_Kroketlerin_Besin_Bilesimi_ve_Duyusal_Analizleri_Acisindan_Incelenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "other presentations", "year": 2024, "sort_date": "2024-11-09", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Marine Life in Antarctica", "event": "Maltepe Kadir Has Science and Art Center, Student Seminar", "date_place": "9 November 2024, İstanbul, Türkiye", "date_display": "2024, November 9", "location": "İstanbul, Türkiye", "tags": ["invited speaker", "seminar"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2023, "sort_date": "2023-12-05", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Algae in Extreme Climate Conditions: The Case of Horseshoe Island", "event": "Horseshoe Island and Glacial Lakes Biodiversity Workshop", "date_place": "5–6 December 2023, Erzurum, Türkiye", "date_display": "2023, December 5–6", "location": "Erzurum, Türkiye", "tags": ["invited speaker", "workshop"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2023, "sort_date": "2023-07-01", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "7th National Turkish Antarctic Expedition", "event": "T.C. Ministry of Agriculture and Forest, I. Regional Group Meeting", "date_place": "July 2023, Yalova, Türkiye", "date_display": "2023, July", "location": "Yalova, Türkiye", "tags": ["oral presentation", "meeting"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2023, "sort_date": "2023-06-01", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Studies that carried out in 7th National Turkish Antarctic Expedition", "event": "Career Talks in ÇOMÜ Marine Science and Technology Faculty", "date_place": "June 2023, Çanakkale, Türkiye", "date_display": "2023, June", "location": "Çanakkale, Türkiye", "tags": ["invited speaker", "seminar"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2022, "sort_date": "2022-12-01", "authors": "Çankırılıgil E.C., Ak İ., Türker G., Kara A., Veske E., Apaydın Yağcı M., Kocabaş E., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Türker, G., Kara, A., Veske, E., Apaydın Yağcı, M., Kocabaş, E., & Berik, N.", "title_html": "Biological Activity Evaluation of Macroalgae Distributed on Horseshoe Island (Antarctica) Coasts by Determining Nutrient Composition and Phytochemical Contents – Project Display", "event": "6. National Polar Science Workshop", "date_place": "1 December 2022, Trabzon, Türkiye", "date_display": "2022, December 1", "location": "Trabzon, Türkiye", "tags": ["oral presentation", "workshop"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg3", "sdg14"]}, {"section": "other presentations", "year": 2022, "sort_date": "2022-06-22", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Studies on Macroalgae Culture", "event": "Workshop of Blue Economy and Aquatic Plants", "date_place": "22–23 June 2022, Antalya, Türkiye", "date_display": "2022, June 22–23", "location": "Antalya, Türkiye", "tags": ["oral presentation", "workshop"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "other presentations", "year": 2017, "sort_date": "2017-10-24", "authors": "Çankırılıgil E.C., Çakmak E., Özel O.T., Kasapoğlu N., Alp Erbay E., Özcan Akpınar İ.", "cite_authors": "Çankırılıgil, E. C., Çakmak, E., Özel, O. T., Kasapoğlu, N., Alp Erbay, E., & Özcan Akpınar, İ.", "title_html": "An Overview on Biology, Biochemistry and Aquaculture of the 5th Culture Generation of Black Sea Trout (<em>Salmo trutta labrax</em>) Considering Recent Studies", "event": "Workshop on Aquaculture in the Black Sea: Potential and Opportunities", "date_place": "24–26 October 2017, Trabzon, Türkiye", "date_display": "2017, October 24–26", "location": "Trabzon, Türkiye", "tags": ["oral presentation", "workshop"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}];

    const conferenceList = document.getElementById('conferenceList');
    const otherList = document.getElementById('otherList');
    const toggleBtn = document.getElementById('filterToggle');
    const panel = document.getElementById('filterPanel');
    const closeBtn = document.getElementById('closeFilters');
    const clearBtn = document.getElementById('clearFilters');
    const allCheckbox = document.getElementById('filterAll');
    const visibleCountEl = document.getElementById('visibleCount');
    const totalCountEl = document.getElementById('totalCount');
    const emptyState = document.getElementById('presentationEmpty');

    const countMap = {
      all: document.getElementById('countAll'),
      'conference presentations': document.getElementById('countConference'),
      'other presentations': document.getElementById('countOther'),
      'oral presentation': document.getElementById('countOral'),
      'poster presentation': document.getElementById('countPoster'),
      'full-text': document.getElementById('countFullText'),
      'invited speaker': document.getElementById('countInvited'),
      'international symposium': document.getElementById('countInternational'),
      'national symposium': document.getElementById('countNational'),
      'virtual': document.getElementById('countVirtual'),
      'workshop': document.getElementById('countWorkshop'),
      'seminar': document.getElementById('countSeminar'),
      'meeting': document.getElementById('countMeeting')
    };

    function highlightSelf(authorText) {
      return authorText
        .replace(/Çankırılıgil E\. C\./g, '<span class="self-author">Çankırılıgil E. C.</span>')
        .replace(/Çankırılıgil E\.C\./g, '<span class="self-author">Çankırılıgil E.C.</span>');
    }

    function escapeHtml(text) {
      return text
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;')
        .replace(/'/g, '&#039;');
    }

    function buildApaCitation(entry) {
      return `${entry.cite_authors} (${entry.date_display}). ${entry.title_html.replace(/<[^>]*>/g, '')} [Conference presentation]. ${entry.event}, ${entry.location}.`;
    }

    function createLinkControls(entry) {
      const wrapper = document.createElement('span');
      wrapper.className = 'presentation-links';

      if (entry.rg) {
        const rg = document.createElement('a');
        rg.className = 'presentation-link rg';
        rg.href = entry.rg;
        rg.target = '_blank';
        rg.rel = 'noopener';
        rg.setAttribute('aria-label', 'ResearchGate link');
        rg.innerHTML = `<img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">`;
        wrapper.appendChild(rg);
      }

      entry.links.forEach(url => {
        const extra = document.createElement('a');
        extra.className = 'presentation-link';
        extra.href = url;
        extra.target = '_blank';
        extra.rel = 'noopener';
        extra.setAttribute('aria-label', 'External link');
        extra.textContent = '🔗';
        wrapper.appendChild(extra);
      });

      if (entry.sdgs && entry.sdgs.length) {
        const sdgWrap = document.createElement('span');
        sdgWrap.className = 'sdg-wrap';
        sdgWrap.innerHTML = `
          <button class="sdg-trigger" type="button" aria-label="Show SDGs">
            <img src="{{ '/assets/img/sdgicon.png' | relative_url }}" alt="SDGs">
          </button>
          <div class="sdg-popover">
            <div class="sdg-icons">
              ${entry.sdgs.map(sdg => `<img src="{{ '/assets/img/' | relative_url }}${sdg}.png" alt="${sdg.toUpperCase().replace('SDG', 'SDG ')}">`).join('')}
            </div>
          </div>
        `;
        wrapper.appendChild(sdgWrap);
      }

      const citeWrap = document.createElement('span');
      citeWrap.className = 'cite-wrap';
      const citation = buildApaCitation(entry);
      citeWrap.innerHTML = `
        <button class="cite-trigger" type="button">Cite</button>
        <div class="cite-popover">
          <div class="cite-label">APA 7th</div>
          <div class="cite-text">${escapeHtml(citation)}</div>
          <button class="copy-cite-btn" type="button">Copy</button>
        </div>
      `;
      wrapper.appendChild(citeWrap);

      return wrapper;
    }

    function createEntry(entry) {
      const item = document.createElement('div');
      item.className = 'presentation-entry';
      item.dataset.tags = [entry.section].concat(entry.tags).join(',');
      item.dataset.section = entry.section;
      item.dataset.date = entry.sort_date;

      const meta = document.createElement('div');
      meta.className = 'presentation-meta';

      const chips = document.createElement('div');
      chips.className = 'presentation-chips';
      entry.tags.forEach(tag => {
        const chip = document.createElement('span');
        chip.className = 'presentation-chip';
        chip.textContent = tag.charAt(0).toUpperCase() + tag.slice(1);
        chips.appendChild(chip);
      });

      const linksHtml = createLinkControls(entry).outerHTML;

      item.innerHTML = `
        <div class="presentation-year">${entry.year}</div>
        <div class="presentation-text">
          ${highlightSelf(entry.authors)},
          <span class="presentation-title">${entry.title_html}</span>.
          <span class="presentation-event">${entry.event}</span>, ${entry.date_place}.${linksHtml}
        </div>
      `;
      meta.appendChild(chips);
      item.appendChild(meta);
      return item;
    }

    entries.sort((a, b) => b.sort_date.localeCompare(a.sort_date));

    entries.forEach(entry => {
      const node = createEntry(entry);
      if (entry.section === 'conference presentations') {
        conferenceList.appendChild(node);
      } else {
        otherList.appendChild(node);
      }
    });

    const renderedEntries = Array.from(document.querySelectorAll('.presentation-entry'));
    const checkboxes = Array.from(panel.querySelectorAll('input[type="checkbox"]'));

    function normalizeTag(tag) {
      return tag.trim().toLowerCase();
    }

    function getTags(entry) {
      return (entry.dataset.tags || '')
        .split(',')
        .map(normalizeTag)
        .filter(Boolean);
    }

    function updateStaticCounts() {
      const counts = {};
      renderedEntries.forEach(entry => {
        const tags = getTags(entry);
        counts.all = (counts.all || 0) + 1;
        tags.forEach(tag => counts[tag] = (counts[tag] || 0) + 1);
      });
      Object.keys(countMap).forEach(key => {
        if (countMap[key]) countMap[key].textContent = `(${counts[key] || 0})`;
      });
      totalCountEl.textContent = renderedEntries.length;
    }

    function applyFilters() {
      const selected = checkboxes
        .filter(cb => cb.checked && cb.value !== 'all')
        .map(cb => normalizeTag(cb.value));

      let visibleCount = 0;

      renderedEntries.forEach(entry => {
        const tags = getTags(entry);
        const match = selected.length === 0 || selected.every(tag => tags.includes(tag));
        entry.style.display = match ? '' : 'none';
        if (match) visibleCount += 1;
      });

      visibleCountEl.textContent = visibleCount;
      emptyState.style.display = visibleCount === 0 ? 'block' : 'none';
      allCheckbox.checked = selected.length === 0;
    }

    function clearAllFilters() {
      checkboxes.forEach(cb => cb.checked = false);
      allCheckbox.checked = true;
      applyFilters();
    }

    toggleBtn.addEventListener('click', function () {
      panel.classList.toggle('open');
    });

    closeBtn.addEventListener('click', function () {
      panel.classList.remove('open');
    });

    clearBtn.addEventListener('click', function () {
      clearAllFilters();
    });

    allCheckbox.addEventListener('change', function () {
      if (allCheckbox.checked) clearAllFilters();
    });

    checkboxes.forEach(cb => {
      if (cb !== allCheckbox) {
        cb.addEventListener('change', function () {
          if (cb.checked) allCheckbox.checked = false;
          applyFilters();
        });
      }
    });

    document.addEventListener('click', function (event) {
      if (!panel.contains(event.target) && !toggleBtn.contains(event.target)) {
        panel.classList.remove('open');
      }
    });

    document.addEventListener('click', function (event) {
      const sdgBtn = event.target.closest('.sdg-trigger');
      const citeBtn = event.target.closest('.cite-trigger');
      const copyBtn = event.target.closest('.copy-cite-btn');

      if (sdgBtn) {
        event.stopPropagation();
        const wrap = sdgBtn.closest('.sdg-wrap');
        document.querySelectorAll('.sdg-wrap.open').forEach(el => { if (el !== wrap) el.classList.remove('open'); });
        wrap.classList.toggle('open');
        return;
      }

      if (citeBtn) {
        event.stopPropagation();
        const wrap = citeBtn.closest('.cite-wrap');
        document.querySelectorAll('.cite-wrap.open').forEach(el => { if (el !== wrap) el.classList.remove('open'); });
        wrap.classList.toggle('open');
        return;
      }

      if (copyBtn) {
        const wrap = copyBtn.closest('.cite-wrap');
        const citation = wrap.querySelector('.cite-text').textContent;
        navigator.clipboard.writeText(citation).then(() => {
          copyBtn.textContent = 'Copied';
          setTimeout(() => copyBtn.textContent = 'Copy', 1200);
        }).catch(() => {
          copyBtn.textContent = 'Copy failed';
          setTimeout(() => copyBtn.textContent = 'Copy', 1200);
        });
        return;
      }

      document.querySelectorAll('.sdg-wrap.open, .cite-wrap.open').forEach(el => {
        if (!el.contains(event.target)) el.classList.remove('open');
      });
    });

    updateStaticCounts();
    clearAllFilters();
  })();
</script>
Kitaplık
/
presentations_final.md


---
layout: page
title: Presentations
permalink: /presentations/
nav: true
nav_order: 5
description: Conference and other presentations in reverse chronological order.
---

<style>
  .presentations-controls {
    display: flex;
    justify-content: flex-end;
    margin-bottom: 1rem;
    position: relative;
  }

  .filter-toggle {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.45rem 0.9rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.95rem;
  }

  .filter-panel {
    display: none;
    position: absolute;
    top: 2.7rem;
    right: 0;
    z-index: 20;
    width: min(380px, 94vw);
    padding: 0.95rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 14px;
    background: var(--global-bg-color);
    box-shadow: 0 8px 24px rgba(0,0,0,0.08);
  }

  .filter-panel.open {
    display: block;
  }

  .filter-title {
    font-weight: 700;
    margin-bottom: 0.35rem;
  }

  .filter-subtitle {
    font-size: 0.88rem;
    color: var(--global-theme-color);
    margin-bottom: 0.7rem;
  }

  .filter-group {
    margin-bottom: 0.85rem;
  }

  .filter-group-title {
    font-weight: 700;
    font-size: 0.9rem;
    margin-bottom: 0.35rem;
  }

  .filter-options {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem 0.8rem;
  }

  .filter-options label {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
    font-size: 0.92rem;
    cursor: pointer;
  }

  .filter-options .count {
    color: var(--global-theme-color);
    font-size: 0.85rem;
  }

  .filter-actions {
    display: flex;
    justify-content: space-between;
    margin-top: 0.8rem;
    gap: 0.6rem;
  }

  .filter-btn {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.4rem 0.8rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.9rem;
  }

  .presentation-section-title {
    margin: 1.25rem 0 0.6rem 0;
  }

  .presentation-list {
    display: flex;
    flex-direction: column;
  }

  .presentation-entry {
    padding: 0.85rem 0;
    border-bottom: 1px solid color-mix(in srgb, var(--global-divider-color) 70%, transparent 30%);
  }

  .presentation-entry:last-child {
    border-bottom: none;
  }

  .presentation-year {
    color: var(--global-theme-color);
    font-weight: 700;
    margin-bottom: 0.2rem;
  }

  .presentation-text {
    line-height: 1.65;
    color: var(--global-text-color);
  }

  .self-author {
    color: var(--global-theme-color);
    font-weight: 700;
  }

  .presentation-title {
    font-weight: 700;
    color: var(--global-text-color);
  }

  .presentation-event {
    font-style: italic;
  }

  .presentation-meta {
    margin-top: 0.55rem;
  }

  .presentation-links {
    display: inline-flex;
    align-items: center;
    gap: 0.45rem;
    flex-wrap: wrap;
    margin-left: 0.35rem;
    vertical-align: middle;
  }

  .presentation-link {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    color: var(--global-theme-color);
    line-height: 1;
    cursor: pointer;
    background: none;
    border: none;
    padding: 0;
    font-size: 0.95rem;
  }

  .presentation-link:hover {
    opacity: 0.8;
    text-decoration: none;
  }

  .presentation-link.rg img {
    width: 16px;
    height: 16px;
    display: block;
  }

  .sdg-trigger img {
    width: 16px;
    height: 16px;
    display: block;
  }

  .sdg-wrap,
  .cite-wrap {
    position: relative;
    display: inline-flex;
    align-items: center;
  }

  .sdg-trigger,
  .cite-trigger {
    display: inline-flex;
    align-items: center;
    justify-content: center;
    padding: 0;
    background: none;
    border: none;
    color: var(--global-theme-color);
    cursor: pointer;
    font-size: 0.95rem;
    line-height: 1;
  }

  .sdg-popover,
  .cite-popover {
    display: none;
    position: absolute;
    top: 1.8rem;
    left: 0;
    z-index: 15;
    min-width: 240px;
    max-width: min(92vw, 420px);
    padding: 0.7rem;
    border: 1px solid var(--global-divider-color);
    border-radius: 12px;
    background: var(--global-bg-color);
    box-shadow: 0 8px 24px rgba(0,0,0,0.08);
  }

  .sdg-wrap.open .sdg-popover,
  .cite-wrap.open .cite-popover {
    display: block;
  }

  .sdg-icons {
    display: flex;
    flex-wrap: wrap;
    gap: 0.4rem;
  }

  .sdg-icons img {
    width: 36px;
    height: 36px;
    object-fit: contain;
    display: block;
  }

  .cite-label {
    font-weight: 700;
    margin-bottom: 0.35rem;
    font-size: 0.9rem;
  }

  .cite-text {
    font-size: 0.88rem;
    line-height: 1.55;
    color: var(--global-text-color);
    margin-bottom: 0.45rem;
  }

  .copy-cite-btn {
    border: 1px solid var(--global-divider-color);
    background: var(--global-bg-color);
    color: var(--global-text-color);
    padding: 0.28rem 0.7rem;
    border-radius: 999px;
    cursor: pointer;
    font-size: 0.82rem;
  }

  .presentation-chips {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
  }

  .presentation-chip {
    display: inline-flex;
    align-items: center;
    padding: 0.22rem 0.55rem;
    border-radius: 999px;
    background: color-mix(in srgb, var(--global-divider-color) 20%, transparent 80%);
    color: #111;
    font-size: 0.82rem;
    line-height: 1.2;
  }

  .presentation-empty {
    display: none;
    margin-top: 1rem;
    color: var(--global-text-color);
  }
</style>

<div class="section-card">
  <div class="presentations-controls">
    <button class="filter-toggle" type="button" id="filterToggle">Filter</button>

    <div class="filter-panel" id="filterPanel">
      <div class="filter-title">Filter presentations</div>
      <div class="filter-subtitle">Showing <span id="visibleCount">0</span> of <span id="totalCount">0</span></div>

      <div class="filter-group">
        <div class="filter-group-title">Quick</div>
        <div class="filter-options">
          <label><input type="checkbox" value="all" id="filterAll"> All <span class="count" id="countAll">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Sections</div>
        <div class="filter-options">
          <label><input type="checkbox" value="conference presentations"> Conference presentations <span class="count" id="countConference">(0)</span></label>
          <label><input type="checkbox" value="other presentations"> Other presentations <span class="count" id="countOther">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Types</div>
        <div class="filter-options">
          <label><input type="checkbox" value="oral presentation"> Oral presentation <span class="count" id="countOral">(0)</span></label>
          <label><input type="checkbox" value="poster presentation"> Poster presentation <span class="count" id="countPoster">(0)</span></label>
          <label><input type="checkbox" value="full-text"> Full-text <span class="count" id="countFullText">(0)</span></label>
          <label><input type="checkbox" value="invited speaker"> Invited speaker <span class="count" id="countInvited">(0)</span></label>
        </div>
      </div>

      <div class="filter-group">
        <div class="filter-group-title">Format / scope</div>
        <div class="filter-options">
          <label><input type="checkbox" value="international symposium"> International <span class="count" id="countInternational">(0)</span></label>
          <label><input type="checkbox" value="national symposium"> National <span class="count" id="countNational">(0)</span></label>
          <label><input type="checkbox" value="virtual"> Virtual <span class="count" id="countVirtual">(0)</span></label>
          <label><input type="checkbox" value="workshop"> Workshop <span class="count" id="countWorkshop">(0)</span></label>
          <label><input type="checkbox" value="seminar"> Seminar <span class="count" id="countSeminar">(0)</span></label>
          <label><input type="checkbox" value="meeting"> Meeting <span class="count" id="countMeeting">(0)</span></label>
        </div>
      </div>

      <div class="filter-actions">
        <button class="filter-btn" type="button" id="clearFilters">Clear</button>
        <button class="filter-btn" type="button" id="closeFilters">Close</button>
      </div>
    </div>
  </div>

  <h2 class="section-title">Conference Presentations</h2>
  <div class="presentation-list" id="conferenceList"></div>

  <h2 class="section-title presentation-section-title">Other Presentations</h2>
  <div class="presentation-list" id="otherList"></div>

  <p class="presentation-empty" id="presentationEmpty">No presentations match the selected filters.</p>
</div>

<script>
  (function () {
    const entries = [{"section": "conference presentations", "year": 2026, "sort_date": "2026-08-31", "authors": "Çankırılıgil E.C., Uslu A.A., Özel O.T.", "cite_authors": "Çankırılıgil, E. C., Uslu, A. A., & Özel, O. T.", "title_html": "Protein and Lipid Quality of Fillets from Rainbow Trout Fed Diets Containing Black Soldier Fly and Mealworm Meals", "event": "11th National Limnology Symposium", "date_place": "31 August–2 September 2026, Balıkesir, Türkiye", "date_display": "2026, August 31–September 2", "location": "Balıkesir, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2026, "sort_date": "2026-08-31", "authors": "Çankırılıgil E.C., Özel O.T., Çoşkun İ., Berik N., Çakmak E.", "cite_authors": "Çankırılıgil, E. C., Özel, O. T., Çoşkun, İ., Berik, N., & Çakmak, E.", "title_html": "Effects of Carotenoids on the Intestinal Histomorphology of Black Sea Trout (<em>Salmo labrax</em>)", "event": "11th National Limnology Symposium", "date_place": "31 August–2 September 2026, Balıkesir, Türkiye", "date_display": "2026, August 31–September 2", "location": "Balıkesir, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "other presentations", "year": 2026, "sort_date": "2026-06-11", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Preliminary Findings on the Bioecological Characteristics of Scallops Distributed in the Sea of Marmara", "event": "INTERREG NEXT “Black Sea Basin 2021–2027”, Project BSB01206 TIMMOD-NEXT, National Stakeholder Meeting", "date_place": "11 June 2026, Trabzon, Türkiye", "date_display": "2026, June 11", "location": "Trabzon, Türkiye", "tags": ["invited speaker", "meeting"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg13", "sdg14"]}, {"section": "other presentations", "year": 2026, "sort_date": "2026-06-11", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Biotechnological Potential of Antarctic Macroalgae", "event": "INTERREG NEXT “Black Sea Basin 2021–2027”, Project BSB01206 TIMMOD-NEXT, National Stakeholder Meeting", "date_place": "11 June 2026, Trabzon, Türkiye", "date_display": "2026, June 11", "location": "Trabzon, Türkiye", "tags": ["invited speaker", "meeting"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2025, "sort_date": "2025-11-05", "authors": "Çankırılıgil E.C., Ak İ.", "cite_authors": "Çankırılıgil, E. C., & Ak, İ.", "title_html": "Antarktika Makroalgleri ve İklim Değişikliği: Horseshoe Adası Örneği", "event": "National Polar Sciences Symposium", "date_place": "5–6 November 2025, İzmir, Türkiye", "date_display": "2025, November 5–6", "location": "İzmir, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/398987908_Antarctic_Macroalgae_and_Climate_Change_The_Case_of_Horseshoe_Island", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2025, "sort_date": "2025-08-04", "authors": "Apaydın Yağcı M., Yağcı A., Çankırılıgil E. C., Kocabaş E.", "cite_authors": "Apaydın Yağcı, M., Yağcı, A., Çankırılıgil, E. C., & Kocabaş, E.", "title_html": "A Preliminary Study on the Zooplankton Fauna of Gölbaşı Lake (Bursa/Kestel – Türkiye)", "event": "The XVII International Rotifer Symposium", "date_place": "4–8 August 2025, Rio de Janeiro, Brazil", "date_display": "2025, August 4–8", "location": "Rio de Janeiro, Brazil", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/394522886_A_preliminary_study_on_the_Rotifera_fauna_of_Golbasi_Lake_Kestel_Bursa-Turkiye", "links": [], "sdgs": ["sdg14"]}, {"section": "conference presentations", "year": 2024, "sort_date": "2024-11-08", "authors": "Çankırılıgil E.C., Ak İ., Apaydın Yağcı M., Türker G., Kara A., Veske E., Kocabaş E., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Apaydın Yağcı, M., Türker, G., Kara, A., Veske, E., Kocabaş, E., & Berik, N.", "title_html": "Snapshots of Marine Life at Horseshoe Island, Antarctica: Highlights from Underwater Observations and Specimen Collections", "event": "8th National Polar Sciences Symposium", "date_place": "8 November 2024, Kocaeli, Türkiye", "date_display": "2024, November 8", "location": "Kocaeli, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/387327570_Snapshots_of_Marine_Life_at_Horseshoe_Island_Antarctica_Highlights_from_Underwater_Observations_and_Specimen_Collections", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2024, "sort_date": "2024-11-08", "authors": "Çankırılıgil E.C., Ak İ., Türker G., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Türker, G., & Berik, N.", "title_html": "Profiling Chemical Components of Seaweed Species from the Antarctic Peninsula", "event": "8th National Polar Sciences Symposium", "date_place": "8 November 2024, Kocaeli, Türkiye", "date_display": "2024, November 8", "location": "Kocaeli, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/387327560_Profiling_Chemical_Components_of_Seaweed_Species_from_the_Antarctic_Peninsula", "links": [], "sdgs": ["sdg2", "sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2024, "sort_date": "2024-11-08", "authors": "Ak İ., Çankırılıgil E.C.", "cite_authors": "Ak, İ., & Çankırılıgil, E. C.", "title_html": "Observations on the Diversity of Benthic Macroalgae Along the Shores of Horseshoe Island, Antarctica", "event": "8th National Polar Sciences Symposium", "date_place": "8 November 2024, Gebze, Kocaeli, Türkiye", "date_display": "2024, November 8", "location": "Gebze, Kocaeli, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/387327564_Observations_on_the_Diversity_of_Benthic_Macroalgae_Along_the_Shores_of_Horseshoe_Island_Antarctica", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2023, "sort_date": "2023-12-04", "authors": "Çankırılıgil E.C., Ak İ., Türker G., Kara A., Veske E., Apaydın Yağcı M., Kocabaş E., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Türker, G., Kara, A., Veske, E., Apaydın Yağcı, M., Kocabaş, E., & Berik, N.", "title_html": "Antarktika Horseshoe Adası Makroalgleri: Yedinci Ulusal Antarktika Bilim Seferi Kapsamında Yapılan Çalışmalar", "event": "7. Ulusal Kutup Bilimleri Sempozyumu", "date_place": "4 December 2023, İstanbul, Türkiye", "date_display": "2023, December 4", "location": "İstanbul, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/377223123_Macroalgae_of_Horseshoe_Island_Antarctica_Studies_Conducted_in_the_Seventh_National_Antarctic_Science_Expedition", "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-09-20", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Nutritional Composition and Texture Profile of Wild and Culture Adapted Blue Crab (<em>Callinectes sapidus</em>) Meat", "event": "The 8th Aquatic Biodiversity International Conference (ABIC 8)", "date_place": "20–22 September 2022, Sibiu, Transylvania, Romania", "date_display": "2022, September 20–22", "location": "Sibiu, Transylvania, Romania", "tags": ["oral presentation", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/363668764_Nutritional_Composition_and_Texture_Profile_of_Wild_and_Culture_Adapted_Blue_Crab_Callinectes_sapidus_Meat", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-09-15", "authors": "Özel O.T., Çakmak E., Çankırılıgil E.C., Düzgüneş Z.D., Çimagil R.", "cite_authors": "Özel, O. T., Çakmak, E., Çankırılıgil, E. C., Düzgüneş, Z. D., & Çimagil, R.", "title_html": "Farklı Yaşlarda Cinsel Olgunluğa Ulaşan Karadeniz Somonu Anaçlarının (<em>Salmo labrax</em> PALLAS, 1811) Üreme Performansı", "event": "6th National Trout Symposium", "date_place": "15–16 September 2022, Isparta, Türkiye", "date_display": "2022, September 15–16", "location": "Isparta, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/363668832_Ilk_Cinsel_Olgunluga_Farkli_Yaslarda_Ulasan_Karadeniz_Somonu_Anaclarinin_Salmo_labrax_PALLAS_1814_Ureme_Performansinin_Karsilastirilmasi", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-09-15", "authors": "Özel O.T., Çakmak E., Çankırılıgil E.C., Çimagil R., Düzgüneş Z.D.", "cite_authors": "Özel, O. T., Çakmak, E., Çankırılıgil, E. C., Çimagil, R., & Düzgüneş, Z. D.", "title_html": "Kuluçkahane Kökenli F5 ve F6 Nesil Karadeniz Somonu Anaçlarının (<em>Salmo labrax</em> PALLAS, 1811) Üreme Performansı İlişkisi", "event": "6th National Trout Symposium", "date_place": "15–16 September 2022, Isparta, Türkiye", "date_display": "2022, September 15–16", "location": "Isparta, Türkiye", "tags": ["oral presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/363668839_Kuluckahane_Kokenli_F5_ve_F6_Nesil_Karadeniz_Somonu_Anaclarinin_Salmo_labrax_PALLAS_1811_Ureme_Performansi_Iliskisi", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-06-01", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "A Preliminary Study on the Antioxidant Activity and Amino Acid Composition of Marine Sponge <em>Aplysina aerophoba</em> Collected from Northeastern Aegean Sea", "event": "5th National Marine Sciences Congress", "date_place": "1–3 June 2022, Trabzon, Türkiye", "date_display": "2022, June 1–3", "location": "Trabzon, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/361109263_A_Preliminary_Study_on_the_Antioxidant_Activity_and_Amino_Acid_Composition_of_Marine_Sponge_Aplysina_aerophoba_Collected_from_Northeastern_Aegean_Sea", "links": [], "sdgs": ["sdg3", "sdg14"]}, {"section": "conference presentations", "year": 2022, "sort_date": "2022-01-14", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Determination of Amino Acid Composition, Color and Texture Profile of Fresh and Processed Sea Cucumber (<em>Holothuria tubulosa</em>)", "event": "Tokyo Summit-V, 5th International Conference on Innovative Studies of Contemporary Sciences", "date_place": "14–16 January 2022, Tokyo, Japan", "date_display": "2022, January 14–16", "location": "Tokyo, Japan", "tags": ["oral presentation", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/357869097_Determination_of_Amino_Acid_Composition_Color_and_Texture_Profile_of_Fresh_and_Processed_Sea_Cucumber_Holothuria_tubulosa", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-11-04", "authors": "Çankırılıgil E.C., Ak İ.", "cite_authors": "Çankırılıgil, E. C., & Ak, İ.", "title_html": "Amino Acid Composition of Seaweeds from Çanakkale, Türkiye", "event": "HydroMediT 2021 - 4th International Congress on Applied Ichthyology, Oceanography & Aquatic Environment", "date_place": "4–6 November 2021, Greece", "date_display": "2021, November 4–6", "location": "Greece", "tags": ["oral presentation", "full-text", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/356913912_Amino_Acid_Composition_of_Seaweeds_from_Canakkale_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-11-04", "authors": "Çankırılıgil E.C., Ak İ.", "cite_authors": "Çankırılıgil, E. C., & Ak, İ.", "title_html": "Amino Acid Composition of <em>Ceramium rubrum</em> (Rhodophyceae) from North Aegean Sea, Türkiye", "event": "HydroMediT 2021 - 4th International Congress on Applied Ichthyology, Oceanography & Aquatic Environment", "date_place": "4–6 November 2021, Greece", "date_display": "2021, November 4–6", "location": "Greece", "tags": ["poster presentation", "full-text", "international symposium", "virtual"], "rg": "https://www.researchgate.net/publication/356914177_Amino_Acid_Composition_of_Ceramium_rubrum_Rhodophyceae_from_North_Aegean_Sea_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-10-01", "authors": "Uslu A.A., Özel O.T., Örnekçi N., Çankırılıgil E.C., Çoşkun İ., Şenel G.U.", "cite_authors": "Uslu, A. A., Özel, O. T., Örnekçi, N., Çankırılıgil, E. C., Çoşkun, İ., & Şenel, G. U.", "title_html": "Black soldier fly (<em>Hermetia illucens</em>) prepupae meal as a possible alternative to fish meal in Rainbow trout (<em>Oncorhynchus mykiss</em>) diets", "event": "TURFAJ 2021, 2nd International Congress of the Turkish Journal of Agriculture - Food Science and Technology", "date_place": "October 2021, Gazimağusa", "date_display": "2021, October", "location": "Gazimağusa", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/357737768_Black_soldier_fly_Hermetia_illucens_prepupae_meal_as_a_possible_alternative_to_fish_meal_in_Rainbow_trout_Oncorhynchus_mykiss_diets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2021, "sort_date": "2021-09-07", "authors": "Uslu A.A., Özel O.T., Çelik B., Çankırılıgil E.C., Çoşkun İ.", "cite_authors": "Uslu, A. A., Özel, O. T., Çelik, B., Çankırılıgil, E. C., & Çoşkun, İ.", "title_html": "Fish Meal Replacement by Mealworm (<em>Tenebrio molitor</em>) Larvae Meal in Diets for Rainbow Trout (<em>Oncorhynchus mykiss</em>)", "event": "FABA 2021 - International Symposium on Fisheries and Aquatic Sciences", "date_place": "7–8 September 2021, İzmir, Türkiye", "date_display": "2021, September 7–8", "location": "İzmir, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/356378976_Fish_Meal_Replacement_by_Mealworm_Tenebrio_molitor_Larvae_Meal_in_Diets_for_Rainbow_Trout_Oncorhynchus_mykiss", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-09-26", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Effects of Astaxanthine, Canthaxanthin and Lycopene Containing Diets on the Chemical Quality and Textural Properties of the Black Sea Trout (<em>Salmo labrax</em>) Fillets", "event": "BioEco2019 International Biodiversity & Ecology Sciences Symposium", "date_place": "26–28 September 2019, Istanbul, Türkiye", "date_display": "2019, September 26–28", "location": "Istanbul, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/336150403_Effects_of_Astaxanthine_Canthaxanthin_and_Lycopene_Containing_Diets_on_the_Chemical_Quality_and_Textural_Properties_of_the_Black_Sea_Trout_Salmo_labrax_Fillets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-09-26", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Histological Examination of Black Sea Trout (<em>Salmo labrax</em>) Fed by Carotenoid Containing Diets", "event": "BioEco2019 International Biodiversity & Ecology Sciences Symposium", "date_place": "26–28 September 2019, Istanbul, Türkiye", "date_display": "2019, September 26–28", "location": "Istanbul, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/336150472_Histological_Examination_of_Black_Sea_Trout_Salmo_labrax_Fed_by_Carotenoid_Containing_Diets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-04-20", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Evaluation of Fatty Acid Compositions of Commercial Fish Oils Considering Recommended Omega Fatty Acid Uptake for a Healthy Diet", "event": "4. Uluslararası Anadolu Tarım, Gıda, Çevre ve Biyoloji Kongresi", "date_place": "20–22 April 2019, Afyonkarahisar, Türkiye", "date_display": "2019, April 20–22", "location": "Afyonkarahisar, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/332544748_Evaluation_of_Fatty_Acid_Compositions_of_Commercial_Fish_Oils_Considering_Recommended_Omega_Fatty_Acid_Uptake_for_a_Healthy_Diet", "links": [], "sdgs": ["sdg2", "sdg3", "sdg14"]}, {"section": "conference presentations", "year": 2019, "sort_date": "2019-04-20", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Seasonal Fatty Acid Composition of Green Seaweed (<em>Ulva rigida</em>)", "event": "4. Uluslararası Anadolu Tarım, Gıda, Çevre ve Biyoloji Kongresi", "date_place": "20–22 April 2019, Afyonkarahisar, Türkiye", "date_display": "2019, April 20–22", "location": "Afyonkarahisar, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/332544744_Seasonal_Fatty_Acid_Composition_of_Green_Seaweed_Ulva_Rigida", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2018, "sort_date": "2018-07-05", "authors": "Ozel O., Türe M., Cakmak E., Cimagil R., Çankırılıgil E.C., Kutlu İ.", "cite_authors": "Ozel, O., Türe, M., Cakmak, E., Cimagil, R., Çankırılıgil, E. C., & Kutlu, İ.", "title_html": "Effects of Dietary Daphne (<em>Laurus nobilis</em> L.) and Fennel (<em>Foeniculum vulgare</em> L.) Essential Oils on Some Intestinal Bacteria of Black Sea Trout (<em>Salmo labrax</em>)", "event": "4th International Agriculture Congress", "date_place": "5–8 July 2018, Kırşehir, Türkiye", "date_display": "2018, July 5–8", "location": "Kırşehir, Türkiye", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/328957639_Effects_of_dietary_daphne_Laurus_nobilis_L_and_fennel_Foeniculum_vulgare_L_oils_on_some_intestinal_bacteria_of_Black_Sea_trout_Salmo_labrax", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-10-27", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "The Processing of Pufferfish and Usage of Tetrodotoxin in the Pharmaceutical Industry", "event": "Jubilee International Scientific Conference “Bulgaria of the Regions”", "date_place": "27–28 October 2017, Plovdiv, Bulgaria", "date_display": "2017, October 27–28", "location": "Plovdiv, Bulgaria", "tags": ["poster presentation", "full-text", "international symposium"], "rg": "https://www.researchgate.net/publication/320620528_The_Processing_of_Pufferfish_and_Usage_of_Tetrodotoxin_in_the_Pharmaceutical_Industry", "links": ["https://regions.uard.bg/index.php/jubilee/jisc/paper/view/140"], "sdgs": ["sdg3", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-10-04", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Element Composition of Farmed Rainbow Trout (<em>Oncorhynchus mykiss</em>) Obtained from Fish Farm in the Mount Ida", "event": "ISEEP-2017 VIII. International Symposium on Ecology and Environmental Problems", "date_place": "4–7 October 2017, Çanakkale, Türkiye", "date_display": "2017, October 4–7", "location": "Çanakkale, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/320191714_Element_Composition_of_Farmed_Rainbow_Trout_Oncorhynchus_mykiss_Obtained_from_Fish_farm_in_the_Mount_Ida", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-10-04", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "The Seasonal Elemental Composition of Green Seaweed (<em>Ulva rigida</em>) Collected from Canakkale, Türkiye", "event": "ISEEP-2017 VIII. International Symposium on Ecology and Environmental Problems", "date_place": "4–7 October 2017, Çanakkale, Türkiye", "date_display": "2017, October 4–7", "location": "Çanakkale, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/320191598_The_Seasonal_Elemental_Composition_of_Green_Seaweed_Ulva_rigida_Collected_from_Canakkale_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-09-12", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Farklı Su Ürünlerinden Elde Edilen Kaplama Ürünlerin Duyusal Özelliklerinin Belirlenmesi", "event": "19. Ulusal Su Ürünleri Sempozyumu", "date_place": "12–15 September 2017, Sinop, Türkiye", "date_display": "2017, September 12–15", "location": "Sinop, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/320011682_Farkli_Su_Urunlerinden_Elde_Edilen_Kaplama_Urunlerin_Duyusal_Ozelliklerinin_Belirlenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-09-12", "authors": "Çankırılıgil E.C., Güven A., Balçık Mısır G.", "cite_authors": "Çankırılıgil, E. C., Güven, A., & Balçık Mısır, G.", "title_html": "Kültüre Alınan Altınbaş Kefalin (<em>Liza aurata</em>) Kas Dokusu ve Atıklarının Amino Asit Kompozisyonunun Belirlenmesi", "event": "19. Ulusal Su Ürünleri Sempozyumu", "date_place": "12–15 September 2017, Sinop, Türkiye", "date_display": "2017, September 12–15", "location": "Sinop, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/319998160_Kulture_Alinan_Altinbas_Kefalin_Liza_aurata_Kas_Dokusu_ve_Atiklarinin_Amino_Asit_Kompozisyonunun_Belirlenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-09-12", "authors": "Kasapoğlu N., Güven A., Çakmak E., Çankırılıgil E.C., Firidin Ş.", "cite_authors": "Kasapoğlu, N., Güven, A., Çakmak, E., Çankırılıgil, E. C., & Firidin, Ş.", "title_html": "Karadeniz Kefal Avcılığında Hedef Dışı Av Oranları", "event": "19. Ulusal Su Ürünleri Sempozyumu", "date_place": "12–15 September 2017, Sinop, Türkiye", "date_display": "2017, September 12–15", "location": "Sinop, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/320557038_Karadeniz_Kefal_Avciliginda_Hedef_Disi_Av_Oranlari", "links": [], "sdgs": ["sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Çankırılıgil E.C., Çakmak E., Özel O.T., Kasapoğlu N.", "cite_authors": "Çankırılıgil, E. C., Çakmak, E., Özel, O. T., & Kasapoğlu, N.", "title_html": "Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811) Culture in Türkiye and Morphometric Characteristics of Fifth Culture Generation", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318318294_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811_Culture_in_Turkey_and_Morphometric_Characteristics_of_Fifth_Culture_Generation", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Amino Acid Composition of Cultured Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811)", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318318094_Amino_Acid_Composition_of_Cultured_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Scallop Species in Türkiye and Evaluation in terms of Food Safety Considering 9th Task Group of Marine Strategy Framework Directive", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318318091_Scallop_Species_in_Turkey_and_Evaluation_in_terms_of_Food_Safety_Considering_9th_Task_Group_of_Marine_Strategy_Framework_Directive", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2017, "sort_date": "2017-07-05", "authors": "Kasapoğlu N., Düzgüneş E., Çankırılıgil E.C.", "cite_authors": "Kasapoğlu, N., Düzgüneş, E., & Çankırılıgil, E. C.", "title_html": "Biodiversity in the Black Sea Bottom Trawl Fisheries and Processing Possibilities of Discard Species", "event": "SEAB 2017, International Symposium on EuroAsian Biodiversity", "date_place": "5–8 July 2017, Minsk, Belarus", "date_display": "2017, July 5–8", "location": "Minsk, Belarus", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/318339614_Biodiversity_in_the_Black_Sea_Bottom_Trawl_Fisheries_and_Processing_Possibilities_of_Discard_Species", "links": [], "sdgs": ["sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-11-03", "authors": "Çankırılıgil E.C., Berik N., Çakmak E.", "cite_authors": "Çankırılıgil, E. C., Berik, N., & Çakmak, E.", "title_html": "Meat Color Changes in Different Generations of Cultured Black Sea Trout (<em>Salmo trutta labrax</em>): A Preliminary Study", "event": "FABA 2016, International Symposium on Fisheries and Aquatic Sciences", "date_place": "3–5 November 2016, Antalya, Türkiye", "date_display": "2016, November 3–5", "location": "Antalya, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310704030_Meat_color_changes_in_different_generations_of_cultured_Black_Sea_trout_Salmo_trutta_labrax_a_preliminary_study", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-11-03", "authors": "Çankırılıgil E.C., Alp Erbay E.", "cite_authors": "Çankırılıgil, E. C., & Alp Erbay, E.", "title_html": "Effect of Different Thawing Techniques on Color of Black Sea Trout (<em>Salmo trutta labrax</em>) Fillets", "event": "FABA 2016, International Symposium on Fisheries and Aquatic Sciences", "date_place": "3–5 November 2016, Antalya, Türkiye", "date_display": "2016, November 3–5", "location": "Antalya, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310704780_Effect_of_Different_Thawing_Techniques_on_Color_of_Black_Sea_Trout_Salmo_trutta_labrax_Fillets", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-11-03", "authors": "Kasapoğlu N., Çankırılıgil E.C., Çakmak E.", "cite_authors": "Kasapoğlu, N., Çankırılıgil, E. C., & Çakmak, E.", "title_html": "A Preliminary Study on Growth Characteristics of Striped Sea Bream, <em>Lithognathus mormyrus</em>, in the Black Sea", "event": "FABA 2016, International Symposium on Fisheries and Aquatic Sciences", "date_place": "3–5 November 2016, Antalya, Türkiye", "date_display": "2016, November 3–5", "location": "Antalya, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310721246_A_PRELIMINARY_STUDY_ON_GROWTH_CHARACTERISTICS_OF_STRIPED_SEA_BREAM_Lithognathus_mormyrus_IN_THE_BLACK_SEA", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-10-21", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Changes in Fatty Acid and Mineral Compositions of Rose-Shrimp Croquettes during Production Process", "event": "63rd Scientific Conference with International Participation “Food Science, Engineering and Technology 2016”", "date_place": "21–22 October 2016, Plovdiv, Bulgaria", "date_display": "2016, October 21–22", "location": "Plovdiv, Bulgaria", "tags": ["oral presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/310705586_Changes_in_Fatty_Acid_and_Mineral_Compositions_of_Rose-Shrimp_Croquettes_During_Production_Process", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-09-12", "authors": "Çankırılıgil E.C., Çakmak E., Özcan Akpınar İ.", "cite_authors": "Çankırılıgil, E. C., Çakmak, E., & Özcan Akpınar, İ.", "title_html": "Histological Development of the Digestive Tract of Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811) During Larval Ontogeny", "event": "41th CIESM Congress, Living Resources & Marine Ecosystems Committee", "date_place": "12–16 September 2016, Kiel, Germany", "date_display": "2016, September 12–16", "location": "Kiel, Germany", "tags": ["oral presentation", "poster presentation", "full-text", "international symposium"], "rg": "https://www.researchgate.net/publication/310705507_Histological_Development_of_the_Digestive_Tract_of_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811_During_Larval_Ontogeny", "links": ["https://ciesm.org/online/archives/abstracts/pdf/41/CIESM_Congress_2016_Kiel_article_0330.pdf"], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2016, "sort_date": "2016-09-12", "authors": "Kasapoğlu N., Çakmak E., Çankırılıgil E.C.", "cite_authors": "Kasapoğlu, N., Çakmak, E., & Çankırılıgil, E. C.", "title_html": "Differences Between Cultured and Wild Black Sea Trout (<em>Salmo trutta labrax</em>) Otoliths: A Comparative Study", "event": "41th CIESM Congress, Living Resources & Marine Ecosystems Committee", "date_place": "12–16 September 2016, Kiel, Germany", "date_display": "2016, September 12–16", "location": "Kiel, Germany", "tags": ["oral presentation", "poster presentation", "full-text", "international symposium"], "rg": "https://www.researchgate.net/publication/310719575_Differences_Between_Cultured_and_Wild_Black_Sea_Trout_Salmo_trutta_labrax_Otoliths_A_Comparative_Study", "links": ["https://ciesm.org/online/archives/abstracts/pdf/41/CIESM_Congress_2016_Kiel_article_0519.pdf"], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2015, "sort_date": "2015-09-18", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Mineral Contents of Meat and Digestive Glands of Scallops (<em>Flexopecten glaber</em>) Caught in Çanakkale Strait, Türkiye", "event": "MACODESU 2015, Conference of Sea and Coastal Development in the frame of Sustainability", "date_place": "18–20 September 2015, Trabzon, Türkiye", "date_display": "2015, September 18–20", "location": "Trabzon, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/280134261_Mineral_Contents_of_Meat_and_Digestive_Glands_of_Scallops_Flexopecten_glaber_Catched_in_Canakkale_Strait_Turkey", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2013, "sort_date": "2013-09-03", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Gökkuşağı Alabalığı (<em>Oncorhynchus mykiss</em>) Kroketlerinin Soğuk Muhafazada (+4ºC) Raf Ömrünün Belirlenmesi", "event": "17. Ulusal Su Ürünleri Sempozyumu", "date_place": "3–6 September 2013, İstanbul, Türkiye", "date_display": "2013, September 3–6", "location": "İstanbul, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831368_Gokkusagi_Alabaligi_Oncorhynchus_mykiss_Kroketlerinin_Soguk_Muhafazada_4C_Raf_Omrunun_Belirlenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2012, "sort_date": "2012-11-09", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Determination of Proximate Composition and Sensory Attributes of Scallop (<em>Flexopecten glaber</em>) Gonads", "event": "Turkish-Japanese Marine Forum, Harmonization of Bio-diversity and Marine Industries Symposium", "date_place": "9–12 November 2012, Türkiye", "date_display": "2012, November 9–12", "location": "Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/314209537_Determination_of_Proximate_Composition_and_Sensory_Attributes_of_Scallop_Flexopecten_glaber_Gonads", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2012, "sort_date": "2012-11-09", "authors": "Çankırılıgil E.C., Berik N.", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Production of Croquettes from Deep-Water Rose Shrimp (<em>Parapenaeus longirostris</em>) Meat", "event": "Turkish-Japanese Marine Forum, Harmonization of Bio-diversity and Marine Industries Symposium", "date_place": "9–12 November 2012, Çanakkale, Türkiye", "date_display": "2012, November 9–12", "location": "Çanakkale, Türkiye", "tags": ["poster presentation", "international symposium"], "rg": "https://www.researchgate.net/publication/261830662_Production_of_Croquettes_from_Deep-Water_Rose_Shrimp_Parapenaeus_longirostris_Meat", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2011, "sort_date": "2011-10-25", "authors": "Berik N., Çankırılıgil E.C.", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Çanakkale Balık Halinden Temin Edilen Deniz Tarağına (<em>Flexopecten glaber</em>) Farklı Pişirme Tekniklerinin Uygulanması", "event": "16. Ulusal Su Ürünleri Sempozyumu", "date_place": "25–27 October 2011, Antalya, Türkiye", "date_display": "2011, October 25–27", "location": "Antalya, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831190_Canakkale_Balik_Halinden_Temin_Edilen_Deniz_Taragina_Flexopecten_glaber_Farkli_Pisirme_Tekniklerinin_Uygulanmasi", "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "conference presentations", "year": 2010, "sort_date": "2010-07-06", "authors": "Berik N., Kahraman D., Çankırılıgil E.C.", "cite_authors": "Berik, N., Kahraman, D., & Çankırılıgil, E. C.", "title_html": "Alabalık (<em>Oncorhynchus mykiss</em>) Marinatlarının Duyusal ve Besin Değeri Bakımından Değerlendirilmesi", "event": "2. Ulusal Alabalık Sempozyumu", "date_place": "6–8 July 2010, Karaman, Türkiye", "date_display": "2010, July 6–8", "location": "Karaman, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831194_Alabalik_Oncorhynchus_mykiss_Marinatlarinin_Duyusal_ve_Besin_Degeri_Bakimindan_Degerlendirilmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "conference presentations", "year": 2010, "sort_date": "2010-07-06", "authors": "Berik N., Çankırılıgil E.C., Kahraman D.", "cite_authors": "Berik, N., Çankırılıgil, E. C., & Kahraman, D.", "title_html": "Alabalık (<em>Oncorhynchus mykiss</em>) Eti Kullanılarak Hazırlanan Kroketlerin Besin Bileşimi ve Duyusal Analizleri Açısından İncelenmesi", "event": "2nd National Trout Symposium", "date_place": "6–8 July 2010, Karaman, Türkiye", "date_display": "2010, July 6–8", "location": "Karaman, Türkiye", "tags": ["poster presentation", "national symposium"], "rg": "https://www.researchgate.net/publication/261831381_Alabalik_Oncorhynchus_mykiss_Eti_Kullanilarak_Hazirlanan_Kroketlerin_Besin_Bilesimi_ve_Duyusal_Analizleri_Acisindan_Incelenmesi", "links": [], "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "other presentations", "year": 2024, "sort_date": "2024-11-09", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Marine Life in Antarctica", "event": "Maltepe Kadir Has Science and Art Center, Student Seminar", "date_place": "9 November 2024, İstanbul, Türkiye", "date_display": "2024, November 9", "location": "İstanbul, Türkiye", "tags": ["invited speaker", "seminar"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2023, "sort_date": "2023-12-05", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Algae in Extreme Climate Conditions: The Case of Horseshoe Island", "event": "Horseshoe Island and Glacial Lakes Biodiversity Workshop", "date_place": "5–6 December 2023, Erzurum, Türkiye", "date_display": "2023, December 5–6", "location": "Erzurum, Türkiye", "tags": ["invited speaker", "workshop"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2023, "sort_date": "2023-07-01", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "7th National Turkish Antarctic Expedition", "event": "T.C. Ministry of Agriculture and Forest, I. Regional Group Meeting", "date_place": "July 2023, Yalova, Türkiye", "date_display": "2023, July", "location": "Yalova, Türkiye", "tags": ["oral presentation", "meeting"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2023, "sort_date": "2023-06-01", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Studies that carried out in 7th National Turkish Antarctic Expedition", "event": "Career Talks in ÇOMÜ Marine Science and Technology Faculty", "date_place": "June 2023, Çanakkale, Türkiye", "date_display": "2023, June", "location": "Çanakkale, Türkiye", "tags": ["invited speaker", "seminar"], "rg": null, "links": [], "sdgs": ["sdg13", "sdg14"]}, {"section": "other presentations", "year": 2022, "sort_date": "2022-12-01", "authors": "Çankırılıgil E.C., Ak İ., Türker G., Kara A., Veske E., Apaydın Yağcı M., Kocabaş E., Berik N.", "cite_authors": "Çankırılıgil, E. C., Ak, İ., Türker, G., Kara, A., Veske, E., Apaydın Yağcı, M., Kocabaş, E., & Berik, N.", "title_html": "Biological Activity Evaluation of Macroalgae Distributed on Horseshoe Island (Antarctica) Coasts by Determining Nutrient Composition and Phytochemical Contents – Project Display", "event": "6. National Polar Science Workshop", "date_place": "1 December 2022, Trabzon, Türkiye", "date_display": "2022, December 1", "location": "Trabzon, Türkiye", "tags": ["oral presentation", "workshop"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg3", "sdg14"]}, {"section": "other presentations", "year": 2022, "sort_date": "2022-06-22", "authors": "Çankırılıgil E.C.", "cite_authors": "Çankırılıgil, E. C.", "title_html": "Studies on Macroalgae Culture", "event": "Workshop of Blue Economy and Aquatic Plants", "date_place": "22–23 June 2022, Antalya, Türkiye", "date_display": "2022, June 22–23", "location": "Antalya, Türkiye", "tags": ["oral presentation", "workshop"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}, {"section": "other presentations", "year": 2017, "sort_date": "2017-10-24", "authors": "Çankırılıgil E.C., Çakmak E., Özel O.T., Kasapoğlu N., Alp Erbay E., Özcan Akpınar İ.", "cite_authors": "Çankırılıgil, E. C., Çakmak, E., Özel, O. T., Kasapoğlu, N., Alp Erbay, E., & Özcan Akpınar, İ.", "title_html": "An Overview on Biology, Biochemistry and Aquaculture of the 5th Culture Generation of Black Sea Trout (<em>Salmo trutta labrax</em>) Considering Recent Studies", "event": "Workshop on Aquaculture in the Black Sea: Potential and Opportunities", "date_place": "24–26 October 2017, Trabzon, Türkiye", "date_display": "2017, October 24–26", "location": "Trabzon, Türkiye", "tags": ["oral presentation", "workshop"], "rg": null, "links": [], "sdgs": ["sdg2", "sdg14"]}];

    const conferenceList = document.getElementById('conferenceList');
    const otherList = document.getElementById('otherList');
    const toggleBtn = document.getElementById('filterToggle');
    const panel = document.getElementById('filterPanel');
    const closeBtn = document.getElementById('closeFilters');
    const clearBtn = document.getElementById('clearFilters');
    const allCheckbox = document.getElementById('filterAll');
    const visibleCountEl = document.getElementById('visibleCount');
    const totalCountEl = document.getElementById('totalCount');
    const emptyState = document.getElementById('presentationEmpty');

    const countMap = {
      all: document.getElementById('countAll'),
      'conference presentations': document.getElementById('countConference'),
      'other presentations': document.getElementById('countOther'),
      'oral presentation': document.getElementById('countOral'),
      'poster presentation': document.getElementById('countPoster'),
      'full-text': document.getElementById('countFullText'),
      'invited speaker': document.getElementById('countInvited'),
      'international symposium': document.getElementById('countInternational'),
      'national symposium': document.getElementById('countNational'),
      'virtual': document.getElementById('countVirtual'),
      'workshop': document.getElementById('countWorkshop'),
      'seminar': document.getElementById('countSeminar'),
      'meeting': document.getElementById('countMeeting')
    };

    function highlightSelf(authorText) {
      return authorText
        .replace(/Çankırılıgil E\. C\./g, '<span class="self-author">Çankırılıgil E. C.</span>')
        .replace(/Çankırılıgil E\.C\./g, '<span class="self-author">Çankırılıgil E.C.</span>');
    }

    function escapeHtml(text) {
      return text
        .replace(/&/g, '&amp;')
        .replace(/</g, '&lt;')
        .replace(/>/g, '&gt;')
        .replace(/"/g, '&quot;')
        .replace(/'/g, '&#039;');
    }

    function buildApaCitation(entry) {
      return `${entry.cite_authors} (${entry.date_display}). ${entry.title_html.replace(/<[^>]*>/g, '')} [Conference presentation]. ${entry.event}, ${entry.location}.`;
    }

    function createLinkControls(entry) {
      const wrapper = document.createElement('span');
      wrapper.className = 'presentation-links';

      if (entry.rg) {
        const rg = document.createElement('a');
        rg.className = 'presentation-link rg';
        rg.href = entry.rg;
        rg.target = '_blank';
        rg.rel = 'noopener';
        rg.setAttribute('aria-label', 'ResearchGate link');
        rg.innerHTML = `<img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">`;
        wrapper.appendChild(rg);
      }

      entry.links.forEach(url => {
        const extra = document.createElement('a');
        extra.className = 'presentation-link';
        extra.href = url;
        extra.target = '_blank';
        extra.rel = 'noopener';
        extra.setAttribute('aria-label', 'External link');
        extra.textContent = '🔗';
        wrapper.appendChild(extra);
      });

      if (entry.sdgs && entry.sdgs.length) {
        const sdgWrap = document.createElement('span');
        sdgWrap.className = 'sdg-wrap';
        sdgWrap.innerHTML = `
          <button class="sdg-trigger" type="button" aria-label="Show SDGs">
            <img src="{{ '/assets/img/sdgicon.png' | relative_url }}" alt="SDGs">
          </button>
          <div class="sdg-popover">
            <div class="sdg-icons">
              ${entry.sdgs.map(sdg => `<img src="{{ '/assets/img/' | relative_url }}${sdg}.png" alt="${sdg.toUpperCase().replace('SDG', 'SDG ')}">`).join('')}
            </div>
          </div>
        `;
        wrapper.appendChild(sdgWrap);
      }

      const citeWrap = document.createElement('span');
      citeWrap.className = 'cite-wrap';
      const citation = buildApaCitation(entry);
      citeWrap.innerHTML = `
        <button class="cite-trigger" type="button">Cite</button>
        <div class="cite-popover">
          <div class="cite-label">APA 7th</div>
          <div class="cite-text">${escapeHtml(citation)}</div>
          <button class="copy-cite-btn" type="button">Copy</button>
        </div>
      `;
      wrapper.appendChild(citeWrap);

      return wrapper;
    }

    function createEntry(entry) {
      const item = document.createElement('div');
      item.className = 'presentation-entry';
      item.dataset.tags = [entry.section].concat(entry.tags).join(',');
      item.dataset.section = entry.section;
      item.dataset.date = entry.sort_date;

      const meta = document.createElement('div');
      meta.className = 'presentation-meta';

      const chips = document.createElement('div');
      chips.className = 'presentation-chips';
      entry.tags.forEach(tag => {
        const chip = document.createElement('span');
        chip.className = 'presentation-chip';
        chip.textContent = tag.charAt(0).toUpperCase() + tag.slice(1);
        chips.appendChild(chip);
      });

      const linksHtml = createLinkControls(entry).outerHTML;

      item.innerHTML = `
        <div class="presentation-year">${entry.year}</div>
        <div class="presentation-text">
          ${highlightSelf(entry.authors)},
          <span class="presentation-title">${entry.title_html}</span>.
          <span class="presentation-event">${entry.event}</span>, ${entry.date_place}.${linksHtml}
        </div>
      `;
      meta.appendChild(chips);
      item.appendChild(meta);
      return item;
    }

    entries.sort((a, b) => b.sort_date.localeCompare(a.sort_date));

    entries.forEach(entry => {
      const node = createEntry(entry);
      if (entry.section === 'conference presentations') {
        conferenceList.appendChild(node);
      } else {
        otherList.appendChild(node);
      }
    });

    const renderedEntries = Array.from(document.querySelectorAll('.presentation-entry'));
    const checkboxes = Array.from(panel.querySelectorAll('input[type="checkbox"]'));

    function normalizeTag(tag) {
      return tag.trim().toLowerCase();
    }

    function getTags(entry) {
      return (entry.dataset.tags || '')
        .split(',')
        .map(normalizeTag)
        .filter(Boolean);
    }

    function updateStaticCounts() {
      const counts = {};
      renderedEntries.forEach(entry => {
        const tags = getTags(entry);
        counts.all = (counts.all || 0) + 1;
        tags.forEach(tag => counts[tag] = (counts[tag] || 0) + 1);
      });
      Object.keys(countMap).forEach(key => {
        if (countMap[key]) countMap[key].textContent = `(${counts[key] || 0})`;
      });
      totalCountEl.textContent = renderedEntries.length;
    }

    function applyFilters() {
      const selected = checkboxes
        .filter(cb => cb.checked && cb.value !== 'all')
        .map(cb => normalizeTag(cb.value));

      let visibleCount = 0;

      renderedEntries.forEach(entry => {
        const tags = getTags(entry);
        const match = selected.length === 0 || selected.every(tag => tags.includes(tag));
        entry.style.display = match ? '' : 'none';
        if (match) visibleCount += 1;
      });

      visibleCountEl.textContent = visibleCount;
      emptyState.style.display = visibleCount === 0 ? 'block' : 'none';
      allCheckbox.checked = selected.length === 0;
    }

    function clearAllFilters() {
      checkboxes.forEach(cb => cb.checked = false);
      allCheckbox.checked = true;
      applyFilters();
    }

    toggleBtn.addEventListener('click', function () {
      panel.classList.toggle('open');
    });

    closeBtn.addEventListener('click', function () {
      panel.classList.remove('open');
    });

    clearBtn.addEventListener('click', function () {
      clearAllFilters();
    });

    allCheckbox.addEventListener('change', function () {
      if (allCheckbox.checked) clearAllFilters();
    });

    checkboxes.forEach(cb => {
      if (cb !== allCheckbox) {
        cb.addEventListener('change', function () {
          if (cb.checked) allCheckbox.checked = false;
          applyFilters();
        });
      }
    });

    document.addEventListener('click', function (event) {
      if (!panel.contains(event.target) && !toggleBtn.contains(event.target)) {
        panel.classList.remove('open');
      }
    });

    document.addEventListener('click', function (event) {
      const sdgBtn = event.target.closest('.sdg-trigger');
      const citeBtn = event.target.closest('.cite-trigger');
      const copyBtn = event.target.closest('.copy-cite-btn');

      if (sdgBtn) {
        event.stopPropagation();
        const wrap = sdgBtn.closest('.sdg-wrap');
        document.querySelectorAll('.sdg-wrap.open').forEach(el => { if (el !== wrap) el.classList.remove('open'); });
        wrap.classList.toggle('open');
        return;
      }

      if (citeBtn) {
        event.stopPropagation();
        const wrap = citeBtn.closest('.cite-wrap');
        document.querySelectorAll('.cite-wrap.open').forEach(el => { if (el !== wrap) el.classList.remove('open'); });
        wrap.classList.toggle('open');
        return;
      }

      if (copyBtn) {
        const wrap = copyBtn.closest('.cite-wrap');
        const citation = wrap.querySelector('.cite-text').textContent;
        navigator.clipboard.writeText(citation).then(() => {
          copyBtn.textContent = 'Copied';
          setTimeout(() => copyBtn.textContent = 'Copy', 1200);
        }).catch(() => {
          copyBtn.textContent = 'Copy failed';
          setTimeout(() => copyBtn.textContent = 'Copy', 1200);
        });
        return;
      }

      document.querySelectorAll('.sdg-wrap.open, .cite-wrap.open').forEach(el => {
        if (!el.contains(event.target)) el.classList.remove('open');
      });
    });

    updateStaticCounts();
    clearAllFilters();
  })();
</script>
