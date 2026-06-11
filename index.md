---
layout: default
title: Home
---

<section class="hero">
  <img class="portrait" src="{{ '/assets/img/portrait.svg' | relative_url }}" alt="{{ site.author.name }}">
  <h1>{{ site.author.name }}</h1>
  <p class="role">{{ site.author.role }}, {{ site.author.affiliation }}</p>
  <div class="bio">
    <p>I am a researcher at the International Monetary Fund's Research Department working on macroeconomic development. My main research interests include firm dynamics, demography, and competition policy. My work has been covered by The Economist, BBC, <a href="{{ '/assets/press/NZZ_am_Sonntag_2025-09-28.pdf' | relative_url }}">NZZ</a>, Reuters, Bloomberg, and the Financial Times.</p>
    <p>In earlier assignments at the Fund, I covered the Democratic Republic of the Congo, Saudi Arabia, as well as regional issues in the Eastern Caribbean and Latin American countries. I received my Ph.D. in Economics from the University of California, Los Angeles in 2019, and degrees in mathematical economics from the London School of Economics and engineering from the École des Ponts.</p>
    {% include social.html %}
  </div>
</section>

<section class="section">
  <h2>New</h2>
  {% for item in site.data.news %}
  <div class="entry">
    <span class="date">{{ item.date }}</span>
    <div>{{ item.html }}</div>
  </div>
  {% endfor %}
</section>
