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
    width: min(320px, 90vw);
    padding: 0.9rem;
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
    margin-bottom: 0.55rem;
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

  .presentation-links {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;
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

  .presentation-chips {
    display: flex;
    flex-wrap: wrap;
    gap: 0.45rem;
    margin-top: 0.55rem;
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
      <div class="filter-title">Select filters</div>
      <div class="filter-options">
        <label><input type="checkbox" value="oral presentation"> Oral presentation</label>
        <label><input type="checkbox" value="poster presentation"> Poster presentation</label>
        <label><input type="checkbox" value="full-text"> Full-text</label>
        <label><input type="checkbox" value="international symposium"> International symposium</label>
        <label><input type="checkbox" value="national symposium"> National symposium</label>
        <label><input type="checkbox" value="virtual"> Virtual</label>
        <label><input type="checkbox" value="workshop"> Workshop</label>
        <label><input type="checkbox" value="seminar"> Seminar</label>
        <label><input type="checkbox" value="meeting"> Meeting</label>
        <label><input type="checkbox" value="invited speaker"> Invited speaker</label>
      </div>
      <div class="filter-actions">
        <button class="filter-btn" type="button" id="clearFilters">Clear</button>
        <button class="filter-btn" type="button" id="closeFilters">Close</button>
      </div>
    </div>
  </div>

  <h2 class="section-title">Conference Presentations</h2>

  <div class="presentation-list" id="presentationList">

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2025-08-04" data-group="conference">
      <div class="presentation-year">2025</div>
      <div class="presentation-text">
        Apaydın Yağcı M., Yağcı A., <span class="self-author">Çankırılıgil E. C.</span>, Kocabaş E.,
        <span class="presentation-title">A Preliminary Study on the Zooplankton Fauna of Gölbaşı Lake (Bursa/Kestel – Türkiye)</span>.
        <span class="presentation-event">The XVII International Rotifer Symposium</span>, 4–8 August 2025, Rio de Janeiro, Brazil.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/394522886_A_preliminary_study_on_the_Rotifera_fauna_of_Golbasi_Lake_Kestel_Bursa-Turkiye" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,national symposium" data-date="2025-11-05" data-group="conference">
      <div class="presentation-year">2025</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Ak İ.,
        <span class="presentation-title">Antarktika Makroalgleri ve İklim Değişikliği: Horseshoe Adası Örneği</span>.
        <span class="presentation-event">National Polar Sciences Symposium</span>, 5–6 November 2025, İzmir, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/398987908_Antarctic_Macroalgae_and_Climate_Change_The_Case_of_Horseshoe_Island" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,national symposium" data-date="2024-11-08" data-group="conference">
      <div class="presentation-year">2024</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Ak İ., Türker G., Berik N.,
        <span class="presentation-title">Profiling Chemical Components of Seaweed Species from the Antarctic Peninsula</span>.
        <span class="presentation-event">8th National Polar Sciences Symposium</span>, 8 November 2024, Kocaeli, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/387327560_Profiling_Chemical_Components_of_Seaweed_Species_from_the_Antarctic_Peninsula" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2024-11-08" data-group="conference">
      <div class="presentation-year">2024</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Ak İ., Apaydın Yağcı M., Türker G., Kara A., Veske E., Kocabaş E., Berik N.,
        <span class="presentation-title">Snapshots of Marine Life at Horseshoe Island, Antarctica: Highlights from Underwater Observations and Specimen Collections</span>.
        <span class="presentation-event">8th National Polar Sciences Symposium</span>, 8 November 2024, Kocaeli, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/387327570_Snapshots_of_Marine_Life_at_Horseshoe_Island_Antarctica_Highlights_from_Underwater_Observations_and_Specimen_Collections" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2024-11-08" data-group="conference">
      <div class="presentation-year">2024</div>
      <div class="presentation-text">
        Ak İ., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Observations on the Diversity of Benthic Macroalgae Along the Shores of Horseshoe Island, Antarctica</span>.
        <span class="presentation-event">8th National Polar Sciences Symposium</span>, 8 November 2024, Gebze, Kocaeli, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/387327564_Observations_on_the_Diversity_of_Benthic_Macroalgae_Along_the_Shores_of_Horseshoe_Island_Antarctica" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,national symposium" data-date="2023-12-04" data-group="conference">
      <div class="presentation-year">2023</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Ak İ., Türker G., Kara A., Veske E., Apaydın Yağcı M., Kocabaş E., Berik N.,
        <span class="presentation-title">Antarktika Horseshoe Adası Makroalgleri: Yedinci Ulusal Antarktika Bilim Seferi Kapsamında Yapılan Çalışmalar</span>.
        <span class="presentation-event">7. Ulusal Kutup Bilimleri Sempozyumu</span>, 4 Aralık 2023, İstanbul, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/377223123_Macroalgae_of_Horseshoe_Island_Antarctica_Studies_Conducted_in_the_Seventh_National_Antarctic_Science_Expedition" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium,virtual" data-date="2022-09-20" data-group="conference">
      <div class="presentation-year">2022</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Nutritional Composition and Texture Profile of Wild and Culture Adapted Blue Crab (<em>Callinectes sapidus</em>) Meat</span>.
        <span class="presentation-event">The 8th Aquatic Biodiversity International Conference (ABIC 8)</span>, 20–22 September 2022, Sibiu, Transylvania, Romania.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/363668764_Nutritional_Composition_and_Texture_Profile_of_Wild_and_Culture_Adapted_Blue_Crab_Callinectes_sapidus_Meat" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
        <span class="presentation-chip">Virtual</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,national symposium" data-date="2022-09-15" data-group="conference">
      <div class="presentation-year">2022</div>
      <div class="presentation-text">
        Özel O.T., Çakmak E., <span class="self-author">Çankırılıgil E.C.</span>, Düzgüneş Z.D., Çimagil R.,
        <span class="presentation-title">Farklı Yaşlarda Cinsel Olgunluğa Ulaşan Karadeniz Somonu Anaçlarının (<em>Salmo labrax</em> PALLAS, 1811) Üreme Performansı</span>.
        <span class="presentation-event">6th National Trout Symposium</span>, 15–16 September 2022, Isparta, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/363668832_Ilk_Cinsel_Olgunluga_Farkli_Yaslarda_Ulasan_Karadeniz_Somonu_Anaclarinin_Salmo_labrax_PALLAS_1814_Ureme_Performansinin_Karsilastirilmasi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,national symposium" data-date="2022-09-15" data-group="conference">
      <div class="presentation-year">2022</div>
      <div class="presentation-text">
        Özel O.T., Çakmak E., <span class="self-author">Çankırılıgil E.C.</span>, Çimagil R., Düzgüneş Z.D.,
        <span class="presentation-title">Kuluçkahane Kökenli F5 ve F6 Nesil Karadeniz Somonu Anaçlarının (<em>Salmo labrax</em> PALLAS, 1811) Üreme Performansı İlişkisi</span>.
        <span class="presentation-event">6th National Trout Symposium</span>, 15–16 September 2022, Isparta, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/363668839_Kuluckahane_Kokenli_F5_ve_F6_Nesil_Karadeniz_Somonu_Anaclarinin_Salmo_labrax_PALLAS_1811_Ureme_Performansi_Iliskisi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2022-06-01" data-group="conference">
      <div class="presentation-year">2022</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">A Preliminary Study on the Antioxidant Activity and Amino Acid Composition of Marine Sponge <em>Aplysina aerophoba</em> Collected from Northeastern Aegean Sea</span>.
        <span class="presentation-event">5th National Marine Sciences Congress</span>, 1–3 June 2022, Trabzon, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/361109263_A_Preliminary_Study_on_the_Antioxidant_Activity_and_Amino_Acid_Composition_of_Marine_Sponge_Aplysina_aerophoba_Collected_from_Northeastern_Aegean_Sea" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium,virtual" data-date="2022-01-14" data-group="conference">
      <div class="presentation-year">2022</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Determination of Amino Acid Composition, Color and Texture Profile of Fresh and Processed Sea Cucumber (<em>Holothuria tubulosa</em>)</span>.
        <span class="presentation-event">Tokyo Summit-V, 5th International Conference on Innovative Studies of Contemporary Sciences</span>, 14–16 January 2022, Tokyo, Japan.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/357869097_Determination_of_Amino_Acid_Composition_Color_and_Texture_Profile_of_Fresh_and_Processed_Sea_Cucumber_Holothuria_tubulosa" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
        <span class="presentation-chip">Virtual</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,full-text,international symposium,virtual" data-date="2021-11-04" data-group="conference">
      <div class="presentation-year">2021</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Ak İ.,
        <span class="presentation-title">Amino Acid Composition of Seaweeds from Çanakkale, Turkey</span>.
        <span class="presentation-event">HydroMediT 2021 - 4th International Congress on Applied Ichthyology, Oceanography & Aquatic Environment</span>, 4–6 November 2021, Greece.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/356913912_Amino_Acid_Composition_of_Seaweeds_from_Canakkale_Turkey" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">Full-text</span>
        <span class="presentation-chip">International symposium</span>
        <span class="presentation-chip">Virtual</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,full-text,international symposium,virtual" data-date="2021-11-04" data-group="conference">
      <div class="presentation-year">2021</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Ak İ.,
        <span class="presentation-title">Amino Acid Composition of <em>Ceramium rubrum</em> (Rhodophyceae) from North Aegean Sea, Turkey</span>.
        <span class="presentation-event">HydroMediT 2021 - 4th International Congress on Applied Ichthyology, Oceanography & Aquatic Environment</span>, 4–6 November 2021, Greece.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/356914177_Amino_Acid_Composition_of_Ceramium_rubrum_Rhodophyceae_from_North_Aegean_Sea_Turkey" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">Full-text</span>
        <span class="presentation-chip">International symposium</span>
        <span class="presentation-chip">Virtual</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2021-10-01" data-group="conference">
      <div class="presentation-year">2021</div>
      <div class="presentation-text">
        Uslu A.A., Özel O.T., Örnekçi N., <span class="self-author">Çankırılıgil E.C.</span>, Çoşkun İ., Şenel G.U.,
        <span class="presentation-title">Black soldier fly (<em>Hermetia illucens</em>) prepupae meal as a possible alternative to fish meal in Rainbow trout (<em>Oncorhynchus mykiss</em>) diets</span>.
        <span class="presentation-event">TURFAJ 2021, 2nd International Congress of the Turkish Journal of Agriculture - Food Science and Technology</span>, October 2021, Gazimağusa.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/357737768_Black_soldier_fly_Hermetia_illucens_prepupae_meal_as_a_possible_alternative_to_fish_meal_in_Rainbow_trout_Oncorhynchus_mykiss_diets" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2021-09-07" data-group="conference">
      <div class="presentation-year">2021</div>
      <div class="presentation-text">
        Uslu A.A., Özel O.T., Çelik B., <span class="self-author">Çankırılıgil E.C.</span>, Çoşkun İ.,
        <span class="presentation-title">Fish Meal Replacement by Mealworm (<em>Tenebrio molitor</em>) Larvae Meal in Diets for Rainbow Trout (<em>Oncorhynchus mykiss</em>)</span>.
        <span class="presentation-event">FABA 2021 - International Symposium on Fisheries and Aquatic Sciences</span>, 7–8 September 2021, İzmir, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/356378976_Fish_Meal_Replacement_by_Mealworm_Tenebrio_molitor_Larvae_Meal_in_Diets_for_Rainbow_Trout_Oncorhynchus_mykiss" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2019-09-26" data-group="conference">
      <div class="presentation-year">2019</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Effects of Astaxanthine, Canthaxanthin and Lycopene Containing Diets on the Chemical Quality and Textural Properties of the Black Sea Trout (<em>Salmo labrax</em>) Fillets</span>.
        <span class="presentation-event">BioEco2019 International Biodiversity & Ecology Sciences Symposium</span>, 26–28 September 2019, Istanbul, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/336150403_Effects_of_Astaxanthine_Canthaxanthin_and_Lycopene_Containing_Diets_on_the_Chemical_Quality_and_Textural_Properties_of_the_Black_Sea_Trout_Salmo_labrax_Fillets" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2019-09-26" data-group="conference">
      <div class="presentation-year">2019</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Histological Examination of Black Sea Trout (<em>Salmo labrax</em>) Fed by Carotenoid Containing Diets</span>.
        <span class="presentation-event">BioEco2019 International Biodiversity & Ecology Sciences Symposium</span>, 26–28 September 2019, Istanbul, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/336150472_Histological_Examination_of_Black_Sea_Trout_Salmo_labrax_Fed_by_Carotenoid_Containing_Diets" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2019-04-20" data-group="conference">
      <div class="presentation-year">2019</div>
      <div class="presentation-text">
        Berik N., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Evaluation of Fatty Acid Compositions of Commercial Fish Oils Considering Recommended Omega Fatty Acid Uptake for a Healthy Diet</span>.
        <span class="presentation-event">4. Uluslararası Anadolu Tarım, Gıda, Çevre ve Biyoloji Kongresi</span>, 20–22 April 2019, Afyonkarahisar, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/332544748_Evaluation_of_Fatty_Acid_Compositions_of_Commercial_Fish_Oils_Considering_Recommended_Omega_Fatty_Acid_Uptake_for_a_Healthy_Diet" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2019-04-20" data-group="conference">
      <div class="presentation-year">2019</div>
      <div class="presentation-text">
        Berik N., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Seasonal Fatty Acid Composition of Green Seaweed (<em>Ulva rigida</em>)</span>.
        <span class="presentation-event">4. Uluslararası Anadolu Tarım, Gıda, Çevre ve Biyoloji Kongresi</span>, 20–22 April 2019, Afyonkarahisar, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/332544744_Seasonal_Fatty_Acid_Composition_of_Green_Seaweed_Ulva_Rigida" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2018-07-05" data-group="conference">
      <div class="presentation-year">2018</div>
      <div class="presentation-text">
        Ozel O., Türe M., Cakmak E., Cimagil R., <span class="self-author">Çankırılıgil E.C.</span>, Kutlu İ.,
        <span class="presentation-title">Effects of Dietary Daphne (<em>Laurus nobilis</em> L.) and Fennel (<em>Foeniculum vulgare</em> L.) Essential Oils on Some Intestinal Bacteria of Black Sea Trout (<em>Salmo labrax</em>)</span>.
        <span class="presentation-event">4th International Agriculture Congress</span>, 5–8 July 2018, Kırşehir, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/328957639_Effects_of_dietary_daphne_Laurus_nobilis_L_and_fennel_Foeniculum_vulgare_L_oils_on_some_intestinal_bacteria_of_Black_Sea_trout_Salmo_labrax" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,full-text,international symposium" data-date="2017-10-27" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">The Processing of Pufferfish and Usage of Tetrodotoxin in the Pharmaceutical Industry</span>.
        <span class="presentation-event">Jubilee International Scientific Conference “Bulgaria of the Regions”</span>, 27–28 October 2017, Plovdiv, Bulgaria.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/320620528_The_Processing_of_Pufferfish_and_Usage_of_Tetrodotoxin_in_the_Pharmaceutical_Industry" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
          <a class="presentation-link" href="https://regions.uard.bg/index.php/jubilee/jisc/paper/view/140" target="_blank" rel="noopener" aria-label="Abstract or event link">🔗</a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">Full-text</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2017-10-04" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Element Composition of Farmed Rainbow Trout (<em>Oncorhynchus mykiss</em>) Obtained from Fish Farm in the Mount Ida</span>.
        <span class="presentation-event">ISEEP-2017 VIII. International Symposium on Ecology and Environmental Problems</span>, 4–7 October 2017, Çanakkale, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/320191714_Element_Composition_of_Farmed_Rainbow_Trout_Oncorhynchus_mykiss_Obtained_from_Fish_farm_in_the_Mount_Ida" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2017-10-04" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        Berik N., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">The Seasonal Elemental Composition of Green Seaweed (<em>Ulva rigida</em>) Collected from Canakkale, Turkey</span>.
        <span class="presentation-event">ISEEP-2017 VIII. International Symposium on Ecology and Environmental Problems</span>, 4–7 October 2017, Çanakkale, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/320191598_The_Seasonal_Elemental_Composition_of_Green_Seaweed_Ulva_rigida_Collected_from_Canakkale_Turkey" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2017-09-12" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Farklı Su Ürünlerinden Elde Edilen Kaplama Ürünlerin Duyusal Özelliklerinin Belirlenmesi</span>.
        <span class="presentation-event">19. Ulusal Su Ürünleri Sempozyumu</span>, 12–15 September 2017, Sinop, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/320011682_Farkli_Su_Urunlerinden_Elde_Edilen_Kaplama_Urunlerin_Duyusal_Ozelliklerinin_Belirlenmesi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2017-09-12" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Güven A., Balçık Mısır G.,
        <span class="presentation-title">Kültüre Alınan Altınbaş Kefalin (<em>Liza aurata</em>) Kas Dokusu ve Atıklarının Amino Asit Kompozisyonunun Belirlenmesi</span>.
        <span class="presentation-event">19. Ulusal Su Ürünleri Sempozyumu</span>, 12–15 September 2017, Sinop, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/319998160_Kulture_Alinan_Altinbas_Kefalin_Liza_aurata_Kas_Dokusu_ve_Atiklarinin_Amino_Asit_Kompozisyonunun_Belirlenmesi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2017-09-12" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        Kasapoğlu N., Güven A., Çakmak E., <span class="self-author">Çankırılıgil E.C.</span>, Firidin Ş.,
        <span class="presentation-title">Karadeniz Kefal Avcılığında Hedef Dışı Av Oranları</span>.
        <span class="presentation-event">19. Ulusal Su Ürünleri Sempozyumu</span>, 12–15 September 2017, Sinop, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/320557038_Karadeniz_Kefal_Avciliginda_Hedef_Disi_Av_Oranlari" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2017-07-05" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Çakmak E., Özel O.T., Kasapoğlu N.,
        <span class="presentation-title">Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811) Culture in Turkey and Morphometric Characteristics of Fifth Culture Generation</span>.
        <span class="presentation-event">SEAB 2017, International Symposium on EuroAsian Biodiversity</span>, 5–8 July 2017, Minsk, Belarus.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/318318294_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811_Culture_in_Turkey_and_Morphometric_Characteristics_of_Fifth_Culture_Generation" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2017-07-05" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Amino Acid Composition of Cultured Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811)</span>.
        <span class="presentation-event">SEAB 2017, International Symposium on EuroAsian Biodiversity</span>, 5–8 July 2017, Minsk, Belarus.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/318318094_Amino_Acid_Composition_of_Cultured_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2017-07-05" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Scallop Species in Turkey and Evaluation in terms of Food Safety Considering 9th Task Group of Marine Strategy Framework Directive</span>.
        <span class="presentation-event">SEAB 2017, International Symposium on EuroAsian Biodiversity</span>, 5–8 July 2017, Minsk, Belarus.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/318318091_Scallop_Species_in_Turkey_and_Evaluation_in_terms_of_Food_Safety_Considering_9th_Task_Group_of_Marine_Strategy_Framework_Directive" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2017-07-05" data-group="conference">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        Kasapoğlu N., Düzgüneş E., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Biodiversity in the Black Sea Bottom Trawl Fisheries and Processing Possibilities of Discard Species</span>.
        <span class="presentation-event">SEAB 2017, International Symposium on EuroAsian Biodiversity</span>, 5–8 July 2017, Minsk, Belarus.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/318339614_Biodiversity_in_the_Black_Sea_Bottom_Trawl_Fisheries_and_Processing_Possibilities_of_Discard_Species" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2016-11-03" data-group="conference">
      <div class="presentation-year">2016</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N., Çakmak E.,
        <span class="presentation-title">Meat Color Changes in Different Generations of Cultured Black Sea Trout (<em>Salmo trutta labrax</em>): A Preliminary Study</span>.
        <span class="presentation-event">FABA 2016, International Symposium on Fisheries and Aquatic Sciences</span>, 3–5 November 2016, Antalya, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/310704030_Meat_color_changes_in_different_generations_of_cultured_Black_Sea_trout_Salmo_trutta_labrax_a_preliminary_study" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2016-11-03" data-group="conference">
      <div class="presentation-year">2016</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Alp Erbay E.,
        <span class="presentation-title">Effect of Different Thawing Techniques on Color of Black Sea Trout (<em>Salmo trutta labrax</em>) Fillets</span>.
        <span class="presentation-event">FABA 2016, International Symposium on Fisheries and Aquatic Sciences</span>, 3–5 November 2016, Antalya, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/310704780_Effect_of_Different_Thawing_Techniques_on_Color_of_Black_Sea_Trout_Salmo_trutta_labrax_Fillets" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2016-11-03" data-group="conference">
      <div class="presentation-year">2016</div>
      <div class="presentation-text">
        Kasapoğlu N., <span class="self-author">Çankırılıgil E.C.</span>, Çakmak E.,
        <span class="presentation-title">A Preliminary Study on Growth Characteristics of Striped Sea Bream, <em>Lithognathus mormyrus</em>, in the Black Sea</span>.
        <span class="presentation-event">FABA 2016, International Symposium on Fisheries and Aquatic Sciences</span>, 3–5 November 2016, Antalya, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/310721246_A_PRELIMINARY_STUDY_ON_GROWTH_CHARACTERISTICS_OF_STRIPED_SEA_BREAM_Lithognathus_mormyrus_IN_THE_BLACK_SEA" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,international symposium" data-date="2016-10-21" data-group="conference">
      <div class="presentation-year">2016</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Changes in Fatty Acid and Mineral Compositions of Rose-Shrimp Croquettes during Production Process</span>.
        <span class="presentation-event">63rd Scientific Conference with International Participation “Food Science, Engineering and Technology 2016”</span>, 21–22 October 2016, Plovdiv, Bulgaria.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/310705586_Changes_in_Fatty_Acid_and_Mineral_Compositions_of_Rose-Shrimp_Croquettes_During_Production_Process" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,poster presentation,full-text,international symposium" data-date="2016-09-12" data-group="conference">
      <div class="presentation-year">2016</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Çakmak E., Özcan Akpınar İ.,
        <span class="presentation-title">Histological Development of the Digestive Tract of Black Sea Trout (<em>Salmo trutta labrax</em> PALLAS, 1811) During Larval Ontogeny</span>.
        <span class="presentation-event">41th CIESM Congress, Living Resources & Marine Ecosystems Committee</span>, 12–16 September 2016, Kiel, Germany.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/310705507_Histological_Development_of_the_Digestive_Tract_of_Black_Sea_Trout_Salmo_trutta_labrax_PALLAS_1811_During_Larval_Ontogeny" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
          <a class="presentation-link" href="https://ciesm.org/online/archives/abstracts/pdf/41/CIESM_Congress_2016_Kiel_article_0519.pdf" target="_blank" rel="noopener" aria-label="Abstract or event link">🔗</a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">Full-text</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,poster presentation,full-text,international symposium" data-date="2016-09-12" data-group="conference">
      <div class="presentation-year">2016</div>
      <div class="presentation-text">
        Kasapoğlu N., Çakmak E., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Diffrerences Between Cultured and Wild Black Sea Trout (<em>Salmo trutta labrax</em>) Otoliths: a Comparative Study</span>.
        <span class="presentation-event">41th CIESM Congress, Living Resources & Marine Ecosystems Committee</span>, 12–16 September 2016, Kiel, Germany.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/310719575_Differences_Between_Cultured_and_Wild_Black_Sea_Trout_Salmo_trutta_labrax_Otoliths_A_Comparative_Study" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
          <a class="presentation-link" href="https://ciesm.org/online/archives/abstracts/pdf/41/CIESM_Congress_2016_Kiel_article_0519.pdf" target="_blank" rel="noopener" aria-label="Abstract or event link">🔗</a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">Full-text</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2015-09-18" data-group="conference">
      <div class="presentation-year">2015</div>
      <div class="presentation-text">
        Berik N., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Mineral Contents of Meat and Digestive Glands of Scallops (<em>Flexopecten glaber</em>) Caught in Çanakkale Strait, Turkey</span>.
        <span class="presentation-event">MACODESU 2015, Conference of Sea and Coastal Development in the frame of Sustainability</span>, 18–20 September 2015, Trabzon, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/280134261_Mineral_Contents_of_Meat_and_Digestive_Glands_of_Scallops_Flexopecten_glaber_Catched_in_Canakkale_Strait_Turkey" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2013-09-03" data-group="conference">
      <div class="presentation-year">2013</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Gökkuşağı Alabalığı (<em>Oncorhynchus mykiss</em>) Kroketlerinin Soğuk Muhafazada (+4ºC) Raf Ömrünün Belirlenmesi</span>.
        <span class="presentation-event">17. Ulusal Su Ürünleri Sempozyumu</span>, 3–6 September 2013, İstanbul, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/261831368_Gokkusagi_Alabaligi_Oncorhynchus_mykiss_Kroketlerinin_Soguk_Muhafazada_4C_Raf_Omrunun_Belirlenmesi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2012-11-09" data-group="conference">
      <div class="presentation-year">2012</div>
      <div class="presentation-text">
        Berik N., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Determination of Proximate Composition and Sensory Attributes of Scallop (<em>Flexopecten glaber</em>) Gonads</span>.
        <span class="presentation-event">Turkish-Japanese Marine Forum, Harmonization of Bio-diversity and Marine Industries Symposium</span>, 9–12 November 2012, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/314209537_Determination_of_Proximate_Composition_and_Sensory_Attributes_of_Scallop_Flexopecten_glaber_Gonads" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,international symposium" data-date="2012-11-09" data-group="conference">
      <div class="presentation-year">2012</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Berik N.,
        <span class="presentation-title">Production of Croquettes from Deep-Water Rose Shrimp (<em>Parapenaeus longirostris</em>) Meat</span>.
        <span class="presentation-event">Turkish-Japanese Marine Forum, Harmonization of Bio-diversity and Marine Industries Symposium</span>, 9–12 November 2012, Çanakkale, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/261830662_Production_of_Croquettes_from_Deep-Water_Rose_Shrimp_Parapenaeus_longirostris_Meat" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">International symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2011-10-25" data-group="conference">
      <div class="presentation-year">2011</div>
      <div class="presentation-text">
        Berik N., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Çanakkale Balık Halinden Temin Edilen Deniz Tarağına (<em>Flexopecten glaber</em>) Farklı Pişirme Tekniklerinin Uygulanması</span>.
        <span class="presentation-event">16. Ulusal Su Ürünleri Sempozyumu</span>, 25–27 October 2011, Antalya, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/261831190_Canakkale_Balik_Halinden_Temin_Edilen_Deniz_Taragina_Flexopecten_glaber_Farkli_Pisirme_Tekniklerinin_Uygulanmasi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2010-07-06" data-group="conference">
      <div class="presentation-year">2010</div>
      <div class="presentation-text">
        Berik N., Kahraman D., <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Alabalık (<em>Oncorhynchus mykiss</em>) Marinatlarının Duyusal ve Besin Değeri Bakımından Değerlendirilmesi</span>.
        <span class="presentation-event">2. Ulusal Alabalık Sempozyumu</span>, 6–8 July 2010, Karaman, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/261831194_Alabalik_Oncorhynchus_mykiss_Marinatlarinin_Duyusal_ve_Besin_Degeri_Bakimindan_Degerlendirilmesi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="poster presentation,national symposium" data-date="2010-07-06" data-group="conference">
      <div class="presentation-year">2010</div>
      <div class="presentation-text">
        Berik N., <span class="self-author">Çankırılıgil E.C.</span>, Kahraman D.,
        <span class="presentation-title">Alabalık (<em>Oncorhynchus mykiss</em>) Eti Kullanılarak Hazırlanan Kroketlerin Besin Bileşimi ve Duyusal Analizleri Açısından İncelenmesi</span>.
        <span class="presentation-event">2nd National Trout Symposium</span>, 6–8 July 2010, Karaman, Türkiye.
        <span class="presentation-links">
          <a class="presentation-link rg" href="https://www.researchgate.net/publication/261831381_Alabalik_Oncorhynchus_mykiss_Eti_Kullanilarak_Hazirlanan_Kroketlerin_Besin_Bilesimi_ve_Duyusal_Analizleri_Acisindan_Incelenmesi" target="_blank" rel="noopener" aria-label="ResearchGate link">
            <img src="{{ '/assets/img/researchgate.svg' | relative_url }}" alt="ResearchGate">
          </a>
        </span>
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Poster presentation</span>
        <span class="presentation-chip">National symposium</span>
      </div>
    </div>

  </div>

  <h2 class="section-title presentation-section-title">Other Presentations</h2>

  <div class="presentation-list" id="otherPresentationList">

    <div class="presentation-entry" data-tags="invited speaker,seminar" data-date="2024-11-09" data-group="other">
      <div class="presentation-year">2024</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Marine Life in Antarctica</span>.
        <span class="presentation-event">Maltepe Kadir Has Science and Art Center, Student Seminar</span>, 9 November 2024, İstanbul, Türkiye.
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Invited speaker</span>
        <span class="presentation-chip">Seminar</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="invited speaker,workshop" data-date="2023-12-05" data-group="other">
      <div class="presentation-year">2023</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Algae in Extreme Climate Conditions: The Case of Horseshoe Island</span>.
        <span class="presentation-event">Horseshoe Island and Glacial Lakes Biodiversity Workshop</span>, 5–6 December 2023, Erzurum, Türkiye.
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Invited speaker</span>
        <span class="presentation-chip">Workshop</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,meeting" data-date="2023-07-01" data-group="other">
      <div class="presentation-year">2023</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">7th National Turkish Antarctic Expedition</span>.
        <span class="presentation-event">T.C. Ministry of Agriculture and Forest, I. Regional Group Meeting</span>, July 2023, Yalova, Türkiye.
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">Meeting</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="invited speaker,seminar" data-date="2023-06-01" data-group="other">
      <div class="presentation-year">2023</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Studies that carried out in 7th National Turkish Antarctic Expedition</span>.
        <span class="presentation-event">Career Talks in ÇOMÜ Marine Science and Technology Faculty</span>, June 2023, Çanakkale, Türkiye.
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Invited speaker</span>
        <span class="presentation-chip">Seminar</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,workshop" data-date="2022-12-01" data-group="other">
      <div class="presentation-year">2022</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Ak İ., Türker G., Kara A., Veske E., Apaydın Yağcı M., Kocabaş E., Berik N.,
        <span class="presentation-title">Biological Activity Evaluation of Macroalgae Distributed on Horseshoe Island (Antarctica) Coasts by Determining Nutrient Composition and Phytochemical Contents – Project Display</span>.
        <span class="presentation-event">6. National Polar Science Workshop</span>, 1 December 2022, Trabzon, Türkiye.
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">Workshop</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,workshop" data-date="2022-06-22" data-group="other">
      <div class="presentation-year">2022</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>,
        <span class="presentation-title">Studies on Macroalgae Culture</span>.
        <span class="presentation-event">Workshop of Blue Economy and Aquatic Plants</span>, 22–23 June 2022, Antalya, Türkiye.
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">Workshop</span>
      </div>
    </div>

    <div class="presentation-entry" data-tags="oral presentation,workshop" data-date="2017-10-24" data-group="other">
      <div class="presentation-year">2017</div>
      <div class="presentation-text">
        <span class="self-author">Çankırılıgil E.C.</span>, Çakmak E., Özel O.T., Kasapoğlu N., Alp Erbay E., Özcan Akpınar İ.,
        <span class="presentation-title">An Overview on Biology, Biochemistry and Aquaculture of the 5th Culture Generation of Black Sea Trout (<em>Salmo trutta labrax</em>) Considering Recent Studies</span>.
        <span class="presentation-event">Workshop on Aquaculture in the Black Sea: Potential and Opportunities</span>, 24–26 October 2017, Trabzon, Türkiye.
      </div>
      <div class="presentation-chips">
        <span class="presentation-chip">Oral presentation</span>
        <span class="presentation-chip">Workshop</span>
      </div>
    </div>

  </div>

  <p class="presentation-empty" id="presentationEmpty">No presentations match the selected filters.</p>
</div>

<script>
  (function () {
    const toggleBtn = document.getElementById('filterToggle');
    const panel = document.getElementById('filterPanel');
    const closeBtn = document.getElementById('closeFilters');
    const clearBtn = document.getElementById('clearFilters');
    const checkboxes = Array.from(panel.querySelectorAll('input[type="checkbox"]'));
    const entries = Array.from(document.querySelectorAll('.presentation-entry'));
    const emptyState = document.getElementById('presentationEmpty');

    function normalizeTag(tag) {
      return tag.trim().toLowerCase();
    }

    function applyFilters() {
      const selected = checkboxes
        .filter(cb => cb.checked)
        .map(cb => normalizeTag(cb.value));

      let visibleCount = 0;

      entries.forEach(entry => {
        const tags = (entry.dataset.tags || '')
          .split(',')
          .map(normalizeTag)
          .filter(Boolean);

        const match = selected.every(tag => tags.includes(tag));
        entry.style.display = match ? '' : 'none';

        if (match) visibleCount += 1;
      });

      emptyState.style.display = visibleCount === 0 ? 'block' : 'none';
    }

    toggleBtn.addEventListener('click', function () {
      panel.classList.toggle('open');
    });

    closeBtn.addEventListener('click', function () {
      panel.classList.remove('open');
    });

    clearBtn.addEventListener('click', function () {
      checkboxes.forEach(cb => cb.checked = false);
      applyFilters();
    });

    checkboxes.forEach(cb => {
      cb.addEventListener('change', applyFilters);
    });

    document.addEventListener('click', function (event) {
      if (!panel.contains(event.target) && !toggleBtn.contains(event.target)) {
        panel.classList.remove('open');
      }
    });
  })();
</script>
