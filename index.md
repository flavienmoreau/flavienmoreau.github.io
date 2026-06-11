---
layout: default
title: Home
---

<section class="hero">
  <img class="portrait" src="{{ '/assets/img/portrait.svg' | relative_url }}" alt="{{ site.author.name }}">
  <h1>{{ site.author.name }}</h1>
  <p class="role">{{ site.author.role }}, {{ site.author.affiliation }}</p>
  <div class="bio">
    <p>I am an economist working on [your fields — e.g. macroeconomics, international finance, monetary policy]. [One or two sentences on your main research agenda and the questions you care about.]</p>
    <p>I received my PhD in Economics from [University] in [year]. Here is my <a href="{{ site.social.cv | relative_url }}">CV</a> and my <a href="{{ '/research/' | relative_url }}">research</a>.</p>
  </div>
</section>

<section class="section">
  <h2>News</h2>
  {% for item in site.data.news %}
  <div class="entry">
    <span class="date">{{ item.date }}</span>
    <div>{{ item.html }}</div>
  </div>
  {% endfor %}
</section>

<section class="section">
  <h2>Contact</h2>
  <div class="contact">
    <p>{{ site.author.affiliation }}<br>[Address line]<br>[City, Country]</p>
    <p><a href="mailto:{{ site.email }}">{{ site.email }}</a></p>
    {% include social.html %}
  </div>
</section>
