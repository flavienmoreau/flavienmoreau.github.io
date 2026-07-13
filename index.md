---
layout: default
title: Home
---

<section class="hero">
  <img class="portrait" src="{{ '/assets/img/portrait.svg' | relative_url }}" alt="{{ site.author.name }}">
  <h1>{{ site.author.name }}</h1>
  <!-- <p class="role">{{ site.author.role }}, {{ site.author.affiliation }}</p> -->
  <div class="bio">
    <p>I am a macroeconomist with broad interests that intersect firm dynamics, development, demography, climate finance, and competition policy. My work has been covered by <a href="https://www.economist.com/the-americas/2024/06/13/why-latin-america-is-the-worlds-trade-pipsqueak">The Economist</a>, BBC, <a href="{{ '/assets/press/NZZ_am_Sonntag_2025-09-28.pdf' | relative_url }}">NZZ</a>, Reuters, Bloomberg, and the Financial Times.</p>
    <p> I work in the Macroeconomic Development Division at the International Monetary Fund's Research Department. In earlier assignments at the Fund, I covered a broad range of economies, including the Democratic Republic of the Congo, Saudi Arabia, as well Latin American countries and Small Island States. I received my Ph.D. in Economics from the University of California, Los Angeles in 2019, and degrees in mathematical economics from the London School of Economics and engineering from the École des Ponts.</p>
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
<div style="margin-top:48px;padding-top:20px;border-top:1px solid var(--rule);">
  <p style="font-size:.82rem;color:var(--muted);line-height:1.55;margin:0;">The views expressed on this website are those of the author and do not necessarily represent the views of the IMF, its Executive Board, or IMF management.</p>
</div>
