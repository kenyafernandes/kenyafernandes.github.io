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
  <h2 class="category" style="font-size: 20px; color: grey;">Current</h2>
</a>
<div class="team-list current">
  <div class="row row-cols-1 row-cols-md-3">
    {% for person in current_people %}
      <div class="team-member">
        <img src="{{ person.image }}" alt="{{ person.name }}" style="width: 150px; height: 150px; object-fit: cover; margin-bottom: 15px;">
        <h3 style="font-size: 16px; font-weight: normal;">{{ person.name }}</h3> <!-- Reduced font size for name -->
        <p class="role">{{ person.role }}</p>
        <p>{{ person.bio }}</p>
      </div>
    {% endfor %}
  </div>
</div>



<!-- Past Section -->
<a id="past" href=".#past">
  <h2 class="category" style="font-size: 20px; color: grey;">Past</h2>
</a>
<div class="team-list past">
  <div class="row row-cols-1 row-cols-md-3">
    {% for person in past_people %}
      <div class="team-member">
      <img src="{{ person.image }}" alt="{{ person.name }}" style="width: 150px; height: 150px; object-fit: cover; margin-bottom: 15px;">
        <h3 style="font-size: 16px; font-weight: normal;">{{ person.name }}</h3> <!-- Reduced font size for name -->
        <p class="role">{{ person.role }}</p>
        <p>{{ person.bio }}</p>
      </div>
    {% endfor %}
  </div>
</div>
