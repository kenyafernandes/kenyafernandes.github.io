---
layout: page
title: People
permalink: /people/
description: Current and past lab members.
nav: true
nav_order: 5
display_categories: [current, past]
horizontal: false
---

<div class="people">
  {% assign current_people = site.data.people | where: "tag", "current" %}
  {% assign past_people = site.data.people | where: "tag", "past" %} 

  <!-- Current Section -->
  <a id="current" href=".#current">
    <h2 class="category" style="font-size: 22px; color: grey; margin-bottom: 20px;">Current</h2>
  </a>
  <div class="team-list current row row-cols-1 row-cols-md-3 g-4">
    {% for person in current_people %}
      <div class="col">
        <div class="team-member card h-100 text-center p-3 shadow-sm">
          <img src="{{ person.image }}" alt="{{ person.name }}" class="rounded-circle mb-3" style="width:150px; height:150px; object-fit:cover;">
          <h3 class="card-title" style="font-size: 18px;">{{ person.name }}</h3>
          <p class="role text-muted">{{ person.role }}</p>

          {% if person.project %}
            <p class="card-text"><strong>Project:</strong> {{ person.project }}</p>
          {% endif %}

          {% if person.supervisors %}
            <p class="card-text"><strong>Supervisors:</strong> {{ person.supervisors }}</p>
          {% endif %}

          {% if person.bio %}
            <p class="card-text">{{ person.bio }}</p>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>

  <!-- Past Section -->
  <a id="past" href=".#past">
    <h2 class="category" style="font-size: 22px; color: grey; margin-top:40px; margin-bottom: 20px;">Past</h2>
  </a>
  <div class="team-list past row row-cols-1 row-cols-md-3 g-4">
    {% for person in past_people %}
      <div class="col">
        <div class="team-member card h-100 text-center p-3 shadow-sm">
          <img src="{{ person.image }}" alt="{{ person.name }}" class="rounded-circle mb-3" style="width:150px; height:150px; object-fit:cover;">
          <h3 class="card-title" style="font-size: 18px;">{{ person.name }}</h3>
          <p class="role text-muted">{{ person.role }}</p>

          {% if person.project %}
            <p class="card-text"><strong>Project:</strong> {{ person.project }}</p>
          {% endif %}

          {% if person.supervisors %}
            <p class="card-text"><strong>Supervisors:</strong> {{ person.supervisors }}</p>
          {% endif %}

          {% if person.bio %}
            <p class="card-text">{{ person.bio }}</p>
          {% endif %}
        </div>
      </div>
    {% endfor %}
  </div>
</div>
