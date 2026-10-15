---
layout: page
permalink: /media/
title: media
nav: true
nav_order: 4
description: Features and coverage in popular media.
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

<ul>
{% for item in items %}
  <li>
    <a href="{{ item.url }}" target="_blank" rel="noopener noreferrer">{{ item.title }}</a>
    <span class="text-muted">({{ item.outlet }}, {{ item.date | date: "%b %Y" }})</span>
  </li>
{% endfor %}
</ul>