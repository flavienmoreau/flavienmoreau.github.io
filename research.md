---
layout: default
title: Research
---

<section class="hero" style="padding-bottom:0">
  <h1>Research</h1>
</section>

{% assign pubs = site.data.publications | sort: "year" | reverse %}

<section class="section">
  <h2>Publications &amp; working papers</h2>
  {% for p in pubs %}
  <div class="entry">
    <span class="date">{{ p.year }}</span>
    <div class="title">{{ p.title }}</div>
    <div class="meta">{{ p.authors }}{% if p.venue %} · <em>{{ p.venue }}</em>{% endif %}{% if p.status %} · {{ p.status }}{% endif %}</div>
    {% if p.abstract %}<div class="abstract">{{ p.abstract }}</div>{% endif %}
    {% if p.links %}<div class="links">{% for l in p.links %}<a href="{{ l.url }}">{{ l.text }}</a>{% endfor %}</div>{% endif %}
  </div>
  {% endfor %}
</section>
