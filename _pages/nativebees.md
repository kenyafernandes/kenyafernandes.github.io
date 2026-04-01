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

/* ── SPECIES ── */
.nb-species-grid {
  display: grid;
  grid-template-columns: 1.25fr 1fr 1.1fr;
  gap: 1.75rem;
  align-items: end;
}
.nb-species-card:nth-child(2) { margin-bottom: 3rem; }
.nb-species-card:nth-child(3) { margin-bottom: 1.25rem; }
.nb-species-img { overflow: hidden; display: block; }
.nb-species-img img {
  width: 100%;
  aspect-ratio: 4/3;
  object-fit: cover;
  display: block;
  filter: saturate(0.88) contrast(1.06);
  transition: transform 0.6s ease, filter 0.4s ease;
}
.nb-species-img:hover img { transform: scale(1.03); filter: saturate(1) contrast(1.04); }
.nb-species-meta { padding: 0.6rem 0 0; }
.nb-species-name {
  font-family: 'DM Serif Display', Georgia, serif;
  font-style: italic;
  font-size: 0.98rem;
  color: var(--nb-forest);
  display: block;
}
.nb-species-credit {
  font-family: 'DM Sans', sans-serif;
  font-size: 0.73rem;
  color: var(--nb-muted);
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
.nb-seed-list { list-style: none; display: flex; flex-wrap: wrap; column-gap: 2rem; row-gap: 0.35rem; padding: 0; margin: 0; }
.nb-seed-list li {
  font-family: 'Lora', Georgia, serif;
  font-size: 0.86rem;
  font-style: italic;
  color: rgba(183,210,175,0.9);
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.nb-seed-list li::before { content: ''; width: 4px; height: 4px; background: var(--nb-honey-light); border-radius: 50%; flex-shrink: 0; }

/* ── FACTS ── */
.nb-facts-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1px;
  background: var(--nb-rule);
  border: 1px solid var(--nb-rule);
  margin-top: 2.75rem;
}
.nb-fact-card { background: var(--nb-cream); padding: 2.25rem 1.75rem; transition: background 0.3s; }
.nb-fact-card:hover { background: var(--nb-parchment); }
.nb-fact-marker { width: 34px; height: 34px; background: var(--nb-honey); display: flex; align-items: center; justify-content: center; margin-bottom: 1.35rem; }
.nb-fact-marker svg { width: 16px; height: 16px; }
.nb-fact-card h4 {
  font-family: 'DM Serif Display', Georgia, serif !important;
  font-size: 1.1rem !important;
  color: var(--nb-forest) !important;
  margin-bottom: 0.65rem !important;
  line-height: 1.25 !important;
  font-weight: 400 !important;
}
.nb-fact-card p { font-size: 0.87rem; color: var(--nb-muted); line-height: 1.7; margin: 0; }

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
  .nb-species-grid { grid-template-columns: 1fr 1fr; }
  .nb-species-card:nth-child(2), .nb-species-card:nth-child(3) { margin-bottom: 0; }
  .nb-why { grid-template-columns: 1fr; padding: 3rem 1.5rem; gap: 2.25rem; margin: 0 -10px; }
  .nb-pull-quote { position: static; }
  .nb-workshops-grid { grid-template-columns: 1fr; }
  .nb-instructions { padding: 3rem 1.5rem; margin: 0 -10px; }
  .nb-instructions-grid { grid-template-columns: 1fr; gap: 2.5rem; }
  .nb-seed-species { grid-column: 1; }
  .nb-facts-grid { grid-template-columns: 1fr; gap: 0; background: transparent; border: none; }
  .nb-fact-card { border-bottom: 1px solid var(--nb-rule); }
  .nb-links { grid-template-columns: 1fr; padding: 3rem 1.5rem; margin: 0 -10px; gap: 2rem; }
}
</style>

<div class="nb-page">

<!-- HERO -->
<section class="nb-hero">
  <div class="nb-hero-bg"></div>
  <div class="nb-hero-text">
    <p class="nb-eyebrow"> </p>
    <h1>The World of<br><em>Native Bees</em></h1>
    <p class="nb-hero-sub">Building homes, planting gardens, and protecting the extraordinary pollinators that hold our ecosystems together.</p>
  </div>
  <div class="nb-hero-bee">
    <svg width="260" height="260" viewBox="0 0 320 320" fill="none" xmlns="http://www.w3.org/2000/svg">
      <g class="nb-bee-group">
        <g class="nb-wing-top">
          <ellipse cx="115" cy="130" rx="52" ry="26" fill="rgba(240,232,208,0.18)" stroke="rgba(212,145,32,0.5)" stroke-width="1.5"/>
          <ellipse cx="205" cy="130" rx="52" ry="26" fill="rgba(240,232,208,0.18)" stroke="rgba(212,145,32,0.5)" stroke-width="1.5"/>
        </g>
        <g class="nb-wing-bot">
          <ellipse cx="118" cy="152" rx="38" ry="18" fill="rgba(240,232,208,0.12)" stroke="rgba(212,145,32,0.35)" stroke-width="1"/>
          <ellipse cx="202" cy="152" rx="38" ry="18" fill="rgba(240,232,208,0.12)" stroke="rgba(212,145,32,0.35)" stroke-width="1"/>
        </g>
        <ellipse cx="160" cy="188" rx="44" ry="54" fill="#3A6B4F" stroke="#1B3527" stroke-width="2"/>
        <path d="M116 178 Q160 172 204 178 Q204 188 204 188 Q160 182 116 188 Z" fill="#D49120" opacity="0.9"/>
        <path d="M117 200 Q160 194 203 200 Q203 210 203 210 Q160 204 117 210 Z" fill="#D49120" opacity="0.9"/>
        <path d="M138 228 Q160 244 182 228" stroke="#1B3527" stroke-width="1.5" fill="none"/>
        <ellipse cx="160" cy="150" rx="26" ry="20" fill="#275238" stroke="#1B3527" stroke-width="2"/>
        <path d="M144 147 Q150 142 160 143 Q170 142 176 147" stroke="rgba(212,145,32,0.5)" stroke-width="1" fill="none"/>
        <circle cx="160" cy="126" r="18" fill="#275238" stroke="#1B3527" stroke-width="2"/>
        <circle cx="153" cy="123" r="4.5" fill="#D49120" opacity="0.9"/>
        <circle cx="167" cy="123" r="4.5" fill="#D49120" opacity="0.9"/>
        <circle cx="153" cy="122" r="2" fill="#1B3527"/>
        <circle cx="167" cy="122" r="2" fill="#1B3527"/>
        <path d="M154 109 Q148 92 138 85" stroke="rgba(212,145,32,0.8)" stroke-width="1.5" fill="none" stroke-linecap="round"/>
        <path d="M166 109 Q172 92 182 85" stroke="rgba(212,145,32,0.8)" stroke-width="1.5" fill="none" stroke-linecap="round"/>
        <circle cx="137" cy="84" r="3.5" fill="#D49120"/>
        <circle cx="183" cy="84" r="3.5" fill="#D49120"/>
      </g>
      <g opacity="0.4">
        <circle cx="58" cy="72" r="5" fill="#D49120" opacity="0.6"/>
        <circle cx="48" cy="66" r="4" fill="#3A6B4F" opacity="0.5"/>
        <circle cx="68" cy="66" r="4" fill="#3A6B4F" opacity="0.5"/>
        <circle cx="48" cy="78" r="4" fill="#3A6B4F" opacity="0.5"/>
        <circle cx="68" cy="78" r="4" fill="#3A6B4F" opacity="0.5"/>
        <path d="M58 77 Q55 90 52 100" stroke="#3A6B4F" stroke-width="1.5" fill="none" stroke-linecap="round"/>
        <circle cx="258" cy="240" r="5" fill="#D49120" opacity="0.6"/>
        <circle cx="248" cy="234" r="4" fill="#3A6B4F" opacity="0.5"/>
        <circle cx="268" cy="234" r="4" fill="#3A6B4F" opacity="0.5"/>
        <circle cx="248" cy="246" r="4" fill="#3A6B4F" opacity="0.5"/>
        <circle cx="268" cy="246" r="4" fill="#3A6B4F" opacity="0.5"/>
      </g>
    </svg>
  </div>
</section>

<!-- SPECIES -->
<section class="nb-section nb-reveal">
  <div class="nb-section-header">
    <p class="nb-section-eyebrow">Australia's Native Pollinators</p>
    <h2 class="nb-section-title">Meet the <em>species</em></h2>
  </div>
  <div class="nb-species-grid">
    <div class="nb-species-card">
      <span class="nb-species-img">
        <img src="{{ 'assets/img/amegilla.jpg' | relative_url }}" alt="Amegilla bombiformis - teddy bear bee" loading="lazy">
      </span>
      <div class="nb-species-meta">
        <span class="nb-species-name">Amegilla bombiformis</span>
        <span class="nb-species-credit">Photo: notesafield</span>
      </div>
    </div>
    <div class="nb-species-card">
      <span class="nb-species-img">
        <img src="{{ 'assets/img/thyreus.jpg' | relative_url }}" alt="Thyreus nitidulus - neon cuckoo bee" loading="lazy">
      </span>
      <div class="nb-species-meta">
        <span class="nb-species-name">Thyreus nitidulus</span>
        <span class="nb-species-credit">Photo: Dianne Clarke</span>
      </div>
    </div>
    <div class="nb-species-card">
      <span class="nb-species-img">
        <img src="{{ 'assets/img/megachile.jpg' | relative_url }}" alt="Megachile aurifons - leafcutter bee" loading="lazy">
      </span>
      <div class="nb-species-meta">
        <span class="nb-species-name">Megachile aurifons</span>
        <span class="nb-species-credit">Photo: maxhr54</span>
      </div>
    </div>
  </div>
</section>

<!-- WORKSHOPS -->
<section class="nb-section nb-reveal">
  <div class="nb-section-header">
    <p class="nb-section-eyebrow">Hands-on Learning</p>
    <h2 class="nb-section-title">Workshops</h2>
  </div>
  <div class="nb-workshops-grid">
    <div class="nb-workshop-card">
      <img src="{{ 'assets/img/beehotel.jpg' | relative_url }}" alt="Native bee hotel made from natural materials">
      <div class="nb-workshop-content">
        <span class="nb-workshop-tag">Workshop 01</span>
        <h3>Build a Native Bee Hotel</h3>
        <p>Create cozy homes for native bees using natural materials like bamboo and hollow stems. These hotels give solitary bees safe places to lay their eggs and complete their remarkable life cycle.</p>
      </div>
    </div>
    <div class="nb-workshop-card">
      <img src="{{ 'assets/img/seedbombs.jpg' | relative_url }}" alt="Native flower seed bombs">
      <div class="nb-workshop-content">
        <span class="nb-workshop-tag">Workshop 02</span>
        <h3>Make Native Seed Bombs</h3>
        <p>Mix clay, soil, and native flower seeds to create seed bombs that grow into beautiful, bee-friendly gardens. A simple, tactile craft with a lasting impact on your local ecosystem.</p>
      </div>
    </div>
  </div>
</section>

<!-- INSTRUCTIONS -->
<section class="nb-instructions nb-reveal">
  <div class="nb-section-header">
    <p class="nb-section-eyebrow">Field Guide</p>
    <h2 class="nb-section-title">How to use your workshop kit</h2>
    <p class="nb-instructions-sub">A practical guide to getting the best results from your bee hotel and seed bombs.</p>
  </div>
  <div class="nb-instructions-grid">

    <div>
      <div class="nb-inst-header">
        <p class="nb-inst-label">Bee Hotel</p>
        <h3>Installing your hotel</h3>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">1</span>
        <div class="nb-step-body">
          <strong>Choose a sheltered, dry spot under cover</strong>
          <p>A verandah or under a tree branch works well — anything that shields the hotel from rain and harsh weather.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">2</span>
        <div class="nb-step-body">
          <strong>Position 1–2 metres above ground, facing east or north-east</strong>
          <p>This height protects from ground predators; the eastern orientation provides warming morning sun.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">3</span>
        <div class="nb-step-body">
          <strong>Secure tightly — no wobbling</strong>
          <p>The structure shouldn't swing in the wind, as movement disturbs nesting bees.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">4</span>
        <div class="nb-step-body">
          <strong>Leave it undisturbed</strong>
          <p>Don't open, shake, or disassemble the hotel once installed. Let the bees nest peacefully through their full life cycle.</p>
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
          <strong>Choose bare soil or a pot</strong>
          <p>Avoid established grasses — seedlings shouldn't have to compete for space and nutrients.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">2</span>
        <div class="nb-step-body">
          <strong>Place on the surface or press in lightly</strong>
          <p>Don't bury it deeply — seeds need access to light and air to germinate properly.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">3</span>
        <div class="nb-step-body">
          <strong>Water well and keep moist while germinating</strong>
          <p>Consistently moist but not waterlogged during the germination period.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">4</span>
        <div class="nb-step-body">
          <strong>Allow semi-drying once established</strong>
          <p>Let the soil semi-dry between waterings to encourage deep root growth.</p>
        </div>
      </div>
      <div class="nb-step">
        <span class="nb-step-num">5</span>
        <div class="nb-step-body">
          <strong>Best used within 6 months</strong>
          <p>Seed viability decreases over time — plant your bombs relatively soon after receiving them.</p>
        </div>
      </div>
    </div>

    <div class="nb-seed-species">
      <h4>Native flower species in your seed bomb</h4>
      <ul class="nb-seed-list">
        <li>Golden Cluster Everlasting</li>
        <li>Swan River Daisy</li>
        <li>Pink &amp; White Everlasting Daisy</li>
        <li>Dwarf Strawflower</li>
        <li>Billy Buttons</li>
        <li>Red &amp; Yellow Kangaroo Paw</li>
        <li>Blue Lace Flower</li>
        <li>Native Wisteria</li>
        <li>Coral Creeper</li>
        <li>Ashburton Pea</li>
      </ul>
    </div>

  </div>
</section>

<!-- FACTS -->
<section class="nb-section nb-reveal">
  <div class="nb-section-header">
    <p class="nb-section-eyebrow">Natural History</p>
    <h2 class="nb-section-title">Remarkable bee <em>facts</em></h2>
  </div>
  <div class="nb-facts-grid">
    <div class="nb-fact-card">
      <div class="nb-fact-marker">
        <svg viewBox="0 0 24 24" fill="none" stroke="#FAF6ED" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
          <path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/>
        </svg>
      </div>
      <h4>Tiny Architects</h4>
      <p>Native bees build extraordinary nests in hollow stems, holes in wood, and underground burrows — each species with its own ingenious construction method.</p>
    </div>
    <div class="nb-fact-card">
      <div class="nb-fact-marker">
        <svg viewBox="0 0 24 24" fill="none" stroke="#FAF6ED" stroke-width="2" stroke-linecap="round">
          <circle cx="12" cy="12" r="10"/>
          <path d="M8.56 2.75c4.37 6.03 6.02 9.42 8.03 17.72m2.54-15.38c-3.72 4.35-8.94 5.66-16.88 5.85m19.5 1.9c-3.5-.93-6.63-.82-8.94 0-2.58.92-5.01 2.86-7.44 6.32"/>
        </svg>
      </div>
      <h4>Buzz Pollination</h4>
      <p>Some native bees are specialist "buzz pollinators" — they grip flowers and vibrate their flight muscles at a precise frequency, shaking loose pollen other insects can't reach.</p>
    </div>
    <div class="nb-fact-card">
      <div class="nb-fact-marker">
        <svg viewBox="0 0 24 24" fill="none" stroke="#FAF6ED" stroke-width="2" stroke-linecap="round">
          <circle cx="12" cy="12" r="5"/>
          <line x1="12" y1="1" x2="12" y2="3"/><line x1="12" y1="21" x2="12" y2="23"/>
          <line x1="4.22" y1="4.22" x2="5.64" y2="5.64"/><line x1="18.36" y1="18.36" x2="19.78" y2="19.78"/>
          <line x1="1" y1="12" x2="3" y2="12"/><line x1="21" y1="12" x2="23" y2="12"/>
          <line x1="4.22" y1="19.78" x2="5.64" y2="18.36"/><line x1="18.36" y1="5.64" x2="19.78" y2="4.22"/>
        </svg>
      </div>
      <h4>A Rainbow of Colours</h4>
      <p>Native bees come in spectacular colours — metallic green, electric blue, fuzzy orange, and intricate stripes. Australia's 2,000+ species are among the world's most diverse.</p>
    </div>
  </div>
</section>

<!-- LINKS -->
<section class="nb-links nb-reveal">
  <h3 class="nb-links-heading">Go deeper —<br><em>learn more</em></h3>
  <ul class="nb-links-list">
    <li>
      <a href="https://www.aussiebee.com.au/beesinyourarea.html/" target="_blank" rel="noopener">
        Which native bees are in your area? — Aussie Bees
        <span class="nb-link-arrow">→</span>
      </a>
    </li>
    <li>
      <a href="https://www.krg.nsw.gov.au/Environment/Your-local-environment/Wildlife/Living-with-wildlife/Bee-hotels" target="_blank" rel="noopener">
        Bee Hotels — Ku-ring-gai Council
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
