---
layout: page
title: Native Bees
permalink: /nativebees/
description:
nav: true
nav_order: 3
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=Lora:ital,wght@0,400;0,600;1,400&family=DM+Sans:wght@300;400;500&display=swap" rel="stylesheet">

<style>
*, *::before, *::after { box-sizing: border-box; }

:root {
  --nb-cream: #FAF6ED;
  --nb-parchment: #F0E8D0;
  --nb-forest: #1B3527;
  --nb-forest-mid: #275238;
  --nb-forest-light: #3A6B4F;
  --nb-honey: #B37410;
  --nb-honey-light: #D49120;
  --nb-brown: #3A2518;
  --nb-muted: #7A6E62;
  --nb-rule: #C8B89A;
}

.nb-page {
  font-family: 'Lora', Georgia, serif;
  color: var(--nb-brown);
  line-height: 1.75;
  -webkit-font-smoothing: antialiased;
}
.nb-page * { box-sizing: border-box; }

/* ── HERO ── */
.nb-hero {
  background: var(--nb-forest);
  padding: 4rem 3.5rem 3.5rem;
  display: grid;
  grid-template-columns: 1fr 290px;
  gap: 2rem;
  align-items: center;
  overflow: hidden;
  position: relative;
  margin: 0 -15px;
}
.nb-hero-bg {
  position: absolute;
  inset: 0;
  opacity: 0.04;
  background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='56' height='100'%3E%3Cpath d='M28 66L0 50V16L28 0l28 16v34L28 66zM28 100L0 84V50l28-16 28 16v34L28 100z' fill='none' stroke='%23FAF6ED' stroke-width='1'/%3E%3C/svg%3E");
  pointer-events: none;
}
.nb-hero-text { position: relative; z-index: 1; }
.nb-eyebrow {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.72rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--nb-honey-light);
  margin-bottom: 1rem;
  display: flex;
  align-items: center;
  gap: 0.75rem;
}
.nb-eyebrow::before {
  content: '';
  display: inline-block;
  width: 22px;
  height: 1px;
  background: var(--nb-honey-light);
}
.nb-hero h1 {
  font-family: 'DM Serif Display', Georgia, serif !important;
  font-size: clamp(2.4rem, 5vw, 4.2rem) !important;
  font-weight: 400 !important;
  line-height: 1.05 !important;
  color: #F0E8D0 !important;
  margin-bottom: 1.25rem !important;
  border: none !important;
  padding: 0 !important;
}
.nb-hero h1 em { font-style: italic; color: var(--nb-honey-light); }
.nb-hero-sub {
  font-size: 1rem;
  line-height: 1.7;
  color: rgba(183,210,175,0.85);
  max-width: 42ch;
  font-style: italic;
}
.nb-hero-stats {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  margin-top: 1.5rem;
}
.nb-hero-pill {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.72rem;
  letter-spacing: 0.04em;
  background: rgba(212,145,32,0.18);
  border: 1px solid rgba(212,145,32,0.4);
  color: var(--nb-honey-light);
  padding: 0.3rem 0.8rem;
  border-radius: 20px;
}
.nb-hero-bee { position: relative; z-index: 1; display: flex; align-items: center; justify-content: center; }

@keyframes nb-float {
  0%, 100% { transform: translateY(0) rotate(-4deg); }
  50% { transform: translateY(-16px) rotate(4deg); }
}
@keyframes nb-wingbeat {
  0%, 100% { transform: scaleY(1) skewX(-2deg); opacity: 0.75; }
  50% { transform: scaleY(0.6) skewX(2deg); opacity: 0.9; }
}
.nb-bee-group { animation: nb-float 7s ease-in-out infinite; transform-origin: center; }
.nb-wing-top { animation: nb-wingbeat 0.18s ease-in-out infinite; transform-origin: 50% 100%; }
.nb-wing-bot { animation: nb-wingbeat 0.18s ease-in-out infinite 0.09s; transform-origin: 50% 0%; }

/* ── SECTIONS ── */
.nb-section { padding: 4.5rem 0; }
.nb-section-header { margin-bottom: 2.75rem; }
.nb-section-eyebrow {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.7rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: var(--nb-honey);
  margin-bottom: 0.5rem;
}
.nb-section-title {
  font-family: 'DM Serif Display', Georgia, serif !important;
  font-size: 2rem !important;
  font-weight: 400 !important;
  color: var(--nb-forest) !important;
  line-height: 1.15 !important;
  border: none !important;
  padding: 0 !important;
}
.nb-section-title em { font-style: italic; color: var(--nb-honey); }
.nb-section-lead {
  font-size: 1rem;
  color: var(--nb-muted);
  font-style: italic;
  max-width: 55ch;
  margin-top: 0.5rem;
}

/* ── BEE GALLERY (species + facts merged) ── */
.nb-bee-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
}
.nb-bee-card {
  background: var(--nb-cream);
  border: 1px solid var(--nb-rule);
  overflow: hidden;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.nb-bee-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 12px 32px rgba(27,53,39,0.12);
}
.nb-bee-card-img {
  width: 100%;
  aspect-ratio: 4/3;
  object-fit: cover;
  display: block;
  filter: saturate(0.9) contrast(1.05);
  transition: transform 0.5s ease, filter 0.4s ease;
}
.nb-bee-card:hover .nb-bee-card-img {
  transform: scale(1.04);
  filter: saturate(1.05) contrast(1.03);
}
.nb-bee-card-img-wrap { overflow: hidden; }

.nb-bee-placeholder {
  width: 100%;
  aspect-ratio: 4/3;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;
}
.nb-bee-placeholder svg { opacity: 0.4; }
.nb-bee-placeholder span {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.7rem;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  opacity: 0.5;
}

.nb-bee-card-body { padding: 1.1rem 1.25rem 1.4rem; }
.nb-bee-tag-row { display: flex; flex-wrap: wrap; gap: 0.35rem; margin-bottom: 0.7rem; }
.nb-bee-tag {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.65rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  padding: 0.2rem 0.6rem;
  border-radius: 20px;
  font-weight: 500;
}
/* tag colours */
.nb-tag-amber { background: #FAEEDA; color: #854F0B; border: 0.5px solid #FAC775; }
.nb-tag-green  { background: #EAF3DE; color: #27500A; border: 0.5px solid #C0DD97; }
.nb-tag-teal   { background: #E1F5EE; color: #085041; border: 0.5px solid #9FE1CB; }
.nb-tag-pink   { background: #FBEAF0; color: #72243E; border: 0.5px solid #F4C0D1; }
.nb-tag-blue   { background: #E6F1FB; color: #0C447C; border: 0.5px solid #B5D4F4; }
.nb-tag-purple { background: #EEEDFE; color: #3C3489; border: 0.5px solid #CECBF6; }

.nb-bee-card-name {
  font-family: 'DM Serif Display', Georgia, serif;
  font-size: 1.05rem;
  color: var(--nb-forest);
  display: block;
  margin-bottom: 0.2rem;
  line-height: 1.2;
}
.nb-bee-card-sciname {
  font-family: 'Lora', Georgia, serif;
  font-style: italic;
  font-size: 0.78rem;
  color: var(--nb-muted);
  display: block;
  margin-bottom: 0.65rem;
}
.nb-bee-card-fact {
  font-size: 0.85rem;
  color: var(--nb-brown);
  line-height: 1.65;
  margin: 0;
}
.nb-bee-card-credit {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.68rem;
  color: var(--nb-muted);
  margin-top: 0.75rem;
  padding-top: 0.6rem;
  border-top: 1px solid var(--nb-rule);
  display: block;
}

/* ── WHY ── */
.nb-why {
  background: var(--nb-parchment);
  padding: 5rem 3.5rem;
  display: grid;
  grid-template-columns: 5fr 7fr;
  gap: 4.5rem;
  align-items: start;
  margin: 0 -15px;
}
.nb-pull-quote {
  font-family: 'DM Serif Display', Georgia, serif;
  font-size: 1.5rem;
  line-height: 1.4;
  color: var(--nb-forest);
  font-style: italic;
  padding-left: 1.5rem;
  border-left: 3px solid var(--nb-honey);
  position: sticky;
  top: 80px;
}
.nb-pull-quote span {
  display: block;
  margin-top: 1.2rem;
  font-family: 'DM Sans', sans-serif;
  font-size: 0.67rem;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--nb-honey);
  font-style: normal;
}
.nb-why-body p { margin-bottom: 1.1rem; color: var(--nb-brown); font-size: 1.02rem; }
.nb-why-body p:last-child { margin-bottom: 0; }

/* ── WORKSHOPS ── */
.nb-workshops-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1.75rem;
  margin-top: 2.75rem;
}
.nb-workshop-card { background: var(--nb-forest); overflow: hidden; }
.nb-workshop-card img {
  width: 100%;
  height: 210px;
  object-fit: cover;
  display: block;
  filter: saturate(0.6) brightness(0.75);
  transition: filter 0.4s ease;
}
.nb-workshop-card:hover img { filter: saturate(0.8) brightness(0.85); }
.nb-workshop-content { padding: 1.75rem 2.25rem 2.25rem; }
.nb-workshop-tag {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.68rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: var(--nb-honey-light);
  margin-bottom: 0.6rem;
  display: block;
}
.nb-workshop-card h3 {
  font-family: 'DM Serif Display', Georgia, serif !important;
  font-size: 1.5rem !important;
  font-weight: 400 !important;
  color: #F0E8D0 !important;
  margin-bottom: 0.75rem !important;
  line-height: 1.2 !important;
  border: none !important;
  padding: 0 !important;
}
.nb-workshop-card p { font-size: 0.9rem; color: rgba(183,210,175,0.85); line-height: 1.7; margin: 0; }

/* ── INSTRUCTIONS ── */
.nb-instructions {
  background: white;
  padding: 4.5rem 3.5rem;
  margin: 0 -15px;
}
.nb-instructions-sub {
  max-width: 55ch;
  color: var(--nb-muted);
  font-style: italic;
  margin-top: 0.5rem;
  font-size: 0.95rem;
}
.nb-instructions-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 3.5rem 5rem;
  margin-top: 3.25rem;
}
.nb-inst-header {
  margin-bottom: 2rem;
  padding-bottom: 1.1rem;
  border-bottom: 1px solid var(--nb-rule);
}
.nb-inst-label {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.67rem;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--nb-honey);
  margin-bottom: 0.2rem;
}
.nb-inst-header h3 {
  font-family: 'DM Serif Display', Georgia, serif !important;
  font-size: 1.4rem !important;
  color: var(--nb-forest) !important;
  font-style: italic !important;
  font-weight: 400 !important;
  line-height: 1.25 !important;
  border: none !important;
  padding: 0 !important;
  margin: 0 !important;
}
.nb-step { display: flex; gap: 1.1rem; margin-bottom: 1.5rem; align-items: flex-start; }
.nb-step-num {
  font-family: 'DM Serif Display', Georgia, serif;
  font-size: 1.85rem;
  color: var(--nb-rule);
  line-height: 1;
  min-width: 1.8rem;
  font-style: italic;
  margin-top: -0.1rem;
}
.nb-step-body strong {
  display: block;
  font-family: 'DM Sans', sans-serif;
  font-size: 0.8rem;
  font-weight: 500;
  color: var(--nb-forest);
  margin-bottom: 0.25rem;
  text-transform: uppercase;
  letter-spacing: 0.07em;
}
.nb-step-body p { font-size: 0.88rem; color: var(--nb-muted); line-height: 1.65; margin: 0; }

/* ── SEED SPECIES ── */
.nb-seed-species {
  background: var(--nb-forest-mid);
  padding: 1.75rem 2.25rem;
  grid-column: 1 / -1;
}
.nb-seed-species h4 {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.66rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: var(--nb-honey-light);
  margin-bottom: 1.1rem;
  font-weight: 400;
}
.nb-seed-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; }
.nb-seed-tag {
  font-family: 'Lora', Georgia, serif;
  font-size: 0.82rem;
  font-style: italic;
  padding: 0.3rem 0.85rem;
  border-radius: 20px;
  border: 1px solid rgba(212,145,32,0.3);
}
/* alternate tag colours for the flower list */
.nb-seed-tag:nth-child(3n+1) { background: rgba(212,145,32,0.15); color: #D49120; }
.nb-seed-tag:nth-child(3n+2) { background: rgba(58,107,79,0.25); color: #9FE1CB; }
.nb-seed-tag:nth-child(3n)   { background: rgba(240,232,208,0.12); color: #F0E8D0; border-color: rgba(240,232,208,0.2); }

/* ── LINKS ── */
.nb-links {
  background: var(--nb-forest);
  padding: 4.5rem 3.5rem;
  display: grid;
  grid-template-columns: 2fr 3fr;
  gap: 4rem;
  align-items: center;
  margin: 0 -15px;
}
.nb-links-heading {
  font-family: 'DM Serif Display', Georgia, serif;
  font-size: 1.85rem;
  color: #F0E8D0;
  font-style: italic;
  line-height: 1.25;
  margin: 0;
}
.nb-links-heading em { color: var(--nb-honey-light); font-style: normal; }
.nb-links-list { list-style: none; padding: 0; margin: 0; }
.nb-links-list li { border-top: 1px solid rgba(240,232,208,0.12); }
.nb-links-list li:last-child { border-bottom: 1px solid rgba(240,232,208,0.12); }
.nb-links-list a {
  color: rgba(183,210,175,0.85);
  text-decoration: none;
  font-size: 0.95rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
  gap: 1rem;
  transition: color 0.2s;
  font-family: 'Lora', Georgia, serif;
}
.nb-links-list a:hover { color: #F0E8D0; }
.nb-link-arrow { font-family: 'DM Sans', sans-serif; color: var(--nb-honey-light); flex-shrink: 0; transition: transform 0.2s; }
.nb-links-list a:hover .nb-link-arrow { transform: translateX(4px); }

/* ── REVEAL ── */
.nb-reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.75s ease, transform 0.75s ease; }
.nb-reveal.nb-in { opacity: 1; transform: none; }

/* ── RESPONSIVE ── */
@media (max-width: 900px) {
  .nb-hero { grid-template-columns: 1fr; padding: 3rem 1.5rem 2.5rem; margin: 0 -10px; }
  .nb-hero-bee { display: none; }
  .nb-section { padding: 3rem 0; }
  .nb-bee-grid { grid-template-columns: 1fr 1fr; }
  .nb-why { grid-template-columns: 1fr; padding: 3rem 1.5rem; gap: 2.25rem; margin: 0 -10px; }
  .nb-pull-quote { position: static; }
  .nb-workshops-grid { grid-template-columns: 1fr; }
  .nb-instructions { padding: 3rem 1.5rem; margin: 0 -10px; }
  .nb-instructions-grid { grid-template-columns: 1fr; gap: 2.5rem; }
  .nb-seed-species { grid-column: 1; }
  .nb-links { grid-template-columns: 1fr; padding: 3rem 1.5rem; margin: 0 -10px; gap: 2rem; }
}
@media (max-width: 600px) {
  .nb-bee-grid { grid-template-columns: 1fr; }
}
</style>

<div class="nb-page">

<!-- HERO -->
<section class="nb-hero">
  <div class="nb-hero-bg"></div>
  <div class="nb-hero-text">

    <h1>There are over 2,000 native bee species<br><em>in Australia.</em></h1>
    <p class="nb-hero-sub">Most live alone, don't make honey, and look nothing like a honeybee.</p>

  </div>

</section>

<!-- BEE GALLERY: species + facts merged -->
<section class="nb-section nb-reveal">
  <div class="nb-section-header">
    <h2 class="nb-section-title">Let's meet <em>some of them</em></h2>
  </div>

  <div class="nb-bee-grid">

    <!-- 1 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/amegillabombiformis.jpg' | relative_url }}" alt="Teddy bear bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Teddy bear bee</span>
        <span class="nb-bee-card-sciname">Amegilla bombiformis</span>
        <p class="nb-bee-card-fact">This one looks like a flying furball. The thick orange fur isn't just cute — it helps trap and carry pollen between flowers.</p>
        <span class="nb-bee-card-credit">Photo: austenarmstrong on iNaturalist</span>
      </div>
    </div>

    <!-- 2 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/thyreusnitidulus.jpg' | relative_url }}" alt="Neon cuckoo bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Neon cuckoo bee</span>
        <span class="nb-bee-card-sciname">Thyreus nitidulus</span>
        <p class="nb-bee-card-fact">This bee sneaks into other bees' nests and lays its own eggs there. The host bee raises the cuckoo's babies without knowing!</p>
        <span class="nb-bee-card-credit">Photo: lroganentsocvic on iNaturalist</span>
      </div>
    </div>

    <!-- 3 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/megachilemaculariformis.jpg' | relative_url }}" alt="Leafcutter bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Leafcutter bee</span>
        <span class="nb-bee-card-sciname">Megachile maculariformis</span>
        <p class="nb-bee-card-fact">This bee snips perfect circles from leaves with its jaws and rolls them into tiny leaf burritos to wrap its eggs in. If you see neat round holes in your garden leaves, a leafcutter has been busy.</p>
        <span class="nb-bee-card-credit">Photo: debtaylor142 on iNaturalist</span>
      </div>
    </div>

    <!-- 4 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/xylocopaaerata.jpg' | relative_url }}" alt="Green carpenter bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Green carpenter bee</span>
        <span class="nb-bee-card-sciname">Xylocopa aerata</span>
        <p class="nb-bee-card-fact">One of Australia's most spectacular bees — its body shimmers like a tiny piece of green metal. It bores neat tunnels into soft wood to build its nest.</p>
        <span class="nb-bee-card-credit">Photo: drickett on iNaturalist</span>
      </div>
    </div>

    <!-- 5 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/tetragonulacarbonaria.jpg' | relative_url }}" alt="Sugarbag bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Sugarbag bee</span>
        <span class="nb-bee-card-sciname">Tetragonula carbonaria</span>
        <p class="nb-bee-card-fact">One of the few native bees that actually makes honey — and it's delicious. Indigenous Australians have harvested sugarbag honey for thousands of years.</p>
        <span class="nb-bee-card-credit">Photo: katsinabox on iNaturalist</span>
      </div>
    </div>

    <!-- 6 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/amegillacingulata.jpg' | relative_url }}" alt="Blue-banded bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Blue-banded bee</span>
        <span class="nb-bee-card-sciname">Amegilla cingulata</span>
        <p class="nb-bee-card-fact">Famous for buzz-pollination — it grabs flowers and vibrates so fast (350 times per second!) that the pollen shakes right out. Tomato farmers love these bees.</p>
        <span class="nb-bee-card-credit">Photo: jenny_thynne on iNaturalist</span>
      </div>
    </div>

    <!-- 7 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/megachilemystaceana.jpg' | relative_url }}" alt="Fire-tailed resin bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Fire-tailed resin bee</span>
        <span class="nb-bee-card-sciname">Megachile mystaceana</span>
        <p class="nb-bee-card-fact">Instead of leaves or mud, resin bees collect sticky plant sap to build the walls of their nests. Some mix in sand, bark, or even flower petals to get exactly the right texture.</p>
        <span class="nb-bee-card-credit">Photo: pennytaylor on iNaturalist</span>
      </div>
    </div>

    <!-- 8 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/hylaeusnubilosus.jpg' | relative_url }}" alt="Masked bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Masked bee</span>
        <span class="nb-bee-card-sciname">Hylaeus nubilosus</span>
        <p class="nb-bee-card-fact">Wasp-like and nearly hairless. No fur, no pollen baskets — masked bees swallow pollen to carry it home in their stomach and regurgitate it into their nest cells.</p>
        <span class="nb-bee-card-credit">Photo: sockrosma on iNaturalist</span>
      </div>
    </div>

    <!-- 9 -->
    <div class="nb-bee-card">
      <div class="nb-bee-card-img-wrap">
        <img class="nb-bee-card-img" src="{{ 'assets/img/lasioglossumhemichalceum.jpg' | relative_url }}" alt="Sweat bee" loading="lazy">
      </div>
      <div class="nb-bee-card-body">
        <span class="nb-bee-card-name">Sweat bee</span>
        <span class="nb-bee-card-sciname">Lasioglossum hemichalceum</span>
        <p class="nb-bee-card-fact">Sometimes called ‘sweat bees’ because they’re attracted to the salts in human sweat, which they collect as a mineral source.</p>
        <span class="nb-bee-card-credit">Photo: rewildingsuburbia on iNaturalist</span>
      </div>
    </div>

  </div>
</section>

<!-- WORKSHOPS -->
<section class="nb-section nb-reveal">
  <div class="nb-section-header">

    <h2 class="nb-section-title">Workshops</h2>
  </div>
  <div class="nb-workshops-grid">
    <div class="nb-workshop-card">
      <img src="{{ 'assets/img/beehotel.jpg' | relative_url }}" alt="Native bee hotel made from natural materials">
      <div class="nb-workshop-content">
        <span class="nb-workshop-tag">Workshop 01</span>
        <h3>Build a bee hotel</h3>
        <p>Bundle up hollow sticks and bamboo to make a home for solitary bees. They'll move in, lay eggs, and raise their young — right in your backyard.</p>
      </div>
    </div>
    <div class="nb-workshop-card">
      <img src="{{ 'assets/img/seedbombs.jpg' | relative_url }}" alt="Native flower seed bombs">
      <div class="nb-workshop-content">
        <span class="nb-workshop-tag">Workshop 02</span>
        <h3>Make seed bombs</h3>
        <p>Mix clay, soil, and native flower seeds into a ball — then throw it at a patch of bare dirt. Water it and wait. A bee garden grows from a lump of mud.</p>
      </div>
    </div>
  </div>
</section>

<!-- INSTRUCTIONS -->
<section class="nb-instructions nb-reveal">
  <div class="nb-section-header">

    <h2 class="nb-section-title">How to use your workshop kit</h2>
    <p class="nb-instructions-sub">Simple steps to get the best out of your bee hotel and seed bombs.</p>
  </div>
  <div class="nb-instructions-grid">

    <div>
      <div class="nb-inst-header">
        <p class="nb-inst-label">Bee Hotel</p>
        <h3>Setting up your hotel</h3>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">1</span>
        <div class="nb-step-body">
          <strong>Choose a sheltered, dry spot under cover</strong>
          <p>Find a location like a verandah or under a tree branch that protects the hotel from rain and harsh weather.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">2</span>
        <div class="nb-step-body">
          <strong>Position 1–2 metres above ground, facing east or north-east</strong>
          <p>This height keeps the hotel safe from ground predators and the eastern orientation provides gentle morning sun.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">3</span>
        <div class="nb-step-body">
          <strong>Make sure the hotel is secured tightly</strong>
          <p>The structure shouldn't wobble or swing in the wind, as this can disturb nesting bees.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">4</span>
        <div class="nb-step-body">
          <strong>Do not attempt to open, shake, or disassemble the hotel</strong>
          <p>Once installed, leave it undisturbed so the bees can nest peacefully and complete their life cycle.</p>
        </div>
      </div>
    </div>

    <div>
      <div class="nb-inst-header">
        <p class="nb-inst-label">Seed Bomb</p>
        <h3>Planting your seed bomb</h3>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">1</span>
        <div class="nb-step-body">
          <strong>Choose a bare soil spot in your garden or use a pot</strong>
          <p>Avoid planting in established grasses so seedlings don't have to compete for space and nutrients.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">2</span>
        <div class="nb-step-body">
          <strong>Place the seed bomb on the soil surface or press in lightly</strong>
          <p>Don't bury it deeply — the seeds need access to light and air to germinate properly.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">3</span>
        <div class="nb-step-body">
          <strong>Water well and don't let dry out once germinating</strong>
          <p>Keep the soil consistently moist but not waterlogged during the germination period.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">4</span>
        <div class="nb-step-body">
          <strong>Water well if steady rainfall is not forecast</strong>
          <p>Until plants are established, try to allow soil to semi-dry between waterings to encourage deep root growth.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">5</span>
        <div class="nb-step-body">
          <strong>Best used within 6 months</strong>
          <p>Seed viability decreases over time, so plant your seed bombs relatively soon after receiving them.</p>
        </div>
      </div>
    </div>

    <div class="nb-seed-species">
      <h4>Native flowers in your seed bomb</h4>
      <div class="nb-seed-tags">
        <span class="nb-seed-tag">Golden cluster everlasting</span>
        <span class="nb-seed-tag">Swan River daisy</span>
        <span class="nb-seed-tag">Pink &amp; white everlasting daisy</span>
        <span class="nb-seed-tag">Dwarf strawflower</span>
        <span class="nb-seed-tag">Billy buttons</span>
        <span class="nb-seed-tag">Red &amp; yellow kangaroo paw</span>
        <span class="nb-seed-tag">Blue lace flower</span>
        <span class="nb-seed-tag">Native wisteria</span>
        <span class="nb-seed-tag">Coral creeper</span>
        <span class="nb-seed-tag">Ashburton pea</span>
      </div>
    </div>

  </div>
</section>

<!-- LINKS -->
<section class="nb-links nb-reveal">
  <h3 class="nb-links-heading"><em>Learn more</em></h3>
  <ul class="nb-links-list">
    <li>
      <a href="https://www.aussiebee.com.au/beesinyourarea.html/" target="_blank" rel="noopener">
        Which native bees live in your area? — Aussie Bees
        <span class="nb-link-arrow">→</span>
      </a>
    </li>
    <li>
      <a href="https://www.krg.nsw.gov.au/Environment/Your-local-environment/Wildlife/Living-with-wildlife/Bee-hotels" target="_blank" rel="noopener">
        Bee hotels — Ku-ring-gai Council
        <span class="nb-link-arrow">→</span>
      </a>
    </li>
    <li>
      <a href="https://www.inaturalist.org/projects/australian-native-bees-nsw-and-act" target="_blank" rel="noopener">
        Australian Native Bees - iNaturalist
        <span class="nb-link-arrow">→</span>
      </a>
    </li>
  </ul>
</section>

</div><!-- end .nb-page -->

<script>
(function() {
  var obs = new IntersectionObserver(function(entries) {
    entries.forEach(function(e) {
      if (e.isIntersecting) { e.target.classList.add('nb-in'); obs.unobserve(e.target); }
    });
  }, { threshold: 0.08 });
  document.querySelectorAll('.nb-reveal').forEach(function(el) { obs.observe(el); });
})();
</script>
