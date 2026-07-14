---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% if site.author.googlescholar %}
<p class="pub-scholar-link">You can also find my papers on <a href="{{ site.author.googlescholar }}">my Google Scholar profile</a>.</p>
{% endif %}

<div class="pub-area-nav">
  <a href="#fairness">Algorithmic Fairness &amp; AI Evaluation</a>
  <a href="#law">AI &amp; the Law / Governance</a>
  <a href="#deployments">AI Deployments on the Ground</a>
</div>

{% assign areas = "fairness|Algorithmic Fairness & AI Evaluation,law|AI & the Law / Governance,deployments|Learning from AI Deployments on the Ground" | split: "," %}
{% for area_pair in areas %}
  {% assign parts = area_pair | split: "|" %}
  {% assign area_key = parts[0] %}
  {% assign area_title = parts[1] %}
  <h2 id="{{ area_key }}" class="pub-area-title">{{ area_title }}</h2>
  {% assign area_pubs = site.data.publications | where: "area", area_key | sort: "year" | reverse %}
  {% for pub in area_pubs %}
    {% include publication-entry.html %}
  {% endfor %}
{% endfor %}
