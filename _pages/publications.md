---
layout: page
title: Publications
permalink: /publications/
nav: true
nav_order: 4
description: Publications.
---

<style>
  .pub-controls { display:flex; justify-content:flex-end; margin-bottom:1rem; position:relative; }
  .filter-toggle { border:1px solid var(--global-divider-color); background:var(--global-bg-color); color:var(--global-text-color); padding:0.45rem 0.9rem; border-radius:999px; cursor:pointer; font-size:0.95rem; }
  .filter-panel { display:none; position:absolute; top:2.7rem; right:0; z-index:20; width:min(380px,94vw); padding:0.95rem; border:1px solid var(--global-divider-color); border-radius:14px; background:var(--global-bg-color); box-shadow:0 8px 24px rgba(0,0,0,0.08); }
  .filter-panel.open { display:block; }
  .filter-title { font-weight:700; margin-bottom:0.35rem; }
  .filter-subtitle { font-size:0.88rem; color:var(--global-theme-color); margin-bottom:0.7rem; }
  .filter-group { margin-bottom:0.85rem; }
  .filter-group-title { font-weight:700; font-size:0.9rem; margin-bottom:0.35rem; }
  .filter-options { display:flex; flex-wrap:wrap; gap:0.45rem 0.8rem; }
  .filter-options label { display:inline-flex; align-items:center; gap:0.35rem; font-size:0.92rem; cursor:pointer; }
  .filter-options .count { color:var(--global-theme-color); font-size:0.85rem; }
  .filter-actions { display:flex; justify-content:space-between; margin-top:0.8rem; gap:0.6rem; }
  .filter-btn { border:1px solid var(--global-divider-color); background:var(--global-bg-color); color:var(--global-text-color); padding:0.4rem 0.8rem; border-radius:999px; cursor:pointer; font-size:0.9rem; }
  .pub-section-title { margin:1.25rem 0 0.6rem 0; }
  .pub-list { display:flex; flex-direction:column; }
  .pub-entry { display:grid; grid-template-columns:100px 1fr; gap:1rem; align-items:start; padding:0.95rem 0; border-bottom:1px solid color-mix(in srgb, var(--global-divider-color) 70%, transparent 30%); }
  .pub-entry:last-child { border-bottom:none; }
  .pub-thumb { width:100px; height:140px; display:flex; align-items:center; justify-content:center; overflow:hidden; border:1px solid var(--global-divider-color); border-radius:8px; background:#fff; }
  .pub-thumb img { width:100%; height:100%; object-fit:contain; object-position:center; display:block; background:#fff; }
  .pub-year { color:var(--global-theme-color); font-weight:700; margin-bottom:0.18rem; }
  .pub-text { line-height:1.65; color:var(--global-text-color); }
  .self-author { color:var(--global-theme-color); font-weight:700; }
  .pub-title { font-weight:700; color:var(--global-text-color); }
  .pub-links-inline { display:inline-flex; align-items:center; gap:0.45rem; margin-left:0.35rem; vertical-align:middle; flex-wrap:wrap; }
  .pub-link { display:inline-flex; align-items:center; justify-content:center; text-decoration:none; color:var(--global-theme-color); line-height:1; cursor:pointer; background:none; border:none; padding:0; font-size:0.95rem; }
  .pub-link:hover { opacity:0.8; text-decoration:none; }
  .sdg-wrap, .cite-wrap { position:relative; display:inline-flex; align-items:center; }
  .sdg-trigger, .cite-trigger { display:inline-flex; align-items:center; justify-content:center; padding:0; background:none; border:none; color:var(--global-theme-color); cursor:pointer; font-size:0.95rem; line-height:1; }
  .sdg-trigger img { width:16px; height:16px; display:block; }
  .sdg-popover, .cite-popover { display:none; position:absolute; top:1.8rem; left:0; z-index:15; min-width:240px; max-width:min(92vw,420px); padding:0.7rem; border:1px solid var(--global-divider-color); border-radius:12px; background:var(--global-bg-color); box-shadow:0 8px 24px rgba(0,0,0,0.08); }
  .sdg-wrap.open .sdg-popover, .cite-wrap.open .cite-popover { display:block; }
  .sdg-icons { display:flex; flex-wrap:wrap; gap:0.4rem; }
  .sdg-icons img { width:36px; height:36px; object-fit:contain; display:block; }
  .cite-label { font-weight:700; margin-bottom:0.35rem; font-size:0.9rem; }
  .cite-text { font-size:0.88rem; line-height:1.55; color:var(--global-text-color); margin-bottom:0.45rem; }
  .copy-cite-btn { border:1px solid var(--global-divider-color); background:var(--global-bg-color); color:var(--global-text-color); padding:0.28rem 0.7rem; border-radius:999px; cursor:pointer; font-size:0.82rem; }
  .pub-meta-row { display:flex; justify-content:space-between; align-items:flex-start; gap:1rem; margin-top:0.55rem; }
  .pub-chips { display:flex; flex-wrap:wrap; gap:0.45rem; }
  .pub-chip { display:inline-flex; align-items:center; padding:0.22rem 0.55rem; border-radius:999px; background:color-mix(in srgb, var(--global-divider-color) 20%, transparent 80%); color:#111; font-size:0.82rem; line-height:1.2; }
  .citation-count { white-space:nowrap; font-size:0.88rem; color:var(--global-text-color); }
  .citation-note { margin-top:1.5rem; font-size:0.88rem; color:#777; font-style:italic; }
  .pub-empty { display:none; margin-top:1rem; color:var(--global-text-color); }
  @media (max-width:768px) { .pub-entry{grid-template-columns:76px 1fr; gap:0.85rem;} .pub-thumb{width:76px; height:108px;} .pub-meta-row{flex-direction:column; align-items:flex-start; gap:0.6rem;} }
</style>

<div class="section-card">
  <div class="pub-controls">
    <button class="filter-toggle" type="button" id="filterToggle">Filter</button>
    <div class="filter-panel" id="filterPanel">
      <div class="filter-title">Filter publications</div>
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
          <label><input type="checkbox" value="articles"> Publications <span class="count" id="countArticles">(0)</span></label>
          <label><input type="checkbox" value="book sections"> Book sections <span class="count" id="countBookSections">(0)</span></label>
        </div>
      </div>
      <div class="filter-group">
        <div class="filter-group-title">Indexes</div>
        <div class="filter-options">
          <label><input type="checkbox" value="SCI"> SCI <span class="count" id="countSCI">(0)</span></label>
          <label><input type="checkbox" value="Q2"> Q2 <span class="count" id="countQ2">(0)</span></label>
          <label><input type="checkbox" value="Q3"> Q3 <span class="count" id="countQ3">(0)</span></label>
          <label><input type="checkbox" value="Q4"> Q4 <span class="count" id="countQ4">(0)</span></label>
          <label><input type="checkbox" value="E-SCI"> E-SCI <span class="count" id="countESCI">(0)</span></label>
          <label><input type="checkbox" value="SCOPUS"> SCOPUS <span class="count" id="countSCOPUS">(0)</span></label>
          <label><input type="checkbox" value="TRDizin"> TRDizin <span class="count" id="countTRDizin">(0)</span></label>
          <label><input type="checkbox" value="Zoological Record"> Zoological Record <span class="count" id="countZR">(0)</span></label>
          <label><input type="checkbox" value="Other International Indexes"> International Index <span class="count" id="countInternationalIndex">(0)</span></label>
          <label><input type="checkbox" value="Book section"> Book section <span class="count" id="countBookSectionTag">(0)</span></label>
          <label><input type="checkbox" value="International"> International <span class="count" id="countInternational">(0)</span></label>
          <label><input type="checkbox" value="National"> National <span class="count" id="countNational">(0)</span></label>
        </div>
      </div>
      <div class="filter-actions">
        <button class="filter-btn" type="button" id="clearFilters">Clear</button>
        <button class="filter-btn" type="button" id="closeFilters">Close</button>
      </div>
    </div>
  </div>

  <h2 class="section-title">Publications</h2>
  <div class="pub-list" id="articleList"></div>

  <h2 class="section-title pub-section-title">Book Sections</h2>
  <div class="pub-list" id="bookList"></div>

  <p class="pub-empty" id="pubEmpty">No publications match the selected filters.</p>
  <p class="citation-note">*Citation counts were obtained from Google Scholar and are subject to change.</p>
</div>

<script>
(function () {
  const entries = [{"section": "articles", "year": 2026, "sort_date": "2026-01-01", "authors_html": "Ak İ., <span class=\"self-author\">Çankırılıgil E. C.</span>,", "cite_authors": "Ak, İ., & Çankırılıgil, E. C.", "title_html": "Biodiversity and Distribution Patterns of Benthic Macroalgae on Horseshoe Island, Antarctica, with New Records", "source_html": "<em>Polar Biology</em>, 49(13).", "tags": ["articles", "SCI", "Q3"], "link": "https://link.springer.com/article/10.1007/s00300-026-03452-7", "citations": 0, "sdgs": ["sdg13", "sdg14"]}, {"section": "articles", "year": 2025, "sort_date": "2025-01-01", "authors_html": "<span class=\"self-author\">Çankırılıgil E. C.</span>, Berik N.,", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Unlocking the Nutritional Potential of Endemic Salmonid Species (Black Sea Salmon, <em>Salmo labrax</em>): Carotenoids and Their Impact on Fillet Characteristics", "source_html": "<em>Turkish Journal of Fisheries and Aquatic Sciences</em>, 25(12), 27539.", "tags": ["articles", "SCI", "Q2"], "link": "https://trjfas.org/abstract.php?id=15129", "citations": 0, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2024, "sort_date": "2024-01-01", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Altuntaş, A.", "cite_authors": "Çankırılıgil, E. C., & Altuntaş, A.", "title_html": "Chemical Composition of Two Grey Mullet Species (<em>Chelon auratus</em>, <em>Mugil cephalus</em>): A Comparative Study on Wild and Aquaculture-Adapted Species", "source_html": "<em>Çanakkale Onsekiz Mart University Journal of Marine Sciences and Fisheries</em>, 7(1), 52–66.", "tags": ["articles", "TRDizin", "Zoological Record"], "link": "https://dergipark.org.tr/tr/pub/jmsf/article/1494918", "citations": 3, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2023, "sort_date": "2023-12-31", "authors_html": "Özel O.T., <span class=\"self-author\">Çankırılıgil E.C.</span>, Ertürk-Gürkan S., Coşkun İ., Türe M.,", "cite_authors": "Özel, O. T., Çankırılıgil, E. C., Ertürk-Gürkan, S., Coşkun, İ., & Türe, M.", "title_html": "Influence of Laurel (<em>Laurus nobilis</em>) Essential Oil on Gut Function of Black Sea Salmon (<em>Salmo labrax</em>) Juveniles", "source_html": "<em>Tropical Animal Health and Production</em>, 54(6), 390.", "tags": ["articles", "SCI", "Q2"], "link": "https://link.springer.com/article/10.1007/s11250-022-03396-0", "citations": 7, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2023, "sort_date": "2023-12-30", "authors_html": "Özel O.T., Çakmak E., <span class=\"self-author\">Çankırılıgil E.C.</span>, Düzgüneş Z.D., Çimagil R., Batır E.,", "cite_authors": "Özel, O. T., Çakmak, E., Çankırılıgil, E. C., Düzgüneş, Z. D., Çimagil, R., & Batır, E.", "title_html": "Comparison of reproductive performance of Black Sea salmon broodstock (<em>Salmo labrax</em> PALLAS, 1814) reaching first sexual maturity at different ages", "source_html": "<em>Ege Journal of Fisheries and Aquatic Sciences</em>, 40(3), 166–173.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/en/download/article-file/2936281", "citations": 3, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2023, "sort_date": "2023-12-29", "authors_html": "Özel O.T., Çakmak E., <span class=\"self-author\">Çankırılıgil E.C.</span>, Çimagil R., Düzgüneş Z.D.,", "cite_authors": "Özel, O. T., Çakmak, E., Çankırılıgil, E. C., Çimagil, R., & Düzgüneş, Z. D.", "title_html": "Reproductive Performance of Hatchery-Originated Black Sea Salmon Broodstocks' (<em>Salmo labrax</em> PALLAS, 1814) F5 and F6 Filial Generations", "source_html": "<em>Acta Aquatica Turcica</em>, 40(3), 166–173.", "tags": ["articles", "TRDizin", "Zoological Record"], "link": "https://dergipark.org.tr/en/pub/actaquatr/article/1232320", "citations": 1, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2023, "sort_date": "2023-12-28", "authors_html": "Uslu, A.A., Özel, O.T., Örnekçi, G.N., Çelik, B., <span class=\"self-author\">Çankırılıgil, E.C.</span>, Çoşkun, İ., Uslu Şenel, G.,", "cite_authors": "Uslu, A. A., Özel, O. T., Örnekçi, G. N., Çelik, B., Çankırılıgil, E. C., Çoşkun, İ., & Uslu Şenel, G.", "title_html": "Insect Larval Meal as a Possible Alternative to Fish Meal in Rainbow Trout (<em>Oncorhynchus mykiss</em>) diets: Black Soldier Fly (<em>Hermetia illucens</em>), Mealworm (<em>Tenebrio molitor</em>)", "source_html": "<em>Journal of Limnology and Freshwater Fisheries Research</em>, 9(1), 43–52.", "tags": ["articles", "TRDizin"], "link": "https://dergipark.org.tr/en/pub/limnofish/article/1081945", "citations": 9, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2022, "sort_date": "2022-12-31", "authors_html": "Ak İ., <span class=\"self-author\">Çankırılıgil E.C.</span>, Türker G., Sever O., Abomohra A.", "cite_authors": "Ak, İ., Çankırılıgil, E. C., Türker, G., Sever, O., & Abomohra, A.", "title_html": "Enhancement of Antioxidant Properties of <em>Gongolaria barbata</em> (Phaeophyceae) by Optimization of Combined Light Intensity and Salinity Stress", "source_html": "<em>Phycologia</em>, 61(6), 584–594.", "tags": ["articles", "SCI", "Q3"], "link": "https://www.tandfonline.com/doi/abs/10.1080/00318884.2022.2099136", "citations": 9, "sdgs": ["sdg3", "sdg13", "sdg14"]}, {"section": "articles", "year": 2022, "sort_date": "2022-12-30", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Berik N., Çakmak E., Özel O.T., Alp-Erbay E.,", "cite_authors": "Çankırılıgil, E. C., Berik, N., Çakmak, E., Özel, O. T., & Alp-Erbay, E.", "title_html": "Dietary Carotenoids Influence Growth, Fillet Pigmentation, and Quality Characteristics of Black Sea Trout (<em>Salmo labrax</em> Pallas, 1814)", "source_html": "<em>Thalassas: An International Journal of Marine Sciences</em>, 38, 793–809.", "tags": ["articles", "SCI", "Q4"], "link": "https://link.springer.com/article/10.1007/s41208-022-00407-7", "citations": 7, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2022, "sort_date": "2022-12-29", "authors_html": "Çakmak E., Firidin Ş., Aksungur N., Çavdar Y., Kurtoğlu İ.Z., Aksungur M., Özel O.T., <span class=\"self-author\">Çankırılıgil E.C.</span>, Düzgüneş Z.D., Esin B.,", "cite_authors": "Çakmak, E., Firidin, Ş., Aksungur, N., Çavdar, Y., Kurtoğlu, İ. Z., Aksungur, M., Özel, O. T., Çankırılıgil, E. C., Düzgüneş, Z. D., & Esin, B.", "title_html": "Improving Reproductive Yield of the Black Sea Salmon (<em>Salmo labrax</em> PALLAS, 1814) with a Selective Breeding Program", "source_html": "<em>Aquatic Sciences and Engineering</em>, 37(3), 161–168.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/en/pub/ase/article/1079847", "citations": 7, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2022, "sort_date": "2022-12-28", "authors_html": "Veske E., <span class=\"self-author\">Çankırılıgil E.C.</span>, Yavuzcan Yıldız H.,", "cite_authors": "Veske, E., Çankırılıgil, E. C., & Yavuzcan Yıldız, H.", "title_html": "Seasonal Proximate Composition, Amino Acid and Trace Metal Contents of the Great Mediterranean scallop (<em>Pecten jacobaeus</em>) Collected from the Gulf of Antalya", "source_html": "<em>Journal of Anatolian Environmental and Animal Sciences</em>, 7(3), 358–366.", "tags": ["articles", "TRDizin"], "link": "https://dergipark.org.tr/en/pub/jaes/article/1111135", "citations": 6, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2022, "sort_date": "2022-12-27", "authors_html": "Berik N., <span class=\"self-author\">Çankırılıgil E.C.</span>, Ormancı H.B., Akyıldız A.,", "cite_authors": "Berik, N., Çankırılıgil, E. C., Ormancı, H. B., & Akyıldız, A.", "title_html": "Çanakkale Boğazı’ndan Toplanan Deniz Marulu (<em>Ulva rigida</em>)’nun Mevsimsel Besin İçeriğinin Belirlenerek Salata ve Çorba olarak Değerlendirilmesi", "source_html": "<em>Food and Health</em>, 8(2), 127–140.", "tags": ["articles", "TRDizin"], "link": "http://jfhs.scientificwebjournals.com/en/pub/article/993737", "citations": 4, "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "book sections", "year": 2022, "sort_date": "2022-01-01", "authors_html": "Ak İ., Koru E., Türker G., <span class=\"self-author\">Çankırılıgil E.C.</span>, Dereli M. G.,", "cite_authors": "Ak, İ., Koru, E., Türker, G., Çankırılıgil, E. C., & Dereli, M. G.", "title_html": "Chapter 3: Biochemical compounds of Algae: Sustainable Energy Sources for Biofuel Production", "source_html": "In <em>Handbook of Algal Biofuels: Aspects of Cultivation, Conversion and Biorefinery</em> (Ed., El-Sheekh M., Abomohra A. E.), Elsevier, 57–58.", "tags": ["book sections", "Book section", "International"], "link": "https://www.sciencedirect.com/science/chapter/edited-volume/abs/pii/B9780128237649000261", "citations": 0, "sdgs": ["sdg7", "sdg13", "sdg14"]}, {"section": "articles", "year": 2021, "sort_date": "2021-12-31", "authors_html": "Ak İ., <span class=\"self-author\">Çankırılıgil E.C.</span>, Türker G., Sever O.,", "cite_authors": "Ak, İ., Çankırılıgil, E. C., Türker, G., & Sever, O.", "title_html": "Assessment of Light Intensity and Salinity Regimes on the Element Levels of Brown Macroalgae, <em>Treptacantha barbata</em>: Application of Response Surface Methodology (RSM)", "source_html": "<em>Food Science and Technology</em>, 41(4), 1–9.", "tags": ["articles", "SCI", "Q3"], "link": "https://www.scielo.br/j/cta/a/y5QmLdzMRmWgN5BgRjzrzyP/?lang=en", "citations": 12, "sdgs": ["sdg2", "sdg14"]}, {"section": "book sections", "year": 2021, "sort_date": "2021-01-01", "authors_html": "Düzgüneş Z.D., <span class=\"self-author\">Çankırılıgil E.C.</span>, Beken A.T., Özel O.T., Cebeci A.,", "cite_authors": "Düzgüneş, Z. D., Çankırılıgil, E. C., Beken, A. T., Özel, O. T., & Cebeci, A.", "title_html": "Bölüm 7: Akuatik Biyoteknoloji", "source_html": "In <em>Biyoteknoloji</em> (Ed., Usta M.), Trabzon Üniversitesi.", "tags": ["book sections", "Book section", "National"], "link": "https://www.researchgate.net/publication/358647199_Akuatik_Biyoteknoloji", "citations": 0, "sdgs": ["sdg9", "sdg14"]}, {"section": "articles", "year": 2020, "sort_date": "2020-12-31", "authors_html": "Kasapoglu N., <span class=\"self-author\">Çankırılıgil E.C.</span>, Çakmak E., Özel O. T.,", "cite_authors": "Kasapoglu, N., Çankırılıgil, E. C., Çakmak, E., & Özel, O. T.", "title_html": "Meristic and Morphometric Characteristics of the Black Sea Salmon, <em>Salmo labrax</em> Pallas,1814 Culture Line: an Endemic Species for Eastern Black Sea", "source_html": "<em>Journal of Fisheries</em>, 8(3), 935–939.", "tags": ["articles", "E-SCI", "SCOPUS"], "link": "https://journal.bdfish.org/index.php/fisheries/article/view/JFish20250", "citations": 5, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2020, "sort_date": "2020-12-30", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Berik N., Alp Erbay E.,", "cite_authors": "Çankırılıgil, E. C., Berik, N., & Alp Erbay, E.", "title_html": "Optimization of Hydrolization Procedure for Amino Acid Analysis in Fish Meat with HPLC-DAD by Response Surface Methodology (RSM)", "source_html": "<em>Ege Journal of Fisheries and Aquatic Sciences</em>, 37(2), 113–123.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/en/download/article-file/884259", "citations": 14, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2020, "sort_date": "2020-12-29", "authors_html": "Kasapoglu N., <span class=\"self-author\">Çankırılıgil E.C.</span>, Düzgüneş, Z.D., Çakmak E., Eroğlu, O.,", "cite_authors": "Kasapoglu, N., Çankırılıgil, E. C., Düzgüneş, Z. D., Çakmak, E., & Eroğlu, O.", "title_html": "The Bio-ecological and Genetic Characteristics of Sand Steenbras (<em>Lithognathus mormyrus</em>) in the Black Sea", "source_html": "<em>Journal of the Black Sea / Mediterranean Environment</em>, 26(3), 249–262.", "tags": ["articles", "Zoological Record"], "link": "https://blackmeditjournal.org/volumes-archive/vol-26-2020/vol-26-2020-no-3-2/the-bio-ecological-and-genetic-characteristics-of-sand-steenbras-lithognathus-mormyrus-in-the-black-sea/", "citations": 3, "sdgs": ["sdg14"]}, {"section": "articles", "year": 2020, "sort_date": "2020-12-28", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Berik N.,", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Chemical Composition of the Black Sea Trout (<em>Salmo labrax</em> Pallas, 1814): A Comparative Study", "source_html": "<em>Aquatic Research</em>, 3(4), 208–219.", "tags": ["articles", "TRDizin", "SCOPUS", "Zoological Record"], "link": "https://dergipark.org.tr/en/download/article-file/1265953", "citations": 7, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2019, "sort_date": "2019-12-31", "authors_html": "Berik N., <span class=\"self-author\">Çankırılıgil E.C.</span>,", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "The Elemental Composition of Green Seaweed (<em>Ulva rigida</em>) Collected from Çanakkale, Turkey", "source_html": "<em>Aquatic Sciences and Engineering</em>, 34(3), 74–79.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/en/pub/ase/article/557380", "citations": 30, "sdgs": ["sdg14"]}, {"section": "articles", "year": 2019, "sort_date": "2019-12-30", "authors_html": "Çakmak E., <span class=\"self-author\">Çankırılıgil E.C.</span>, Düzgüneş Z.D., Özel O.T., Eroğlu O., Firidin Ş.,", "cite_authors": "Çakmak, E., Çankırılıgil, E. C., Düzgüneş, Z. D., Özel, O. T., Eroğlu, O., & Firidin, Ş.", "title_html": "Triploid Black Sea Trout (<em>Salmo labrax</em> Pallas, 1814) Induced by Heat Shock and Evaluation of Triploidy with Different Techniques", "source_html": "<em>Genetics of Aquatic Organisms (GenAqua)</em>, 3(1), 01–07.", "tags": ["articles", "SCOPUS", "Zoological Record"], "link": "https://www.genaqua.org/uploads/pdf_24.pdf", "citations": 6, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2018, "sort_date": "2018-12-31", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Berik N.,", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Sensorial Evaluation of Fish Croquettes Produced from Different Seafood", "source_html": "<em>Aquatic Sciences and Engineering</em>, 3(3), 96–101.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/tr/download/article-file/496909", "citations": 11, "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "articles", "year": 2018, "sort_date": "2018-12-30", "authors_html": "Çakmak E., <span class=\"self-author\">Çankırılıgil E.C.</span>, Özel, O.T.,", "cite_authors": "Çakmak, E., Çankırılıgil, E. C., & Özel, O. T.", "title_html": "The Fifth Culture Generation of Black Sea Trout (<em>Salmo trutta labrax</em>): Culture Characteristics, Meat Yield and Proximate Composition", "source_html": "<em>Ege Journal of Fisheries and Aquatic Sciences</em>, 35(1), 103–110.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/en/download/article-file/439799", "citations": 16, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2018, "sort_date": "2018-12-29", "authors_html": "Özel, O.T., Çakmak E., Çoşkun, İ., <span class=\"self-author\">Çankırılıgil E.C.</span>,", "cite_authors": "Özel, O. T., Çakmak, E., Çoşkun, İ., & Çankırılıgil, E. C.", "title_html": "Evaluation of Growth Performance and Intestine Villi Morphology of Black Sea Trout (<em>Salmo trutta labrax</em>) Fed with Different Protein Levels Containing Diets", "source_html": "<em>Ege Journal of Fisheries and Aquatic Sciences</em>, 35(2), 125–130.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/tr/download/article-file/491124", "citations": 15, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2017, "sort_date": "2017-12-31", "authors_html": "Berik N., <span class=\"self-author\">Çankırılıgil E.C.</span>, Gül G.,", "cite_authors": "Berik, N., Çankırılıgil, E. C., & Gül, G.", "title_html": "Mineral Content of Smooth Scallop (<em>Flexopecten glaber</em>) Caught Canakkale, Turkey and Evaluation in terms of Food Safety", "source_html": "<em>Journal of Trace Elements in Medicine and Biology</em>, 42, 97–102.", "tags": ["articles", "SCI", "Q2"], "link": "https://www.sciencedirect.com/science/article/abs/pii/S0946672X16304369", "citations": 36, "sdgs": ["sdg2", "sdg3", "sdg14"]}, {"section": "articles", "year": 2017, "sort_date": "2017-12-30", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Berik N.,", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Effects of Deep-Frying to Sardine Croquettes’ Chemical Composition", "source_html": "<em>Ege Journal of Fisheries and Aquatic Sciences</em>, 34(3), 293–302.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/en/download/article-file/313128", "citations": 11, "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "articles", "year": 2017, "sort_date": "2017-12-29", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Berik N.,", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Gökkuşağı Alabalığı (<em>Oncorhynchus mykiss</em>) Kroketlerinin Soğuk Muhafazada (+4°C) Raf Ömrünün Belirlenmesi", "source_html": "<em>Turkish Journal of Aquatic Sciences</em>, 32, 35–48.", "tags": ["articles", "E-SCI", "TRDizin", "SCOPUS"], "link": "https://dergipark.org.tr/tr/download/article-file/270559", "citations": 13, "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "articles", "year": 2017, "sort_date": "2017-12-28", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Alp Erbay, E.,", "cite_authors": "Çankırılıgil, E. C., & Alp Erbay, E.", "title_html": "Effect of different thawing techniques on color of Black Sea trout (<em>Salmo labrax</em> PALLAS, 1814) fillets", "source_html": "<em>International Journal of Agriculture, Environment and Food Sciences</em>, 1(1), 27–32.", "tags": ["articles", "TRDizin"], "link": "https://dergipark.org.tr/en/pub/jaefs/article/348552", "citations": 2, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2017, "sort_date": "2017-12-27", "authors_html": "<span class=\"self-author\">Çankırılıgil E.C.</span>, Berik N.,", "cite_authors": "Çankırılıgil, E. C., & Berik, N.", "title_html": "Changes in Fatty Acid and Mineral Compositions of Rose-Shrimp Croquettes during Production Process", "source_html": "<em>American Journal of Food Technology</em>, 12(4), 254–261.", "tags": ["articles", "Other International Indexes"], "link": "https://scialert.net/abstract/?doi=ajft.2017.254.261", "citations": 12, "sdgs": ["sdg2", "sdg12", "sdg14"]}, {"section": "articles", "year": 2017, "sort_date": "2017-12-26", "authors_html": "Berik N., <span class=\"self-author\">Çankırılıgil E.C.</span>, Gül, G.,", "cite_authors": "Berik, N., Çankırılıgil, E. C., & Gül, G.", "title_html": "Meat Yield and Shell Dimension of Smooth Scallop (<em>Flexopecten glaber</em>) Caught from Cardak Lagoon in Canakkale, Turkey", "source_html": "<em>Journal of Aquaculture & Marine Biology (JAMB)</em>, 5:3, 122.", "tags": ["articles", "Other International Indexes"], "link": "http://medcraveonline.com/JAMB/JAMB-05-00122.pdf", "citations": 23, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2016, "sort_date": "2016-12-31", "authors_html": "Kasapoğlu N., <span class=\"self-author\">Çankırılıgil E.C.</span>, Firidin Ş., Çakmak E.,", "cite_authors": "Kasapoğlu, N., Çankırılıgil, E. C., Firidin, Ş., & Çakmak, E.", "title_html": "A Preliminary Study of Some Biological Characters for the Black Sea, Turkey: East Atlantic Peacock Wrasse, <em>Symphodus tinca</em>", "source_html": "<em>International Journal of the Black Sea / Mediterranean Environment</em>, 22:3, 289–294.", "tags": ["articles", "SCOPUS", "Zoological Record"], "link": "https://blackmeditjournal.org/volumes-archive/vol22-2016/vol-22-2016-no-3/a-preliminary-study-on-some-biological-characters-of-east-atlantic-peacock-wrasse-symphodus-tinca-in-the-black-sea-turkey/", "citations": 6, "sdgs": ["sdg14"]}, {"section": "articles", "year": 2013, "sort_date": "2013-12-31", "authors_html": "Berik N., <span class=\"self-author\">Çankırılıgil E.C.</span>,", "cite_authors": "Berik, N., & Çankırılıgil, E. C.", "title_html": "Determination of Proximate Composition and Sensory Attributes of Scallop (<em>Flexopecten glaber</em>) Gonads", "source_html": "<em>Marine Science and Technology Bulletin</em>, 3, 5–8.", "tags": ["articles", "Other International Indexes"], "link": "https://dergipark.org.tr/en/download/article-file/207936", "citations": 18, "sdgs": ["sdg2", "sdg14"]}, {"section": "articles", "year": 2011, "sort_date": "2011-12-31", "authors_html": "Berik N., <span class=\"self-author\">Çankırılıgil E.C.</span>, Kahraman D.,", "cite_authors": "Berik, N., Çankırılıgil, E. C., & Kahraman, D.", "title_html": "Determination of Quality Attributes and Production of Fingers from Rainbow Trout (<em>Oncorhynchus mykiss</em>) Fillet", "source_html": "<em>Kafkas Univ Vet Fak Derg</em>, 17, 735–740.", "tags": ["articles", "SCI", "Q2"], "link": "https://vetdergikafkas.org/uploads/pdf/pdf_KVFD_991.pdf", "citations": 13, "sdgs": ["sdg2", "sdg12", "sdg14"]}];
  const articleList = document.getElementById('articleList');
  const bookList = document.getElementById('bookList');
  const filterToggle = document.getElementById('filterToggle');
  const filterPanel = document.getElementById('filterPanel');
  const closeFilters = document.getElementById('closeFilters');
  const clearFilters = document.getElementById('clearFilters');
  const filterAll = document.getElementById('filterAll');
  const visibleCount = document.getElementById('visibleCount');
  const totalCount = document.getElementById('totalCount');
  const pubEmpty = document.getElementById('pubEmpty');
  const sdgIconPath = "{{ '/assets/img/sdgicon.png' | relative_url }}";
  const sdgBasePath = "{{ '/assets/img/' | relative_url }}";

  const countMap = {
    all: document.getElementById('countAll'),
    'articles': document.getElementById('countArticles'),
    'book sections': document.getElementById('countBookSections'),
    'SCI': document.getElementById('countSCI'),
    'Q2': document.getElementById('countQ2'),
    'Q3': document.getElementById('countQ3'),
    'Q4': document.getElementById('countQ4'),
    'E-SCI': document.getElementById('countESCI'),
    'SCOPUS': document.getElementById('countSCOPUS'),
    'TRDizin': document.getElementById('countTRDizin'),
    'Zoological Record': document.getElementById('countZR'),
    'Other International Indexes': document.getElementById('countInternationalIndex'),
    'Book section': document.getElementById('countBookSectionTag'),
    'International': document.getElementById('countInternational'),
    'National': document.getElementById('countNational')
  };

  function escapeHtml(text) {
    return String(text).replace(/&/g,'&amp;').replace(/</g,'&lt;').replace(/>/g,'&gt;').replace(/"/g,'&quot;').replace(/'/g,'&#039;');
  }

  function buildApaCitation(entry) {
    return `${entry.cite_authors} (${entry.year}). ${entry.title_html.replace(/<[^>]*>/g,'')}. ${entry.source_html.replace(/<[^>]*>/g,'')}`;
  }

  function createEntry(entry) {
    const node = document.createElement('div');
    node.className = 'pub-entry';
    node.dataset.tags = entry.tags.join(',');
    node.dataset.section = entry.section;
    const imgPath = `{{ '/assets/img/' | relative_url }}${entry.image}`;
    const citationHtml = entry.citations > 0 ? `<div class="citation-count">Cited by ${entry.citations}</div>` : '';
    node.innerHTML = `
      <div class="pub-thumb"><img src="${imgPath}" alt="${entry.image}"></div>
      <div class="pub-body">
        <div class="pub-year">${entry.year}</div>
        <div class="pub-text">
          ${entry.authors_html}
          <span class="pub-title">${entry.title_html}</span>.
          ${entry.source_html}
          <span class="pub-links-inline">
            <a class="pub-link" href="${entry.link}" target="_blank" rel="noopener" aria-label="Publication link">🔗</a>
            <span class="sdg-wrap">
              <button class="sdg-trigger" type="button" aria-label="Show SDGs"><img src="${sdgIconPath}" alt="SDG"></button>
              <span class="sdg-popover"><span class="sdg-icons">${entry.sdgs.map(sdg => `<img src="${sdgBasePath}${sdg}.png" alt="${sdg.toUpperCase().replace('SDG','SDG ')}">`).join('')}</span></span>
            </span>
            <span class="cite-wrap">
              <button class="cite-trigger" type="button">Cite</button>
              <span class="cite-popover">
                <div class="cite-label">APA 7th</div>
                <div class="cite-text">${escapeHtml(buildApaCitation(entry))}</div>
                <button class="copy-cite-btn" type="button">Copy</button>
              </span>
            </span>
          </span>
        </div>
        <div class="pub-meta-row">
          <div class="pub-chips">${entry.tags.filter(t => t !== 'articles' && t !== 'book sections').map(t => `<span class="pub-chip">${escapeHtml(t)}</span>`).join('')}</div>
          ${citationHtml}
        </div>
      </div>`;
    return node;
  }

  function renderEntries() {
    entries.forEach(entry => {
      const node = createEntry(entry);
      if (entry.section === 'articles') articleList.appendChild(node);
      else bookList.appendChild(node);
    });
  }

  function getTags(node) {
    return (node.dataset.tags || '').split(',').map(s => s.trim()).filter(Boolean);
  }

  function updateCounts() {
    const nodes = Array.from(document.querySelectorAll('.pub-entry'));
    const counts = {};
    nodes.forEach(node => {
      counts.all = (counts.all || 0) + 1;
      counts[node.dataset.section] = (counts[node.dataset.section] || 0) + 1;
      getTags(node).forEach(tag => counts[tag] = (counts[tag] || 0) + 1);
    });
    Object.keys(countMap).forEach(key => { if (countMap[key]) countMap[key].textContent = `(${counts[key] || 0})`; });
    totalCount.textContent = nodes.length;
  }

  function applyFilters() {
    const selected = Array.from(filterPanel.querySelectorAll('input[type="checkbox"]'))
      .filter(cb => cb.checked && cb.value !== 'all')
      .map(cb => cb.value);

    const nodes = Array.from(document.querySelectorAll('.pub-entry'));
    let shown = 0, shownArticles = 0, shownBooks = 0;
    nodes.forEach(node => {
      const haystack = [...getTags(node), node.dataset.section];
      const match = selected.length === 0 || selected.every(tag => haystack.includes(tag));
      node.style.display = match ? '' : 'none';
      if (match) {
        shown++;
        if (node.dataset.section === 'articles') shownArticles++;
        if (node.dataset.section === 'book sections') shownBooks++;
      }
    });

    const titles = document.querySelectorAll('.section-title');
    if (titles[0]) titles[0].style.display = shownArticles ? '' : 'none';
    const bookTitle = document.querySelector('.pub-section-title');
    if (bookTitle) bookTitle.style.display = shownBooks ? '' : 'none';
    articleList.style.display = shownArticles ? '' : 'none';
    bookList.style.display = shownBooks ? '' : 'none';
    visibleCount.textContent = shown;
    pubEmpty.style.display = shown ? 'none' : 'block';
    filterAll.checked = selected.length === 0;
  }

  function clearAll() {
    Array.from(filterPanel.querySelectorAll('input[type="checkbox"]')).forEach(cb => cb.checked = false);
    filterAll.checked = true;
    applyFilters();
  }

  renderEntries();
  updateCounts();
  clearAll();

  filterToggle.addEventListener('click', () => filterPanel.classList.toggle('open'));
  closeFilters.addEventListener('click', () => filterPanel.classList.remove('open'));
  clearFilters.addEventListener('click', clearAll);
  filterAll.addEventListener('change', () => { if (filterAll.checked) clearAll(); });

  Array.from(filterPanel.querySelectorAll('input[type="checkbox"]')).forEach(cb => {
    if (cb !== filterAll) cb.addEventListener('change', () => { if (cb.checked) filterAll.checked = false; applyFilters(); });
  });

  document.addEventListener('click', e => {
    if (!filterPanel.contains(e.target) && !filterToggle.contains(e.target)) filterPanel.classList.remove('open');
    document.querySelectorAll('.sdg-wrap.open, .cite-wrap.open').forEach(el => { if (!el.contains(e.target)) el.classList.remove('open'); });
  });

  document.querySelectorAll('.sdg-trigger').forEach(btn => {
    btn.addEventListener('click', e => {
      e.stopPropagation();
      const wrap = btn.closest('.sdg-wrap');
      document.querySelectorAll('.sdg-wrap.open').forEach(el => { if (el !== wrap) el.classList.remove('open'); });
      wrap.classList.toggle('open');
    });
  });

  document.querySelectorAll('.cite-wrap').forEach(wrap => {
    const trigger = wrap.querySelector('.cite-trigger');
    const copyBtn = wrap.querySelector('.copy-cite-btn');
    const citation = wrap.querySelector('.cite-text').textContent;
    trigger.addEventListener('click', e => {
      e.stopPropagation();
      document.querySelectorAll('.cite-wrap.open').forEach(el => { if (el !== wrap) el.classList.remove('open'); });
      wrap.classList.toggle('open');
    });
    copyBtn.addEventListener('click', async () => {
      try { await navigator.clipboard.writeText(citation); copyBtn.textContent = 'Copied'; setTimeout(() => copyBtn.textContent = 'Copy', 1200); }
      catch { copyBtn.textContent = 'Copy failed'; setTimeout(() => copyBtn.textContent = 'Copy', 1200); }
    });
  });
})();
</script>
