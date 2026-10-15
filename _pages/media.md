---
layout: page
permalink: /media/
title: media
nav: true
nav_order: 3
description: Test
media:
  - date: 2026-03-12
    title: "Electrodes partially restore movement, sensation in spinal cord patients"
    outlet: Powers Health
    url: https://www.powershealth.org/about-us/newsroom/health-library/2026/03/12/electrodes-partially-restore-movement-sensation-in-spinal-cord-patients
  - date: 2026-03-11
    title: "Electrical stimulation can restore ability to move limbs"
    outlet: Brown University News
    url: https://www.brown.edu/news/2026-03-11/spinal-cord-stimulation
  - date: 2021-09-28
    title: "Carney Graduate Fellowship Award"
    outlet: Carney Institute for Brain Science
    url: https://carney.brown.edu/news/2021-09-28/gradawards
  - date: 2021-04-20
    title: "Presidential Award for Excellence in Teaching"
    outlet: Brown University Graduate School
    url: https://graduateschool.brown.edu/news/2021-04-20/lakshmi-govindarajan
---

{% assign items = page.media | sort: "date" | reverse %}
{% assign current_year = "" %}

{% for item in items %}
  {% assign year = item.date | date: "%Y" %}
  {% if year != current_year %}
    {% unless forloop.first %}</ul>{% endunless %}
<h2 class="year">{{ year }}</h2>
<ul class="list-unstyled">
    {% assign current_year = year %}
  {% endif %}
  <li class="mb-3">
    <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer"><strong>{{ item.title }}</strong></a><br>
    <span class="text-muted">{{ item.outlet }} · {{ item.date | date: "%B %-d, %Y" }}</span>
  </li>
  {% if forloop.last %}</ul>{% endif %}
{% endfor %}