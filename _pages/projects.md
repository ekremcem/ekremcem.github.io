---
layout: page
title: Projects
permalink: /projects/
nav: true
nav_order: 3
---

<style>
.project-card {
  display: grid;
  grid-template-columns: 300px 1fr;
  gap: 20px;
  margin-bottom: 30px;
  padding: 15px;
  border: 1px solid #ddd;
  border-radius: 16px;
}

.project-img {
  border: 1px solid #ccc;
  border-radius: 12px;
  overflow: hidden;
}

.project-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.project-year {
  color: #2a7ae2;
  font-weight: 700;
}

.project-title {
  font-weight: 700;
  margin: 5px 0;
}

.project-funder {
  font-style: italic;
}

.tags span {
  background: #eee;
  padding: 4px 8px;
  border-radius: 20px;
  margin-right: 5px;
  font-size: 12px;
}

.actions button {
  margin: 5px 5px 5px 0;
  padding: 5px 10px;
  border-radius: 20px;
  border: 1px solid #ccc;
  background: white;
  cursor: pointer;
}

.panel {
  display: none;
  margin-top: 10px;
  padding: 10px;
  border: 1px solid #eee;
  border-radius: 10px;
  background: #fafafa;
}
</style>

## As a Project Leader

<div class="project-card">
<div class="project-img">
<img src="/assets/img/proje3.jpg">
</div>
<div>

<div class="project-year">2027–2030 (Proposal stage)</div>

<div class="project-title">
Assessment of the Bioecological Characteristics of Oyster Species...
</div>

<div class="project-funder">
Supported by Republic of Türkiye, Ministry of Agriculture and Forestry (TAGEM)
</div>

<p>
<strong>Project Leader:</strong> Dr. Ekrem Cem Çankırılıgil<br>
<strong>Executive Organization:</strong> Sheep Breeding Research Institute
</p>

<div class="tags">
<span>TAGEM</span><span>AR-GE</span><span>Aquaculture</span>
</div>

<div class="actions">
<button onclick="toggle('a1')">Abstract</button>
<button onclick="toggle('b1')">Budget</button>
<button onclick="toggle('c1')">Team</button>
<button onclick="toggle('d1')">Collaborators</button>
</div>

<div id="a1" class="panel">
(ABSTRACT BURADA)
</div>

<div id="b1" class="panel">1.750.000 TL</div>

</div>
</div>

---

## As a Researcher

<div class="list-item">
<strong>2026–2028</strong><br>
Determining the Marine Connectivity Between Dominant Predator...
</div>

<script>
function toggle(id){
  var el = document.getElementById(id);
  el.style.display = el.style.display === "block" ? "none" : "block";
}
</script>
